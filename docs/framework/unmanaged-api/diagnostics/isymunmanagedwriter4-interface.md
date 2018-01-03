---
title: ISymUnmanagedWriter4-Schnittstelle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 4af5e8c0-987d-405e-b934-8b9e70fcae6e
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 5531b491da70cb78de1234e750c2e15390c10ce5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedwriter4-interface"></a><span data-ttu-id="caf43-102">ISymUnmanagedWriter4-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="caf43-102">ISymUnmanagedWriter4 Interface</span></span>
<span data-ttu-id="caf43-103">ISymUnmanagedWriter4-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="caf43-103">ISymUnmanagedWriter4 interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="caf43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="caf43-104">Syntax</span></span>  
  
```idl  
[object,uuid(BC7E3F53-F458-4C23-9DBD-A189E6E96594),pointer_default(unique)]interface ISymUnmanagedWriter4 : ISymUnmanagedWriter3  
```  
  
## <a name="methods"></a><span data-ttu-id="caf43-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="caf43-105">Methods</span></span>  
 <span data-ttu-id="caf43-106">Diese Schnittstelle enthält die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="caf43-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="caf43-107">Methode</span><span class="sxs-lookup"><span data-stu-id="caf43-107">Method</span></span>|<span data-ttu-id="caf43-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caf43-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="caf43-109">GetDebugInfoWithPadding-Methode</span><span class="sxs-lookup"><span data-stu-id="caf43-109">GetDebugInfoWithPadding Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-getdebuginfowithpadding-method.md)|<span data-ttu-id="caf43-110">Funktioniert genauso wie [GetDebugInfo-Methode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) mit dem Unterschied, dass die Pfadzeichenfolge mit Nullen nach dem das abschließende Nullzeichen, den Zeichenfolgendaten eine feste Größe von Stellen aufgefüllt wird `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="caf43-110">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="caf43-111">Auffüllung wird nur ausgegeben, wenn die Zeichenfolge Pfadlänge selbst ist kleiner als `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="caf43-111">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span><br /><br /> <span data-ttu-id="caf43-112">Dies erleichtert es, Tools, Unterschied PE-Dateien zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="caf43-112">This makes it easier to write tools that difference PE files.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="caf43-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caf43-113">Requirements</span></span>  
 <span data-ttu-id="caf43-114">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="caf43-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="caf43-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caf43-115">See Also</span></span>  
 [<span data-ttu-id="caf43-116">Diagnosesymbolspeicher-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="caf43-116">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="caf43-117">ISymUnmanagedWriter3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="caf43-117">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
