---
title: ICorDebugNativeFrame::GetIP-Methode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetIP
helpviewer_keywords:
- GetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
- ICorDebugNativeFrame::GetIP method [.NET Framework debugging]
ms.assetid: 99f693f3-d3b9-4fd8-9d09-b8efd03f7b67
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d17ac4230296674381c87851377fcb535837ad3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416818"
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
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch  
 
