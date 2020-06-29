---
title: Pianificazione della distribuzione del server di MBAM 2.5
description: Pianificazione della distribuzione del server di MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826215"
---
# <span data-ttu-id="89749-103">Pianificazione della distribuzione del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="89749-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="89749-104">Questo argomento elenca le caratteristiche che vengono distribuite per le topologie di MBAM autonomo e di gestione configurazione ed elenca l'ordine in cui è necessario distribuirle.</span><span class="sxs-lookup"><span data-stu-id="89749-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="89749-105">Esiste una configurazione consigliata per ogni topologia.</span><span class="sxs-lookup"><span data-stu-id="89749-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="89749-106">Tuttavia, è possibile configurare i database e le funzionalità di MBAM server in diverse configurazioni e in più server, a seconda dei requisiti di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="89749-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="89749-107">Considerazioni importanti sulla pianificazione per entrambe le topologie</span><span class="sxs-lookup"><span data-stu-id="89749-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="89749-108">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="89749-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="89749-109">Dettagli o finalità</span><span class="sxs-lookup"><span data-stu-id="89749-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89749-110">Prima di avviare la distribuzione, vedere la seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="89749-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="89749-111">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="89749-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="89749-112">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="89749-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="89749-113">Ogni caratteristica MBAM ha prerequisiti specifici che devono essere soddisfatti prima di avviare l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="89749-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89749-114">Le chiavi di ripristino di BitLocker in MBAM scadono dopo un uso singolo.</span><span class="sxs-lookup"><span data-stu-id="89749-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="89749-115">Un uso singolo indica che la chiave di ripristino è stata recuperata tramite il sito Web di amministrazione e monitoraggio (noto anche come Help desk), portale self-service o usando il <strong> cmdlet Get-MbamBitLockerRecoveryKey di </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89749-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89749-116">Tenere traccia dei nomi dei computer in cui si configura ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="89749-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="89749-117">Userai queste informazioni durante il processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="89749-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="89749-118">Per questo scopo, è consigliabile usare l' <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> elenco di controllo della distribuzione di MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="89749-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89749-119">Configurare solo le impostazioni di criteri di gruppo nel nodo MDOP MBAM (BitLocker Management).</span><span class="sxs-lookup"><span data-stu-id="89749-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="89749-120">Non modificare le impostazioni dei criteri di gruppo nel nodo crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="89749-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="89749-121">Se si modificano le impostazioni dei criteri di gruppo nel nodo crittografia unità BitLocker, MBAM non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="89749-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="89749-122">Pianificazione per la distribuzione di MBAM server-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="89749-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="89749-123">Per la topologia autonoma è consigliabile usare una configurazione a due server per gli ambienti di produzione, anche se possono essere usate configurazioni da tre a quattro server.</span><span class="sxs-lookup"><span data-stu-id="89749-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="89749-124">L'infrastruttura server per la topologia autonoma di MBAM contiene le caratteristiche seguenti, che devono essere configurate nell'ordine indicato:</span><span class="sxs-lookup"><span data-stu-id="89749-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="89749-125">Database (database di conformità e database di controllo e ripristino)</span><span class="sxs-lookup"><span data-stu-id="89749-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="89749-126">Rapporti</span><span class="sxs-lookup"><span data-stu-id="89749-126">Reports</span></span>

3.  <span data-ttu-id="89749-127">Applicazioni Web (e relativi servizi Web)</span><span class="sxs-lookup"><span data-stu-id="89749-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="89749-128">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="89749-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="89749-129">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="89749-129">Self-Service Portal</span></span>

<span data-ttu-id="89749-130">Per una descrizione di queste funzionalità, Vedi l' [architettura di alto livello di MBAM 2,5 con topologia autonoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="89749-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="89749-131">Pianificazione per la distribuzione di MBAM server-topologia di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="89749-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="89749-132">Per la topologia di integrazione di Configuration Manager, è consigliabile una configurazione a tre server per gli ambienti di produzione, anche se è possibile usare configurazioni di server aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="89749-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="89749-133">L'infrastruttura server per la topologia di MBAM Configuration Manager contiene le caratteristiche seguenti, che devono essere configurate o eseguite nell'ordine indicato:</span><span class="sxs-lookup"><span data-stu-id="89749-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="89749-134">Database (database di conformità e database di controllo e ripristino)</span><span class="sxs-lookup"><span data-stu-id="89749-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="89749-135">Rapporti</span><span class="sxs-lookup"><span data-stu-id="89749-135">Reports</span></span>

3.  <span data-ttu-id="89749-136">Applicazioni Web (e relativi servizi Web)</span><span class="sxs-lookup"><span data-stu-id="89749-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="89749-137">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="89749-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="89749-138">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="89749-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="89749-139">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="89749-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="89749-140">Per una descrizione di queste funzionalità, Vedi l' [architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="89749-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="89749-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89749-141">Related topics</span></span>


[<span data-ttu-id="89749-142">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="89749-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="89749-143">Distribuzione dell'infrastruttura server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="89749-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="89749-144">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="89749-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="89749-145">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="89749-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="89749-146">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="89749-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





