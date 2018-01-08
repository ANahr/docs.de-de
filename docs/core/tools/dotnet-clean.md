---
title: "dotnet clean-Befehl – .NET Core-CLI"
description: "Mit dem Befehl „dotnet clean“ wird das aktuelle Verzeichnis bereinigt."
author: mairaw
ms.author: mairaw
ms.date: 08/13/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.workload: dotnetcore
ms.openlocfilehash: f56ccc485884114262cd1364cf9398e302f2c48a
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/23/2017
---
# <a name="dotnet-clean"></a><span data-ttu-id="2532b-103">dotnet-clean</span><span class="sxs-lookup"><span data-stu-id="2532b-103">dotnet-clean</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="2532b-104">name</span><span class="sxs-lookup"><span data-stu-id="2532b-104">Name</span></span>

<span data-ttu-id="2532b-105">`dotnet clean`: Löscht die Ausgabe eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="2532b-105">`dotnet clean` - Cleans the output of a project.</span></span>

## <a name="synopsis"></a><span data-ttu-id="2532b-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2532b-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="2532b-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="2532b-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="2532b-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="2532b-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-v|--verbosity]
dotnet clean [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="2532b-109">description</span><span class="sxs-lookup"><span data-stu-id="2532b-109">Description</span></span>

<span data-ttu-id="2532b-110">Der Befehl `dotnet clean` löscht die Ausgabe des vorherigen Builds.</span><span class="sxs-lookup"><span data-stu-id="2532b-110">The `dotnet clean` command cleans the output of the previous build.</span></span> <span data-ttu-id="2532b-111">Er ist als [MSBuild-Ziel](/visualstudio/msbuild/msbuild-targets) implementiert, sodass das Projekt ausgewertet wird, wenn der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2532b-111">It's implemented as an [MSBuild target](/visualstudio/msbuild/msbuild-targets), so the project is evaluated when the command is run.</span></span> <span data-ttu-id="2532b-112">Es werden nur die Ausgaben gelöscht, die während des Builds erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2532b-112">Only the outputs created during the build are cleaned.</span></span> <span data-ttu-id="2532b-113">Sowohl der Ordner für Zwischenausgabe (*obj*) als auch der Ordner für die endgültige Ausgabe (*bin*) werden bereinigt.</span><span class="sxs-lookup"><span data-stu-id="2532b-113">Both intermediate (*obj*) and final output (*bin*) folders are cleaned.</span></span>

## <a name="arguments"></a><span data-ttu-id="2532b-114">Argumente</span><span class="sxs-lookup"><span data-stu-id="2532b-114">Arguments</span></span>

`PROJECT`

<span data-ttu-id="2532b-115">Das zu bereinigende MSBuild-Projekt.</span><span class="sxs-lookup"><span data-stu-id="2532b-115">The MSBuild project to clean.</span></span> <span data-ttu-id="2532b-116">Wenn Sie keine Projektdatei angeben, durchsucht MSBuild das aktuelle Arbeitsverzeichnis nach einer Dateierweiterung, die mit *proj* endet, und verwendet diese.</span><span class="sxs-lookup"><span data-stu-id="2532b-116">If a project file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in *proj* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="2532b-117">Optionen</span><span class="sxs-lookup"><span data-stu-id="2532b-117">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="2532b-118">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="2532b-118">.NET Core 2.x</span></span>](#tab/netcore2x)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="2532b-119">Legt die Buildkonfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="2532b-119">Defines the build configuration.</span></span> <span data-ttu-id="2532b-120">Der Standardwert ist `Debug`.</span><span class="sxs-lookup"><span data-stu-id="2532b-120">The default value is `Debug`.</span></span> <span data-ttu-id="2532b-121">Diese Option ist bei der Bereinigung nur erforderlich, wenn Sie sie bei der Erstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2532b-121">This option is only required when cleaning if you specified it during build time.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="2532b-122">Das [Framework](../../standard/frameworks.md), das bei der Erstellung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2532b-122">The [framework](../../standard/frameworks.md) that was specified at build time.</span></span> <span data-ttu-id="2532b-123">Das Framework muss in der [Projektdatei](csproj.md) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2532b-123">The framework must be defined in the [project file](csproj.md).</span></span> <span data-ttu-id="2532b-124">Wenn Sie das Framework bei der Erstellung angegeben haben, müssen Sie das Framework bei der Bereinigung angeben.</span><span class="sxs-lookup"><span data-stu-id="2532b-124">If you specified the framework at build time, you must specify the framework when cleaning.</span></span>

`-h|--help`

<span data-ttu-id="2532b-125">Druckt eine kurze Hilfe für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="2532b-125">Prints out a short help for the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="2532b-126">Verzeichnis, in dem die Buildausgaben abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="2532b-126">Directory in which the build outputs are placed.</span></span> <span data-ttu-id="2532b-127">Geben Sie den `-f|--framework <FRAMEWORK>`-Schalter mit dem Schalter des Ausgabeverzeichnisses an, wenn Sie das Framework bei der Erstellung des Projekts angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2532b-127">Specify the `-f|--framework <FRAMEWORK>` switch with the output directory switch if you specified the framework when the project was built.</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="2532b-128">Bereinigt den Ausgabeordner der angegebenen Runtime</span><span class="sxs-lookup"><span data-stu-id="2532b-128">Cleans the output folder of the specified runtime.</span></span> <span data-ttu-id="2532b-129">Wird bei der Erstellung einer [eigenständigen Bereitstellung](../deploying/index.md#self-contained-deployments-scd) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2532b-129">This is used when a [self-contained deployment](../deploying/index.md#self-contained-deployments-scd) was created.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="2532b-130">Legt den Ausführlichkeitsgrad für den Befehl fest.</span><span class="sxs-lookup"><span data-stu-id="2532b-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="2532b-131">Zulässige Grade sind q[uiet], m[inimal], n[ormal], d[etailed] und diag[nostic].</span><span class="sxs-lookup"><span data-stu-id="2532b-131">Allowed levels are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="2532b-132">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="2532b-132">.NET Core 1.x</span></span>](#tab/netcore1x)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="2532b-133">Legt die Buildkonfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="2532b-133">Defines the build configuration.</span></span> <span data-ttu-id="2532b-134">Der Standardwert ist `Debug`.</span><span class="sxs-lookup"><span data-stu-id="2532b-134">The default value is `Debug`.</span></span> <span data-ttu-id="2532b-135">Diese Option ist bei der Bereinigung nur erforderlich, wenn Sie sie bei der Erstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2532b-135">This option is only required when cleaning if you specified it during build time.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="2532b-136">Das [Framework](../../standard/frameworks.md), das bei der Erstellung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2532b-136">The [framework](../../standard/frameworks.md) that was specified at build time.</span></span> <span data-ttu-id="2532b-137">Das Framework muss in der [Projektdatei](csproj.md) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2532b-137">The framework must be defined in the [project file](csproj.md).</span></span> <span data-ttu-id="2532b-138">Wenn Sie das Framework bei der Erstellung angegeben haben, müssen Sie das Framework bei der Bereinigung angeben.</span><span class="sxs-lookup"><span data-stu-id="2532b-138">If you specified the framework at build time, you must specify the framework when cleaning.</span></span>

`-h|--help`

<span data-ttu-id="2532b-139">Druckt eine kurze Hilfe für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="2532b-139">Prints out a short help for the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="2532b-140">Verzeichnis, in dem die Buildausgaben abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="2532b-140">Directory in which the build outputs are placed.</span></span> <span data-ttu-id="2532b-141">Geben Sie den `-f|--framework <FRAMEWORK>`-Schalter mit dem Schalter des Ausgabeverzeichnisses an, wenn Sie das Framework bei der Erstellung des Projekts angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2532b-141">Specify the `-f|--framework <FRAMEWORK>` switch with the output directory switch if you specified the framework when the project was built.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="2532b-142">Legt den Ausführlichkeitsgrad für den Befehl fest.</span><span class="sxs-lookup"><span data-stu-id="2532b-142">Sets the verbosity level of the command.</span></span> <span data-ttu-id="2532b-143">Zulässige Grade sind q[uiet], m[inimal], n[ormal], d[etailed] und diag[nostic].</span><span class="sxs-lookup"><span data-stu-id="2532b-143">Allowed levels are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].</span></span>

---

## <a name="examples"></a><span data-ttu-id="2532b-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2532b-144">Examples</span></span>

<span data-ttu-id="2532b-145">Bereinigen Sie einen Standardbuild des Projekts:</span><span class="sxs-lookup"><span data-stu-id="2532b-145">Clean a default build of the project:</span></span>

`dotnet clean`

<span data-ttu-id="2532b-146">Bereinigen Sie ein Projektbuild mit der Konfiguration „Release“:</span><span class="sxs-lookup"><span data-stu-id="2532b-146">Clean a project built using the Release configuration:</span></span>

`dotnet clean --configuration Release`
