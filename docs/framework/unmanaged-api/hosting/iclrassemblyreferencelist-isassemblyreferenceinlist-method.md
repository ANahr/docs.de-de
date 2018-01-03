---
title: ICLRAssemblyReferenceList::IsAssemblyReferenceInList-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRAssemblyReferenceList.IsAssemblyReferenceInList
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRAssemblyReferenceList::IsAssemblyReferenceInList
helpviewer_keywords:
- ICLRAssemblyReferenceList::IsAssemblyReferenceInList method [.NET Framework hosting]
- IsAssemblyReferenceInList method [.NET Framework hosting]
ms.assetid: 8a570813-21be-407e-92a6-7ae8de3bc728
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: e403cd3a2adfa77bd2faf368a6effdfa42213a76
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="iclrassemblyreferencelistisassemblyreferenceinlist-method"></a><span data-ttu-id="71314-102">ICLRAssemblyReferenceList::IsAssemblyReferenceInList-Methode</span><span class="sxs-lookup"><span data-stu-id="71314-102">ICLRAssemblyReferenceList::IsAssemblyReferenceInList Method</span></span>
<span data-ttu-id="71314-103">Ruft einen Wert, der angibt, ob der angegebene Zeiger auf eine Assembly in der Liste verweist.</span><span class="sxs-lookup"><span data-stu-id="71314-103">Gets a value that indicates whether the supplied pointer refers to an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71314-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71314-104">Syntax</span></span>  
  
```  
HRESULT IsAssemblyReferenceInList (  
    [in] IUnknown *pName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="71314-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="71314-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="71314-106">[in] Ein Schnittstellenzeiger auf die Assembly nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="71314-106">[in] An interface pointer to the assembly for which to search.</span></span> <span data-ttu-id="71314-107">Gültige Werte sind vom Typ `IAssemblyName` oder `IReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="71314-107">Valid values are of type `IAssemblyName` or `IReferenceIdentity`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="71314-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71314-108">Return Value</span></span>  
  
|<span data-ttu-id="71314-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="71314-109">HRESULT</span></span>|<span data-ttu-id="71314-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71314-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="71314-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="71314-111">S_OK</span></span>|<span data-ttu-id="71314-112">Die Zeichenfolge, die in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="71314-112">The string appears in the list.</span></span>|  
|<span data-ttu-id="71314-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="71314-113">S_FALSE</span></span>|<span data-ttu-id="71314-114">Die Zeichenfolge wird in der Liste nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71314-114">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="71314-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="71314-115">E_FAIL</span></span>|<span data-ttu-id="71314-116">Ein Unbekannter Schwerwiegender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="71314-116">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="71314-117">Nachdem eine Methode E_FAIL zurückgegeben hat, ist die common Language Runtime nicht mehr verwendbar innerhalb des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="71314-117">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="71314-118">Nachfolgende Aufrufe zum Hosten der Methoden HOST_E_CLRNOTAVAILABLE zurück.</span><span class="sxs-lookup"><span data-stu-id="71314-118">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="71314-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71314-119">Requirements</span></span>  
 <span data-ttu-id="71314-120">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="71314-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71314-121">**Header:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="71314-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="71314-122">**Bibliothek:** als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="71314-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="71314-123">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71314-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71314-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71314-124">See Also</span></span>  
 [<span data-ttu-id="71314-125">ICLRAssemblyIdentityManager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71314-125">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [<span data-ttu-id="71314-126">ICLRAssemblyReferenceList-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71314-126">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="71314-127">IHostAssemblyManager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71314-127">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="71314-128">IHostAssemblyStore-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71314-128">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
