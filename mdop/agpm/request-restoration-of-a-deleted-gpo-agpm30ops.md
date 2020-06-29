---
title: Richiedere il ripristino di un oggetto Criteri di gruppo eliminato
description: Richiedere il ripristino di un oggetto Criteri di gruppo eliminato
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820366"
---
# <span data-ttu-id="bafc4-103">Richiedere il ripristino di un oggetto Criteri di gruppo eliminato</span><span class="sxs-lookup"><span data-stu-id="bafc4-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="bafc4-104">A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere il ripristino di un oggetto Criteri di gruppo eliminato dal Cestino per restituirlo all'archivio.</span><span class="sxs-lookup"><span data-stu-id="bafc4-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="bafc4-105">Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="bafc4-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="bafc4-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="bafc4-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="bafc4-107">Per richiedere il ripristino di un oggetto Criteri di stato eliminato</span><span class="sxs-lookup"><span data-stu-id="bafc4-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="bafc4-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="bafc4-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="bafc4-109">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di stato eliminati.</span><span class="sxs-lookup"><span data-stu-id="bafc4-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="bafc4-110">Fare clic con il pulsante destro del mouse sull'oggetto che si vuole ripristinare e quindi scegliere **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="bafc4-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="bafc4-111">A meno che non si disponga di autorizzazioni speciali per il ripristino di GPO, è necessario inviare una richiesta di ripristino dell'oggetto Criteri di ricerca eliminato.</span><span class="sxs-lookup"><span data-stu-id="bafc4-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="bafc4-112">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="bafc4-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="bafc4-113">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="bafc4-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="bafc4-114">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="bafc4-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="bafc4-115">L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .</span><span class="sxs-lookup"><span data-stu-id="bafc4-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="bafc4-116">**Nota**  Se un oggetto Criteri di stato è stato eliminato dall'ambiente di produzione, il suo ripristino nell'archivio non verrà ridistribuito automaticamente nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="bafc4-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="bafc4-117">Per restituire il GPO all'ambiente di produzione, distribuire il GPO.</span><span class="sxs-lookup"><span data-stu-id="bafc4-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="bafc4-118">Per informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="bafc4-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="bafc4-119">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="bafc4-119">Additional considerations</span></span>

-   <span data-ttu-id="bafc4-120">Per impostazione predefinita, è necessario essere un editor per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="bafc4-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="bafc4-121">In particolare, è necessario avere il **contenuto dell'elenco** e le autorizzazioni di **modifica delle impostazioni** per il GPO.</span><span class="sxs-lookup"><span data-stu-id="bafc4-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="bafc4-122">Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="bafc4-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="bafc4-123">Il GPO verrà restituito nella scheda **Cestino** .</span><span class="sxs-lookup"><span data-stu-id="bafc4-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="bafc4-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="bafc4-124">Additional references</span></span>

-   [<span data-ttu-id="bafc4-125">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bafc4-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





