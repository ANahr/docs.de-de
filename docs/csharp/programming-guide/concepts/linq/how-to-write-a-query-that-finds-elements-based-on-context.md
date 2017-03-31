---
title: 'Vorgehensweise: Schreiben einer Abfrage, die Elemente basierend auf dem Kontext sucht (C#) | Microsoft-Dokumentation'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 3ff79ef0-fc8b-42fe-8cc0-10dc32b06b4e
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: dbb188e8a043671c1a33a90fb95d10d6d86168bb
ms.lasthandoff: 03/13/2017


---
# <a name="how-to-write-a-query-that-finds-elements-based-on-context-c"></a>Vorgehensweise: Schreiben einer Abfrage, die Elemente basierend auf dem Kontext sucht (C#)
Es kann vorkommen, dass Sie eine Abfrage schreiben möchten, die Elemente auf der Grundlage ihres Kontexts sucht. Dabei soll die Filterung auf den vorausgehenden oder folgenden nebengeordneten Elementen erfolgen. Außerdem möchten Sie vielleicht auch nach untergeordneten oder indirekt übergeordneten Elementen filtern.  
  
 Um dies zu bewerkstelligen, können Sie eine Abfrage schreiben und die Ergebnisse dieser Abfrage in der `where`-Klausel verwenden. Wenn Sie zunächst eine Prüfung auf NULL-Werte vornehmen müssen und dann den Wert testen, empfiehlt es sich, die Abfrage in einer `let`-Klausel durchzuführen und die Ergebnisse dann in der `where`-Klausel zu verwenden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden alle `p`-Elemente ausgewählt, die sofort von einem `ul`-Element gefolgt werden.  
  
```csharp  
XElement doc = XElement.Parse(@"<Root>  
    <p id=""1""/>  
    <ul>abc</ul>  
    <Child>  
        <p id=""2""/>  
        <notul/>  
        <p id=""3""/>  
        <ul>def</ul>  
        <p id=""4""/>  
    </Child>  
    <Child>  
        <p id=""5""/>  
        <notul/>  
        <p id=""6""/>  
        <ul>abc</ul>  
        <p id=""7""/>  
    </Child>  
</Root>");  
  
IEnumerable<XElement> items =  
    from e in doc.Descendants("p")  
    let z = e.ElementsAfterSelf().FirstOrDefault()  
    where z != null && z.Name.LocalName == "ul"  
    select e;  
  
foreach (XElement e in items)  
    Console.WriteLine("id = {0}", (string)e.Attribute("id"));  
```  
  
 Dieser Code erzeugt die folgende Ausgabe:  
  
```  
id = 1  
id = 3  
id = 6  
```  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird dieselbe Abfrage für XML in einem Namespace gezeigt. Weitere Informationen finden Sie unter [Arbeiten mit XML-Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).  
  
```csharp  
XElement doc = XElement.Parse(@"<Root xmlns='http://www.adatum.com'>  
    <p id=""1""/>  
    <ul>abc</ul>  
    <Child>  
        <p id=""2""/>  
        <notul/>  
        <p id=""3""/>  
        <ul>def</ul>  
        <p id=""4""/>  
    </Child>  
    <Child>  
        <p id=""5""/>  
        <notul/>  
        <p id=""6""/>  
        <ul>abc</ul>  
        <p id=""7""/>  
    </Child>  
</Root>");  
  
XNamespace ad = "http://www.adatum.com";  
  
IEnumerable<XElement> items =  
    from e in doc.Descendants(ad + "p")  
    let z = e.ElementsAfterSelf().FirstOrDefault()  
    where z != null && z.Name == ad.GetName("ul")  
    select e;  
  
foreach (XElement e in items)  
    Console.WriteLine("id = {0}", (string)e.Attribute("id"));  
```  
  
 Dieser Code erzeugt die folgende Ausgabe:  
  
```  
id = 1  
id = 3  
id = 6  
```  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Xml.Linq.XElement.Parse%2A>   
 <xref:System.Xml.Linq.XContainer.Descendants%2A>   
 <xref:System.Xml.Linq.XNode.ElementsAfterSelf%2A>   
 <xref:System.Linq.Enumerable.FirstOrDefault%2A>   
 [Basic Queries (LINQ to XML) (C#) (Standardabfragen (LINQ to XML) (C#))](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
