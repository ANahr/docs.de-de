---
title: 'Vorgehensweise: Verwenden von Zeigern zum Kopieren eines Bytearrays – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 04/20/2018
helpviewer_keywords:
- byte arrays [C#]
- arrays [C#], byte
- pointers [C#], to copy bytes
ms.openlocfilehash: 49151c6d2a573a24e63f733a5279faeee40de1b7
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241125"
---
# <a name="how-to-use-pointers-to-copy-an-array-of-bytes--c-programming-guide"></a>Vorgehensweise: Verwenden von Zeigern zum Kopieren eines Bytearrays (C#-Programmierhandbuch)

In folgendem Beispiel werden Zeiger verwendet, um Bytes aus einem Array in ein anderes zu kopieren.

In diesem Beispiel wird das Schlüsselwort [unsafe](../../language-reference/keywords/unsafe.md) verwendet, mit dem Sie Zeiger in der `Copy`-Methode verwenden können. Die Anweisung [fixed](../../language-reference/keywords/fixed-statement.md) wird verwendet, um Zeiger auf das Quell- und Zielarray zu deklarieren. Diese `fixed`-Anweisung *heftet* den Speicherort des Quell- und Zielarrays im Speicher an, damit diese während der automatischen Speicherbereinigung nicht verschoben werden. Die Speicherblöcke der Arrays werden gelöst, wenn der `fixed`-Block abgeschlossen wird. Da die `Copy`-Methode in diesem Beispiel das Schlüsselwort `unsafe` verwendet, muss sie mit der Compileroption [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md) kompiliert werden.

In diesem Beispiel werden Indizes anstelle eines zweiten nicht verwalteten Zeigers verwendet, um auf die Elemente beider Arrays zuzugreifen. Die Deklaration der Zeiger `pSource` und `pTarget` heftet die Arrays an. Dieses Feature ist ab C# 7.3 verfügbar.

## <a name="example"></a>Beispiel

[!code-csharp[Struct with embedded inline array](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#8)]

## <a name="see-also"></a>Siehe auch

- [C#-Programmierhandbuch](../index.md)  
- [Unsicherer Code und Zeiger](index.md)  
- [-unsafe (C#-Compileroptionen)](../../language-reference/compiler-options/unsafe-compiler-option.md)  
- [Garbage Collection](../../../standard/garbage-collection/index.md)  
