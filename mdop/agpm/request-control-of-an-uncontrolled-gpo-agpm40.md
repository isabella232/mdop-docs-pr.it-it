---
title: Richiedere il controllo di un oggetto Criteri di gruppo non controllato
description: Richiedere il controllo di un oggetto Criteri di gruppo non controllato
author: dansimp
ms.assetid: a34e0aeb-33a1-4c9f-b187-1d08493a785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfccd7285f82990c2447319485738131cf559f48
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818446"
---
# <span data-ttu-id="3f0c8-103">Richiedere il controllo di un oggetto Criteri di gruppo non controllato</span><span class="sxs-lookup"><span data-stu-id="3f0c8-103">Request Control of an Uncontrolled GPO</span></span>


<span data-ttu-id="3f0c8-104">Per specificare il controllo delle modifiche per un oggetto Criteri di gruppo (GPO) esistente, è necessario che il GPO sia controllato.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-104">To provide change control for an existing Group Policy Object (GPO), the GPO must be controlled.</span></span> <span data-ttu-id="3f0c8-105">A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere che venga controllato.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="3f0c8-106">Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="3f0c8-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="3f0c8-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3f0c8-108">Per controllare un oggetto Criteri di controllo non controllato</span><span class="sxs-lookup"><span data-stu-id="3f0c8-108">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="3f0c8-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3f0c8-110">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="3f0c8-111">Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="3f0c8-112">A meno che non si disponga di autorizzazioni speciali per controllare gli oggetti Criteri di controllo, è necessario inviare una richiesta di controllo.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="3f0c8-113">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="3f0c8-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="3f0c8-114">Digitare un commento da visualizzare nella **cronologia** del GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="3f0c8-115">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="3f0c8-116">Il GPO viene rimosso dall'elenco nella scheda non **controllata** e aggiunto alla scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="3f0c8-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="3f0c8-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3f0c8-117">Additional considerations</span></span>

-   <span data-ttu-id="3f0c8-118">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="3f0c8-119">In particolare, per il dominio è necessario disporre delle autorizzazioni per il **contenuto degli elenchi** e per le **impostazioni di lettura** .</span><span class="sxs-lookup"><span data-stu-id="3f0c8-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="3f0c8-120">Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="3f0c8-121">Il GPO verrà restituito alla scheda non **controllata** .</span><span class="sxs-lookup"><span data-stu-id="3f0c8-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="3f0c8-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="3f0c8-122">Additional references</span></span>

-   [<span data-ttu-id="3f0c8-123">Creazione o controllo di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3f0c8-123">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





