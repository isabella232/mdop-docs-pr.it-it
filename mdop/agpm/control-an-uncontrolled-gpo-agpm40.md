---
title: Controllare un oggetto Criteri di gruppo non controllato
description: Controllare un oggetto Criteri di gruppo non controllato
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818905"
---
# <span data-ttu-id="02f9c-103">Controllare un oggetto Criteri di gruppo non controllato</span><span class="sxs-lookup"><span data-stu-id="02f9c-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="02f9c-104">Per specificare il controllo di modifica per un oggetto Criteri di gruppo, è necessario prima di tutto controllare il GPO.</span><span class="sxs-lookup"><span data-stu-id="02f9c-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="02f9c-105">Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento.</span><span class="sxs-lookup"><span data-stu-id="02f9c-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="02f9c-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="02f9c-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="02f9c-107">Per controllare un oggetto Criteri di controllo non controllato</span><span class="sxs-lookup"><span data-stu-id="02f9c-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="02f9c-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="02f9c-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="02f9c-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.</span><span class="sxs-lookup"><span data-stu-id="02f9c-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="02f9c-110">Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.</span><span class="sxs-lookup"><span data-stu-id="02f9c-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="02f9c-111">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="02f9c-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="02f9c-112">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="02f9c-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="02f9c-113">Il GPO viene rimosso dall'elenco **nella scheda non controllata e** aggiunto alla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="02f9c-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="02f9c-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="02f9c-114">Additional considerations</span></span>

-   <span data-ttu-id="02f9c-115">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="02f9c-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="02f9c-116">In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni **GPO** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="02f9c-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="02f9c-117">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="02f9c-117">Additional references</span></span>

-   [<span data-ttu-id="02f9c-118">Creazione o controllo di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="02f9c-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





