---
title: Informazioni sui report autonomi di MBAM 2.5
description: Informazioni sui report autonomi di MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804480"
---
# <span data-ttu-id="13beb-103">Informazioni sui report autonomi di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13beb-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="13beb-104">In questo argomento vengono descritti i report disponibili quando si esegue Microsoft BitLocker Administration and Monitoring (MBAM) nella topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="13beb-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="13beb-105">Nota</span><span class="sxs-lookup"><span data-stu-id="13beb-105">Note</span></span>**  
<span data-ttu-id="13beb-106">Se si esegue MBAM con la topologia di integrazione di Configuration Manager, è possibile generare report da Configuration Manager invece che da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="13beb-107">Per altre informazioni su questi report, vedere [visualizzazione di report di MBAM 2,5 per la topologia di integrazione di Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .</span><span class="sxs-lookup"><span data-stu-id="13beb-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="13beb-108">Informazioni sui report della topologia autonoma di MBAM</span><span class="sxs-lookup"><span data-stu-id="13beb-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="13beb-109">MBAM offre tre tipi di report che è possibile usare per monitorare l'organizzazione per la conformità a BitLocker:</span><span class="sxs-lookup"><span data-stu-id="13beb-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="13beb-110">Report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="13beb-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="13beb-111">Report conformità computer</span><span class="sxs-lookup"><span data-stu-id="13beb-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="13beb-112">Report di controllo del ripristino</span><span class="sxs-lookup"><span data-stu-id="13beb-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="13beb-113">Per accedere ai report di MBAM quando si esegue MBAM nella topologia autonoma, aprire un Web browser e quindi aprire il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="13beb-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="13beb-114">Selezionare **report** nella barra dei menu a sinistra.</span><span class="sxs-lookup"><span data-stu-id="13beb-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="13beb-115">Nella barra dei menu superiore selezionare il tipo di report che si desidera generare.</span><span class="sxs-lookup"><span data-stu-id="13beb-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="13beb-116">Per altre informazioni sulla generazione di questi report, vedere generazione di report autonomi di [MBAM 2,5](generating-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="13beb-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="13beb-117">Report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="13beb-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="13beb-118">Usare questo tipo di report per raccogliere informazioni sulla conformità complessiva di BitLocker nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="13beb-119">È possibile usare i filtri per limitare i risultati della ricerca per ottenere maggiori informazioni sullo stato di conformità e sullo stato di errore dei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="13beb-120">Panoramica sulla conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="13beb-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13beb-121">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="13beb-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="13beb-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13beb-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-123">Computer gestiti</span><span class="sxs-lookup"><span data-stu-id="13beb-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-124">Numero di computer gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-125">Conforme%</span><span class="sxs-lookup"><span data-stu-id="13beb-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-126">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-127">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="13beb-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-128">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-129">% Esenti</span><span class="sxs-lookup"><span data-stu-id="13beb-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-130">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-131">% Non esenti</span><span class="sxs-lookup"><span data-stu-id="13beb-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-132">Percentuale di computer non esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-133">Conformi</span><span class="sxs-lookup"><span data-stu-id="13beb-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-134">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-135">Non conforme</span><span class="sxs-lookup"><span data-stu-id="13beb-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-136">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-137">Esenti</span><span class="sxs-lookup"><span data-stu-id="13beb-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-138">Totale computer esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-139">Non esenti</span><span class="sxs-lookup"><span data-stu-id="13beb-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-140">Totale computer non esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13beb-141">Dettagli del computer conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="13beb-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13beb-142">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="13beb-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="13beb-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13beb-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-144">Nome computer</span><span class="sxs-lookup"><span data-stu-id="13beb-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-145">Nome DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-146">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="13beb-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-147">Nome di dominio completo in cui risiede il computer client e gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-148">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-149">Stato di conformità per il computer, in base ai criteri specificati per il computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="13beb-150">Gli Stati non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="13beb-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="13beb-151">Per altre informazioni su come interpretare gli Stati di conformità, vedere la tabella degli Stati di conformità dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="13beb-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-152">Esenzione</span><span class="sxs-lookup"><span data-stu-id="13beb-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-153">Stato che indica se il computer è esentato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-154">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-155">Messaggi di errore e di stato relativi allo stato di conformità del computer in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="13beb-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-156">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="13beb-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-157">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="13beb-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="13beb-158">La frequenza dei contatti è configurabile.</span><span class="sxs-lookup"><span data-stu-id="13beb-158">The contact frequency is configurable.</span></span> <span data-ttu-id="13beb-159">Per altre informazioni, Vedi le impostazioni dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="13beb-160">Report conformità computer</span><span class="sxs-lookup"><span data-stu-id="13beb-160">Computer Compliance Report</span></span>

<span data-ttu-id="13beb-161">Usare questo tipo di report per raccogliere informazioni specifiche per un computer o un utente.</span><span class="sxs-lookup"><span data-stu-id="13beb-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="13beb-162">Per visualizzare questo report, fare clic sul nome del computer nel report conformità aziendale oppure digitare il nome del computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="13beb-163">Questo report Mostra informazioni dettagliate sulla crittografia di ogni unità (sistema operativo e unità dati fisse) in un computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="13beb-164">Indica anche il criterio applicato a ogni tipo di unità nel computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="13beb-165">Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="13beb-166">Nota</span><span class="sxs-lookup"><span data-stu-id="13beb-166">Note</span></span>**  
<span data-ttu-id="13beb-167">Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.</span><span class="sxs-lookup"><span data-stu-id="13beb-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="13beb-168">Campi rapporto conformità computer</span><span class="sxs-lookup"><span data-stu-id="13beb-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13beb-169">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="13beb-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="13beb-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13beb-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-171">Nome computer</span><span class="sxs-lookup"><span data-stu-id="13beb-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-172">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-173">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="13beb-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-174">Nome di dominio completo in cui risiede il computer client e gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-175">Tipo di computer</span><span class="sxs-lookup"><span data-stu-id="13beb-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-176">Tipo di computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-176">Type of computer.</span></span> <span data-ttu-id="13beb-177">I tipi validi non sono portatili e portatili.</span><span class="sxs-lookup"><span data-stu-id="13beb-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-178">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="13beb-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-179">Tipo di sistema operativo trovato nel computer client gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-180">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-181">Stato di conformità generale del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="13beb-182">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="13beb-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="13beb-183">Si noti che lo stato di conformità per unità (vedere la tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="13beb-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="13beb-184">Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="13beb-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-185">Intensità cifratura criteri</span><span class="sxs-lookup"><span data-stu-id="13beb-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-186">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM (ad esempio, 128 bit con diffusore).</span><span class="sxs-lookup"><span data-stu-id="13beb-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-187">Unità del sistema operativo dei criteri</span><span class="sxs-lookup"><span data-stu-id="13beb-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-188">Indica se è necessaria la crittografia per il sistema operativo e Mostra il tipo di protezione appropriato.</span><span class="sxs-lookup"><span data-stu-id="13beb-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-189">Criteri-unità dati fissata</span><span class="sxs-lookup"><span data-stu-id="13beb-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-190">Indica se è necessaria la crittografia per l'unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="13beb-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-191">Unità dati rimovibili dei criteri</span><span class="sxs-lookup"><span data-stu-id="13beb-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-192">Indica se è necessaria la crittografia per l'unità rimovibile.</span><span class="sxs-lookup"><span data-stu-id="13beb-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-193">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="13beb-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-194">Utenti noti nel computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-195">Esenzione</span><span class="sxs-lookup"><span data-stu-id="13beb-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-196">Stato che indica se il computer è esentato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-197">Produttore</span><span class="sxs-lookup"><span data-stu-id="13beb-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-198">Nome del produttore del computer, come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-199">Modello</span><span class="sxs-lookup"><span data-stu-id="13beb-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-200">Nome del modello del produttore del computer, come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="13beb-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-201">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-202">Messaggi di errore e di stato relativi allo stato di conformità del computer, in conformità con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="13beb-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-203">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="13beb-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-204">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="13beb-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="13beb-205">La frequenza dei contatti è configurabile.</span><span class="sxs-lookup"><span data-stu-id="13beb-205">The contact frequency is configurable.</span></span> <span data-ttu-id="13beb-206">Per altre informazioni, Vedi le impostazioni dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13beb-207">Campi unità report conformità computer</span><span class="sxs-lookup"><span data-stu-id="13beb-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13beb-208">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="13beb-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="13beb-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13beb-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-210">Lettera di unità</span><span class="sxs-lookup"><span data-stu-id="13beb-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-211">Lettera dell'unità del computer assegnata all'unità specifica dall'utente.</span><span class="sxs-lookup"><span data-stu-id="13beb-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-212">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="13beb-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-213">Tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="13beb-213">Type of drive.</span></span> <span data-ttu-id="13beb-214">I valori validi sono unità di sistema operativo e unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="13beb-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="13beb-215">Si tratta di unità fisiche anziché di volumi logici.</span><span class="sxs-lookup"><span data-stu-id="13beb-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-216">Intensità cifratura</span><span class="sxs-lookup"><span data-stu-id="13beb-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-217">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="13beb-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-218">Tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="13beb-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-219">Tipo di protezione selezionata tramite l'impostazione di criteri di gruppo utilizzata per crittografare un sistema operativo o un volume di dati fisso.</span><span class="sxs-lookup"><span data-stu-id="13beb-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-220">Stato Protector</span><span class="sxs-lookup"><span data-stu-id="13beb-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-221">Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="13beb-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="13beb-222">Gli stati validi sono attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="13beb-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-223">Stato di crittografia</span><span class="sxs-lookup"><span data-stu-id="13beb-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-224">Stato di crittografia dell'unità.</span><span class="sxs-lookup"><span data-stu-id="13beb-224">Encryption state of the drive.</span></span> <span data-ttu-id="13beb-225">Gli stati validi sono crittografati, non crittografati e crittografati.</span><span class="sxs-lookup"><span data-stu-id="13beb-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-226">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-227">Stato che indica se l'unità è conforme ai criteri.</span><span class="sxs-lookup"><span data-stu-id="13beb-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="13beb-228">Gli Stati non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="13beb-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-229">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="13beb-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-230">Messaggi di errore e di stato dello stato di conformità del computer, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="13beb-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="13beb-231">Report di controllo del ripristino</span><span class="sxs-lookup"><span data-stu-id="13beb-231">Recovery Audit Report</span></span>

<span data-ttu-id="13beb-232">Usare questo tipo di report per controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="13beb-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="13beb-233">Il report offre diversi filtri in base ai criteri di filtro desiderati.</span><span class="sxs-lookup"><span data-stu-id="13beb-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="13beb-234">È possibile filtrare in base a un tipo specifico di utente (un utente dell'help desk o un utente finale), se la richiesta non è riuscita o ha avuto esito positivo, il tipo specifico di chiave richiesta e un intervallo di date durante il quale si è verificato il recupero.</span><span class="sxs-lookup"><span data-stu-id="13beb-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="13beb-235">Campi rapporto di controllo ripristino</span><span class="sxs-lookup"><span data-stu-id="13beb-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13beb-236">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="13beb-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="13beb-237">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13beb-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-238">Richiedere data e ora</span><span class="sxs-lookup"><span data-stu-id="13beb-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-239">Data e ora in cui una richiesta di recupero tasti è stata effettuata da un utente finale o da un utente dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="13beb-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-240">Origine della richiesta di controllo</span><span class="sxs-lookup"><span data-stu-id="13beb-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-241">Il sito da cui è stata avviata la richiesta.</span><span class="sxs-lookup"><span data-stu-id="13beb-241">The site from which the request was initiated.</span></span> <span data-ttu-id="13beb-242">Questa voce avrà uno dei due valori seguenti: <strong> portale self-service </strong> o <strong> helpdesk </strong> .</span><span class="sxs-lookup"><span data-stu-id="13beb-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-243">Stato della richiesta</span><span class="sxs-lookup"><span data-stu-id="13beb-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-244">Stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="13beb-244">Status of the request.</span></span> <span data-ttu-id="13beb-245">Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</span><span class="sxs-lookup"><span data-stu-id="13beb-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-246">Utente helpdesk</span><span class="sxs-lookup"><span data-stu-id="13beb-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-247">Utente dell'help desk che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="13beb-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="13beb-248">Nota</span><span class="sxs-lookup"><span data-stu-id="13beb-248">Note</span></span></strong><br/><p><span data-ttu-id="13beb-249">Se un utente di helpdesk avanzato ripristina la chiave senza specificare l'utente finale, il <strong> campo utente finale </strong> sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="13beb-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="13beb-250">Un utente di helpdesk standard deve specificare l'utente finale e l'utente verrà visualizzato in questo campo.</span><span class="sxs-lookup"><span data-stu-id="13beb-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="13beb-251">Un recupero tramite il portale self-service elenca l'utente finale richiedente sia in questo campo che nel <strong> campo utente finale </strong> .</span><span class="sxs-lookup"><span data-stu-id="13beb-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-252">Utente finale</span><span class="sxs-lookup"><span data-stu-id="13beb-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-253">Utente finale che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="13beb-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-254">Computer</span><span class="sxs-lookup"><span data-stu-id="13beb-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-255">Nome computer del computer recuperato.</span><span class="sxs-lookup"><span data-stu-id="13beb-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13beb-256">Tipo di chiave</span><span class="sxs-lookup"><span data-stu-id="13beb-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-257">Tipo di chiave richiesto dall'utente dell'help desk o dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="13beb-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="13beb-258">I tre tipi di chiavi che MBAM raccoglie sono:</span><span class="sxs-lookup"><span data-stu-id="13beb-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="13beb-259">Password chiave di ripristino (usata per recuperare un computer in modalità di ripristino)</span><span class="sxs-lookup"><span data-stu-id="13beb-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="13beb-260">ID chiave di ripristino (usato per recuperare un computer in modalità di ripristino per conto di un altro utente)</span><span class="sxs-lookup"><span data-stu-id="13beb-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="13beb-261">Hash della password TPM (usato per recuperare un computer con un TPM bloccato)</span><span class="sxs-lookup"><span data-stu-id="13beb-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13beb-262">Descrizione motivo</span><span class="sxs-lookup"><span data-stu-id="13beb-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="13beb-263">Motivo per cui il tipo di chiave specificato è stato richiesto dall'utente dell'help desk o dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="13beb-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="13beb-264">I motivi sono specificati nelle funzionalità di recupero unità e Gestisci TPM del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="13beb-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="13beb-265">Le voci valide sono testo immesso dall'utente o uno dei codici motivo seguenti:</span><span class="sxs-lookup"><span data-stu-id="13beb-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="13beb-266">Modifica dell'ordine di avvio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="13beb-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="13beb-267">BIOS modificato</span><span class="sxs-lookup"><span data-stu-id="13beb-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="13beb-268">File di sistema operativo modificati</span><span class="sxs-lookup"><span data-stu-id="13beb-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="13beb-269">Tasto di avvio perduto</span><span class="sxs-lookup"><span data-stu-id="13beb-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="13beb-270">PIN perduto</span><span class="sxs-lookup"><span data-stu-id="13beb-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="13beb-271">Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="13beb-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="13beb-272">Passphrase smarrita</span><span class="sxs-lookup"><span data-stu-id="13beb-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="13beb-273">Smartcard persa</span><span class="sxs-lookup"><span data-stu-id="13beb-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="13beb-274">Reimposta blocco PIN</span><span class="sxs-lookup"><span data-stu-id="13beb-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="13beb-275">Attivare il TPM</span><span class="sxs-lookup"><span data-stu-id="13beb-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="13beb-276">Disattivare TPM</span><span class="sxs-lookup"><span data-stu-id="13beb-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="13beb-277">Modificare la password del TPM</span><span class="sxs-lookup"><span data-stu-id="13beb-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="13beb-278">Cancellare TPM</span><span class="sxs-lookup"><span data-stu-id="13beb-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13beb-279">Nota</span><span class="sxs-lookup"><span data-stu-id="13beb-279">Note</span></span>**  
<span data-ttu-id="13beb-280">I risultati del report possono essere salvati in un file facendo clic sul pulsante **Esporta** nella barra dei menu **report** .</span><span class="sxs-lookup"><span data-stu-id="13beb-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="13beb-281">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13beb-281">Related topics</span></span>


[<span data-ttu-id="13beb-282">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13beb-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="13beb-283">Generazione di report autonomi di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13beb-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="13beb-284">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="13beb-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="13beb-285">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="13beb-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="13beb-286">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="13beb-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





