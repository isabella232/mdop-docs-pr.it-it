---
title: Funzionalità della scheda Contenuto
description: Funzionalità della scheda Contenuto
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818895"
---
# <span data-ttu-id="e1bb8-103">Funzionalità della scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="e1bb8-103">Contents Tab Features</span></span>


<span data-ttu-id="e1bb8-104">Ogni scheda secondaria nella scheda **Sommario** include due sezioni, ovvero**oggetti Criteri di gruppo** e **gruppi e utenti**.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="e1bb8-105">Sezione oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e1bb8-105">Group Policy objects section</span></span>


<span data-ttu-id="e1bb8-106">Nella sezione **oggetti Criteri di gruppo** viene visualizzato un elenco filtrato degli oggetti Criteri di gruppo e vengono identificati gli attributi seguenti per ogni GPO.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO.</span></span> <span data-ttu-id="e1bb8-107">È possibile usare la casella di **ricerca** per cercare GPO con attributi specifici.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-107">You can use the **Search** box to search for GPOs with specific attributes.</span></span> <span data-ttu-id="e1bb8-108">Per altre informazioni, vedere [cercare e filtrare l'elenco degli oggetti Criteri di ricerca](search-and-filter-the-list-of-gpos.md).</span><span class="sxs-lookup"><span data-stu-id="e1bb8-108">For more information, see [Search and Filter the List of GPOs](search-and-filter-the-list-of-gpos.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1bb8-109">Attributo GPO</span><span class="sxs-lookup"><span data-stu-id="e1bb8-109">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="e1bb8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1bb8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-111">Name</span><span class="sxs-lookup"><span data-stu-id="e1bb8-111">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-112">Nome dell'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-112">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-113">Stato</span><span class="sxs-lookup"><span data-stu-id="e1bb8-113">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-114">Stato dell'oggetto Criteri di stato selezionato</span><span class="sxs-lookup"><span data-stu-id="e1bb8-114">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-115">Modificato da</span><span class="sxs-lookup"><span data-stu-id="e1bb8-115">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-116">L'editor che ha effettuato l'accesso o l'approvatore che ha distribuito l'oggetto Criteri di selezione selezionato.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-116">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-117">Modifica data</span><span class="sxs-lookup"><span data-stu-id="e1bb8-117">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-118">Per un GPO controllato, la data più recente in cui è stata archiviata dopo essere stata modificata o disattivata per la modifica.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-118">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="e1bb8-119">Per un GPO non controllato, la data in cui è stata modificata l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-119">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-120">Comment</span><span class="sxs-lookup"><span data-stu-id="e1bb8-120">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-121">Un commento immesso dalla persona che ha effettuato l'accesso o ha distribuito un oggetto Criteri di controllo nel momento in cui è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-121">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="e1bb8-122">Utile per identificare le specifiche della versione in caso di necessità di eseguire il rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-122">Useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-123">Versione computer</span><span class="sxs-lookup"><span data-stu-id="e1bb8-123">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-124">Versione generata automaticamente della parte di configurazione del computer del GPO.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-124">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-125">Versione utente</span><span class="sxs-lookup"><span data-stu-id="e1bb8-125">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-126">Versione generata automaticamente della parte di configurazione dell'utente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-126">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-127">Stato GPO</span><span class="sxs-lookup"><span data-stu-id="e1bb8-127">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-128">La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-128">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="e1bb8-129">Lo stato dell'oggetto Criteri di stato indica quali parti del GPO sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-129">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-130">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="e1bb8-130">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-131">Visualizzare i filtri WMI applicati a questo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-131">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="e1bb8-132">I filtri WMI vengono gestiti nella <strong> cartella filtri WMI </strong> per il dominio nell'albero della console di GPMC.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-132">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e1bb8-133">Sezione gruppi e utenti</span><span class="sxs-lookup"><span data-stu-id="e1bb8-133">Groups and Users section</span></span>


<span data-ttu-id="e1bb8-134">Quando viene selezionato un oggetto Criteri di gruppo, nella sezione **gruppi e utenti** viene visualizzato un elenco di gruppi e utenti con accesso a tale oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-134">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="e1bb8-135">Le autorizzazioni e l'ereditarietà consentite vengono visualizzate per ogni gruppo o utente.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-135">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="e1bb8-136">Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni usando ruoli Advanced Group Policy Management (editor, approvatore, revisore e amministratore della gestione avanzata) o una combinazione personalizzata di autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-136">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1bb8-137">Button</span><span class="sxs-lookup"><span data-stu-id="e1bb8-137">Button</span></span></th>
<th align="left"><span data-ttu-id="e1bb8-138">Effetto</span><span class="sxs-lookup"><span data-stu-id="e1bb8-138">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-139">Aggiungi</span><span class="sxs-lookup"><span data-stu-id="e1bb8-139">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-140">Aggiungere una nuova voce al descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-140">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="e1bb8-141">È possibile aggiungere qualsiasi utente o gruppo in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-141">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-142">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="e1bb8-142">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-143">Rimuovere la voce selezionata dall'elenco di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-143">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1bb8-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1bb8-144">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-145">Visualizzare le proprietà per l'oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="e1bb8-145">Display the properties for the selected object.</span></span> <span data-ttu-id="e1bb8-146">La pagina delle proprietà è la stessa visualizzata per un oggetto in <strong> utenti e computer di Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="e1bb8-146">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1bb8-147">Avanzate</span><span class="sxs-lookup"><span data-stu-id="e1bb8-147">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1bb8-148">Aprire l' <strong> Editor elenco di controllo di Access </strong> .</span><span class="sxs-lookup"><span data-stu-id="e1bb8-148">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e1bb8-149">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e1bb8-149">Additional considerations</span></span>

-   <span data-ttu-id="e1bb8-150">Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks-agpm40.md), esecuzione di attività dell' [Editor](performing-editor-tasks-agpm40.md), esecuzione di [attività di approvazione](performing-approver-tasks-agpm40.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e1bb8-150">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="e1bb8-151">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="e1bb8-151">Additional references</span></span>

-   [<span data-ttu-id="e1bb8-152">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="e1bb8-152">Contents Tab</span></span>](contents-tab-agpm40.md)

 

 





