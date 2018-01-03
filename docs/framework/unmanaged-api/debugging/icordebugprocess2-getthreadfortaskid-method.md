---
title: ICorDebugProcess2::GetThreadForTaskID-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess2.GetThreadForTaskID
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess2::GetThreadForTaskID
helpviewer_keywords:
- ICorDebugProcess2::GetThreadForTaskId method [.NET Framework debugging]
- GetThreadForTaskID method [.NET Framework debugging]
ms.assetid: 32d54a5b-8ad3-405b-a1b9-0936a3b49d1e
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: af63e6cf0d7e4b51f9365c1ccc4ac78158c091bf
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugprocess2getthreadfortaskid-method"></a><span data-ttu-id="80f4a-102">ICorDebugProcess2::GetThreadForTaskID-Methode</span><span class="sxs-lookup"><span data-stu-id="80f4a-102">ICorDebugProcess2::GetThreadForTaskID Method</span></span>
<span data-ttu-id="80f4a-103">Ruft den Thread, in dem die Aufgabe mit dem angegebenen Bezeichner ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80f4a-103">Gets the thread on which the task with the specified identifier is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80f4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80f4a-104">Syntax</span></span>  
  
```  
HRESULT GetThreadForTaskID (  
    [in]  TASKID            taskid,  
    [out] ICorDebugThread2  **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="80f4a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="80f4a-105">Parameters</span></span>  
 `taskid`  
 <span data-ttu-id="80f4a-106">[in] Der Bezeichner der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="80f4a-106">[in] The identifier of the task.</span></span>  
  
 `ppThread`  
 <span data-ttu-id="80f4a-107">[out] Ein Zeiger auf die Adresse eines ICorDebugThread2-Objekts, die der Thread darstellt, abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="80f4a-107">[out] A pointer to the address of an ICorDebugThread2 object that represents the thread to be retrieved.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="80f4a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80f4a-108">Remarks</span></span>  
 <span data-ttu-id="80f4a-109">Der Host kann der Task-ID festlegen, mit der [ICLRTask:: SetTaskIdentifier](../../../../docs/framework/unmanaged-api/hosting/iclrtask-settaskidentifier-method.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="80f4a-109">The host can set the task identifier by using the [ICLRTask::SetTaskIdentifier](../../../../docs/framework/unmanaged-api/hosting/iclrtask-settaskidentifier-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80f4a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80f4a-110">Requirements</span></span>  
 <span data-ttu-id="80f4a-111">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="80f4a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80f4a-112">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="80f4a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="80f4a-113">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="80f4a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="80f4a-114">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80f4a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
