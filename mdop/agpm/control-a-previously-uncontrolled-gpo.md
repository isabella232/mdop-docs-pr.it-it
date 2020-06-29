---
title: Controllare un oggetto Criteri di gruppo in precedenza non controllato
description: Controllare un oggetto Criteri di gruppo in precedenza non controllato
author: dansimp
ms.assetid: 452689a9-4e32-4e3b-8208-56353a82bf36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d7349b16b326a49b701efae5379c313bde0964f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818886"
---
# <span data-ttu-id="e6b99-103">Controllare un oggetto Criteri di gruppo in precedenza non controllato</span><span class="sxs-lookup"><span data-stu-id="e6b99-103">Control a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="e6b99-104">Per usare Advanced Group Policy Management per specificare il controllo delle modifiche per un oggetto Criteri di gruppo, è necessario prima di tutto controllare l'oggetto Criteri di gruppo con Advanced Manager.</span><span class="sxs-lookup"><span data-stu-id="e6b99-104">To use Advanced Group Policy Management (AGPM) to provide change control for a Group Policy object (GPO), you must first control the GPO with AGPM.</span></span>

<span data-ttu-id="e6b99-105">Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="e6b99-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e6b99-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e6b99-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e6b99-107">Per controllare un oggetto Criteri di controllo non controllato in precedenza</span><span class="sxs-lookup"><span data-stu-id="e6b99-107">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="e6b99-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="e6b99-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e6b99-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.</span><span class="sxs-lookup"><span data-stu-id="e6b99-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="e6b99-110">Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.</span><span class="sxs-lookup"><span data-stu-id="e6b99-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="e6b99-111">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6b99-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="e6b99-112">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="e6b99-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e6b99-113">Il GPO viene rimosso dall'elenco **nella scheda non controllata e** aggiunto alla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="e6b99-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="e6b99-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e6b99-114">Additional considerations</span></span>

-   <span data-ttu-id="e6b99-115">Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="e6b99-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e6b99-116">In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni **GPO** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="e6b99-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="e6b99-117">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="e6b99-117">Additional references</span></span>

-   [<span data-ttu-id="e6b99-118">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e6b99-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





