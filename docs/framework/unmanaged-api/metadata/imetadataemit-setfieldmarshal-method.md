---
title: IMetaDataEmit::SetFieldMarshal-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.SetFieldMarshal
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::SetFieldMarshal
helpviewer_keywords:
- SetFieldMarshal method [.NET Framework metadata]
- IMetaDataEmit::SetFieldMarshal method [.NET Framework metadata]
ms.assetid: be232314-7f69-4855-bfab-63361bd22307
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3ef1d50d0d74a92a5bcaf23981226e5a6c852edd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitsetfieldmarshal-method"></a><span data-ttu-id="1708e-102">IMetaDataEmit::SetFieldMarshal-Methode</span><span class="sxs-lookup"><span data-stu-id="1708e-102">IMetaDataEmit::SetFieldMarshal Method</span></span>
<span data-ttu-id="1708e-103">Legt die PInvoke Marshallinginformationen für den Parameter Feld,-Methodenrückgabe oder eine Methode, die durch das angegebene Token verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1708e-103">Sets the PInvoke marshaling information for the field, method return, or method parameter referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1708e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1708e-104">Syntax</span></span>  
  
```  
HRESULT SetFieldMarshal (  
    [in]  mdToken          tk,   
    [in]  PCCOR_SIGNATURE  pvNativeType,   
    [in]  ULONG            cbNativeType   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1708e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1708e-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="1708e-106">[in] Das Token für Ziel-Datenelement.</span><span class="sxs-lookup"><span data-stu-id="1708e-106">[in] The token for target data item.</span></span> <span data-ttu-id="1708e-107">Dies liegt entweder an einem `mdFieldDef` oder ein `mdParamDef` token.</span><span class="sxs-lookup"><span data-stu-id="1708e-107">This is either a `mdFieldDef` or a `mdParamDef` token.</span></span>  
  
 `pvNativeType`  
 <span data-ttu-id="1708e-108">[in] Die Signatur für den nicht verwalteten Typ.</span><span class="sxs-lookup"><span data-stu-id="1708e-108">[in] The signature for unmanaged type.</span></span>  
  
 `cbNativeType`  
 <span data-ttu-id="1708e-109">[in] Die Anzahl der Bytes im `pvNativeType`.</span><span class="sxs-lookup"><span data-stu-id="1708e-109">[in] The count of bytes in `pvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1708e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1708e-110">Requirements</span></span>  
 <span data-ttu-id="1708e-111">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1708e-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1708e-112">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1708e-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1708e-113">**Bibliothek:** als Ressource in MSCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="1708e-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1708e-114">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1708e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1708e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1708e-115">See Also</span></span>  
 [<span data-ttu-id="1708e-116">IMetaDataEmit-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1708e-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="1708e-117">IMetaDataEmit2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1708e-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
