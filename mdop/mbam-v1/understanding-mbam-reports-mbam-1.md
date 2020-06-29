---
title: Informazioni sui report di MBAM
description: Informazioni sui report di MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822866"
---
# <span data-ttu-id="c20df-103">Informazioni sui report di MBAM</span><span class="sxs-lookup"><span data-stu-id="c20df-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="c20df-104">Microsoft BitLocker Administration and Monitoring (MBAM) genera diversi report per monitorare l'uso e la conformità di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c20df-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="c20df-105">Questo argomento descrive i report di MBAM per conformità aziendali, singoli computer, compatibilità hardware e attività di ripristino delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="c20df-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="c20df-106">Informazioni sui report</span><span class="sxs-lookup"><span data-stu-id="c20df-106">Understanding Reports</span></span>


<span data-ttu-id="c20df-107">Per accedere alla caratteristica report di MBAM, aprire il sito Web di amministrazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="c20df-108">Selezionare **report** nel riquadro di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c20df-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="c20df-109">Nel riquadro contenuto principale fare clic sulla scheda relativa al tipo di report: **report conformità aziendale**, report **conformità computer**, **report controllo hardware**o **rapporto di controllo del ripristino**.</span><span class="sxs-lookup"><span data-stu-id="c20df-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="c20df-110">Report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="c20df-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="c20df-111">Un report di conformità aziendale fornisce informazioni sulla conformità complessiva di BitLocker nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c20df-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="c20df-112">I filtri disponibili per questo report consentono di limitare i risultati della ricerca in base allo stato di conformità e allo stato di errore.</span><span class="sxs-lookup"><span data-stu-id="c20df-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="c20df-113">Questo report viene eseguito ogni sei ore.</span><span class="sxs-lookup"><span data-stu-id="c20df-113">This report runs every six hours.</span></span>

**<span data-ttu-id="c20df-114">Campi rapporto conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="c20df-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-115">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="c20df-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c20df-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-117">Nome computer</span><span class="sxs-lookup"><span data-stu-id="c20df-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-118">Il nome DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-119">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="c20df-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-120">Il nome di dominio completo in cui risiede il computer client e viene gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-121">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-122">Lo stato di conformità per il computer, in base ai criteri specificati per il computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="c20df-123">Gli stati possibili non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="c20df-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="c20df-124">Per altre informazioni, vedere Stati di conformità del report conformità aziendale in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c20df-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-125">Esenzione</span><span class="sxs-lookup"><span data-stu-id="c20df-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-126">Lo stato dell'hardware del computer per determinare l'identificazione del tipo di hardware e se il computer è esentato dai criteri.</span><span class="sxs-lookup"><span data-stu-id="c20df-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="c20df-127">Ci sono tre possibili stati: hardware sconosciuto (il tipo di hardware non è stato identificato da MBAM), l'hardware è esentato (il tipo di hardware è stato identificato ed è stato contrassegnato come esentato dai criteri di MBAM) e non è esentato (l'hardware è stato identificato e non è esentato dai criteri).</span><span class="sxs-lookup"><span data-stu-id="c20df-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-128">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="c20df-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-129">Utenti noti nel computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-130">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-131">Messaggi di errore e di stato relativi allo stato di conformità del computer in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c20df-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-132">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="c20df-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-133">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="c20df-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c20df-134">Questa volta è configurabile.</span><span class="sxs-lookup"><span data-stu-id="c20df-134">This time is configurable.</span></span> <span data-ttu-id="c20df-135">Vedi impostazioni dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c20df-136">Stati di conformità del report conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="c20df-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-137">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="c20df-138">Esenzione</span><span class="sxs-lookup"><span data-stu-id="c20df-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="c20df-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-139">Description</span></span></th>
<th align="left"><span data-ttu-id="c20df-140">Azione utente</span><span class="sxs-lookup"><span data-stu-id="c20df-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-141">Non conforme</span><span class="sxs-lookup"><span data-stu-id="c20df-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-142">Non esenti</span><span class="sxs-lookup"><span data-stu-id="c20df-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-143">Il computer non è conforme ai criteri specificati e il tipo di hardware non è stato indicato come esenti da criteri.</span><span class="sxs-lookup"><span data-stu-id="c20df-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-144">Fare clic su <strong> nome computer </strong> per espandere il report conformità computer e determinare se lo stato di ogni unità è conforme ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c20df-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="c20df-145">Se lo stato di crittografia indica che il computer non è crittografato, la crittografia potrebbe essere ancora in corso oppure potrebbe esserci un errore nel computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="c20df-146">Se non è presente alcun errore, la causa probabile è che il computer sia ancora in fase di connessione o di determinazione dello stato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="c20df-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="c20df-147">Controllare più avanti per determinare se lo stato cambia.</span><span class="sxs-lookup"><span data-stu-id="c20df-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-148">Conformi</span><span class="sxs-lookup"><span data-stu-id="c20df-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-149">Non esenti</span><span class="sxs-lookup"><span data-stu-id="c20df-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-150">Il computer è conforme ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c20df-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-151">Non è necessaria alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="c20df-151">No Action needed.</span></span> <span data-ttu-id="c20df-152">Facoltativamente, è possibile visualizzare il report conformità computer per confermare lo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-153">Conformi</span><span class="sxs-lookup"><span data-stu-id="c20df-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-154">Componenti hardware esenti</span><span class="sxs-lookup"><span data-stu-id="c20df-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-155">Se il tipo di hardware è esonerato.</span><span class="sxs-lookup"><span data-stu-id="c20df-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="c20df-156">Indipendentemente dal modo in cui è impostato il criterio o dallo stato individuale di ogni disco rigido, lo stato complessivo viene considerato conforme.</span><span class="sxs-lookup"><span data-stu-id="c20df-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-157">Non è necessaria alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="c20df-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-158">Conformi</span><span class="sxs-lookup"><span data-stu-id="c20df-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-159">Hardware sconosciuto</span><span class="sxs-lookup"><span data-stu-id="c20df-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-160">MBAM riconosce il tipo di hardware, ma MBAM non sa se è esentasse o non è esonerato.</span><span class="sxs-lookup"><span data-stu-id="c20df-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="c20df-161">Questo problema si verifica se l'amministratore non ha impostato lo stato compatibile per l'hardware.</span><span class="sxs-lookup"><span data-stu-id="c20df-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="c20df-162">Di conseguenza, MBAM ripristina lo stato di conformità per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c20df-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-163">Questo è lo stato iniziale di un client MBAM appena distribuito.</span><span class="sxs-lookup"><span data-stu-id="c20df-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="c20df-164">Si tratta in genere solo di uno stato temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c20df-164">It is typically only a transient state.</span></span> <span data-ttu-id="c20df-165">Anche se l'amministratore ha contrassegnato l'hardware come compatibile, può essere necessario un ritardo significativo o un tempo di attesa configurabile prima che il computer client ritorni.</span><span class="sxs-lookup"><span data-stu-id="c20df-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="c20df-166">Prendere nota dell'ora dell'ultimo contatto ed eseguire di nuovo il check-in dopo l'intervallo specificato per verificare se lo stato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="c20df-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="c20df-167">Se lo stato non è stato modificato, potrebbe essersi verificato un errore per il computer o il tipo di hardware.</span><span class="sxs-lookup"><span data-stu-id="c20df-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c20df-168">Report conformità computer</span><span class="sxs-lookup"><span data-stu-id="c20df-168">Computer Compliance Report</span></span>

<span data-ttu-id="c20df-169">Il report conformità computer Visualizza le informazioni specifiche di un computer o un utente.</span><span class="sxs-lookup"><span data-stu-id="c20df-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="c20df-170">Il report conformità computer offre informazioni dettagliate sulla crittografia e i criteri applicabili per ogni unità di un computer, incluse le unità del sistema operativo e le unità dati fisse.</span><span class="sxs-lookup"><span data-stu-id="c20df-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="c20df-171">Per visualizzare questo tipo di report, fare clic sul nome del computer nel report conformità aziendale oppure digitare il nome del computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="c20df-172">Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="c20df-173">**Nota**  Questo report non offre lo stato di crittografia per i volumi di dati rimovibili.</span><span class="sxs-lookup"><span data-stu-id="c20df-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="c20df-174">Campi rapporto conformità computer</span><span class="sxs-lookup"><span data-stu-id="c20df-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-175">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="c20df-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c20df-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-177">Nome computer</span><span class="sxs-lookup"><span data-stu-id="c20df-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-178">Il nome del computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-179">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="c20df-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-180">Il nome di dominio completo in cui risiede il computer client e viene gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-181">Tipo di computer</span><span class="sxs-lookup"><span data-stu-id="c20df-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-182">Tipo di portabilità del computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-182">The portability type of computer.</span></span> <span data-ttu-id="c20df-183">I tipi validi non sono portatili e portatili.</span><span class="sxs-lookup"><span data-stu-id="c20df-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-184">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c20df-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-185">Tipo di sistema operativo installato nel computer client gestito MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-186">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-187">Lo stato di conformità complessivo del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="c20df-188">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="c20df-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="c20df-189">Mentre è possibile avere unità conformi e non conformi nello stesso computer, questo campo indica la conformità complessiva del computer per ogni criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="c20df-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-190">Forza di Cypher dei criteri</span><span class="sxs-lookup"><span data-stu-id="c20df-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-191">La forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="c20df-192">Ad esempio, 128 bit con il diffusore</span><span class="sxs-lookup"><span data-stu-id="c20df-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-193">Unità del sistema operativo dei criteri</span><span class="sxs-lookup"><span data-stu-id="c20df-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-194">Indica se è necessaria la crittografia per l'O/S e il tipo di protezione, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="c20df-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-195">Unità dati fissata per i criteri</span><span class="sxs-lookup"><span data-stu-id="c20df-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-196">Indica se è necessaria la crittografia per l'unità fissa.</span><span class="sxs-lookup"><span data-stu-id="c20df-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-197">Unità dati rimovibili dei criteri</span><span class="sxs-lookup"><span data-stu-id="c20df-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-198">Indica se è necessaria la crittografia per l'unità rimovibile.</span><span class="sxs-lookup"><span data-stu-id="c20df-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-199">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="c20df-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-200">Fornisce l'identità degli utenti noti nel computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-201">Esenzione</span><span class="sxs-lookup"><span data-stu-id="c20df-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-202">Indica se il tipo di hardware del computer è riconosciuto da MBAM e, se noto, se il computer è stato indicato come esenti da criteri.</span><span class="sxs-lookup"><span data-stu-id="c20df-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="c20df-203">Ci sono tre stati: hardware sconosciuto (il tipo di hardware non è stato identificato da MBAM); Hardware esenti (il tipo di hardware è stato identificato ed è stato contrassegnato come esenti dai criteri di MBAM); e non esenti (l'hardware è stato identificato e non è esentato dai criteri).</span><span class="sxs-lookup"><span data-stu-id="c20df-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-204">Produttore</span><span class="sxs-lookup"><span data-stu-id="c20df-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-205">Nome del produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-206">Modello</span><span class="sxs-lookup"><span data-stu-id="c20df-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-207">Nome del modello di produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-208">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-209">Messaggi di errore e di stato dello stato di conformità del computer in conformità con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c20df-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-210">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="c20df-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-211">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="c20df-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="c20df-212">T</span><span class="sxs-lookup"><span data-stu-id="c20df-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c20df-213">Campi unità report conformità computer</span><span class="sxs-lookup"><span data-stu-id="c20df-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-214">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="c20df-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c20df-215">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-216">Lettera di unità</span><span class="sxs-lookup"><span data-stu-id="c20df-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-217">Lettera dell'unità del computer assegnata a questa specifica unità dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c20df-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-218">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="c20df-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-219">Tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="c20df-219">Type of drive.</span></span> <span data-ttu-id="c20df-220">I valori validi sono unità di sistema operativo e unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="c20df-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="c20df-221">Si tratta di unità fisiche anziché di volumi logici.</span><span class="sxs-lookup"><span data-stu-id="c20df-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-222">Forza di cifratura</span><span class="sxs-lookup"><span data-stu-id="c20df-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-223">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c20df-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-224">Tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="c20df-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-225">Tipo di protezione selezionata tramite criteri usati per crittografare un sistema operativo o un volume fisso.</span><span class="sxs-lookup"><span data-stu-id="c20df-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="c20df-226">I tipi di protezione validi in un'unità del sistema operativo sono TPM o TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="c20df-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="c20df-227">L'unico tipo di protezione valido per un volume di dati fisso è la password.</span><span class="sxs-lookup"><span data-stu-id="c20df-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-228">Stato Protector</span><span class="sxs-lookup"><span data-stu-id="c20df-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-229">Questo campo indica se il computer ha abilitato il tipo di protezione specificato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="c20df-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="c20df-230">Gli stati validi sono attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="c20df-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-231">Stato di crittografia</span><span class="sxs-lookup"><span data-stu-id="c20df-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-232">Questo è lo stato di crittografia corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="c20df-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="c20df-233">Gli stati validi sono crittografati, non crittografati e crittografati.</span><span class="sxs-lookup"><span data-stu-id="c20df-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-234">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-235">Indica se l'unità è conforme ai criteri.</span><span class="sxs-lookup"><span data-stu-id="c20df-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="c20df-236">Gli Stati non sono conformi e conforme.</span><span class="sxs-lookup"><span data-stu-id="c20df-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-237">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="c20df-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-238">Contiene messaggi di errore e di stato relativi allo stato di conformità del computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c20df-239">Report di controllo hardware</span><span class="sxs-lookup"><span data-stu-id="c20df-239">Hardware Audit Report</span></span>

<span data-ttu-id="c20df-240">Questo report consente di controllare le modifiche apportate allo stato di compatibilità hardware di specifiche funzionalità e modelli di computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="c20df-241">Per limitare i risultati della ricerca, questo report include l'applicazione di filtri ai criteri, ad esempio il tipo di modifica e l'ora dell'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="c20df-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="c20df-242">Ogni modifica dello stato viene rilevata dall'utente e dalla data e dall'ora.</span><span class="sxs-lookup"><span data-stu-id="c20df-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="c20df-243">Il tipo di hardware viene automaticamente compilato dall'agente MBAM che viene eseguito nel computer client.</span><span class="sxs-lookup"><span data-stu-id="c20df-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="c20df-244">Questo report consente di tenere traccia delle modifiche apportate dall'utente alle informazioni raccolte direttamente da MBAM Managed computer.</span><span class="sxs-lookup"><span data-stu-id="c20df-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="c20df-245">Una tipica modifica amministrativa cambia da compatibile a non compatibile.</span><span class="sxs-lookup"><span data-stu-id="c20df-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="c20df-246">Tuttavia, l'amministratore può anche rivedere qualsiasi campo.</span><span class="sxs-lookup"><span data-stu-id="c20df-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="c20df-247">Campi rapporto di controllo hardware</span><span class="sxs-lookup"><span data-stu-id="c20df-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-248">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="c20df-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c20df-249">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-250">Data e ora</span><span class="sxs-lookup"><span data-stu-id="c20df-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-251">Data e ora in cui è stata apportata una modifica al tipo di hardware.</span><span class="sxs-lookup"><span data-stu-id="c20df-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="c20df-252">Tieni presente che ogni tipo di hardware univoco viene assegnato ad almeno una voce.</span><span class="sxs-lookup"><span data-stu-id="c20df-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-253">Utente</span><span class="sxs-lookup"><span data-stu-id="c20df-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-254">Utente amministrativo che ha apportato la modifica per la voce specifica.</span><span class="sxs-lookup"><span data-stu-id="c20df-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-255">Tipo di modifica</span><span class="sxs-lookup"><span data-stu-id="c20df-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-256">Tipo di modifica apportata alle informazioni sul tipo di hardware.</span><span class="sxs-lookup"><span data-stu-id="c20df-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="c20df-257">I valori validi sono addizione (nuova voce), aggiornamento (modifica voce esistente) o eliminazione (Rimuovi voce esistente).</span><span class="sxs-lookup"><span data-stu-id="c20df-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-258">Valore originale</span><span class="sxs-lookup"><span data-stu-id="c20df-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-259">Valore della specifica del tipo di hardware prima che venisse apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="c20df-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-260">Valore corrente</span><span class="sxs-lookup"><span data-stu-id="c20df-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-261">Valore della specifica del tipo di hardware dopo che è stata apportata la modifica.</span><span class="sxs-lookup"><span data-stu-id="c20df-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c20df-262">Report di controllo del ripristino</span><span class="sxs-lookup"><span data-stu-id="c20df-262">Recovery Audit Report</span></span>

<span data-ttu-id="c20df-263">Il report di controllo del recupero consente di controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c20df-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="c20df-264">I criteri di filtro per questo report includono il tipo di utente che effettua la richiesta, il tipo di chiave richiesta, l'ora dell'occorrenza, l'esito positivo o negativo, l'ora dell'occorrenza e il tipo di richiesta dell'utente (Help desk, utente finale).</span><span class="sxs-lookup"><span data-stu-id="c20df-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="c20df-265">Questo report consente agli amministratori di produrre report contestuali in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c20df-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="c20df-266">Campi rapporto di controllo ripristino</span><span class="sxs-lookup"><span data-stu-id="c20df-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c20df-267">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="c20df-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="c20df-268">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20df-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-269">Richiedere data e ora</span><span class="sxs-lookup"><span data-stu-id="c20df-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-270">La data e l'ora in cui una richiesta di recupero tasti è stata effettuata da un utente finale o da un utente dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="c20df-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-271">Stato della richiesta</span><span class="sxs-lookup"><span data-stu-id="c20df-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-272">Stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="c20df-272">Status of the request.</span></span> <span data-ttu-id="c20df-273">Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</span><span class="sxs-lookup"><span data-stu-id="c20df-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-274">Utente helpdesk</span><span class="sxs-lookup"><span data-stu-id="c20df-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-275">L'utente dell'help desk che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="c20df-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="c20df-276">Se l'utente dell'help desk recupera la chiave per conto di un utente finale, il campo utente finale sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="c20df-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-277">Utente</span><span class="sxs-lookup"><span data-stu-id="c20df-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-278">L'utente finale che ha avviato la richiesta di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="c20df-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c20df-279">Tipo di chiave</span><span class="sxs-lookup"><span data-stu-id="c20df-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-280">Il tipo di chiave richiesto.</span><span class="sxs-lookup"><span data-stu-id="c20df-280">The type of key that was requested.</span></span> <span data-ttu-id="c20df-281">MBAM raccoglie tre tipi di chiave: password chiave di ripristino (per il ripristino di un computer in modalità di ripristino); ID chiave di ripristino (per recuperare un computer in modalità di ripristino per conto di un altro utente); e hash della password Trusted Platform Module (TPM) (per recuperare un computer con un TPM bloccato).</span><span class="sxs-lookup"><span data-stu-id="c20df-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c20df-282">Descrizione motivo</span><span class="sxs-lookup"><span data-stu-id="c20df-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="c20df-283">Il motivo per cui è stato richiesto il tipo di chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="c20df-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="c20df-284">I motivi sono specificati nelle funzionalità di recupero unità e Gestisci TPM del sito Web amministrativo.</span><span class="sxs-lookup"><span data-stu-id="c20df-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="c20df-285">Le voci valide includono il testo immesso dall'utente o uno dei codici motivo seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20df-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="c20df-286">Modifica dell'ordine di avvio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c20df-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="c20df-287">BIOS modificato</span><span class="sxs-lookup"><span data-stu-id="c20df-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="c20df-288">File di sistema operativo modificati</span><span class="sxs-lookup"><span data-stu-id="c20df-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="c20df-289">Tasto di avvio perduto</span><span class="sxs-lookup"><span data-stu-id="c20df-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="c20df-290">PIN perduto</span><span class="sxs-lookup"><span data-stu-id="c20df-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="c20df-291">Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="c20df-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="c20df-292">Passphrase smarrita</span><span class="sxs-lookup"><span data-stu-id="c20df-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="c20df-293">Smartcard persa</span><span class="sxs-lookup"><span data-stu-id="c20df-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="c20df-294">Reimposta blocco PIN</span><span class="sxs-lookup"><span data-stu-id="c20df-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="c20df-295">Attivare il TPM</span><span class="sxs-lookup"><span data-stu-id="c20df-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="c20df-296">Disattivare TPM</span><span class="sxs-lookup"><span data-stu-id="c20df-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="c20df-297">Modificare la password del TPM</span><span class="sxs-lookup"><span data-stu-id="c20df-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="c20df-298">Cancellare TPM</span><span class="sxs-lookup"><span data-stu-id="c20df-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c20df-299">**Nota**  Per salvare i risultati del report in un file, fare clic sul pulsante **Esporta** nella barra dei menu report.</span><span class="sxs-lookup"><span data-stu-id="c20df-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="c20df-300">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c20df-300">Related topics</span></span>


[<span data-ttu-id="c20df-301">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c20df-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





