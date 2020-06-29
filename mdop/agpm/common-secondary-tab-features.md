---
title: Funzionalità comuni della scheda Secondario
description: Funzionalità comuni della scheda Secondario
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819086"
---
# <span data-ttu-id="a182e-103">Funzionalità comuni della scheda Secondario</span><span class="sxs-lookup"><span data-stu-id="a182e-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="a182e-104">Ogni scheda secondaria include due sezioni, ovvero**oggetti Criteri di gruppo** e **gruppi e utenti**.</span><span class="sxs-lookup"><span data-stu-id="a182e-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="a182e-105">Sezione oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a182e-105">Group Policy objects section</span></span>


<span data-ttu-id="a182e-106">La sezione **oggetti Criteri di gruppo** consente di visualizzare un elenco filtrato degli oggetti Criteri di gruppo e di identificare le caratteristiche seguenti per ogni GPO:</span><span class="sxs-lookup"><span data-stu-id="a182e-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a182e-107">Caratteristica GPO</span><span class="sxs-lookup"><span data-stu-id="a182e-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="a182e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a182e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-109">Name</span><span class="sxs-lookup"><span data-stu-id="a182e-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-110">Nome dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a182e-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-111">Computer (comp.)</span><span class="sxs-lookup"><span data-stu-id="a182e-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-112">Versione generata automaticamente della parte di configurazione del computer dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a182e-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-113">Utente</span><span class="sxs-lookup"><span data-stu-id="a182e-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-114">Versione generata automaticamente della parte di configurazione utente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a182e-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-115">Stato</span><span class="sxs-lookup"><span data-stu-id="a182e-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-116">Stato dell'oggetto Criteri di selezione selezionato:</span><span class="sxs-lookup"><span data-stu-id="a182e-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="a182e-117">Non controllata: </strong> non gestita da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="a182e-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="a182e-118">Archiviato: </strong> disponibile per gli editor autorizzati per l'estrazione per la modifica o per un amministratore di criteri di gruppo da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a182e-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="a182e-119">Estratto: </strong> attualmente in fase di modifica.</span><span class="sxs-lookup"><span data-stu-id="a182e-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="a182e-120">Non è disponibile per altri editor per l'estrazione fino a quando l'editor non l'ha estratto o un amministratore della gestione avanzata Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a182e-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="a182e-121">In sospeso: in attesa </strong> di approvazione da un amministratore di criteri di gruppo prima di essere creato, controllato, distribuito o eliminato.</span><span class="sxs-lookup"><span data-stu-id="a182e-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="a182e-122">Eliminata: </strong> eliminata dall'archivio, ma comunque in grado di essere ripristinata.</span><span class="sxs-lookup"><span data-stu-id="a182e-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="a182e-123">Modello: </strong> versione statica di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="a182e-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="a182e-124">Modello (impostazione predefinita): </strong> per impostazione predefinita, questo modello rappresenta il punto di partenza usato per la creazione di un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="a182e-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-125">Stato GPO</span><span class="sxs-lookup"><span data-stu-id="a182e-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-126">La configurazione del computer e la configurazione dell'utente possono essere gestite separatamente.</span><span class="sxs-lookup"><span data-stu-id="a182e-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="a182e-127">Lo stato dell'oggetto Criteri di stato indica quali parti del GPO sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="a182e-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-128">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="a182e-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-129">Visualizzare i filtri WMI applicati a questo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="a182e-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="a182e-130">I filtri WMI vengono gestiti nel <strong> nodo filtri WMI </strong> per il dominio nell'albero della console di GPMC.</span><span class="sxs-lookup"><span data-stu-id="a182e-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-131">Modificato</span><span class="sxs-lookup"><span data-stu-id="a182e-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-132">Per un GPO controllato, la data più recente in cui è stata archiviata dopo essere stata modificata o disattivata per la modifica.</span><span class="sxs-lookup"><span data-stu-id="a182e-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="a182e-133">Per un GPO non controllato, la data in cui è stata modificata l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="a182e-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-134">Proprietario</span><span class="sxs-lookup"><span data-stu-id="a182e-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-135">L'editor che ha effettuato l'accesso o l'approvatore che ha distribuito l'oggetto Criteri di selezione selezionato.</span><span class="sxs-lookup"><span data-stu-id="a182e-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a182e-136">Sezione gruppi e utenti</span><span class="sxs-lookup"><span data-stu-id="a182e-136">Groups and Users section</span></span>


<span data-ttu-id="a182e-137">Quando viene selezionato un oggetto Criteri di gruppo, nella sezione **gruppi e utenti** viene visualizzato un elenco di gruppi e utenti con accesso a tale oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a182e-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="a182e-138">Le autorizzazioni e l'ereditarietà consentite vengono visualizzate per ogni gruppo o utente.</span><span class="sxs-lookup"><span data-stu-id="a182e-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="a182e-139">Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni usando ruoli Advanced Group Policy Management (editor, approvatore e revisore) o una combinazione personalizzata di autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a182e-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a182e-140">Button</span><span class="sxs-lookup"><span data-stu-id="a182e-140">Button</span></span></th>
<th align="left"><span data-ttu-id="a182e-141">Effetto</span><span class="sxs-lookup"><span data-stu-id="a182e-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-142">Aggiungi</span><span class="sxs-lookup"><span data-stu-id="a182e-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-143">Aggiungere una nuova voce al descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a182e-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="a182e-144">È possibile aggiungere qualsiasi utente o gruppo in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a182e-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-145">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="a182e-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-146">Rimuovere la voce selezionata dall'elenco di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="a182e-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a182e-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a182e-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-148">Visualizzare le proprietà per l'oggetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="a182e-148">Display the properties for the selected object.</span></span> <span data-ttu-id="a182e-149">La pagina delle proprietà è la stessa visualizzata per un oggetto in <strong> utenti e computer di Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="a182e-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a182e-150">Avanzate</span><span class="sxs-lookup"><span data-stu-id="a182e-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a182e-151">Aprire l' <strong> Editor elenco di controllo di Access </strong> .</span><span class="sxs-lookup"><span data-stu-id="a182e-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a182e-152">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a182e-152">Additional considerations</span></span>

-   <span data-ttu-id="a182e-153">Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks.md), esecuzione di attività dell' [Editor](performing-editor-tasks.md), esecuzione di [attività di approvazione](performing-approver-tasks.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="a182e-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="a182e-154">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="a182e-154">Additional references</span></span>

-   [<span data-ttu-id="a182e-155">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="a182e-155">Contents Tab</span></span>](contents-tab.md)

 

 





