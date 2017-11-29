---
title: 4203 - RenewLockSystemError
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 06d4695eb125475f41a94c7f2266df6d2c3f400d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2017
---
# <a name="4203---renewlocksystemerror"></a><span data-ttu-id="95701-102">4203 - RenewLockSystemError</span><span class="sxs-lookup"><span data-stu-id="95701-102">4203 - RenewLockSystemError</span></span>
## <a name="properties"></a><span data-ttu-id="95701-103">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95701-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="95701-104">ID</span><span class="sxs-lookup"><span data-stu-id="95701-104">ID</span></span>|<span data-ttu-id="95701-105">4203</span><span class="sxs-lookup"><span data-stu-id="95701-105">4203</span></span>|  
|<span data-ttu-id="95701-106">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95701-106">Keywords</span></span>|<span data-ttu-id="95701-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="95701-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="95701-108">Ebene</span><span class="sxs-lookup"><span data-stu-id="95701-108">Level</span></span>|<span data-ttu-id="95701-109">Fehler</span><span class="sxs-lookup"><span data-stu-id="95701-109">Error</span></span>|  
|<span data-ttu-id="95701-110">Kanal</span><span class="sxs-lookup"><span data-stu-id="95701-110">Channel</span></span>|<span data-ttu-id="95701-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="95701-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="95701-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95701-112">Description</span></span>  
 <span data-ttu-id="95701-113">Gibt an, dass der SQL-Anbieter die Sperre nicht verlängern konnte, da die Gültigkeit der Sperre bereits abgelaufen war oder der Sperrenbesitzer gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="95701-113">Indicates SQL provider has failed to extend lock expiration due to either lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="95701-114">Das SqlWorkflowInstanceStore wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95701-114">The SqlWorkflowInstanceStore will be aborted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="95701-115">Meldung</span><span class="sxs-lookup"><span data-stu-id="95701-115">Message</span></span>  
 <span data-ttu-id="95701-116">Die Gültigkeit der Sperre konnte nicht verlängert werden. Die Sperre ist abgelaufen, oder der Besitzer wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="95701-116">Failed to extend lock expiration, lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="95701-117">SqlWorkflowInstanceStore wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95701-117">Aborting SqlWorkflowInstanceStore.</span></span>  
  
## <a name="details"></a><span data-ttu-id="95701-118">Details</span><span class="sxs-lookup"><span data-stu-id="95701-118">Details</span></span>  
  
|<span data-ttu-id="95701-119">Datenelementname</span><span class="sxs-lookup"><span data-stu-id="95701-119">Data Item Name</span></span>|<span data-ttu-id="95701-120">Datenelementtyp</span><span class="sxs-lookup"><span data-stu-id="95701-120">Data Item Type</span></span>|<span data-ttu-id="95701-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95701-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="95701-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="95701-122">AppDomain</span></span>|<span data-ttu-id="95701-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="95701-123">xs:string</span></span>|<span data-ttu-id="95701-124">Die von AppDomain.CurrentDomain.FriendlyName zurückgegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="95701-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
