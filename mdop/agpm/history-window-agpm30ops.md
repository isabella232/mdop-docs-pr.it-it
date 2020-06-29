---
title: Finestra Cronologia
description: Finestra Cronologia
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820796"
---
# <span data-ttu-id="ab48d-103">Finestra Cronologia</span><span class="sxs-lookup"><span data-stu-id="ab48d-103">History Window</span></span>


<span data-ttu-id="ab48d-104">La cronologia di un oggetto Criteri di gruppo può essere visualizzata facendo doppio clic su un GPO oppure facendo clic con il pulsante destro del mouse su un GPO e quindi scegliendo **cronologia**.</span><span class="sxs-lookup"><span data-stu-id="ab48d-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="ab48d-105">Viene visualizzata anche nella console di **gestione di criteri di gruppo** come scheda per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="ab48d-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="ab48d-106">La cronologia fornisce un record di eventi nella durata dell'oggetto Criteri di stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="ab48d-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="ab48d-107">Nella finestra **cronologia** è possibile ottenere un report delle impostazioni in una versione dell'oggetto Criteri di gruppo, confrontare più versioni di un oggetto Criteri di gruppo o eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ab48d-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="ab48d-108">Filtrare gli eventi nella finestra cronologia</span><span class="sxs-lookup"><span data-stu-id="ab48d-108">Filtering events in the History window</span></span>


<span data-ttu-id="ab48d-109">Le schede nella finestra **cronologia** filtrano gli Stati nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ab48d-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab48d-110">Schede</span><span class="sxs-lookup"><span data-stu-id="ab48d-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="ab48d-111">Filtro</span><span class="sxs-lookup"><span data-stu-id="ab48d-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-112">Tutti gli Stati</span><span class="sxs-lookup"><span data-stu-id="ab48d-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-113">Visualizzare tutti gli Stati nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ab48d-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-114">Versioni esclusive</span><span class="sxs-lookup"><span data-stu-id="ab48d-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-115">Visualizza solo le versioni univoche dell'oggetto Criteri di controllo archiviate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ab48d-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="ab48d-116">La versione distribuita nell'ambiente di produzione, i tasti di scelta rapida per le versioni esclusive e gli Stati informativi vengono omessi dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="ab48d-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ab48d-117">Informazioni sugli eventi</span><span class="sxs-lookup"><span data-stu-id="ab48d-117">Event information</span></span>


<span data-ttu-id="ab48d-118">Le informazioni vengono fornite per ogni stato nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ab48d-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab48d-119">Attributo GPO</span><span class="sxs-lookup"><span data-stu-id="ab48d-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="ab48d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab48d-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-121">Modifica data</span><span class="sxs-lookup"><span data-stu-id="ab48d-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-122">Indicatore di data e ora di quando <strong> </strong> è stata eseguita l'azione nella colonna stato.</span><span class="sxs-lookup"><span data-stu-id="ab48d-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-123">Stato</span><span class="sxs-lookup"><span data-stu-id="ab48d-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-124">Uno stato nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ab48d-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-125">Modificato da</span><span class="sxs-lookup"><span data-stu-id="ab48d-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-126">La persona che ha eseguito l'accesso o ha distribuito l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab48d-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-127">Comment</span><span class="sxs-lookup"><span data-stu-id="ab48d-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-128">Un commento immesso dalla persona che ha effettuato l'accesso o ha distribuito un GPO al momento della modifica di questa versione.</span><span class="sxs-lookup"><span data-stu-id="ab48d-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="ab48d-129">Utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="ab48d-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-130">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="ab48d-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-131">Se questa versione del GPO può essere eliminata se il numero di versioni univoche di ogni oggetto Criteri di controllo conservati nell'archivio è limitato.</span><span class="sxs-lookup"><span data-stu-id="ab48d-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ab48d-132">Nota</span><span class="sxs-lookup"><span data-stu-id="ab48d-132">Note</span></span></strong><br/><p><span data-ttu-id="ab48d-133">Per modificare la versione di un oggetto Criteri di cancellabile, è possibile fare clic con il pulsante destro del mouse su di esso e quindi fare clic su non <strong> consentire l'eliminazione </strong> o <strong> consentire l'eliminazione </strong> .</span><span class="sxs-lookup"><span data-stu-id="ab48d-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-134">Versione computer</span><span class="sxs-lookup"><span data-stu-id="ab48d-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-135">Versione generata automaticamente della parte di configurazione del computer dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab48d-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-136">Versione utente</span><span class="sxs-lookup"><span data-stu-id="ab48d-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-137">Versione generata automaticamente della parte di configurazione utente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab48d-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-138">Stato GPO</span><span class="sxs-lookup"><span data-stu-id="ab48d-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-139">La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente.</span><span class="sxs-lookup"><span data-stu-id="ab48d-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="ab48d-140">Questo stato Mostra le parti del GPO abilitate.</span><span class="sxs-lookup"><span data-stu-id="ab48d-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-141">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="ab48d-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-142">Visualizzare i filtri WMI applicati a questo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ab48d-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="ab48d-143">I filtri WMI vengono gestiti nella <strong> cartella filtri WMI </strong> per il dominio nell'albero della console di GPMC.</span><span class="sxs-lookup"><span data-stu-id="ab48d-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ab48d-144">Rapporti</span><span class="sxs-lookup"><span data-stu-id="ab48d-144">Reports</span></span>


<span data-ttu-id="ab48d-145">I pulsanti **Impostazioni** e **differenze** consentono di visualizzare i report sulle impostazioni GPO per la versione o le versioni degli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="ab48d-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="ab48d-146">Facendo clic con il pulsante destro del mouse su versioni GPO è disponibile l'opzione per visualizzare anche i report basati su XML.</span><span class="sxs-lookup"><span data-stu-id="ab48d-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab48d-147">Button</span><span class="sxs-lookup"><span data-stu-id="ab48d-147">Button</span></span></th>
<th align="left"><span data-ttu-id="ab48d-148">Effetto</span><span class="sxs-lookup"><span data-stu-id="ab48d-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-149">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="ab48d-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-150">Generare un report basato su HTML che visualizzi le impostazioni nella versione selezionata del GPO.</span><span class="sxs-lookup"><span data-stu-id="ab48d-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-151">Differenze</span><span class="sxs-lookup"><span data-stu-id="ab48d-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-152">Generare un report basato su HTML che confronti le impostazioni in più versioni selezionate dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ab48d-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ab48d-153">Chiave per i report differenze</span><span class="sxs-lookup"><span data-stu-id="ab48d-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab48d-154">Simbolo</span><span class="sxs-lookup"><span data-stu-id="ab48d-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="ab48d-155">Significato</span><span class="sxs-lookup"><span data-stu-id="ab48d-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="ab48d-156">Colore</span><span class="sxs-lookup"><span data-stu-id="ab48d-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab48d-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ab48d-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab48d-158">L'elemento esiste con impostazioni identiche in entrambi i GPO</span><span class="sxs-lookup"><span data-stu-id="ab48d-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab48d-159">Varia in base al livello</span><span class="sxs-lookup"><span data-stu-id="ab48d-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-160">[#]</span><span class="sxs-lookup"><span data-stu-id="ab48d-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-161">L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</span><span class="sxs-lookup"><span data-stu-id="ab48d-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab48d-162">Blu</span><span class="sxs-lookup"><span data-stu-id="ab48d-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab48d-163">[-]</span><span class="sxs-lookup"><span data-stu-id="ab48d-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-164">L'elemento esiste solo nel primo GPO</span><span class="sxs-lookup"><span data-stu-id="ab48d-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab48d-165">Rosso</span><span class="sxs-lookup"><span data-stu-id="ab48d-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab48d-166">[+]</span><span class="sxs-lookup"><span data-stu-id="ab48d-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab48d-167">L'elemento esiste solo nel secondo GPO</span><span class="sxs-lookup"><span data-stu-id="ab48d-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab48d-168">Verde</span><span class="sxs-lookup"><span data-stu-id="ab48d-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="ab48d-169">Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso.</span><span class="sxs-lookup"><span data-stu-id="ab48d-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="ab48d-170">Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.</span><span class="sxs-lookup"><span data-stu-id="ab48d-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="ab48d-171">Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi diversi (uno presente solo nel primo GPO, uno presente solo nel secondo), anziché un elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="ab48d-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="ab48d-172">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="ab48d-172">Additional references</span></span>

-   [<span data-ttu-id="ab48d-173">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="ab48d-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









