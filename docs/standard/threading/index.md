---
title: Verwaltetes Threading
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], about threading
- managed threading
ms.assetid: 7b46a7d9-c6f1-46d1-a947-ae97471bba87
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c6447cd37e4718093acfb3a0e2db053c13a027d3
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147454"
---
# <a name="managed-threading"></a>Verwaltetes Threading
Unabhängig davon, ob eine Anwendung für einen Computer mit einem oder mehreren Prozessoren entwickelt wurde, sollte sie optimal auf die Interaktion mit einem Benutzer reagieren, auch wenn sie gerade mit anderen Aufgaben befasst ist. Die Verwendung verschiedener Ausführungsthreads stellt eine der effektivsten Möglichkeiten dar, eine Anwendung entsprechend reaktionsschnell zu gestalten und gleichzeitig den Prozessor zwischen Benutzerereignissen oder sogar währenddessen zu nutzen. In diesem Abschnitt werden die grundlegenden Threadingkonzepte eingeführt und insbesondere verwaltete Threadingkonzepte und die Verwendung von verwaltetem Threading ausführlich behandelt.  
  
> [!NOTE]
>  Beginnend mit [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] wurde die Multithreadprogrammierung durch die Klassen <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType> und <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>, [Parallel LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md), neue parallele Auflistungsklassen im <xref:System.Collections.Concurrent?displayProperty=nameWithType>-Namespace und ein neues Programmiermodell, das auf dem Konzept von Aufgaben anstatt von Threads basiert, erheblich vereinfacht. Weitere Informationen finden Sie unter [Parallele Programmierung in .NET Framework](../../../docs/standard/parallel-programming/index.md).  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Grundlagen des verwalteten Threadings](../../../docs/standard/threading/managed-threading-basics.md)  
 Enthält eine Übersicht über das verwaltete Threading und erläutert, in welchen Fällen mehrere Threads verwendet werden.  
  
 [Verwenden von Threads und Threading](../../../docs/standard/threading/using-threads-and-threading.md)  
 Erklärt das Erstellen, Starten, Anhalten, Fortsetzen und Abbrechen von Threads.  
  
 [Empfohlene Vorgehensweise für das verwaltete Threading](../../../docs/standard/threading/managed-threading-best-practices.md)  
 Behandelt Synchronisierungsstufen, die Vermeidung von Deadlock- und Racebedingungen und weitere Threadingprobleme.  
  
 [Threadingobjekte und -funktionen](../../../docs/standard/threading/threading-objects-and-features.md)  
 Beschreibt die verwalteten Klassen, mit denen Sie Threadingaktivitäten sowie die Daten von Objekten, auf die in verschiedenen Threads zugegriffen wird, synchronisieren können, und bietet eine Übersicht über Threadpoolthreads.  
  
## <a name="reference"></a>Referenz  
 <xref:System.Threading>  
 Enthält Klassen zum Verwenden und Synchronisieren von verwalteten Threads.  
  
 <xref:System.Collections.Concurrent>  
 Enthält Auflistungsklassen, die sicher mit mehreren Threads verwendet werden können.  
  
 <xref:System.Threading.Tasks>  
 Enthält Klassen zum Erstellen und Planen von parallelen Verarbeitungsaufgaben.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Anwendungsdomänen](../../../docs/framework/app-domains/application-domains.md)  
 Übersicht über Anwendungsdomänen und deren Verwendung durch die Common Language-Infrastruktur.  
  
 [Asynchrone Datei-E/A](../../../docs/standard/io/asynchronous-file-i-o.md)  
 Beschreibt die Leistungsvorteile und den grundlegenden Ablauf der asynchronen E/A.  
  
 [Aufgabenbasiertes asynchrones Muster](../../../docs/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap.md)  
 Bietet eine Übersicht über das empfohlene Muster für asynchrone Programmierung in .NET.  
  
 [Asynchrones Aufrufen von synchronen Methoden](../../../docs/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously.md)  
 Erläutert das Aufrufen von Methoden für Threadpoolthreads mithilfe der integrierten Features von Delegaten.  
  
 [Parallele Programmierung](../../../docs/standard/parallel-programming/index.md)  
 Beschreibt die parallelen Programmierbibliotheken, die die Verwendung mehrerer Threads in Anwendungen vereinfachen.  
  
 [Paralleles LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)  
 Beschreibt ein System zum parallelen Ausführen von Abfragen, um die Vorteile mehrerer Prozessoren zu nutzen.
