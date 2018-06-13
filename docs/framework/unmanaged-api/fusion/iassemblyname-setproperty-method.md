---
title: IAssemblyName::SetProperty-Methode
ms.date: 03/30/2017
api_name:
- IAssemblyName.SetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::SetProperty
helpviewer_keywords:
- IAssemblyName::SetProperty method [.NET Framework fusion]
- SetProperty method [.NET Framework fusion]
ms.assetid: 496c3add-f60b-4073-943f-d1bcf33330cb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bcfb584fc2380a7ae1567d3d4d6203b537676220
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429698"
---
# <a name="iassemblynamesetproperty-method"></a><span data-ttu-id="1cd7a-102">IAssemblyName::SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="1cd7a-102">IAssemblyName::SetProperty Method</span></span>
<span data-ttu-id="1cd7a-103">Legt den Wert der Eigenschaft, die vom Bezeichner angegebene Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1cd7a-103">Sets the value of the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cd7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd7a-104">Syntax</span></span>  
  
```  
HRESULT SetProperty (  
    [in] DWORD  PropertyId,  
    [in] LPVOID pvProperty,  
    [in] DWORD  cbProperty  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1cd7a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cd7a-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="1cd7a-106">[in] Der eindeutige Bezeichner der Eigenschaft, deren Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1cd7a-106">[in] The unique identifier of the property whose value will be set.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="1cd7a-107">[in] Der Wert, der zum Festlegen der Eigenschaft verweist `PropertyId`.</span><span class="sxs-lookup"><span data-stu-id="1cd7a-107">[in] The value to which to set the property referenced by `PropertyId`.</span></span>  
  
 `cbProperty`  
 <span data-ttu-id="1cd7a-108">[in] Die Größe in Bytes, der `pvProperty`.</span><span class="sxs-lookup"><span data-stu-id="1cd7a-108">[in] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cd7a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cd7a-109">Requirements</span></span>  
 <span data-ttu-id="1cd7a-110">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1cd7a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1cd7a-111">**Header:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="1cd7a-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="1cd7a-112">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1cd7a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cd7a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cd7a-113">See Also</span></span>  
 [<span data-ttu-id="1cd7a-114">IAssemblyName-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1cd7a-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
