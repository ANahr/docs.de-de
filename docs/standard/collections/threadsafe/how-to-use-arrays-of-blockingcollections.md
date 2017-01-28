---
title: 'Gewusst wie: Verwenden von Arrays mit blockierenden Auflistungen in einer Pipeline'
description: 'Gewusst wie: Verwenden von Arrays mit blockierenden Auflistungen in einer Pipeline'
keywords: .NET, .NET Core
author: mairaw
ms.author: mairaw
ms.date: 06/20/2016
ms.topic: article
ms.prod: .net
ms.technology: dotnet-standard
ms.devlang: dotnet
ms.assetid: 278a6566-09ba-4022-8802-e160e75b86af
translationtype: Human Translation
ms.sourcegitcommit: c15f2da15c6448cf1c36dea2d5fd53e734bb6608
ms.openlocfilehash: 4f637ea8985a2be9fc22b5ede88fc625864046dc

---

# <a name="how-to-use-arrays-of-blocking-collections-in-a-pipeline"></a>Gewusst wie: Verwenden von Arrays mit blockierenden Auflistungen in einer Pipeline

Das folgende Beispiel zeigt die Verwendung von [System.Collections.Concurrent.BlockingCollection&lt;T&gt;](https://docs.microsoft.com/dotnet/core/api/System.Collections.Concurrent.BlockingCollection-1)-Objektarrays mit statischen Methoden wie `TryAddToAny` und `TryTakeFromAny`, um eine schnelle und flexible Datenübertragung zwischen Komponenten zu implementieren. 

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht eine grundlegende Pipeline-Implementierung, in der alle Objekte gleichzeitig Daten aus der Eingabeauflistung entnehmen, sie transformieren und dann an die Ausgabeauflistung übergeben.

```csharp
using System;
using System.Collections.Concurrent;
using System.Linq;
using System.Threading;
using System.Threading.Tasks;


class PipeLineDemo
{
   public static void Main()
   {
      CancellationTokenSource cts = new CancellationTokenSource();

      // Start up a UI thread for cancellation.
      Task.Run(() =>
          {
              if(Console.ReadKey(true).KeyChar == 'c')
              {
                  cts.Cancel();
              }  
          });

      //Generate some source data.
      BlockingCollection<int>[] sourceArrays = new BlockingCollection<int>[5];
      for(int i = 0; i < sourceArrays.Length; i++)
          sourceArrays[i] = new BlockingCollection<int>(500);
      Parallel.For(0, sourceArrays.Length * 500, (j) =>
                          {
                              int k = BlockingCollection<int>.TryAddToAny(sourceArrays, j);
                              if(k >=0)
                                  Console.WriteLine("added {0} to source data", j);
                          });

      foreach (var arr in sourceArrays)
          arr.CompleteAdding();

      // First filter accepts the ints, keeps back a small percentage
      // as a processing fee, and converts the results to decimals.
      var filter1 = new PipelineFilter<int, decimal>
      (
          sourceArrays,
          (n) => Convert.ToDecimal(n * 0.97),
          cts.Token,
          "filter1"
       );

      // Second filter accepts the decimals and converts them to
      // System.Strings.
      var filter2 = new PipelineFilter<decimal, string>
      (
          filter1.m_output,
          (s) => String.Format("{0}", s),
          cts.Token,
          "filter2"
       );

      // Third filter uses the constructor with an Action<T>
      // that renders its output to the screen,
      // not a blocking collection.
      var filter3 = new PipelineFilter<string, string>
      (
          filter2.m_output,
          (s) => Console.WriteLine("The final result is {0}", s),
          cts.Token,
          "filter3"
       );

       // Start up the pipeline!
      try
      {
          Parallel.Invoke(
                       () => filter1.Run(),
                       () => filter2.Run(),
                       () => filter3.Run()
                   );
      }
      catch (AggregateException ae) 
      {
          foreach(var ex in ae.InnerExceptions)
              Console.WriteLine(ex.Message + ex.StackTrace);
      }
      finally 
      {
         cts.Dispose();
      }
      // You will need to press twice if you ran to the end:
      // once for the cancellation thread, and once for this thread.
      Console.WriteLine("Press any key.");
      Console.ReadKey(true);
  }

   class PipelineFilter<TInput, TOutput>
   {
      Func<TInput, TOutput> m_processor = null;
      public BlockingCollection<TInput>[] m_input;
      public BlockingCollection<TOutput>[] m_output = null;
      Action<TInput> m_outputProcessor = null;
      CancellationToken m_token;
      public string Name { get; private set; }

      public PipelineFilter(
          BlockingCollection<TInput>[] input,
          Func<TInput, TOutput> processor,
          CancellationToken token,
          string name)
          {
              m_input = input;
              m_output = new BlockingCollection<TOutput>[5];
              for (int i = 0; i < m_output.Length; i++)
              {
                    m_output[i] = new BlockingCollection<TOutput>(500);
              }      
              m_processor = processor;
              m_token = token;
              Name = name;
            }

      // Use this constructor for the final endpoint, which does
      // something like write to file or screen, instead of
      // pushing to another pipeline filter.
      public PipelineFilter(
          BlockingCollection<TInput>[] input,
          Action<TInput> renderer,
          CancellationToken token,
          string name)
          {
              m_input = input;
              m_outputProcessor = renderer;
              m_token = token;
              Name = name;
          }

      public void Run()
      {
          Console.WriteLine("{0} is running", this.Name);
          while (!m_input.All(bc => bc.IsCompleted) && !m_token.IsCancellationRequested)
          {
              TInput receivedItem;
              int i = BlockingCollection<TInput>.TryTakeFromAny(
                  m_input, out receivedItem, 50, m_token);
              if ( i >= 0)
              {
                  if (m_output != null) // we pass data to another blocking collection
                  {
                      TOutput outputItem = m_processor(receivedItem);
                      BlockingCollection<TOutput>.AddToAny(m_output, outputItem);
                      Console.WriteLine("{0} sent {1} to next", this.Name, outputItem);
                  }
                  else // we're an endpoint
                  {
                      m_outputProcessor(receivedItem);
                  }
              }
              else
              {
                  Console.WriteLine("Unable to retrieve data from previous filter");
              }
          }
          if (m_output != null)
          {
              foreach (var bc in m_output) bc.CompleteAdding();
          }
      }
   }
}
```

## <a name="see-also"></a>Siehe auch

[System.Collections.Concurrent](https://docs.microsoft.com/dotnet/core/api/System.Collections.Concurrent)

[Threadsichere Sammlungen](index.md)



<!--HONumber=Nov16_HO3-->


