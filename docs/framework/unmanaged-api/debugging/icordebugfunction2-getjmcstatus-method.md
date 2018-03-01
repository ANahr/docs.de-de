---
title: ICorDebugFunction2::GetJMCStatus-Methode
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
- ICorDebugFunction2.GetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::GetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::GetJMCStatus method [.NET Framework debugging]
- GetJMCStatus method [.NET Framework debugging]
ms.assetid: 840a71ed-bf5a-4f5e-8ed6-762222b34493
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: d877b534ca2501117153047858a1a1f2736bdd4f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugfunction2getjmcstatus-method"></a><span data-ttu-id="fa190-102">ICorDebugFunction2::GetJMCStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="fa190-102">ICorDebugFunction2::GetJMCStatus Method</span></span>
<span data-ttu-id="fa190-103">Ruft einen Wert, der angibt, ob die Funktion, die von diesem ICorDebugFunction2-Objekt dargestellt wird als Benutzercode markiert ist.</span><span class="sxs-lookup"><span data-stu-id="fa190-103">Gets a value that indicates whether the function that is represented by this ICorDebugFunction2 object is marked as user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa190-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa190-104">Syntax</span></span>  
  
```  
HRESULT GetJMCStatus (  
    [out] BOOL   *pbIsJustMyCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fa190-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa190-105">Parameters</span></span>  
 `pbIsJustMyCode`  
 <span data-ttu-id="fa190-106">[out] Ein Zeiger auf einen booleschen Wert, der `true`, wenn diese Funktion als Benutzercode markiert ist; andernfalls wird der Wert `false`.</span><span class="sxs-lookup"><span data-stu-id="fa190-106">[out] A pointer to a Boolean value that is `true`, if this function is marked as user code; otherwise, the value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa190-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa190-107">Remarks</span></span>  
 <span data-ttu-id="fa190-108">Wenn die Funktion von diesem dargestellt `ICorDebugFunction2` kann nicht debuggt werden, `pbIsJustMyCode` immer `false`.</span><span class="sxs-lookup"><span data-stu-id="fa190-108">If the function represented by this `ICorDebugFunction2` cannot be debugged, `pbIsJustMyCode` will always be `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa190-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa190-109">Requirements</span></span>  
 <span data-ttu-id="fa190-110">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa190-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa190-111">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fa190-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fa190-112">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa190-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa190-113">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa190-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
