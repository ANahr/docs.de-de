---
title: 'Vorgehensweise: Explizites Implementieren von Membern zweier Schnittstellen – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [C#], explicitly implementing interface members
- interfaces [C#], explicitly implementing with inheritance
ms.assetid: 8b402ddc-dff9-4869-89cb-d718c764e68e
ms.openlocfilehash: 3e03e80279db8c36cb975715f390ff6899d593cb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238324"
---
# <a name="how-to-explicitly-implement-members-of-two-interfaces-c-programming-guide"></a>Vorgehensweise: Explizites Implementieren von Membern zweier Schnittstellen (C#-Programmierhandbuch)
Die explizite [Schnittstellenimplementierung](../../../csharp/language-reference/keywords/interface.md) erlaubt dem Programmierer auch, zwei Schnittstellen zu implementieren, die über die gleichen Membernamen verfügen, sowie jedem Schnittstellenmember eine separate Implementierung zu geben. Dieses Beispiel zeigt die Dimensionen eines Felds in jeweils der metrischen und der englischen Einheit. Das Feld [class](../../../csharp/language-reference/keywords/class.md) implementiert zwei Schnittstellen, „IEnglishDimensions“ und „IMetricDimensions“, die die unterschiedlichen Messsysteme darstellen. Beide Schnittstellen verfügen über identische Elementnamen, sowie unterschiedliche Länge und Breite.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[csProgGuideInheritance#9](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_1.cs)]  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Wenn Sie die Standardmessungen in englischen Einheiten durchführen möchten, implementieren Sie die Methoden Länge und Breite normal, und implementieren Sie explizit die Methoden Länge und Breite aus der „IMetricDimensions“-Schnittstelle.  
  
 [!code-csharp[csProgGuideInheritance#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_2.cs)]  
  
 In diesem Fall können Sie auf die englischen Einheiten von der Klasseninstanz aus zugreifen und auf die metrischen Einheiten von der Schnittstelleninstanz aus.  
  
 [!code-csharp[csProgGuideInheritance#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-explicitly-implement-members-of-two-interfaces_3.cs)]  
  
## <a name="see-also"></a>Siehe auch

- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)  
- [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)  
- [Schnittstellen](../../../csharp/programming-guide/interfaces/index.md)  
- [Vorgehensweise: Explizites Implementieren von Schnittstellenmembern](../../../csharp/programming-guide/interfaces/how-to-explicitly-implement-interface-members.md)
