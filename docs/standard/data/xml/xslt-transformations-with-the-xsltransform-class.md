---
title: XSLT-Transformationen mit der XslTransform-Klasse
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: 500335af-f9b5-413b-968a-e6d9a824478c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 67062ab87182bcb42793cb166323020178ac1688
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/18/2018
ms.locfileid: "45746418"
---
# <a name="xslt-transformations-with-the-xsltransform-class"></a>XSLT-Transformationen mit der XslTransform-Klasse

> [!NOTE]
> Die <xref:System.Xml.Xsl.XslTransform>-Klasse ist in [!INCLUDE[dnprdnext](../../../../includes/dnprdnext-md.md)] veraltet. Mithilfe der <xref:System.Xml.Xsl.XslCompiledTransform>-Klasse können Sie XSLT-Transformationen (Extensible Stylesheet Language for Transformations) vornehmen. Weitere Informationen finden Sie unter [Verwenden der XslCompiledTransform-Klasse](using-the-xslcompiledtransform-class.md) und [Migrieren von der XslTransform-Klasse](migrating-from-the-xsltransform-class.md).

Zweck der XSLT ist es, den Inhalt eines XML-Quelldokuments in ein anderes Dokument zu transformieren, das ein anderes Format oder eine andere Struktur aufweist (beispielsweise kann XML für die Verwendung in einer Website in HTML transformiert werden, oder aber in ein Dokument, das nur die Felder enthält, die von einer Anwendung benötigt werden). Dieser Transformationsprozess wird in der W3C-Empfehlung (W3C = World Wide Web Consortium) zur [XSLT-Version 1.0](https://www.w3.org/TR/1999/REC-xslt-19991116) angegeben. In [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] ist die <xref:System.Xml.Xsl.XslTransform>-Klasse im <xref:System.Xml.Xsl>-Namespace der XSLT-Prozessor, der die Funktionen dieser Spezifikation implementiert. Einige wenige Funktionen aus der Empfehlung des W3C zu XSLT, Version 1.0, die nicht implementiert wurden, sind in [Ausgaben aus XslTransform](outputs-from-an-xsltransform.md) aufgelistet. In der folgenden Abbildung wird die Transformationsarchitektur von [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] dargestellt.

## <a name="overview"></a>Übersicht

![XSLT-Transformationsarchitektur](media/xslttransformationswithxsltransformclass.gif "XsltTransformationsWithXslTransformClass")  
Transformationsarchitektur

Die XSLT-Empfehlung verwendet XPath (XML Path Language) zum Auswählen von Teilen eines XML-Dokuments, wobei XPath eine Abfragesprache ist, die zum Navigieren in Knoten einer Dokumentstruktur verwendet wird. Wie in der Abbildung gezeigt, wird die [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]-Implementierung von XPath zum Auswählen von XML-Teilen verwendet, die in mehreren Klassen gespeichert sind, z. B. ein <xref:System.Xml.XmlDocument>, ein <xref:System.Xml.XmlDataDocument> oder ein <xref:System.Xml.XPath.XPathDocument>. Ein <xref:System.Xml.XPath.XPathDocument> ist ein optimierter XSLT-Datenspeicher, der bei Verwendung zusammen mit <xref:System.Xml.Xsl.XslTransform> leistungsfähige XSLT-Transformationen ermöglicht.

In der folgenden Tabelle werden Klassen aufgelistet, die beim Arbeiten mit <xref:System.Xml.Xsl.XslTransform> und XPath und deren Funktionen verwendet werden.

|Klasse oder Schnittstelle|Funktion|
|------------------------|--------------|
|<xref:System.Xml.XPath.XPathNavigator>|Eine API, die ein Cursormodell für die Navigation in einem Speicher bereitstellt und XPath-Abfragen unterstützt. Sie ermöglicht keine Bearbeitung des zugrunde liegenden Speichers. Verwenden Sie zum Bearbeiten die <xref:System.Xml.XmlDocument>-Klasse.|
|<xref:System.Xml.XPath.IXPathNavigable>|Eine Schnittstelle, die einem `CreateNavigator` für den Speicher eine <xref:System.Xml.XPath.XPathNavigator>-Methode bereitstellt.|
|<xref:System.Xml.XmlDocument>|Ermöglicht die Bearbeitung dieses Dokuments. Implementiert <xref:System.Xml.XPath.IXPathNavigable> und ermöglicht so Dokumentbearbeitungen, bei denen nachfolgend XSLT-Transformationen benötigt werden. Weitere Informationen finden Sie unter [XmlDocument-Eingaben in XslTransform](xmldocument-input-to-xsltransform.md).|
|<xref:System.Xml.XmlDataDocument>|Wird aus dem <xref:System.Xml.XmlDocument> abgeleitet. Stellt eine Brücke zwischen XML und den relationalen Daten her. Dazu wird ein <xref:System.Data.DataSet> verwendet, um die Speicherung von strukturierten Daten innerhalb des XML-Dokuments gemäß festgelegten Zuordnungen für das <xref:System.Data.DataSet> zu optimieren. Implementiert <xref:System.Xml.XPath.IXPathNavigable>, sodass XSLT-Transformationen über relationale Daten ausgeführt werden können, die aus einer Datenbank abgerufen wurden. Weitere Informationen finden Sie unter [XML-Integration mit relationalen Daten und ADO.NET](xml-integration-with-relational-data-and-adonet.md).|
|<xref:System.Xml.XPath.XPathDocument>|Diese Klasse ist für die <xref:System.Xml.Xsl.XslTransform>-Verarbeitung und für XPath-Abfragen optimiert. Sie stellt einen sehr leistungsfähigen schreibgeschützten Zwischenspeicher bereit. Implementiert <xref:System.Xml.XPath.IXPathNavigable> und ist der bevorzugte Speicher für XSLT-Transformationen.|
|<xref:System.Xml.XPath.XPathNodeIterator>|Ermöglicht Navigation über XPath-Knotengruppen. Alle XPath-Auswahlmethoden für den <xref:System.Xml.XPath.XPathNavigator> geben einen <xref:System.Xml.XPath.XPathNodeIterator> zurück. Mehrere <xref:System.Xml.XPath.XPathNodeIterator>-Objekte können für den gleichen Speicher erstellt werden, wobei jedes eine ausgewählte Knotengruppe darstellt.|

## <a name="msxml-xslt-extensions"></a>MSXML-XSLT-Erweiterungen

Die Funktionen `msxsl:script` und `msxsl:node-set` sind die einzigen XSLT-Erweiterungen von MSXML (Microsoft XML Core Services), die von der <xref:System.Xml.Xsl.XslTransform>-Klasse unterstützt werden.

## <a name="example"></a>Beispiel

Das folgende Codebeispiel lädt ein XSLT-Stylesheet, liest eine Datei mit dem Namen mydata.xml in ein <xref:System.Xml.XPath.XPathDocument> ein und transformiert die Daten für eine fiktive Datei mit dem Namen myStyleSheet.xsl, wobei die formatierte Ausgabe an die Konsole gesendet wird.

```vb
Imports System
Imports System.IO
Imports System.Xml
Imports System.Xml.XPath
Imports System.Xml.Xsl

Public Class Sample
    Private filename As [String] = "mydata.xml"
    Private stylesheet As [String] = "myStyleSheet.xsl"

    Public Shared Sub Main()
        Dim xslt As New XslTransform()
        xslt.Load(stylesheet)
        Dim xpathdocument As New XPathDocument(filename)
        Dim writer As New XmlTextWriter(Console.Out)
        writer.Formatting = Formatting.Indented

        xslt.Transform(xpathdocument, Nothing, writer, Nothing)
    End Sub 'Main
End Class 'Sample
```

```csharp
using System;
using System.IO;
using System.Xml;
using System.Xml.XPath;
using System.Xml.Xsl;

public class Sample 
{
    private const String filename = "mydata.xml";
    private const String stylesheet = "myStyleSheet.xsl";

    public static void Main()
    {
        XslTransform xslt = new XslTransform();
        xslt.Load(stylesheet);
        XPathDocument xpathdocument = new XPathDocument(filename);
        XmlTextWriter writer = new XmlTextWriter(Console.Out);
        writer.Formatting = Formatting.Indented;

        xslt.Transform(xpathdocument, null, writer, null);
    }
}
```

## <a name="see-also"></a>Siehe auch

- <xref:System.Xml.Xsl.XslTransform>  
- [Implementierung des XSLT-Prozessors durch die XslTransform-Klasse](xsltransform-class-implements-the-xslt-processor.md)  
- [Implementierung von freigegebenen Verhaltensweisen in der XslTransform-Klasse](implementation-of-discretionary-behaviors-in-the-xsltransform-class.md)  
- [„XPathNavigator“ in Transformationen](xpathnavigator-in-transformations.md)  
- [„XPathNodeIterator“ in Transformationen](xpathnodeiterator-in-transformations.md)  
- [XPathDocument-Eingaben in XslTransform](xpathdocument-input-to-xsltransform.md)  
- [XmlDataDocument-Eingaben in „XslTransform“](xmldatadocument-input-to-xsltransform.md)  
- [XmlDocument-Eingaben in „XslTransform“](xmldocument-input-to-xsltransform.md)  
