---
title: ISymUnmanagedSymbolSearchInfo::GetSearchPath-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedSymbolSearchInfo.GetSearchPath
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedSymbolSearchInfo::GetSearchPath
helpviewer_keywords:
- GetSearchPath method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPath method [.NET Framework debugging]
ms.assetid: b588d470-53c2-4492-be8c-957323eaca0b
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c896c8bc8aa852fb69f182e484243a0c379e0a1e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpath-method"></a><span data-ttu-id="28b24-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath-Methode</span><span class="sxs-lookup"><span data-stu-id="28b24-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath Method</span></span>
<span data-ttu-id="28b24-103">Ruft den Suchpfad ab.</span><span class="sxs-lookup"><span data-stu-id="28b24-103">Gets the search path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28b24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b24-104">Syntax</span></span>  
  
```  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="28b24-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="28b24-105">Parameters</span></span>  
 `pcchPath`  
 <span data-ttu-id="28b24-106">[out] Ein Zeiger auf eine `ULONG32` , empfängt die Größe Puffers in Zeichen, die benötigt, um den Suchpfad aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="28b24-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="28b24-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28b24-107">Return Value</span></span>  
 <span data-ttu-id="28b24-108">S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="28b24-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28b24-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28b24-109">Requirements</span></span>  
 <span data-ttu-id="28b24-110">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="28b24-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28b24-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28b24-111">See Also</span></span>  
 [<span data-ttu-id="28b24-112">ISymUnmanagedSymbolSearchInfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="28b24-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
