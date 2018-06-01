---
title: -pathmap (C#-Compileroptionen)
ms.date: 05/16/2018
f1_keywords:
- /pathmap
helpviewer_keywords:
- -pathmap compiler option [C#]
- pathmap compiler option [C#]
- /pathmap compiler option [C#]
ms.openlocfilehash: 36196ffea19cfde7ff5f830ea358d2bd83edf419
ms.sourcegitcommit: 77d9a94dac4c05827ed0663d95e0f9ad35d6682e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2018
ms.locfileid: "34472813"
---
# <a name="-pathmap-c-compiler-options"></a>-pathmap (C#-Compileroptionen)

Mit der Compileroption **-pathmap** wird angegeben, wie physische Pfade den Quellpfadnamen zugeordnet werden, die vom Compiler ausgegeben werden.

## <a name="syntax"></a>Syntax

```console
-pathmap:path1=sourcePath1,path2=sourcePath2
```

## <a name="arguments"></a>Argumente

 `path1` Vollständiger Pfad zu den Quelldateien in der aktuellen Umgebung.

 `sourcePath1` Quellpfad, der in allen Ausgabedateien `path1` ersetzt.

Trennen Sie mehrere zugeordnete Quellpfade durch ein Komma.

## <a name="remarks"></a>Hinweise

Es gibt folgende Gründe, warum der Compiler den Quellpfad in die Ausgabe schreibt:

1. Der Quellpfad ersetzt ein Argument, wenn das <xref:System.Runtime.CompilerServices.CallerFilePathAttribute> auf einen optionalen Parameter angewendet wird.
1. Der Quellpfad ist in eine PDB-Datei eingebettet.
1. Der Pfad der PDB-Datei ist in einer PE-Datei (Portable Executable, portierbare ausführbare Datei) eingebettet.

Bei dieser Option wird jeder physische Pfad auf dem Computer, auf dem der Compiler ausgeführt wird, einem entsprechenden Pfad zugeordnet, der in die Ausgabedateien geschrieben werden sollte.

## <a name="example"></a>Beispiel

Kompilieren Sie `t.cs` im Verzeichnis **C:\\work\\tests**, und ordnen Sie dieses Verzeichnis **\publish** in der Ausgabe zu:

```console
csc -pathmap:C:\work\tests=\publish t.cs
```

## <a name="see-also"></a>Siehe auch

 [C#-Compileroptionen](../../../csharp/language-reference/compiler-options/index.md)  
 [Verwalten von Projekt- und Projektmappeneigenschaften](/visualstudio/ide/managing-project-and-solution-properties)
