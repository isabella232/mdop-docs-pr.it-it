---
title: Come usare il sito Web di gestione e monitoraggio
description: Come usare il sito Web di gestione e monitoraggio
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804683"
---
# <span data-ttu-id="6fdad-103">Come usare il sito Web di gestione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="6fdad-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="6fdad-104">Il sito Web di amministrazione e monitoraggio, noto anche come Help desk, è un'interfaccia amministrativa per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6fdad-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="6fdad-105">Usare il sito Web per esaminare i report, recuperare le unità degli utenti finali e gestire le TPMs degli utenti finali, come descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6fdad-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="6fdad-106">**Nota**  Se si usa MBAM nella topologia autonoma, è possibile visualizzare tutti i report dal sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6fdad-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="6fdad-107">Se si usa la topologia di integrazione di Configuration Manager, è possibile visualizzare tutti i report di Configuration Manager, ad eccezione del report di controllo del ripristino, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6fdad-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="6fdad-108">Per altre informazioni sui report, vedere [monitoraggio e segnalazione della conformità di BitLocker con MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="6fdad-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="6fdad-109">Ruoli obbligatori per l'uso del sito Web amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="6fdad-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="6fdad-110">Per accedere a specifiche aree del sito Web di amministrazione e monitoraggio, è necessario avere uno dei ruoli seguenti, ovvero i gruppi creati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6fdad-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="6fdad-111">Puoi usare qualsiasi nome per questi gruppi.</span><span class="sxs-lookup"><span data-stu-id="6fdad-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6fdad-112">Account</span><span class="sxs-lookup"><span data-stu-id="6fdad-112">Account</span></span></th>
<th align="left"><span data-ttu-id="6fdad-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fdad-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fdad-114">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="6fdad-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-115">Consente di accedere a tutte le aree del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6fdad-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="6fdad-116">Gli utenti che hanno questo ruolo immettono solo la chiave di ripristino e non il nome utente e il dominio dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità.</span><span class="sxs-lookup"><span data-stu-id="6fdad-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="6fdad-117">Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti di mbam Advanced helpdesk eseguono l'override delle autorizzazioni di gruppo utenti di MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="6fdad-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fdad-118">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="6fdad-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-119">Consente di accedere alle aree Gestisci TPM e ripristino unità del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6fdad-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="6fdad-120">Gli utenti che hanno questo ruolo devono compilare tutti i campi, incluso il dominio dell'utente finale e il nome dell'account, quando usano un'area qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="6fdad-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="6fdad-121">Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti di mbam Advanced helpdesk eseguono l'override delle autorizzazioni di gruppo utenti di MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="6fdad-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fdad-122">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="6fdad-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-123">Consente di accedere ai report nell' <strong> area report </strong> del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6fdad-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6fdad-124">Attività che è possibile eseguire nel sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="6fdad-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="6fdad-125">La tabella seguente riepiloga le attività che è possibile eseguire nel sito Web di amministrazione e monitoraggio e fornisce collegamenti ad altre informazioni su ogni attività.</span><span class="sxs-lookup"><span data-stu-id="6fdad-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6fdad-126">Attività</span><span class="sxs-lookup"><span data-stu-id="6fdad-126">Task</span></span></th>
<th align="left"><span data-ttu-id="6fdad-127">Area del sito Web in cui si accede all'attività</span><span class="sxs-lookup"><span data-stu-id="6fdad-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="6fdad-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fdad-128">Description</span></span></th>
<th align="left"><span data-ttu-id="6fdad-129">Per altre informazioni</span><span class="sxs-lookup"><span data-stu-id="6fdad-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fdad-130">Visualizzare i report</span><span class="sxs-lookup"><span data-stu-id="6fdad-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-131">Rapporti</span><span class="sxs-lookup"><span data-stu-id="6fdad-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-132">Consente di eseguire report per monitorare l'utilizzo, la conformità e l'attività di ripristino della chiave di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6fdad-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="6fdad-133">I report includono dati relativi alla conformità aziendale, ai singoli computer e alle persone che hanno richiesto le chiavi di ripristino o il pacchetto OwnerAuth TPM per un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="6fdad-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="6fdad-134">Visualizzazione dei report di MBAM 2.5 per la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="6fdad-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fdad-135">Determinare lo stato di crittografia di BitLocker per i computer persi o rubati</span><span class="sxs-lookup"><span data-stu-id="6fdad-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-136">Rapporti</span><span class="sxs-lookup"><span data-stu-id="6fdad-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-137">Determinare se un volume è stato crittografato se il computer viene perso o rubato.</span><span class="sxs-lookup"><span data-stu-id="6fdad-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="6fdad-138">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="6fdad-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fdad-139">Recuperare le unità perse</span><span class="sxs-lookup"><span data-stu-id="6fdad-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-140">Ripristino unità</span><span class="sxs-lookup"><span data-stu-id="6fdad-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-141">Recuperare le unità che sono:</span><span class="sxs-lookup"><span data-stu-id="6fdad-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="6fdad-142">In modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="6fdad-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="6fdad-143">Sono stati spostati</span><span class="sxs-lookup"><span data-stu-id="6fdad-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="6fdad-144">Sono danneggiati</span><span class="sxs-lookup"><span data-stu-id="6fdad-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="6fdad-145">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="6fdad-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="6fdad-146">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="6fdad-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="6fdad-147">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="6fdad-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fdad-148">Reimpostare un blocco TPM</span><span class="sxs-lookup"><span data-stu-id="6fdad-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-149">Gestisci TPM</span><span class="sxs-lookup"><span data-stu-id="6fdad-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fdad-150">Consente di accedere ai dati del TPM raccolti dal client MBAM.</span><span class="sxs-lookup"><span data-stu-id="6fdad-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="6fdad-151">In un blocco TPM usare il sito Web amministrazione e monitoraggio per recuperare il file di password necessario per sbloccare il TPM.</span><span class="sxs-lookup"><span data-stu-id="6fdad-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="6fdad-152">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="6fdad-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="6fdad-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fdad-153">Related topics</span></span>


[<span data-ttu-id="6fdad-154">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6fdad-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="6fdad-155">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="6fdad-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6fdad-156">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="6fdad-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6fdad-157">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6fdad-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





