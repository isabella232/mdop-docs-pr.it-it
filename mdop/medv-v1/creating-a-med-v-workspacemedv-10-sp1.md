---
title: Creazione di un'area di lavoro MED-V
description: Creazione di un'area di lavoro MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824865"
---
# <span data-ttu-id="c6878-103">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="c6878-104">Un'area di lavoro MED-V è l'ambiente desktop in cui gli utenti finali interagiscono con la macchina virtuale fornita da MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6878-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="c6878-105">L'area di lavoro MED-V viene creata e personalizzata dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="c6878-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="c6878-106">È costituito da un'immagine e dal criterio, che definisce le regole e le funzionalità dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6878-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="c6878-107">È possibile creare più aree di lavoro MED-V, ognuna personalizzata con la propria configurazione, le impostazioni e le regole.</span><span class="sxs-lookup"><span data-stu-id="c6878-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="c6878-108">Un utente, un gruppo o più utenti o gruppi può essere associato a ogni area di lavoro MED-V, rendendo così disponibile l'area di lavoro MED-V solo per i computer dell'utente o del gruppo associato.</span><span class="sxs-lookup"><span data-stu-id="c6878-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="c6878-109">Come aggiungere un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="c6878-110">Per aggiungere un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="c6878-111">Fare clic sul pulsante Gestione **criteri** per aprire il modulo dei **criteri** .</span><span class="sxs-lookup"><span data-stu-id="c6878-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="c6878-112">Il modulo dei **criteri** è costituito dal menu **aree di lavoro** a sinistra e dalle schede **generale**, **macchina virtuale**, **distribuzione**, **applicazioni**, **Web**, **configurazione VM**, **rete**e **prestazioni** .</span><span class="sxs-lookup"><span data-stu-id="c6878-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="c6878-113">Nel menu **criteri** selezionare **nuova area di lavoro**oppure fare clic su **Aggiungi** per creare una nuova area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6878-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="c6878-114">Nel campo **nome** della scheda **generale** immettere il nome dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6878-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="c6878-115">Nel campo **Descrizione** immettere una descrizione per l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6878-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="c6878-116">Nel campo **informazioni contatto di supporto** immettere le informazioni di contatto per il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="c6878-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="c6878-117">Per altre informazioni sulla configurazione di un'area di lavoro MED-V, vedere [configurazione dei criteri di area di lavoro MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c6878-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="c6878-118">Come clonare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="c6878-119">Un'area di lavoro MED-V può essere clonata in modo da poter creare un'area di lavoro MED-V identica a un'area di lavoro MED-V esistente.</span><span class="sxs-lookup"><span data-stu-id="c6878-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="c6878-120">Per clonare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="c6878-121">Fare clic sull'area di lavoro MED-V per clonare.</span><span class="sxs-lookup"><span data-stu-id="c6878-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="c6878-122">Nel menu **criteri** selezionare **clona area di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="c6878-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="c6878-123">Viene creata una nuova area di lavoro MED-V con il nome &lt; area di lavoro originale Med-v &gt; -2.</span><span class="sxs-lookup"><span data-stu-id="c6878-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="c6878-124">Come eliminare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="c6878-125">Per eliminare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c6878-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="c6878-126">Nel modulo **criteri** , mentre il riquadro area di lavoro è in stato di attivazione, fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="c6878-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="c6878-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6878-127">Related topics</span></span>


[<span data-ttu-id="c6878-128">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="c6878-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





