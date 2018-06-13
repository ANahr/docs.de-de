---
title: ICorDebugModule::GetAssembly-Methode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetAssembly
helpviewer_keywords:
- ICorDebugModule::GetAssembly method [.NET Framework debugging]
- GetAssembly method [.NET Framework debugging]
ms.assetid: 989762c4-3d15-4485-b8ee-69e0fa8ec895
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78bfc91bdd0f9fa68252c6a07e1362807eb507b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416022"
---
# <a name="icordebugmodulegetassembly-method"></a><span data-ttu-id="8a84c-102">ICorDebugModule::GetAssembly-Methode</span><span class="sxs-lookup"><span data-stu-id="8a84c-102">ICorDebugModule::GetAssembly Method</span></span>
<span data-ttu-id="8a84c-103">Ruft die enthaltende Assembly für dieses Modul ab.</span><span class="sxs-lookup"><span data-stu-id="8a84c-103">Gets the containing assembly for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a84c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a84c-104">Syntax</span></span>  
  
```  
HRESULT GetAssembly(  
    [out] ICorDebugAssembly **ppAssembly  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8a84c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a84c-105">Parameters</span></span>  
 `ppAssembly`  
 <span data-ttu-id="8a84c-106">[out] Ein Zeiger auf ein ICorDebugAssembly-Objekt, das die Assembly mit diesem Modul darstellt.</span><span class="sxs-lookup"><span data-stu-id="8a84c-106">[out] A pointer to an ICorDebugAssembly object that represents the assembly containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a84c-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a84c-107">Requirements</span></span>  
 <span data-ttu-id="8a84c-108">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a84c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a84c-109">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8a84c-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a84c-110">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a84c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a84c-111">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a84c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
