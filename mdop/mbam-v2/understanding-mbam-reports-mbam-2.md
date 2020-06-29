---
title: Informazioni sui report di MBAM
description: Informazioni sui report di MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823815"
---
# <span data-ttu-id="429de-103">Informazioni sui report di MBAM</span><span class="sxs-lookup"><span data-stu-id="429de-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="429de-104">Se si è scelta la topologia autonoma quando è stato installato Microsoft BitLocker Administration and Monitoring (MBAM), è possibile eseguire report diversi in MBAM per monitorare l'uso e la conformità di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="429de-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="429de-105">MBAM riporta la conformità e altre informazioni su tutti i computer e i dispositivi gestiti.</span><span class="sxs-lookup"><span data-stu-id="429de-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="429de-106">Le informazioni contenute in questo argomento possono essere usate per comprendere i report di amministrazione e monitoraggio di Microsoft BitLocker per le aziende e la conformità dei singoli computer e per l'attività di ripristino delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="429de-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="429de-107">**Nota**  Se si è scelta la topologia di Configuration Manager quando è stato installato Microsoft BitLocker Administration and Monitoring (MBAM), i report vengono generati da Configuration Manager invece che da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="429de-108">Per altre informazioni sui report eseguiti da Configuration Manager, vedere Concetti relativi [ai report di mbam in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="429de-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="429de-109">Informazioni sui report</span><span class="sxs-lookup"><span data-stu-id="429de-109">Understanding Reports</span></span>


<span data-ttu-id="429de-110">Per accedere alla caratteristica report di amministrazione e monitoraggio di Microsoft BitLocker, aprire un Web browser e aprire il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="429de-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="429de-111">Selezionare **report** nella barra dei menu a sinistra e quindi selezionare una delle opzioni che si desidera generare nella barra del menu superiore.</span><span class="sxs-lookup"><span data-stu-id="429de-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="429de-112">Report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="429de-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="429de-113">Usare questo tipo di report per raccogliere informazioni sulla conformità complessiva di BitLocker nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="429de-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="429de-114">Puoi usare filtri diversi per limitare i risultati della ricerca allo stato di conformità e allo stato di errore.</span><span class="sxs-lookup"><span data-stu-id="429de-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="429de-115">Le informazioni del report vengono aggiornate ogni sei ore.</span><span class="sxs-lookup"><span data-stu-id="429de-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="429de-116">Campi rapporto conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="429de-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="429de-117">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="429de-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="429de-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429de-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-119">Nome computer</span><span class="sxs-lookup"><span data-stu-id="429de-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-120">Nome DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-121">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="429de-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-122">Nome di dominio completo in cui risiede il computer client e gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-123">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="429de-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-124">Stato di conformità per il computer, in base ai criteri specificati per il computer.</span><span class="sxs-lookup"><span data-stu-id="429de-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="429de-125">Gli Stati non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="429de-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="429de-126">Per altre informazioni su come interpretare gli Stati di conformità, vedere la tabella Stati di conformità del report conformità aziendale.</span><span class="sxs-lookup"><span data-stu-id="429de-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-127">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="429de-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-128">Messaggi di errore e di stato dello stato di conformità del computer in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-129">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="429de-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-130">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="429de-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="429de-131">La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</span><span class="sxs-lookup"><span data-stu-id="429de-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="429de-132">Stati di conformità del report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="429de-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="429de-133">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="429de-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="429de-134">Esenzione</span><span class="sxs-lookup"><span data-stu-id="429de-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="429de-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429de-135">Description</span></span></th>
<th align="left"><span data-ttu-id="429de-136">Azione utente</span><span class="sxs-lookup"><span data-stu-id="429de-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-137">Non conforme</span><span class="sxs-lookup"><span data-stu-id="429de-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-138">Non esenti</span><span class="sxs-lookup"><span data-stu-id="429de-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-139">Il computer non è conforme, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-140">Espandere i dettagli del report di conformità del computer facendo clic su <strong> nome computer </strong> e determinare se lo stato di ogni unità è conforme ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="429de-141">Se lo stato di crittografia indica che il computer non è crittografato, è possibile che la crittografia sia in corso oppure si verifichi un errore nel computer.</span><span class="sxs-lookup"><span data-stu-id="429de-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="429de-142">Se non è presente alcun errore, la causa probabile è che il computer sia ancora in fase di connessione o di determinazione dello stato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="429de-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="429de-143">Controllare più avanti per determinare se lo stato cambia.</span><span class="sxs-lookup"><span data-stu-id="429de-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-144">Conformi</span><span class="sxs-lookup"><span data-stu-id="429de-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-145">Non esenti</span><span class="sxs-lookup"><span data-stu-id="429de-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-146">Il computer è conforme, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-147">Nessuna azione necessaria; lo stato del computer può essere confermato visualizzando il report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="429de-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="429de-148">Report conformità computer</span><span class="sxs-lookup"><span data-stu-id="429de-148">Computer Compliance Report</span></span>

<span data-ttu-id="429de-149">Usare questo tipo di report per raccogliere informazioni specifiche per un computer o un utente.</span><span class="sxs-lookup"><span data-stu-id="429de-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="429de-150">Questo report può essere visualizzato facendo clic sul nome del computer nel report conformità aziendale oppure digitando il nome del computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="429de-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="429de-151">Il report conformità computer fornisce informazioni dettagliate sulla crittografia per ogni unità (sistema operativo e unità dati fisse) in un computer e anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer.</span><span class="sxs-lookup"><span data-stu-id="429de-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="429de-152">Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.</span><span class="sxs-lookup"><span data-stu-id="429de-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="429de-153">**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non verrà visualizzato nel report.</span><span class="sxs-lookup"><span data-stu-id="429de-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="429de-154">Campi rapporto conformità computer</span><span class="sxs-lookup"><span data-stu-id="429de-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="429de-155">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="429de-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="429de-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429de-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-157">Nome computer</span><span class="sxs-lookup"><span data-stu-id="429de-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-158">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-159">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="429de-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-160">Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-161">Tipo di computer</span><span class="sxs-lookup"><span data-stu-id="429de-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-162">Tipo di computer.</span><span class="sxs-lookup"><span data-stu-id="429de-162">Type of computer.</span></span> <span data-ttu-id="429de-163">I tipi validi non sono portatili e portatili.</span><span class="sxs-lookup"><span data-stu-id="429de-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-164">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="429de-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-165">Tipo di sistema operativo disponibile nel computer client di MBAM-Managed.</span><span class="sxs-lookup"><span data-stu-id="429de-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-166">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="429de-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-167">Stato complessivo di conformità del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="429de-168">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="429de-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="429de-169">Si noti che lo stato di conformità per unità (vedere la tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="429de-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="429de-170">Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-171">Intensità cifratura criteri</span><span class="sxs-lookup"><span data-stu-id="429de-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-172">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM (ad esempio, 128 bit con diffusore).</span><span class="sxs-lookup"><span data-stu-id="429de-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-173">Unità del sistema operativo dei criteri</span><span class="sxs-lookup"><span data-stu-id="429de-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-174">Indica se è necessaria la crittografia per il sistema operativo e Mostra il tipo di protezione appropriato.</span><span class="sxs-lookup"><span data-stu-id="429de-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-175">Criteri-unità dati fissata</span><span class="sxs-lookup"><span data-stu-id="429de-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-176">Indica se è necessaria la crittografia per l'unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="429de-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-177">Unità dati rimovibili dei criteri</span><span class="sxs-lookup"><span data-stu-id="429de-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-178">Indica se è necessaria la crittografia per l'unità rimovibile.</span><span class="sxs-lookup"><span data-stu-id="429de-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-179">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="429de-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-180">Utenti noti nel computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-181">Produttore</span><span class="sxs-lookup"><span data-stu-id="429de-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-182">Nome del produttore del computer, come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="429de-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-183">Modello</span><span class="sxs-lookup"><span data-stu-id="429de-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-184">Nome del modello del produttore del computer, come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="429de-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-185">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="429de-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-186">Messaggi di errore e di stato dello stato di conformità del computer, in conformità con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-187">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="429de-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-188">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="429de-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="429de-189">La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</span><span class="sxs-lookup"><span data-stu-id="429de-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="429de-190">Campi unità report conformità computer</span><span class="sxs-lookup"><span data-stu-id="429de-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="429de-191">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="429de-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="429de-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429de-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-193">Lettera di unità</span><span class="sxs-lookup"><span data-stu-id="429de-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-194">Lettera dell'unità del computer assegnata all'unità specifica dall'utente.</span><span class="sxs-lookup"><span data-stu-id="429de-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-195">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="429de-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-196">Tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="429de-196">Type of drive.</span></span> <span data-ttu-id="429de-197">I valori validi sono unità di sistema operativo e unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="429de-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="429de-198">Si tratta di unità fisiche anziché di volumi logici.</span><span class="sxs-lookup"><span data-stu-id="429de-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-199">Intensità cifratura</span><span class="sxs-lookup"><span data-stu-id="429de-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-200">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="429de-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-201">Tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="429de-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-202">Tipo di protezione selezionata tramite il criterio usato per crittografare un sistema operativo o un volume di dati fisso.</span><span class="sxs-lookup"><span data-stu-id="429de-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-203">Stato Protector</span><span class="sxs-lookup"><span data-stu-id="429de-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-204">Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="429de-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="429de-205">Gli stati validi sono attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="429de-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-206">Stato di crittografia</span><span class="sxs-lookup"><span data-stu-id="429de-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-207">Stato di crittografia dell'unità.</span><span class="sxs-lookup"><span data-stu-id="429de-207">Encryption state of the drive.</span></span> <span data-ttu-id="429de-208">Gli stati validi sono crittografati, non crittografati e crittografati.</span><span class="sxs-lookup"><span data-stu-id="429de-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-209">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="429de-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-210">Stato che indica se l'unità è conforme ai criteri.</span><span class="sxs-lookup"><span data-stu-id="429de-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="429de-211">Gli Stati non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="429de-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-212">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="429de-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-213">Messaggi di errore e di stato dello stato di conformità del computer, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="429de-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="429de-214">Report di controllo del ripristino</span><span class="sxs-lookup"><span data-stu-id="429de-214">Recovery Audit Report</span></span>

<span data-ttu-id="429de-215">Usare questo tipo di report per controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="429de-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="429de-216">Il report offre diversi filtri in base ai criteri di filtro desiderati.</span><span class="sxs-lookup"><span data-stu-id="429de-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="429de-217">Gli utenti possono filtrare in base a un tipo specifico di utente, un utente dell'help desk o un utente finale, se la richiesta non è riuscita o ha avuto esito positivo, il tipo specifico di chiave richiesta e un intervallo di date durante il quale si è verificato il recupero.</span><span class="sxs-lookup"><span data-stu-id="429de-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="429de-218">L'amministratore può produrre report contestuali in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="429de-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="429de-219">Campi rapporto di controllo ripristino</span><span class="sxs-lookup"><span data-stu-id="429de-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="429de-220">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="429de-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="429de-221">Descrizione</span><span class="sxs-lookup"><span data-stu-id="429de-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-222">Richiedere data e ora</span><span class="sxs-lookup"><span data-stu-id="429de-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-223">Data e ora in cui una richiesta di recupero tasti è stata effettuata da un utente finale o da un utente dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="429de-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-224">Stato della richiesta</span><span class="sxs-lookup"><span data-stu-id="429de-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-225">Stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="429de-225">Status of the request.</span></span> <span data-ttu-id="429de-226">Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</span><span class="sxs-lookup"><span data-stu-id="429de-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-227">Utente helpdesk</span><span class="sxs-lookup"><span data-stu-id="429de-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-228">Utente dell'help desk che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="429de-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="429de-229">Nota: se l'utente dell'help desk recupera la chiave per conto di un utente finale, il campo utente finale sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="429de-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-230">Utente</span><span class="sxs-lookup"><span data-stu-id="429de-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-231">Utente finale che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="429de-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="429de-232">Tipo di chiave</span><span class="sxs-lookup"><span data-stu-id="429de-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-233">Tipo di chiave richiesto dall'utente dell'help desk o dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="429de-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="429de-234">I tre tipi di chiavi che MBAM raccoglie sono: password chiave di ripristino (usata per il ripristino di un computer in modalità di ripristino), ID chiave di ripristino (usata per recuperare un computer in modalità di ripristino per conto di un altro utente) e hash della password del TPM (usato per recuperare un computer con un TPM bloccato).</span><span class="sxs-lookup"><span data-stu-id="429de-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="429de-235">Descrizione motivo</span><span class="sxs-lookup"><span data-stu-id="429de-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="429de-236">Motivo per cui il tipo di chiave specificato è stato richiesto dall'utente dell'help desk o dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="429de-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="429de-237">I motivi sono specificati nelle funzionalità di recupero unità e Gestisci TPM del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="429de-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="429de-238">Le voci valide sono testo immesso dall'utente o uno dei codici motivo seguenti:</span><span class="sxs-lookup"><span data-stu-id="429de-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="429de-239">Modifica dell'ordine di avvio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="429de-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="429de-240">BIOS modificato</span><span class="sxs-lookup"><span data-stu-id="429de-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="429de-241">File di sistema operativo modificati</span><span class="sxs-lookup"><span data-stu-id="429de-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="429de-242">Tasto di avvio perduto</span><span class="sxs-lookup"><span data-stu-id="429de-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="429de-243">PIN perduto</span><span class="sxs-lookup"><span data-stu-id="429de-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="429de-244">Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="429de-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="429de-245">Passphrase smarrita</span><span class="sxs-lookup"><span data-stu-id="429de-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="429de-246">Smartcard persa</span><span class="sxs-lookup"><span data-stu-id="429de-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="429de-247">Reimposta blocco PIN</span><span class="sxs-lookup"><span data-stu-id="429de-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="429de-248">Attivare il TPM</span><span class="sxs-lookup"><span data-stu-id="429de-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="429de-249">Disattivare TPM</span><span class="sxs-lookup"><span data-stu-id="429de-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="429de-250">Modificare la password del TPM</span><span class="sxs-lookup"><span data-stu-id="429de-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="429de-251">Cancellare TPM</span><span class="sxs-lookup"><span data-stu-id="429de-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="429de-252">**Nota**  I risultati del report possono essere salvati in un file facendo clic sul pulsante **Esporta** nella barra dei menu report.</span><span class="sxs-lookup"><span data-stu-id="429de-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="429de-253">Per altre informazioni su come eseguire i report di MBAM, vedere [come generare report di mbam](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="429de-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="429de-254">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="429de-254">Related topics</span></span>


[<span data-ttu-id="429de-255">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="429de-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





