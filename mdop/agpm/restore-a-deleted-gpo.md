---
title: Ripristinare un oggetto Criteri di gruppo eliminato
description: Ripristinare un oggetto Criteri di gruppo eliminato
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818415"
---
# <span data-ttu-id="dd463-103">Ripristinare un oggetto Criteri di gruppo eliminato</span><span class="sxs-lookup"><span data-stu-id="dd463-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="dd463-104">Advanced Group Policy Management consente agli approvatori di ripristinare un oggetto Criteri di gruppo eliminato dal Cestino e di restituirlo all'archivio.</span><span class="sxs-lookup"><span data-stu-id="dd463-104">Advanced Group Policy Management (AGPM) enables Approvers to restore a deleted Group Policy object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="dd463-105">Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="dd463-105">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="dd463-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="dd463-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="dd463-107">Per ripristinare un oggetto Criteri di stato eliminato</span><span class="sxs-lookup"><span data-stu-id="dd463-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="dd463-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="dd463-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="dd463-109">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di stato eliminati.</span><span class="sxs-lookup"><span data-stu-id="dd463-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="dd463-110">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di ripristino e quindi scegliere **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="dd463-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="dd463-111">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd463-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="dd463-112">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="dd463-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="dd463-113">L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .</span><span class="sxs-lookup"><span data-stu-id="dd463-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="dd463-114">**Nota**  Se un oggetto Criteri di stato è stato eliminato dall'ambiente di produzione, il suo ripristino nell'archivio non verrà ridistribuito automaticamente nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="dd463-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="dd463-115">Per restituire il GPO all'ambiente di produzione, distribuire il GPO.</span><span class="sxs-lookup"><span data-stu-id="dd463-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="dd463-116">Per informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="dd463-116">For information, see [Deploy a GPO](deploy-a-gpo.md).</span></span>

 

### <span data-ttu-id="dd463-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="dd463-117">Additional considerations</span></span>

-   <span data-ttu-id="dd463-118">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="dd463-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="dd463-119">In particolare, devi avere il **contenuto dell'elenco** e **modificare le impostazioni**, **distribuire GPO**o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="dd463-119">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="dd463-120">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="dd463-120">Additional references</span></span>

-   [<span data-ttu-id="dd463-121">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="dd463-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





