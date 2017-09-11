---
title: / optionexplicit | Microsoft-Dokumentation
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- /optionexplicit
dev_langs:
- VB
helpviewer_keywords:
- /optionexplicit compiler option [Visual Basic]
- optionexplicit compiler option [Visual Basic]
- -optionexplicit compiler option [Visual Basic]
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
caps.latest.revision: 16
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 3d2622c08b863233c8e1088bad252b37b3b38b04
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="optionexplicit"></a><span data-ttu-id="e37f2-102">/optionexplicit</span><span class="sxs-lookup"><span data-stu-id="e37f2-102">/optionexplicit</span></span>
<span data-ttu-id="e37f2-103">Bewirkt, dass der Compiler Fehler meldet, wenn Variablen nicht deklariert werden, bevor sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e37f2-103">Causes the compiler to report errors if variables are not declared before they are used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e37f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e37f2-104">Syntax</span></span>  
  
```  
/optionexplicit[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="e37f2-105">Argumente</span><span class="sxs-lookup"><span data-stu-id="e37f2-105">Arguments</span></span>  
 <span data-ttu-id="e37f2-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="e37f2-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="e37f2-107">Optional.</span><span class="sxs-lookup"><span data-stu-id="e37f2-107">Optional.</span></span> <span data-ttu-id="e37f2-108">Geben Sie `/optionexplicit+` explizite Deklaration von Variablen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e37f2-108">Specify `/optionexplicit+` to require explicit declaration of variables.</span></span> <span data-ttu-id="e37f2-109">Die `/optionexplicit+` Option ist die Standardeinstellung und entspricht der `/optionexplicit`.</span><span class="sxs-lookup"><span data-stu-id="e37f2-109">The `/optionexplicit+` option is the default and is the same as `/optionexplicit`.</span></span> <span data-ttu-id="e37f2-110">Die `/optionexplicit-` Option ermöglicht die implizite Deklaration von Variablen.</span><span class="sxs-lookup"><span data-stu-id="e37f2-110">The `/optionexplicit-` option enables implicit declaration of variables.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e37f2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e37f2-111">Remarks</span></span>  
 <span data-ttu-id="e37f2-112">Wenn die Quellcodedatei enthält eine [Option Explicit-Anweisung](../../../visual-basic/language-reference/statements/option-explicit-statement.md), überschreibt die Anweisung die `/optionexplicit` Befehlszeilencompiler-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e37f2-112">If the source code file contains an [Option Explicit Statement](../../../visual-basic/language-reference/statements/option-explicit-statement.md), the statement overrides the `/optionexplicit` command-line compiler setting.</span></span>  
  
### <a name="to-set-optionexplicit-in-the-visual-studio-ide"></a><span data-ttu-id="e37f2-113">/ Optionexplicit in der Visual Studio-IDE festlegen</span><span class="sxs-lookup"><span data-stu-id="e37f2-113">To set /optionexplicit in the Visual Studio IDE</span></span>  
  
1.  <span data-ttu-id="e37f2-114">Ein Projekt auswählen in **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="e37f2-114">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="e37f2-115">Auf der **Projekt** Menü klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e37f2-115">On the **Project** menu, click **Properties**.</span></span> <span data-ttu-id="e37f2-116">Weitere Informationen finden Sie unter [Einführung in den Projekt-Designer](http://msdn.microsoft.com/en-us/898dd854-c98d-430c-ba1b-a913ce3c73d7).</span><span class="sxs-lookup"><span data-stu-id="e37f2-116">For more information, see [Introduction to the Project Designer](http://msdn.microsoft.com/en-us/898dd854-c98d-430c-ba1b-a913ce3c73d7).</span></span>  
  
2.  <span data-ttu-id="e37f2-117">Klicken Sie auf die **Kompilieren** Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="e37f2-117">Click the **Compile** tab.</span></span>  
  
3.  <span data-ttu-id="e37f2-118">Ändern Sie den Wert in der **Option Explicit** Feld.</span><span class="sxs-lookup"><span data-stu-id="e37f2-118">Modify the value in the **Option Explicit** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e37f2-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e37f2-119">Example</span></span>  
 <span data-ttu-id="e37f2-120">Der folgende Code wird kompiliert, wenn `/optionexplicit-` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e37f2-120">The following code compiles when `/optionexplicit-` is used.</span></span>  
  
 <span data-ttu-id="e37f2-121">[!code-vb[VbVbalrCompiler&5;](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/optionexplicit_1.vb)]</span><span class="sxs-lookup"><span data-stu-id="e37f2-121">[!code-vb[VbVbalrCompiler#5](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/optionexplicit_1.vb)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e37f2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e37f2-122">See Also</span></span>  
 <span data-ttu-id="e37f2-123">[Visual Basic-Befehlszeilencompiler](../../../visual-basic/reference/command-line-compiler/index.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-123">[Visual Basic Command-Line Compiler](../../../visual-basic/reference/command-line-compiler/index.md) </span></span>  
<span data-ttu-id="e37f2-124"> [/ optioncompare](../../../visual-basic/reference/command-line-compiler/optioncompare.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-124"> [/optioncompare](../../../visual-basic/reference/command-line-compiler/optioncompare.md) </span></span>  
<span data-ttu-id="e37f2-125"> [/ optionstrict](../../../visual-basic/reference/command-line-compiler/optionstrict.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-125"> [/optionstrict](../../../visual-basic/reference/command-line-compiler/optionstrict.md) </span></span>  
<span data-ttu-id="e37f2-126"> [/ optioninfer](../../../visual-basic/reference/command-line-compiler/optioninfer.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-126"> [/optioninfer](../../../visual-basic/reference/command-line-compiler/optioninfer.md) </span></span>  
<span data-ttu-id="e37f2-127"> [Beispiel für Kompilierungsbefehlszeilen](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-127"> [Sample Compilation Command Lines](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md) </span></span>  
<span data-ttu-id="e37f2-128"> [Option Explicit-Anweisung](../../../visual-basic/language-reference/statements/option-explicit-statement.md) </span><span class="sxs-lookup"><span data-stu-id="e37f2-128"> [Option Explicit Statement](../../../visual-basic/language-reference/statements/option-explicit-statement.md) </span></span>  
<span data-ttu-id="e37f2-129"> [VB-Standard, Projekte, Dialogfeld „Optionen“](https://docs.microsoft.com/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="e37f2-129"> [Visual Basic Defaults, Projects, Options Dialog Box](https://docs.microsoft.com/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)</span></span>
