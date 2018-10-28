---
title: Wählen Sie die Version der Visual Basic-Sprache
description: Der Compiler auf, um die Validierung Syntax mit einer bestimmten Compilerversion zu konfigurieren.
ms.date: 05/24/2018
ms.openlocfilehash: 7628b5a7c27f5b26171d42e44a58598ef3d5d49f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194721"
---
# <a name="select-the-visual-basic-language-version"></a><span data-ttu-id="ff4cb-103">Wählen Sie die Version der Visual Basic-Sprache</span><span class="sxs-lookup"><span data-stu-id="ff4cb-103">Select the Visual Basic language version</span></span>

<span data-ttu-id="ff4cb-104">Visual Basic-Compiler standardmäßig die neueste Version der Sprache, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-104">The Visual Basic compiler defaults to the latest major version of the language that has been released.</span></span> <span data-ttu-id="ff4cb-105">Sie können jedes Projekt mit einem neuen Punktrelease der Sprache kompilieren.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-105">You may choose to compile any project using a new point release of the language.</span></span> <span data-ttu-id="ff4cb-106">Mit einer neueren Version der Sprache können Sie die neuesten Sprachfeatures in Ihrem Projekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-106">Choosing a newer version of the language enables your project to make use of the latest language features.</span></span> <span data-ttu-id="ff4cb-107">In anderen Szenarios müssen Sie möglicherweise überprüfen, dass ein Projekt ordnungsgemäß kompiliert wird, wenn Sie eine ältere Version der Sprache verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-107">In other scenarios, you may need to validate that a project compiles cleanly when using an older version of the language.</span></span>

<span data-ttu-id="ff4cb-108">Diese Funktion entkoppelt das Installieren neuer Versionen vom SDK und den Tools in Ihrer Entwicklungsumgebung von der Entscheidung, neue Sprachfeatures in einem Projekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-108">This capability decouples the decision to install new versions of the SDK and tools in your development environment from the decision to incorporate new language features in a project.</span></span> <span data-ttu-id="ff4cb-109">Sie können das neueste SDK und die neuesten Tools auf Ihrem Buildcomputer installieren.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-109">You can install the latest SDK and tools on your build machine.</span></span> <span data-ttu-id="ff4cb-110">Jedes Projekt kann dazu konfiguriert werden, eine spezifische Version der Sprache für das Build zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-110">Each project can be configured to use a specific version of the language for its build.</span></span>

<span data-ttu-id="ff4cb-111">Es gibt drei Möglichkeiten, um die Sprachversion festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ff4cb-111">There are three ways to set the language version:</span></span>

- <span data-ttu-id="ff4cb-112">Manuelles Bearbeiten Ihre [ **vbproj** Datei](#edit-the-vbproj-file)</span><span class="sxs-lookup"><span data-stu-id="ff4cb-112">Manually edit your [**.vbproj** file](#edit-the-vbproj-file)</span></span>
- <span data-ttu-id="ff4cb-113">Legen Sie die Sprachversion [für mehrere Projekte in einem Unterverzeichnis](#configure-multiple-projects)</span><span class="sxs-lookup"><span data-stu-id="ff4cb-113">Set the language version [for multiple projects in a subdirectory](#configure-multiple-projects)</span></span>
- <span data-ttu-id="ff4cb-114">Konfigurieren der [ `-langversion` -Compileroption](#set-the-langversion-compiler-option)</span><span class="sxs-lookup"><span data-stu-id="ff4cb-114">Configure the [`-langversion` compiler option](#set-the-langversion-compiler-option)</span></span>

## <a name="edit-the-vbproj-file"></a><span data-ttu-id="ff4cb-115">Bearbeiten Sie die Vbproj-Datei</span><span class="sxs-lookup"><span data-stu-id="ff4cb-115">Edit the vbproj file</span></span>

<span data-ttu-id="ff4cb-116">Sie können die Sprachversion festlegen, in Ihre **vbproj** Datei.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-116">You can set the language version in your **.vbproj** file.</span></span> <span data-ttu-id="ff4cb-117">Fügen Sie das folgende Element hinzu:</span><span class="sxs-lookup"><span data-stu-id="ff4cb-117">Add the following element:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="ff4cb-118">Der Wert `latest` verwendet die neueste Nebenversion der Visual Basic-Sprache.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-118">The value `latest` uses the latest minor version of the Visual Basic language.</span></span> <span data-ttu-id="ff4cb-119">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ff4cb-119">Valid values are:</span></span>

|<span data-ttu-id="ff4cb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ff4cb-120">Value</span></span>|<span data-ttu-id="ff4cb-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff4cb-121">Meaning</span></span>|
|------------|-------------|
|<span data-ttu-id="ff4cb-122">default</span><span class="sxs-lookup"><span data-stu-id="ff4cb-122">default</span></span>|<span data-ttu-id="ff4cb-123">Der Compiler akzeptiert jede gültige Sprachsyntax der letzten Hauptversion, die unterstützen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-123">The compiler accepts all valid language syntax from the latest major version that it can support.</span></span>|
|<span data-ttu-id="ff4cb-124">9</span><span class="sxs-lookup"><span data-stu-id="ff4cb-124">9</span></span>|<span data-ttu-id="ff4cb-125">Der Compiler akzeptiert nur Syntax, die in Visual Basic 9.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-125">The compiler accepts only syntax that is included in Visual Basic 9.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-126">10</span><span class="sxs-lookup"><span data-stu-id="ff4cb-126">10</span></span>|<span data-ttu-id="ff4cb-127">Der Compiler akzeptiert nur Syntax, die in Visual Basic 10.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-127">The compiler accepts only syntax that is included in Visual Basic 10.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-128">11</span><span class="sxs-lookup"><span data-stu-id="ff4cb-128">11</span></span>|<span data-ttu-id="ff4cb-129">Der Compiler akzeptiert nur Syntax, die in Visual Basic-11.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-129">The compiler accepts only syntax that is included in Visual Basic 11.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-130">12</span><span class="sxs-lookup"><span data-stu-id="ff4cb-130">12</span></span>|<span data-ttu-id="ff4cb-131">Der Compiler akzeptiert nur Syntax, die in Visual Basic-12.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-131">The compiler accepts only syntax that is included in Visual Basic 12.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-132">14</span><span class="sxs-lookup"><span data-stu-id="ff4cb-132">14</span></span>|<span data-ttu-id="ff4cb-133">Der Compiler akzeptiert nur Syntax, die in Visual Basic-14.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-133">The compiler accepts only syntax that is included in Visual Basic 14.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-134">15</span><span class="sxs-lookup"><span data-stu-id="ff4cb-134">15</span></span>|<span data-ttu-id="ff4cb-135">Der Compiler akzeptiert nur Syntax, die in Visual Basic-15.0 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-135">The compiler accepts only syntax that is included in Visual Basic 15.0 or lower.</span></span>|
|<span data-ttu-id="ff4cb-136">15.3</span><span class="sxs-lookup"><span data-stu-id="ff4cb-136">15.3</span></span>|<span data-ttu-id="ff4cb-137">Der Compiler akzeptiert nur Syntax, die in Visual Basic 15.3 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-137">The compiler accepts only syntax that is included in Visual Basic 15.3 or lower.</span></span>|
|<span data-ttu-id="ff4cb-138">15.5</span><span class="sxs-lookup"><span data-stu-id="ff4cb-138">15.5</span></span>|<span data-ttu-id="ff4cb-139">Der Compiler akzeptiert nur Syntax, die in Visual Basic 15.5 oder früher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-139">The compiler accepts only syntax that is included in Visual Basic 15.5 or lower.</span></span>|
|<span data-ttu-id="ff4cb-140">latest</span><span class="sxs-lookup"><span data-stu-id="ff4cb-140">latest</span></span>|<span data-ttu-id="ff4cb-141">Der Compiler akzeptiert alle gültige Sprachsyntax, die es unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-141">The compiler accepts all valid language syntax that it can support.</span></span>|

<span data-ttu-id="ff4cb-142">Die Auflösung der speziellen Zeichenfolgen `default` und `latest` sind die Haupt- und Nebensprachversionen, die jeweils auf dem Buildcomputer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-142">The special strings `default` and `latest` resolve to the latest major and minor language versions installed on the build machine, respectively.</span></span>

## <a name="configure-multiple-projects"></a><span data-ttu-id="ff4cb-143">Konfigurieren mehrerer Projekte</span><span class="sxs-lookup"><span data-stu-id="ff4cb-143">Configure multiple projects</span></span>

<span data-ttu-id="ff4cb-144">Sie können eine **Directory.build.props**-Datei erstellen, die das Element `<LangVersion>` enthält, um mehrere Verzeichnisse zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-144">You can create a **Directory.build.props** file that contains the `<LangVersion>` element to configure multiple directories.</span></span> <span data-ttu-id="ff4cb-145">In der Regel führen Sie dies im Projektmappenverzeichnis durch.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-145">You typically do that in your solution directory.</span></span> <span data-ttu-id="ff4cb-146">Fügen Sie Folgendes in eine **Directory.build.props**-Datei in Ihrem Projektmappenverzeichnis ein:</span><span class="sxs-lookup"><span data-stu-id="ff4cb-146">Add the following to a **Directory.build.props** file in your solution directory:</span></span>

```xml
<Project>
 <PropertyGroup>
   <LangVersion>15.5</LangVersion>
 </PropertyGroup>
</Project>
```

<span data-ttu-id="ff4cb-147">Builds in jedes Unterverzeichnis des Verzeichnisses, enthält diese Datei werden jetzt Visual Basic-Version 15.5-Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-147">Now, builds in every subdirectory of the directory containing that file will use Visual Basic version 15.5 syntax.</span></span> <span data-ttu-id="ff4cb-148">Weitere Informationen finden Sie im Artikel zum [Anpassen Ihres Builds](/visualstudio/msbuild/customize-your-build.md).</span><span class="sxs-lookup"><span data-stu-id="ff4cb-148">For more information, see the article on [Customize your build](/visualstudio/msbuild/customize-your-build.md).</span></span>

## <a name="set-the-langversion-compiler-option"></a><span data-ttu-id="ff4cb-149">Festlegen der Compileroption „langversion“</span><span class="sxs-lookup"><span data-stu-id="ff4cb-149">Set the langversion compiler option</span></span>

<span data-ttu-id="ff4cb-150">Sie können die Befehlszeilenoption `-langversion` verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-150">You can use the `-langversion` command-line option.</span></span> <span data-ttu-id="ff4cb-151">Weitere Informationen finden Sie im Artikel zur Compileroption [-langversion](../reference/command-line-compiler/langversion.md).</span><span class="sxs-lookup"><span data-stu-id="ff4cb-151">For more information, see the article on the [-langversion](../reference/command-line-compiler/langversion.md) compiler option.</span></span> <span data-ttu-id="ff4cb-152">Sie können eine Liste der gültigen Werte anzeigen, indem Sie die Eingabe `vbc -langversion:?` .</span><span class="sxs-lookup"><span data-stu-id="ff4cb-152">You can see a list of the valid values by typing  `vbc -langversion:?` .</span></span>