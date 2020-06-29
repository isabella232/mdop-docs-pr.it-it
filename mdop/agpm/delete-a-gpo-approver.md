---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820985"
---
# <span data-ttu-id="0a4b9-103">Eliminare un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a4b9-103">Delete a GPO</span></span>


<span data-ttu-id="0a4b9-104">Advanced Group Policy Management consente agli approvatori di eliminare un oggetto Criteri di gruppo controllato, spostandolo nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="0a4b9-105">Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="0a4b9-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="0a4b9-107">Per eliminare un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="0a4b9-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="0a4b9-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="0a4b9-109">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="0a4b9-110">Fare clic con il pulsante destro del mouse sul GPO da eliminare e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="0a4b9-111">Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio (Annulla controllo)**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="0a4b9-112">Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="0a4b9-113">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="0a4b9-114">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0a4b9-115">Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="0a4b9-116">Se l'oggetto Criteri di stato è stato eliminato solo dall'archivio, viene visualizzato anche nella scheda non **controllata** .</span><span class="sxs-lookup"><span data-stu-id="0a4b9-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="0a4b9-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0a4b9-117">Additional considerations</span></span>

-   <span data-ttu-id="0a4b9-118">Per impostazione predefinita, è necessario essere un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un GPO distribuito.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="0a4b9-119">In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="0a4b9-120">Per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un oggetto Criteri di stato dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="0a4b9-121">In particolare, è necessario avere **contenuto elenco** e **modificare le impostazioni** o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="0a4b9-122">Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su \*\* &lt; dominio &gt; \*\*e quindi su **oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="0a4b9-123">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="0a4b9-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="0a4b9-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="0a4b9-124">Additional references</span></span>

-   [<span data-ttu-id="0a4b9-125">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0a4b9-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





