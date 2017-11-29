---
title: ICorDebugEval::Abort-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugEval.Abort
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugEval::Abort
helpviewer_keywords:
- Abort method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::Abort method [.NET Framework debugging]
ms.assetid: 7070b6d0-f2e0-44ff-b124-0944cd807e69
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a53597067d14c5b3dc1f8829b8ea0a0df07de25a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugevalabort-method"></a><span data-ttu-id="34894-102">ICorDebugEval::Abort-Methode</span><span class="sxs-lookup"><span data-stu-id="34894-102">ICorDebugEval::Abort Method</span></span>
<span data-ttu-id="34894-103">Bricht die Berechnung, die derzeit diese ICorDebugEval-Objekt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34894-103">Aborts the computation this ICorDebugEval object is currently performing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34894-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34894-104">Syntax</span></span>  
  
```  
HRESULT Abort ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="34894-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34894-105">Remarks</span></span>  
 <span data-ttu-id="34894-106">Wenn die Auswertung geschachtelt ist und es nicht der aktuellste Auftrag ist die `Abort` -Methode schlägt möglicherweise fehl.</span><span class="sxs-lookup"><span data-stu-id="34894-106">If the evaluation is nested and it is not the most recent one, the `Abort` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34894-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34894-107">Requirements</span></span>  
 <span data-ttu-id="34894-108">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="34894-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34894-109">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="34894-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="34894-110">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="34894-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="34894-111">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34894-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
