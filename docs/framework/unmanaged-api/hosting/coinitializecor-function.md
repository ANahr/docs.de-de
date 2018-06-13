---
title: CoInitializeCor-Funktion
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91315e8af0cc46a3450a7515b885988cffe34927
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429987"
---
# <a name="coinitializecor-function"></a><span data-ttu-id="d4cd5-102">CoInitializeCor-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4cd5-102">CoInitializeCor Function</span></span>
<span data-ttu-id="d4cd5-103">`CoInitializeCor` ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4cd5-103">`CoInitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4cd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4cd5-104">Syntax</span></span>  
  
```  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="d4cd5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4cd5-105">Remarks</span></span>  
 <span data-ttu-id="d4cd5-106">Verwenden Sie zum Initialisieren der common Language Runtime entweder [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) oder [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4cd5-106">To initialize the common language runtime, use either [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4cd5-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4cd5-107">Requirements</span></span>  
 <span data-ttu-id="d4cd5-108">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d4cd5-108">**Header:** Cor.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4cd5-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4cd5-109">See Also</span></span>  
 [<span data-ttu-id="d4cd5-110">Globale statische Metadatenfunktionen</span><span class="sxs-lookup"><span data-stu-id="d4cd5-110">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
