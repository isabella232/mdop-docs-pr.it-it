---
title: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
description: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820316"
---
# <span data-ttu-id="ba13a-103">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="ba13a-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="ba13a-104">A meno che non si sia un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo), è necessario richiedere la creazione di un nuovo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ba13a-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="ba13a-105">Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ba13a-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ba13a-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="ba13a-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ba13a-107">Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ba13a-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="ba13a-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ba13a-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ba13a-109">Fare clic con il pulsante destro del mouse su **Cambia controllo**e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="ba13a-110">A meno che non si disponga di autorizzazioni speciali per la creazione di GPO, è necessario inviare una richiesta di creazione.</span><span class="sxs-lookup"><span data-stu-id="ba13a-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="ba13a-111">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="ba13a-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="ba13a-112">Per ricevere una copia della richiesta, immettere l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="ba13a-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="ba13a-113">Digitare un nome per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ba13a-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="ba13a-114">Facoltativo: digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ba13a-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="ba13a-115">Per distribuire il nuovo GPO nell'ambiente di produzione del dominio subito dopo l'approvazione, fare clic su **Crea Live**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-115">To deploy the new GPO to the production environment of the domain immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="ba13a-116">Per creare il nuovo GPO offline senza distribuirlo immediatamente dopo l'approvazione, fare clic su **Crea offline**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="ba13a-117">Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ba13a-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="ba13a-118">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="ba13a-119">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ba13a-120">Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="ba13a-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="ba13a-121">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ba13a-121">Additional considerations</span></span>

-   <span data-ttu-id="ba13a-122">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore.</span><span class="sxs-lookup"><span data-stu-id="ba13a-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="ba13a-123">In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="ba13a-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="ba13a-124">Per ritirare la richiesta prima di approvarla, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="ba13a-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="ba13a-125">Il GPO verrà distrutto.</span><span class="sxs-lookup"><span data-stu-id="ba13a-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="ba13a-126">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="ba13a-126">Additional references</span></span>

-   [<span data-ttu-id="ba13a-127">Creazione o controllo di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ba13a-127">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





