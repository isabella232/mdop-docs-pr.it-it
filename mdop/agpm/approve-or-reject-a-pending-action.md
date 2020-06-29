---
title: Approvare o rifiutare un'azione in sospeso
description: Approvare o rifiutare un'azione in sospeso
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819216"
---
# <span data-ttu-id="c1870-103">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="c1870-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="c1870-104">La responsabilità principale di un responsabile approvazione consiste nel valutare e quindi approvare o rifiutare le richieste per la creazione, la distribuzione e l'eliminazione di oggetti Criteri di gruppo da parte di editori o revisori che non dispongono delle autorizzazioni necessarie per completare tali azioni.</span><span class="sxs-lookup"><span data-stu-id="c1870-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="c1870-105">Le funzionalità del report avanzate per la gestione dei criteri di gruppo possono aiutare un responsabile dell'approvazione a valutare una nuova versione di un GPO.</span><span class="sxs-lookup"><span data-stu-id="c1870-105">The report capabilities of Advanced Group Policy Management (AGPM) can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="c1870-106">Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="c1870-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="c1870-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c1870-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c1870-108">Per approvare o rifiutare una richiesta in sospeso</span><span class="sxs-lookup"><span data-stu-id="c1870-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="c1870-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c1870-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c1870-110">Nella scheda **contenuto** fare clic sulla scheda **in sospeso** per visualizzare gli oggetti Criteri di stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c1870-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="c1870-111">Fare clic con il pulsante destro del mouse su un GPO in sospeso e quindi scegliere **approva** o **rifiuta**.</span><span class="sxs-lookup"><span data-stu-id="c1870-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="c1870-112">Se si approva la distribuzione, fare clic su **Avanzate** nella finestra di dialogo **Approva operazione in sospeso** per rivedere i collegamenti al GPO.</span><span class="sxs-lookup"><span data-stu-id="c1870-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="c1870-113">Posizionare il puntatore del mouse su un nodo nell'albero per visualizzare i dettagli.</span><span class="sxs-lookup"><span data-stu-id="c1870-113">Pause the mouse pointer on a node in the tree to display details.</span></span>

    -   <span data-ttu-id="c1870-114">Per impostazione predefinita, tutti i collegamenti al GPO verranno ripristinati.</span><span class="sxs-lookup"><span data-stu-id="c1870-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="c1870-115">Per impedire il ripristino di un collegamento, deselezionare la casella di controllo relativa al collegamento.</span><span class="sxs-lookup"><span data-stu-id="c1870-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="c1870-116">Per impedire il ripristino di tutti i collegamenti, deselezionare la casella di controllo **Ripristina collegamenti** nella finestra di dialogo **Distribuisci GPO** .</span><span class="sxs-lookup"><span data-stu-id="c1870-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="c1870-117">Fare clic su **Sì** o **OK** per confermare l'approvazione o il rifiuto dell'azione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c1870-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="c1870-118">Se è stata approvata la richiesta, il GPO viene spostato nella scheda appropriata per l'azione eseguita.</span><span class="sxs-lookup"><span data-stu-id="c1870-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="c1870-119">**Nota**  Se l'indirizzo di posta elettronica di un responsabile dell'approvazione è incluso nel campo **a** della scheda **delega** del **dominio** , l'approvatore riceverà la posta elettronica dall'alias Advanced Policy Management quando un editor o un revisore invia una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c1870-119">**Note** If an Approver's e-mail address is included in the **To** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="c1870-120">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="c1870-120">Additional considerations</span></span>

-   <span data-ttu-id="c1870-121">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="c1870-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c1870-122">In particolare, è necessario disporre delle autorizzazioni necessarie per eseguire la richiesta che si sta approvando.</span><span class="sxs-lookup"><span data-stu-id="c1870-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="c1870-123">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="c1870-123">Additional references</span></span>

-   [<span data-ttu-id="c1870-124">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="c1870-124">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





