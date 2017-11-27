---
title: IMetaDataEmit::DefineEvent-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DefineEvent
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DefineEvent
helpviewer_keywords:
- IMetaDataEmit::DefineEvent method [.NET Framework metadata]
- DefineEvent method [.NET Framework metadata]
ms.assetid: cf064bac-9a9f-41c5-9e1d-108ff7af3afe
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: bf790ce270565abaf1d91e54c9e3569a50ab3435
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitdefineevent-method"></a><span data-ttu-id="1e8ce-102">IMetaDataEmit::DefineEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="1e8ce-102">IMetaDataEmit::DefineEvent Method</span></span>
<span data-ttu-id="1e8ce-103">Erstellt eine Definition für ein Ereignis mit der angegebenen Metadatensignatur und ruft ein Token für die Ereignisdefinition ab.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-103">Creates a definition for an event with the specified metadata signature, and gets a token to that event definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e8ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e8ce-104">Syntax</span></span>  
  
```  
HRESULT DefineEvent (   
    [in]  mdTypeDef    td,   
    [in]  LPCWSTR      szEvent,   
    [in]  DWORD        dwEventFlags,   
    [in]  mdToken      tkEventType,   
    [in]  mdMethodDef  mdAddOn,   
    [in]  mdMethodDef  mdRemoveOn,   
    [in]  mdMethodDef  mdFire,   
    [in]  mdMethodDef  rmdOtherMethods[],   
    [out] mdEvent      *pmdEvent   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1e8ce-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e8ce-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="1e8ce-106">[in] Das Token für die Zielklasse oder Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-106">[in] The token for the target class or interface.</span></span> <span data-ttu-id="1e8ce-107">Dies liegt entweder an einem `mdTypeDef` oder `mdTypeDefNil` token.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-107">This is either a `mdTypeDef` or `mdTypeDefNil` token.</span></span>  
  
 `szEvent`  
 <span data-ttu-id="1e8ce-108">[in] Der Name des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-108">[in] The name of the event.</span></span>  
  
 `dwEventFlags`  
 <span data-ttu-id="1e8ce-109">[in] Ereignisflags.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-109">[in] Event flags.</span></span>  
  
 `tkEventType`  
 <span data-ttu-id="1e8ce-110">[in] Das Token für die Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-110">[in] The token for the event class.</span></span> <span data-ttu-id="1e8ce-111">Dies ist eine `mdTypeDef`, `mdTypeRef`, oder ein `mdTokenNil` token.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-111">This is a `mdTypeDef`, a `mdTypeRef`, or a `mdTokenNil` token.</span></span>  
  
 `mdAddOn`  
 <span data-ttu-id="1e8ce-112">[in] Die Methode, die zum Abonnieren der Ereignis- oder Null.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-112">[in] The method used to subscribe to the event, or null.</span></span>  
  
 `mdRemoveOn`  
 <span data-ttu-id="1e8ce-113">[in] Die Methode verwendet, um das Ereignis bzw. Null Kündigen des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-113">[in] The method used to unsubscribe to the event, or null.</span></span>  
  
 `mdFire`  
 <span data-ttu-id="1e8ce-114">[in] Die Methode, die zum Auslösen des Ereignisses (durch eine abgeleitete Klasse) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-114">[in] The method used (by a derived class) to raise the event.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="1e8ce-115">[in] Ein Array von Token für andere Methoden, die dem Ereignis zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-115">[in] An array of tokens for other methods associated with the event.</span></span> <span data-ttu-id="1e8ce-116">Das Array wird durch beendet eine `mdMethodDefNil` token.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-116">The array is terminated with a `mdMethodDefNil` token.</span></span>  
  
 `pmdEvent`  
 <span data-ttu-id="1e8ce-117">[out] Das Metadatentoken, das dem Ereignis zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-117">[out] The metadata token assigned to the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e8ce-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-118">Requirements</span></span>  
 <span data-ttu-id="1e8ce-119">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1e8ce-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e8ce-120">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1e8ce-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1e8ce-121">**Bibliothek:** als Ressource in MSCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="1e8ce-121">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1e8ce-122">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e8ce-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e8ce-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e8ce-123">See Also</span></span>  
 [<span data-ttu-id="1e8ce-124">IMetaDataEmit-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e8ce-124">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="1e8ce-125">IMetaDataEmit2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e8ce-125">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
