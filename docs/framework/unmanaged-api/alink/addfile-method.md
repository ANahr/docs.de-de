---
title: AddFile Methode1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IALink.AddFile
- AddFile
api_location: alink.dll
api_type: COM
f1_keywords: AddFile
helpviewer_keywords: AddFile method
ms.assetid: 9e707abb-f905-4568-9356-12aa21d1b11c
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9463f2c41f56287ebfc4fb55aa8208c37522a57f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="addfile-method1"></a><span data-ttu-id="99401-102">AddFile Methode1</span><span class="sxs-lookup"><span data-stu-id="99401-102">AddFile Method1</span></span>
<span data-ttu-id="99401-103">Dateien hinzugefügt der Assembly.</span><span class="sxs-lookup"><span data-stu-id="99401-103">Adds files to the assembly.</span></span> <span data-ttu-id="99401-104">Kann auch zum Erstellen von ungebundener Modules verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99401-104">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99401-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99401-105">Syntax</span></span>  
  
```  
HRESULT AddFile(  
    mdAssembly      AssemblyID,  
    LPCWSTR         pszFilename,  
    DWORD           dwFlags,  
    IMetaDataEmit*  pEmitter,  
    mdFile*         pFileToken  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99401-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99401-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="99401-107">Eindeutige ID der Assembly, die erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="99401-107">Unique ID of the assembly to be augmented.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="99401-108">Vollständig qualifizierte Name der hinzuzufügenden Datei um.</span><span class="sxs-lookup"><span data-stu-id="99401-108">Fully qualified name of file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="99401-109">COM+-FileDef-flags, z. B. `ffContainsNoMetaData` und `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="99401-109">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="99401-110">`dwFlags`wird zum übergeben [DefineFile-Methode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="99401-110">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="99401-111">[IMetaDataEmit-Schnittstelle](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) Schnittstelle zum Ausgeben von Metadaten verwendet werden, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="99401-111">[IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface to be used to emit metadata, if necessary.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="99401-112">Zeiger auf, wo die eindeutige ID der hinzugefügten Datei gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99401-112">Pointer to where the unique ID of the added file will be stored.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99401-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99401-113">Return Value</span></span>  
 <span data-ttu-id="99401-114">Gibt S_OK zurück, wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99401-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99401-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99401-115">Requirements</span></span>  
 <span data-ttu-id="99401-116">Erfordert alink.h.</span><span class="sxs-lookup"><span data-stu-id="99401-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99401-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99401-117">See Also</span></span>  
 [<span data-ttu-id="99401-118">IALink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="99401-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="99401-119">IALink2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="99401-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="99401-120">ALink-API</span><span class="sxs-lookup"><span data-stu-id="99401-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
