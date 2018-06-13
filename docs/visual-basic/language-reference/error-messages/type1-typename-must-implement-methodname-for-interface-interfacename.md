---
title: '&lt;Typ1&gt;&#39;&lt;Typename&gt; &#39; implementieren müssen &#39; &lt;Methodname&gt; &#39; für Schnittstelle &#39; &lt;Schnittstellenname&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: daeeab853f6a7f582542fa15ffc09ce749731d6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594382"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="a8da3-102">&lt;Typ1&gt;&#39;&lt;Typename&gt; &#39; implementieren müssen &#39; &lt;Methodname&gt; &#39; für Schnittstelle &#39; &lt;Schnittstellenname&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="a8da3-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="a8da3-103">Eine Klasse oder Struktur Ansprüche an, um eine Schnittstelle zu implementieren, implementiert jedoch keine Prozedur, die von der Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a8da3-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="a8da3-104">Jeder Member der Schnittstelle muss implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8da3-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="a8da3-105">**Fehler-ID:** BC30149</span><span class="sxs-lookup"><span data-stu-id="a8da3-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a8da3-106">So beheben Sie diesen Fehler</span><span class="sxs-lookup"><span data-stu-id="a8da3-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="a8da3-107">Deklarieren Sie eine Prozedur mit demselben Namen und derselben Signatur wie in der Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a8da3-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="a8da3-108">Schließen Sie unbedingt mit mindestens der `End Function` oder `End Sub` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="a8da3-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="a8da3-109">Hinzufügen einer `Implements` -Klausel, um das Ende der `Function` oder `Sub` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="a8da3-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="a8da3-110">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8da3-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a8da3-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8da3-111">See Also</span></span>  
 [<span data-ttu-id="a8da3-112">Implements-Anweisung</span><span class="sxs-lookup"><span data-stu-id="a8da3-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)  
 [<span data-ttu-id="a8da3-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a8da3-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
