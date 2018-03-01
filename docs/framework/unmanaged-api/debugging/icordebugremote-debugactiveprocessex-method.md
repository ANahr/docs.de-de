---
title: ICorDebugRemote::DebugActiveProcessEx-Methode
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
- ICorDebugRemote.DebugActiveProcessEx
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::DebugActiveProcessEx
helpviewer_keywords:
- ICorDebugRemote::DebugActiveProcessEx method [.NET Framework debugging]
- DebugActiveProcessEx method, ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: b0df5c5d-9a2e-47bf-894c-6f8a9fe24a1f
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 09bc98b477231eb1466300451585f4569aff222c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugremotedebugactiveprocessex-method"></a><span data-ttu-id="00647-102">ICorDebugRemote::DebugActiveProcessEx-Methode</span><span class="sxs-lookup"><span data-stu-id="00647-102">ICorDebugRemote::DebugActiveProcessEx Method</span></span>
<span data-ttu-id="00647-103">Startet einen Prozess auf einem Remotecomputer unter dem Debugger.</span><span class="sxs-lookup"><span data-stu-id="00647-103">Launches a process on a remote machine under the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00647-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00647-104">Syntax</span></span>  
  
```  
HRESULT DebugActiveProcessEx (  
    [in]  ICorDebugRemoteTarget *   pRemoteTarget,  
    [in]  DWORD                     dwProcessId,  
    [in]  BOOL                      fWin32Attach,  
    [out] ICorDebugProcess **       ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="00647-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="00647-105">Parameters</span></span>  
 `pRemoteTarget`  
 <span data-ttu-id="00647-106">[in] Zeiger auf eine [ICorDebugRemoteTarget-Schnittstelle](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md).</span><span class="sxs-lookup"><span data-stu-id="00647-106">[in] Pointer to an [ICorDebugRemoteTarget Interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md).</span></span> <span data-ttu-id="00647-107">Dieser Parameter wird verwendet, um den Computer zu ermitteln, auf dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00647-107">This parameter is used to determine the machine on which the process is running.</span></span>  
  
 `id`  
 <span data-ttu-id="00647-108">[in] Die ID des Prozesses, zu dem der Debugger angefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="00647-108">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="00647-109">[in] `true` , wenn der Debugger sollte sich so wie die Win32-Debugger für den Prozess Verhalten und die nicht verwalteten Rückrufe; anderenfalls `false`.</span><span class="sxs-lookup"><span data-stu-id="00647-109">[in] `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="00647-110">[out] Ein Zeiger auf die Adresse eines Objekts "ICorDebugProcess", das den Prozess darstellt, an dem der Debugger angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="00647-110">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00647-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00647-111">Return Value</span></span>  
 <span data-ttu-id="00647-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="00647-112">S_OK</span></span>  
 <span data-ttu-id="00647-113">An den Prozess auf dem Remotecomputer wurde erfolgreich angefügt.</span><span class="sxs-lookup"><span data-stu-id="00647-113">Successfully attached to the process on the remote machine.</span></span>  
  
 <span data-ttu-id="00647-114">E_FAIL (oder andere E_-Rückgabecodes)</span><span class="sxs-lookup"><span data-stu-id="00647-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="00647-115">Anfügen an den Prozess auf dem Remotecomputer ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="00647-115">Unable to attach to the process on the remote machine.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="00647-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00647-116">Remarks</span></span>  
 <span data-ttu-id="00647-117">Debuggen im gemischten Modus ist in Silverlight nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00647-117">Mixed-mode debugging is not supported in Silverlight.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00647-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00647-118">Requirements</span></span>  
 <span data-ttu-id="00647-119">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00647-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00647-120">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="00647-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="00647-121">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="00647-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="00647-122">**.NET Framework-Versionen:** 4.5, 4, 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="00647-122">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00647-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00647-123">See Also</span></span>  
 [<span data-ttu-id="00647-124">ICorDebugRemote-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="00647-124">ICorDebugRemote Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-interface.md)  
 [<span data-ttu-id="00647-125">ICorDebug-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="00647-125">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
    
 [<span data-ttu-id="00647-126">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="00647-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
