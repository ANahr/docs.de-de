---
title: Zeichenfolgen – C#-Programmierhandbuch
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, strings
- strings [C#]
ms.assetid: 21580405-cb25-4541-89d5-037846a38b07
ms.openlocfilehash: ba0c9abe9a38962ab19a204019abd3ac89ae6915
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236361"
---
# <a name="strings-c-programming-guide"></a>Zeichenfolgen (C#-Programmierhandbuch)
Eine Zeichenfolge ist ein Objekt des Typs <xref:System.String>, dessen Wert Text ist. Intern wird der Text als sequenzielle schreibgeschützte Auflistung von <xref:System.Char>-Objekten gespeichert. Es gibt kein mit NULL endendes Zeichen am Ende einer C#-Zeichenfolge. Deshalb kann eine C#-Zeichenfolge eine beliebige Anzahl eingebetteter NULL-Zeichen („\0“) enthalten. Die Eigenschaft <xref:System.String.Length%2A> einer Zeichenfolge stellt die Anzahl von `Char`-Objekten dar, die darin enthalten sind, nicht die Anzahl der Unicode-Zeichen. Verwenden Sie für den Zugriff auf einzelne Unicode-Codepunkte in einer Zeichenfolge das Objekt <xref:System.Globalization.StringInfo>.  
  
## <a name="string-vs-systemstring"></a>String im Vergleich zu System.String  
 In C# ist das Schlüsselwort `string` ein Alias für <xref:System.String>. Aus diesem Grund sind `String` und `string` gleich, und Sie können eine beliebige Benennungskonvention verwenden. Die `String`-Klasse bietet viele Methoden zum sicheren Erstellen, Bearbeiten und Vergleichen von Zeichenfolgen. Außerdem überlädt die Programmiersprache C# einige Operatoren, um allgemeine Zeichenfolgenoperationen zu vereinfachen. Weitere Informationen über das Schlüsselwort finden Sie unter [String](../../../csharp/language-reference/keywords/string.md). Weitere Informationen zum Typ und dessen Methoden finden Sie unter <xref:System.String>.  
  
## <a name="declaring-and-initializing-strings"></a>Deklarieren und Initialisieren von Zeichenfolgen  
 Sie können Zeichenfolgen auf verschiedene Weise deklarieren und Initialisieren, wie im folgenden Beispiel gezeigt:  
  
 [!code-csharp[csProgGuideStrings#1](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_1.cs)]  
  
 Beachten Sie, dass Sie nicht den [neuen](../../../csharp/language-reference/keywords/new-operator.md) Operator zum Erstellen eines Zeichenfolgenobjekts verwenden, außer wenn Sie die Zeichenfolge mit einem Array von Chars initialisieren.  
  
 Initialisieren Sie eine Zeichenfolge mit dem konstanten Wert <xref:System.String.Empty>, um ein neues <xref:System.String>-Objekt zu erstellen, dessen Zeichenfolge eine Länge von 0 hat. Die Darstellung des Zeichenfolgenliterals einer Zeichenfolge mit einer Länge von 0 ist "". Indem Zeichenfolgen mit dem Wert <xref:System.String.Empty> anstatt [NULL](../../../csharp/language-reference/keywords/null.md) initialisiert werden, können Sie die Chancen einer auftretenden <xref:System.NullReferenceException> reduzieren. Verwenden Sie die statische Methode <xref:System.String.IsNullOrEmpty%28System.String%29>, um den Wert einer Zeichenfolge zu überprüfen, bevor Sie versuchen, auf sie zuzugreifen.  
  
## <a name="immutability-of-string-objects"></a>Unveränderlichkeit von Zeichenfolgenobjekten  
 Zeichenfolgenobjekte sind *unveränderlich*: sie können nicht geändert werden, nachdem sie erstellt wurden. Alle <xref:System.String>-Methoden und C#-Operatoren, die eine Zeichenfolge scheinbar verändern, geben in Wirklichkeit die Ergebnisse in einem neuen Zeichenfolgenobjekt zurück. Im folgenden Beispiel werden die beiden ursprünglichen Zeichenfolgen nicht geändert, wenn die Inhalte von `s1` und `s2` verkettet werden, um eine einzelne Zeichenfolge zu bilden. Der `+=`-Operator erstellt eine neue Zeichenfolge, die die kombinierten Inhalte enthält. Das neue Objekt wird der Variablen `s1` zugewiesen, und das ursprüngliche Objekt, das `s1` zugewiesen wurde, wird für die Garbage Collection freigegeben, da keine andere Variable einen Verweis darauf enthält.  
  
 [!code-csharp[csProgGuideStrings#2](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_2.cs)]  
  
 Da eine „Zeichenfolgenänderung“ in Wirklichkeit eine neue Erstellung von Zeichenfolgen ist, müssen Sie vorsichtig sein, wenn Sie Verweise auf Zeichenfolgen erstellen. Wenn Sie einen Verweis auf eine Zeichenfolge erstellen und dann die ursprüngliche Zeichenfolge „ändern“, wird der Verweis weiterhin auf das ursprüngliche Objekt anstelle des neuen Objekts zeigen, das erstellt wurde, als die Zeichenfolge geändert wurde. Der folgende Code veranschaulicht dieses Verhalten:  
  
 [!code-csharp[csProgGuideStrings#25](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_3.cs)]  
  
 Weitere Informationen zum Erstellen neuer Zeichenfolgen, die auf Änderungen wie Such- und Ersetzungsvorgängen in der ursprünglichen Zeichenfolge basieren, finden Sie unter [Vorgehensweise: Ändern von Zeichenfolgeninhalten](../../how-to/modify-string-contents.md).  
  
## <a name="regular-and-verbatim-string-literals"></a>Reguläre und ausführliche Zeichenfolgenliterale  
 Verwenden Sie reguläre Zeichenfolgenliterale, wenn Sie von C# bereitgestellte Escapezeichen einbetten müssen, wie im folgenden Beispiel gezeigt:  
  
 [!code-csharp[csProgGuideStrings#3](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_4.cs)]  
  
 Verwenden Sie ausführliche Zeichenfolgen der Einfachheit und Lesbarkeit halber, wenn der Text der Zeichenfolge umgekehrte Schrägstriche enthält, z.B. in Dateipfaden. Da ausführliche Zeichenfolgen neue Zeilenzeichen als Teil des Texts der Zeichenfolge beibehalten, können sie verwendet werden, um mehrzeilige Zeichenfolgen zu initialisieren. Verwenden Sie doppelte Anführungszeichen, um ein Anführungszeichen in eine ausführliche Zeichenfolge einzubetten. Im folgenden Beispiel werden einige gängige Verwendungszwecke für allgemeine Zeichenfolgen dargestellt:  
  
 [!code-csharp[csProgGuideStrings#4](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_5.cs)]  
  
## <a name="string-escape-sequences"></a>Zeichenfolgen-Escapesequenzen  
  
|Escapesequenz|Zeichenname|Unicode-Codierung|  
|---------------------|--------------------|----------------------|  
|\\'|Einfaches Anführungszeichen|0x0027|  
|\\"|Doppeltes Anführungszeichen|0x0022|  
|\\\\ |Umgekehrter Schrägstrich|0x005C|  
|\0|Null|0x0000|  
|\a|Warnung|0x0007|  
|\b|Rückschritt|0x0008|  
|\f|Seitenvorschub|0x000C|  
|\n|Zeilenwechsel|0x000A|  
|\r|Wagenrücklauf|0x000D|  
|\t|Horizontaler Tabulator|0x0009|  
|\U|Unicode-Escapesequenz für Ersatzzeichenpaare|\Unnnnnnnn|  
|\u|Unicode-Escapesequenz|\u0041 = "A"|  
|\v|Vertikaler Tabulator|0x000B|  
|\x|Unicode-Escapesequenz, die ähnlich wie "\u" ist, außer mit variabler Länge|\x0041 oder \x41 = "A"|  
  
> [!NOTE]
>  Zum Zeitpunkt der Kompilierung werden ausführliche Zeichenfolgen in normale Zeichenfolgen mit gleichen Escapesequenzen konvertiert. Aus diesem Grund sehen Sie die Escapezeichen, die vom Compiler hinzugefügt werden, und nicht die ausführliche Version aus Ihrem Sourcecode, wenn Sie eine ausführliche Zeichenfolge in Debugger-Überwachungsfenster anzeigen. Die ausführliche Zeichenfolge @"C:\files.txt" wird im Überwachungsfenster z.B. als „C:\\\files.txt“ angezeigt.  
  
## <a name="format-strings"></a>Formatzeichenfolgen  
 Eine Formatzeichenfolge ist eine Zeichenfolge, deren Inhalt zur Laufzeit dynamisch bestimmt wird. Formatzeichenfolgen werden erstellt, indem *interpolierte Ausdrücke* oder Platzhalter in geschweifte Klammern innerhalb einer Zeichenfolge eingebettet werden. Der in den Klammern (`{...}`) eingeschlossene Inhalt wird in einen Wert aufgelöst und zur Laufzeit als formatierte Zeichenfolge ausgegeben. Es gibt zwei Methoden zum Erstellen von Formatzeichenfolgen: Zeichenfolgeninterpolation und kombinierte Formatierung.

### <a name="string-interpolation"></a>Zeichenfolgeninterpolierung
In C# 6.0 und höheren Versionen werden [*interpolierte Zeichenfolgen*](../../language-reference/tokens/interpolated.md) durch das Sonderzeichen `$` identifiziert und interpolierte Ausdrücke in geschweifte Klammern eingeschlossen. Wenn Sie noch nicht mit der Zeichenfolgeninterpolation vertraut sind, erhalten Sie im interaktiven Tutorial [Zeichenfolgeninterpolation in C#](../../tutorials/intro-to-csharp/interpolated-strings.yml) eine kurze Übersicht.

Verwenden Sie die Zeichenfolgeninterpolation, um die Lesbarkeit und die Wartungsfähigkeit Ihres Codes zu verbessern. Mit der Zeichenfolgeninterpolation werden die gleichen Ergebnisse erzielt wie mit der `String.Format`-Methode, es wird jedoch die Benutzerfreundlichkeit und Übersichtlichkeit verbessert.

[!code-csharp[csProgGuideFormatStrings](~/samples/snippets/csharp/programming-guide/strings/Strings_1.cs#StringInterpolation)]

### <a name="composite-formatting"></a>Kombinierte Formatierung
<xref:System.String.Format%2A?displayProperty=nameWithType> verwendet Platzhalter in geschweiften Klammern, um eine Formatzeichenfolge zu erstellen. Dieses Beispiel liefert als Ergebnis eine ähnliche Ausgabe wie die oben verwendete Methode zur Zeichenfolgeninterpolation.
  
[!code-csharp[csProgGuideFormatStrings](~/samples/snippets/csharp/programming-guide/strings/Strings_1.cs#StringFormat)]

Weitere Informationen zum Formatieren von .NET-Typen finden Sie unter [Formatieren von Typen in .NET](../../../standard/base-types/formatting-types.md).
  
## <a name="substrings"></a>Teilzeichenfolgen  
 Eine Teilzeichenfolge ist eine beliebige Sequenz von Zeichen, die in einer Zeichenfolge enthalten ist. Verwenden Sie die <xref:System.String.Substring%2A>-Methode, um eine neue Zeichenfolge aus einem Teil der ursprünglichen Zeichenfolge zu erstellen. Sie können nach einem oder mehreren Vorkommnissen einer Teilzeichenfolge suchen, indem Sie die <xref:System.String.IndexOf%2A>-Methode verwenden. Verwenden Sie die <xref:System.String.Replace%2A>-Methode, um alle Vorkommnisse einer angegebenen Teilzeichenfolge mit einer neuen Zeichenfolge zu ersetzen. Genauso wie die <xref:System.String.Substring%2A>-Methode gibt <xref:System.String.Replace%2A> tatsächlich eine neue Zeichenfolge zurück und ändert nicht die ursprüngliche Zeichenfolge. Weitere Informationen finden Sie unter [Vorgehensweise: Suchen von Zeichenfolgen](../../how-to/search-strings.md) und [Vorgehensweise: Ändern von Zeichenfolgeninhalten](../../how-to/modify-string-contents.md).  
  
 [!code-csharp[csProgGuideStrings#7](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_7.cs)]  
  
## <a name="accessing-individual-characters"></a>Zugreifen auf einzelne Zeichen  
 Sie können die Arraynotation mit einem Indexwert verwenden, um schreibgeschützten Zugriff auf einzelne Zeichen zu erhalten, so wie in folgendem Beispiel gezeigt:  
  
 [!code-csharp[csProgGuideStrings#9](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_8.cs)]  
  
 Wenn die <xref:System.String>-Methoden nicht die Funktionen bieten, die Sie zum Bearbeiten einzelner Zeichen in einer Zeichenfolge benötigen, können Sie ein <xref:System.Text.StringBuilder>-Objekt verwenden, um die einzelnen Chars „direkt“ zu bearbeiten und anschließend eine neue Zeichenfolge zu <xref:System.Text.StringBuilder>-Methoden zu speichern. Im folgenden Beispiel wird davon ausgegangen, dass Sie die ursprüngliche Zeichenfolge auf eine bestimmte Weise ändern und die Ergebnisse für die zukünftige Verwendung speichern müssen:  
  
 [!code-csharp[csProgGuideStrings#8](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_9.cs)]  
  
## <a name="null-strings-and-empty-strings"></a>NULL-Zeichenfolgen und leere Zeichenfolgen  
 Eine leere Zeichenfolge ist eine Instanz eines <xref:System.String?displayProperty=nameWithType>-Objekts, dass 0 Zeichen enthält. Leere Zeichenfolgen werden häufig in verschiedenen Programmierszenarios verwendet, um ein leeres Textfeld darzustellen. Sie können Methoden für leere Zeichenfolgen aufrufen, da sie gültige <xref:System.String?displayProperty=nameWithType>-Objekte sind. Leere Zeichenfolgen werden wie folgt initialisiert:  
  
```  
string s = String.Empty;  
```  
  
 Im Gegensatz dazu, verweist eine NULL-Zeichenfolge nicht auf eine Instanz eines <xref:System.String?displayProperty=nameWithType>-Objekts und jeder Versuch, eine Methode für eine NULL-Zeichenfolge aufzurufen, löst eine <xref:System.NullReferenceException> aus. Allerdings können Sie NULL-Zeichenfolgen in Verkettungs- und Vergleichsoperationen mit anderen Zeichenfolgen verwenden. Die folgenden Beispiele veranschaulichen einige Fälle, in denen ein Verweis auf eine NULL-Zeichenfolge nicht dazu führt, dass eine Ausnahme ausgelöst wird:  
  
 [!code-csharp[csProgGuideStrings#27](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_10.cs)]  
  
## <a name="using-stringbuilder-for-fast-string-creation"></a>Verwenden von StringBuilder für die schnelle Erstellung von Zeichenfolgen  
 Zeichenfolgenoperationen in .NET werden hochgradig optimiert und wirken sich in den meisten Fällen nicht erheblich auf die Leistung aus. In einigen Szenarios, z.B. in engen Schleifen, die Hunderttausende Male ausgeführt werden, können sich Zeichenfolgenoperationen auf die Leistung auswirken. Die <xref:System.Text.StringBuilder>-Klasse erstellt einen Zeichenfolgenpuffer, der eine verbesserte Leistung mit sich bringt, wenn Ihr Programm viele Zeichenfolgenbearbeitungen durchführt. Mit der <xref:System.Text.StringBuilder>-Zeichenfolge können Sie auch einzelne Zeichen erneut zuweisen, was der integrierte String-Datentyp nicht unterstützt. Dieser Code ändert z.B. den Inhalt einer Zeichenfolge ohne eine neue Zeichenfolge zu erstellen:  
  
 [!code-csharp[csProgGuideStrings#20](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_11.cs)]  
  
 In diesem Beispiel wird ein <xref:System.Text.StringBuilder>-Objekt zum Erstellen einer Zeichenfolge aus einem Satz von numerischen Typen verwendet:  
  
 [!code-csharp[csProgGuideStrings#15](../../../csharp/programming-guide/strings/codesnippet/CSharp/index_12.cs)]  
  
## <a name="strings-extension-methods-and-linq"></a>Zeichenfolgen, Erweiterungsmethoden und LINQ  
 Da der <xref:System.String>-Typ <xref:System.Collections.Generic.IEnumerable%601> implementiert, können Sie die Erweiterungsmethode verwenden, die in der <xref:System.Linq.Enumerable>-Klasse auf Zeichenfolgen definiert ist. Um „visuelle Überfrachtung“ zu vermeiden, werden diese Methode für den <xref:System.String>-Typ aus IntelliSense ausgeschlossen, nichtsdestotrotz sind sie weiterhin verfügbar. Sie können auch [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]-Abfrageausdrücke in Zeichenfolgen verwenden. Weitere Informationen finden Sie unter [LINQ und Zeichenfolgen](../../../csharp/programming-guide/concepts/linq/linq-and-strings.md).  
  
## <a name="related-topics"></a>Verwandte Themen  
  
|Thema|Beschreibung|  
|-----------|-----------------|  
|[Vorgehensweise: Ändern von Zeichenfolgeninhalten](../../how-to/modify-string-contents.md)|Veranschaulicht Methoden zum Transformieren von Zeichenfolgen und Modifizieren von Zeichenfolgeninhalten.|  
|[Vorgehensweise: Vergleichen von Zeichenfolgen](../../how-to/compare-strings.md)|So führen Sie ordinale und kulturspezifische Zeichenfolgenvergleiche durch.|  
|[Vorgehensweise: Verketten von mehreren Zeichenfolgen](../../how-to/concatenate-multiple-strings.md)|Veranschaulicht verschiedene Möglichkeiten, mehrere Zeichenfolgen zu einer einzigen zu verknüpfen.|
|[Vorgehensweise: Analysieren von Zeichenfolgen mithilfe von String.Split](../../how-to/parse-strings-using-split.md)|Enthält Codebeispiele, die veranschaulichen, wie Sie die `String.Split`-Methode zum Analysieren von Zeichenfolgen verwenden.|  
|[Vorgehensweise: Durchsuchen von Zeichenfolgen](../../how-to/search-strings.md)|Erläutert, wie Sie mit der Suche Zeichenfolgen nach spezifischem Text oder spezifischen Mustern durchsuchen können.|  
|[Vorgehensweise: Bestimmen, ob eine Zeichenfolge einen numerischen Wert darstellt](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)|Zeigt, wie Sie sicher eine Zeichenfolge analysieren, um zu sehen, ob diese über einen gültigen numerischen Wert verfügt|  
|[Zeichenfolgeninterpolation](../../language-reference/tokens/interpolated.md)|Beschreibt die Funktion zur Zeichenfolgeninterpolation, die eine zweckmäßige Syntax zum Formatieren von Zeichenfolgen bietet.|
|[Grundlegende Zeichenfolgenoperationen](../../../../docs/standard/base-types/basic-string-operations.md)|Stellt Links zu Themen bereit, die <xref:System.String?displayProperty=nameWithType>- und <xref:System.Text.StringBuilder?displayProperty=nameWithType>-Methoden verwenden, um grundlegende Zeichenfolgenoperationen durchzuführen|  
|[Parsing Strings](../../../standard/base-types/parsing-strings.md)|Beschreibt das Konvertieren von Zeichenfolgendarstellungen der .NET-Basistypen in Instanzen der entsprechenden Typen.|  
|[Analysieren von Zeichenfolgen für Datum und Uhrzeit in .NET](../../../standard/base-types/parsing-datetime.md)|Zeigt, wie eine Zeichenfolge wie "01/24/2008" in ein <xref:System.DateTime?displayProperty=nameWithType>-Objekt konvertiert wird|  
|[Vergleichen von Zeichenfolgen](../../../../docs/standard/base-types/comparing.md)|Enthält Informationen, wie Zeichenfolgen verglichen werden, und gibt Beispiele in C# und Visual Basic|  
|[Verwenden der StringBuilder-Klasse](../../../standard/base-types/stringbuilder.md)|Beschreibt das Erstellen und Ändern dynamischer Zeichenfolgenobjekte mithilfe der <xref:System.Text.StringBuilder>-Klasse|  
|[LINQ und Zeichenfolgen](../../../csharp/programming-guide/concepts/linq/linq-and-strings.md)|Enthält Informationen zum Ausführen verschiedener Zeichenfolgenoperationen mithilfe von LINQ-Abfragen|  
|[C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)|Enthält Links zu Themen, in denen die Konstrukte der Programmierung in C# beschrieben werden|  
