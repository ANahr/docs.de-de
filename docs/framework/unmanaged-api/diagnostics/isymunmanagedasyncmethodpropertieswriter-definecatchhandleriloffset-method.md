---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset-Methode
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce462c4e7e9c8fb11ee74a91f3ece2465a44a834
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425430"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a><span data-ttu-id="62f3c-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset-Methode</span><span class="sxs-lookup"><span data-stu-id="62f3c-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Method</span></span>
<span data-ttu-id="62f3c-103">Legt fest, die IL-offset für den vom Compiler generierte Catch-Handler, der eine asynchrone Methode umschließt.</span><span class="sxs-lookup"><span data-stu-id="62f3c-103">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span>  
  
 <span data-ttu-id="62f3c-104">Der IL-Offset des generierten Catch wird vom Debugger verwendet, an um den Catch zu behandeln, als wäre er Nichtbenutzercode, obwohl es in einer Benutzer-Codemethode auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="62f3c-104">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code even though it might occur in a user code method.</span></span> <span data-ttu-id="62f3c-105">Insbesondere, dient er als Antwort auf eine **CatchHandlerFound** Ausnahmeereignisses.</span><span class="sxs-lookup"><span data-stu-id="62f3c-105">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62f3c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62f3c-106">Syntax</span></span>  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="62f3c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="62f3c-107">Parameters</span></span>  
  
|<span data-ttu-id="62f3c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62f3c-108">Parameter</span></span>|<span data-ttu-id="62f3c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62f3c-109">Description</span></span>|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a><span data-ttu-id="62f3c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62f3c-110">Return Value</span></span>  
 <span data-ttu-id="62f3c-111">Gibt `HRESULT`zurück.</span><span class="sxs-lookup"><span data-stu-id="62f3c-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62f3c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62f3c-112">Requirements</span></span>  
 <span data-ttu-id="62f3c-113">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="62f3c-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62f3c-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62f3c-114">See Also</span></span>  
 [<span data-ttu-id="62f3c-115">ISymUnmanagedAsyncMethodPropertiesWriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="62f3c-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
