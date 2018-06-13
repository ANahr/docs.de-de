---
title: ICorDebugSymbolProvider::GetObjectSize-Methode
ms.date: 03/30/2017
ms.assetid: 3c564396-ac64-4ef3-b4f6-df96f1d46fc7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1da526ac133604fa43081f86988459c4238517c9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421502"
---
# <a name="icordebugsymbolprovidergetobjectsize-method"></a><span data-ttu-id="5643e-102">ICorDebugSymbolProvider::GetObjectSize-Methode</span><span class="sxs-lookup"><span data-stu-id="5643e-102">ICorDebugSymbolProvider::GetObjectSize Method</span></span>
<span data-ttu-id="5643e-103">Gibt die Objektgröße eines Objekts basierend auf seiner TypeSpec-Signatur zurück.</span><span class="sxs-lookup"><span data-stu-id="5643e-103">Returns the object size for an object based on its typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5643e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5643e-104">Syntax</span></span>  
  
```  
HRESULT GetObjectSize(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [out] ULONG32 *pObjectSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5643e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5643e-105">Parameters</span></span>  
 `cbSignature`  
 <span data-ttu-id="5643e-106">[in] Die Anzahl der Bytes in der TypeSpec-Signatur.</span><span class="sxs-lookup"><span data-stu-id="5643e-106">[in] The number of bytes in the typespec signature.</span></span>  
  
 <span data-ttu-id="5643e-107">typeSig</span><span class="sxs-lookup"><span data-stu-id="5643e-107">typeSig</span></span>  
 <span data-ttu-id="5643e-108">[in] Die TypeSpec-Signatur.</span><span class="sxs-lookup"><span data-stu-id="5643e-108">[in] The typespec signature.</span></span>  
  
 `pObjectSize`  
 <span data-ttu-id="5643e-109">[out] Ein Zeiger auf die Größe des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5643e-109">[out] A pointer to the size of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5643e-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5643e-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5643e-111">Diese Methode ist nur mit .NET Native verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5643e-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5643e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5643e-112">Requirements</span></span>  
 <span data-ttu-id="5643e-113">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5643e-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5643e-114">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5643e-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5643e-115">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5643e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5643e-116">**.NET Framework-Versionen:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5643e-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5643e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5643e-117">See Also</span></span>  
 [<span data-ttu-id="5643e-118">ICorDebugSymbolProvider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5643e-118">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="5643e-119">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5643e-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
