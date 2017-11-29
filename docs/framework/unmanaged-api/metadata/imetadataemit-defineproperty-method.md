---
title: IMetaDataEmit::DefineProperty-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DefineProperty
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: fc0403fd51f028510eb60d93ff96fc7d05606366
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="dec73-102">IMetaDataEmit::DefineProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="dec73-102">IMetaDataEmit::DefineProperty Method</span></span>
<span data-ttu-id="dec73-103">Erstellt eine Eigenschaftsdefinition für den angegebenen Typ mit dem angegebenen `get` und `set` Methodenaccessoren und ruft ein Token auf, Eigenschaftsdefinition ab.</span><span class="sxs-lookup"><span data-stu-id="dec73-103">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dec73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec73-104">Syntax</span></span>  
  
```  
HRESULT DefineProperty (   
    [in]  mdTypeDef          td,   
    [in]  LPCWSTR            szProperty,   
    [in]  DWORD              dwPropFlags,   
    [in]  PCCOR_SIGNATURE    pvSig,   
    [in]  ULONG              cbSig,   
    [in]  DWORD              dwCPlusTypeFlag,   
    [in]  void const         *pValue,   
    [in]  ULONG              cchValue,   
    [in]  mdMethodDef        mdSetter,   
    [in]  mdMethodDef        mdGetter,   
    [in]  mdMethodDef        rmdOtherMethods[],   
    [out] mdProperty         *pmdProp   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dec73-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec73-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="dec73-106">[in] Das Token für die Klasse oder Schnittstelle, die auf dem die Eigenschaft definiert wird.</span><span class="sxs-lookup"><span data-stu-id="dec73-106">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="dec73-107">[in] Der Name der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dec73-107">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="dec73-108">[in] Die Eigenschaftenflags.</span><span class="sxs-lookup"><span data-stu-id="dec73-108">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="dec73-109">[in] Die Signatur der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dec73-109">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="dec73-110">[in] Die Anzahl der Bytes im `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="dec73-110">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="dec73-111">[in] Der Typ des Standardwerts für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dec73-111">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="dec73-112">[in] Der Standardwert für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dec73-112">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="dec73-113">[in] Die Anzahl von (Unicode-) Zeichen `pValue`.</span><span class="sxs-lookup"><span data-stu-id="dec73-113">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="dec73-114">[in] Die Methode, die den Wert der Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="dec73-114">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="dec73-115">[in] Die Methode, die den Eigenschaftswert abruft.</span><span class="sxs-lookup"><span data-stu-id="dec73-115">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="dec73-116">[in] Ein Array von anderen Methoden, die der Eigenschaft zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dec73-116">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="dec73-117">Beenden Sie das Array mit einem `mdTokenNil`.</span><span class="sxs-lookup"><span data-stu-id="dec73-117">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="dec73-118">[out] Die `mdProperty` Token zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="dec73-118">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dec73-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dec73-119">Requirements</span></span>  
 <span data-ttu-id="dec73-120">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dec73-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dec73-121">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="dec73-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dec73-122">**Bibliothek:** als Ressource in MSCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="dec73-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dec73-123">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dec73-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dec73-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dec73-124">See Also</span></span>  
 [<span data-ttu-id="dec73-125">IMetaDataEmit-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dec73-125">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="dec73-126">IMetaDataEmit2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dec73-126">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
