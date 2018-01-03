---
title: EndMerge-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IALink.EndMerge
- EndMerge
api_location: alink.dll
api_type: COM
f1_keywords: EndMerge
helpviewer_keywords: EndMerge method
ms.assetid: 1d03bb15-a2c8-4a04-8fc6-b126c89c3778
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 58e9cecae43fb69f1ce2e90eb9d6551d287ca7b3
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="endmerge-method"></a><span data-ttu-id="5a897-102">EndMerge-Methode</span><span class="sxs-lookup"><span data-stu-id="5a897-102">EndMerge Method</span></span>
<span data-ttu-id="5a897-103">Gibt an, dass alle benutzerdefinierten Attribute in den Bereich Emit zusammengeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a897-103">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a897-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a897-104">Syntax</span></span>  
  
```  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5a897-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a897-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="5a897-106">Die ID der Assembly.</span><span class="sxs-lookup"><span data-stu-id="5a897-106">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5a897-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a897-107">Return Value</span></span>  
 <span data-ttu-id="5a897-108">Gibt S_OK zurück, wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a897-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5a897-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a897-109">Requirements</span></span>  
 <span data-ttu-id="5a897-110">Erfordert alink.h</span><span class="sxs-lookup"><span data-stu-id="5a897-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a897-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a897-111">See Also</span></span>  
 [<span data-ttu-id="5a897-112">IALink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a897-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="5a897-113">IALink2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a897-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="5a897-114">Alink-API</span><span class="sxs-lookup"><span data-stu-id="5a897-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
