---
title: Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software
description: Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815856"
---
# <span data-ttu-id="e5f48-103">Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="e5f48-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="e5f48-104">Se si decide di usare i server di streaming in combinazione con il sistema ESD per rendere disponibile il contenuto dell'applicazione per i computer degli utenti finali, è possibile scegliere tra diverse alternative, sfruttando qualsiasi tipo di infrastruttura già in vigore.</span><span class="sxs-lookup"><span data-stu-id="e5f48-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="e5f48-105">Ad esempio, se il sistema ESD include condivisioni di distribuzione del software nei server delle succursali dei campi, è possibile inserire la condivisione di Application Virtualization \\CONTENT su tali server e quindi configurare i client per l'uso della condivisione di contenuto come origine di contenuto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5f48-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="e5f48-106">Le opzioni supportate includono l'uso di un file server o di un server IIS.</span><span class="sxs-lookup"><span data-stu-id="e5f48-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="e5f48-107">È anche possibile installare Application Virtualization Streaming Server in un file server o un server IIS esistente.</span><span class="sxs-lookup"><span data-stu-id="e5f48-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="e5f48-108">Application Virtualization Streaming Server offre il supporto per la funzionalità di aggiornamento attivo nella virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e5f48-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="e5f48-109">La funzionalità di aggiornamento attivo consente di aggiungere una nuova versione di un'applicazione a un server di gestione di App-V o a un server di flusso senza influire sugli utenti che stanno attualmente eseguendo l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5f48-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="e5f48-110">I client App-V riceveranno automaticamente la versione più recente dell'applicazione dall'App-V Management Server o dal server di streaming la volta successiva che l'utente avvia l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5f48-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="e5f48-111">Per questa caratteristica è necessario usare il protocollo RTSP (S).</span><span class="sxs-lookup"><span data-stu-id="e5f48-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="e5f48-112">Se si sceglie di non usare Application Virtualization Streaming Server, è necessario gestire in modo esplicito gli aggiornamenti dei pacchetti di applicazioni tramite il sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="e5f48-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="e5f48-113">**Nota**  L'accesso alle applicazioni viene controllato tramite gruppi di sicurezza in servizi di dominio Active Directory, quindi sarà necessario pianificare un processo per la configurazione di un gruppo di sicurezza per ogni applicazione virtuale e per la gestione degli utenti aggiunti a ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="e5f48-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="e5f48-114">L'amministratore dell'Application Virtualization System configura ogni server di flusso per l'uso di questi gruppi di Active Directory applicando gli elenchi ACL alle directory dell'applicazione sotto la condivisione di contenuto, che controlla l'accesso ai pacchetti in base all'appartenenza ai gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e5f48-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="e5f48-115">Le caratteristiche delle opzioni di flusso disponibili sono riepilogate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e5f48-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

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
<th align="left"><span data-ttu-id="e5f48-116">Tipo di server</span><span class="sxs-lookup"><span data-stu-id="e5f48-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="e5f48-117">Protocollo</span><span class="sxs-lookup"><span data-stu-id="e5f48-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="e5f48-118">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="e5f48-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="e5f48-119">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="e5f48-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="e5f48-120">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="e5f48-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5f48-121">File server</span><span class="sxs-lookup"><span data-stu-id="e5f48-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5f48-122">SMB</span><span class="sxs-lookup"><span data-stu-id="e5f48-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-123">Soluzione semplice a basso costo per configurare il file server esistente con la condivisione di \CONTENT</span><span class="sxs-lookup"><span data-stu-id="e5f48-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-124">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="e5f48-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="e5f48-125">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="e5f48-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5f48-126">Server IIS</span><span class="sxs-lookup"><span data-stu-id="e5f48-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5f48-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="e5f48-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-128">Supporta la sicurezza avanzata con il protocollo HTTPS</span><span class="sxs-lookup"><span data-stu-id="e5f48-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="e5f48-129">Supporta lo streaming in computer remoti su Internet</span><span class="sxs-lookup"><span data-stu-id="e5f48-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="e5f48-130">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="e5f48-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="e5f48-131">Scalabile</span><span class="sxs-lookup"><span data-stu-id="e5f48-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="e5f48-132">Protocollo familiare</span><span class="sxs-lookup"><span data-stu-id="e5f48-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-133">Necessità di gestire IIS</span><span class="sxs-lookup"><span data-stu-id="e5f48-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="e5f48-134">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="e5f48-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="e5f48-135">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="e5f48-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5f48-136">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="e5f48-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5f48-137">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="e5f48-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-138">Aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="e5f48-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="e5f48-139">Supporta la sicurezza avanzata tramite il protocollo RTSPs</span><span class="sxs-lookup"><span data-stu-id="e5f48-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="e5f48-140">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="e5f48-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e5f48-141">Infrastruttura duale</span><span class="sxs-lookup"><span data-stu-id="e5f48-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="e5f48-142">Requisito di amministrazione del server</span><span class="sxs-lookup"><span data-stu-id="e5f48-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="e5f48-143">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e5f48-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e5f48-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5f48-144">Related topics</span></span>


[<span data-ttu-id="e5f48-145">Come configurare i server per la distribuzione basata su ESD</span><span class="sxs-lookup"><span data-stu-id="e5f48-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="e5f48-146">Panoramica di sicurezza e protezione</span><span class="sxs-lookup"><span data-stu-id="e5f48-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="e5f48-147">Pubblicazione delle applicazioni virtuali con distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="e5f48-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





