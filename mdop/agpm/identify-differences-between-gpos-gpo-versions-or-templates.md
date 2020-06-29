---
title: Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli
description: Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820756"
---
# <span data-ttu-id="50205-103">Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli</span><span class="sxs-lookup"><span data-stu-id="50205-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="50205-104">Per analizzare le differenze tra gli oggetti Criteri di gruppo, i modelli o le diverse versioni di un GPO, è possibile generare report di differenze basati su HTML o su XML.</span><span class="sxs-lookup"><span data-stu-id="50205-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="50205-105">Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="50205-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="50205-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="50205-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="50205-107">Identificazione delle differenze tra GPO, versioni GPO o modelli</span><span class="sxs-lookup"><span data-stu-id="50205-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="50205-108">Tra due GPO o modelli</span><span class="sxs-lookup"><span data-stu-id="50205-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="50205-109">Tra un GPO e un modello</span><span class="sxs-lookup"><span data-stu-id="50205-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="50205-110">Tra due versioni di un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="50205-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="50205-111">Tra una versione di un GPO e un modello</span><span class="sxs-lookup"><span data-stu-id="50205-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="50205-112">Per identificare le differenze tra due GPO o modelli</span><span class="sxs-lookup"><span data-stu-id="50205-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="50205-113">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="50205-114">Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).</span><span class="sxs-lookup"><span data-stu-id="50205-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="50205-115">Selezionare i due GPO o i modelli.</span><span class="sxs-lookup"><span data-stu-id="50205-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="50205-116">Fare clic con il pulsante destro del mouse su uno dei GPO o sui modelli, scegliere **differenze**e quindi fare clic su **report HTML** o **report XML** per visualizzare un report differenze che riepiloga le impostazioni dei GPO o modelli.</span><span class="sxs-lookup"><span data-stu-id="50205-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="50205-117">Per identificare le differenze tra un GPO e un modello</span><span class="sxs-lookup"><span data-stu-id="50205-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="50205-118">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="50205-119">Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).</span><span class="sxs-lookup"><span data-stu-id="50205-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="50205-120">Fare clic con il pulsante destro del mouse sul GPO, scegliere **differenze**e quindi fare clic su **modello**.</span><span class="sxs-lookup"><span data-stu-id="50205-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="50205-121">Selezionare il modello e il tipo di report e quindi fare clic su **OK** per visualizzare un report di differenza che riepiloga le impostazioni del GPO e del modello.</span><span class="sxs-lookup"><span data-stu-id="50205-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="50205-122">Per identificare le differenze tra due versioni di un oggetto Criteri di tipo</span><span class="sxs-lookup"><span data-stu-id="50205-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="50205-123">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="50205-124">Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).</span><span class="sxs-lookup"><span data-stu-id="50205-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="50205-125">Fare doppio clic sull'oggetto Criteri di confronto per visualizzarne la cronologia e quindi evidenziare le versioni da confrontare.</span><span class="sxs-lookup"><span data-stu-id="50205-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="50205-126">Fare clic con il pulsante destro del mouse su una delle versioni, scegliere **differenze**e quindi fare clic su **report HTML** o **report XML** per visualizzare un report di differenza che riepiloga le impostazioni degli oggetti Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="50205-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="50205-127">Per identificare le differenze tra una versione di un GPO e un modello</span><span class="sxs-lookup"><span data-stu-id="50205-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="50205-128">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="50205-129">Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).</span><span class="sxs-lookup"><span data-stu-id="50205-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="50205-130">Fare doppio clic sul GPO per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="50205-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="50205-131">Fare clic con il pulsante destro del mouse sulla versione degli oggetti Criteri di interesse, scegliere **differenze**e quindi fare clic su **modello**.</span><span class="sxs-lookup"><span data-stu-id="50205-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="50205-132">Selezionare il modello e il tipo di report e quindi fare clic su **OK** per visualizzare un report di differenza che riepiloga le impostazioni della versione e del modello del GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="50205-133">Chiave per i report differenze</span><span class="sxs-lookup"><span data-stu-id="50205-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50205-134">Simbolo</span><span class="sxs-lookup"><span data-stu-id="50205-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="50205-135">Significato</span><span class="sxs-lookup"><span data-stu-id="50205-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="50205-136">Colore</span><span class="sxs-lookup"><span data-stu-id="50205-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50205-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50205-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="50205-138">L'elemento esiste con impostazioni identiche in entrambi i GPO</span><span class="sxs-lookup"><span data-stu-id="50205-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="50205-139">Varia in base al livello</span><span class="sxs-lookup"><span data-stu-id="50205-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="50205-140">[#]</span><span class="sxs-lookup"><span data-stu-id="50205-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="50205-141">L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</span><span class="sxs-lookup"><span data-stu-id="50205-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="50205-142">Blu</span><span class="sxs-lookup"><span data-stu-id="50205-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="50205-143">[-]</span><span class="sxs-lookup"><span data-stu-id="50205-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="50205-144">L'elemento esiste solo nel primo GPO</span><span class="sxs-lookup"><span data-stu-id="50205-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="50205-145">Rosso</span><span class="sxs-lookup"><span data-stu-id="50205-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="50205-146">[+]</span><span class="sxs-lookup"><span data-stu-id="50205-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="50205-147">L'elemento esiste solo nel secondo GPO</span><span class="sxs-lookup"><span data-stu-id="50205-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="50205-148">Verde</span><span class="sxs-lookup"><span data-stu-id="50205-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="50205-149">Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso.</span><span class="sxs-lookup"><span data-stu-id="50205-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="50205-150">Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.</span><span class="sxs-lookup"><span data-stu-id="50205-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="50205-151">Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi diversi (uno presente solo nel primo GPO, uno presente solo nel secondo) anziché un elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="50205-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="50205-152">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="50205-152">Additional considerations</span></span>

-   <span data-ttu-id="50205-153">Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="50205-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="50205-154">In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO.</span><span class="sxs-lookup"><span data-stu-id="50205-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="50205-155">Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="50205-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="50205-156">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="50205-156">Additional references</span></span>

-   [<span data-ttu-id="50205-157">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="50205-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





