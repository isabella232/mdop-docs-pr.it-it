---
title: Rinominare un oggetto Criteri di gruppo o un modello
description: Rinominare un oggetto Criteri di gruppo o un modello
author: dansimp
ms.assetid: 64a1aaf4-f672-48b5-94c6-473bf1076cf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 495fc090487ff324bc19c89dcd36ecf0efbcb151
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818495"
---
# <span data-ttu-id="232b9-103">Rinominare un oggetto Criteri di gruppo o un modello</span><span class="sxs-lookup"><span data-stu-id="232b9-103">Rename a GPO or Template</span></span>


<span data-ttu-id="232b9-104">È possibile rinominare un oggetto Criteri di gruppo (GPO) controllato o un modello.</span><span class="sxs-lookup"><span data-stu-id="232b9-104">You can rename a controlled Group Policy object (GPO) or a template.</span></span>

<span data-ttu-id="232b9-105">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di criteri di raggruppamento avanzati.</span><span class="sxs-lookup"><span data-stu-id="232b9-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="232b9-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="232b9-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="232b9-107">Per rinominare un GPO o un modello</span><span class="sxs-lookup"><span data-stu-id="232b9-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="232b9-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="232b9-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="232b9-109">Nella scheda **contenuto** fare clic sulla scheda **controlli** o **modelli** per visualizzare l'elemento da rinominare.</span><span class="sxs-lookup"><span data-stu-id="232b9-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="232b9-110">Fare clic con il pulsante destro del mouse sull'oggetto o sul modello da rinominare e scegliere **Rinomina**.</span><span class="sxs-lookup"><span data-stu-id="232b9-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="232b9-111">Digitare il nuovo nome per il GPO o il modello e un commento, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="232b9-111">Type the new name for the GPO or template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="232b9-112">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="232b9-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="232b9-113">L'oggetto Criteri di gruppo o il modello viene visualizzato sotto il nuovo nome nella scheda **contenuto** .</span><span class="sxs-lookup"><span data-stu-id="232b9-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="232b9-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="232b9-114">Additional considerations</span></span>

-   <span data-ttu-id="232b9-115">Per impostazione predefinita, è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato, un editor o un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="232b9-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="232b9-116">In particolare, è necessario avere il **contenuto dell'elenco** e le autorizzazioni di **modifica delle impostazioni** per il GPO.</span><span class="sxs-lookup"><span data-stu-id="232b9-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="232b9-117">Quando si rinomina un oggetto Criteri di distribuzione distribuito, il nome viene immediatamente modificato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="232b9-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="232b9-118">Il nome viene modificato nell'ambiente di produzione solo quando il GPO viene ridistribuito.</span><span class="sxs-lookup"><span data-stu-id="232b9-118">The name is changed in the production environment only when the GPO is redeployed.</span></span>

    <span data-ttu-id="232b9-119">Finché il GPO non viene ridistribuito o la copia di produzione viene eliminata, il vecchio nome è ancora in uso nell'ambiente di produzione e quindi non può essere usato per un altro GPO.</span><span class="sxs-lookup"><span data-stu-id="232b9-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="232b9-120">Analogamente, l'oggetto Criteri di stato nell'archivio non può essere rinominato nel nome originale finché l'oggetto Criteri di stato non è stato distribuito (modificando il nome della copia di produzione) o se la copia di produzione è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="232b9-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="232b9-121">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="232b9-121">Additional references</span></span>

-   [<span data-ttu-id="232b9-122">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="232b9-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





