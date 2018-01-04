---
title: ActivityTransfer
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 7f3db50a32fabc117c79eef5ac086a7798f86ed3
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="activitytransfer"></a><span data-ttu-id="32236-102">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="32236-102">ActivityTransfer</span></span>
<span data-ttu-id="32236-103">Aktivitätsübertragungsereignis</span><span class="sxs-lookup"><span data-stu-id="32236-103">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32236-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32236-104">Syntax</span></span>  
  
```  
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="32236-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="32236-105">Methods</span></span>  
 <span data-ttu-id="32236-106">Von der ActivityTransfer-Klasse werden keine Methoden definiert.</span><span class="sxs-lookup"><span data-stu-id="32236-106">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="32236-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32236-107">Properties</span></span>  
 <span data-ttu-id="32236-108">Die ActivityTransfer-Klasse besitzt folgende Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="32236-108">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="32236-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="32236-109">ActivityID</span></span>  
  
-   <span data-ttu-id="32236-110">Datentyp: object</span><span class="sxs-lookup"><span data-stu-id="32236-110">Data type: object</span></span>  
    <span data-ttu-id="32236-111">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32236-111">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="32236-112">Aktivitäts-ID</span><span class="sxs-lookup"><span data-stu-id="32236-112">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="32236-113">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="32236-113">RelatedActivityID</span></span>  
  
-   <span data-ttu-id="32236-114">Datentyp: object</span><span class="sxs-lookup"><span data-stu-id="32236-114">Data type: object</span></span>  
    <span data-ttu-id="32236-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="32236-115">Access type: Read-only</span></span>  
  
-   <span data-ttu-id="32236-116">Verwandte Aktivitäts-ID</span><span class="sxs-lookup"><span data-stu-id="32236-116">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32236-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32236-117">Requirements</span></span>  
  
|<span data-ttu-id="32236-118">MOF</span><span class="sxs-lookup"><span data-stu-id="32236-118">MOF</span></span>|<span data-ttu-id="32236-119">Deklariert in Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="32236-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="32236-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="32236-120">Namespace</span></span>|<span data-ttu-id="32236-121">Definiert in root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="32236-121">Defined in root\ServiceModel.</span></span>|
