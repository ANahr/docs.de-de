---
title: ':: Operator – C#-Referenz'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2e456be075f3487676228244e0119ff46ed9a538
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243477"
---
# <a name="-operator-c-reference"></a>:: Operator (C#-Referenz)
Der Namespacealias-Qualifizierer (`::`) wird verwendet, um nach Bezeichnern zu suchen. Er befindet sich immer zwischen zwei Bezeichnern, wie im folgenden Beispiel:  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

Der Operator `::` kann auch mit einer *Alias-Direktive* verwendet werden:

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a>Hinweise  
 Der Namespacealias-Qualifizierer kann `global` sein. Dadurch wird eine Suche im globalen Namespace anstatt Namespacealias aufgerufen.  
  
## <a name="for-more-information"></a>Weitere Informationen  
 Ein Beispiel zur Verwendung des `::`-Operators finden Sie im folgenden Abschnitt:  
  
-   [Vorgehensweise: Verwenden des globalen Namespacealias](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a>C#-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)  
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)  
- [C#-Operatoren](../../../csharp/language-reference/operators/index.md)  
- [Namespaceschlüsselwörter](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [. Operator](../../../csharp/language-reference/operators/member-access-operator.md)  
- [extern alias](../../../csharp/language-reference/keywords/extern-alias.md)
