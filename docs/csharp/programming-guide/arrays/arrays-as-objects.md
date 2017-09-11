---
title: Arrays als Objekte (C#-Programmierhandbuch)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- arrays [C#], as objects
ms.assetid: f76d4403-bd0a-42a0-9bc8-694c55b2c926
caps.latest.revision: 17
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
ms.openlocfilehash: 396d0df9196b7331e94127730b83782ffc8ea593
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="arrays-as-objects-c-programming-guide"></a><span data-ttu-id="81390-102">Arrays als Objekte (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="81390-102">Arrays as Objects (C# Programming Guide)</span></span>
<span data-ttu-id="81390-103">In C# sind Arrays tatsächlich Objekte und nicht nur adressierbare Regionen zusammenhängender Speicher wie in C und C++.</span><span class="sxs-lookup"><span data-stu-id="81390-103">In C#, arrays are actually objects, and not just addressable regions of contiguous memory as in C and C++.</span></span> <span data-ttu-id="81390-104"><xref:System.Array> ist der abstrakte Basistyp aller Typen von Arrays.</span><span class="sxs-lookup"><span data-stu-id="81390-104"><xref:System.Array> is the abstract base type of all array types.</span></span> <span data-ttu-id="81390-105">Sie können die Eigenschaften und die anderen Klassenmember verwenden, über die <xref:System.Array> verfügt.</span><span class="sxs-lookup"><span data-stu-id="81390-105">You can use the properties, and other class members, that <xref:System.Array> has.</span></span> <span data-ttu-id="81390-106">Ein Beispiel dafür wäre die Verwendung der <xref:System.Array.Length%2A>-Eigenschaft, um die Länge eines Arrays zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="81390-106">An example of this would be using the <xref:System.Array.Length%2A> property to get the length of an array.</span></span> <span data-ttu-id="81390-107">Der folgende Code weist die Länge des `numbers`-Arrays, die `5` beträgt, einer Variablen mit dem Namen `lengthOfNumbers` zu:</span><span class="sxs-lookup"><span data-stu-id="81390-107">The following code assigns the length of the `numbers` array, which is `5`, to a variable called `lengthOfNumbers`:</span></span>  
  
 <span data-ttu-id="81390-108">[!code-cs[csProgGuideArrays#3](../../../csharp/programming-guide/arrays/codesnippet/CSharp/arrays-as-objects_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="81390-108">[!code-cs[csProgGuideArrays#3](../../../csharp/programming-guide/arrays/codesnippet/CSharp/arrays-as-objects_1.cs)]</span></span>  
  
 <span data-ttu-id="81390-109">Die <xref:System.Array>-Klasse bietet viele weitere nützliche Methoden und Eigenschaften zum Sortieren, Durchsuchen und Kopieren von Arrays.</span><span class="sxs-lookup"><span data-stu-id="81390-109">The <xref:System.Array> class provides many other useful methods and properties for sorting, searching, and copying arrays.</span></span>  
  
## <a name="example"></a><span data-ttu-id="81390-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81390-110">Example</span></span>  
 <span data-ttu-id="81390-111">In diesem Beispiel wird die <xref:System.Array.Rank%2A>-Eigenschaft verwendet, um die Anzahl der Dimensionen eines Arrays anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81390-111">This example uses the <xref:System.Array.Rank%2A> property to display the number of dimensions of an array.</span></span>  
  
 <span data-ttu-id="81390-112">[!code-cs[csProgGuideArrays#2](../../../csharp/programming-guide/arrays/codesnippet/CSharp/arrays-as-objects_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="81390-112">[!code-cs[csProgGuideArrays#2](../../../csharp/programming-guide/arrays/codesnippet/CSharp/arrays-as-objects_2.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81390-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81390-113">See Also</span></span>  
 <span data-ttu-id="81390-114">[C#-Programmierhandbuch](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="81390-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="81390-115">[Arrays](../../../csharp/programming-guide/arrays/index.md) </span><span class="sxs-lookup"><span data-stu-id="81390-115">[Arrays](../../../csharp/programming-guide/arrays/index.md) </span></span>  
 <span data-ttu-id="81390-116">[Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span><span class="sxs-lookup"><span data-stu-id="81390-116">[Single-Dimensional Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span></span>  
 <span data-ttu-id="81390-117">[Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) </span><span class="sxs-lookup"><span data-stu-id="81390-117">[Multidimensional Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) </span></span>  
 [<span data-ttu-id="81390-118">Verzweigte Arrays</span><span class="sxs-lookup"><span data-stu-id="81390-118">Jagged Arrays</span></span>](../../../csharp/programming-guide/arrays/jagged-arrays.md)

