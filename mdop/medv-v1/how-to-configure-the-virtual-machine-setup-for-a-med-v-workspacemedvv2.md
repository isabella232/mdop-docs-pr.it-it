---
title: Come configurare la macchina virtuale per un'area di lavoro MED-V
description: Come configurare la macchina virtuale per un'area di lavoro MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827075"
---
# <span data-ttu-id="e0475-103">Come configurare la macchina virtuale per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="e0475-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="e0475-104">Tutte le impostazioni di configurazione della macchina virtuale sono configurate nel modulo **criteri** , nella scheda **configurazione VM** .</span><span class="sxs-lookup"><span data-stu-id="e0475-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="e0475-105">Come configurare la configurazione della macchina virtuale per un'area di lavoro MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="e0475-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="e0475-106">Per configurare la configurazione della macchina virtuale per un'area di lavoro MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="e0475-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="e0475-107">Fare clic su un'area di lavoro MED-V persistente da configurare.</span><span class="sxs-lookup"><span data-stu-id="e0475-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="e0475-108">Nella sezione **configurazione di VM persistente** configurare le proprietà come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e0475-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="e0475-109">Nota</span><span class="sxs-lookup"><span data-stu-id="e0475-109">Note</span></span>**  
    <span data-ttu-id="e0475-110">Le proprietà di configurazione di VM persistenti sono abilitate solo per un'area di lavoro MED-V persistente.</span><span class="sxs-lookup"><span data-stu-id="e0475-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="e0475-111">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="e0475-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="e0475-112">Proprietà di configurazione della VM persistente</span><span class="sxs-lookup"><span data-stu-id="e0475-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0475-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0475-113">Property</span></span></th>
<th align="left"><span data-ttu-id="e0475-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0475-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0475-115">Eseguire l'installazione di VM</span><span class="sxs-lookup"><span data-stu-id="e0475-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0475-116">Selezionare questa casella di controllo per eseguire uno script di configurazione la prima volta che viene eseguita l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="e0475-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0475-117">Editor script</span><span class="sxs-lookup"><span data-stu-id="e0475-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0475-118">Fare clic per configurare lo script di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e0475-118">Click to configure the setup script.</span></span> <span data-ttu-id="e0475-119">Per altre informazioni, vedere <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> come configurare le azioni di script </a> .</span><span class="sxs-lookup"><span data-stu-id="e0475-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e0475-120">Nota</span><span class="sxs-lookup"><span data-stu-id="e0475-120">Note</span></span></strong><br/><p><span data-ttu-id="e0475-121">Questo pulsante è abilitato solo quando <strong> è selezionata l'opzione Esegui script di configurazione VM </strong> .</span><span class="sxs-lookup"><span data-stu-id="e0475-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0475-122">Messaggio visualizzato durante l'esecuzione dello script</span><span class="sxs-lookup"><span data-stu-id="e0475-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0475-123">Messaggio da visualizzare durante l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="e0475-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="e0475-124">Se lasciato vuoto, viene visualizzato il messaggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="e0475-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e0475-125">Nota</span><span class="sxs-lookup"><span data-stu-id="e0475-125">Note</span></span></strong><br/><p><span data-ttu-id="e0475-126">Questo campo è abilitato solo quando <strong> è selezionata l'opzione Esegui script di configurazione VM </strong> .</span><span class="sxs-lookup"><span data-stu-id="e0475-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0475-127">Come configurare la configurazione della macchina virtuale per un'area di lavoro di Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="e0475-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="e0475-128">Per configurare la configurazione della macchina virtuale per un'area di lavoro di revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="e0475-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="e0475-129">Fare clic su un'area di lavoro di revertible MED-V da configurare.</span><span class="sxs-lookup"><span data-stu-id="e0475-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="e0475-130">Nella sezione **configurazione di REVERTIBLE VM** configurare le proprietà come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e0475-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="e0475-131">Nota</span><span class="sxs-lookup"><span data-stu-id="e0475-131">Note</span></span>**  
    <span data-ttu-id="e0475-132">Le proprietà di configurazione di revertible VM sono abilitate solo per un'area di lavoro di revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="e0475-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="e0475-133">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="e0475-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="e0475-134">Proprietà di configurazione di Revertible VM</span><span class="sxs-lookup"><span data-stu-id="e0475-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0475-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0475-135">Property</span></span></th>
<th align="left"><span data-ttu-id="e0475-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0475-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0475-137">Rinominare la VM in base al modello di nome computer</span><span class="sxs-lookup"><span data-stu-id="e0475-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0475-138">Selezionare questa casella di controllo per assegnare un nome univoco a ogni computer che usa l'area di lavoro MED-V in modo da poter distinguere tra più computer usando la stessa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="e0475-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="e0475-139">Per altre informazioni sulla configurazione dei nomi delle immagini del computer, vedere <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> come configurare le proprietà del modello di nome computer VM </a> .</span><span class="sxs-lookup"><span data-stu-id="e0475-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0475-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0475-140">Related topics</span></span>


[<span data-ttu-id="e0475-141">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="e0475-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="e0475-142">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="e0475-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="e0475-143">Esempi di configurazioni della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e0475-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









