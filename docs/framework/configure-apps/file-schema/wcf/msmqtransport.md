---
title: '&lt;msmqTransport&gt;'
ms.date: 03/30/2017
ms.assetid: 19d89f35-76ac-49dc-832b-e8bec2d5e33b
ms.openlocfilehash: a771e4e74078feed5bb9f6c76d991ccee4c4ea29
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143492"
---
# <a name="ltmsmqtransportgt"></a>&lt;msmqTransport&gt;
Führt dazu, dass ein Kanal Nachrichten in der MSMQ-Sitzung überträgt, wenn er in einer benutzerdefinierten Bindung enthalten ist.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<MsmqIntegration >  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<msmqTransport>  
    customDeadLetterQueue="Uri"  
    deadLetterQueue="Custom/None/System"  
    durable="Boolean"  
    exactlyOnce="Boolean"  
    manualAddressing="Boolean"  
    maxBufferPoolSize="Integer"  
    maxImmediateRetries="Integer"  
    maxPoolSize="Integer"  
    maxReceivedMessageSize="Integer"  
    maxRetryCycles="Integer"  
....queueTransferProtocol="Native/Srmp/SrmpSecure"  
    rejectAfterLastRetry="Boolean"  
    retryCycleDelay="TimeSpan"  
    timeToLive="TimeSpan"  
    useActiveDirectory="Boolean"  
    useSourceJournal="Boolean"  
    useMsmqTracing="Boolean"  
    <msmqTransportSecurity>  
    </msmqTransportSecurity>  
</msmqIntegration>  
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|customDeadLetterQueue|Ein URI, der den Speicherort der Warteschlange für unzustellbare Nachrichten für jede Anwendung enthält, in der abgelaufene oder nicht an die Anwendung übertragene Nachrichten platziert werden.<br /><br /> Bei Nachrichten, die ExactlyOnce-Zusicherungen erfordern (das heißt, das `exactlyOnce`-Attribut ist auf `true` festgelegt), ist dieses Attribut standardmäßig die systemweite Transaktionswarteschlange für unzustellbare Nachrichten in MSMQ.<br /><br /> Für Nachrichten, die keine Zusicherungen erfordern (das heißt, `exactlyOnce` ist auf `false` festgelegt), ist dieses Attribut standardmäßig `null`.<br /><br /> Der Wert muss das net.msmq-Schema verwenden. Die Standardeinstellung ist `null`.<br /><br /> Wenn `deadLetterQueue` auf `None` oder `System` festgelegt ist, muss dieses Attribut auf `null` festgelegt sein. Wenn dieses Attribut nicht auf `null` festgelegt ist, muss `deadLetterQueue` auf `Custom` festgelegt sein.|  
|deadLetterQueue|Gibt den zu verwendenden Typ der Warteschlange für unzustellbare Nachrichten an.<br /><br /> Gültige Werte sind<br /><br /> -Benutzerdefiniert: Benutzerdefinierte Warteschlange für unzustellbare Nachrichten-Warteschlange.<br />– None: Es wurde keine Warteschlange für unzustellbare Nachrichten ist, verwendet werden soll.<br />-System: Verwenden Sie die Systemwarteschlange für unzustellbare Nachrichten.<br /><br /> Dieses Attribut ist vom Typ DeadLetterQueue.|  
|durable|Ein boolescher Wert, der angibt, ob die von dieser Bindung verarbeiteten Nachrichten permanent oder flüchtig sind. Die Standardeinstellung ist `true`.<br /><br /> Eine permanente Meldung überlebt einen Warteschlangen-Managerabsturz, was für eine flüchtige Meldung nicht gilt. Flüchtige Nachrichten sind nützlich, wenn Anwendungen eine geringere Latenz erfordern und eine geringe Anzahl verlorener Nachrichten tolerieren können.<br /><br /> Wenn `exactlyOnce` auf `true` festgelegt ist, müssen die Nachrichten permanent sein.|  
|exactlyOnce|Ein boolescher Wert, der angibt, ob die von dieser Bindung verarbeiteten Nachrichten genau einmal empfangen werden. Die Standardeinstellung ist `true`.<br /><br /> Eine Meldung kann mit oder ohne Zusicherungen gesendet werden. Eine Zusicherung ermöglicht einer Anwendung, sicherzustellen, dass eine gesendete Nachricht die empfangende Nachrichtenwarteschlange erreicht hat. Andernfalls kann die Anwendung dies durch Lesen der Warteschlange für unzustellbare Nachrichten bestimmen.<br /><br /> `exactlyOnce`, wenn auf `true` festgelegt, gibt an, dass MSMQ sicherstellt, dass eine gesendete Nachricht genau einmal an die empfangende Nachrichtenwarteschlange gesendet wird. Wenn die Zustellung fehlschlägt, wird die Nachricht an die Warteschlange für unzustellbare Nachrichten gesendet.<br /><br /> Mit `exactlyOnce` gesendete Nachrichten, die auf `true` festgelegt sind, dürfen nur an eine Transaktionswarteschlange gesendet werden.|  
|manualAddressing|Ein boolescher Wert , der es dem Benutzer ermöglicht, die Kontrolle über die Nachrichtenadressierung zu übernehmen. Diese Eigenschaft wird i.&#160;d.&#160;R. in Routerumgebungen verwendet, wenn das Ziel der Nachricht von der Anwendung bestimmt wird.<br /><br /> Wenn diese Eigenschaft auf `true` festgelegt ist, wird vom Kanal angenommen, dass die Nachricht bereits adressiert wurde, und es werden ihr keine weiteren Informationen hinzugefügt. Der Benutzer kann dann jede Nachricht einzeln adressieren.<br /><br /> Wenn als Wert `false` festgelegt wurde, erstellt der Standard-Windows Communication Foundation (WCF)-Adressiermechanismus automatisch Adressen für alle Nachrichten.<br /><br /> Die Standardeinstellung ist `false`.|  
|maxBufferPoolSize|Eine positive ganze Zahl, die die maximale Pufferpoolgröße angibt. Der Standard ist 524288.<br /><br /> Viele Bereiche von WCF verwenden Puffer. Das Erstellen und Zerstören von Puffern bei jeder Verwendung ist kostspielig. Dasselbe gilt für die Garbage Collection für Puffer. Bei Pufferpools können Sie einen zu verwendenden Puffer aus dem Pool nehmen und ihn nach der Verwendung wieder dem Pool zuführen. So wird der Aufwand beim Erstellen und Zerstören von Puffern vermieden.|  
|maxImmediateRetries|Versucht, eine ganze Zahl, die angibt, die maximale Anzahl von unmittelbaren Wiederholungsversuchen für eine Nachricht, die aus der Anwendungswarteschlange gelesen wird. Der Standard ist 5.<br /><br /> Wenn die maximale Anzahl der sofortigen Zustellungsversuche erreicht ist und die Nachricht nicht von der Anwendung empfangen wurde, wird die Nachricht an eine Wiederholungswarteschlange gesendet, um sie später erneut zuzustellen. Wenn keine Wiederholungszyklen angegeben sind, wird die Nachricht entweder an die Warteschlange für potenziell schädliche Nachrichten gesendet, oder es wird eine negative Bestätigung zurück zum Absender geschickt.|  
|maxPoolSize|Eine positive ganze Zahl, die die maximale Puffergröße angibt. Der Standard ist 524288.|  
|maxReceivedMessageSize|Eine positive ganze Zahl, die die maximale Nachrichtengröße in Byte, einschließlich Header, angibt. Der Absender einer Nachricht erhält einen SOAP-Fehler, wenn die Nachricht zu groß für den Empfänger ist. Der Empfänger verwirft die Nachricht und erstellt einen Eintrag des Ereignisses im Ablaufverfolgungsprotokoll. Der Standard ist 65536.|  
|MaxRetryCycles|Eine ganze Zahl, welche die maximale Anzahl von Wiederholungszyklen angibt, mit denen versucht wird, Nachrichten an die empfangende Anwendung zu senden. Die Standardeinstellung ist <xref:System.Int32.MaxValue>.<br /><br /> Ein einzelner Wiederholungszyklus versucht, einer Anwendung eine Nachricht mit einer festgelegten Häufigkeit zuzustellen. Die Anzahl von unternommenen Versuchen wird durch das `maxImmediateRetries`-Attribut festgelegt. Wenn die Anwendung die Nachricht nicht empfangen kann, nachdem die Zustellungsversuche beendet sind, wird die Nachricht an eine Wiederholungswarteschlange gesendet. Nachfolgende Wiederholungszyklen bestehen aus der Nachricht, die von der Wiederholungswarteschlange an die Anwendungswarteschlange zurückgegeben wurde, um erneut zu versuchen, der Anwendung die Nachricht nach einer durch das `retryCycleDelay`-Attribut angegebenen Verzögerung zuzustellen. Das `maxRetryCycles`-Attribut gibt die Anzahl der Wiederholungszyklen an, welche die Anwendung für die Zustellung der Nachricht verwendet.|  
|queueTransferProtocol|Gibt den von dieser Bindung verwendeten Kommunikationskanaltransport in der Warteschlange an. Folgende Werte sind gültig:<br /><br /> -Native:  Verwenden Sie das systemeigene MSMQ-Protokoll.<br />-Srmp:  Verwenden Sie das Soap Reliable Messaging Protocol (SRMP).<br />-SrmpSecure: Verwenden Sie den Soap Reliable Messaging Protocol Secure (SRMPS)-Transport.<br /><br /> Dieses Attribut ist vom Typ <xref:System.ServiceModel.QueueTransferProtocol>.<br /><br /> Da MSMQ die Active Directory-Adressierung wird bei Verwendung des SOAP Reliable Messaging Protocol nicht unterstützt wird, sollten Sie dieses Attribut nicht auf Srmp oder Srmps festlegen beim `useActiveDirectory` nastaven NA hodnotu `true`.|  
|rejectAfterLastRetry|Ein boolescher Wert, der angibt, welche Aktion für eine Nachricht erfolgen soll, deren Zustellung auch nach der maximalen Anzahl von Wiederholungen fehlgeschlagen ist.<br /><br /> `true` bedeutet, dass eine negative Bestätigung zurück zum Absender geschickt wird und die Nachricht verworfen wird; `false` bedeutet, dass die Nachricht an die Warteschlange für potenziell schädliche Nachrichten gesendet wird. Die Standardeinstellung ist `false`.<br /><br /> Falls der Wert `false` lautet, kann die empfangende Anwendung die Warteschlange für potenziell schädliche Nachrichten lesen, um solche Nachrichten zu verarbeiten (das heißt, Nachrichten, die nicht zugestellt werden konnten).<br /><br /> MSMQ 3.0 unterstützt das Zurücksenden einer negativen Bestätigung an den Absender nicht. Dieses Attribut wird also in MSMQ 3.0 ignoriert.|  
|retryCycleDelay|Ein <xref:System.TimeSpan>, der die Zeitverzögerung zwischen den Wiederholungszyklen angibt, wenn versucht wird, eine Nachricht zuzustellen, die nicht sofort zugestellt werden konnte. Der Standardwert ist 00:10:00.<br /><br /> Ein einzelner Wiederholungszyklus versucht, einer empfangenden Anwendung eine Nachricht mit einer festgelegten Häufigkeit zuzustellen. Die Anzahl von unternommenen Versuchen wird durch das `maxImmediateRetries`-Attribut angegeben. Wenn die Anwendung die Nachricht nach der angegebenen Anzahl von Wiederholungsversuchen nicht empfangen kann, wird die Nachricht an eine Wiederholungswarteschlange gesendet. Nachfolgende Wiederholungszyklen bestehen aus der Nachricht, die von der Wiederholungswarteschlange an die Anwendungswarteschlange zurückgegeben wurde, um erneut zu versuchen, der Anwendung die Nachricht nach einer durch das `retryCycleDelay`-Attribut angegebenen Verzögerung zuzustellen. Die Anzahl von Wiederholungszyklen wird durch das `maxRetryCycles`-Attribut angegeben.|  
|timeToLive|Ein <xref:System.TimeSpan>-Wert, der angibt, wie lange die Nachricht gültig ist, bis sie abläuft und in die Warteschlange für unzustellbare Nachrichten übertragen wird. Der Standard ist 1.00:00:00, was 1 Tag bedeutet.<br /><br /> Dieses Attribut wird festgelegt, um sicherzustellen, dass zeitkritische Nachrichten nicht veralten, bevor sie von den empfangenden Anwendungen verarbeitet werden. Eine Nachricht in einer Warteschlange, die nicht von der empfangenden Anmeldung innerhalb des angegebenen Zeitintervalls verarbeitet wird, läuft ab. Abgelaufene Nachrichten werden an eine besondere Warteschlange gesendet: die Warteschlange für unzustellbare Nachrichten. Der Speicherort der Warteschlange für unzustellbare Meldungen wird mithilfe des `customDeadLetterQueue`-Attributs festgelegt. Andernfalls gilt die entsprechende, auf den Zusicherungen basierende Standardeinstellung.|  
|UseActiveDirectory|Ein boolescher Wert, der angibt, ob die Warteschlangenadressen mit Active Directory konvertiert werden sollen.<br /><br /> MSMQ-Warteschlangenadressen können aus Pfadnamen oder aus direkten Formatnamen bestehen. Bei direkten Formatnamen wird der Computername von MSMQ mit DNS, NetBIOS oder IP aufgelöst. Bei Pfadnamen wird der Computername von MSMQ mit Active Directory aufgelöst. Standardmäßig konvertiert der WCF-Warteschlangentransport den URI einer Nachrichtenwarteschlange in einen direkten Formatnamen. Durch Festlegen dieses Attributs auf `true` kann eine Anwendung angeben, dass der Computername vom Warteschlangentransport mit Active Directory statt mit DNS, NetBIOS oder IP aufgelöst werden soll.|  
|useMsmqTracing|Ein boolescher Wert, der angibt, ob von dieser Bindung verarbeitete Nachrichten verfolgt werden sollen. Die Standardeinstellung ist `false`.<br /><br /> Wenn die Ablaufverfolgung aktiviert ist, werden Berichtsnachrichten erstellt und jedes Mal an die Berichtswarteschlange gesendet, wenn die Nachricht einen Computer mit Message Queuing erreicht oder verlässt.|  
|useSourceJournal|Ein boolescher Wert, der angibt, ob Kopien der von dieser Bindung verarbeiteten Nachrichten in der Quelljournalwarteschlange gespeichert werden sollen. Die Standardeinstellung ist `false`.<br /><br /> Anwendungen in Warteschlangen, die Nachrichten aufzeichnen möchten, die die Ausgangswarteschlange des Computers verlassen haben, können die Nachrichten in eine Journalwarteschlange kopieren. Wenn eine Nachricht die Ausgangswarteschlange verlässt und eine Bestätigung empfangen wird, dass die Nachricht auf dem Zielcomputer empfangen wurde, wird eine Kopie der Nachricht in der Systemjournalwarteschlange des sendenden Computers beibehalten.|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<MsmqTransportSecurity >](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqtransportsecurity.md)|Gibt Transportsicherheitseinstellungen für diese Bindung an. Dieses Element ist vom Typ <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<binding>](../../../../../docs/framework/misc/binding.md)|Definiert alle Bindungsmöglichkeiten der benutzerdefinierten Bindung.|  
  
## <a name="remarks"></a>Hinweise  
 Das `msmqTransport`-Element ermöglicht es dem Benutzer, die Eigenschaften des Warteschlangenkommunikationskanals festzulegen. Der Warteschlangenkommunikationskanal verwendet das Message Queuing für den Transport.  
  
 Dieses Bindungselement ist das Standardbindungselement für die Message Queuing-Standardbindung (`netMsmqBinding`).  
  
## <a name="see-also"></a>Siehe auch  
 <xref:System.ServiceModel.Configuration.MsmqTransportElement>  
 <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>  
 <xref:System.ServiceModel.Channels.TransportBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [Warteschlangen in WCF](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [Transportprotokolle](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [Auswählen eines Transports](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [Bindungen](../../../../../docs/framework/wcf/bindings.md)  
 [Erweitern von Bindungen](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [Benutzerdefinierte Bindungen](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
