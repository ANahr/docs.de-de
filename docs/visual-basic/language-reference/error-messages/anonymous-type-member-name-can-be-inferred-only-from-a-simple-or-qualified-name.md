---
title: Der Membername eines anonymen Typs kann nur von einem einfachen oder qualifizierten Namen ohne Argumente abgeleitet werden
ms.date: 07/20/2015
ms.prod: .net
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc36556
- bc36556
helpviewer_keywords: BC36556
ms.assetid: e3ba1f33-3a71-4f03-9b04-ed5ec17de17c
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 7068928a17ee5fdb7bf6b5e0a40aaa7e5ef32f11
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="anonymous-type-member-name-can-be-inferred-only-from-a-simple-or-qualified-name-with-no-arguments"></a>Der Membername eines anonymen Typs kann nur von einem einfachen oder qualifizierten Namen ohne Argumente abgeleitet werden
Ein anonymer Typ Elementnamen aus einem komplexen Ausdruck kann nicht abgeleitet werden.  
  
```vb  
Dim numbers() As Integer = {1, 2, 3, 4, 5}  
' Not valid.  
' Dim instanceName1 = New With {numbers(3)}  
```  
  
 Weitere Informationen zu Datenquellen aus der anonyme Typen können und nicht die Namen und Typen ableiten, finden Sie unter [wie: Ableiten von Eigenschaftennamen und Typen in Deklarationen von anonymen Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md).  
  
 **Fehler-ID:** BC36556  
  
## <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Weisen Sie den Ausdruck zu einem Elementnamen, wie im folgenden Code gezeigt:  
  
    ```  
    Dim instanceName2 = New With {.number = numbers(3)}  
    ```  
  
## <a name="see-also"></a>Siehe auch  
 [Anonyme Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)  
 [Gewusst wie: Ableiten von Eigenschaftennamen und Typen in Deklarationen von anonymen Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
