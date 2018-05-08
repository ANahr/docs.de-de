---
title: Optionale Parameter müssen einen Standardwert bestimmen.
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: 6788a7908489591e266af6d141006f2aa2d0e6f1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="optional-parameters-must-specify-a-default-value"></a>Optionale Parameter müssen einen Standardwert bestimmen.
Optionale Parameter müssen Standardwerte angeben, die verwendet werden kann, wenn eine aufrufende Prozedur keine Parameter angegeben wird.  
  
 **Fehler-ID:** BC30812  
  
## <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Angeben von Standardwerten für optionale Parameter; Zum Beispiel:  
  
    ```  
    Sub Proc1(ByVal X As Integer,   
          Optional ByVal Y As String = "Default Value")  
       MsgBox("Default argument is: " & Y)  
    End Sub  
    ```  
  
## <a name="see-also"></a>Siehe auch  
 [Optional](../../../visual-basic/language-reference/modifiers/optional.md)
