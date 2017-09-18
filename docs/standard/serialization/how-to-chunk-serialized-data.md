---
title: 'Vorgehensweise: Segmentieren serialisierter Daten'
ms.date: 03/30/2017
ms.prod: .net
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- chunking serialized data
- data chunking
- binary serialization, chunking data
- large data set chunking
- serialization, chunking data
- serialization, examples
- binary serialization, examples
ms.assetid: 22f1b818-7e0d-428a-8680-f17d6ebdd185
caps.latest.revision: 3
author: Erikre
ms.author: erikre
manager: erikre
ms.translationtype: HT
ms.sourcegitcommit: 717bcb6f9f72a728d77e2847096ea558a9c50902
ms.openlocfilehash: 5d8c56be905d6dbfa966546c109a322e013baaac
ms.contentlocale: de-de
ms.lasthandoff: 08/21/2017

---
# <a name="how-to-chunk-serialized-data"></a>Vorgehensweise: Segmentieren serialisierter Daten

[!INCLUDE [binary-serialization-warning](../../../includes/binary-serialization-warning.md)]

Beim Senden großer Datasätze in Webdienstnachrichten treten die zwei Probleme auf:  
  
1.  Ein großes Workingset (Arbeitsspeicher) aufgrund der Pufferung durch das Serialisierungsmodul  
  
2.  Unregelmäßige Bandbreitennutzung aufgrund von 33&#160;% Inflation nach der Base64-Codierung  
  
 Zur Lösung dieser Probleme implementieren Sie die <xref:System.Xml.Serialization.IXmlSerializable>-Schnittstelle, um die Serialisierung und Deserialisierung zu steuern. Implementieren Sie insbesondere die <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>-Methode und die <xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A>-Methode, um die Daten zu segmentieren.  
  
### <a name="to-implement-server-side-chunking"></a>So implementieren Sie serverseitige Segmentierung:  
  
1.  Die Webmethode muss die ASP.NET-Pufferung auf dem Servercomputer deaktivieren und einen Typ zurückgeben, der <xref:System.Xml.Serialization.IXmlSerializable> implementiert.  
  
2.  Der Typ, der <xref:System.Xml.Serialization.IXmlSerializable> implementiert, segmentiert die Daten in der <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>-Methode.  
  
### <a name="to-implement-client-side-processing"></a>So implementieren Sie clientseitige Verarbeitung  
  
1.  Ändern Sie die Webmethode auf dem Clientproxy so, dass der Typ zurückgegeben wird, der <xref:System.Xml.Serialization.IXmlSerializable> implementiert. Sie können <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension> verwenden, um diesen Vorgang automatisch auszuführen, aber dies wird hier nicht beschrieben.  
  
2.  Implementieren Sie die <xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A>-Methode, um den segmentierten Datenstream zu lesen und die Bytes auf den Datenträger zu schreiben. Diese Implementierung löst auch Statusereignisse aus, die von einem grafischen Steuerelement, z.&#160;B. einer Statusleiste, verwendet werden können.  
  
## <a name="example"></a>Beispiel  
Das folgende Codebeispiel veranschaulicht die Webmethode auf dem Client, mit der die ASP.NET-Pufferung deaktiviert wird. Es zeigt zudem die clientseitige Implementierung der <xref:System.Xml.Serialization.IXmlSerializable>-Schnittstelle, die die Daten in der <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>-Methode segmentiert.  
  
[!code-csharp[HowToChunkSerializedData#1](../../../samples/snippets/csharp/VS_Snippets_Remoting/HowToChunkSerializedData/CS/SerializationChunk.cs#1)] [!code-vb[HowToChunkSerializedData#1](../../../samples/snippets/visualbasic/VS_Snippets_Remoting/HowToChunkSerializedData/VB/SerializationChunk.vb#1)]  
[!code-csharp[HowToChunkSerializedData#2](../../../samples/snippets/csharp/VS_Snippets_Remoting/HowToChunkSerializedData/CS/SerializationChunk.cs#2)] [!code-vb[HowToChunkSerializedData#2](../../../samples/snippets/visualbasic/VS_Snippets_Remoting/HowToChunkSerializedData/VB/SerializationChunk.vb#2)]  
[!code-csharp[HowToChunkSerializedData#3](../../../samples/snippets/csharp/VS_Snippets_Remoting/HowToChunkSerializedData/CS/SerializationChunk.cs#3)] [!code-vb[HowToChunkSerializedData#3](../../../samples/snippets/visualbasic/VS_Snippets_Remoting/HowToChunkSerializedData/VB/SerializationChunk.vb#3)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
-   In diesem Code werden die folgenden Namespaces verwendet: <xref:System>, <xref:System.Runtime.Serialization>, <xref:System.Web.Services>, <xref:System.Web.Services.Protocols>, <xref:System.Xml>, <xref:System.Xml.Serialization> und <xref:System.Xml.Schema>.  
  
## <a name="see-also"></a>Siehe auch  
 [Benutzerdefinierte Serialisierung](custom-serialization.md)
