---
title: Elenco di controllo per la pianificazione di MBAM 2.5
description: Elenco di controllo per la pianificazione di MBAM 2.5
author: dansimp
ms.assetid: ffe11eb8-44db-4886-8300-6dffec8bcfa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 505f2890d67f36056ab5bb87df2a894473cd3306
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826545"
---
# <span data-ttu-id="e33f5-103">Elenco di controllo per la pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-103">MBAM 2.5 Planning Checklist</span></span>


<span data-ttu-id="e33f5-104">Puoi usare gli elenchi di controllo seguenti per preparare l'ambiente di elaborazione per la distribuzione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="e33f5-104">You can use the following checklists to help you prepare your computing environment for the Microsoft BitLocker Administration and Monitoring (MBAM) deployment.</span></span> <span data-ttu-id="e33f5-105">Gli elenchi di controllo includono un elenco di elementi di alto livello da tenere in considerazione durante la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f5-105">The checklists provide a high-level list of items to consider when planning the deployment.</span></span> <span data-ttu-id="e33f5-106">Sono disponibili elenchi di controllo distinti per la topologia autonoma e la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e33f5-106">There are separate checklists for the Stand-alone topology and the Configuration Manager Integration topology.</span></span> <span data-ttu-id="e33f5-107">È consigliabile copiare l'elenco di controllo desiderato in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="e33f5-107">You might want to copy the desired checklist into a spreadsheet and customize it for your use.</span></span>

**<span data-ttu-id="e33f5-108">Elenco di controllo pianificazione per una distribuzione di MBAM</span><span class="sxs-lookup"><span data-stu-id="e33f5-108">Planning checklist for an MBAM deployment</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="e33f5-109">Attività</span><span class="sxs-lookup"><span data-stu-id="e33f5-109">Task</span></span></th>
<th align="left"><span data-ttu-id="e33f5-110">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="e33f5-110">References</span></span></th>
<th align="left"><span data-ttu-id="e33f5-111">Note</span><span class="sxs-lookup"><span data-stu-id="e33f5-111">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-112">Esaminare le &quot; informazioni introduttive &quot; per comprendere il prodotto prima di avviare la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f5-112">Review the &quot;Getting started&quot; information to understand the product before you start deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-25.md" data-raw-source="[Getting Started with MBAM 2.5](getting-started-with-mbam-25.md)"><span data-ttu-id="e33f5-113">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-113">Getting Started with MBAM 2.5</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-114">Esaminare l'architettura di alto livello consigliata per una distribuzione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-114">Review the recommended high-level architecture for an MBAM deployment.</span></span> <span data-ttu-id="e33f5-115">Si potrebbe anche voler rivedere una figura e una descrizione delle singole parti (database, siti Web, report) di una distribuzione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-115">You might also want to review an illustration and description of the individual parts (databases, websites, Reports) of an MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="e33f5-116">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-116">High-Level Architecture for MBAM 2.5</span></span></a></p>
<p><a href="illustrated-features-of-an-mbam-25-deployment.md" data-raw-source="[Illustrated Features of an MBAM 2.5 Deployment](illustrated-features-of-an-mbam-25-deployment.md)"><span data-ttu-id="e33f5-117">Funzionalità illustrate di una distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-117">Illustrated Features of an MBAM 2.5 Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-118">Esaminare e completare i prerequisiti per le topologie di integrazione di MBAM stand-alone e Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e33f5-118">Review and complete the prerequisites for the MBAM Stand-alone and Configuration Manager Integration topologies.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="e33f5-119">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e33f5-119">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-120">Se si prevede di usare la topologia di integrazione di Configuration Manager, completare i prerequisiti aggiuntivi che si applicano solo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="e33f5-120">If you plan to use the Configuration Manager Integration topology, complete the additional prerequisites that apply only to this topology.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="e33f5-121">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e33f5-121">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-122">Rivedere e soddisfare i prerequisiti di MBAM 2,5 per il client MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-122">Review and meet the MBAM 2.5 prerequisites for the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="prerequisites-for-mbam-25-clients.md" data-raw-source="[Prerequisites for MBAM 2.5 Clients](prerequisites-for-mbam-25-clients.md)"><span data-ttu-id="e33f5-123">Prerequisiti per i client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-123">Prerequisites for MBAM 2.5 Clients</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-124">Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-124">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="e33f5-125">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-125">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-126">Pianificare e creare i gruppi di sicurezza di ActiveDirectoryDomainServices necessari.</span><span class="sxs-lookup"><span data-stu-id="e33f5-126">Plan for and create the necessary ActiveDirectoryDomainServices security groups.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"><span data-ttu-id="e33f5-127">Pianificazione di gruppi e account di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-127">Planning for MBAM 2.5 Groups and Accounts</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-128">Pianificare come proteggere i siti Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-128">Plan how you will secure the MBAM websites.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"><span data-ttu-id="e33f5-129">Pianificazione di come proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="e33f5-129">Planning How to Secure the MBAM Websites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-130">Esaminare le configurazioni supportate da MBAM per verificare che l'hardware soddisfi i requisiti di sistema per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e33f5-130">Review the MBAM Supported Configurations to ensure that your hardware meets the installation system requirements.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="e33f5-131">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-131">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-132">Esaminare le considerazioni per la distribuzione delle caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-132">Review the considerations for deploying the MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-server-deployment.md" data-raw-source="[Planning for MBAM 2.5 Server Deployment](planning-for-mbam-25-server-deployment.md)"><span data-ttu-id="e33f5-133">Pianificazione della distribuzione del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-133">Planning for MBAM 2.5 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-134">Esaminare le considerazioni per la distribuzione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="e33f5-134">Review the considerations for deploying the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-client-deployment.md" data-raw-source="[Planning for MBAM 2.5 Client Deployment](planning-for-mbam-25-client-deployment.md)"><span data-ttu-id="e33f5-135">Pianificazione della distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-135">Planning for MBAM 2.5 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-136">Esaminare i requisiti e i passaggi per distribuire MBAM in una configurazione altamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e33f5-136">Review the requirements and steps to deploy MBAM in a highly available configuration.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-high-availability.md" data-raw-source="[Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md)"><span data-ttu-id="e33f5-137">Pianificazione della disponibilità elevata per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-137">Planning for MBAM 2.5 High Availability</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-138">Esaminare le considerazioni sulla sicurezza di MBAM che riguardano il modulo Trusted Platform, i file di log e la crittografia dei dati trasparente.</span><span class="sxs-lookup"><span data-stu-id="e33f5-138">Review the MBAM security considerations that pertain to the Trusted Platform Module, log files, and transparent data encryption.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"><span data-ttu-id="e33f5-139">Considerazioni sulla sicurezza per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-139">MBAM 2.5 Security Considerations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e33f5-140">Facoltativamente, esaminare la procedura per valutare MBAM in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="e33f5-140">Optionally, review the steps to evaluate MBAM in a test environment.</span></span></p></td>
<td align="left"><p><a href="evaluating-mbam-25-in-a-test-environment.md" data-raw-source="[Evaluating MBAM 2.5 in a Test Environment](evaluating-mbam-25-in-a-test-environment.md)"><span data-ttu-id="e33f5-141">Valutazione di MBAM 2.5 in un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="e33f5-141">Evaluating MBAM 2.5 in a Test Environment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="e33f5-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e33f5-142">Related topics</span></span>


[<span data-ttu-id="e33f5-143">Pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e33f5-143">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 

 
## <span data-ttu-id="e33f5-144">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="e33f5-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e33f5-145">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e33f5-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e33f5-146">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e33f5-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




