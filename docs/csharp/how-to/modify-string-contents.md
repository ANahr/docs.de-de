---
title: "Vorgehensweise: Ändern von Zeichenfolgeninhalten (C#-Leitfaden)"
ms.date: 02/26/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- strings [C#], modifying
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: a67cf24c0f6024d23bc1106943d3447620f18b1f
ms.sourcegitcommit: d95a91d685565f4d95c8773b558752864a6a3d7e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2018
---
# <a name="how-to-modify-string-contents-in-c"></a><span data-ttu-id="78052-102">Vorgehensweise: Ändern von Zeichenfolgeninhalten in C#</span><span class="sxs-lookup"><span data-stu-id="78052-102">How to: Modify string contents in C#</span></span> #

<span data-ttu-id="78052-103">In diesem Artikel werden verschiedene Methoden zum Erzeugen einer `string` durch Modifizieren einer vorhandenen `string` erläutert.</span><span class="sxs-lookup"><span data-stu-id="78052-103">This article demonstrates several techniques to produce a `string` by modifying an existing `string`.</span></span> <span data-ttu-id="78052-104">Alle diese gezeigten Methoden geben das Ergebnis der Modifizierung als neues `string`-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="78052-104">All the techniques demonstrated return the result of the modifications as a new `string` object.</span></span> <span data-ttu-id="78052-105">Um dies deutlich zu machen, wird das Ergebnis in den Beispielen als neue Variable gespeichert.</span><span class="sxs-lookup"><span data-stu-id="78052-105">To clearly demonstrate this, the examples all store the result in a new variable.</span></span> <span data-ttu-id="78052-106">Dann können Sie sich sowohl die ursprüngliche `string` als auch die `string` ansehen, die durch die Modifizierung beim Ausführen jedes Beispiels entsteht.</span><span class="sxs-lookup"><span data-stu-id="78052-106">You can then examine both the original `string` and the `string` resulting from the modification when you run each example.</span></span>

<span data-ttu-id="78052-107">In diesem Artikel werden mehrere Methoden aufgezeigt.</span><span class="sxs-lookup"><span data-stu-id="78052-107">There are several techniques demonstrated in this article.</span></span> <span data-ttu-id="78052-108">Sie können vorhandenen Text ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78052-108">You can replace existing text.</span></span> <span data-ttu-id="78052-109">Sie können nach Mustern suchen und übereinstimmenden Text durch anderen Text ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78052-109">You can search for patterns and replace matching text with other text.</span></span> <span data-ttu-id="78052-110">Sie können Zeichenfolgen als Zeichensequenzen behandeln.</span><span class="sxs-lookup"><span data-stu-id="78052-110">You can treat a string as a sequence of characters.</span></span> <span data-ttu-id="78052-111">Sie können zudem Hilfsmethoden verwenden, die Leerräume entfernen.</span><span class="sxs-lookup"><span data-stu-id="78052-111">You can also use convenience methods that remove white space.</span></span> <span data-ttu-id="78052-112">Sie sollten sich für die Methoden entscheiden, die am besten zu Ihrem Szenario passen.</span><span class="sxs-lookup"><span data-stu-id="78052-112">You should choose the techniques that most closely match your scenario.</span></span>

## <a name="replace-text"></a><span data-ttu-id="78052-113">Ersetzen von Text</span><span class="sxs-lookup"><span data-stu-id="78052-113">Replace text</span></span>

<span data-ttu-id="78052-114">Der folgende Code erstellt eine neue Zeichenfolge, indem er vorhandenen Text ersetzt.</span><span class="sxs-lookup"><span data-stu-id="78052-114">The following code creates a new string by replacing existing text with a substitute.</span></span>

[!code-csharp-interactive[replace creates a new string](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#1)]

<span data-ttu-id="78052-115">Der vorherige Code veranschaulicht diese *unveränderliche* Eigenschaft von Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="78052-115">The preceding code demonstrates this *immutable* property of strings.</span></span> <span data-ttu-id="78052-116">Im vorherigen Beispiel können Sie sehen, dass die ursprüngliche Zeichenfolge `source` nicht modifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="78052-116">You can see in the preceding example that the original string, `source`, is not modified.</span></span> <span data-ttu-id="78052-117">Die Methode <xref:System.String.Replace%2A?displayProperty=nameWithType> erstellt eine neue `string`, die die Modifizierungen enthält.</span><span class="sxs-lookup"><span data-stu-id="78052-117">The <xref:System.String.Replace%2A?displayProperty=nameWithType> method creates a new `string` containing the modifications.</span></span>

<span data-ttu-id="78052-118">Die Methode <xref:System.String.Replace%2A> kann entweder Zeichenfolgen oder einzelne Zeichen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78052-118">The <xref:System.String.Replace%2A> method can replace either strings or single characters.</span></span> <span data-ttu-id="78052-119">In beiden Fällen wird jedes Vorkommen des gesuchten Texts ersetzt.</span><span class="sxs-lookup"><span data-stu-id="78052-119">In both cases, every occurrence of the sought text is replaced.</span></span>  <span data-ttu-id="78052-120">In folgendem Beispiel werden alle „ “-Zeichen durch \_ ersetzt:</span><span class="sxs-lookup"><span data-stu-id="78052-120">The following example replaces all ' ' characters with '\_':</span></span>

[!code-csharp-interactive[replace characters](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#2)]

<span data-ttu-id="78052-121">Die Quellzeichenfolge bleibt unverändert, und es wird eine neue Zeichenfolge mit der Ersetzung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78052-121">The source string is unchanged, and a new string is returned with the replacement.</span></span>

## <a name="trim-white-space"></a><span data-ttu-id="78052-122">Entfernen von Leerräumen</span><span class="sxs-lookup"><span data-stu-id="78052-122">Trim white space</span></span>

<span data-ttu-id="78052-123">Sie können die Methoden <xref:System.String.Trim%2A?displayProperty=nameWithType>, <xref:System.String.TrimStart%2A?displayProperty=nameWithType> und <xref:System.String.TrimEnd%2A?displayProperty=nameWithType> verwenden, um führende oder nachfolgende Leerräume zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="78052-123">You can use the <xref:System.String.Trim%2A?displayProperty=nameWithType>, <xref:System.String.TrimStart%2A?displayProperty=nameWithType>, and <xref:System.String.TrimEnd%2A?displayProperty=nameWithType> methods to remove any leading or trailing white space.</span></span>  <span data-ttu-id="78052-124">Im folgenden Code ist ein Beispiel für jede Methode dargestellt.</span><span class="sxs-lookup"><span data-stu-id="78052-124">The following code shows an example of each.</span></span> <span data-ttu-id="78052-125">Die Quellzeichenfolge bleibt unverändert. Diese Methoden geben eine neue Zeichenfolge mit modifiziertem Inhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="78052-125">The source string does not change; these methods return a new string with the modified contents.</span></span>

[!code-csharp-interactive[trim white space](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#3)]

## <a name="remove-text"></a><span data-ttu-id="78052-126">Entfernen von Text</span><span class="sxs-lookup"><span data-stu-id="78052-126">Remove text</span></span>

<span data-ttu-id="78052-127">Mit der Methode <xref:System.String.Remove%2A?displayProperty=nameWithType> können Sie Text aus einer Zeichenfolge entfernen.</span><span class="sxs-lookup"><span data-stu-id="78052-127">You can remove text from a string using the <xref:System.String.Remove%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="78052-128">Diese Methode entfernt mehrere Zeichen ab einem spezifischen Index.</span><span class="sxs-lookup"><span data-stu-id="78052-128">This method removes a number of characters starting at a specific index.</span></span> <span data-ttu-id="78052-129">In folgendem Beispiel wird gezeigt, wie Sie <xref:System.String.IndexOf%2A?displayProperty=nameWithType> gefolgt von <xref:System.String.Remove%2A> verwenden können, um Text aus einer Zeichenfolge zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="78052-129">The following example shows how to use <xref:System.String.IndexOf%2A?displayProperty=nameWithType> followed by <xref:System.String.Remove%2A> to remove text from a string:</span></span>

[!code-csharp-interactive[remove text](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#4)]

## <a name="replace-matching-patterns"></a><span data-ttu-id="78052-130">Ersetzen von übereinstimmenden Mustern</span><span class="sxs-lookup"><span data-stu-id="78052-130">Replace matching patterns</span></span>

<span data-ttu-id="78052-131">Sie können [reguläre Ausdrücke](../../standard/base-types/regular-expressions.md) verwenden, um Text, der mit Mustern übereinstimmt, durch neuen Text zu ersetzen, der auch durch ein Muster definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="78052-131">You can use [regular expressions](../../standard/base-types/regular-expressions.md) to replace text matching patterns with new text, possibly defined by a pattern.</span></span> <span data-ttu-id="78052-132">In folgendem Beispiel wird die Klasse <xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> verwendet, um ein Muster in einer Quellzeichenfolge zu finden und dieses durch Text mit korrekter Großschreibung zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78052-132">The following example uses the <xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> class to find a pattern in a source string and replace it with proper capitalization.</span></span> <span data-ttu-id="78052-133">Die Methode <xref:System.Text.RegularExpressions.Regex.Replace(System.String,System.String,System.Text.RegularExpressions.MatchEvaluator,System.Text.RegularExpressions.RegexOptions)?displayProperty=nameWithType> akzeptiert eine Funktion, die die Logik der Ersetzung als eines ihrer Argumente bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="78052-133">The <xref:System.Text.RegularExpressions.Regex.Replace(System.String,System.String,System.Text.RegularExpressions.MatchEvaluator,System.Text.RegularExpressions.RegexOptions)?displayProperty=nameWithType> method takes a function that provides the logic of the replacement as one of its arguments.</span></span> <span data-ttu-id="78052-134">In diesem Beispiel ist diese Funktion `LocalReplaceMatchCase` eine **lokale Funktion**, die in der Beispielmethode deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="78052-134">In this example, that function, `LocalReplaceMatchCase` is a **local function** declared inside the sample method.</span></span> <span data-ttu-id="78052-135">`LocalReplaceMatchCase` verwendet die <xref:System.Text.StringBuilder?displayProperty=nameWithType>-Klasse zum Erstellen der Ersatzzeichenfolge mit korrekter Großschreibung.</span><span class="sxs-lookup"><span data-stu-id="78052-135">`LocalReplaceMatchCase` uses the <xref:System.Text.StringBuilder?displayProperty=nameWithType> class to build the replacement string with proper capitalization.</span></span>

<span data-ttu-id="78052-136">Reguläre Ausdrücke sind besonders beim Suchen und Ersetzen von Text nützlich, der einem bestimmten Muster folgt, und nicht so sehr bei bekanntem Text.</span><span class="sxs-lookup"><span data-stu-id="78052-136">Regular expressions are most useful for searching and replacing text that follows a pattern, rather than known text.</span></span> <span data-ttu-id="78052-137">Weitere Informationen finden Sie unter [Vorgehensweise: Durchsuchen von Zeichenfolgen](search-strings.md).</span><span class="sxs-lookup"><span data-stu-id="78052-137">See [How to: search strings](search-strings.md) for more details.</span></span> <span data-ttu-id="78052-138">Das Suchmuster „the\s“ sucht nach dem Wort „the“ gefolgt von einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="78052-138">The search pattern, "the\s" searches for the word "the" followed by a white-space character.</span></span> <span data-ttu-id="78052-139">Der Teil des Musters stellt sicher, das es nicht „there“ als Übereinstimmung in der Quellzeichenfolge ansieht.</span><span class="sxs-lookup"><span data-stu-id="78052-139">That part of the pattern ensures that it doesn't match "there" in the source string.</span></span> <span data-ttu-id="78052-140">Weitere Informationen zur Sprache für reguläre Ausdrücke finden Sie unter [Sprachelemente für reguläre Ausdrücke – Kurzübersicht](../../standard/base-types/regular-expression-language-quick-reference.md).</span><span class="sxs-lookup"><span data-stu-id="78052-140">For more information on regular expression language elements, see [Regular Expression Language - Quick Reference](../../standard/base-types/regular-expression-language-quick-reference.md).</span></span>

[!code-csharp-interactive[replace creates a new string](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#5)]

<span data-ttu-id="78052-141">Die Methode <xref:System.Text.StringBuilder.ToString%2A?displayProperty=nameWithType> gibt eine unveränderliche Zeichenfolge zurück, die den Inhalt im <xref:System.Text.StringBuilder>-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="78052-141">The <xref:System.Text.StringBuilder.ToString%2A?displayProperty=nameWithType> method returns an immutable string with the contents in the <xref:System.Text.StringBuilder> object.</span></span>

## <a name="modifying-individual-characters"></a><span data-ttu-id="78052-142">Modifizieren einzelner Zeichen</span><span class="sxs-lookup"><span data-stu-id="78052-142">Modifying individual characters</span></span>

<span data-ttu-id="78052-143">Sie können ein Zeichenarray aus einer Zeichenfolge erzeugen, den Inhalt des Arrays modifizieren und dann eine neue Zeichenfolge aus dem modifizierten Inhalt des Arrays erstellen.</span><span class="sxs-lookup"><span data-stu-id="78052-143">You can produce a character array from a string, modify the contents of the array, and then create a new string from the modified contents of the array.</span></span>

<span data-ttu-id="78052-144">In folgendem Beispiel wird gezeigt, wie Sie mehrere Zeichen in einer Zeichenfolge ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78052-144">The following example shows how to replace a set of characters in a string.</span></span> <span data-ttu-id="78052-145">Zunächst wird die Methode <xref:System.String.ToCharArray?displayProperty=nameWithName> verwendet, um ein Zeichenarray zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78052-145">First, it uses the <xref:System.String.ToCharArray?displayProperty=nameWithName> method to create an array of characters.</span></span> <span data-ttu-id="78052-146">Die Methode <xref:System.String.IndexOf%2A> wird verwendet, um den Startindex des Worts „fox“ zu finden.</span><span class="sxs-lookup"><span data-stu-id="78052-146">It uses the <xref:System.String.IndexOf%2A> method to find the starting index of the word "fox."</span></span> <span data-ttu-id="78052-147">Die folgenden drei Zeichen werden durch ein anderes Wort ersetzt.</span><span class="sxs-lookup"><span data-stu-id="78052-147">The next three characters are replaced with a different word.</span></span> <span data-ttu-id="78052-148">Zum Schluss wird eine neue Zeichenfolge aus dem aktualisierten Zeichenarray erstellt.</span><span class="sxs-lookup"><span data-stu-id="78052-148">Finally, a new string is constructed from the updated character array.</span></span>

[!code-csharp-interactive[replace creates a new string](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#6)]

## <a name="unsafe-modifications-to-string"></a><span data-ttu-id="78052-149">Unsichere Modifizierung einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="78052-149">Unsafe modifications to string</span></span>

<span data-ttu-id="78052-150">Mit **unsicherem Code** können Sie eine Zeichenfolge „direkt“ modifizieren, nachdem sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="78052-150">Using **unsafe** code, you can modify a string "in place" after it has been created.</span></span> <span data-ttu-id="78052-151">Unsicherer Code umgeht viele der Features von .NET, die dazu gedacht sind, bestimmte Fehler in Code zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="78052-151">Unsafe code bypasses many of the features of .NET designed to minimize certain types of bugs in code.</span></span> <span data-ttu-id="78052-152">Sie müssen unsicheren Code verwenden, um eine Zeichenfolge direkt zu modifizieren, weil die Zeichenfolgenklasse als **unveränderlicher** Typ konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="78052-152">You need to use unsafe code to modify a string in place because the string class is designed as an **immutable** type.</span></span> <span data-ttu-id="78052-153">Sobald Sie erstellt wurde, kann ihr Wert nicht verändert werden.</span><span class="sxs-lookup"><span data-stu-id="78052-153">Once it has been created, its value does not change.</span></span> <span data-ttu-id="78052-154">Unsicherer Code umgeht diese Eigenschaft, indem er auf den Speicher zugreift und diesen modifiziert, der von einer `string` verwendet wird, ohne normale `string`-Methoden zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="78052-154">Unsafe code circumvents this property by accessing and modifying the memory used by a `string` without using normal `string` methods.</span></span>
<span data-ttu-id="78052-155">Das folgende Beispiel können Sie verwenden, falls Sie eine Zeichenfolge direkt mit unsicherem Code modifizieren möchte. Dies kommt jedoch sehr selten vor.</span><span class="sxs-lookup"><span data-stu-id="78052-155">The following example is provided for those rare situations where you want to modify a string in-place using unsafe code.</span></span> <span data-ttu-id="78052-156">Im folgenden Beispiel wird die Verwendung des Schlüsselworts `fixed` veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="78052-156">The example shows how to use the `fixed` keyword.</span></span> <span data-ttu-id="78052-157">Das Schlüsselwort `fixed` verhindert, dass der Garbage Collector (GC) das Zeichenfolgenobjekt im Speicher verschiebt, während der Code mit einem unsicheren Zeiger auf den Speicher zugreift.</span><span class="sxs-lookup"><span data-stu-id="78052-157">The `fixed` keyword prevents the garbage collector (GC) from moving the string object in memory while code accesses the memory using the unsafe pointer.</span></span> <span data-ttu-id="78052-158">Darüber hinaus wird ein möglicher Nebeneffekt unsicherer Vorgänge auf Zeichenfolgen gezeigt, die daraus entstehen, dass der C#-Compiler Zeichenfolgen intern speichert (hält).</span><span class="sxs-lookup"><span data-stu-id="78052-158">It also demonstrates one possible side effect of unsafe operations on strings that results from the way that the C# compiler stores (interns) strings internally.</span></span> <span data-ttu-id="78052-159">Im Allgemeinen sollten Sie dieses Verfahren nicht verwenden, es sei denn, es ist unbedingt notwendig.</span><span class="sxs-lookup"><span data-stu-id="78052-159">In general, you shouldn't use this technique unless it is absolutely necessary.</span></span> <span data-ttu-id="78052-160">Weitere Informationen erhalten Sie in den Artikeln zu [unsafe](../language-reference/keywords/unsafe.md) und [fixed](../language-reference/keywords/fixed-statement.md).</span><span class="sxs-lookup"><span data-stu-id="78052-160">You can learn more in the articles on [unsafe](../language-reference/keywords/unsafe.md) and [fixed](../language-reference/keywords/fixed-statement.md).</span></span> <span data-ttu-id="78052-161">Die API-Referenz für <xref:System.String.Intern%2A> enthält Informationen zum Internalisieren von Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="78052-161">The API reference for <xref:System.String.Intern%2A> includes inforamtion on string interning.</span></span>

[!code-csharp-interactive[unsafe ways to create a new string](../../../samples/snippets/csharp/how-to/strings/ModifyStrings.cs#7)]

<span data-ttu-id="78052-162">Sie können diese Beispiele ausprobieren, indem Sie sich den Code in unserem [GitHub-Repository](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings) ansehen.</span><span class="sxs-lookup"><span data-stu-id="78052-162">You can try these samples by looking at the code in our [GitHub repository](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings).</span></span> <span data-ttu-id="78052-163">Alternativ dazu können Sie die Beispiele [als ZIP-Datei](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings.zip) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="78052-163">Or you can download the samples [as a zip file](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings.zip).</span></span>

## <a name="see-also"></a><span data-ttu-id="78052-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78052-164">See also</span></span>

[<span data-ttu-id="78052-165">Reguläre Ausdrücke von .NET Framework</span><span class="sxs-lookup"><span data-stu-id="78052-165">.NET Framework Regular Expressions</span></span>](../../standard/base-types/regular-expressions.md)  
 [<span data-ttu-id="78052-166">Sprachelemente für reguläre Ausdrücke – Kurzübersicht</span><span class="sxs-lookup"><span data-stu-id="78052-166">Regular Expression Language - Quick Reference</span></span>](../../standard/base-types/regular-expression-language-quick-reference.md)  