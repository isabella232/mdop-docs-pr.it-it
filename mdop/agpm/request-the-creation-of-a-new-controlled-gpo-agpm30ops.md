---
title: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
description: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: 4194c2f3-8116-4a35-be1a-81c84072daec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f9d7dd8a604bf2d2e3638142c070fed8b6d44e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820326"
---
# <span data-ttu-id="12712-103">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="12712-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="12712-104">A meno che non si sia un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo), è necessario richiedere la creazione di un nuovo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="12712-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="12712-105">Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="12712-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="12712-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="12712-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="12712-107">Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="12712-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="12712-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="12712-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="12712-109">Fare clic con il pulsante destro del mouse su **Cambia controllo**e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="12712-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="12712-110">A meno che non si disponga di autorizzazioni speciali per la creazione di GPO, è necessario inviare una richiesta di creazione.</span><span class="sxs-lookup"><span data-stu-id="12712-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="12712-111">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="12712-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="12712-112">Per ricevere una copia della richiesta, immettere l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="12712-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="12712-113">Digitare un nome per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="12712-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="12712-114">Facoltativo: digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="12712-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="12712-115">Per distribuire il nuovo GPO nell'ambiente di produzione subito dopo l'approvazione, fare clic su **Crea Live**.</span><span class="sxs-lookup"><span data-stu-id="12712-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="12712-116">Per creare il nuovo GPO offline senza distribuirlo immediatamente dopo l'approvazione, fare clic su **Crea offline**.</span><span class="sxs-lookup"><span data-stu-id="12712-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="12712-117">Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="12712-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="12712-118">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="12712-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="12712-119">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="12712-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="12712-120">Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="12712-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="12712-121">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="12712-121">Additional considerations</span></span>

-   <span data-ttu-id="12712-122">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore.</span><span class="sxs-lookup"><span data-stu-id="12712-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="12712-123">In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="12712-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="12712-124">Per ritirare la richiesta prima di approvarla, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="12712-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="12712-125">Il GPO verrà distrutto.</span><span class="sxs-lookup"><span data-stu-id="12712-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="12712-126">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="12712-126">Additional references</span></span>

-   [<span data-ttu-id="12712-127">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="12712-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





