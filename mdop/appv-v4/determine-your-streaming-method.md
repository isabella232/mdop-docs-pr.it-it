---
title: Determinare il metodo di streaming
description: Determinare il metodo di streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821666"
---
# <span data-ttu-id="a3183-103">Determinare il metodo di streaming</span><span class="sxs-lookup"><span data-stu-id="a3183-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="a3183-104">La prima volta che un utente fa doppio clic sull'icona inserita in un computer tramite il processo di pubblicazione, l'Application Virtualization Client otterrà il contenuto del pacchetto dell'applicazione virtuale da una posizione di origine di flusso.</span><span class="sxs-lookup"><span data-stu-id="a3183-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="a3183-105">**Nota** 
 Il *flusso* è il termine usato per descrivere il processo di ottenimento del contenuto da un pacchetto di applicazione sequenziata, a partire dal blocco di funzionalità principale e quindi ottenendo blocchi aggiuntivi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="a3183-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="a3183-106">La posizione di origine del flusso è in genere un server accessibile dal computer dell'utente; Tuttavia, alcuni sistemi di distribuzione elettronica, come Microsoft endpoint Configuration Manager, possono distribuire il file SFT nel computer dell'utente e quindi eseguire il flusso del pacchetto dell'applicazione virtuale localmente dalla cache di tale computer.</span><span class="sxs-lookup"><span data-stu-id="a3183-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="a3183-107">**Nota**  Una posizione di origine di flusso per i pacchetti virtuali può essere configurata in un computer che non è un server.</span><span class="sxs-lookup"><span data-stu-id="a3183-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="a3183-108">Ciò è particolarmente utile in una piccola filiale che non ha un server.</span><span class="sxs-lookup"><span data-stu-id="a3183-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="a3183-109">Le origini di flusso che possono essere usate per archiviare le applicazioni sequenziate sono descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a3183-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="a3183-110">Tipo di server</span><span class="sxs-lookup"><span data-stu-id="a3183-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="a3183-111">Protocollo</span><span class="sxs-lookup"><span data-stu-id="a3183-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="a3183-112">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="a3183-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="a3183-113">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="a3183-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="a3183-114">Collegamenti</span><span class="sxs-lookup"><span data-stu-id="a3183-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3183-115">File server</span><span class="sxs-lookup"><span data-stu-id="a3183-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3183-116">File</span><span class="sxs-lookup"><span data-stu-id="a3183-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-117">Soluzione semplice a basso costo per configurare il file server esistente con la condivisione di \CONTENT</span><span class="sxs-lookup"><span data-stu-id="a3183-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-118">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="a3183-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="a3183-119">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="a3183-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3183-120">Server IIS</span><span class="sxs-lookup"><span data-stu-id="a3183-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3183-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="a3183-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-122">Supporta la sicurezza avanzata usando il protocollo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a3183-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="a3183-123">Supporta lo streaming in computer remoti su Internet</span><span class="sxs-lookup"><span data-stu-id="a3183-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="a3183-124">Aprire una sola porta nel firewall</span><span class="sxs-lookup"><span data-stu-id="a3183-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="a3183-125">Altamente scalabile</span><span class="sxs-lookup"><span data-stu-id="a3183-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="a3183-126">Protocollo familiare</span><span class="sxs-lookup"><span data-stu-id="a3183-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-127">Necessità di gestire IIS</span><span class="sxs-lookup"><span data-stu-id="a3183-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="a3183-128">Nessun aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="a3183-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="a3183-129">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="a3183-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3183-130">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="a3183-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3183-131">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="a3183-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-132">Aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="a3183-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="a3183-133">Supporta la sicurezza avanzata tramite il protocollo RTSPs</span><span class="sxs-lookup"><span data-stu-id="a3183-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="a3183-134">Solo una porta nel firewall per l'apertura (solo RTSPs)</span><span class="sxs-lookup"><span data-stu-id="a3183-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3183-135">Infrastruttura duale</span><span class="sxs-lookup"><span data-stu-id="a3183-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="a3183-136">Requisito di amministrazione del server</span><span class="sxs-lookup"><span data-stu-id="a3183-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="a3183-137">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a3183-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a3183-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3183-138">Related topics</span></span>


[<span data-ttu-id="a3183-139">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="a3183-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="a3183-140">Panoramica di uno scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="a3183-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="a3183-141">Determinare il metodo di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="a3183-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





