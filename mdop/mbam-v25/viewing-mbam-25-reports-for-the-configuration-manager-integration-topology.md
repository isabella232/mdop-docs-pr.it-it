---
title: Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager
description: Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824045"
---
# <span data-ttu-id="f41c4-103">Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f41c4-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="f41c4-104">Questo argomento descrive i report disponibili quando si configura Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f41c4-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f41c4-105">I report mostrano la conformità di BitLocker per l'organizzazione e per i singoli computer e dispositivi gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="f41c4-106">I report contengono informazioni tabulari e grafici e contengono filtri che consentono di visualizzare i dati da prospettive diverse.</span><span class="sxs-lookup"><span data-stu-id="f41c4-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="f41c4-107">Nella topologia di integrazione di Configuration Manager è possibile visualizzare i report di Configuration Manager invece che dal sito Web di amministrazione e monitoraggio, ad eccezione del **report di controllo del ripristino**, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f41c4-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f41c4-108">Per informazioni sui report MBAM per la topologia autonoma, vedere [visualizzazione di report di mbam 2,5 per la topologia](viewing-mbam-25-reports-for-the-stand-alone-topology.md)autonoma.</span><span class="sxs-lookup"><span data-stu-id="f41c4-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="f41c4-109">Accesso ai report in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f41c4-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="f41c4-110">Per accedere alla funzionalità report in Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="f41c4-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-111">Versione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f41c4-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="f41c4-112">Come visualizzare i report</span><span class="sxs-lookup"><span data-stu-id="f41c4-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-113">ConfigurationManager di SystemCenter2012</span><span class="sxs-lookup"><span data-stu-id="f41c4-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f41c4-114">Nel riquadro sinistro selezionare l'area di <strong> </strong> lavoro monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f41c4-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="f41c4-115">Nell'albero, espandere <strong> Panoramica </strong> &gt; <strong> </strong> &gt; <strong> report </strong> &gt; <strong> mbam </strong> .</span><span class="sxs-lookup"><span data-stu-id="f41c4-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f41c4-116">Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="f41c4-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-117">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f41c4-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f41c4-118">Nel riquadro sinistro espandere <strong> Gestione computer </strong> &gt; <strong> Reporting </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; report nome server &gt; </strong> &gt; <strong> cartella </strong> &gt; <strong> mbam </strong> .</span><span class="sxs-lookup"><span data-stu-id="f41c4-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f41c4-119">Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="f41c4-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f41c4-120">Descrizione dei report in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f41c4-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="f41c4-121">Esistono alcune differenze minime nei report per la topologia di integrazione di Configuration Manager e per la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="f41c4-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="f41c4-122">Nelle sezioni seguenti vengono descritti i dati nei report di MBAM per la topologia di integrazione di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="f41c4-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="f41c4-123">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="f41c4-124">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="f41c4-125">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="f41c4-126">Report conformità computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="f41c4-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="f41c4-127">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="f41c4-128">Il dashboard conformità Enterprise di BitLocker offre i grafici seguenti, che mostrano lo stato di conformità di BitLocker nell'organizzazione:</span><span class="sxs-lookup"><span data-stu-id="f41c4-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="f41c4-129">Distribuzione dello stato di conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="f41c4-130">Distribuzione di errori non conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="f41c4-131">Distribuzione dello stato di conformità per tipo di unità</span><span class="sxs-lookup"><span data-stu-id="f41c4-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="f41c4-132">Distribuzione dello stato di conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="f41c4-133">Questo grafico a torta mostra lo stato di conformità per i computer all'interno dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="f41c4-134">Viene inoltre visualizzata la percentuale di computer, in confronto al numero totale di computer della raccolta selezionata, con lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="f41c4-135">Viene visualizzato anche il numero effettivo di computer con ogni stato.</span><span class="sxs-lookup"><span data-stu-id="f41c4-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="f41c4-136">Il grafico a torta Mostra gli Stati di conformità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f41c4-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="f41c4-137">Conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-137">Compliant</span></span>

-   <span data-ttu-id="f41c4-138">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-138">Non Compliant</span></span>

-   <span data-ttu-id="f41c4-139">Esenzione dall'utente</span><span class="sxs-lookup"><span data-stu-id="f41c4-139">User Exempt</span></span>

-   <span data-ttu-id="f41c4-140">Esenzione dall'utente temporaneo</span><span class="sxs-lookup"><span data-stu-id="f41c4-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="f41c4-141">Criteri non applicati</span><span class="sxs-lookup"><span data-stu-id="f41c4-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="f41c4-142">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f41c4-142">Unknown.</span></span> <span data-ttu-id="f41c4-143">Questo computer ha segnalato un errore di stato o fa parte della raccolta, ma non ha mai segnalato lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="f41c4-144">Se il computer è disconnesso dall'organizzazione, potrebbe verificarsi la mancanza di uno stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="f41c4-145">Distribuzione di errori non conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="f41c4-146">Questo grafico a torta mostra le categorie di computer dell'organizzazione che non sono conformi ai criteri di crittografia unità BitLocker e Mostra il numero di computer in ogni categoria.</span><span class="sxs-lookup"><span data-stu-id="f41c4-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="f41c4-147">Ogni percentuale di categoria viene calcolata a partire dal numero totale di computer non conformi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f41c4-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="f41c4-148">Crittografia rimandata dall'utente</span><span class="sxs-lookup"><span data-stu-id="f41c4-148">User postponed encryption</span></span>

-   <span data-ttu-id="f41c4-149">Non è possibile trovare TPM compatibile</span><span class="sxs-lookup"><span data-stu-id="f41c4-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="f41c4-150">Partizione di sistema non disponibile o abbastanza grande</span><span class="sxs-lookup"><span data-stu-id="f41c4-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="f41c4-151">Conflitto di criteri</span><span class="sxs-lookup"><span data-stu-id="f41c4-151">Policy conflict</span></span>

-   <span data-ttu-id="f41c4-152">Attesa del provisioning automatico del TPM</span><span class="sxs-lookup"><span data-stu-id="f41c4-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="f41c4-153">Si è verificato un errore sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f41c4-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="f41c4-154">Nessuna informazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-154">No information.</span></span> <span data-ttu-id="f41c4-155">Questi computer non hanno installato il client MBAM, o hanno installato il client MBAM, ma non attivato (ad esempio, il servizio non funziona).</span><span class="sxs-lookup"><span data-stu-id="f41c4-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="f41c4-156">Distribuzione dello stato di conformità per tipo di unità</span><span class="sxs-lookup"><span data-stu-id="f41c4-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="f41c4-157">Questo grafico a barre Mostra lo stato di conformità corrente di BitLocker per tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="f41c4-158">Gli Stati sono **conformi** e **non conformi**.</span><span class="sxs-lookup"><span data-stu-id="f41c4-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="f41c4-159">Le barre vengono visualizzate per le unità dati fisse e le unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f41c4-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="f41c4-160">I computer che non dispongono di un'unità dati fissa sono inclusi e visualizzano un valore solo nella barra dell' **unità del sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="f41c4-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="f41c4-161">Il grafico non include gli utenti a cui è stata concessa un'esenzione dal criterio di crittografia unità BitLocker o dalla categoria nessun criterio.</span><span class="sxs-lookup"><span data-stu-id="f41c4-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="f41c4-162">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="f41c4-163">Questo report Mostra le informazioni sulla conformità complessiva di BitLocker nell'organizzazione per la raccolta di computer mirati per l'uso di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="f41c4-164">Campi dettagli conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="f41c4-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-165">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="f41c4-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f41c4-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-167">Computer gestiti</span><span class="sxs-lookup"><span data-stu-id="f41c4-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-168">Numero di computer gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-169">Conforme%</span><span class="sxs-lookup"><span data-stu-id="f41c4-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-170">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-171">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-172">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-173">% Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f41c4-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-174">Percentuale di computer con uno stato di conformità non noto.</span><span class="sxs-lookup"><span data-stu-id="f41c4-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-175">% Esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-176">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-177">% Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-178">Percentuale di computer non esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-179">Conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-180">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-181">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-182">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-183">Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f41c4-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-184">Percentuale di computer con uno stato di conformità non noto.</span><span class="sxs-lookup"><span data-stu-id="f41c4-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-185">Esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-186">Totale computer esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-187">Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-188">Totale computer non esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f41c4-189">Stati dei dettagli di conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="f41c4-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-190">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="f41c4-191">Esenzione</span><span class="sxs-lookup"><span data-stu-id="f41c4-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="f41c4-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-193">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-194">Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-195">Il computer non è conforme, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-196">Conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-197">Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-198">Il computer è conforme ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="f41c4-199">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="f41c4-200">Usare questo tipo di report per visualizzare informazioni sulla conformità complessiva di BitLocker nell'organizzazione e per mostrare la conformità per i singoli computer presenti nella raccolta di computer destinati all'uso di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="f41c4-201">Campi di riepilogo conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="f41c4-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-202">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="f41c4-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f41c4-203">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-204">Computer gestiti</span><span class="sxs-lookup"><span data-stu-id="f41c4-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-205">Numero di computer gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-206">Conforme%</span><span class="sxs-lookup"><span data-stu-id="f41c4-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-207">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-208">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-209">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-210">% Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f41c4-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-211">Percentuale di computer con uno stato di conformità non noto.</span><span class="sxs-lookup"><span data-stu-id="f41c4-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-212">% Esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-213">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-214">% Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-215">Percentuale di computer non esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-216">Conformi</span><span class="sxs-lookup"><span data-stu-id="f41c4-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-217">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-218">Non conforme</span><span class="sxs-lookup"><span data-stu-id="f41c4-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-219">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-220">Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f41c4-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-221">Percentuale di computer con uno stato di conformità non noto.</span><span class="sxs-lookup"><span data-stu-id="f41c4-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-222">Esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-223">Totale computer esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-224">Non esenti</span><span class="sxs-lookup"><span data-stu-id="f41c4-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-225">Totale computer non esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f41c4-226">Dettagli del computer di riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f41c4-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-227">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="f41c4-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f41c4-228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-229">Nome computer</span><span class="sxs-lookup"><span data-stu-id="f41c4-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-230">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-231">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="f41c4-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-232">Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-233">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-234">Stato complessivo di conformità del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="f41c4-235">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f41c4-236">Si noti che lo stato di conformità per unità (Vedi la tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="f41c4-237">Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-238">Esenzione</span><span class="sxs-lookup"><span data-stu-id="f41c4-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-239">Stato che indica se l'utente è esonerato o non è esentato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-240">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="f41c4-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-241">Utente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f41c4-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-242">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-243">Messaggi di errore e di stato relativi allo stato di conformità del computer in conformità con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-244">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="f41c4-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-245">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f41c4-246">La frequenza dei contatti può essere configurata tramite le impostazioni dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f41c4-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="f41c4-247">Report conformità computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="f41c4-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="f41c4-248">Usare questo tipo di report per raccogliere informazioni specifiche di un computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="f41c4-249">Il report conformità computer BitLocker fornisce informazioni dettagliate sulla crittografia di ogni unità in un computer (sistema operativo e unità dati fisse).</span><span class="sxs-lookup"><span data-stu-id="f41c4-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="f41c4-250">Fornisce anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="f41c4-251">Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="f41c4-252">**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.</span><span class="sxs-lookup"><span data-stu-id="f41c4-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="f41c4-253">Report conformità computer BitLocker: campi dettagli computer</span><span class="sxs-lookup"><span data-stu-id="f41c4-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-254">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="f41c4-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f41c4-255">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-256">Nome computer</span><span class="sxs-lookup"><span data-stu-id="f41c4-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-257">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-258">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="f41c4-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-259">Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-260">Tipo di computer</span><span class="sxs-lookup"><span data-stu-id="f41c4-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-261">Tipo di computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-261">Type of computer.</span></span> <span data-ttu-id="f41c4-262">I tipi validi non sono portatili e portatili.</span><span class="sxs-lookup"><span data-stu-id="f41c4-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-263">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f41c4-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-264">Tipo di sistema operativo disponibile nel computer client di MBAM Managed.</span><span class="sxs-lookup"><span data-stu-id="f41c4-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-265">Conformità complessiva</span><span class="sxs-lookup"><span data-stu-id="f41c4-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-266">Stato complessivo di conformità del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="f41c4-267">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f41c4-268">Si noti che lo stato di conformità per unità (Vedi la tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="f41c4-269">Tuttavia, questo campo rappresenta lo stato di conformità in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-270">Conformità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f41c4-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-271">Stato di conformità del sistema operativo gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="f41c4-272">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-273">Conformità con l'unità dati fissa</span><span class="sxs-lookup"><span data-stu-id="f41c4-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-274">Stato di conformità dell'unità dati fissa gestita da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="f41c4-275">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="f41c4-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-276">Data ultimo aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f41c4-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-277">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f41c4-278">La frequenza dei contatti può essere configurata tramite le impostazioni dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f41c4-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-279">Esenzione</span><span class="sxs-lookup"><span data-stu-id="f41c4-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-280">Stato che indica se l'utente è esonerato o non è esentato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-281">Utente esentato</span><span class="sxs-lookup"><span data-stu-id="f41c4-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-282">Utente che è esonerato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f41c4-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-283">Data di esenzione</span><span class="sxs-lookup"><span data-stu-id="f41c4-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-284">Data in cui è stata concessa l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="f41c4-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-285">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="f41c4-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-286">Messaggi di errore e di stato relativi allo stato di conformità del computer in conformità con i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-287">Intensità cifratura criteri</span><span class="sxs-lookup"><span data-stu-id="f41c4-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-288">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri MBAM, ad esempio 128 bit con diffusore.</span><span class="sxs-lookup"><span data-stu-id="f41c4-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-289">Criteri: unità di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f41c4-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-290">Indica se è necessaria la crittografia per il sistema operativo e per il tipo di protezione appropriato.</span><span class="sxs-lookup"><span data-stu-id="f41c4-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-291">Criteri: unità dati fissa</span><span class="sxs-lookup"><span data-stu-id="f41c4-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-292">Indica se è necessaria la crittografia per l'unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="f41c4-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-293">Produttore</span><span class="sxs-lookup"><span data-stu-id="f41c4-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-294">Nome del produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-295">Modello</span><span class="sxs-lookup"><span data-stu-id="f41c4-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-296">Nome del modello del produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="f41c4-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-297">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="f41c4-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-298">Utenti noti nel computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f41c4-299">Report conformità computer BitLocker: campi volume computer</span><span class="sxs-lookup"><span data-stu-id="f41c4-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f41c4-300">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="f41c4-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f41c4-301">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f41c4-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-302">Lettera di unità</span><span class="sxs-lookup"><span data-stu-id="f41c4-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-303">Lettera dell'unità del computer assegnata all'unità specifica dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f41c4-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-304">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="f41c4-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-305">Tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-305">Type of drive.</span></span> <span data-ttu-id="f41c4-306">I valori validi sono unità di sistema operativo e unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="f41c4-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f41c4-307">Si tratta di unità fisiche anziché di volumi logici.</span><span class="sxs-lookup"><span data-stu-id="f41c4-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-308">Intensità cifratura</span><span class="sxs-lookup"><span data-stu-id="f41c4-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-309">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="f41c4-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-310">Tipi di protezione</span><span class="sxs-lookup"><span data-stu-id="f41c4-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-311">Tipo di protezione selezionata tramite il criterio usato per crittografare un sistema operativo o un'unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="f41c4-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="f41c4-312">I tipi di protezione validi per un sistema operativo sono TPM o TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="f41c4-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="f41c4-313">Il tipo di protezione valido per un'unità dati fissa è una password.</span><span class="sxs-lookup"><span data-stu-id="f41c4-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f41c4-314">Stato Protector</span><span class="sxs-lookup"><span data-stu-id="f41c4-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-315">Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="f41c4-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="f41c4-316">Gli stati validi sono attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="f41c4-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f41c4-317">Stato di crittografia</span><span class="sxs-lookup"><span data-stu-id="f41c4-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f41c4-318">Stato di crittografia dell'unità.</span><span class="sxs-lookup"><span data-stu-id="f41c4-318">Encryption state of the drive.</span></span> <span data-ttu-id="f41c4-319">Gli stati validi sono crittografati, non crittografati e crittografati.</span><span class="sxs-lookup"><span data-stu-id="f41c4-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f41c4-320">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f41c4-320">Related topics</span></span>


[<span data-ttu-id="f41c4-321">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f41c4-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="f41c4-322">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="f41c4-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f41c4-323">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f41c4-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f41c4-324">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f41c4-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





