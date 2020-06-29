---
title: Configurazione delle funzionalità server di MBAM 2.5
description: Configurazione delle funzionalità server di MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823056"
---
# <span data-ttu-id="ff340-103">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="ff340-104">Usare queste informazioni come punto di partenza per configurare le caratteristiche del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 dopo l' [installazione del software mbam 2,5 Server](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="ff340-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="ff340-105">Esistono due metodi che è possibile usare per configurare MBAM:</span><span class="sxs-lookup"><span data-stu-id="ff340-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="ff340-106">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="ff340-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="ff340-107">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff340-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="ff340-108">Prima di iniziare a configurare le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="ff340-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="ff340-109">Esaminare e completare i passaggi seguenti prima di iniziare a configurare le caratteristiche del server MBAM:</span><span class="sxs-lookup"><span data-stu-id="ff340-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff340-110">Passaggio</span><span class="sxs-lookup"><span data-stu-id="ff340-110">Step</span></span></th>
<th align="left"><span data-ttu-id="ff340-111">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="ff340-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff340-112">Esaminare l'architettura consigliata per MBAM.</span><span class="sxs-lookup"><span data-stu-id="ff340-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="ff340-113">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff340-114">Esaminare le configurazioni supportate per MBAM.</span><span class="sxs-lookup"><span data-stu-id="ff340-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="ff340-115">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff340-116">Completare i prerequisiti necessari per ogni server.</span><span class="sxs-lookup"><span data-stu-id="ff340-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="ff340-117">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff340-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="ff340-118">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff340-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff340-119">Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="ff340-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="ff340-120">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff340-121">Esaminare i prerequisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM (se si usa questo metodo per configurare le caratteristiche del server MBAM).</span><span class="sxs-lookup"><span data-stu-id="ff340-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="ff340-122">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff340-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ff340-123">Procedura per la configurazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="ff340-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="ff340-124">Ogni riga della tabella seguente descrive le caratteristiche che verranno configurate in un server distinto, in base all' [architettura di alto livello consigliata per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ff340-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ff340-125">Caratteristiche da installare</span><span class="sxs-lookup"><span data-stu-id="ff340-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="ff340-126">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="ff340-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff340-127">Configurare i database.</span><span class="sxs-lookup"><span data-stu-id="ff340-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="ff340-128">Come configurare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff340-129">Configurare i report.</span><span class="sxs-lookup"><span data-stu-id="ff340-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="ff340-130">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ff340-131">Configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="ff340-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="ff340-132">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ff340-133">Configurare l'integrazione di System Center Configuration Manager (se applicabile).</span><span class="sxs-lookup"><span data-stu-id="ff340-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="ff340-134">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff340-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ff340-135">Per un elenco degli eventi relativi alla configurazione delle funzionalità di MBAM server, vedere [log eventi del server](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="ff340-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="ff340-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff340-136">Related topics</span></span>


<span data-ttu-id="ff340-137">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ff340-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="ff340-138">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="ff340-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ff340-139">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ff340-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ff340-140">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ff340-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



