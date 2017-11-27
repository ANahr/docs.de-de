---
title: ICorDebugNativeFrame::GetIP-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugNativeFrame.GetIP
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugNativeFrame::GetIP
helpviewer_keywords:
- GetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
- ICorDebugNativeFrame::GetIP method [.NET Framework debugging]
ms.assetid: 99f693f3-d3b9-4fd8-9d09-b8efd03f7b67
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ceb0188ce2a52c3950b5fc89ea15c96852910d88
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugnativeframegetip-method"></a>ICorDebugNativeFrame::GetIP-Methode
Ruft der systemeigene Code offset Speicherort, der der Anweisungszeiger aktuell festgelegt ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetIP (  
    [out] ULONG32           *pnOffset  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pnOffset`  
 [out] Ein Zeiger auf die Offsetposition im systemeigenen Code.  
  
## <a name="remarks"></a>Hinweise  
 Wenn der Stapelrahmen, der durch diese "ICorDebugNativeFrame" dargestellt wird aktiv ist, ist der Offset die Adresse der nächsten Anweisung ausgeführt werden. Wenn dieser Stapelrahmen nicht aktiv ist, ist der Offset der Adresse der nächsten Anweisung bei neuaktivierung des Stapelrahmens ausgeführt werden.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 
