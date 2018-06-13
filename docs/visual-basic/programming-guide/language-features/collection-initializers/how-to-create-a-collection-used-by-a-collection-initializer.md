---
title: 'Gewusst wie: Erstellen einer Auflistung für einen Auflistungsinitialisierer (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: 6158b6f02d95260e2955e77d732fae8b8d9d5e04
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33654160"
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a><span data-ttu-id="cb58f-102">Gewusst wie: Erstellen einer Auflistung für einen Auflistungsinitialisierer (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cb58f-102">How to: Create a Collection Used by a Collection Initializer (Visual Basic)</span></span>
<span data-ttu-id="cb58f-103">Wenn Sie einen Auflistungsinitialisierer verwenden, um eine Sammlung erstellen, sucht Visual Basic-Compiler für eine `Add` Methode des Auflistungstyps, für die die Parameter für die `Add` Methode überein, die die Typen der Werte im Auflistungsinitialisierer.</span><span class="sxs-lookup"><span data-stu-id="cb58f-103">When you use a collection initializer to create a collection, the Visual Basic compiler searches for an `Add` method of the collection type for which the parameters for the `Add` method match the types of the values in the collection initializer.</span></span> <span data-ttu-id="cb58f-104">Dies `Add` Methode beim Auffüllen der Auflistung mit den Werten aus den Auflistungsinitialisierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb58f-104">This `Add` method is used to populate the collection with the values from the collection initializer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb58f-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb58f-105">Example</span></span>  
 <span data-ttu-id="cb58f-106">Das folgende Beispiel zeigt eine `OrderCollection` Sammlung mit einem öffentlichen `Add` Methode, mit der ein Auflistungsinitialisierer zum Hinzufügen von Objekten des Typs `Order`.</span><span class="sxs-lookup"><span data-stu-id="cb58f-106">The following example shows an `OrderCollection` collection that contains a public `Add` method that a collection initializer can use to add objects of type `Order`.</span></span> <span data-ttu-id="cb58f-107">Die `Add` Methode können Sie die gekürzte Auflistungsinitialisierersyntax zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb58f-107">The `Add` method enables you to use the shortened collection initializer syntax.</span></span>  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_1.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_2.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_3.vb)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](../../../../visual-basic/programming-guide/language-features/collection-initializers/codesnippet/VisualBasic/how-to-create-a-collection-used-by-a-collection-initializer_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="cb58f-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb58f-108">See Also</span></span>  
 [<span data-ttu-id="cb58f-109">Auflistungsinitialisierer</span><span class="sxs-lookup"><span data-stu-id="cb58f-109">Collection Initializers</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)  
 [<span data-ttu-id="cb58f-110">Gewusst wie: Erstellen einer Add-Erweiterungsmethode für einen Auflistungsinitialisierer</span><span class="sxs-lookup"><span data-stu-id="cb58f-110">How to: Create an Add Extension Method Used by a Collection Initializer</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
