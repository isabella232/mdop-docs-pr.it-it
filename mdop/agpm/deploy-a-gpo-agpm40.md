---
title: Distribuire un oggetto Criteri di gruppo
description: Distribuire un oggetto Criteri di gruppo
author: dansimp
ms.assetid: a6febeaa-144b-4c02-99af-d972f0f2b544
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 208fd95ec48f81b6c3a2a59bf92f53128eb3d529
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818705"
---
# <span data-ttu-id="5c1f7-103">Distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="5c1f7-103">Deploy a GPO</span></span>


<span data-ttu-id="5c1f7-104">Un responsabile approvazione può distribuire un oggetto Criteri di gruppo nuovo o modificato nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-104">An Approver can deploy a new or edited Group Policy Object (GPO) to the production environment.</span></span> <span data-ttu-id="5c1f7-105">Per informazioni su come ridistribuire una versione precedente di un oggetto Criteri di controllo, vedere [eseguire il rollback a una versione precedente di un oggetto Criteri di](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)ricerca.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-105">For information about redeploying an earlier version of a GPO, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

<span data-ttu-id="5c1f7-106">Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5c1f7-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5c1f7-108">Per distribuire un GPO nell'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="5c1f7-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="5c1f7-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5c1f7-110">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5c1f7-111">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distribuzione e quindi scegliere **Distribuisci**.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="5c1f7-112">Per rivedere i collegamenti all'oggetto Criteri di controllo, fare clic su **Avanzate**.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="5c1f7-113">Posizionare il puntatore del mouse su un elemento nell'albero per visualizzare i dettagli.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="5c1f7-114">Per impostazione predefinita, tutti i collegamenti al GPO verranno ripristinati.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="5c1f7-115">Per impedire il ripristino di un collegamento, deselezionare la casella di controllo relativa al collegamento.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="5c1f7-116">Per impedire il ripristino di tutti i collegamenti, deselezionare la casella di controllo **Ripristina collegamenti** nella finestra di dialogo **Distribuisci GPO** .</span><span class="sxs-lookup"><span data-stu-id="5c1f7-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="5c1f7-117">Fai clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-117">Click **Yes**.</span></span> <span data-ttu-id="5c1f7-118">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="5c1f7-119">**Nota**  Per verificare se la versione più recente di un oggetto Criteri di controllo è stata distribuita, fare doppio clic sul GPO nella scheda **controllati** per visualizzarne la **cronologia**.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="5c1f7-120">Nella **cronologia** per il GPO la colonna **stato** indica se un oggetto Criteri di ricerca è stato distribuito.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="5c1f7-121">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="5c1f7-121">Additional considerations</span></span>

-   <span data-ttu-id="5c1f7-122">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="5c1f7-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5c1f7-123">In particolare, devi avere il **contenuto dell'elenco** e distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5c1f7-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="5c1f7-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="5c1f7-124">Additional references</span></span>

-   [<span data-ttu-id="5c1f7-125">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="5c1f7-125">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





