---
title: Elenco di controllo per la distribuzione di MBAM 1.0
description: Elenco di controllo per la distribuzione di MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804300"
---
# <span data-ttu-id="86b6f-103">Elenco di controllo per la distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="86b6f-104">Questo elenco di controllo è progettato per facilitare la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="86b6f-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="86b6f-105">Nota</span><span class="sxs-lookup"><span data-stu-id="86b6f-105">Note</span></span>**  
<span data-ttu-id="86b6f-106">Questo elenco di controllo illustra la procedura consigliata e fornisce un elenco di elementi di alto livello da considerare quando si distribuiscono le caratteristiche di MBAM.</span><span class="sxs-lookup"><span data-stu-id="86b6f-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="86b6f-107">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo in base alle specifiche esigenze.</span><span class="sxs-lookup"><span data-stu-id="86b6f-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="86b6f-108">Attività</span><span class="sxs-lookup"><span data-stu-id="86b6f-108">Task</span></span></th>
<th align="left"><span data-ttu-id="86b6f-109">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="86b6f-109">References</span></span></th>
<th align="left"><span data-ttu-id="86b6f-110">Note</span><span class="sxs-lookup"><span data-stu-id="86b6f-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-111">Completare la fase di pianificazione per preparare l'ambiente di calcolo per la distribuzione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="86b6f-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="86b6f-112">Elenco di controllo per la pianificazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-113">Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="86b6f-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="86b6f-114">Configurazioni supportate di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-115">Eseguire la configurazione di MBAM per distribuire le caratteristiche del server MBAM nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="86b6f-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="86b6f-116">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="86b6f-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="86b6f-117">Database di stato conformità</span><span class="sxs-lookup"><span data-stu-id="86b6f-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="86b6f-118">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="86b6f-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="86b6f-119">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="86b6f-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="86b6f-120">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="86b6f-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="86b6f-121">Nota</span><span class="sxs-lookup"><span data-stu-id="86b6f-121">Note</span></span></strong><br/><p><span data-ttu-id="86b6f-122">Tenere traccia dei nomi dei server in cui è installata ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="86b6f-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="86b6f-123">Si utilizzeranno queste informazioni durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="86b6f-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="86b6f-124">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-125">Aggiungere gruppi di sicurezza di servizi di dominio Active Directory creati durante la fase di pianificazione per i gruppi di amministratori locali appropriati di MBAM server nei server appropriati.</span><span class="sxs-lookup"><span data-stu-id="86b6f-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="86b6f-126">Pianificazione per i ruoli di amministratore di MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> come gestire i ruoli di amministratore di mbam</span><span class="sxs-lookup"><span data-stu-id="86b6f-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-127">Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="86b6f-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="86b6f-128">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="86b6f-129">Distribuire il software del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="86b6f-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="86b6f-130">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="86b6f-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86b6f-131">Related topics</span></span>


[<span data-ttu-id="86b6f-132">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="86b6f-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









