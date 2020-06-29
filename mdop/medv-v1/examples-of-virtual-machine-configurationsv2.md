---
title: Esempi di configurazioni della macchina virtuale
description: Esempi di configurazioni della macchina virtuale
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824586"
---
# <span data-ttu-id="c94ea-103">Esempi di configurazioni della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c94ea-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="c94ea-104">Di seguito sono riportati alcuni esempi di configurazioni tipiche della macchina virtuale: una in un'area di lavoro MED-V persistente e una in un'area di lavoro di revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="c94ea-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="c94ea-105">**Nota**  Questi esempi non sono progettati per l'uso in tutti gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="c94ea-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="c94ea-106">Regolare la configurazione in base all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="c94ea-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="c94ea-107">Per configurare una configurazione tipica di un dominio in un'area di lavoro MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="c94ea-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="c94ea-108">Configurare Sysprep nell'immagine di base per creare un SID univoco.</span><span class="sxs-lookup"><span data-stu-id="c94ea-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="c94ea-109">Per altre informazioni, vedere [creazione di un'immagine Virtual PC per MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="c94ea-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="c94ea-110">Nella scheda **configurazione VM** selezionare la casella di controllo **Esegui configurazione VM** .</span><span class="sxs-lookup"><span data-stu-id="c94ea-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="c94ea-111">Nella sezione **modello di nome computer VM** configura il modello per il nome dell'immagine computer.</span><span class="sxs-lookup"><span data-stu-id="c94ea-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="c94ea-112">Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="c94ea-113">Fare clic su **editor di script**, quindi nella finestra di dialogo Editor di **script della configurazione VM** configurare le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c94ea-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="c94ea-114">Rinominare il computer</span><span class="sxs-lookup"><span data-stu-id="c94ea-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="c94ea-115">Riavviare Windows</span><span class="sxs-lookup"><span data-stu-id="c94ea-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="c94ea-116">Verificare la connettività</span><span class="sxs-lookup"><span data-stu-id="c94ea-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="c94ea-117">Join Domain</span><span class="sxs-lookup"><span data-stu-id="c94ea-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="c94ea-118">Disabilitare l'accesso automatico</span><span class="sxs-lookup"><span data-stu-id="c94ea-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="c94ea-119">Per altre informazioni, vedere [come configurare le azioni di script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="c94ea-120">Nel menu **criteri** fare clic su **commit**.</span><span class="sxs-lookup"><span data-stu-id="c94ea-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="c94ea-121">Per configurare una configurazione tipica in un'area di lavoro di revertible</span><span class="sxs-lookup"><span data-stu-id="c94ea-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="c94ea-122">Nella scheda **configurazione VM** selezionare la casella di controllo **Rinomina la VM in base al modello di nome computer** .</span><span class="sxs-lookup"><span data-stu-id="c94ea-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="c94ea-123">Nella sezione **modello di nome computer VM** configura il modello per il nome dell'immagine computer.</span><span class="sxs-lookup"><span data-stu-id="c94ea-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="c94ea-124">Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="c94ea-125">Nel menu **criteri** fare clic su **commit**.</span><span class="sxs-lookup"><span data-stu-id="c94ea-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="c94ea-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c94ea-126">Related topics</span></span>


[<span data-ttu-id="c94ea-127">Come configurare la macchina virtuale per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c94ea-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="c94ea-128">Come configurare le proprietà dei modelli di nome dei computer VM</span><span class="sxs-lookup"><span data-stu-id="c94ea-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="c94ea-129">Come configurare le azioni script</span><span class="sxs-lookup"><span data-stu-id="c94ea-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





