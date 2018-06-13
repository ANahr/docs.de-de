---
title: -optionexplicit
ms.date: 07/20/2015
f1_keywords:
- /optionexplicit
- -optionexplicit
helpviewer_keywords:
- /optionexplicit compiler option [Visual Basic]
- optionexplicit compiler option [Visual Basic]
- -optionexplicit compiler option [Visual Basic]
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
ms.openlocfilehash: 072a816f189a772543fbbd63e7202441469c0177
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653597"
---
# <a name="-optionexplicit"></a><span data-ttu-id="5ef46-102">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="5ef46-102">-optionexplicit</span></span>
<span data-ttu-id="5ef46-103">Bewirkt, dass der Compiler gemeldet, wenn keine Variablen deklariert werden, bevor sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ef46-103">Causes the compiler to report errors if variables are not declared before they are used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ef46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef46-104">Syntax</span></span>  
  
```  
-optionexplicit[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="5ef46-105">Argumente</span><span class="sxs-lookup"><span data-stu-id="5ef46-105">Arguments</span></span>  
 <span data-ttu-id="5ef46-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="5ef46-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="5ef46-107">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5ef46-107">Optional.</span></span> <span data-ttu-id="5ef46-108">Geben Sie `-optionexplicit+` explizite Deklaration von Variablen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5ef46-108">Specify `-optionexplicit+` to require explicit declaration of variables.</span></span> <span data-ttu-id="5ef46-109">Die `-optionexplicit+` Option ist die Standardeinstellung und entspricht dem `-optionexplicit`.</span><span class="sxs-lookup"><span data-stu-id="5ef46-109">The `-optionexplicit+` option is the default and is the same as `-optionexplicit`.</span></span> <span data-ttu-id="5ef46-110">Die `-optionexplicit-` Option ermöglicht die implizite Deklaration von Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ef46-110">The `-optionexplicit-` option enables implicit declaration of variables.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5ef46-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ef46-111">Remarks</span></span>  
 <span data-ttu-id="5ef46-112">Wenn die Quellcodedatei enthält eine [Option Explicit-Anweisung](../../../visual-basic/language-reference/statements/option-explicit-statement.md), überschreibt die Anweisung die `-optionexplicit` Befehlszeilencompiler-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5ef46-112">If the source code file contains an [Option Explicit statement](../../../visual-basic/language-reference/statements/option-explicit-statement.md), the statement overrides the `-optionexplicit` command-line compiler setting.</span></span>  
  
### <a name="to-set--optionexplicit-in-the-visual-studio-ide"></a><span data-ttu-id="5ef46-113">-Optionexplicit in der Visual Studio-IDE festlegen</span><span class="sxs-lookup"><span data-stu-id="5ef46-113">To set -optionexplicit in the Visual Studio IDE</span></span>  
  
1.  <span data-ttu-id="5ef46-114">Ein Projekt auswählen in **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="5ef46-114">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="5ef46-115">Klicken Sie im Menü **Projekt** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="5ef46-115">On the **Project** menu, click **Properties**.</span></span>   
  
2.  <span data-ttu-id="5ef46-116">Klicken Sie auf die Registerkarte **Kompilieren**.</span><span class="sxs-lookup"><span data-stu-id="5ef46-116">Click the **Compile** tab.</span></span>  
  
3.  <span data-ttu-id="5ef46-117">Ändern Sie den Wert in der **Option Explicit** Feld.</span><span class="sxs-lookup"><span data-stu-id="5ef46-117">Modify the value in the **Option Explicit** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ef46-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ef46-118">Example</span></span>  
 <span data-ttu-id="5ef46-119">Im folgende Code wird kompiliert, wenn `-optionexplicit-` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ef46-119">The following code compiles when `-optionexplicit-` is used.</span></span>  
  
 [!code-vb[VbVbalrCompiler#5](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/optionexplicit_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="5ef46-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ef46-120">See Also</span></span>  
 [<span data-ttu-id="5ef46-121">Visual Basic-Befehlszeilencompiler</span><span class="sxs-lookup"><span data-stu-id="5ef46-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="5ef46-122">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="5ef46-122">-optioncompare</span></span>](../../../visual-basic/reference/command-line-compiler/optioncompare.md)  
 [<span data-ttu-id="5ef46-123">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="5ef46-123">-optionstrict</span></span>](../../../visual-basic/reference/command-line-compiler/optionstrict.md)  
 [<span data-ttu-id="5ef46-124">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="5ef46-124">-optioninfer</span></span>](../../../visual-basic/reference/command-line-compiler/optioninfer.md)  
 [<span data-ttu-id="5ef46-125">Beispiele für Kompilierungsbefehlszeilen</span><span class="sxs-lookup"><span data-stu-id="5ef46-125">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="5ef46-126">Option Explicit-Anweisung</span><span class="sxs-lookup"><span data-stu-id="5ef46-126">Option Explicit Statement</span></span>](../../../visual-basic/language-reference/statements/option-explicit-statement.md)  
 [<span data-ttu-id="5ef46-127">VB-Standard, Projekte, Dialogfeld „Optionen“</span><span class="sxs-lookup"><span data-stu-id="5ef46-127">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
