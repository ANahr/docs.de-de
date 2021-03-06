---
title: DataContractSerializer-Beispiel
ms.date: 03/30/2017
helpviewer_keywords:
- XML Formatter
ms.assetid: e0a2fe89-3534-48c8-aa3c-819862224571
ms.openlocfilehash: d35798ea2cd5f2fe6285bce4e465e4c79f44cb50
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53242656"
---
# <a name="datacontractserializer-sample"></a>DataContractSerializer-Beispiel
Das DataContractSerializer-Beispiel veranschaulicht den <xref:System.Runtime.Serialization.DataContractSerializer>, der allgemeine Serialisierungs- und Deserialisierungsdienste für die Datenvertragsklassen ausführt. Das Beispiel erstellt eine `Record` Objekt, das in einen Speicherdatenstrom serialisiert und deserialisiert diesen wieder in einen anderen `Record` Objekt, das veranschaulichen der Verwendung von der <xref:System.Runtime.Serialization.DataContractSerializer>. Das Beispiel serialisiert dann das `Record`-Objekt mithilfe eines Binärwriters, um zu veranschaulichen, wie der Writer die Serialisierung beeinflusst.  
  
> [!NOTE]
>  Die Setupprozedur und die Buildanweisungen für dieses Beispiel befinden sich am Ende dieses Themas.  
  
 Der Datenvertrag für `Record` wird im folgenden Beispielcode gezeigt.  
  
```csharp  
[DataContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
internal class Record  
{  
    private double n1;  
    private double n2;  
    private string operation;  
    private double result;  
  
    internal Record(double n1, double n2, string operation, double result)  
    {  
        this.n1 = n1;  
        this.n2 = n2;  
        this.operation = operation;  
        this.result = result;  
    }  
  
    [DataMember]  
    internal double OperandNumberOne  
    {  
        get { return n1; }  
        set { n1 = value; }  
    }  
  
    [DataMember]  
    internal double OperandNumberTwo  
    {  
        get { return n2; }  
        set { n2 = value; }  
    }  
  
    [DataMember]  
    internal string Operation  
    {  
        get { return operation; }  
        set { operation = value; }  
    }  
  
    [DataMember]  
    internal double Result  
    {  
        get { return result; }  
        set { result = value; }  
    }  
  
    public override string ToString()  
    {  
        return $"Record: {n1} {operation} {n2} = {result}";
    }  
}  
```  
  
 Der Beispielcode erstellt ein `Record`-Objekt namens `record1` und zeigt dann das Objekt an.  
  
```csharp
Record record1 = new Record(1, 2, "+", 3);  
Console.WriteLine("Original record: {0}", record1.ToString());  
```  
  
 Das Beispiel nutzt dann <xref:System.Runtime.Serialization.DataContractSerializer>, um `record1` in einen Speicherstream zu serialisieren.  
  
```csharp  
MemoryStream stream1 = new MemoryStream();  
  
//Serialize the Record object to a memory stream using DataContractSerializer.  
DataContractSerializer serializer = new DataContractSerializer(typeof(Record));  
serializer.WriteObject(stream1, record1);  
```  
  
 Danach nutzt das Beispiel <xref:System.Runtime.Serialization.DataContractSerializer>, um den Speicherstream in ein neues `Record`-Objekt zu deserialisieren, und zeigt es an.  
  
```csharp  
stream1.Position = 0;  
  
//Deserialize the Record object back into a new record object.  
Record record2 = (Record)serializer.ReadObject(stream1);  
  
Console.WriteLine("Deserialized record: {0}", record2.ToString());  
```  
  
 Standardmäßig codiert `DataContractSerializer` Objekte mithilfe einer Textdarstellung von XML in einen Stream. Sie können die XML-Codierung allerdings beeinflussen, indem Sie an einen anderen Writer übergeben. Im Beispiel wird ein Binärwriter durch den Aufruf von <xref:System.Xml.XmlDictionaryWriter.CreateBinaryWriter%2A> erstellt. Der Writer und das Datensatzobjekt werden dann an das Serialisierungsprogramm übergeben, wenn <xref:System.Runtime.Serialization.DataContractSerializer.WriteObjectContent%2A> aufgerufen wird. Im Beispiel wird schließlich der Writer geleert und die Länge des Streams gemeldet.  
  
```csharp  
MemoryStream stream2 = new MemoryStream();  
  
XmlDictionaryWriter binaryDictionaryWriter = XmlDictionaryWriter.CreateBinaryWriter(stream2);  
serializer.WriteObject(binaryDictionaryWriter, record1);  
binaryDictionaryWriter.Flush();  
  
//report the length of the streams  
Console.WriteLine("Text Stream is {0} bytes long", stream1.Length);  
Console.WriteLine("Binary Stream is {0} bytes long", stream2.Length);  
```  
  
 Bei der Durchführung des Beispiels werden der Originaldatensatz und der deserialisierte Datensatz gefolgt vom Vergleich zwischen der Länge der Textcodierung und der binären Codierung angezeigt. Drücken Sie im Clientfenster die EINGABETASTE, um den Client zu schließen.  
  
```console  
Original record: Record: 1 + 2 = 3  
Deserialized record: Record: 1 + 2 = 3  
Text Stream is 233 bytes long  
Binary Stream is 156 bytes long  
  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a>So können Sie das Beispiel einrichten, erstellen und ausführen  
  
1.  Stellen Sie sicher, dass Sie ausgeführt haben die [Schritte der Einrichtung einmaligen Setupverfahren für Windows Communication Foundation-Beispiele](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2.  Um die C#- oder Visual Basic .NET-Edition der Projektmappe zu erstellen, befolgen Sie die unter [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md)aufgeführten Anweisungen.  
  
3.  Um das Beispiel auszuführen, starten Sie den Client, indem Sie client\bin\client.exe in die Eingabeaufforderung eingeben.  
  
> [!IMPORTANT]
>  Die Beispiele sind möglicherweise bereits auf dem Computer installiert. Suchen Sie nach dem folgenden Verzeichnis (Standardverzeichnis), bevor Sie fortfahren.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Wenn dieses Verzeichnis nicht vorhanden ist, fahren Sie mit [Windows Communication Foundation (WCF) und Windows Workflow Foundation (WF) Samples für .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) alle Windows Communication Foundation (WCF) herunterladen und [!INCLUDE[wf1](../../../../includes/wf1-md.md)] Beispiele. Dieses Beispiel befindet sich im folgenden Verzeichnis.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Contract\Data\DataContractSerializer`  
  
## <a name="see-also"></a>Siehe auch
