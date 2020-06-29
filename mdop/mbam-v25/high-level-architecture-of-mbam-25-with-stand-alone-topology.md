---
title: Architettura di alto livello di MBAM 2.5 con topologia autonoma
description: Architettura di alto livello di MBAM 2.5 con topologia autonoma
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826556"
---
# <span data-ttu-id="084bb-103">Architettura di alto livello di MBAM 2.5 con topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="084bb-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="084bb-104">Questo argomento descrive l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia autonoma di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="084bb-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="084bb-105">In questa topologia MBAM viene distribuito come prodotto autonomo.</span><span class="sxs-lookup"><span data-stu-id="084bb-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="084bb-106">Puoi in alternativa distribuire MBAM con la topologia di integrazione di Configuration Manager, che si integra con MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="084bb-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="084bb-107">Per altre informazioni, Vedi [architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="084bb-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="084bb-108">Per un elenco delle versioni supportate del software menzionato in questo argomento, Vedi le [configurazioni supportate di MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="084bb-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="084bb-109">**Nota**  Ti consigliamo di usare un'architettura a server singolo solo in ambienti di test.</span><span class="sxs-lookup"><span data-stu-id="084bb-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="084bb-110">Numero consigliato di server e numero di client supportati</span><span class="sxs-lookup"><span data-stu-id="084bb-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="084bb-111">Il numero consigliato di server e il numero di client supportati in un ambiente di produzione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="084bb-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="084bb-112">Architettura consigliata in un ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="084bb-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="084bb-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="084bb-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="084bb-114">Numero di server e altri computer</span><span class="sxs-lookup"><span data-stu-id="084bb-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="084bb-115">Due server</span><span class="sxs-lookup"><span data-stu-id="084bb-115">Two servers</span></span></p>
<p><span data-ttu-id="084bb-116">Una workstation</span><span class="sxs-lookup"><span data-stu-id="084bb-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="084bb-117">Numero di computer client supportati</span><span class="sxs-lookup"><span data-stu-id="084bb-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="084bb-118">500.000</span><span class="sxs-lookup"><span data-stu-id="084bb-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="084bb-119">Consigliabile MBAM architettura di alto livello con la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="084bb-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="084bb-120">Il diagramma e la tabella seguenti descrivono l'architettura a due server di alto livello consigliata per MBAM con la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="084bb-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="084bb-121">Le distribuzioni di MBAM multi-Forest richiedono un trust unidirezionale o bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="084bb-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="084bb-122">I trust unidirezionali richiedono che il dominio del server si fidi del dominio client.</span><span class="sxs-lookup"><span data-stu-id="084bb-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="084bb-124">Funzionalità del server da configurare nel server di database della descrizione del server</span><span class="sxs-lookup"><span data-stu-id="084bb-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="084bb-125">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="084bb-125">Compliance and Audit Database</span></span>

<span data-ttu-id="084bb-126">Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="084bb-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="084bb-127">Il **database di conformità e controllo** archivia i dati di conformità, che vengono usati principalmente per i report ospitati da SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="084bb-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="084bb-128">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="084bb-128">Recovery Database</span></span>

<span data-ttu-id="084bb-129">Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="084bb-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="084bb-130">Il **database di ripristino** archivia i dati di recupero raccolti dai computer client di mbam.</span><span class="sxs-lookup"><span data-stu-id="084bb-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="084bb-131">Rapporti</span><span class="sxs-lookup"><span data-stu-id="084bb-131">Reports</span></span>

<span data-ttu-id="084bb-132">Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="084bb-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="084bb-133">I **report** includono i dati di controllo del ripristino e dello stato di conformità relativi ai computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="084bb-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="084bb-134">È possibile accedere ai report dal sito Web di amministrazione e monitoraggio o direttamente da SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="084bb-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="084bb-135">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="084bb-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="084bb-136">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="084bb-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="084bb-137">Questa caratteristica è configurata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="084bb-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="084bb-138">Il **sito Web di amministrazione e monitoraggio** viene usato per:</span><span class="sxs-lookup"><span data-stu-id="084bb-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="084bb-139">Aiutare gli utenti finali a recuperare l'accesso ai propri computer quando sono bloccati. (L'area del sito Web viene comunemente chiamata Help desk).</span><span class="sxs-lookup"><span data-stu-id="084bb-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="084bb-140">Visualizzare i report che mostrano lo stato di conformità e l'attività di ripristino per i computer client.</span><span class="sxs-lookup"><span data-stu-id="084bb-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="084bb-141">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="084bb-141">Self-Service Portal</span></span>

<span data-ttu-id="084bb-142">Questa caratteristica è configurata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="084bb-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="084bb-143">Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="084bb-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="084bb-144">Monitoraggio dei servizi Web per questo sito Web</span><span class="sxs-lookup"><span data-stu-id="084bb-144">Monitoring web services for this website</span></span>

<span data-ttu-id="084bb-145">Questa caratteristica è configurata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="084bb-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="084bb-146">I **servizi Web di monitoraggio** vengono usati dal client mbam e dai siti Web per comunicare con il database.</span><span class="sxs-lookup"><span data-stu-id="084bb-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="084bb-147">**Importante**  Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 dato che i siti Web di MBAM comunicano direttamente con il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="084bb-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="084bb-148">Workstation di gestione</span><span class="sxs-lookup"><span data-stu-id="084bb-148">Management workstation</span></span>

<span data-ttu-id="084bb-149">Modelli di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="084bb-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="084bb-150">I modelli dei criteri di gruppo di MBAM sono impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione per MBAM, che consentono di gestire la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="084bb-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="084bb-151">Prima di eseguire MBAM, è necessario scaricare i modelli di criteri di gruppo da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.</span><span class="sxs-lookup"><span data-stu-id="084bb-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="084bb-152">La workstation non deve essere un computer dedicato.</span><span class="sxs-lookup"><span data-stu-id="084bb-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="084bb-153">Client MBAM e computer client di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="084bb-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="084bb-154">Software client MBAM</span><span class="sxs-lookup"><span data-stu-id="084bb-154">MBAM Client software</span></span>

<span data-ttu-id="084bb-155">Il client MBAM:</span><span class="sxs-lookup"><span data-stu-id="084bb-155">The MBAM Client:</span></span>

-   <span data-ttu-id="084bb-156">USA gli oggetti Criteri di gruppo per applicare la crittografia unità BitLocker nei computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="084bb-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="084bb-157">Raccoglie la chiave di ripristino di BitLocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).</span><span class="sxs-lookup"><span data-stu-id="084bb-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="084bb-158">Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.</span><span class="sxs-lookup"><span data-stu-id="084bb-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="084bb-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="084bb-159">Related topics</span></span>


[<span data-ttu-id="084bb-160">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="084bb-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="084bb-161">Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="084bb-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="084bb-162">Funzionalità illustrate di una distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="084bb-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="084bb-163">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="084bb-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="084bb-164">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="084bb-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="084bb-165">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="084bb-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





