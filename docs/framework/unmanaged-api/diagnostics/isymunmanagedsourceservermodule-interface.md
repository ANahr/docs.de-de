---
title: ISymUnmanagedSourceServerModule-Schnittstelle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ISymUnmanagedSourceServerModule
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule
helpviewer_keywords:
- ISymUnmanagedSourceServerModule interface [.NET Framework debugging]
ms.assetid: a19b23bd-2061-476e-b67d-252f57404f8b
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: f183c3ea69de15387f729a67328bf5ea57931750
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedsourceservermodule-interface"></a>ISymUnmanagedSourceServerModule-Schnittstelle
Server-Quelldaten bereitstellt für ein Modul. Rufen Sie diese Schnittstelle durch den Aufruf `QueryInterface` auf ein Objekt, implementiert die [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) Schnittstelle.  
  
## <a name="methods"></a>Methoden  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[GetSourceServerData-Methode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-getsourceserverdata-method.md)|Gibt die Quelldaten für die Server für das Modul zurück.|  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Siehe auch  
 [Diagnosesymbolspeicher-Schnittstellen](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
