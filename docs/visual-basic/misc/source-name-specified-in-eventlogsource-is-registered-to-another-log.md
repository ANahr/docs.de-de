---
title: "Der in \"EventLogSource\" angegebene Quellenname ist für ein anderes als in \"EventLogName\" angegebenes Protokoll registriert"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: 7317e100-098b-408d-86e5-7c74cf8558c7
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: c190caa7634760c2e4dc4a2bb7a9a09f532eb0ed
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="source-name-specified-in-eventlogsource-is-registered-to-a-log-other-than-that-specified-in-eventlogname"></a><span data-ttu-id="20931-102">Der in "EventLogSource" angegebene Quellenname ist für ein anderes als in "EventLogName" angegebenes Protokoll registriert</span><span class="sxs-lookup"><span data-stu-id="20931-102">Source name specified in EventLogSource is registered to a log other than that specified in EventLogName</span></span>
<span data-ttu-id="20931-103">`EventLog` versucht, auf eine Quelle zu verweisen, die für ein anderes Protokoll registriert ist.</span><span class="sxs-lookup"><span data-stu-id="20931-103">The `EventLog` is attempting to refer to a source that is registered to a different log.</span></span> <span data-ttu-id="20931-104">Wenn Sie Einträge in ein Ereignisprotokoll schreiben, müssen Sie die <xref:System.Diagnostics.EventLog.Source%2A> -Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="20931-104">If you are writing entries to an event log, you must specify the <xref:System.Diagnostics.EventLog.Source%2A> property.</span></span> <span data-ttu-id="20931-105">Die <xref:System.Diagnostics.EventLog.Source%2A> -Eigenschaft registriert die Komponente beim Ereignisprotokoll als gültige Quelle für Einträge.</span><span class="sxs-lookup"><span data-stu-id="20931-105">The <xref:System.Diagnostics.EventLog.Source%2A> property registers your component with the event log as a valid source of entries.</span></span> <span data-ttu-id="20931-106">Eine einzelne Quelle kann nur jeweils einem Ereignisprotokoll zugeordnet werden (und somit Einträge jeweils in nur ein Ereignisprotokoll schreiben).</span><span class="sxs-lookup"><span data-stu-id="20931-106">A single source can be associated with (and therefore write entries to) only one event log at a time.</span></span>  
  
 <span data-ttu-id="20931-107">Wenn Sie den Versuch unternehmen, einen Eintrag zu schreiben, ohne zuerst die Komponente als gültige Quelle zu registrieren, registriert das System standardmäßig die Quelle automatisch beim Ereignisprotokoll. Dazu wird der Wert der <xref:System.Diagnostics.EventLog.Source%2A> -Eigenschaft als Quellzeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="20931-107">By default, if you try to write an entry without first having registered your component as a valid source, the system automatically registers the source with the event log, using the value of the <xref:System.Diagnostics.EventLog.Source%2A> property as the source string.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="20931-108">So beheben Sie diesen Fehler</span><span class="sxs-lookup"><span data-stu-id="20931-108">To correct this error</span></span>  
  
-   <span data-ttu-id="20931-109">Stellen Sie sicher, dass die Quelle beim richtigen Protokoll registriert ist.</span><span class="sxs-lookup"><span data-stu-id="20931-109">Make sure the source is registered to the correct log.</span></span> <span data-ttu-id="20931-110">Verwenden Sie dazu die <xref:System.Diagnostics.EventLog.CreateEventSource%2A> -Methode oder eine ihrer Überladungen, um eine Zeichenfolge anzugeben, die die Komponente beim Ereignisprotokoll eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="20931-110">To do this, use the <xref:System.Diagnostics.EventLog.CreateEventSource%2A> method or one of its overloads to specify a string that uniquely identifies your component to the event log.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20931-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20931-111">See Also</span></span>  
 [<span data-ttu-id="20931-112">Verwalten von Ereignisprotokollen</span><span class="sxs-lookup"><span data-stu-id="20931-112">Administering Event Logs</span></span>](http://msdn.microsoft.com/en-us/35f53238-bdd2-417b-acd8-2fd9f7397f18)  
 [<span data-ttu-id="20931-113">-Ereignisprotokollverweise</span><span class="sxs-lookup"><span data-stu-id="20931-113">Event Log References</span></span>](http://msdn.microsoft.com/en-us/4af0661c-6c96-49f4-961d-b26ed9bc3e87)  
 [<span data-ttu-id="20931-114">Vorgehensweise: Hinzufügen von Ihrer Anwendung als Quelle für Einträge im Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="20931-114">How to: Add Your Application as a Source of Event Log Entries</span></span>](http://msdn.microsoft.com/en-us/948ff920-a739-4e66-a191-ee951512d42c)  
 [<span data-ttu-id="20931-115">Vorgehensweise: entfernen eine Ereignisquelle</span><span class="sxs-lookup"><span data-stu-id="20931-115">How to: Remove an Event Source</span></span>](http://msdn.microsoft.com/en-us/bc66c900-4b8a-426a-b8e2-17031a20167e)
