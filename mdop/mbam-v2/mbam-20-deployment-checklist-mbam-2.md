---
title: Elenco di controllo per la distribuzione di MBAM 2.0
description: Elenco di controllo per la distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826436"
---
# <span data-ttu-id="d589f-103">Elenco di controllo per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="d589f-104">Questo elenco di controllo può essere usato per facilitare la distribuzione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker con una topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="d589f-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="d589f-105">Nota</span><span class="sxs-lookup"><span data-stu-id="d589f-105">Note</span></span>**  
<span data-ttu-id="d589f-106">Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da tenere in considerazione durante la distribuzione delle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d589f-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="d589f-107">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="d589f-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="d589f-108">Attività</span><span class="sxs-lookup"><span data-stu-id="d589f-108">Task</span></span></th>
<th align="left"><span data-ttu-id="d589f-109">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="d589f-109">References</span></span></th>
<th align="left"><span data-ttu-id="d589f-110">Note</span><span class="sxs-lookup"><span data-stu-id="d589f-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-111">Completare la fase di pianificazione per preparare l'ambiente di calcolo per la distribuzione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="d589f-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="d589f-112">Elenco di controllo per la pianificazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-113">Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="d589f-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="d589f-114">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-115">Eseguire la configurazione di MBAM per distribuire le caratteristiche del server MBAM nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="d589f-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="d589f-116">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="d589f-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="d589f-117">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="d589f-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="d589f-118">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="d589f-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="d589f-119">Server self-service</span><span class="sxs-lookup"><span data-stu-id="d589f-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="d589f-120">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="d589f-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="d589f-121">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="d589f-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="d589f-122">Nota</span><span class="sxs-lookup"><span data-stu-id="d589f-122">Note</span></span></strong><br/><p><span data-ttu-id="d589f-123">Tenere traccia dei nomi dei server in cui è installata ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d589f-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="d589f-124">Queste informazioni verranno usate durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="d589f-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="d589f-125">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-126">Aggiungere gruppi di sicurezza di servizi di dominio Active Directory creati durante la fase di pianificazione per i gruppi di amministratori locali appropriati di MBAM server nei server appropriati.</span><span class="sxs-lookup"><span data-stu-id="d589f-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="d589f-127">Pianificazione per i ruoli di amministratore di MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> come gestire i ruoli di amministratore di mbam</span><span class="sxs-lookup"><span data-stu-id="d589f-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-128">Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="d589f-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="d589f-129">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d589f-130">Distribuire il software del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="d589f-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="d589f-131">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d589f-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d589f-132">Related topics</span></span>


[<span data-ttu-id="d589f-133">Distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d589f-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









