---
title: Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato
description: Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818465"
---
# <span data-ttu-id="1cd64-103">Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato</span><span class="sxs-lookup"><span data-stu-id="1cd64-103">Request Control of a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="1cd64-104">Per usare Gestione avanzata Criteri di gruppo per specificare il controllo delle modifiche per un oggetto Criteri di gruppo esistente, è necessario che il GPO sia controllato con Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="1cd64-104">To use Advanced Group Policy Management (AGPM) to provide change control for an existing Group Policy object (GPO), the GPO must be controlled with AGPM.</span></span> <span data-ttu-id="1cd64-105">A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere che venga controllato.</span><span class="sxs-lookup"><span data-stu-id="1cd64-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="1cd64-106">Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="1cd64-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="1cd64-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="1cd64-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1cd64-108">Per controllare un oggetto Criteri di controllo non controllato in precedenza</span><span class="sxs-lookup"><span data-stu-id="1cd64-108">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="1cd64-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="1cd64-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1cd64-110">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.</span><span class="sxs-lookup"><span data-stu-id="1cd64-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="1cd64-111">Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.</span><span class="sxs-lookup"><span data-stu-id="1cd64-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="1cd64-112">A meno che non si disponga di autorizzazioni speciali per controllare gli oggetti Criteri di controllo, è necessario inviare una richiesta di controllo.</span><span class="sxs-lookup"><span data-stu-id="1cd64-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="1cd64-113">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="1cd64-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="1cd64-114">Digitare un commento da visualizzare nella **cronologia** del GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="1cd64-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="1cd64-115">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="1cd64-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="1cd64-116">Il GPO viene rimosso dall'elenco nella scheda non **controllata** e aggiunto alla scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="1cd64-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="1cd64-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="1cd64-117">Additional considerations</span></span>

-   <span data-ttu-id="1cd64-118">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore.</span><span class="sxs-lookup"><span data-stu-id="1cd64-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="1cd64-119">In particolare, per il dominio è necessario disporre delle autorizzazioni per il **contenuto degli elenchi** e per le **impostazioni di lettura** .</span><span class="sxs-lookup"><span data-stu-id="1cd64-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="1cd64-120">Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="1cd64-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="1cd64-121">Il GPO verrà restituito alla scheda non **controllata** .</span><span class="sxs-lookup"><span data-stu-id="1cd64-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="1cd64-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="1cd64-122">Additional references</span></span>

-   [<span data-ttu-id="1cd64-123">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1cd64-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





