---
title: Modificare un oggetto Criteri di gruppo offline
description: Modificare un oggetto Criteri di gruppo offline
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820886"
---
# <span data-ttu-id="2e517-103">Modificare un oggetto Criteri di gruppo offline</span><span class="sxs-lookup"><span data-stu-id="2e517-103">Edit a GPO Offline</span></span>


<span data-ttu-id="2e517-104">Per apportare modifiche a un oggetto Criteri di gruppo controllato, è necessario prima di tutto estrarre una copia del GPO dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="2e517-104">To make changes to a controlled Group Policy object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="2e517-105">Nessun altro sarà in grado di modificare l'oggetto Criteri di gruppo finché non viene archiviato di nuovo, impedendo l'introduzione di modifiche in conflitto da parte di più amministratori di criteri di gruppi.</span><span class="sxs-lookup"><span data-stu-id="2e517-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="2e517-106">Dopo aver modificato l'oggetto Criteri di controllo, è possibile archiviarlo nell'archivio, in modo che possa essere esaminato e distribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="2e517-106">When you have finished modifying the GPO, you check it into the archive, so it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="2e517-107">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di criteri di raggruppamento avanzati.</span><span class="sxs-lookup"><span data-stu-id="2e517-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2e517-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2e517-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="2e517-109">Modifica di un GPO offline</span><span class="sxs-lookup"><span data-stu-id="2e517-109">Editing a GPO offline</span></span>


<span data-ttu-id="2e517-110">Per modificare un oggetto Criteri di controllo, Estrai l'oggetto Criteri di ricerca dall'archivio, modifica il GPO offline e quindi controlla l'oggetto Criteri di ricerca nell'archivio, in modo che possa essere esaminato e distribuito (o modificato da altri editor).</span><span class="sxs-lookup"><span data-stu-id="2e517-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive, so it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="2e517-111">Estrarre un GPO</span><span class="sxs-lookup"><span data-stu-id="2e517-111">Check out a GPO</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="2e517-112">Modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="2e517-112">Edit a GPO</span></span>](#bkmk-edit)

-   [<span data-ttu-id="2e517-113">Archiviare un oggetto Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="2e517-113">Check in a GPO</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="2e517-114">Per estrarre un oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="2e517-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="2e517-115">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="2e517-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2e517-116">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="2e517-116">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="2e517-117">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di modifica e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="2e517-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="2e517-118">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e517-118">Type a comment to be displayed in the History of the GPO while it is checked out, then click **OK**.</span></span>

5.  <span data-ttu-id="2e517-119">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="2e517-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="2e517-120">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene ora identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="2e517-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="2e517-121">Per modificare un GPO offline</span><span class="sxs-lookup"><span data-stu-id="2e517-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="2e517-122">Nella scheda **controllato** fare clic con il pulsante destro del mouse sull'oggetto Criteri di modifica e quindi scegliere **modifica**.</span><span class="sxs-lookup"><span data-stu-id="2e517-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="2e517-123">Nell' **Editor oggetti Criteri di gruppo**apportare modifiche a una copia offline del GPO.</span><span class="sxs-lookup"><span data-stu-id="2e517-123">In the **Group Policy Object Editor**, make changes to an offline copy of the GPO.</span></span>

3.  <span data-ttu-id="2e517-124">Dopo aver modificato il GPO, chiudere l' **Editor oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="2e517-124">When you have finished modifying the GPO, close the **Group Policy Object Editor**.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="2e517-125">Per controllare un GPO nell'archivio</span><span class="sxs-lookup"><span data-stu-id="2e517-125">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="2e517-126">Nella scheda **controllati** :</span><span class="sxs-lookup"><span data-stu-id="2e517-126">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="2e517-127">Se non sono state apportate modifiche al GPO, fare clic con il pulsante destro del mouse sull'oggetto Criteri di ricerca e scegliere **Annulla estrazione**, quindi fare clic su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="2e517-127">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="2e517-128">Se sono state apportate modifiche al GPO, fare clic con il pulsante destro del mouse sull'oggetto Criteri di ricerca e scegliere **Archivia**.</span><span class="sxs-lookup"><span data-stu-id="2e517-128">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="2e517-129">Digitare un commento da visualizzare nella traccia di controllo del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e517-129">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="2e517-130">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="2e517-130">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="2e517-131">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.</span><span class="sxs-lookup"><span data-stu-id="2e517-131">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="2e517-132">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="2e517-132">Additional considerations</span></span>

-   <span data-ttu-id="2e517-133">Per estrarre e modificare un oggetto Criteri di controllo, per impostazione predefinita, è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di ricerca, un editor o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="2e517-133">To check out and edit a GPO, by default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="2e517-134">In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2e517-134">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="2e517-135">Per modificare l'oggetto Criteri di controllo, è inoltre necessario essere l'utente che ha estratto l'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="2e517-135">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="2e517-136">Per archiviare un GPO per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="2e517-136">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="2e517-137">In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2e517-137">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="2e517-138">Se non si è un approvatore o un amministratore della gestione avanzata Criteri di gruppo con l'autorizzazione **Distribuisci GPO** , è necessario essere l'editor che ha estratto il GPO.</span><span class="sxs-lookup"><span data-stu-id="2e517-138">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="2e517-139">Quando si modifica un oggetto Criteri di gruppo, qualsiasi aggiornamento dell'installazione del software di un pacchetto in un altro GPO deve fare riferimento al GPO distribuito, non alla copia Estratto.</span><span class="sxs-lookup"><span data-stu-id="2e517-139">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, not the checked-out copy.</span></span>

### <span data-ttu-id="2e517-140">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="2e517-140">Additional references</span></span>

-   [<span data-ttu-id="2e517-141">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2e517-141">Editing a GPO</span></span>](editing-a-gpo.md)

-   <span data-ttu-id="2e517-142">Revisione di un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="2e517-142">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="2e517-143">Esaminare le impostazioni dell'oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2e517-143">Review GPO Settings</span></span>](review-gpo-settings.md)

    -   [<span data-ttu-id="2e517-144">Esaminare i collegamenti dell'oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2e517-144">Review GPO Links</span></span>](review-gpo-links.md)

    -   [<span data-ttu-id="2e517-145">Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli</span><span class="sxs-lookup"><span data-stu-id="2e517-145">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   <span data-ttu-id="2e517-146">Distribuzione di un GPO</span><span class="sxs-lookup"><span data-stu-id="2e517-146">Deploying a GPO</span></span>

    -   [<span data-ttu-id="2e517-147">Richiedere la distribuzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2e517-147">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo.md)

    -   [<span data-ttu-id="2e517-148">Distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2e517-148">Deploy a GPO</span></span>](deploy-a-gpo.md)

 

 





