---
title: Delegatklasse &#39; &lt;Classname&gt;&#39; hat Sie keine Invoke-Methode, damit ein Ausdruck dieses Typs kann nicht das Ziel eines Methodenaufrufs sein.
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords: BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 55d0e2442807e25737d90ac4b45a59b9d3e73037
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="delegate-class-39ltclassnamegt39-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a><span data-ttu-id="a288d-102">Delegatklasse &#39; &lt;Classname&gt;&#39; hat Sie keine Invoke-Methode, damit ein Ausdruck dieses Typs kann nicht das Ziel eines Methodenaufrufs sein.</span><span class="sxs-lookup"><span data-stu-id="a288d-102">Delegate class &#39;&lt;classname&gt;&#39; has no Invoke method, so an expression of this type cannot be the target of a method call</span></span>
<span data-ttu-id="a288d-103">Ein Aufruf von `Invoke` über einen Delegaten ist fehlgeschlagen, da `Invoke` nicht auf die Delegate-Klasse implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a288d-103">A call to `Invoke` through a delegate has failed because `Invoke` is not implemented on the delegate class.</span></span>  
  
 <span data-ttu-id="a288d-104">**Fehler-ID:** BC30220</span><span class="sxs-lookup"><span data-stu-id="a288d-104">**Error ID:** BC30220</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a288d-105">So beheben Sie diesen Fehler</span><span class="sxs-lookup"><span data-stu-id="a288d-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="a288d-106">Stellen Sie sicher, dass eine Instanz der Delegatklasse mit erstellt wurde eine `Dim` -Anweisung und die Delegatinstanz mit eine Prozedur zugewiesen wurde die `AddressOf` Operator.</span><span class="sxs-lookup"><span data-stu-id="a288d-106">Ensure that an instance of the delegate class has been created with a `Dim` statement and that a procedure has been assigned to the delegate instance with the `AddressOf` operator.</span></span>  
  
2.  <span data-ttu-id="a288d-107">Suchen Sie den Code, der die Delegate-Klasse implementiert, und stellen Sie sicher, dass es implementiert die `Invoke` Prozedur.</span><span class="sxs-lookup"><span data-stu-id="a288d-107">Locate the code that implements the delegate class and make sure it implements the `Invoke` procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a288d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a288d-108">See Also</span></span>  
 [<span data-ttu-id="a288d-109">Delegaten</span><span class="sxs-lookup"><span data-stu-id="a288d-109">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)  
 [<span data-ttu-id="a288d-110">Delegate-Anweisung</span><span class="sxs-lookup"><span data-stu-id="a288d-110">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [<span data-ttu-id="a288d-111">AddressOf-Operator</span><span class="sxs-lookup"><span data-stu-id="a288d-111">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [<span data-ttu-id="a288d-112">Dim-Anweisung</span><span class="sxs-lookup"><span data-stu-id="a288d-112">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
