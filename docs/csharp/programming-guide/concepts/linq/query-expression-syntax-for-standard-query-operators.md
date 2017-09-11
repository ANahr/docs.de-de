---
title: "Abfrageausdruckssyntax für Standardabfrageoperatoren (C#)"
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
ms.assetid: e1e17ef2-68ff-4c26-b6e2-015668227fa5
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 30e994329234b8bd455f739694e50121bac63d5d
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="query-expression-syntax-for-standard-query-operators-c"></a><span data-ttu-id="7a6cc-102">Abfrageausdruckssyntax für Standardabfrageoperatoren (C#)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-102">Query Expression Syntax for Standard Query Operators (C#)</span></span>
<span data-ttu-id="7a6cc-103">Einige der häufiger verwendeten Standardabfrageoperatoren verfügen über eine dedizierte Schlüsselwortsyntax von C#, wodurch sie als Teil eines *Abfrageausdrucks* aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="7a6cc-103">Some of the more frequently used standard query operators have dedicated C# language keyword syntax that enables them to be called as part of a *query expression*.</span></span> <span data-ttu-id="7a6cc-104">Mit einem Abfrageausdruck kann eine Abfrage besser lesbar ausgedrückt werden als mit dessen *methodenbasierter* Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="7a6cc-104">A query expression is a different, more readable form of expressing a query than its *method-based*  equivalent.</span></span> <span data-ttu-id="7a6cc-105">Die Abfrageausdrucksklauseln werden bei der Kompilierung in Aufrufe der Abfragemethoden übersetzt.</span><span class="sxs-lookup"><span data-stu-id="7a6cc-105">Query expression clauses are translated into calls to the query methods at compile time.</span></span>  
  
## <a name="query-expression-syntax-table"></a><span data-ttu-id="7a6cc-106">Tabelle: Abfrageausdruckssyntax</span><span class="sxs-lookup"><span data-stu-id="7a6cc-106">Query Expression Syntax Table</span></span>  
 <span data-ttu-id="7a6cc-107">In der folgenden Tabelle finden Sie eine Liste von Standardabfrageoperatoren, die über äquivalente Abfrageausdrucksklauseln verfügen.</span><span class="sxs-lookup"><span data-stu-id="7a6cc-107">The following table lists the standard query operators that have equivalent query expression clauses.</span></span>  
  
|<span data-ttu-id="7a6cc-108">Methode</span><span class="sxs-lookup"><span data-stu-id="7a6cc-108">Method</span></span>|<span data-ttu-id="7a6cc-109">C#-Abfrageausdruckssyntax</span><span class="sxs-lookup"><span data-stu-id="7a6cc-109">C# Query Expression Syntax</span></span>|  
|------------|---------------------------------|  
|<xref:System.Linq.Enumerable.Cast%2A>|<span data-ttu-id="7a6cc-110">Verwenden Sie eine explizit typisierte Bereichsvariable, z.B.:</span><span class="sxs-lookup"><span data-stu-id="7a6cc-110">Use an explicitly typed range variable, for example:</span></span><br /><br /> `from int i in numbers`<br /><br /> <span data-ttu-id="7a6cc-111">(Weitere Informationen finden Sie unter [from-Klausel](../../../../csharp/language-reference/keywords/from-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-111">(For more information, see [from clause](../../../../csharp/language-reference/keywords/from-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.GroupBy%2A>|`group … by`<br /><br /> <span data-ttu-id="7a6cc-112">- oder - </span><span class="sxs-lookup"><span data-stu-id="7a6cc-112">-or-</span></span><br /><br /> `group … by … into …`<br /><br /> <span data-ttu-id="7a6cc-113">(Weitere Informationen finden Sie unter [group-Klausel](../../../../csharp/language-reference/keywords/group-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-113">(For more information, see [group clause](../../../../csharp/language-reference/keywords/group-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.GroupJoin%60%604%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%2CSystem.Func%7B%60%600%2C%60%602%7D%2CSystem.Func%7B%60%601%2C%60%602%7D%2CSystem.Func%7B%60%600%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%2C%60%603%7D%29>|`join … in … on … equals … into …`<br /><br /> <span data-ttu-id="7a6cc-114">(Weitere Informationen finden Sie unter [join-Klausel](../../../../csharp/language-reference/keywords/join-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-114">(For more information, see [join clause](../../../../csharp/language-reference/keywords/join-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.Join%60%604%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Collections.Generic.IEnumerable%7B%60%601%7D%2CSystem.Func%7B%60%600%2C%60%602%7D%2CSystem.Func%7B%60%601%2C%60%602%7D%2CSystem.Func%7B%60%600%2C%60%601%2C%60%603%7D%29>|`join … in … on … equals …`<br /><br /> <span data-ttu-id="7a6cc-115">(Weitere Informationen finden Sie unter [join-Klausel](../../../../csharp/language-reference/keywords/join-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-115">(For more information, see [join clause](../../../../csharp/language-reference/keywords/join-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.OrderBy%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29>|`orderby`<br /><br /> <span data-ttu-id="7a6cc-116">(Weitere Informationen finden Sie unter [orderby-Klausel](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-116">(For more information, see [orderby clause](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span></span>|  
<xref:System.Linq.Enumerable.OrderByDescending%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29>|`orderby … descending`<br /><br /> <span data-ttu-id="7a6cc-117">(Weitere Informationen finden Sie unter [orderby-Klausel](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-117">(For more information, see [orderby clause](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.Select%2A>|`select`<br /><br /> <span data-ttu-id="7a6cc-118">(Weitere Informationen finden Sie unter [select-Klausel](../../../../csharp/language-reference/keywords/select-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-118">(For more information, see [select clause](../../../../csharp/language-reference/keywords/select-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.SelectMany%2A>|<span data-ttu-id="7a6cc-119">Mehrere `from`-Klauseln.</span><span class="sxs-lookup"><span data-stu-id="7a6cc-119">Multiple `from` clauses.</span></span><br /><br /> <span data-ttu-id="7a6cc-120">(Weitere Informationen finden Sie unter [from-Klausel](../../../../csharp/language-reference/keywords/from-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-120">(For more information, see [from clause](../../../../csharp/language-reference/keywords/from-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.ThenBy%60%602%28System.Linq.IOrderedEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29>|`orderby …, …`<br /><br /> <span data-ttu-id="7a6cc-121">(Weitere Informationen finden Sie unter [orderby-Klausel](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-121">(For more information, see [orderby clause](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.ThenByDescending%60%602%28System.Linq.IOrderedEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29>|`orderby …, … descending`<br /><br /> <span data-ttu-id="7a6cc-122">(Weitere Informationen finden Sie unter [orderby-Klausel](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-122">(For more information, see [orderby clause](../../../../csharp/language-reference/keywords/orderby-clause.md).)</span></span>|  
|<xref:System.Linq.Enumerable.Where%2A>|`where`<br /><br /> <span data-ttu-id="7a6cc-123">(Weitere Informationen finden Sie unter [where-Klausel](../../../../csharp/language-reference/keywords/where-clause.md).)</span><span class="sxs-lookup"><span data-stu-id="7a6cc-123">(For more information, see [where clause](../../../../csharp/language-reference/keywords/where-clause.md).)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7a6cc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a6cc-124">See Also</span></span>  
 <span data-ttu-id="7a6cc-125"><xref:System.Linq.Enumerable></span><span class="sxs-lookup"><span data-stu-id="7a6cc-125"><xref:System.Linq.Enumerable></span></span>   
 <span data-ttu-id="7a6cc-126"><xref:System.Linq.Queryable></span><span class="sxs-lookup"><span data-stu-id="7a6cc-126"><xref:System.Linq.Queryable></span></span>   
 <span data-ttu-id="7a6cc-127">[Übersicht über Standardabfrageoperatoren (C#)](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md) </span><span class="sxs-lookup"><span data-stu-id="7a6cc-127">[Standard Query Operators Overview (C#)](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md) </span></span>  
 [<span data-ttu-id="7a6cc-128">Classification of Standard Query Operators by Manner of Execution (C#) (Klassifizierung von Standardabfrageoperatoren nach Ausführungsarten (C#))</span><span class="sxs-lookup"><span data-stu-id="7a6cc-128">Classification of Standard Query Operators by Manner of Execution (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/classification-of-standard-query-operators-by-manner-of-execution.md)

