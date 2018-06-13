---
title: IGCThreadControl::SuspensionEnding-Methode
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d0986645a8ce4076c27f39f2ae8004ef20bb4bdb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437751"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="8f7fd-102">IGCThreadControl::SuspensionEnding-Methode</span><span class="sxs-lookup"><span data-stu-id="8f7fd-102">IGCThreadControl::SuspensionEnding Method</span></span>
<span data-ttu-id="8f7fd-103">Benachrichtigt den Host an, dass die Laufzeit Threads nach einer Garbagecollection oder einer anderen Unterbrechung fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7fd-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f7fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f7fd-104">Syntax</span></span>  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8f7fd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7fd-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="8f7fd-106">[in] Die Generierung, für die eine Garbagecollection ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f7fd-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8f7fd-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f7fd-107">Remarks</span></span>  
 <span data-ttu-id="8f7fd-108">Darf nicht verlegt werden alle Threads, die während der `SuspensionEnding` Rückruf.</span><span class="sxs-lookup"><span data-stu-id="8f7fd-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f7fd-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f7fd-109">Requirements</span></span>  
 <span data-ttu-id="8f7fd-110">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8f7fd-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f7fd-111">**Header:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8f7fd-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8f7fd-112">**Bibliothek:** als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="8f7fd-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f7fd-113">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f7fd-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f7fd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f7fd-114">See Also</span></span>  
 [<span data-ttu-id="8f7fd-115">IGCThreadControl-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8f7fd-115">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
