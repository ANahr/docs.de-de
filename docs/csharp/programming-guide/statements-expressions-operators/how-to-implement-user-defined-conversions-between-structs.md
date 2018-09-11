---
title: 'Gewusst wie: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen (C#-Programmierhandbuch)'
ms.date: 07/20/2015
helpviewer_keywords:
- user-defined conversions [C#]
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
ms.openlocfilehash: cff85d60c1b59f4d1ca028f8fc02fee5728fa3d6
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2018
ms.locfileid: "44251972"
---
# <a name="how-to-implement-user-defined-conversions-between-structs-c-programming-guide"></a>Gewusst wie: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen (C#-Programmierhandbuch)
Dieses Beispiel definiert zwei Strukturen, `RomanNumeral` und `BinaryNumeral`, und zeigt Konvertierungen zwischen diesen.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[csProgGuideStatements#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_1.cs)]  
  
## <a name="robust-programming"></a>Stabile Programmierung  
  
-   Im vorherigen Beispiel führt die Anweisung  
  
     [!code-csharp[csProgGuideStatements#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_2.cs)]  
  
     führt eine Konvertierung von `RomanNumeral` zu `BinaryNumeral` durch. Da es keine direkte Konvertierung von `RomanNumeral` zu `BinaryNumeral` gibt, wird eine Umwandlung für die Konvertierung von `RomanNumeral` zu `int` verwendet, und eine weitere Umwandlung zum Konvertieren von `int` zu `BinaryNumeral`.  
  
-   Die Anweisung  
  
     [!code-csharp[csProgGuideStatements#15](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-implement-user-defined-conversions-between-structs_3.cs)]  
  
     führt eine Konvertierung von `BinaryNumeral` zu `RomanNumeral` durch. Da `RomanNumeral` eine implizierte Konvertierung von `BinaryNumeral` definiert, ist keine Umwandlung erforderlich.  
  
## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)  
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)  
- [Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)
