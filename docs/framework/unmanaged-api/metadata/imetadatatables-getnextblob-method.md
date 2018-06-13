---
title: IMetaDataTables::GetNextBlob-Methode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextBlob
helpviewer_keywords:
- IMetaDataTables::GetNextBlob method [.NET Framework metadata]
- GetNextBlob method [.NET Framework metadata]
ms.assetid: 017c8ab4-4c09-4754-9935-5b0b49cabecb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: caf7faeea4bcec9b73f3c43f0923d308baebf6d0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447619"
---
# <a name="imetadatatablesgetnextblob-method"></a><span data-ttu-id="8bb9a-102">IMetaDataTables::GetNextBlob-Methode</span><span class="sxs-lookup"><span data-stu-id="8bb9a-102">IMetaDataTables::GetNextBlob Method</span></span>
<span data-ttu-id="8bb9a-103">Ruft den Index des nächsten binary large Object (BLOB) in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="8bb9a-103">Gets the index of the next binary large object (BLOB) in the table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bb9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bb9a-104">Syntax</span></span>  
  
```  
HRESULT GetNextBlob (  
    [in]  ULONG   ixBlob,  
    [out] ULONG   *pNext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8bb9a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bb9a-105">Parameters</span></span>  
 `ixBlob`  
 <span data-ttu-id="8bb9a-106">[in] Der Index von einem BLOB-Spalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8bb9a-106">[in] The index, as returned from a column of BLOBs.</span></span>  
  
 `pNext`  
 <span data-ttu-id="8bb9a-107">[out] Ein Zeiger auf den Index des nächsten BLOB.</span><span class="sxs-lookup"><span data-stu-id="8bb9a-107">[out] A pointer to the index of the next BLOB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bb9a-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bb9a-108">Requirements</span></span>  
 <span data-ttu-id="8bb9a-109">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8bb9a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8bb9a-110">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8bb9a-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8bb9a-111">**Bibliothek:** als Ressource in MsCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="8bb9a-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8bb9a-112">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8bb9a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8bb9a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb9a-113">See Also</span></span>  
 [<span data-ttu-id="8bb9a-114">IMetaDataTables-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8bb9a-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="8bb9a-115">IMetaDataTables2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8bb9a-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
