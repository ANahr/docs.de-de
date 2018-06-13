---
title: IMetaDataTables::GetNextString-Methode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextString
helpviewer_keywords:
- IMetaDataTables::GetNextString method [.NET Framework metadata]
- GetNextString method [.NET Framework metadata]
ms.assetid: d9720428-c353-4f07-a7e8-899e106a1b37
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eea43e5eaa037a3b70f482b0602d8d8d3d594f75
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449848"
---
# <a name="imetadatatablesgetnextstring-method"></a><span data-ttu-id="099cc-102">IMetaDataTables::GetNextString-Methode</span><span class="sxs-lookup"><span data-stu-id="099cc-102">IMetaDataTables::GetNextString Method</span></span>
<span data-ttu-id="099cc-103">Ruft den Index der nächsten Zeichenfolge in der aktuellen Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="099cc-103">Gets the index of the next string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="099cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="099cc-104">Syntax</span></span>  
  
```  
HRESULT GetNextString (   
    [in]  ULONG   ixString,  
    [out] ULONG   *pNext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="099cc-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="099cc-105">Parameters</span></span>  
 `ixString`  
 <span data-ttu-id="099cc-106">[in] Der Indexwert aus einer Zeichenfolge Tabellenspalte.</span><span class="sxs-lookup"><span data-stu-id="099cc-106">[in] The index value from a string table column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="099cc-107">[out] Ein Zeiger auf den Index des nächsten Zeichenfolge in der Spalte.</span><span class="sxs-lookup"><span data-stu-id="099cc-107">[out] A pointer to the index of the next string in the column.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="099cc-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="099cc-108">Requirements</span></span>  
 <span data-ttu-id="099cc-109">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="099cc-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="099cc-110">**Header:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="099cc-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="099cc-111">**Bibliothek:** als Ressource in MsCorEE.dll verwendet</span><span class="sxs-lookup"><span data-stu-id="099cc-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="099cc-112">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="099cc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="099cc-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="099cc-113">See Also</span></span>  
 [<span data-ttu-id="099cc-114">IMetaDataTables-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="099cc-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="099cc-115">IMetaDataTables2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="099cc-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
