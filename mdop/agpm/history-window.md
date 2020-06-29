---
title: Finestra Cronologia
description: Finestra Cronologia
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820786"
---
# <span data-ttu-id="aee7e-103">Finestra Cronologia</span><span class="sxs-lookup"><span data-stu-id="aee7e-103">History Window</span></span>


<span data-ttu-id="aee7e-104">La cronologia di un oggetto Criteri di gruppo può essere visualizzata facendo doppio clic su un GPO oppure facendo clic con il pulsante destro del mouse su un GPO e quindi scegliendo **cronologia**.</span><span class="sxs-lookup"><span data-stu-id="aee7e-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="aee7e-105">Viene visualizzata anche nella console di **gestione di criteri di gruppo** come scheda per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="aee7e-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="aee7e-106">La cronologia contiene un elenco di tutte le versioni dell'oggetto Criteri di stato selezionato salvate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="aee7e-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="aee7e-107">Nella finestra **cronologia** è possibile ottenere un report delle impostazioni in un oggetto Criteri di gruppo, confrontare più versioni di un oggetto Criteri di gruppo o eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="aee7e-108">Filtrare gli eventi nella finestra cronologia</span><span class="sxs-lookup"><span data-stu-id="aee7e-108">Filtering events in the History window</span></span>


<span data-ttu-id="aee7e-109">Le schede nella finestra **cronologia** filtrano gli eventi visualizzati.</span><span class="sxs-lookup"><span data-stu-id="aee7e-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aee7e-110">Schede</span><span class="sxs-lookup"><span data-stu-id="aee7e-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="aee7e-111">Filtro</span><span class="sxs-lookup"><span data-stu-id="aee7e-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-112">Mostra tutto</span><span class="sxs-lookup"><span data-stu-id="aee7e-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-113">Visualizza tutte le versioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="aee7e-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-114">Archiviato</span><span class="sxs-lookup"><span data-stu-id="aee7e-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-115">Visualizza solo le versioni archiviate dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="aee7e-116">La versione distribuita viene omessa da questo elenco.</span><span class="sxs-lookup"><span data-stu-id="aee7e-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-117">Solo etichette</span><span class="sxs-lookup"><span data-stu-id="aee7e-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-118">Visualizzare solo i GPO a cui sono associate etichette.</span><span class="sxs-lookup"><span data-stu-id="aee7e-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="aee7e-119">Informazioni sugli eventi</span><span class="sxs-lookup"><span data-stu-id="aee7e-119">Event information</span></span>


<span data-ttu-id="aee7e-120">Le informazioni vengono fornite per ogni evento nella cronologia del GPO selezionato.</span><span class="sxs-lookup"><span data-stu-id="aee7e-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aee7e-121">Caratteristica GPO</span><span class="sxs-lookup"><span data-stu-id="aee7e-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="aee7e-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aee7e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-123">Computer</span><span class="sxs-lookup"><span data-stu-id="aee7e-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-124">Versione generata automaticamente della parte di configurazione del computer dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-125">Utente</span><span class="sxs-lookup"><span data-stu-id="aee7e-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-126">Versione generata automaticamente della parte di configurazione utente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-127">Tempo</span><span class="sxs-lookup"><span data-stu-id="aee7e-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-128">Timestamp della versione del GPO quando è stata eseguita l'azione nel campo stato.</span><span class="sxs-lookup"><span data-stu-id="aee7e-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-129">Stato</span><span class="sxs-lookup"><span data-stu-id="aee7e-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-130">Stato della versione selezionata del GPO:</span><span class="sxs-lookup"><span data-stu-id="aee7e-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="aee7e-131">Distribuito </strong> : questa versione dell'oggetto Criteri di controllo è attualmente attiva nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="aee7e-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="aee7e-132">Check-in </strong> : questa versione dell'oggetto Criteri di gruppo è disponibile per gli editori autorizzati per l'estrazione per la modifica o per l'amministratore dei criteri di raggruppamento da distribuire.</span><span class="sxs-lookup"><span data-stu-id="aee7e-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="aee7e-133">Estratto </strong> : questa versione dell'oggetto Criteri di controllo è attualmente estratta da un editor e non è disponibile per altri editor.</span><span class="sxs-lookup"><span data-stu-id="aee7e-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="aee7e-134">Lo stato estratto non viene registrato nella <strong> pagina Cronologia </strong> tranne che per indicare se un oggetto Criteri di controllo è attualmente estratto.</span><span class="sxs-lookup"><span data-stu-id="aee7e-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="aee7e-135">Created </strong> : identifica la data e l'ora della creazione iniziale del GPO.</span><span class="sxs-lookup"><span data-stu-id="aee7e-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="aee7e-136">Etichettato </strong> : identifica una versione con etichetta dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-137">Stato GPO</span><span class="sxs-lookup"><span data-stu-id="aee7e-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-138">La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente.</span><span class="sxs-lookup"><span data-stu-id="aee7e-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="aee7e-139">Questo stato Mostra le parti del GPO abilitate.</span><span class="sxs-lookup"><span data-stu-id="aee7e-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-140">Proprietario</span><span class="sxs-lookup"><span data-stu-id="aee7e-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-141">La persona che ha eseguito l'accesso o ha distribuito l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-142">Comment</span><span class="sxs-lookup"><span data-stu-id="aee7e-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-143">Un commento immesso dal proprietario di un oggetto Criteri di controllo al momento della modifica di questa versione.</span><span class="sxs-lookup"><span data-stu-id="aee7e-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="aee7e-144">Utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="aee7e-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="aee7e-145">Rapporti</span><span class="sxs-lookup"><span data-stu-id="aee7e-145">Reports</span></span>


<span data-ttu-id="aee7e-146">A seconda che sia selezionata una singola versione di GPO o più versioni di GPO, i pulsanti **Impostazioni** e **differenze** visualizzano i report sulle impostazioni degli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="aee7e-147">Facendo clic con il pulsante destro del mouse su versioni GPO è disponibile l'opzione per visualizzare anche i report basati su XML.</span><span class="sxs-lookup"><span data-stu-id="aee7e-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aee7e-148">Button</span><span class="sxs-lookup"><span data-stu-id="aee7e-148">Button</span></span></th>
<th align="left"><span data-ttu-id="aee7e-149">Effetto</span><span class="sxs-lookup"><span data-stu-id="aee7e-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-150">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="aee7e-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-151">Generare un report basato su HTML che visualizzi le impostazioni nella versione selezionata del GPO.</span><span class="sxs-lookup"><span data-stu-id="aee7e-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-152">Differenze</span><span class="sxs-lookup"><span data-stu-id="aee7e-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-153">Generare un report basato su HTML che confronti le impostazioni in più versioni selezionate dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="aee7e-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="aee7e-154">Chiave per i report differenze</span><span class="sxs-lookup"><span data-stu-id="aee7e-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aee7e-155">Simbolo</span><span class="sxs-lookup"><span data-stu-id="aee7e-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="aee7e-156">Significato</span><span class="sxs-lookup"><span data-stu-id="aee7e-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="aee7e-157">Colore</span><span class="sxs-lookup"><span data-stu-id="aee7e-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aee7e-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aee7e-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="aee7e-159">L'elemento esiste con impostazioni identiche in entrambi i GPO</span><span class="sxs-lookup"><span data-stu-id="aee7e-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="aee7e-160">Varia in base al livello</span><span class="sxs-lookup"><span data-stu-id="aee7e-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-161">[#]</span><span class="sxs-lookup"><span data-stu-id="aee7e-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-162">L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</span><span class="sxs-lookup"><span data-stu-id="aee7e-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="aee7e-163">Blu</span><span class="sxs-lookup"><span data-stu-id="aee7e-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="aee7e-164">[-]</span><span class="sxs-lookup"><span data-stu-id="aee7e-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-165">L'elemento esiste solo nel primo GPO</span><span class="sxs-lookup"><span data-stu-id="aee7e-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="aee7e-166">Rosso</span><span class="sxs-lookup"><span data-stu-id="aee7e-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="aee7e-167">[+]</span><span class="sxs-lookup"><span data-stu-id="aee7e-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="aee7e-168">L'elemento esiste solo nel secondo GPO</span><span class="sxs-lookup"><span data-stu-id="aee7e-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="aee7e-169">Verde</span><span class="sxs-lookup"><span data-stu-id="aee7e-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="aee7e-170">Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso.</span><span class="sxs-lookup"><span data-stu-id="aee7e-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="aee7e-171">Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.</span><span class="sxs-lookup"><span data-stu-id="aee7e-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="aee7e-172">Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi diversi (uno presente solo nel primo GPO, uno presente solo nel secondo), anziché un elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="aee7e-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="aee7e-173">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="aee7e-173">Additional references</span></span>

-   [<span data-ttu-id="aee7e-174">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="aee7e-174">Contents Tab</span></span>](contents-tab.md)

 

 





