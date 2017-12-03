---
title: 1005 - WorkflowApplicationIdled
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 2603621eb23747275e6db22a1743c5260967c6a3
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2017
---
# <a name="1005---workflowapplicationidled"></a><span data-ttu-id="368cf-102">1005 - WorkflowApplicationIdled</span><span class="sxs-lookup"><span data-stu-id="368cf-102">1005 - WorkflowApplicationIdled</span></span>
## <a name="properties"></a><span data-ttu-id="368cf-103">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="368cf-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="368cf-104">ID</span><span class="sxs-lookup"><span data-stu-id="368cf-104">ID</span></span>|<span data-ttu-id="368cf-105">1005</span><span class="sxs-lookup"><span data-stu-id="368cf-105">1005</span></span>|  
|<span data-ttu-id="368cf-106">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="368cf-106">Keywords</span></span>|<span data-ttu-id="368cf-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="368cf-107">WFRuntime</span></span>|  
|<span data-ttu-id="368cf-108">Ebene</span><span class="sxs-lookup"><span data-stu-id="368cf-108">Level</span></span>|<span data-ttu-id="368cf-109">Information</span><span class="sxs-lookup"><span data-stu-id="368cf-109">Information</span></span>|  
|<span data-ttu-id="368cf-110">Kanal</span><span class="sxs-lookup"><span data-stu-id="368cf-110">Channel</span></span>|<span data-ttu-id="368cf-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="368cf-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="368cf-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="368cf-112">Description</span></span>  
 <span data-ttu-id="368cf-113">Gibt an, dass sich eine Workflowanwendung im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="368cf-113">Indicates a workflow application has idled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="368cf-114">Meldung</span><span class="sxs-lookup"><span data-stu-id="368cf-114">Message</span></span>  
 <span data-ttu-id="368cf-115">WorkflowApplication-ID: '%1 ' ist im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="368cf-115">WorkflowApplication Id: '%1' went idle.</span></span>  
  
## <a name="details"></a><span data-ttu-id="368cf-116">Details</span><span class="sxs-lookup"><span data-stu-id="368cf-116">Details</span></span>  
  
|<span data-ttu-id="368cf-117">Datenelementname</span><span class="sxs-lookup"><span data-stu-id="368cf-117">Data Item Name</span></span>|<span data-ttu-id="368cf-118">Datenelementtyp</span><span class="sxs-lookup"><span data-stu-id="368cf-118">Data Item Type</span></span>|<span data-ttu-id="368cf-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="368cf-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="368cf-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="368cf-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="368cf-121">Die Workflowanwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="368cf-121">The workflow application id</span></span>|  
|<span data-ttu-id="368cf-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="368cf-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="368cf-123">Die von AppDomain.CurrentDomain.FriendlyName zurückgegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="368cf-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
