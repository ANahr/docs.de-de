---
title: "Operator % (C#-Referenz)"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '%_CSharpKeyword'
dev_langs:
- CSharp
helpviewer_keywords:
- modulus operator [C#]
- '% operator [C#]'
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
caps.latest.revision: 15
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 658b04f4bee952a20a7b0a740aa931fe4fad9cdf
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="-operator-c-reference"></a><span data-ttu-id="e33e3-102">Operator % (C#-Referenz)</span><span class="sxs-lookup"><span data-stu-id="e33e3-102">% Operator (C# Reference)</span></span>
<span data-ttu-id="e33e3-103">Der Operator `%` berechnet den Rest nach der Division seines ersten Operanden durch den zweiten.</span><span class="sxs-lookup"><span data-stu-id="e33e3-103">The `%` operator computes the remainder after dividing its first operand by its second.</span></span> <span data-ttu-id="e33e3-104">Alle numerischen Typen besitzen vordefinierte Restoperatoren.</span><span class="sxs-lookup"><span data-stu-id="e33e3-104">All numeric types have predefined remainder operators.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e33e3-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e33e3-105">Remarks</span></span>  
 <span data-ttu-id="e33e3-106">Benutzerdefinierte Typen können den Operator `%` überladen (weitere Informationen unter [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="e33e3-106">User-defined types can overload the `%` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="e33e3-107">Wenn ein binärer Operator überladen ist, wird der zugehörige Zuweisungsoperator, sofern er vorhanden ist, auch implizit überladen.</span><span class="sxs-lookup"><span data-stu-id="e33e3-107">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e33e3-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e33e3-108">Example</span></span>  
 <span data-ttu-id="e33e3-109">[!code-cs[csRefOperators#9](../../../csharp/language-reference/operators/codesnippet/CSharp/modulus-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="e33e3-109">[!code-cs[csRefOperators#9](../../../csharp/language-reference/operators/codesnippet/CSharp/modulus-operator_1.cs)]</span></span>  
  
## <a name="comments"></a><span data-ttu-id="e33e3-110">Kommentare</span><span class="sxs-lookup"><span data-stu-id="e33e3-110">Comments</span></span>  
 <span data-ttu-id="e33e3-111">Beachten Sie die Rundungsfehler im Zusammenhang mit dem double-Typ.</span><span class="sxs-lookup"><span data-stu-id="e33e3-111">Note the round-off errors associated with the double type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e33e3-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e33e3-112">See Also</span></span>  
 <span data-ttu-id="e33e3-113">[C#-Referenz](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="e33e3-113">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="e33e3-114">[C#-Programmierhandbuch](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="e33e3-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="e33e3-115">C#-Operatoren</span><span class="sxs-lookup"><span data-stu-id="e33e3-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

