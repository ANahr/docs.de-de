---
title: protected (C#-Referenz)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- protected
- protected_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- protected keyword [C#]
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
caps.latest.revision: 20
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
ms.openlocfilehash: c3d24389f66edec313d4f5238b0aee02518e33b7
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="protected-c-reference"></a><span data-ttu-id="bc60f-102">protected (C#-Referenz)</span><span class="sxs-lookup"><span data-stu-id="bc60f-102">protected (C# Reference)</span></span>
<span data-ttu-id="bc60f-103">Das `protected`-Schlüsselwort ist ein Zugriffsmodifizierer für Member.</span><span class="sxs-lookup"><span data-stu-id="bc60f-103">The `protected` keyword is a member access modifier.</span></span> <span data-ttu-id="bc60f-104">Auf einen geschützten Member kann innerhalb seiner Klasse und von Instanzen abgeleiteter Klasse zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="bc60f-104">A protected member is accessible within its class and by derived class instances.</span></span> <span data-ttu-id="bc60f-105">Einen Vergleich von `protected` mit den anderen Zugriffsmodifizierern finden Sie unter [Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md).</span><span class="sxs-lookup"><span data-stu-id="bc60f-105">For a comparison of `protected` with the other access modifiers, see [Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc60f-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc60f-106">Example</span></span>  
 <span data-ttu-id="bc60f-107">Auf einen geschützten Member einer Basisklasse kann in einer abgeleiteten Klasse zugegriffen werden, nur wenn der Zugriff über den Typ der abgeleiteten Klasse erfolgt.</span><span class="sxs-lookup"><span data-stu-id="bc60f-107">A protected member of a base class is accessible in a derived class only if the access occurs through the derived class type.</span></span> <span data-ttu-id="bc60f-108">Sehen Sie sich z.B. folgenden Codeabschnitt an:</span><span class="sxs-lookup"><span data-stu-id="bc60f-108">For example, consider the following code segment:</span></span>  
  
 <span data-ttu-id="bc60f-109">[!code-cs[csrefKeywordsModifiers#11](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="bc60f-109">[!code-cs[csrefKeywordsModifiers#11](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_1.cs)]</span></span>  
  
 <span data-ttu-id="bc60f-110">Die Anweisung `a.x = 10` generiert einen Fehler, da sie innerhalb der statischen Main-Methode erstellt wird und keine Instanz der Klasse B ist.</span><span class="sxs-lookup"><span data-stu-id="bc60f-110">The statement `a.x = 10` generates an error because it is made within the static method Main, and not an instance of class B.</span></span>  
  
 <span data-ttu-id="bc60f-111">Strukturmember können nicht geschützt werden, da die Struktur nicht vererbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc60f-111">Struct members cannot be protected because the struct cannot be inherited.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc60f-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc60f-112">Example</span></span>  
 <span data-ttu-id="bc60f-113">In diesem Beispiel wird die `DerivedPoint`-Klasse von `Point` abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc60f-113">In this example, the class `DerivedPoint` is derived from `Point`.</span></span> <span data-ttu-id="bc60f-114">Daher können Sie direkt von der abgeleiteten Klasse auf die geschützten Member der Basisklasse zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bc60f-114">Therefore, you can access the protected members of the base class directly from the derived class.</span></span>  
  
 <span data-ttu-id="bc60f-115">[!code-cs[csrefKeywordsModifiers#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="bc60f-115">[!code-cs[csrefKeywordsModifiers#12](../../../csharp/language-reference/keywords/codesnippet/CSharp/protected_2.cs)]</span></span>  
  
 <span data-ttu-id="bc60f-116">Wenn Sie die Zugriffsebenen von `x` und `y` auf [private](../../../csharp/language-reference/keywords/private.md) ändern, wird der Compiler die Fehlermeldungen anzeigen:</span><span class="sxs-lookup"><span data-stu-id="bc60f-116">If you change the access levels of `x` and `y` to [private](../../../csharp/language-reference/keywords/private.md), the compiler will issue the error messages:</span></span>  
  
 `'Point.y' is inaccessible due to its protection level.`  
  
 `'Point.x' is inaccessible due to its protection level.`  
  
## <a name="c-language-specification"></a><span data-ttu-id="bc60f-117">C#-Programmiersprachenspezifikation</span><span class="sxs-lookup"><span data-stu-id="bc60f-117">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bc60f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc60f-118">See Also</span></span>  
 <span data-ttu-id="bc60f-119">[C#-Referenz](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-119">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="bc60f-120">[C#-Programmierhandbuch](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-120">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="bc60f-121">[C#-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-121">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="bc60f-122">[Zugriffsmodifizierer](../../../csharp/language-reference/keywords/access-modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-122">[Access Modifiers](../../../csharp/language-reference/keywords/access-modifiers.md) </span></span>  
 <span data-ttu-id="bc60f-123">[Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-123">[Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) </span></span>  
 <span data-ttu-id="bc60f-124">[Modifizierer](../../../csharp/language-reference/keywords/modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-124">[Modifiers](../../../csharp/language-reference/keywords/modifiers.md) </span></span>  
 <span data-ttu-id="bc60f-125">[Public](../../../csharp/language-reference/keywords/public.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-125">[public](../../../csharp/language-reference/keywords/public.md) </span></span>  
 <span data-ttu-id="bc60f-126">[private](../../../csharp/language-reference/keywords/private.md) </span><span class="sxs-lookup"><span data-stu-id="bc60f-126">[private](../../../csharp/language-reference/keywords/private.md) </span></span>  
 [<span data-ttu-id="bc60f-127">internal</span><span class="sxs-lookup"><span data-stu-id="bc60f-127">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)

