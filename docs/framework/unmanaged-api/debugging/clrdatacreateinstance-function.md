---
title: CLRDataCreateInstance-Funktion
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CLRDataCreateInstance
api_location:
- mscordbi.dll
- mscordacwks.dll
api_type: COM
f1_keywords: CLRDataCreateInstance
helpviewer_keywords: CLRDataCreateInstance function [.NET Framework debugging]
ms.assetid: 440bad90-5a88-45e7-9157-4596801d8d19
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 0740e80732e03ac6c1e7cf974d258113a181ea9d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="clrdatacreateinstance-function"></a><span data-ttu-id="4e170-102">CLRDataCreateInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e170-102">CLRDataCreateInstance Function</span></span>
<span data-ttu-id="4e170-103">Erstellt ein Schnittstellenobjekt für das angegebene Ziel-Element.</span><span class="sxs-lookup"><span data-stu-id="4e170-103">Creates an interface object for the specified target item.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e170-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e170-104">Syntax</span></span>  
  
```  
HRESULT CLRDataCreateInstance (  
    [in]  REFIID           iid,   
    [in]  ICLRDataTarget  *target,   
    [out] void           **iface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4e170-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e170-105">Parameters</span></span>  
 `iid`  
 <span data-ttu-id="4e170-106">[in] Der Bezeichner der Schnittstelle instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e170-106">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="4e170-107">[in] Ein Zeiger auf eine vom Benutzer implementierte [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) Objekt, das des Zielelements für die zum Erstellen des Schnittstellenobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="4e170-107">[in] A pointer to a user-implemented [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="4e170-108">[out] Ein Zeiger auf die Adresse des Objekts zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4e170-108">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4e170-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e170-109">Remarks</span></span>  
 <span data-ttu-id="4e170-110">Die `ICLRDataTarget` Objekt wird vom Writer der Debuganwendung implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e170-110">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="4e170-111">Die Implementierung hängt vom Typ des Zielelements dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e170-111">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="4e170-112">Das Zielelement ist möglicherweise ein Prozess, Speicherabbild Remotecomputer und So weiter.</span><span class="sxs-lookup"><span data-stu-id="4e170-112">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e170-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e170-113">Requirements</span></span>  
 <span data-ttu-id="4e170-114">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e170-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e170-115">**Header:** ClrData.idl</span><span class="sxs-lookup"><span data-stu-id="4e170-115">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="4e170-116">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4e170-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4e170-117">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e170-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e170-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e170-118">See Also</span></span>  
 [<span data-ttu-id="4e170-119">Debuggen von globalen statischen Funktionen</span><span class="sxs-lookup"><span data-stu-id="4e170-119">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
