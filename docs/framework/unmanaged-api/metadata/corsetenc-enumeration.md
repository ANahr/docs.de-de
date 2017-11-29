---
title: CorSetENC-Enumeration
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorSetENC
api_location: mscoree.dll
api_type: COM
f1_keywords: CorSetENC
helpviewer_keywords: CorSetENC enumeration [.NET Framework metadata]
ms.assetid: fe4150e8-071d-43fb-8e06-c3c616dbeed2
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 85a909d92be8bfdb9ada709b54cf252183ff411e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="corsetenc-enumeration"></a><span data-ttu-id="d9718-102">CorSetENC-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d9718-102">CorSetENC Enumeration</span></span>
<span data-ttu-id="d9718-103">Enthält Werte, mit denen das Verhalten während der Generierung von Metadaten beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="d9718-103">Contains values used to influence behavior during the generation of metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9718-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9718-104">Syntax</span></span>  
  
```  
typedef enum CorSetENC {  
  
    MDSetENCOn                  = 0x00000001,  
    MDSetENCOff                 = 0x00000002,  
  
    MDUpdateENC                 = 0x00000001,  
    MDUpdateFull                = 0x00000002,  
    MDUpdateExtension           = 0x00000003,  
    MDUpdateIncremental         = 0x00000004,  
    MDUpdateDelta               = 0x00000005,  
    MDUpdateMask                = 0x00000007  
  
} CorSetENC;  
```  
  
## <a name="members"></a><span data-ttu-id="d9718-105">Member</span><span class="sxs-lookup"><span data-stu-id="d9718-105">Members</span></span>  
  
|<span data-ttu-id="d9718-106">Member</span><span class="sxs-lookup"><span data-stu-id="d9718-106">Member</span></span>|<span data-ttu-id="d9718-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9718-107">Description</span></span>|  
|------------|-----------------|  
|`MDSetENCOn`|<span data-ttu-id="d9718-108">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d9718-108">Obsolete.</span></span>|  
|`MDSetENCOff`|<span data-ttu-id="d9718-109">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d9718-109">Obsolete.</span></span>|  
|`MDUpdateENC`|<span data-ttu-id="d9718-110">Gibt an, dass Metadaten aktualisiert werden kann, Token verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="d9718-110">Indicates that whereas metadata can be updated, tokens cannot be moved.</span></span>|  
|`MDUpdateFull`|<span data-ttu-id="d9718-111">Gibt an, dass Token während eines Updates verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="d9718-111">Indicates that tokens can be moved during updates.</span></span>|  
|`MDUpdateExtension`|<span data-ttu-id="d9718-112">Gibt an, dass die Updates nur von Ergänzungen bestehen können.</span><span class="sxs-lookup"><span data-stu-id="d9718-112">Indicates that updates can consist only of additions.</span></span> <span data-ttu-id="d9718-113">Token können nicht verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d9718-113">Tokens cannot be moved.</span></span>|  
|`MDUpdateIncremental`|<span data-ttu-id="d9718-114">Gibt an, dass die Kompilierung inkrementell ist.</span><span class="sxs-lookup"><span data-stu-id="d9718-114">Indicates that compilation is incremental.</span></span>|  
|`MDUpdateDelta`|<span data-ttu-id="d9718-115">Gibt an, dass nur geänderte Metadaten gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9718-115">Indicates that only changed metadata should be saved.</span></span>|  
|`MDUpdateMask`|<span data-ttu-id="d9718-116">Enthält `MDUpdateENC`, `MDUpdateFull` und `MDUpdateIncremental`.</span><span class="sxs-lookup"><span data-stu-id="d9718-116">Includes `MDUpdateENC`, `MDUpdateFull` and `MDUpdateIncremental`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d9718-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9718-117">Requirements</span></span>  
 <span data-ttu-id="d9718-118">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d9718-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9718-119">**Header:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d9718-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d9718-120">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9718-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9718-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9718-121">See Also</span></span>  
 [<span data-ttu-id="d9718-122">Metadatenenumerationen</span><span class="sxs-lookup"><span data-stu-id="d9718-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
