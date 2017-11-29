---
title: ICorDebugStringValue Schnittstelle1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStringValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStringValue
helpviewer_keywords: ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 03ae6fba5d880b11baac695866853e0b3a4d8cc7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugstringvalue-interface1"></a><span data-ttu-id="8603d-102">ICorDebugStringValue Schnittstelle1</span><span class="sxs-lookup"><span data-stu-id="8603d-102">ICorDebugStringValue Interface1</span></span>
<span data-ttu-id="8603d-103">Eine Unterklasse von ICorDebugHeapValue, die für Zeichenfolgenwerte gilt.</span><span class="sxs-lookup"><span data-stu-id="8603d-103">A subclass of ICorDebugHeapValue that applies to string values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8603d-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="8603d-104">Methods</span></span>  
  
|<span data-ttu-id="8603d-105">Methode</span><span class="sxs-lookup"><span data-stu-id="8603d-105">Method</span></span>|<span data-ttu-id="8603d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8603d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8603d-107">GetLength-Methode</span><span class="sxs-lookup"><span data-stu-id="8603d-107">GetLength Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getlength-method.md)|<span data-ttu-id="8603d-108">Ruft die Anzahl der Zeichen in der Zeichenfolge, die auf die verwiesen wird von diesem `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="8603d-108">Gets the number of characters in the string referenced by this `ICorDebugStringValue`.</span></span>|  
|[<span data-ttu-id="8603d-109">GetString-Methode</span><span class="sxs-lookup"><span data-stu-id="8603d-109">GetString Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getstring-method.md)|<span data-ttu-id="8603d-110">Ruft die Zeichenfolge, die auf die verwiesen wird von diesem `ICorDebugStringValue`.</span><span class="sxs-lookup"><span data-stu-id="8603d-110">Gets the string referenced by this `ICorDebugStringValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8603d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8603d-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8603d-112">Diese Schnittstelle kann weder computerübergreifend noch prozessübergreifend remote aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8603d-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8603d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8603d-113">Requirements</span></span>  
 <span data-ttu-id="8603d-114">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8603d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8603d-115">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8603d-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8603d-116">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8603d-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8603d-117">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8603d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8603d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8603d-118">See Also</span></span>  
 [<span data-ttu-id="8603d-119">Debugschnittstellen</span><span class="sxs-lookup"><span data-stu-id="8603d-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
