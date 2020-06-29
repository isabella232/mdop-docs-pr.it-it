---
title: Informazioni sui report di MBAM in Configuration Manager
description: Informazioni sui report di MBAM in Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823825"
---
# <span data-ttu-id="0427c-103">Informazioni sui report di MBAM in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0427c-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="0427c-104">Quando Microsoft BitLocker Administration and Monitoring (MBAM) viene installato con la topologia integrata di Configuration Manager, le caratteristiche di conformità e Reporting hardware vengono spostate nell'infrastruttura di Configuration Manager e fuori da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="0427c-105">Quando si usa la topologia di Configuration Manager, è possibile eseguire report da Configuration Manager invece che da MBAM, ad eccezione del report di controllo di ripristino, a cui si continua ad accedere tramite il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0427c-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0427c-106">I report per la topologia integrata di Configuration Manager mostrano la conformità di BitLocker per l'organizzazione e per i singoli computer e dispositivi gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="0427c-107">I report offrono sia le informazioni tabulari che i grafici e consentono di filtrare i report per visualizzare i dati da prospettive diverse.</span><span class="sxs-lookup"><span data-stu-id="0427c-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="0427c-108">Le informazioni contenute in questo argomento descrivono i report di MBAM eseguiti da Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0427c-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="0427c-109">Per informazioni sui report di MBAM per la topologia autonoma, vedere Concetti relativi ai [report di mbam](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="0427c-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="0427c-110">Accesso ai report in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0427c-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="0427c-111">Per accedere alla funzionalità report in Configuration Manager, aprire la **console di Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="0427c-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="0427c-112">Per visualizzare l'elenco dei report disponibili:</span><span class="sxs-lookup"><span data-stu-id="0427c-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="0427c-113">In Configuration Manager 2007 espandere il nodo **Gestione computer** e quindi espandere il nodo **report** .</span><span class="sxs-lookup"><span data-stu-id="0427c-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="0427c-114">In SystemCenter2012 ConfigurationManager, nell'area di lavoro monitoraggio in **Panoramica**, espandere il nodo **report** e quindi fare clic su **report**.</span><span class="sxs-lookup"><span data-stu-id="0427c-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="0427c-115">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="0427c-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="0427c-116">Il dashboard conformità Enterprise di BitLocker offre i grafici seguenti, che mostrano lo stato di conformità di BitLocker nell'organizzazione:</span><span class="sxs-lookup"><span data-stu-id="0427c-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="0427c-117">Distribuzione dello stato di conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="0427c-118">Distribuzione di errori non conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="0427c-119">Distribuzione dello stato di conformità per tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0427c-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="0427c-120">Distribuzione dello stato di conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="0427c-121">Questo grafico a torta mostra lo stato di conformità del computer all'interno dell'organizzazione e Mostra la percentuale di computer, in confronto al numero totale di computer della raccolta selezionata, che hanno lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="0427c-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="0427c-122">Viene visualizzato anche il numero effettivo di computer con ogni stato.</span><span class="sxs-lookup"><span data-stu-id="0427c-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="0427c-123">Il grafico a torta Mostra gli Stati di conformità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0427c-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="0427c-124">Conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-124">Compliant</span></span>

-   <span data-ttu-id="0427c-125">Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-125">Non Compliant</span></span>

-   <span data-ttu-id="0427c-126">Esenzione dall'utente</span><span class="sxs-lookup"><span data-stu-id="0427c-126">User Exempt</span></span>

-   <span data-ttu-id="0427c-127">Esenzione dall'utente temporaneo</span><span class="sxs-lookup"><span data-stu-id="0427c-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="0427c-128">Criteri non applicati</span><span class="sxs-lookup"><span data-stu-id="0427c-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="0427c-129">Unknown: i computer il cui stato è stato segnalato come errore o i dispositivi che fanno parte della raccolta, ma che non hanno mai segnalato lo stato di conformità, ad esempio se sono disconnessi dall'organizzazione</span><span class="sxs-lookup"><span data-stu-id="0427c-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="0427c-130">Distribuzione di errori non conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="0427c-131">Questo grafico a torta mostra le categorie di computer dell'organizzazione che non sono conformi ai criteri di crittografia unità BitLocker e Mostra il numero di computer in ogni categoria.</span><span class="sxs-lookup"><span data-stu-id="0427c-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="0427c-132">Ogni percentuale di categoria viene calcolata a partire dal numero totale di computer non conformi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0427c-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="0427c-133">Crittografia rimandata dall'utente</span><span class="sxs-lookup"><span data-stu-id="0427c-133">User postponed encryption</span></span>

-   <span data-ttu-id="0427c-134">Non è possibile trovare TPM compatibile</span><span class="sxs-lookup"><span data-stu-id="0427c-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="0427c-135">Partizione di sistema non disponibile o abbastanza grande</span><span class="sxs-lookup"><span data-stu-id="0427c-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="0427c-136">Conflitto di criteri</span><span class="sxs-lookup"><span data-stu-id="0427c-136">Policy conflict</span></span>

-   <span data-ttu-id="0427c-137">Attesa del provisioning automatico del TPM</span><span class="sxs-lookup"><span data-stu-id="0427c-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="0427c-138">Si è verificato un errore sconosciuto</span><span class="sxs-lookup"><span data-stu-id="0427c-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="0427c-139">Nessuna informazione-computer che non hanno installato il client MBAM o che hanno installato il client MBAM, ma non attivato, ad esempio, il servizio non funziona</span><span class="sxs-lookup"><span data-stu-id="0427c-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="0427c-140">Distribuzione dello stato di conformità per tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0427c-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="0427c-141">Questo grafico a barre Mostra lo stato di conformità corrente di BitLocker per tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="0427c-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="0427c-142">Lo stato è "conforme" e "non conforme".</span><span class="sxs-lookup"><span data-stu-id="0427c-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="0427c-143">Le barre vengono visualizzate per le unità dati fisse e le unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0427c-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="0427c-144">I computer che non dispongono di un'unità dati fissa sono inclusi e visualizzano un valore solo nella barra dell'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0427c-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="0427c-145">Il grafico non include gli utenti a cui è stata concessa un'esenzione dal criterio di crittografia unità BitLocker o dalla categoria "nessun criterio".</span><span class="sxs-lookup"><span data-stu-id="0427c-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="0427c-146">Report dettagli conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="0427c-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="0427c-147">Questo report Mostra le informazioni sulla conformità complessiva di BitLocker nell'organizzazione per la raccolta di computer mirati per l'uso di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="0427c-148">Campi rapporto Dettagli conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="0427c-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-149">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="0427c-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="0427c-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-151">Computer gestiti</span><span class="sxs-lookup"><span data-stu-id="0427c-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-152">Numero di computer gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-153">Conforme%</span><span class="sxs-lookup"><span data-stu-id="0427c-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-154">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-155">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-156">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-157">% Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="0427c-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-158">Percentuale di computer il cui stato di conformità non è noto.</span><span class="sxs-lookup"><span data-stu-id="0427c-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-159">% Esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-160">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-161">% Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-162">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-163">Conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-164">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-165">Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-166">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-167">Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="0427c-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-168">Percentuale di computer il cui stato di conformità non è noto.</span><span class="sxs-lookup"><span data-stu-id="0427c-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-169">Esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-170">Totale computer esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-171">Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-172">Totale computer non esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="0427c-173">Report dettagli conformità di BitLocker Enterprise-stati di conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-174">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="0427c-175">Esenzione</span><span class="sxs-lookup"><span data-stu-id="0427c-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="0427c-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-177">Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-178">Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-179">Il computer non è conforme, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-180">Conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-181">Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-182">Il computer è conforme ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0427c-183">Report di riepilogo conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="0427c-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="0427c-184">Usare questo tipo di report per visualizzare informazioni sulla conformità complessiva di BitLocker nell'organizzazione e per mostrare la conformità per i singoli computer presenti nella raccolta di computer destinati all'uso di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="0427c-185">Campi rapporto di riepilogo conformità Enterprise di BitLocker</span><span class="sxs-lookup"><span data-stu-id="0427c-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-186">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="0427c-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="0427c-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-188">Computer gestiti</span><span class="sxs-lookup"><span data-stu-id="0427c-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-189">Numero di computer gestiti da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-190">Conforme%</span><span class="sxs-lookup"><span data-stu-id="0427c-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-191">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-192">% Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-193">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-194">% Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="0427c-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-195">Percentuale di computer il cui stato di conformità non è noto.</span><span class="sxs-lookup"><span data-stu-id="0427c-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-196">% Esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-197">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-198">% Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-199">Percentuale di computer esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-200">Conformi</span><span class="sxs-lookup"><span data-stu-id="0427c-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-201">Percentuale di computer conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-202">Non conforme</span><span class="sxs-lookup"><span data-stu-id="0427c-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-203">Percentuale di computer non conformi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0427c-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-204">Conformità sconosciuta</span><span class="sxs-lookup"><span data-stu-id="0427c-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-205">Percentuale di computer il cui stato di conformità non è noto.</span><span class="sxs-lookup"><span data-stu-id="0427c-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-206">Esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-207">Totale computer esenti dal requisito di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-208">Non esenti</span><span class="sxs-lookup"><span data-stu-id="0427c-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-209">Totale computer non esenti dal requisito di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="0427c-210">Report di riepilogo conformità aziendale di BitLocker-dettagli computer</span><span class="sxs-lookup"><span data-stu-id="0427c-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-211">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="0427c-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="0427c-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-213">Nome computer</span><span class="sxs-lookup"><span data-stu-id="0427c-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-214">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-215">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="0427c-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-216">Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-217">Stato conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-218">Stato complessivo di conformità del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="0427c-219">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="0427c-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="0427c-220">Si noti che lo stato di conformità per unità (Vedi tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="0427c-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="0427c-221">Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-222">Esenzione</span><span class="sxs-lookup"><span data-stu-id="0427c-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-223">Stato che indica se l'utente è esonerato o non esonerato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-224">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="0427c-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-225">Utente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0427c-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-226">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-227">Messaggi di errore e di stato dello stato di conformità del computer in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-228">Ultimo contatto</span><span class="sxs-lookup"><span data-stu-id="0427c-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-229">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="0427c-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="0427c-230">La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</span><span class="sxs-lookup"><span data-stu-id="0427c-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0427c-231">Report conformità computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="0427c-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="0427c-232">Usare questo tipo di report per raccogliere informazioni specifiche di un computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="0427c-233">Il report conformità computer fornisce informazioni dettagliate sulla crittografia per ogni unità (sistema operativo e unità dati fisse) in un computer e anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="0427c-234">Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="0427c-235">**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.</span><span class="sxs-lookup"><span data-stu-id="0427c-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="0427c-236">Report conformità computer BitLocker-campi dettagli computer</span><span class="sxs-lookup"><span data-stu-id="0427c-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-237">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="0427c-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="0427c-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-239">Nome computer</span><span class="sxs-lookup"><span data-stu-id="0427c-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-240">Nome computer DNS specificato dall'utente gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-241">Nome di dominio</span><span class="sxs-lookup"><span data-stu-id="0427c-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-242">Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-243">Tipo di computer</span><span class="sxs-lookup"><span data-stu-id="0427c-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-244">Tipo di computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-244">Type of computer.</span></span> <span data-ttu-id="0427c-245">I tipi validi non sono portatili e portatili.</span><span class="sxs-lookup"><span data-stu-id="0427c-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-246">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0427c-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-247">Tipo di sistema operativo disponibile nel computer client di MBAM Managed.</span><span class="sxs-lookup"><span data-stu-id="0427c-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-248">Conformità complessiva</span><span class="sxs-lookup"><span data-stu-id="0427c-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-249">Stato complessivo di conformità del computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="0427c-250">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="0427c-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="0427c-251">Si noti che lo stato di conformità per unità (Vedi tabella seguente) può indicare stati di conformità diversi.</span><span class="sxs-lookup"><span data-stu-id="0427c-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="0427c-252">Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-253">Conformità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0427c-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-254">Stato di conformità del sistema operativo gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="0427c-255">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="0427c-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-256">Conformità con l'unità dati fissa</span><span class="sxs-lookup"><span data-stu-id="0427c-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-257">Stato di conformità dell'unità dati fissa gestita da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="0427c-258">Gli stati validi sono conformi e conformi.</span><span class="sxs-lookup"><span data-stu-id="0427c-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-259">Data ultimo aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0427c-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-260">Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="0427c-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="0427c-261">La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</span><span class="sxs-lookup"><span data-stu-id="0427c-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-262">Esenzione</span><span class="sxs-lookup"><span data-stu-id="0427c-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-263">Stato che indica se l'utente è esonerato o non esonerato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-264">Utente esentato</span><span class="sxs-lookup"><span data-stu-id="0427c-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-265">Utente che è esonerato dai criteri di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0427c-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-266">Data di esenzione</span><span class="sxs-lookup"><span data-stu-id="0427c-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-267">Data in cui è stata concessa l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="0427c-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-268">Dettagli sullo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="0427c-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-269">Messaggi di errore e di stato dello stato di conformità del computer in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="0427c-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-270">Intensità cifratura criteri</span><span class="sxs-lookup"><span data-stu-id="0427c-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-271">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="0427c-272">(ad esempio, 128 bit con il diffusore).</span><span class="sxs-lookup"><span data-stu-id="0427c-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-273">Criteri: unità di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0427c-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-274">Indica se è necessaria la crittografia per l'O/S e il tipo di protezione appropriato.</span><span class="sxs-lookup"><span data-stu-id="0427c-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-275">Criteri: unità dati fissa</span><span class="sxs-lookup"><span data-stu-id="0427c-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-276">Indica se è necessaria la crittografia per l'unità fissa.</span><span class="sxs-lookup"><span data-stu-id="0427c-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-277">Produttore</span><span class="sxs-lookup"><span data-stu-id="0427c-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-278">Nome del produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-279">Modello</span><span class="sxs-lookup"><span data-stu-id="0427c-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-280">Nome del modello del produttore del computer come viene visualizzato nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="0427c-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-281">Utenti di dispositivi</span><span class="sxs-lookup"><span data-stu-id="0427c-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-282">Utenti noti nel computer gestito da MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="0427c-283">Report conformità computer BitLocker-campi volume computer</span><span class="sxs-lookup"><span data-stu-id="0427c-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0427c-284">Nome colonna</span><span class="sxs-lookup"><span data-stu-id="0427c-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="0427c-285">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0427c-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-286">Lettera di unità</span><span class="sxs-lookup"><span data-stu-id="0427c-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-287">Lettera dell'unità del computer assegnata all'unità specifica dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0427c-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-288">Tipo di unità</span><span class="sxs-lookup"><span data-stu-id="0427c-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-289">Tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="0427c-289">Type of drive.</span></span> <span data-ttu-id="0427c-290">I valori validi sono unità di sistema operativo e unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="0427c-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="0427c-291">Si tratta di unità fisiche anziché di volumi logici.</span><span class="sxs-lookup"><span data-stu-id="0427c-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-292">Intensità cifratura</span><span class="sxs-lookup"><span data-stu-id="0427c-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-293">Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="0427c-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-294">Tipi di protezione</span><span class="sxs-lookup"><span data-stu-id="0427c-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-295">Tipo di protezione selezionata tramite criteri usati per crittografare un sistema operativo o un volume fisso.</span><span class="sxs-lookup"><span data-stu-id="0427c-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="0427c-296">I tipi di protezione validi in un sistema operativo sono TPM o TPM + PIN e per un volume di dati fisso si intende la password.</span><span class="sxs-lookup"><span data-stu-id="0427c-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0427c-297">Stato Protector</span><span class="sxs-lookup"><span data-stu-id="0427c-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-298">Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="0427c-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="0427c-299">Gli stati validi sono attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="0427c-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0427c-300">Stato di crittografia</span><span class="sxs-lookup"><span data-stu-id="0427c-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="0427c-301">Stato di crittografia dell'unità.</span><span class="sxs-lookup"><span data-stu-id="0427c-301">Encryption state of the drive.</span></span> <span data-ttu-id="0427c-302">Gli stati validi sono crittografati, non crittografati e crittografati.</span><span class="sxs-lookup"><span data-stu-id="0427c-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0427c-303">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0427c-303">Related topics</span></span>


[<span data-ttu-id="0427c-304">Uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0427c-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





