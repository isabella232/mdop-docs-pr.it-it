---
title: Scenari di server con connessione Internet per le reti perimetrali
description: Scenari di server con connessione Internet per le reti perimetrali
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816285"
---
# <span data-ttu-id="5f6a0-103">Scenari di server con connessione Internet per le reti perimetrali</span><span class="sxs-lookup"><span data-stu-id="5f6a0-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="5f6a0-104">App-V 4.5 supporta scenari server con accesso a Internet, in cui gli utenti che non sono connessi alla rete aziendale o che si disconnettono dalla rete possono ancora usare app-V.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="5f6a0-105">Come illustrato nella figura seguente, è supportato solo l'uso di protocolli protetti su Internet (RTSPs e HTTPS).</span><span class="sxs-lookup"><span data-stu-id="5f6a0-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![diagramma di posizionamento del Firewall App-v](images/appvfirewalls.gif)

<span data-ttu-id="5f6a0-107">È possibile configurare una soluzione Internet, usando un server ISA, in cui l'infrastruttura App-V si trova nella rete interna nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f6a0-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="5f6a0-108">Creare una regola di pubblicazione Web per il server IIS che ospita i file ICO e OSD, e facoltativamente i pacchetti per il flusso, che si trovano nella rete interna.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="5f6a0-109">Le procedure dettagliate sono disponibili in <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="5f6a0-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="5f6a0-110">Creare una regola di pubblicazione del server per App-V Web Management Server (RTSPs).</span><span class="sxs-lookup"><span data-stu-id="5f6a0-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="5f6a0-111">Le procedure dettagliate sono disponibili in [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="5f6a0-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="5f6a0-112">Come illustrato nella figura seguente, se l'infrastruttura ha implementato altri firewall tra il client e il server ISA o tra ISA Server e la rete interna, è necessario creare regole del firewall RTSPs (TCP 322) e HTTPS (TCP 443) per supportare il flusso del traffico.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="5f6a0-113">Inoltre, se i firewall sono stati implementati tra ISA Server e la rete interna, il traffico predefinito necessario per i membri del dominio deve essere autorizzato a eseguire il tunneling attraverso il firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="5f6a0-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![diagramma firewall di rete perimetrale App-v](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="5f6a0-115">Poiché le soluzioni firewall variano da ambiente a ambiente, le indicazioni fornite in questo argomento descrivono il traffico che sarebbe necessario per configurare un ambiente App-V con accesso a Internet nella rete perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="5f6a0-116">Queste informazioni includono anche i server di rete interni consigliati.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="5f6a0-117">Posizionare i server seguenti nella rete perimetrale:</span><span class="sxs-lookup"><span data-stu-id="5f6a0-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="5f6a0-118">App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="5f6a0-118">App-V Management Server</span></span>

-   <span data-ttu-id="5f6a0-119">Server IIS per la pubblicazione e lo streaming</span><span class="sxs-lookup"><span data-stu-id="5f6a0-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="5f6a0-120">**Nota**  Si consiglia di posizionare il server di gestione e IIS in computer separati.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="5f6a0-121">Posizionare i server seguenti nella rete interna:</span><span class="sxs-lookup"><span data-stu-id="5f6a0-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="5f6a0-122">Content Server</span><span class="sxs-lookup"><span data-stu-id="5f6a0-122">Content server</span></span>

-   <span data-ttu-id="5f6a0-123">Archivio dati (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="5f6a0-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="5f6a0-124">Controller di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="5f6a0-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="5f6a0-125">Requisiti per il traffico</span><span class="sxs-lookup"><span data-stu-id="5f6a0-125">Traffic Requirements</span></span>


<span data-ttu-id="5f6a0-126">Le tabelle seguenti elencano i requisiti di traffico per la comunicazione da Internet e dalla rete perimetrale e dalla rete perimetrale alla rete interna.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f6a0-127">Requisiti per il traffico da Internet alla rete perimetrale</span><span class="sxs-lookup"><span data-stu-id="5f6a0-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="5f6a0-128">Dettagli</span><span class="sxs-lookup"><span data-stu-id="5f6a0-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f6a0-129">RTSPs (aggiornamento della pubblicazione e pacchetti di flusso)</span><span class="sxs-lookup"><span data-stu-id="5f6a0-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-130">TCP 322 per impostazione predefinita; Questa operazione può essere modificata in App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f6a0-131">HTTPS (Publishing ICO e file OSD e pacchetti di flusso)</span><span class="sxs-lookup"><span data-stu-id="5f6a0-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-132">TCP 443 per impostazione predefinita; Questa operazione può essere modificata nella configurazione di IIS.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f6a0-133">Requisiti per il traffico dalla rete perimetrale alla rete interna</span><span class="sxs-lookup"><span data-stu-id="5f6a0-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="5f6a0-134">Dettagli</span><span class="sxs-lookup"><span data-stu-id="5f6a0-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f6a0-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f6a0-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-136">TCP 1433 è l'impostazione predefinita, ma può essere configurata in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f6a0-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f6a0-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="5f6a0-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-138">Se la directory di contenuto si trova in remoto dal server di gestione o dal server IIS (scelta consigliata).</span><span class="sxs-lookup"><span data-stu-id="5f6a0-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f6a0-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="5f6a0-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-140">TCP e UDP 88</span><span class="sxs-lookup"><span data-stu-id="5f6a0-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f6a0-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="5f6a0-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-142">TCP e UDP 389</span><span class="sxs-lookup"><span data-stu-id="5f6a0-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f6a0-143">DNS</span><span class="sxs-lookup"><span data-stu-id="5f6a0-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f6a0-144">Per la risoluzione dei nomi delle risorse interne (può essere eliminata con l'uso del file dell'host nei server di rete perimetrale)</span><span class="sxs-lookup"><span data-stu-id="5f6a0-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





