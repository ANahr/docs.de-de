---
title: Ein Wert vom Typ &#39; &lt;Typname1&gt;&#39; kann nicht konvertiert werden, um &#39;&lt; Typname2&gt;&#39;
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30955
- bc30955
helpviewer_keywords: BC30955
ms.assetid: 966b61eb-441e-48b0-bedf-ca95384ecb8b
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: b583c4272dd6e964de99fb14d2795152c655f3aa
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="value-of-type-39lttypename1gt39-cannot-be-converted-to-39lttypename2gt39"></a>Ein Wert vom Typ &#39; &lt;Typname1&gt;&#39; kann nicht konvertiert werden, um &#39;&lt; Typname2&gt;&#39;
Wert vom Typ "\<Typname1 >' kann nicht konvertiert werden, um"\<Typname2 > ". Typenkonflikt möglicherweise zurückzuführen. das Mischen eines Dateiverweises mit einem Projektverweis auf Assembly '\<Assemblyname >'. Ersetzen Sie den Dateiverweis auf "\<Filepath >" in Projekt "\<projektname1 >" mit einem Projektverweis auf "\<projektname2 >".  
  
 In einer Situation, in denen ein Projekt einen Projektverweis und ein Dateiverweis erstellt, kann der Compiler nicht garantieren, einem Typ in einen anderen konvertiert werden kann.  
  
 Der folgende Pseudocode veranschaulicht eine Situation, die dieser Fehler generiert werden kann.  
  
 `' ================ Visual Basic project P1 ================`  
  
 `'        P1 makes a PROJECT REFERENCE to project P2`  
  
 `'        and a FILE REFERENCE to project P3.`  
  
 `Public commonObject As P3.commonClass`  
  
 `commonObject = P2.getCommonClass()`  
  
 `' ================ Visual Basic project P2 ================`  
  
 `'        P2 makes a PROJECT REFERENCE to project P3`  
  
 `Public Function getCommonClass() As P3.commonClass`  
  
 `Return New P3.commonClass`  
  
 `End Function`  
  
 `' ================ Visual Basic project P3 ================`  
  
 `Public Class commonClass`  
  
 `End Class`  
  
 Projekt `P1` macht einen indirekten Projektverweis über Projekt `P2` Projekt `P3`, und auch einen direkten Dateiverweis auf `P3`. Die Deklaration von `commonObject` verwendet den Dateiverweis auf `P3`, während im Aufruf von `P2.getCommonClass` verwendet den Projektverweis `P3`.  
  
 Das Problem in diesem Fall ist, dass das Projekt einen Dateipfad und einen Namen für die Ausgabedatei gibt `P3` (normalerweise p3.dll), während das Projekt verweist auf das Quellprojekt ermitteln (`P3`) durch den Namen des Projekts. Aus diesem Grund der Compiler nicht garantieren, dass den Typ `P3.commonClass` stammen aus dem gleichen Quellcode über zwei unterschiedliche Verweise.  
  
 Diese Situation tritt in der Regel auf, wenn Projektverweise und Dateiverweise gemischt werden. In der vorherigen Abbildung sind das Problem würde nicht auftreten, wenn `P1` mit einen direkten Projektverweis vorgenommen `P3` anstelle eines Dateiverweises.  
  
 **Fehler-ID:** BC30955  
  
## <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Den Dateiverweis auf einen Projektverweis zu ändern.  
  
## <a name="see-also"></a>Siehe auch  
 [Konvertierungen in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [Verwalten von Verweisen in einem Projekt](/visualstudio/ide/managing-references-in-a-project)  
 
