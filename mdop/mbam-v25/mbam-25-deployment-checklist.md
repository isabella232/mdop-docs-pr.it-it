---
title: Elenco di controllo per la distribuzione di MBAM 2.5
description: Elenco di controllo per la distribuzione di MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822835"
---
# <span data-ttu-id="00bbc-103">Elenco di controllo per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-103">MBAM 2.5 Deployment Checklist</span></span>


<span data-ttu-id="00bbc-104">Puoi usare questo elenco di controllo per aiutarti durante la distribuzione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker con una topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="00bbc-104">You can use this checklist to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="00bbc-105">Nota</span><span class="sxs-lookup"><span data-stu-id="00bbc-105">Note</span></span>**  
<span data-ttu-id="00bbc-106">Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da considerare quando si distribuiscono le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="00bbc-106">This checklist outlines the recommended steps and a high-level list of items to consider when you deploy Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="00bbc-107">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="00bbc-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="00bbc-108">Attività</span><span class="sxs-lookup"><span data-stu-id="00bbc-108">Task</span></span></th>
<th align="left"><span data-ttu-id="00bbc-109">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="00bbc-109">References</span></span></th>
<th align="left"><span data-ttu-id="00bbc-110">Note</span><span class="sxs-lookup"><span data-stu-id="00bbc-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-111">Esaminare e completare tutte le fasi di pianificazione per preparare l'ambiente per la distribuzione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="00bbc-111">Review and complete all planning steps to prepare your environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)"><span data-ttu-id="00bbc-112">Elenco di controllo per la pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-112">MBAM 2.5 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-113">Esaminare le informazioni sulle configurazioni supportate per verificare che MBAM supporti i computer client e server selezionati.</span><span class="sxs-lookup"><span data-stu-id="00bbc-113">Review the supported configurations information to ensure that MBAM supports the selected client and server computers.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="00bbc-114">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-115">Installare il software del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="00bbc-115">Install the MBAM Server software.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="00bbc-116">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-116">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-117">Configurare le caratteristiche del server MBAM:</span><span class="sxs-lookup"><span data-stu-id="00bbc-117">Configure the MBAM Server features:</span></span></p>
<ul>
<li><p><span data-ttu-id="00bbc-118">Database di conformità e audit e database di ripristino</span><span class="sxs-lookup"><span data-stu-id="00bbc-118">Compliance and Audit Database and Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="00bbc-119">Rapporti</span><span class="sxs-lookup"><span data-stu-id="00bbc-119">Reports</span></span></p></li>
<li><p><span data-ttu-id="00bbc-120">Applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="00bbc-120">Web applications</span></span></p></li>
<li><p><span data-ttu-id="00bbc-121">Topologia di integrazione di Configuration Manager (necessaria solo se si esegue MBAM con questa topologia)</span><span class="sxs-lookup"><span data-stu-id="00bbc-121">Configuration Manager Integration topology (needed only if you are running MBAM with this topology)</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="00bbc-122">Nota</span><span class="sxs-lookup"><span data-stu-id="00bbc-122">Note</span></span></strong><br/><p><span data-ttu-id="00bbc-123">Prendere nota dei nomi dei server in cui si configura ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="00bbc-123">Note the names of the servers on which you configure each feature.</span></span> <span data-ttu-id="00bbc-124">Userai queste informazioni durante il processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="00bbc-124">You will use this information throughout the configuration process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)"><span data-ttu-id="00bbc-125">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-125">Configuring the MBAM 2.5 Server Features</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-126">Convalidare la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="00bbc-126">Validate the MBAM configuration.</span></span></p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)"><span data-ttu-id="00bbc-127">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-127">Validating the MBAM 2.5 Server Feature Configuration</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-128">Copiare il modello dei criteri di gruppo di MBAM e modificare le impostazioni dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="00bbc-128">Copy the MBAM Group Policy Template and edit the Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="00bbc-129">Copiando i modelli di criteri di gruppo di MBAM 2,5 </a> e <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> modificando le impostazioni dei criteri di gruppo di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="00bbc-129">Copying the MBAM 2.5 Group Policy Templates</a> and <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="00bbc-130">Distribuire il software del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="00bbc-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="00bbc-131">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-131">Deploying the MBAM 2.5 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="00bbc-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00bbc-132">Related topics</span></span>


[<span data-ttu-id="00bbc-133">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="00bbc-133">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)




## <span data-ttu-id="00bbc-134">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="00bbc-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="00bbc-135">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="00bbc-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="00bbc-136">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="00bbc-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




