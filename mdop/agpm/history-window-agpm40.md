---
title: Finestra Cronologia
description: Finestra Cronologia
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820795"
---
# <span data-ttu-id="af0ff-103">Finestra Cronologia</span><span class="sxs-lookup"><span data-stu-id="af0ff-103">History Window</span></span>


<span data-ttu-id="af0ff-104">La cronologia di un oggetto Criteri di gruppo può essere visualizzata facendo doppio clic su un GPO oppure facendo clic con il pulsante destro del mouse su un GPO e quindi scegliendo **cronologia**.</span><span class="sxs-lookup"><span data-stu-id="af0ff-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="af0ff-105">Viene visualizzata anche nella console di gestione di criteri di gruppo come scheda per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="af0ff-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="af0ff-106">La cronologia fornisce un record di eventi nella durata dell'oggetto Criteri di stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="af0ff-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="af0ff-107">Nella finestra **cronologia** è possibile ottenere un report delle impostazioni in una versione dell'oggetto Criteri di gruppo, confrontare più versioni di un oggetto Criteri di gruppo o eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="af0ff-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="af0ff-108">Filtrare gli eventi nella finestra cronologia</span><span class="sxs-lookup"><span data-stu-id="af0ff-108">Filtering events in the History window</span></span>


<span data-ttu-id="af0ff-109">Le schede nella finestra **cronologia** filtrano gli Stati nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af0ff-110">Schede</span><span class="sxs-lookup"><span data-stu-id="af0ff-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="af0ff-111">Filtro</span><span class="sxs-lookup"><span data-stu-id="af0ff-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-112">Tutti gli Stati</span><span class="sxs-lookup"><span data-stu-id="af0ff-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-113">Visualizzare tutti gli Stati nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-114">Versioni esclusive</span><span class="sxs-lookup"><span data-stu-id="af0ff-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-115">Visualizza solo le versioni univoche dell'oggetto Criteri di controllo archiviate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="af0ff-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="af0ff-116">La versione distribuita nell'ambiente di produzione, i tasti di scelta rapida per le versioni esclusive e gli Stati informativi vengono omessi dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="af0ff-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af0ff-117">Informazioni sugli eventi</span><span class="sxs-lookup"><span data-stu-id="af0ff-117">Event information</span></span>


<span data-ttu-id="af0ff-118">Le informazioni vengono fornite per ogni stato nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af0ff-119">Attributo GPO</span><span class="sxs-lookup"><span data-stu-id="af0ff-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="af0ff-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af0ff-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-121">Modifica data</span><span class="sxs-lookup"><span data-stu-id="af0ff-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-122">Indicatore di data e ora di quando <strong> </strong> è stata eseguita l'azione nella colonna stato.</span><span class="sxs-lookup"><span data-stu-id="af0ff-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-123">Stato</span><span class="sxs-lookup"><span data-stu-id="af0ff-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-124">Uno stato nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-125">Modificato da</span><span class="sxs-lookup"><span data-stu-id="af0ff-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-126">La persona che ha eseguito l'accesso o ha distribuito l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="af0ff-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-127">Comment</span><span class="sxs-lookup"><span data-stu-id="af0ff-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-128">Un commento immesso dalla persona che ha archiviato o distribuito un GPO al momento della modifica di questa versione, utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="af0ff-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-129">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="af0ff-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-130">Se questa versione del GPO può essere eliminata se il numero di versioni univoche di ogni oggetto Criteri di controllo conservati nell'archivio è limitato.</span><span class="sxs-lookup"><span data-stu-id="af0ff-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="af0ff-131">Nota</span><span class="sxs-lookup"><span data-stu-id="af0ff-131">Note</span></span></strong><br/><p><span data-ttu-id="af0ff-132">È possibile modificare la possibilità di eliminare una versione di un oggetto Criteri di controllo facendo clic con il pulsante destro del mouse sul GPO e quindi scegliendo non <strong> consentire l'eliminazione </strong> o <strong> Consenti l'eliminazione </strong> .</span><span class="sxs-lookup"><span data-stu-id="af0ff-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-133">Versione computer</span><span class="sxs-lookup"><span data-stu-id="af0ff-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-134">Versione generata automaticamente della parte di configurazione del computer del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-135">Versione utente</span><span class="sxs-lookup"><span data-stu-id="af0ff-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-136">Versione generata automaticamente della parte di configurazione dell'utente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="af0ff-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-137">Stato GPO</span><span class="sxs-lookup"><span data-stu-id="af0ff-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-138">La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente.</span><span class="sxs-lookup"><span data-stu-id="af0ff-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="af0ff-139">Questo stato Mostra le parti del GPO abilitate.</span><span class="sxs-lookup"><span data-stu-id="af0ff-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-140">Informazioni GPO di origine</span><span class="sxs-lookup"><span data-stu-id="af0ff-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-141">Per un oggetto Criteri di ricerca importato da un'altra foresta, il nome del GPO originale, il dominio e l'utente e la data associati all'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="af0ff-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="af0ff-142">Rapporti</span><span class="sxs-lookup"><span data-stu-id="af0ff-142">Reports</span></span>


<span data-ttu-id="af0ff-143">I pulsanti **Impostazioni** e **differenze** consentono di visualizzare i report sulle impostazioni GPO per la versione o le versioni degli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="af0ff-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="af0ff-144">Inoltre, se si fa clic con il pulsante destro del mouse su una versione o versioni di un GPO, è possibile visualizzare i report basati su XML.</span><span class="sxs-lookup"><span data-stu-id="af0ff-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af0ff-145">Button</span><span class="sxs-lookup"><span data-stu-id="af0ff-145">Button</span></span></th>
<th align="left"><span data-ttu-id="af0ff-146">Effetto</span><span class="sxs-lookup"><span data-stu-id="af0ff-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-147">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="af0ff-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-148">Generare un report basato su HTML che visualizzi le impostazioni nella versione selezionata del GPO.</span><span class="sxs-lookup"><span data-stu-id="af0ff-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-149">Differenze</span><span class="sxs-lookup"><span data-stu-id="af0ff-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-150">Generare un report basato su HTML che confronti le impostazioni in più versioni selezionate dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="af0ff-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="af0ff-151">Chiave per i report differenze</span><span class="sxs-lookup"><span data-stu-id="af0ff-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="af0ff-152">Simbolo</span><span class="sxs-lookup"><span data-stu-id="af0ff-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="af0ff-153">Significato</span><span class="sxs-lookup"><span data-stu-id="af0ff-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="af0ff-154">Colore</span><span class="sxs-lookup"><span data-stu-id="af0ff-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="af0ff-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af0ff-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="af0ff-156">L'elemento esiste con impostazioni identiche in entrambi i GPO</span><span class="sxs-lookup"><span data-stu-id="af0ff-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="af0ff-157">Varia in base al livello</span><span class="sxs-lookup"><span data-stu-id="af0ff-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-158">[#]</span><span class="sxs-lookup"><span data-stu-id="af0ff-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-159">L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</span><span class="sxs-lookup"><span data-stu-id="af0ff-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="af0ff-160">Blu</span><span class="sxs-lookup"><span data-stu-id="af0ff-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="af0ff-161">[-]</span><span class="sxs-lookup"><span data-stu-id="af0ff-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-162">L'elemento esiste solo nel primo GPO</span><span class="sxs-lookup"><span data-stu-id="af0ff-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="af0ff-163">Rosso</span><span class="sxs-lookup"><span data-stu-id="af0ff-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="af0ff-164">[+]</span><span class="sxs-lookup"><span data-stu-id="af0ff-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="af0ff-165">L'elemento esiste solo nel secondo GPO</span><span class="sxs-lookup"><span data-stu-id="af0ff-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="af0ff-166">Verde</span><span class="sxs-lookup"><span data-stu-id="af0ff-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="af0ff-167">Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso.</span><span class="sxs-lookup"><span data-stu-id="af0ff-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="af0ff-168">Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.</span><span class="sxs-lookup"><span data-stu-id="af0ff-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="af0ff-169">Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi (uno presente solo nel primo GPO, uno presente solo nel secondo), anziché un elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="af0ff-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="af0ff-170">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="af0ff-170">Additional references</span></span>

-   [<span data-ttu-id="af0ff-171">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="af0ff-171">Contents Tab</span></span>](contents-tab-agpm40.md)









