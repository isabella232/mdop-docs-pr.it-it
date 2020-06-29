---
title: Eliminare un oggetto Criteri di gruppo controllato
description: Eliminare un oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818715"
---
# <span data-ttu-id="25185-103">Eliminare un oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="25185-103">Delete a Controlled GPO</span></span>


<span data-ttu-id="25185-104">I responsabili approvazione possono eliminare un oggetto Criteri di gruppo controllato, spostandolo nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="25185-104">Approvers can delete a controlled Group Policy Object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="25185-105">Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento.</span><span class="sxs-lookup"><span data-stu-id="25185-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="25185-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="25185-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="25185-107">Per eliminare un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="25185-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="25185-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="25185-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="25185-109">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="25185-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="25185-110">Fare clic con il pulsante destro del mouse sull'oggetto che si vuole eliminare e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="25185-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="25185-111">Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio**.</span><span class="sxs-lookup"><span data-stu-id="25185-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="25185-112">Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.</span><span class="sxs-lookup"><span data-stu-id="25185-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="25185-113">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="25185-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="25185-114">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="25185-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="25185-115">Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="25185-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="25185-116">Se l'oggetto Criteri di stato è stato eliminato solo dall'archivio, viene visualizzato anche nella scheda non **controllata** .</span><span class="sxs-lookup"><span data-stu-id="25185-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="25185-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="25185-117">Additional considerations</span></span>

-   <span data-ttu-id="25185-118">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="25185-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="25185-119">In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="25185-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="25185-120">Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su \*\* &lt; dominio &gt; \*\*e quindi su **oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="25185-120">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="25185-121">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="25185-121">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="25185-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="25185-122">Additional references</span></span>

-   [<span data-ttu-id="25185-123">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="25185-123">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





