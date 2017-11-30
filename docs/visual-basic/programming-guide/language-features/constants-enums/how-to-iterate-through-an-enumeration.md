---
title: 'Gewusst wie: Durchlaufen einer Enumeration in Visual Basic'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- arrays [Visual Basic], iterating
- enumerations [Visual Basic], iterating
- ListBox control [Windows Forms], populating from an enumeration
ms.assetid: e5aa10eb-cfcd-4a3b-8e76-f06b8f2002be
caps.latest.revision: "20"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 439e6eae7d475316625a2cc1d3a70a9e7181f68a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-iterate-through-an-enumeration-in-visual-basic"></a><span data-ttu-id="35d45-102">Gewusst wie: Durchlaufen einer Enumeration in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="35d45-102">How to: Iterate Through An Enumeration in Visual Basic</span></span>
<span data-ttu-id="35d45-103">Durch Enumerationen wird ein bequemer Weg bereitgestellt, um mit Sätzen verknüpfter Konstanten zu arbeiten, und um konstanten Werten Namen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="35d45-103">Enumerations provide a convenient way to work with sets of related constants, and to associate constant values with names.</span></span> <span data-ttu-id="35d45-104">Um eine Enumeration zu durchlaufen, können Sie es in ein Array mit Verschieben der <xref:System.Enum.GetValues%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="35d45-104">To iterate through an enumeration, you can move it into an array using the <xref:System.Enum.GetValues%2A> method.</span></span> <span data-ttu-id="35d45-105">Durchlaufen Sie können auch eine Enumeration mit einer `For...Each` -Anweisung, mit der <xref:System.Enum.GetNames%2A> oder <xref:System.Enum.GetValues%2A> Methode, um die Zeichenfolge oder einen numerischen Wert zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="35d45-105">You could also iterate through an enumeration using a `For...Each` statement, using the <xref:System.Enum.GetNames%2A> or <xref:System.Enum.GetValues%2A> method to extract the string or numeric value.</span></span>  
  
### <a name="to-iterate-through-an-enumeration"></a><span data-ttu-id="35d45-106">Zum Durchlaufen einer enumeration</span><span class="sxs-lookup"><span data-stu-id="35d45-106">To iterate through an enumeration</span></span>  
  
-   <span data-ttu-id="35d45-107">Ein Array zu deklarieren und konvertieren Sie die Enumeration mit den <xref:System.Enum.GetValues%2A> Methode vor der Übergabe von Arrays als Sie würde jeder anderen Variablen.</span><span class="sxs-lookup"><span data-stu-id="35d45-107">Declare an array and convert the enumeration to it with the <xref:System.Enum.GetValues%2A> method before passing the array as you would any other variable.</span></span> <span data-ttu-id="35d45-108">Im folgende Beispiel werden die einzelnen Member der Enumeration <xref:Microsoft.VisualBasic.FirstDayOfWeek> beim Durchlaufen der Enumeration gezeigt.</span><span class="sxs-lookup"><span data-stu-id="35d45-108">The following example displays each member of the enumeration <xref:Microsoft.VisualBasic.FirstDayOfWeek> as it iterates through the enumeration.</span></span>  
  
     [!code-vb[VbEnumsTask#7](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-iterate-through-an-enumeration_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="35d45-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35d45-109">See Also</span></span>  
 [<span data-ttu-id="35d45-110">Übersicht über Enumerationen</span><span class="sxs-lookup"><span data-stu-id="35d45-110">Enumerations Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)  
 [<span data-ttu-id="35d45-111">Vorgehensweise: Deklarieren einer Enumeration</span><span class="sxs-lookup"><span data-stu-id="35d45-111">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)  
 [<span data-ttu-id="35d45-112">Situationen für die Verwendung von Enumerationen</span><span class="sxs-lookup"><span data-stu-id="35d45-112">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)  
 [<span data-ttu-id="35d45-113">Gewusst wie: Bestimmen der einem Enumerationswert zugeordnete Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="35d45-113">How to: Determine the String Associated with an Enumeration Value</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)  
 [<span data-ttu-id="35d45-114">Gewusst wie: Verweisen auf einen Enumerationsmember</span><span class="sxs-lookup"><span data-stu-id="35d45-114">How to: Refer to an Enumeration Member</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)  
 [<span data-ttu-id="35d45-115">Enumerationen und Namensqualifikation</span><span class="sxs-lookup"><span data-stu-id="35d45-115">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [<span data-ttu-id="35d45-116">Arrays</span><span class="sxs-lookup"><span data-stu-id="35d45-116">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
