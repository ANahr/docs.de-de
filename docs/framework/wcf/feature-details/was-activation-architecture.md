---
title: WAS-Aktivierungsarchitektur
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 58aeffb0-8f3f-4b40-80c8-15f3f1652fd3
caps.latest.revision: "16"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 3ecd0ab8e285ff8c05ad8b39f68e5b2d0a3c7886
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="was-activation-architecture"></a><span data-ttu-id="c2834-102">WAS-Aktivierungsarchitektur</span><span class="sxs-lookup"><span data-stu-id="c2834-102">WAS Activation Architecture</span></span>
<span data-ttu-id="c2834-103">In diesem Thema werden die einzelnen Komponenten des Windows-Prozessaktivierungsdiensts (auch WAS genannt) aufgeführt und erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2834-103">This topic itemizes and discusses the components of the Windows Process Activation Service (also known as WAS).</span></span>  
  
## <a name="activation-components"></a><span data-ttu-id="c2834-104">Aktivierungskomponenten</span><span class="sxs-lookup"><span data-stu-id="c2834-104">Activation Components</span></span>  
 <span data-ttu-id="c2834-105">WAS umfasst mehrere Architekturkomponenten:</span><span class="sxs-lookup"><span data-stu-id="c2834-105">WAS consists of several architectural components:</span></span>  
  
-   <span data-ttu-id="c2834-106">Listeneradapter.</span><span class="sxs-lookup"><span data-stu-id="c2834-106">Listener adapters.</span></span> <span data-ttu-id="c2834-107">Windows-Dienste, die Nachrichten über bestimmte Netzwerkprotokolle empfangen und mit WAS kommunizieren, leiten eingehende Nachrichten an den richtigen Arbeitsprozess weiter.</span><span class="sxs-lookup"><span data-stu-id="c2834-107">Windows services that receive messages on specific network protocols and communicate with WAS to route incoming messages to the correct worker process.</span></span>  
  
-   <span data-ttu-id="c2834-108">WAS.</span><span class="sxs-lookup"><span data-stu-id="c2834-108">WAS.</span></span> <span data-ttu-id="c2834-109">Der Windows-Dienst, der die Erstellung und die Lebensdauer von Arbeitsprozessen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c2834-109">The Windows service that manages the creation and lifetime of worker processes.</span></span>  
  
-   <span data-ttu-id="c2834-110">Die ausführbare Datei für generische Arbeitsprozesse (w3wp.exe).</span><span class="sxs-lookup"><span data-stu-id="c2834-110">The generic worker process executable (w3wp.exe).</span></span>  
  
-   <span data-ttu-id="c2834-111">Anwendungs-Manager</span><span class="sxs-lookup"><span data-stu-id="c2834-111">Application manager.</span></span> <span data-ttu-id="c2834-112">Verwaltet die Erstellung und die Lebensdauer der Anwendungsdomänen, die innerhalb des Arbeitsprozesses als Host von Anwendungen fungieren.</span><span class="sxs-lookup"><span data-stu-id="c2834-112">Manages the creation and lifetime of application domains that host applications within the worker process.</span></span>  
  
-   <span data-ttu-id="c2834-113">Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="c2834-113">Protocol handlers.</span></span> <span data-ttu-id="c2834-114">Protokollspezifische Komponenten, die im Arbeitsprozess ausgeführt werden und die Kommunikation zwischen Arbeitsprozess und den einzelnen Listeneradaptern verwalten.</span><span class="sxs-lookup"><span data-stu-id="c2834-114">Protocol-specific components that run in the worker process and manage communication between the worker process and the individual listener adapters.</span></span> <span data-ttu-id="c2834-115">Es sind zwei Typen von Protokollhandlern verfügbar: Prozessprotokollhandler und AppDomain-Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="c2834-115">Two types of protocol handlers exist: process protocol handlers and AppDomain protocol handlers.</span></span>  
  
 <span data-ttu-id="c2834-116">Wenn WAS eine Arbeitsprozessinstanz aktiviert, werden die erforderlichen Prozessprotokollhandler in den Arbeitsprozess geladen, und mit dem Anwendungs-Manager wird eine Anwendungsdomäne erstellt, in der die Anwendung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c2834-116">When WAS activates a worker process instance, it loads the process protocol handlers required into the worker process and uses the application manager to create an application domain to host the application.</span></span> <span data-ttu-id="c2834-117">Die Anwendungsdomäne lädt sowohl den Anwendungscode als auch die AppDomain-Protokollhandler, die für die von der Anwendung verwendeten Netzwerkprotokolle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2834-117">The application domain loads the application’s code as well as the AppDomain protocol handlers that the network protocols used by the application require.</span></span>  
  
 <span data-ttu-id="c2834-118">![WAS-Architektur](../../../../docs/framework/wcf/feature-details/media/wasarchitecture.gif "WASArchitecture")</span><span class="sxs-lookup"><span data-stu-id="c2834-118">![WAS Architecture](../../../../docs/framework/wcf/feature-details/media/wasarchitecture.gif "WASArchitecture")</span></span>  
  
### <a name="listener-adapters"></a><span data-ttu-id="c2834-119">Listeneradapter</span><span class="sxs-lookup"><span data-stu-id="c2834-119">Listener Adapters</span></span>  
 <span data-ttu-id="c2834-120">Listeneradapter sind einzelne Windows-Dienste, welche für die Netzwerkprotokolle, bei denen sie lauschen, die Netzwerkprotokolllogik zum Empfang von Nachrichten implementieren.</span><span class="sxs-lookup"><span data-stu-id="c2834-120">Listener adapters are individual Windows services that implement the network communication logic used to receive messages using the network protocol on which they listen.</span></span> <span data-ttu-id="c2834-121">In der folgenden Tabelle sind die Listeneradapter für [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2834-121">The following table lists the listener adapters for [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] protocols.</span></span>  
  
|<span data-ttu-id="c2834-122">Dienstname des Listeneradapters</span><span class="sxs-lookup"><span data-stu-id="c2834-122">Listener adapter service name</span></span>|<span data-ttu-id="c2834-123">Protokoll</span><span class="sxs-lookup"><span data-stu-id="c2834-123">Protocol</span></span>|<span data-ttu-id="c2834-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2834-124">Notes</span></span>|  
|-----------------------------------|--------------|-----------|  
|<span data-ttu-id="c2834-125">W3SVC</span><span class="sxs-lookup"><span data-stu-id="c2834-125">W3SVC</span></span>|<span data-ttu-id="c2834-126">http</span><span class="sxs-lookup"><span data-stu-id="c2834-126">http</span></span>|<span data-ttu-id="c2834-127">Allgemeine Komponente, die sowohl für IIS&#160;7.0 als auch für [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] die HTTP-Aktivierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c2834-127">Common component that provides HTTP activation for both IIS 7.0 and [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].</span></span>|  
|<span data-ttu-id="c2834-128">NetTcpActivator</span><span class="sxs-lookup"><span data-stu-id="c2834-128">NetTcpActivator</span></span>|<span data-ttu-id="c2834-129">net.tcp</span><span class="sxs-lookup"><span data-stu-id="c2834-129">net.tcp</span></span>|<span data-ttu-id="c2834-130">Hängt vom NetTcpPortSharing-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="c2834-130">Depends on the NetTcpPortSharing service.</span></span>|  
|<span data-ttu-id="c2834-131">NetPipeActivator</span><span class="sxs-lookup"><span data-stu-id="c2834-131">NetPipeActivator</span></span>|<span data-ttu-id="c2834-132">net.pipe</span><span class="sxs-lookup"><span data-stu-id="c2834-132">net.pipe</span></span>||  
|<span data-ttu-id="c2834-133">NetMsmqActivator</span><span class="sxs-lookup"><span data-stu-id="c2834-133">NetMsmqActivator</span></span>|<span data-ttu-id="c2834-134">net.msmq</span><span class="sxs-lookup"><span data-stu-id="c2834-134">net.msmq</span></span>|<span data-ttu-id="c2834-135">Für die Verwendung mit [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]-basierten Message Queuing-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c2834-135">For use with [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]-based Message Queuing applications.</span></span>|  
|<span data-ttu-id="c2834-136">NetMsmqActivator</span><span class="sxs-lookup"><span data-stu-id="c2834-136">NetMsmqActivator</span></span>|<span data-ttu-id="c2834-137">msmq.formatname</span><span class="sxs-lookup"><span data-stu-id="c2834-137">msmq.formatname</span></span>|<span data-ttu-id="c2834-138">Stellt Abwärtskompatibilität mit vorhandenen Message Queuing-Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="c2834-138">Provides backwards compatibility with existing Message Queuing applications.</span></span>|  
  
 <span data-ttu-id="c2834-139">Listeneradapter für bestimmte Protokolle werden während der Installation in der Datei applicationHost.config registriert. Dies wird im folgenden XML-Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c2834-139">Listener adapters for specific protocols are registered during installation in the applicationHost.config file, as shown in the following XML example.</span></span>  
  
```xml  
<system.applicationHost>  
    <listenerAdapters>  
        <add name="http" />  
        <add name="net.tcp"   
          identity="S-1-5-80-3579033775-2824656752-1522793541-1960352512-462907086" />  
         <add name="net.pipe"   
           identity="S-1-5-80-2943419899-937267781-4189664001-1229628381-3982115073" />  
          <add name="net.msmq"   
            identity="S-1-5-80-89244771-1762554971-1007993102-348796144-2203111529" />  
           <add name="msmq.formatname"   
             identity="S-1-5-80-89244771-1762554971-1007993102-348796144-2203111529" />  
    </listenerAdapters>  
</system.applicationHost>  
```  
  
### <a name="protocol-handlers"></a><span data-ttu-id="c2834-140">Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="c2834-140">Protocol Handlers</span></span>  
 <span data-ttu-id="c2834-141">Prozess- und AppDomain-Protokollhandler für bestimmte Protokolle werden in der Datei Web.config auf Computerebene registriert.</span><span class="sxs-lookup"><span data-stu-id="c2834-141">Process and AppDomain protocol handlers for specific protocols are registered in the machine-level Web.config file.</span></span>  
  
```xml  
<system.web>  
   <protocols>  
      <add name="net.tcp"   
        processHandlerType=  
         "System.ServiceModel.WasHosting.TcpProcessProtocolHandler"  
        appDomainHandlerType=  
         "System.ServiceModel.WasHosting.TcpAppDomainProtocolHandler"  
        validate="false" />  
      <add name="net.pipe"   
        processHandlerType=  
         "System.ServiceModel.WasHosting.NamedPipeProcessProtocolHandler"  
          appDomainHandlerType=  
           "System.ServiceModel.WasHosting.NamedPipeAppDomainProtocolHandler"/>  
      <add name="net.msmq"  
        processHandlerType=  
         "System.ServiceModel.WasHosting.MsmqProcessProtocolHandler"  
        appDomainHandlerType=  
         "System.ServiceModel.WasHosting.MsmqAppDomainProtocolHandler"  
        validate="false" />  
   </protocols>  
</system.web>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c2834-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2834-142">See Also</span></span>  
 [<span data-ttu-id="c2834-143">Konfigurieren von WAS zur Verwendung mit WCF</span><span class="sxs-lookup"><span data-stu-id="c2834-143">Configuring WAS for Use with WCF</span></span>](../../../../docs/framework/wcf/feature-details/configuring-the-wpa--service-for-use-with-wcf.md)  
 [<span data-ttu-id="c2834-144">Windows Server AppFabric-Hostingfunktionen</span><span class="sxs-lookup"><span data-stu-id="c2834-144">Windows Server App Fabric Hosting Features</span></span>](http://go.microsoft.com/fwlink/?LinkId=201276)
