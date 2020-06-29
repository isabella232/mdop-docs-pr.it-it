---
title: Comandi del modello
description: Comandi del modello
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820185"
---
# <span data-ttu-id="3db7d-103">Comandi del modello</span><span class="sxs-lookup"><span data-stu-id="3db7d-103">Template Commands</span></span>


<span data-ttu-id="3db7d-104">Scheda **modelli** :</span><span class="sxs-lookup"><span data-stu-id="3db7d-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="3db7d-105">Visualizza un elenco di modelli disponibili che è possibile usare per creare nuovi oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3db7d-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="3db7d-106">Fornisce un menu di scelta rapida con i comandi per la creazione di un GPO basato su un modello selezionato, sulla gestione dei modelli e sulla visualizzazione dei report per i modelli.</span><span class="sxs-lookup"><span data-stu-id="3db7d-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="3db7d-107">Visualizza un elenco dei gruppi e degli utenti che hanno l'autorizzazione per accedere a un modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="3db7d-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="3db7d-108">Poiché un modello non può essere modificato, i modelli non hanno cronologia.</span><span class="sxs-lookup"><span data-stu-id="3db7d-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="3db7d-109">Tuttavia, come per qualsiasi versione di GPO, le impostazioni di un modello possono essere visualizzate con un report di impostazioni o in confronto a un altro oggetto Criteri di tipo con un report differenze.</span><span class="sxs-lookup"><span data-stu-id="3db7d-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="3db7d-110">**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.</span><span class="sxs-lookup"><span data-stu-id="3db7d-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="3db7d-111">Facendo clic con il pulsante destro del mouse sull'elenco **oggetti Criteri di gruppo** in questa scheda viene visualizzato un menu di scelta rapida, che include le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3db7d-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="3db7d-112">Controllo</span><span class="sxs-lookup"><span data-stu-id="3db7d-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3db7d-113">Comando</span><span class="sxs-lookup"><span data-stu-id="3db7d-113">Command</span></span></th>
<th align="left"><span data-ttu-id="3db7d-114">Effetto</span><span class="sxs-lookup"><span data-stu-id="3db7d-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3db7d-115">Nuovo oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="3db7d-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-116">Creare un nuovo GPO basato sul modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="3db7d-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="3db7d-117">È disponibile l'opzione per distribuire il nuovo GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="3db7d-117">The option to deploy the new GPO to the production environment is provided.</span></span> <span data-ttu-id="3db7d-118">Se non si dispone dell'autorizzazione per creare un GPO, verrà richiesto di inviare una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3db7d-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="3db7d-119">(Questa opzione viene visualizzata se non è selezionato alcun GPO quando si fa clic con il pulsante destro del <strong> mouse Elenco oggetti Criteri di gruppo </strong> .</span><span class="sxs-lookup"><span data-stu-id="3db7d-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3db7d-120">Rapporti</span><span class="sxs-lookup"><span data-stu-id="3db7d-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3db7d-121">Comando</span><span class="sxs-lookup"><span data-stu-id="3db7d-121">Command</span></span></th>
<th align="left"><span data-ttu-id="3db7d-122">Effetto</span><span class="sxs-lookup"><span data-stu-id="3db7d-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3db7d-123">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="3db7d-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-124">Genera un report basato su HTML o basato su XML che visualizza le impostazioni nell'oggetto Criteri di stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="3db7d-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3db7d-125">Differenze</span><span class="sxs-lookup"><span data-stu-id="3db7d-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-126">Genera un report basato su HTML o basato su XML per confrontare le impostazioni in due modelli di GPO selezionati.</span><span class="sxs-lookup"><span data-stu-id="3db7d-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3db7d-127">Gestione dei modelli</span><span class="sxs-lookup"><span data-stu-id="3db7d-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3db7d-128">Comando</span><span class="sxs-lookup"><span data-stu-id="3db7d-128">Command</span></span></th>
<th align="left"><span data-ttu-id="3db7d-129">Effetto</span><span class="sxs-lookup"><span data-stu-id="3db7d-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3db7d-130">Imposta come predefinito</span><span class="sxs-lookup"><span data-stu-id="3db7d-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-131">Imposta il modello selezionato come predefinito da usare automaticamente durante la creazione di un nuovo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3db7d-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3db7d-132">Delete</span><span class="sxs-lookup"><span data-stu-id="3db7d-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-133">Spostare il modello selezionato nel <strong> Cestino </strong> .</span><span class="sxs-lookup"><span data-stu-id="3db7d-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="3db7d-134">Se non si dispone dell'autorizzazione per eliminare un GPO, verrà richiesto di inviare una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3db7d-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3db7d-135">Rename</span><span class="sxs-lookup"><span data-stu-id="3db7d-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-136">Modificare il nome del modello selezionato.</span><span class="sxs-lookup"><span data-stu-id="3db7d-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3db7d-137">Vari</span><span class="sxs-lookup"><span data-stu-id="3db7d-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3db7d-138">Comando</span><span class="sxs-lookup"><span data-stu-id="3db7d-138">Command</span></span></th>
<th align="left"><span data-ttu-id="3db7d-139">Effetto</span><span class="sxs-lookup"><span data-stu-id="3db7d-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3db7d-140">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="3db7d-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-141">Aggiornare la visualizzazione della console di gestione di criteri di gruppo per incorporare le eventuali modifiche.</span><span class="sxs-lookup"><span data-stu-id="3db7d-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="3db7d-142">Alcune modifiche non sono visibili finché non viene aggiornata la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3db7d-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3db7d-143">Help</span><span class="sxs-lookup"><span data-stu-id="3db7d-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3db7d-144">Visualizzare la guida per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="3db7d-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3db7d-145">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="3db7d-145">Additional references</span></span>

-   [<span data-ttu-id="3db7d-146">Scheda Contenuto</span><span class="sxs-lookup"><span data-stu-id="3db7d-146">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="3db7d-147">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="3db7d-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="3db7d-148">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="3db7d-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





