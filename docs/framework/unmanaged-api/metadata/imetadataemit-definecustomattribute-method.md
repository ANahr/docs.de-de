---
title: IMetaDataEmit::DefineCustomAttribute-Methode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineCustomAttribute
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineCustomAttribute
helpviewer_keywords:
- DefineCustomAttribute method [.NET Framework metadata]
- IMetaDataEmit::DefineCustomAttribute method [.NET Framework metadata]
ms.assetid: 7dd14854-b756-4401-b167-88ca576dc8f0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a11e9919dc1338c4b67c3c4b0f082e330c29d9eb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445081"
---
# <a name="imetadataemitdefinecustomattribute-method"></a><span data-ttu-id="c51f5-102">IMetaDataEmit::DefineCustomAttribute-Methode</span><span class="sxs-lookup"><span data-stu-id="c51f5-102">IMetaDataEmit::DefineCustomAttribute Method</span></span>
<span data-ttu-id="c51f5-103">Erstellt eine Definition für ein benutzerdefiniertes Attribut mit der angegebenen Metadaten-Signatur, die an das angegebene Objekt angefügt werden, und ruft ein Token für diese Definition des benutzerdefinierten Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="c51f5-103">Creates a definition for a custom attribute with the specified metadata signature, to be attached to the specified object, and gets a token to that custom attribute definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c51f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c51f5-104">Syntax</span></span>  
  
```  
HRESULT DefineCustomAttribute (   
    [in]  mdToken     tkObj,   
    [in]  mdToken     tkType,   
    [in]  void const  *pCustomAttribute,   
    [in]  ULONG       cbCustomAttribute,   
    [out] mdCustomAttribute *pcv   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c51f5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c51f5-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="c51f5-106">[in] Das Token für den Besitzerelement.</span><span class="sxs-lookup"><span data-stu-id="c51f5-106">[in] The token for the owner item.</span></span>  
  
 `tkType`  
 <span data-ttu-id="c51f5-107">[in] Das Token, das benutzerdefinierte Attribut identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c51f5-107">[in] The token that identifies the custom attribute.</span></span>  
  
 `pCustomAttribute`  
 <span data-ttu-id="c51f5-108">[in] Ein Zeiger auf das benutzerdefinierte Attribut.</span><span class="sxs-lookup"><span data-stu-id="c51f5-108">[in] A pointer to the custom attribute.</span></span>  
  
 `cbCustomAttribute`  
 <span data-ttu-id="c51f5-109">[in] Die Anzahl der Bytes im `pCustomAttribute`.</span><span class="sxs-lookup"><span data-stu-id="c51f5-109">[in] The count of bytes in `pCustomAttribute`.</span></span>  
  
 `pcv`  
 <span data-ttu-id="c51f5-110">[out] Die `mdCustomAttribute` Token zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c51f5-110">[out] The `mdCustomAttribute` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c51f5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c51f5-111">Requirements</span></span>  
 <span data-ttu-id="c51f5-112">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c51f5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c51f5-113">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c51f5-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c51f5-114">**Bibliothek:** als Ressource in MSCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="c51f5-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c51f5-115">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c51f5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c51f5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c51f5-116">See Also</span></span>  
 [<span data-ttu-id="c51f5-117">IMetaDataEmit-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c51f5-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="c51f5-118">IMetaDataEmit2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c51f5-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
