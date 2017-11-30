---
title: ICorDebugLoadedModule::GetName-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 88c304d5-edaa-4c0e-a8e1-144e8a76877e
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: aee475dfc425eea32ce4a1e5b4a081593574ba64
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugloadedmodulegetname-method"></a><span data-ttu-id="ff071-102">ICorDebugLoadedModule::GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="ff071-102">ICorDebugLoadedModule::GetName Method</span></span>
<span data-ttu-id="ff071-103">Ruft den Namen des geladenen Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="ff071-103">Gets the name of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff071-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff071-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,  
   [out] ULONG32 *pcchName,  
   [out, size_is(cchName),  
   length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ff071-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff071-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="ff071-106">[in] Die Anzahl der Zeichen im `szName`-Puffer.</span><span class="sxs-lookup"><span data-stu-id="ff071-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="ff071-107">[out] Ein Zeiger auf die Anzahl der tatsächlich in den `szName`-Puffer geschriebenen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ff071-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="ff071-108">[out] Ein Array von Zeichen, die den Namen des geladenen Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff071-108">[out] An array of characters that contain the name of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ff071-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff071-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ff071-110">Diese Methode ist nur in Verbindung mit .NET Native verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff071-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff071-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff071-111">Requirements</span></span>  
 <span data-ttu-id="ff071-112">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff071-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff071-113">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ff071-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ff071-114">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ff071-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ff071-115">**.NET Framework-Versionen:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff071-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff071-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff071-116">See Also</span></span>  
 [<span data-ttu-id="ff071-117">ICorDebugLoadedModule-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ff071-117">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)  
 [<span data-ttu-id="ff071-118">Debugschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ff071-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
