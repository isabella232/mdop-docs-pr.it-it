---
title: Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server
description: Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815866"
---
# <span data-ttu-id="4360f-103">Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="4360f-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="4360f-104">Se si vuole usare Application Virtualization Streaming Servers in combinazione con l'implementazione basata su Application Virtualization Management Server, è possibile scegliere tra diverse alternative, sfruttando qualsiasi infrastruttura già in vigore.</span><span class="sxs-lookup"><span data-stu-id="4360f-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="4360f-105">Se ad esempio sono già presenti server nelle succursali dei campi, è possibile inserire la condivisione di Application Virtualization \\CONTENT su tali server e quindi configurare i client per l'uso di tale condivisione di contenuto come origine di contenuto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4360f-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="4360f-106">Se si sceglie di usare solo i server di gestione della virtualizzazione delle applicazioni, ad esempio perché si ha una sola sede, i client possono eseguire lo streaming del contenuto da tale server.</span><span class="sxs-lookup"><span data-stu-id="4360f-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="4360f-107">Le opzioni supportate includono l'uso di un file server, di un server IIS o di un Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="4360f-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="4360f-108">È anche possibile installare Application Virtualization Streaming Server in un file server o un server IIS esistente.</span><span class="sxs-lookup"><span data-stu-id="4360f-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="4360f-109">Le caratteristiche di queste diverse opzioni sono riepilogate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4360f-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="4360f-110">**Nota**  La funzionalità di aggiornamento attivo consente di aggiungere una nuova versione di un'applicazione a un server di gestione di App-V o a un server di flusso senza influire sugli utenti che stanno attualmente eseguendo l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4360f-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="4360f-111">I client App-V riceveranno automaticamente la versione più recente dell'applicazione dall'App-V Management Server o dal server di streaming la volta successiva che l'utente avvia l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4360f-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="4360f-112">Per questa caratteristica è necessario usare il protocollo RTSP (S).</span><span class="sxs-lookup"><span data-stu-id="4360f-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4360f-113">Tipo di server</span><span class="sxs-lookup"><span data-stu-id="4360f-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="4360f-114">Protocollo</span><span class="sxs-lookup"><span data-stu-id="4360f-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="4360f-115">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="4360f-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="4360f-116">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="4360f-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="4360f-117">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="4360f-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4360f-118">File server</span><span class="sxs-lookup"><span data-stu-id="4360f-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4360f-119">SMB</span><span class="sxs-lookup"><span data-stu-id="4360f-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-120">Soluzione semplice a basso costo per configurare il file server esistente con la condivisione di \CONTENT</span><span class="sxs-lookup"><span data-stu-id="4360f-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-121">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="4360f-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="4360f-122">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="4360f-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4360f-123">Server IIS</span><span class="sxs-lookup"><span data-stu-id="4360f-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4360f-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="4360f-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-125">Supporta la sicurezza avanzata con il protocollo HTTPS</span><span class="sxs-lookup"><span data-stu-id="4360f-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4360f-126">Supporta lo streaming in computer remoti su Internet</span><span class="sxs-lookup"><span data-stu-id="4360f-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="4360f-127">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="4360f-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="4360f-128">Scalabile</span><span class="sxs-lookup"><span data-stu-id="4360f-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="4360f-129">Protocollo familiare</span><span class="sxs-lookup"><span data-stu-id="4360f-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-130">Necessità di gestire IIS</span><span class="sxs-lookup"><span data-stu-id="4360f-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="4360f-131">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="4360f-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="4360f-132">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="4360f-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4360f-133">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="4360f-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4360f-134">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="4360f-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-135">Aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="4360f-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="4360f-136">Supporta la sicurezza avanzata tramite il protocollo RTSPs</span><span class="sxs-lookup"><span data-stu-id="4360f-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4360f-137">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="4360f-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-138">Infrastruttura duale</span><span class="sxs-lookup"><span data-stu-id="4360f-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="4360f-139">Requisito di amministrazione del server</span><span class="sxs-lookup"><span data-stu-id="4360f-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="4360f-140">Come configurare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="4360f-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4360f-141">Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4360f-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4360f-142">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="4360f-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-143">Aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="4360f-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="4360f-144">Supporta la sicurezza avanzata tramite il protocollo RTSPs</span><span class="sxs-lookup"><span data-stu-id="4360f-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4360f-145">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="4360f-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4360f-146">Infrastruttura duale</span><span class="sxs-lookup"><span data-stu-id="4360f-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="4360f-147">Requisito di amministrazione del server</span><span class="sxs-lookup"><span data-stu-id="4360f-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="4360f-148">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4360f-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4360f-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4360f-149">Related topics</span></span>


[<span data-ttu-id="4360f-150">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="4360f-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="4360f-151">Panoramica dei componenti del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4360f-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="4360f-152">Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4360f-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





