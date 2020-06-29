---
title: Creare un nuovo oggetto Criteri di gruppo controllato
description: Creare un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: 5ce760f6-9f05-42b4-b787-7835ab8e324e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67c6af686b9ba7254cdaf93bd2d294b2d5bbb681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821096"
---
# <span data-ttu-id="674bb-103">Creare un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="674bb-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="674bb-104">I nuovi oggetti Criteri di gruppo creati tramite la cartella del **controllo di modifica** verranno controllati automaticamente, consentendo di gestirli.</span><span class="sxs-lookup"><span data-stu-id="674bb-104">New Group Policy Objects (GPOs) created through the **Change Control** folder will automatically be controlled, enabling you to manage them.</span></span>

<span data-ttu-id="674bb-105">Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento.</span><span class="sxs-lookup"><span data-stu-id="674bb-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="674bb-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="674bb-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="674bb-107">Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="674bb-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="674bb-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="674bb-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="674bb-109">Fare clic con il pulsante destro del mouse su **Cambia controllo**e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="674bb-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="674bb-110">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="674bb-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="674bb-111">Digitare un nome per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="674bb-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="674bb-112">Facoltativo: digitare un commento per il nuovo GPO da visualizzare nella **cronologia** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="674bb-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="674bb-113">Per distribuire immediatamente il nuovo GPO nell'ambiente di produzione del dominio, fare clic su **Crea Live**.</span><span class="sxs-lookup"><span data-stu-id="674bb-113">To immediately deploy the new GPO to the production environment of the domain, click **Create live**.</span></span> <span data-ttu-id="674bb-114">Per creare il nuovo GPO offline senza immediatamente distribuirlo, fare clic su **Crea offline**.</span><span class="sxs-lookup"><span data-stu-id="674bb-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="674bb-115">Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="674bb-115">Select the GPO template to use as a starting point for the new GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="674bb-116">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="674bb-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="674bb-117">Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="674bb-117">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="674bb-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="674bb-118">Additional considerations</span></span>

-   <span data-ttu-id="674bb-119">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="674bb-119">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="674bb-120">In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni **GPO** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="674bb-120">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="674bb-121">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="674bb-121">Additional references</span></span>

-   [<span data-ttu-id="674bb-122">Creazione o controllo di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="674bb-122">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





