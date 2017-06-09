---
title: "1132 - InvokeMethodDoesNotUseAsyncPattern | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 436b3767-4460-46b0-9ea3-fc2963260c11
caps.latest.revision: 2
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 2
---
# 1132 - InvokeMethodDoesNotUseAsyncPattern
## Eigenschaften  
  
|||  
|-|-|  
|ID|1132|  
|Schlüsselwörter|WFRuntime|  
|Ebene|Information|  
|Kanal|Microsoft\-Windows\-Application Server\-Applications\/Debug|  
  
## Beschreibung  
 Während des CacheMetadata\-Schritts gibt die InvokeMethod\-Aktivität an, dass sie das asynchrone Muster für den Methodenaufruf nicht verwendet.  
  
## Meldung  
 InvokeMethod '%1' \- Methode verwendet kein asynchrones Muster.  
  
## Details  
  
|Datenelementname|Datenelementtyp|Beschreibung|  
|----------------------|---------------------|------------------|  
|InvokeMethod|xs:string|Der Anzeigename der InvokeMethod\-Aktivität.|  
|AppDomain|xs:string|Die von AppDomain.CurrentDomain.FriendlyName zurückgegebene Zeichenfolge.|