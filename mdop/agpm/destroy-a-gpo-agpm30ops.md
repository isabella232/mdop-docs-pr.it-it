---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: bfabd71a-47f3-462e-b86f-5f15762b9e28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 842a546c4db9cc6048908521baa05c6cc1a1a8a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818685"
---
# <span data-ttu-id="f092c-103">Eliminare un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f092c-103">Destroy a GPO</span></span>


<span data-ttu-id="f092c-104">I responsabili approvazione possono eliminare un oggetto Criteri di gruppo, rimuoverlo dal Cestino e eliminarlo definitivamente in modo che non possa più essere ripristinato.</span><span class="sxs-lookup"><span data-stu-id="f092c-104">Approvers can destroy a Group Policy Object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="f092c-105">Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento.</span><span class="sxs-lookup"><span data-stu-id="f092c-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f092c-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f092c-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f092c-107">Per eliminare definitivamente un oggetto Criteri di stato in modo che non possa più essere ripristinato</span><span class="sxs-lookup"><span data-stu-id="f092c-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="f092c-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="f092c-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f092c-109">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di stato eliminati.</span><span class="sxs-lookup"><span data-stu-id="f092c-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="f092c-110">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distruzione e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="f092c-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="f092c-111">Fare clic su **Sì** per confermare che si vuole eliminare definitivamente l'oggetto Criteri di stato selezionato e tutti i backup dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="f092c-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="f092c-112">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="f092c-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f092c-113">L'oggetto Criteri di stato viene rimosso dalla scheda **Cestino** e viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="f092c-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="f092c-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="f092c-114">Additional considerations</span></span>

-   <span data-ttu-id="f092c-115">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="f092c-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f092c-116">In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f092c-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="f092c-117">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="f092c-117">Additional references</span></span>

-   [<span data-ttu-id="f092c-118">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f092c-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





