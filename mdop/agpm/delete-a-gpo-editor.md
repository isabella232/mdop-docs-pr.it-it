---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820975"
---
# <span data-ttu-id="60996-103">Eliminare un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="60996-103">Delete a GPO</span></span>


<span data-ttu-id="60996-104">Come editor, potresti non avere l'autorizzazione per completare l'eliminazione di un oggetto Criteri di gruppo, ma hai le autorizzazioni necessarie per avviare il processo e inviare la richiesta a un responsabile dell'approvazione.</span><span class="sxs-lookup"><span data-stu-id="60996-104">As an Editor, you may not have permission to complete the deletion of a Group Policy object (GPO), but you do have the permission necessary to begin the process and submit your request to an Approver.</span></span>

<span data-ttu-id="60996-105">Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="60996-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="60996-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="60996-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="60996-107">Per richiedere l'eliminazione di un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="60996-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="60996-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="60996-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="60996-109">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="60996-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="60996-110">Fare clic con il pulsante destro del mouse sul GPO da eliminare e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="60996-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="60996-111">Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio (Annulla controllo)**.</span><span class="sxs-lookup"><span data-stu-id="60996-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="60996-112">Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.</span><span class="sxs-lookup"><span data-stu-id="60996-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

        <span data-ttu-id="60996-113">A meno che non si disponga di autorizzazioni speciali per eliminare gli oggetti Criteri di ricerca, è necessario inviare una richiesta per l'eliminazione del GPO distribuito.</span><span class="sxs-lookup"><span data-stu-id="60996-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="60996-114">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="60996-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="60996-115">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="60996-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

4.  <span data-ttu-id="60996-116">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="60996-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="60996-117">Il GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato dalla scheda **in sospeso** alla scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="60996-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="60996-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="60996-118">Additional considerations</span></span>

-   <span data-ttu-id="60996-119">Per impostazione predefinita, è necessario essere un editor per richiedere l'eliminazione di un GPO distribuito.</span><span class="sxs-lookup"><span data-stu-id="60996-119">By default, you must be an Editor to request the deletion of a deployed GPO.</span></span> <span data-ttu-id="60996-120">In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="60996-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="60996-121">Per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un oggetto Criteri di stato dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="60996-121">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="60996-122">In particolare, è necessario avere **contenuto elenco** e **modificare le impostazioni** o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="60996-122">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="60996-123">Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="60996-123">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="60996-124">Il GPO verrà restituito alla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="60996-124">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="60996-125">Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su \*\* &lt; dominio &gt; \*\*e quindi su **oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="60996-125">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="60996-126">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="60996-126">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="60996-127">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="60996-127">Additional references</span></span>

-   [<span data-ttu-id="60996-128">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="60996-128">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

 

 





