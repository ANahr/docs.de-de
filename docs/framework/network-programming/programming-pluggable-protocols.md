---
title: Programmieren austauschbarer Protokolle
ms.date: 03/30/2017
helpviewer_keywords:
- downloading Internet resources, pluggable protocols
- WebRequest class, pluggable protocols
- response to Internet request, pluggable protocols
- WebResponse class, pluggable protocols
- sending data, pluggable protocols
- network resources, pluggable protocols
- Internet, pluggable protocols
- programming pluggable protocols
- pluggable protocols, programming
- requesting data from Internet, pluggable protocols
- receiving data, pluggable protocols
- protocols, pluggable
ms.assetid: 66ef8456-7576-4e97-8956-959b216373db
ms.openlocfilehash: 74dd44e704836b209366a7975d08a43375318e90
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2018
ms.locfileid: "50190787"
---
# <a name="programming-pluggable-protocols"></a>Programmieren austauschbarer Protokolle
Die abstrakten Klassen <xref:System.Net.WebRequest> und <xref:System.Net.WebResponse> stellen die Grundlage für austauschbare Protokolle bereit. Durch Ableiten protokollspezifischer Klassen von <xref:System.Net.WebRequest> und <xref:System.Net.WebResponse> kann eine Anwendung Daten von einer Internetressource anfordern und die Antwort ohne Angabe des verwendeten Protokolls lesen.  
  
 Vor dem Erstellen einer protokollspezifischen <xref:System.Net.WebRequest> müssen Sie die Create-Methode registrieren. Verwenden Sie die statische <xref:System.Net.WebRequest.RegisterPrefix%28System.String%2CSystem.Net.IWebRequestCreate%29>-Methode von <xref:System.Net.WebRequest> zur Registrierung eines Nachfolgers von <xref:System.Net.WebRequest>, um eine Reihe von Anforderungen zu behandeln, die an ein bestimmtes Internetschema, an ein Schema und einen Server oder an ein Schema, einen Server und einen Pfad gerichtet sind.  
  
 In den meisten Fällen werden Sie mit den Methoden und Eigenschaften der <xref:System.Net.WebRequest>-Klasse Daten senden und empfangen können. Sollten Sie jedoch auf protokollspezifische Eigenschaften zugreifen müssen, können Sie eine Typumwandlung für <xref:System.Net.WebRequest> in eine bestimmte Instanz mit abgeleiteten Klassen durchführen.  
  
 Damit Sie von austauschbaren Protokollen profitieren können, müssen die <xref:System.Net.WebRequest>-Nachfolger eine Standardtransaktion für Anforderung und Antwort bereitstellen, für die keine protokollspezifischen Eigenschaften festgelegt werden müssen. So stellt beispielsweise die <xref:System.Net.HttpWebRequest>-Klasse, die für HTTP die <xref:System.Net.WebRequest>-Klasse implementiert, standardmäßig eine `GET`-Anforderung bereit und gibt eine <xref:System.Net.HttpWebResponse> zurück, die den vom Webserver zurückgegebenen Datenstrom enthält.  
  
## <a name="see-also"></a>Siehe auch  
 [Deriving from WebRequest (Ableiten von WebRequest)](../../../docs/framework/network-programming/deriving-from-webrequest.md)  
 [Ableiten von WebResponse](../../../docs/framework/network-programming/deriving-from-webresponse.md)  
 [Netzwerkprogrammierung in .NET Framework](../../../docs/framework/network-programming/index.md)  
 [Vorgehensweise: Typumwandlung für ein WebRequest in zugriffsprotokollspezifische Eigenschaften](../../../docs/framework/network-programming/how-to-typecast-a-webrequest-to-access-protocol-specific-properties.md)
