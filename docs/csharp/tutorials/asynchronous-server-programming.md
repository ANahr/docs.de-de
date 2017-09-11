---
title: "Asynchrone Serverprogrammierung – Leitfaden für C#"
description: Lernen Sie Verfahren zur Abladung von Serverworkloads mithilfe der asynchronen Programmierung kennen.
keywords: C#, asynchron, CPU-gebunden, netzwerkgebunden
ms.date: 08/24/2016
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: 7402b29b-1093-456d-be4c-f60ecb8926bb
redirect_url: /dotnet/csharp/tutorials/index
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 390d0eb2c8416165984ffe6c80ed6977e61a2845
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---

# <a name="-asynchronous-server-programming"></a><span data-ttu-id="4b9b2-104">🔧 Asynchrone Serverprogrammierung</span><span class="sxs-lookup"><span data-stu-id="4b9b2-104">🔧 Asynchronous Server Programming</span></span>

> <span data-ttu-id="4b9b2-105">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="4b9b2-105">**Note**</span></span>
> 
> <span data-ttu-id="4b9b2-106">Zu diesem Thema wurde noch nichts geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b9b2-106">This topic hasn’t been written yet!</span></span> 
>
> <span data-ttu-id="4b9b2-107">Wir freuen uns auf Ihre Ideen zur Gestaltung des Umfangs und der Herangehensweise.</span><span class="sxs-lookup"><span data-stu-id="4b9b2-107">We welcome your input to help shape the scope and approach.</span></span> <span data-ttu-id="4b9b2-108">Sie können den Status nachverfolgen und Informationen zu diesem [Problem](https://github.com/dotnet/docs/issues/952) auf GitHub bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4b9b2-108">You can track the status and provide input on this [issue](https://github.com/dotnet/docs/issues/952) at GitHub.</span></span>
> 
> <span data-ttu-id="4b9b2-109">Wenn Sie früher Entwürfe und Überblicke zu diesem Thema erhalten möchten, geben Sie Ihre Kontaktinformationen bei dem Thema an.</span><span class="sxs-lookup"><span data-stu-id="4b9b2-109">If you would like to review early drafts and outlines of this topic, please leave a note with your contact information in the issue.</span></span>
>
> <span data-ttu-id="4b9b2-110">Erfahren Sie mehr darüber, wie Sie zu alledem beitragen können, indem Sie auf [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) gehen.</span><span class="sxs-lookup"><span data-stu-id="4b9b2-110">Learn more about how you can contribute on [GitHub](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md).</span></span>
>

