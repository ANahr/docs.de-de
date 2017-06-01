---
title: "Gewusst wie: Anfordern einer Webseite und Abrufen der Ergebnisse als Stream | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
ms.assetid: d32b7f35-29d8-4fb7-ad71-d219edc5e359
caps.latest.revision: 12
author: "mcleblanc"
ms.author: "markl"
manager: "markl"
caps.handback.revision: 12
---
# Gewusst wie: Anfordern einer Webseite und Abrufen der Ergebnisse als Stream
Dieses Beispiel zeigt, wie Sie um eine Webseite anfordert und die Ergebnisse in einem Stream abruft.  
  
## Beispiel  
  
```csharp  
WebClient myClient = new WebClient();  
Stream response = myClient.OpenRead("http://www.contoso.com/index.htm");  
// The stream data is used here.  
response.Close();  
```  
  
```vb  
Dim myClient As WebClient = New WebClient()  
Dim response As Stream = myClient.OpenRead("http://www.contoso.com/index.htm")  
' The stream data is used here.  
response.Close()  
```  
  
## Kompilieren des Codes  
 Dieses Beispiel setzt Folgendes voraus:  
  
-   Verweise auf den <xref:System.IO>\-Namespace und den <xref:System.Net>\-Namespace.  
  
## Siehe auch  
 [Anfordern von Daten](../../../docs/framework/network-programming/requesting-data.md)