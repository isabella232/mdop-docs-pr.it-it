---
title: Come configurare le proprietà dei modelli di nome dei computer VM
description: Come configurare le proprietà dei modelli di nome dei computer VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827076"
---
# <span data-ttu-id="6c8df-103">Come configurare le proprietà dei modelli di nome dei computer VM</span><span class="sxs-lookup"><span data-stu-id="6c8df-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="6c8df-104">È possibile assegnare un modello di nome computer della macchina virtuale sia per revertible che per le aree di lavoro MED-V permanenti.</span><span class="sxs-lookup"><span data-stu-id="6c8df-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="6c8df-105">Revertible-gli amministratori possono assegnare un nome univoco a ogni istanza di area di lavoro di Revertible MED-V per distinguere tra più computer usando la stessa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="6c8df-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="6c8df-106">Persistente: in un'area di lavoro MED-V persistente, gli amministratori possono impostare un computer per la ridenominazione durante uno script di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6c8df-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="6c8df-107">Come assegnare un modello di nome computer della macchina virtuale a un'area di lavoro di Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="6c8df-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="6c8df-108">Per assegnare un modello di nome computer della macchina virtuale a un'area di lavoro di revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="6c8df-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="6c8df-109">Fare clic sull'area di lavoro revertible MED-V per configurare.</span><span class="sxs-lookup"><span data-stu-id="6c8df-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="6c8df-110">Nella sezione **configurazione di REVERTIBLE VM** selezionare la casella di controllo **Rinomina la VM in base al modello di nome computer** .</span><span class="sxs-lookup"><span data-stu-id="6c8df-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="6c8df-111">Nella sezione **modello di nome computer VM** Immetti il modello da usare per la denominazione delle immagini della macchina virtuale, usando le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c8df-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="6c8df-112">**Costante**: immettere testo gratuito che sarà costante in tutti i computer che usano l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="6c8df-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="6c8df-113">**Variabile**: immettere una variabile facendo clic su **Inserisci variabile**e quindi selezionare una delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c8df-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="6c8df-114">Nome utente</span><span class="sxs-lookup"><span data-stu-id="6c8df-114">User name</span></span>**

        -   **<span data-ttu-id="6c8df-115">Nome dominio</span><span class="sxs-lookup"><span data-stu-id="6c8df-115">Domain name</span></span>**

        -   **<span data-ttu-id="6c8df-116">Nome dell'host</span><span class="sxs-lookup"><span data-stu-id="6c8df-116">Host name</span></span>**

        -   **<span data-ttu-id="6c8df-117">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6c8df-117">Workspace name</span></span>**

        -   **<span data-ttu-id="6c8df-118">Nome macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6c8df-118">Virtual machine name</span></span>**

        <span data-ttu-id="6c8df-119">La variabile selezionata sarà specifica del computer che usa l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="6c8df-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="6c8df-120">Ad esempio, se è selezionato il **nome di dominio** , il nome univoco per ogni computer includerà il nome di dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="6c8df-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="6c8df-121">**Caratteri casuali**: immettere "\ #" per ogni carattere casuale da includere nello schema.</span><span class="sxs-lookup"><span data-stu-id="6c8df-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="6c8df-122">Ogni computer che usa l'area di lavoro MED-V avrà un suffisso della lunghezza specificata, che viene generata in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="6c8df-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="6c8df-123">Nota</span><span class="sxs-lookup"><span data-stu-id="6c8df-123">Note</span></span>**  
    <span data-ttu-id="6c8df-124">Il nome del computer ha un limite di 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6c8df-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="6c8df-125">Se il modello supera il limite, verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="6c8df-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="6c8df-126">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="6c8df-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="6c8df-127">Nota</span><span class="sxs-lookup"><span data-stu-id="6c8df-127">Note</span></span>**  
    <span data-ttu-id="6c8df-128">Un modello di nome computer VM revertible può essere assegnato solo quando si **Rinomina la VM in base ai modelli di nome computer** (nella sezione **configurazione di revertible VM** ) è selezionata.</span><span class="sxs-lookup"><span data-stu-id="6c8df-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="6c8df-129">Come assegnare un modello di nome computer della macchina virtuale a un'area di lavoro MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="6c8df-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="6c8df-130">Per assegnare un modello di nome computer macchina virtuale a un'area di lavoro MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="6c8df-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="6c8df-131">Fare clic sull'area di lavoro MED-V persistente da configurare.</span><span class="sxs-lookup"><span data-stu-id="6c8df-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="6c8df-132">Nella sezione **configurazione di VM persistente** fare clic su **Editor script**.</span><span class="sxs-lookup"><span data-stu-id="6c8df-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="6c8df-133">Nella finestra di dialogo **azioni script** fare clic su **Aggiungi**e quindi nel sottomenu fare clic su **Rinomina computer**.</span><span class="sxs-lookup"><span data-stu-id="6c8df-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="6c8df-134">Fare clic su **OK** per chiudere la finestra di dialogo **azioni script** .</span><span class="sxs-lookup"><span data-stu-id="6c8df-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="6c8df-135">Nella sezione **modello di nome computer VM** della scheda **configurazione VM** immettere il modello da usare per rinominare il computer, usando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6c8df-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="6c8df-136">**Costante**: immettere testo gratuito che verrà incluso nel nome del computer.</span><span class="sxs-lookup"><span data-stu-id="6c8df-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="6c8df-137">**Variabile**: immettere una variabile facendo clic su **Inserisci variabile**e quindi selezionare una delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c8df-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="6c8df-138">Nome utente</span><span class="sxs-lookup"><span data-stu-id="6c8df-138">User name</span></span>**

        -   **<span data-ttu-id="6c8df-139">Nome dominio</span><span class="sxs-lookup"><span data-stu-id="6c8df-139">Domain name</span></span>**

        -   **<span data-ttu-id="6c8df-140">Nome dell'host</span><span class="sxs-lookup"><span data-stu-id="6c8df-140">Host name</span></span>**

        -   **<span data-ttu-id="6c8df-141">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6c8df-141">Workspace name</span></span>**

        -   **<span data-ttu-id="6c8df-142">Nome macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6c8df-142">Virtual machine name</span></span>**

        <span data-ttu-id="6c8df-143">La variabile selezionata sarà specifica del computer che viene rinominato.</span><span class="sxs-lookup"><span data-stu-id="6c8df-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="6c8df-144">Ad esempio, se è selezionato il **nome di dominio** , il nome del computer includerà il nome di dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="6c8df-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="6c8df-145">**Caratteri casuali**: immettere "\ #" per ogni carattere casuale da includere nello schema.</span><span class="sxs-lookup"><span data-stu-id="6c8df-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="6c8df-146">Il computer avrà un suffisso della lunghezza specificata, che viene generata in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="6c8df-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="6c8df-147">Nota</span><span class="sxs-lookup"><span data-stu-id="6c8df-147">Note</span></span>**  
    <span data-ttu-id="6c8df-148">Il nome del computer ha un limite di 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6c8df-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="6c8df-149">Se il modello supera il limite, verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="6c8df-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="6c8df-150">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="6c8df-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="6c8df-151">Nota</span><span class="sxs-lookup"><span data-stu-id="6c8df-151">Note</span></span>**  
    <span data-ttu-id="6c8df-152">Il computer viene rinominato solo se è impostato come azione nella finestra di dialogo **azioni script** .</span><span class="sxs-lookup"><span data-stu-id="6c8df-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="6c8df-153">Per informazioni dettagliate, vedere [come configurare le azioni di script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6c8df-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="6c8df-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c8df-154">Related topics</span></span>


[<span data-ttu-id="6c8df-155">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="6c8df-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="6c8df-156">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="6c8df-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="6c8df-157">Come configurare le azioni script</span><span class="sxs-lookup"><span data-stu-id="6c8df-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="6c8df-158">Esempi di configurazioni della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6c8df-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









