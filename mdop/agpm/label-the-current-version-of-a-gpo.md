---
title: Etichettare la versione corrente di un oggetto Criteri di gruppo
description: Etichettare la versione corrente di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 5e4e50f8-e4a8-4bda-aac4-1569d5fbd6a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a34232dfd1f7a755dd81cdecbe3d5d1957f01294
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820626"
---
# <span data-ttu-id="374e7-103">Etichettare la versione corrente di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="374e7-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="374e7-104">Puoi assegnare un'etichetta alla versione corrente di un oggetto Criteri di gruppo per facilitare l'identificazione nella cronologia.</span><span class="sxs-lookup"><span data-stu-id="374e7-104">You can label the current version of a Group Policy object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="374e7-105">Puoi usare un'etichetta per identificare una versione valida nota a cui puoi eseguire il rollback se si verifica un problema.</span><span class="sxs-lookup"><span data-stu-id="374e7-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="374e7-106">Inoltre, contrassegnando più oggetti Criteri di gruppo con la stessa etichetta contemporaneamente, è possibile contrassegnare gli oggetti Criteri di gruppo correlati che devono essere ripristinati nello stesso punto se il rollback deve essere necessario in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="374e7-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="374e7-107">Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="374e7-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="374e7-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="374e7-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="374e7-109">Per assegnare un'etichetta alla versione corrente di GPO nelle relative cronologie</span><span class="sxs-lookup"><span data-stu-id="374e7-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="374e7-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="374e7-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="374e7-111">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="374e7-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="374e7-112">Fare clic su un GPO per cui assegnare un'etichetta alla versione corrente.</span><span class="sxs-lookup"><span data-stu-id="374e7-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="374e7-113">Per selezionare più GPO, premere MAIUSC e fare clic sull'ultimo GPO in un gruppo di GPO contiguo oppure premere CTRL e fare clic su singoli GPO.</span><span class="sxs-lookup"><span data-stu-id="374e7-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="374e7-114">Fare clic con il pulsante destro del mouse su un GPO selezionato e quindi scegliere **etichetta**.</span><span class="sxs-lookup"><span data-stu-id="374e7-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="374e7-115">Digitare un'etichetta e un commento da visualizzare nella cronologia di ogni GPO selezionato e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="374e7-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="374e7-116">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="374e7-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="374e7-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="374e7-117">Additional considerations</span></span>

-   <span data-ttu-id="374e7-118">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="374e7-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="374e7-119">In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="374e7-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="374e7-120">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="374e7-120">Additional references</span></span>

-   [<span data-ttu-id="374e7-121">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="374e7-121">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





