---
title: IMetaDataImport2::EnumGenericParams-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport2.EnumGenericParams
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport2::EnumGenericParams
helpviewer_keywords:
- EnumGenericParams method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParams method [.NET Framework metadata]
ms.assetid: b50488a5-3cf0-483c-82dc-2892a3ec61ac
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0e6a5dc6cd1d82a3ccd46b09e301a84f90a3f429
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimport2enumgenericparams-method"></a><span data-ttu-id="71d68-102">IMetaDataImport2::EnumGenericParams-Methode</span><span class="sxs-lookup"><span data-stu-id="71d68-102">IMetaDataImport2::EnumGenericParams Method</span></span>
<span data-ttu-id="71d68-103">Ruft einen Enumerator für ein Array von generischen Parameter-Token mit dem angegebenen TypeDef- oder MethodDef verknüpften token.</span><span class="sxs-lookup"><span data-stu-id="71d68-103">Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71d68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71d68-104">Syntax</span></span>  
  
```  
HRESULT EnumGenericParams (  
   [in, out] HCORENUM     *phEnum,   
   [in]  mdToken          tk,  
   [out] mdGenericParam   rGenericParams[],   
   [in]  ULONG            cMax,   
   [out] ULONG            *pcGenericParams  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="71d68-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="71d68-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="71d68-106">[in, out] Ein Zeiger auf den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="71d68-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="71d68-107">[in] Die TypeDef oder MethodDef-Token, dessen generischen Parametern werden aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71d68-107">[in] The TypeDef or MethodDef token whose generic parameters are to be enumerated.</span></span>  
  
 `rGenericParams`  
 <span data-ttu-id="71d68-108">[out] Das Array von generischen Parametern aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="71d68-108">[out] The array of generic parameters to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="71d68-109">[in] Die angeforderte maximale Anzahl von Token zu versehen `rGenericParams`.</span><span class="sxs-lookup"><span data-stu-id="71d68-109">[in] The requested maximum number of tokens to place in `rGenericParams`.</span></span>  
  
 `pcGenericParams`  
 <span data-ttu-id="71d68-110">[out] Die zurückgegebene Anzahl von Token in platziert `rGenericParams`.</span><span class="sxs-lookup"><span data-stu-id="71d68-110">[out] The returned number of tokens placed in `rGenericParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="71d68-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71d68-111">Return Value</span></span>  
  
|<span data-ttu-id="71d68-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="71d68-112">HRESULT</span></span>|<span data-ttu-id="71d68-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71d68-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="71d68-114">`EnumGenericParams`wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71d68-114">`EnumGenericParams` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="71d68-115">`phEnum`verfügt über keine Memberelemente.</span><span class="sxs-lookup"><span data-stu-id="71d68-115">`phEnum` has no member elements.</span></span> <span data-ttu-id="71d68-116">In diesem Fall `pcGenericParams` auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="71d68-116">In this case, `pcGenericParams` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="71d68-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71d68-117">Requirements</span></span>  
 <span data-ttu-id="71d68-118">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="71d68-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71d68-119">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="71d68-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="71d68-120">**Bibliothek:** als Ressource in MsCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="71d68-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="71d68-121">**.NET Framework-Versionen:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71d68-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71d68-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71d68-122">See Also</span></span>  
 [<span data-ttu-id="71d68-123">IMetaDataImport2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71d68-123">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [<span data-ttu-id="71d68-124">IMetaDataImport-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="71d68-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
