---
title: Datentransformationen in ML.NET
description: Machen Sie sich mit den von ML.NET unterstützten Datentransformationen vertraut.
author: JRAlexander
ms.date: 10/16/2018
ms.openlocfilehash: c169319937dac13747935e451952bd75d4cc174d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143947"
---
# <a name="data-transforms-in-mlnet"></a>Datentransformationen in ML.NET

Die folgenden Tabellen enthalten Informationen zu allen Datentransformationen, die in ML.NET unterstützt werden. Durch die Auswahl eines Datentransformationstyps können Sie zur entsprechenden Tabelle navigieren:

* [Kategorische Variablen](#categorical)
* [Kombinierer und Trenner](#combiners-and-segregators)
* [Featureauswahl](#feature-selection)
* [Featurebereitsteller](#featurizers)
* [Bezeichnungsanalyse](#label-parsing)
* [Fehlende Werte](#missing-values)
* [Normalisierung](#normalization)
* [Zeilenfilter](#row-filters)
* [Schema](#schema)
* [Textverarbeitung und Featurebereitstellung](#text-processing-and-featurization)
* [Verschiedenes](#miscellaneous)

> [!NOTE]
> ML.NET ist derzeit als Vorschauversion verfügbar. Nicht alle Datentransformationen werden derzeit unterstützt. Wenn Sie eine Anforderung für eine bestimmte Transformation einreichen möchten, können Sie ein Issue im GitHub-Repository [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues) erstellen.

## <a name="categorical"></a>Kategorische Variablen

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalHashOneHotVectorizer> | Codiert die kategorische Variable mit einer hashbasierten Codierung. |
| <xref:Microsoft.ML.Legacy.Transforms.CategoricalOneHotVectorizer> | Codiert die kategorische Variable mit einer One-Hot-Codierung auf Grundlage eines Kategorienwörterbuchs. |

## <a name="combiners-and-segregators"></a>Kombinierer und Trenner

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CombinerByContiguousGroupId> | Gruppiert Werte einer Skalarspalte auf Grundlage einer ID einer zusammenhängenden Gruppe und überführt diese in einen Vektor. |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureCombiner> | Kombiniert alle Features und überführt diese in eine Featurespalte. |
| <xref:Microsoft.ML.Legacy.Transforms.ManyHeterogeneousModelCombiner> | Kombiniert eine Sequenz von TransformModel-Eigenschaften und eine PredictorModel-Eigenschaft und überführt diese in eine einzelne PredictorModel-Eigenschaft. |
| <xref:Microsoft.ML.Legacy.Transforms.ModelCombiner> | Kombiniert eine Sequenz von TransformModel-Eigenschaften und überführt diese in ein einzelnes Modell. |
| <xref:Microsoft.ML.Legacy.Transforms.Segregator> | Hebt die Gruppierung für Vektorspalten auf und überführt diese in Zeilensequenzen; Umkehrvorgang zur Gruppentransformation. |
| <xref:Microsoft.ML.Legacy.Transforms.TwoHeterogeneousModelCombiner> | Kombiniert eine TransformModel- und PredictorModel-Eigenschaft und überführt diese in eine einzelne PredictorModel-Eigenschaft. |

## <a name="feature-selection"></a>Featureauswahl

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByCount> | Wählt die Slots aus, für die die Anzahl der Nichtstandardwerte größer als oder gleich einem Schwellenwert ist. |
| <xref:Microsoft.ML.Legacy.Transforms.FeatureSelectorByMutualInformation> | Wählt die obersten k Slots aller angegebenen Spalten sortiert nach der Transinformation für die Bezeichnungsspalte aus. |

## <a name="featurizers"></a>Featurebereitsteller

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.HashConverter> | Konvertiert die Spaltenwerte in Hashwerte. Für diese Transformation werden sowohl Texteingaben als auch numerische Eingaben akzeptiert. Es kann sich sowohl um Spalten mit Einzel- als auch mit Vektorwerten handeln. |
| <xref:Microsoft.ML.Legacy.Transforms.TreeLeafFeaturizer> | Trainiert ein Strukturensemble oder lädt es aus einer Datei. Anschließend wird ein numerischer Featurevektor den folgenden drei Ausgaben zugeordnet: 1. Ein Vektor mit den einzelnen Strukturausgaben des Strukturensembles. 2. Ein Vektor, der die Blattknoten kennzeichnet, auf die der Featurevektor im Strukturensemble fällt. 3. Ein Vektor, der die Pfade kennzeichnet, auf die der Featurevektor im Strukturensemble fällt. Wenn sowohl eine Modelldatei als auch ein Trainer angegeben werden, wird für den Vektor die Modelldatei verwendet. Wenn keine Angaben bereitgestellt werden, trainiert der Vektor ein Standard-FastTree-Modell. Dieses kann Schlüsselbezeichnungen verarbeiten, indem ein Regressionsmodell hinsichtlich optional permutierter Indizes trainiert wird. |

## <a name="label-parsing"></a>Bezeichnungsanalyse

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.Dictionarizer> | Konvertiert Eingabewerte (Wörter, Zahlen usw.) für eine Wörterbuchindizierung. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelColumnKeyBooleanConverter> | Transformiert die Bezeichnung entweder in einen Schlüssel oder einen booleschen Wert (falls erforderlich), damit diese zur Klassifizierung verwendet werden kann. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelIndicator> | Von OVA verwendete Neuzuordnung von Bezeichnungen. |
| <xref:Microsoft.ML.Legacy.Transforms.LabelToFloatConverter> | Transformiert die Bezeichnung in einen Gleitkommawert, damit diese für die Regression verwendet werden kann. |
| <xref:Microsoft.ML.Legacy.Transforms.PredictedLabelColumnOriginalValueConverter> | Transformiert eine Spalte mit vorhergesagten Bezeichnungen in ihre Originalwerte. Gilt nicht für boolesche Spalten. |

## <a name="missing-values"></a>Fehlende Werte

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueHandler> | Ersetzt fehlende Werte durch den Standardwert oder durch den Mittel-, Mindest- oder Höchstwert (nur im Fall von Nicht-Text-Spalten). Eine Indikatorspalte kann optional verkettet werden, wenn der Typ der Eingabespalte numerisch ist. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueIndicator> | Erstellt eine boolesche Ausgabespalte, in der sich genauso viele Slots wie in der Eingabespalte befinden. Der Ausgabewert ist TRUE, falls der Wert in der Eingabespalte fehlt. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesDropper> | Entfernt fehlende Werte aus Vektorspalten. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValuesRowDropper> | Filtert Zeilen heraus, die fehlende Werte enthalten. |
| <xref:Microsoft.ML.Legacy.Transforms.MissingValueSubstitutor> | Erstellt eine Ausgabespalte, deren Typ und Größe mit dem bzw. der der Eingabespalte übereinstimmt. Fehlende Werte werden durch den Standardwert oder durch den Mittel-, Mindest- oder Höchstwert (nur im Fall von Nicht-Text-Spalten) ersetzt. |

## <a name="normalization"></a>Normalisierung

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.BinNormalizer> | Die Werte werden Bins (Datengruppen) der gleichen Dichte zugeordnet, und ein Wert wird „bin_number“/„number_of_bins“ zugeordnet. |
| <xref:Microsoft.ML.Legacy.Transforms.ConditionalNormalizer> | Normalisiert die Spalten bei Bedarf. |
| <xref:Microsoft.ML.Legacy.Transforms.GlobalContrastNormalizer> | Führt eine globale Kontrastnormalisierung für die Eingabewerte durch: Y = (s * X – M) / D, wobei s eine Größenordnung, M ein Mittelwert und D entweder die L2-Norm oder Standardabweichung ist. | 
| <xref:Microsoft.ML.Legacy.Transforms.LogMeanVarianceNormalizer> | Normalisiert die Daten basierend auf dem berechneten Mittelwert und der berechneten Varianz des Logarithmus der Daten. |
| <xref:Microsoft.ML.Legacy.Transforms.LpNormalizer> | Normalisiert die Vektoren (Zeilen) einzeln, indem sie auf die Einheitsnorm (L2, L1 oder LInf) skaliert werden. Führt die folgende Operation für einen Vektor X aus: Y = (X – M) / D, wobei M der Mittelwert und D die L2-, L1- oder LInf-Norm ist. |
| <xref:Microsoft.ML.Legacy.Transforms.MeanVarianceNormalizer> | Normalisiert die Daten basierend auf dem berechneten Mittelwert und der berechneten Varianz der Daten. |
| <xref:Microsoft.ML.Legacy.Transforms.MinMaxNormalizer> | Normalisiert die Daten basierend auf den beobachteten minimalen und maximalen Werten der Daten. |

## <a name="row-filters"></a>Zeilenfilter

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.RowRangeFilter> | Filtert eine Datensicht nach einer Spalte des Typs „Single“, „Double“ oder nach ihrem Schlüssel (zusammenhängende Gruppe). Behält die Werte bei, die im Bereich zwischen angegebenem Minimum und Maximum liegen. Fehlende Werte werden stets herausgefiltert. Wenn die Eingabe ein Schlüssel ist, werden die minimalen/maximalen Werte als Prozentsätze der Anzahl der Werte betrachtet. |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipAndTakeFilter> | Ermöglicht das Einschränken der Eingabe auf eine Teilmenge von Zeilen unter Berücksichtigung eines optionalen Offsets. Kann zur Implementierung eines Seitensteuerungsverfahrens für Daten verwendet werden. |
| <xref:Microsoft.ML.Legacy.Transforms.RowSkipFilter> | Ermöglicht das Einschränken der Eingabe auf eine Teilmenge von Zeilen, indem eine bestimmte Anzahl von Zeilen übersprungen wird. |
| <xref:Microsoft.ML.Legacy.Transforms.RowTakeFilter> | Ermöglicht das Einschränken der Eingabe auf eine Teilmenge von Zeilen, indem die ersten N Zeilen berücksichtigt werden. |

## <a name="schema"></a>Schema

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator> | Verkettet zwei Spalten desselben Elementtyps. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnCopier> | Dupliziert die Spalten aus dem Dataset.|
| <xref:Microsoft.ML.Legacy.Transforms.ColumnDropper> | Löscht Spalten aus dem Dataset. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnSelector> | Wählt eine Menge von Spalten aus und löscht alle anderen Spalten. |
| <xref:Microsoft.ML.Legacy.Transforms.ColumnTypeConverter> | Konvertiert eine Spalte mithilfe von Standardkonvertierungen in einen anderen Typ. |
| <xref:Microsoft.ML.Legacy.Transforms.KeyToTextConverter> | KeyToValueTransform nutzt KeyValues-Metadaten, um die Schlüsselindizes den entsprechenden Werten in den KeyValues-Metadaten zuzuordnen. |
| <xref:Microsoft.ML.Legacy.Transforms.NGramTranslator> | Erstellt eine Sammlung mit der Anzahl der N-Gramme (Sequenzen aufeinander folgender Werte der Länge 1–n) in einem angegebenen Schlüsselvektor. Dabei wird ein Wörterbuch mit N-Grammen erstellt, und die ID im Wörterbuch wird als Index in der Sammlung verwendet. | 
| <xref:Microsoft.ML.Legacy.Transforms.OptionalColumnCreator> | Wenn die Quellspalte nach der Deserialisierung nicht existiert, wird eine Spalte mit dem richtigen Typ und den Standardwerten erstellt. |

## <a name="text-processing-and-featurization"></a>Textverarbeitung und Featurebereitstellung

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.CharacterTokenizer> | Zeichenorientierter Tokenizer, der Text als Zeichensequenz verarbeitet. |
| <xref:Microsoft.ML.Legacy.Transforms.TextFeaturizer> | Eine Transformation, durch die eine Sammlung von Textdokumenten in numerische Featurevektoren umgewandelt wird. Bei den Featurevektoren handelt es sich um die normalisierten Anzahlen von N-Grammen (basierend auf Wörtern bzw. Zeichen) in einem bestimmten Tokentext. |
| <xref:Microsoft.ML.Legacy.Transforms.TextToKeyConverter> | Konvertiert Eingabewerte (Wörter, Zahlen usw.) für eine Wörterbuchindizierung. |
| <xref:Microsoft.ML.Legacy.Transforms.WordEmbeddings> | Eine Transformation, durch die Vektoren mit Texttoken mithilfe eines vortrainierten Modells in numerischen Vektoren konvertiert werden. Weitere Informationen zu diesem Verfahren finden Sie auf der Wikipedia-Seite [Word embedding (Distributionelle Semantik)](https://en.wikipedia.org/wiki/Word_embedding). |
| <xref:Microsoft.ML.Legacy.Transforms.WordTokenizer> | Die Eingabe für diese Transformation ist ein Text, und die Ausgabe ist ein Textvektor mit Wörtern (Token) des ursprünglichen Texts. Als Trennzeichen wird das Leerzeichen verwendet. Andere Zeichen (auch mehrere) können jedoch ebenfalls festgelegt werden. |

## <a name="miscellaneous"></a>Verschiedenes

| Transformation | Definition |
| --- | --- |
| <xref:Microsoft.ML.Legacy.Transforms.ApproximateBootstrapSampler> | Bootstrap-Stichprobenentnahme für approximierte Verteilung. |
| <xref:Microsoft.ML.Legacy.Transforms.BinaryPredictionScoreColumnsRenamer> | Benennt im Fall einer binären Vorhersage die Spalten „PredictedLabel“ und „Score“ um, sodass der Name der positiven Klasse eingeschlossen wird.|
| <xref:Microsoft.ML.Legacy.Transforms.DataCache> | Führt mithilfe der angegebenen Cacheoption eine Zwischenspeicherung durch. |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetScorer> | Bewertet ein Dataset mit einem Vorhersagemodell. |
| <xref:Microsoft.ML.Legacy.Transforms.DatasetTransformScorer> | Bewertet ein Dataset mit einem Transformationsmodell. |
| <xref:Microsoft.ML.Legacy.Transforms.NoOperation> | Ohne Wirkung. |
| <xref:Microsoft.ML.Legacy.Transforms.RandomNumberGenerator> | Fügt eine Spalte mit einer generierten Zahlensequenz hinzu. |
| <xref:Microsoft.ML.Legacy.Transforms.ScoreColumnSelector> | Wählt nur die Spalten mit den letzten Bewertungen und den zusätzlichen Spalten aus, die mit den Argumenten angegeben werden. |
| <xref:Microsoft.ML.Legacy.Transforms.Scorer> | Wandelt das Vorhersagemodell in ein Transformationsmodell um. |
| <xref:Microsoft.ML.Legacy.Transforms.SentimentAnalyzer> | Verwendet ein vortrainiertes Stimmungsmodell, um Eingabezeichenfolgen zu bewerten. |
| <xref:Microsoft.ML.Legacy.Transforms.TrainTestDatasetSplitter> | Teilt das Dataset in Trainings- und Testdatasets auf. |
