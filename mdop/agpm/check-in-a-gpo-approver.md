---
title: Archiviare un oggetto Criteri di gruppo
description: Archiviare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819146"
---
# <span data-ttu-id="d3510-103">Archiviare un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d3510-103">Check In a GPO</span></span>


<span data-ttu-id="d3510-104">In genere, gli editor devono eseguire il check-in oggetti Criteri di gruppo che sono stati modificati al termine delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="d3510-104">Ordinarily, Editors should check in Group Policy objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="d3510-105">Per informazioni dettagliate, vedere [modificare un GPO offline](edit-a-gpo-offline.md). Tuttavia, se l'editor non è disponibile, l'approvatore può anche archiviare un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d3510-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="d3510-106">Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="d3510-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="d3510-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d3510-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d3510-108">Per archiviare un oggetto Criteri di controllo Estratto da un editor</span><span class="sxs-lookup"><span data-stu-id="d3510-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="d3510-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="d3510-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d3510-110">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="d3510-110">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="d3510-111">Per ignorare le modifiche apportate dall'editor, fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo, scegliere **Annulla estrazione**e quindi fare clic su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="d3510-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="d3510-112">Per mantenere le modifiche apportate dall'editor, fare clic con il pulsante destro del mouse sull'oggetto Criteri di ricerca e quindi scegliere **Archivia**.</span><span class="sxs-lookup"><span data-stu-id="d3510-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="d3510-113">Digitare un commento da visualizzare nella traccia di controllo del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3510-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="d3510-114">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="d3510-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d3510-115">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.</span><span class="sxs-lookup"><span data-stu-id="d3510-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="d3510-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d3510-116">Additional considerations</span></span>

-   <span data-ttu-id="d3510-117">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="d3510-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d3510-118">In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d3510-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="d3510-119">Se non si è un approvatore o un amministratore della gestione avanzata Criteri di gruppo con l'autorizzazione **Distribuisci GPO** , è necessario essere l'editor che ha estratto il GPO.</span><span class="sxs-lookup"><span data-stu-id="d3510-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="d3510-120">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d3510-120">Additional references</span></span>

-   [<span data-ttu-id="d3510-121">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="d3510-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="d3510-122">Modificare un oggetto Criteri di gruppo offline</span><span class="sxs-lookup"><span data-stu-id="d3510-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline.md)

 

 





