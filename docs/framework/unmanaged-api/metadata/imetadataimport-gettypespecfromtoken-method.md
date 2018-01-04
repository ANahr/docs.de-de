---
title: IMetaDataImport::GetTypeSpecFromToken-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetTypeSpecFromToken
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetTypeSpecFromToken
helpviewer_keywords:
- GetTypeSpecFromToken method [.NET Framework metadata]
- IMetaDataImport::GetTypeSpecFromToken method [.NET Framework metadata]
ms.assetid: ee518bda-3296-482e-a7b7-e9d51dd1a181
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 10d4d9dcad2494410cc361617d5292c519b6dc00
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataimportgettypespecfromtoken-method"></a><span data-ttu-id="7e755-102">IMetaDataImport::GetTypeSpecFromToken-Methode</span><span class="sxs-lookup"><span data-stu-id="7e755-102">IMetaDataImport::GetTypeSpecFromToken Method</span></span>
<span data-ttu-id="7e755-103">Ruft die binäre Metadatensignatur der Typspezifikation ab, die durch das angegebene Token dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e755-103">Gets the binary metadata signature of the type specification represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e755-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e755-104">Syntax</span></span>  
  
```  
HRESULT GetTypeSpecFromToken (   
   [in]  mdTypeSpec            typespec,   
   [out] PCCOR_SIGNATURE       *ppvSig,   
   [out] ULONG                 *pcbSig  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7e755-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e755-105">Parameters</span></span>  
 `typespec`  
 <span data-ttu-id="7e755-106">[in] Das angeforderte Metadatensignatur zugeordnete TypeSpec-Token.</span><span class="sxs-lookup"><span data-stu-id="7e755-106">[in] The TypeSpec token associated with the requested metadata signature.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="7e755-107">[out] Ein Zeiger auf die binäre Metadatensignatur.</span><span class="sxs-lookup"><span data-stu-id="7e755-107">[out] A pointer to the binary metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="7e755-108">[out] Die Größe der Metadatensignatur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7e755-108">[out] The size, in bytes, of the metadata signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7e755-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e755-109">Return Value</span></span>  
 <span data-ttu-id="7e755-110">Ein HRESULT, das Erfolg oder Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="7e755-110">An HRESULT that indicates success or failure.</span></span> <span data-ttu-id="7e755-111">Fehler können mit dem FAILED-Makro getestet werden.</span><span class="sxs-lookup"><span data-stu-id="7e755-111">Failures can be tested with the FAILED macro.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e755-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e755-112">Requirements</span></span>  
 <span data-ttu-id="7e755-113">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7e755-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e755-114">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7e755-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7e755-115">**Bibliothek:** als Ressource in MsCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="7e755-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7e755-116">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e755-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e755-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e755-117">See Also</span></span>  
 [<span data-ttu-id="7e755-118">IMetaDataImport-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7e755-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="7e755-119">IMetaDataImport2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7e755-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
