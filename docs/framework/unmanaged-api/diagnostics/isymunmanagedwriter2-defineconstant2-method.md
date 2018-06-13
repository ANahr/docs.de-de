---
title: ISymUnmanagedWriter2::DefineConstant2-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineConstant2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineConstant2
helpviewer_keywords:
- DefineConstant2 method [.NET Framework debugging]
- ISymUnmanagedWriter2::DefineConstant2 method [.NET Framework debugging]
ms.assetid: dd2bc956-7dbe-49fc-a646-daa0d267f2df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c6f9f198fc1115aed7b531515ab07ddc35d36ba8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427335"
---
# <a name="isymunmanagedwriter2defineconstant2-method"></a><span data-ttu-id="36c42-102">ISymUnmanagedWriter2::DefineConstant2-Methode</span><span class="sxs-lookup"><span data-stu-id="36c42-102">ISymUnmanagedWriter2::DefineConstant2 Method</span></span>
<span data-ttu-id="36c42-103">Definiert einen Namen für einen konstanten Wert.</span><span class="sxs-lookup"><span data-stu-id="36c42-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36c42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36c42-104">Syntax</span></span>  
  
```  
HRESULT DefineConstant2(  
    [in] const WCHAR  *name,  
    [in] VARIANT      value,  
    [in] mdSignature  sigToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="36c42-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="36c42-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="36c42-106">[in] Den Namen der Konstante.</span><span class="sxs-lookup"><span data-stu-id="36c42-106">[in] The constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="36c42-107">[in] Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="36c42-107">[in] The value of the constant.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="36c42-108">[in] Das Metadatentoken der Konstante.</span><span class="sxs-lookup"><span data-stu-id="36c42-108">[in] The metadata token of the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="36c42-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36c42-109">Return Value</span></span>  
 <span data-ttu-id="36c42-110">S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="36c42-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36c42-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36c42-111">Requirements</span></span>  
 <span data-ttu-id="36c42-112">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="36c42-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36c42-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36c42-113">See Also</span></span>  
 [<span data-ttu-id="36c42-114">ISymUnmanagedWriter2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="36c42-114">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 [<span data-ttu-id="36c42-115">DefineConstant-Methode</span><span class="sxs-lookup"><span data-stu-id="36c42-115">DefineConstant Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineconstant-method.md)
