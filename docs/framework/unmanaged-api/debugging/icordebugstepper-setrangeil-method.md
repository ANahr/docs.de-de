---
title: ICorDebugStepper::SetRangeIL-Methode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetRangeIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetRangeIL
helpviewer_keywords:
- SetRangeIL method [.NET Framework debugging]
- ICorDebugStepper::SetRangeIL method [.NET Framework debugging]
ms.assetid: a20c95f0-6da7-4b41-b27f-584211cebb92
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb3c24b3a96a03359dc6983bcaac4a800613ff5d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420530"
---
# <a name="icordebugsteppersetrangeil-method"></a><span data-ttu-id="86400-102">ICorDebugStepper::SetRangeIL-Methode</span><span class="sxs-lookup"><span data-stu-id="86400-102">ICorDebugStepper::SetRangeIL Method</span></span>
<span data-ttu-id="86400-103">Legt einen Wert, der angibt, ob Aufrufe von [ICorDebugStepper:: StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) Argument Werte, die relativ zu den systemeigenen Code oder relativ zum Microsoft intermediate Language (MSIL)-Code der Methode, die schrittweise wird übergeben durch.</span><span class="sxs-lookup"><span data-stu-id="86400-103">Sets a value that specifies whether calls to [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) pass argument values that are relative to the native code or relative to Microsoft intermediate language (MSIL) code of the method that is being stepped through.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86400-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86400-104">Syntax</span></span>  
  
```  
HRESULT SetRangeIL (  
    [in] BOOL    bIL  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="86400-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="86400-105">Parameters</span></span>  
 `bIL`  
 <span data-ttu-id="86400-106">[in] Legen Sie auf `true` um anzugeben, dass die Bereiche relativ zu der MSIL-Code haben.</span><span class="sxs-lookup"><span data-stu-id="86400-106">[in] Set to `true` to specify that the ranges are relative to the MSIL code.</span></span> <span data-ttu-id="86400-107">Legen Sie auf `false` um anzugeben, dass der Bereich relativ zu den systemeigenen Code liegt.</span><span class="sxs-lookup"><span data-stu-id="86400-107">Set to `false` to specify that the ranges are relative to the native code.</span></span> <span data-ttu-id="86400-108">Der Standardwert ist `true`.</span><span class="sxs-lookup"><span data-stu-id="86400-108">The default value is `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86400-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86400-109">Requirements</span></span>  
 <span data-ttu-id="86400-110">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86400-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86400-111">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="86400-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="86400-112">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86400-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="86400-113">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86400-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
