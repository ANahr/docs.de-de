---
title: InitDbgTransportManager-Funktion
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: InitDbgTransportManager
api_location: mscordbi_macx86.dll
api_type: COM
f1_keywords: InitDbgTransportManager
helpviewer_keywords:
- remote debugging API [Silverlight]
- InitDbgTransportManager function
- Silverlight, remote debugging
ms.assetid: a30102ff-c52e-48c9-b3a9-aa14286a42b2
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f9f637589666af3723f11eb1f828d00be57793e5
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="initdbgtransportmanager-function"></a><span data-ttu-id="35f6c-102">InitDbgTransportManager-Funktion</span><span class="sxs-lookup"><span data-stu-id="35f6c-102">InitDbgTransportManager Function</span></span>
<span data-ttu-id="35f6c-103">Initialisiert den Transport-Manager, um eine Verbindung mit einem Remoteziel für eine Prozess- und Runtime-Enumeration herzustellen.</span><span class="sxs-lookup"><span data-stu-id="35f6c-103">Initializes the transport manager to connect to a remote target for process and runtime enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35f6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35f6c-104">Syntax</span></span>  
  
```  
HRESULT InitDbgTransportManager ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="35f6c-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35f6c-105">Return Value</span></span>  
 <span data-ttu-id="35f6c-106">S_OK</span><span class="sxs-lookup"><span data-stu-id="35f6c-106">S_OK</span></span>  
 <span data-ttu-id="35f6c-107">Erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="35f6c-107">Success.</span></span>  
  
 <span data-ttu-id="35f6c-108">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="35f6c-108">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="35f6c-109">Die Funktion konnte keinen Arbeitsspeicher für einen Transport-Manager zuweisen.</span><span class="sxs-lookup"><span data-stu-id="35f6c-109">The function was unable to allocate memory for a transport manager.</span></span>  
  
 <span data-ttu-id="35f6c-110">E_FAIL (oder andere E_-Rückgabecodes)</span><span class="sxs-lookup"><span data-stu-id="35f6c-110">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="35f6c-111">Andere Fehler.</span><span class="sxs-lookup"><span data-stu-id="35f6c-111">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35f6c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35f6c-112">Requirements</span></span>  
 <span data-ttu-id="35f6c-113">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35f6c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35f6c-114">**Header:** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="35f6c-114">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="35f6c-115">**Bibliothek:** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="35f6c-115">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="35f6c-116">**.NET Framework-Versionen:** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="35f6c-116">**.NET Framework Versions:** 3.5 SP1</span></span>
