---
title: Configurazione dei criteri dell'area di lavoro MED-V
description: Configurazione dei criteri dell'area di lavoro MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824856"
---
# <span data-ttu-id="b3d8e-103">Configurazione dei criteri dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="b3d8e-104">Un criterio di area di lavoro MED-V è un gruppo di impostazioni configurabili che definiscono l'esecuzione dell'ambiente virtualizzato e delle applicazioni nel computer host.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="b3d8e-105">Gli argomenti di questa sezione descrivono tutte le impostazioni configurabili nei criteri dell'area di lavoro MED-V e il modo in cui queste impostazioni influenzano l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="b3d8e-106">Sono disponibili i tipi di area di lavoro MED-V seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3d8e-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="b3d8e-107">**Persistente**: in un'area di lavoro MED-v persistente, tutte le modifiche e le aggiunte apportate dall'utente all'area di lavoro MED-v vengono salvate nell'area di lavoro MED-v tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="b3d8e-108">Inoltre, un'area di lavoro MED-V persistente viene in genere usata in un ambiente di dominio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="b3d8e-109">**Revertible**-in un'area di lavoro di Revertible Med-v, al termine di ogni sessione (ovvero quando l'area di lavoro MED-v viene interrotta), l'area di lavoro MED-v ritorna allo stato originale durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="b3d8e-110">Nessuna modifica o aggiunta che l'utente ha eseguito viene salvata nell'area di lavoro MED-V tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="b3d8e-111">Un'area di lavoro di revertible MED-V non può essere usata in un ambiente di dominio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="b3d8e-112">È importante decidere il tipo di area di lavoro MED-V che si sta creando prima di distribuire l'area di lavoro MED-V, perché non è consigliabile riconfigurare il tipo di area di lavoro MED-V dopo la distribuzione di un criterio agli utenti.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="b3d8e-113">**Nota**  Quando si configura un criterio, accanto a campi obbligatori non compilati viene visualizzato un simbolo di avviso.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="b3d8e-114">Se non viene compilato un campo obbligatorio, anche il simbolo viene visualizzato nella scheda.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="b3d8e-115">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="b3d8e-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-116">Come applicare le impostazioni generali a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-117">Descrive le impostazioni generali di un'area di lavoro MED-V e come applicarle a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-118">Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-119">Descrive le impostazioni della macchina virtuale per un'area di lavoro MED-V e come applicarle a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="b3d8e-120">Come configurare un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="b3d8e-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="b3d8e-121">Descrive come configurare gli utenti e i gruppi di dominio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="b3d8e-122">Come configurare le applicazioni pubblicate</span><span class="sxs-lookup"><span data-stu-id="b3d8e-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="b3d8e-123">Descrive le applicazioni e i menu pubblicati e come applicarli a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-124">Come configurare le impostazioni Web per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-125">Descrive le impostazioni Web disponibili per un'area di lavoro MED-V e come applicarle a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-126">Come configurare la macchina virtuale per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-127">Descrive la configurazione della macchina virtuale per un'area di lavoro MED-V e come applicarla a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-128">Come applicare le impostazioni di rete a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-129">Descrive le impostazioni di rete di un'area di lavoro MED-V e come applicarle a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="b3d8e-130">Come applicare le impostazioni delle prestazioni a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b3d8e-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="b3d8e-131">Descrive le impostazioni delle prestazioni di un'area di lavoro MED-V e come applicarle a un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="b3d8e-132">Come importare ed esportare un criterio</span><span class="sxs-lookup"><span data-stu-id="b3d8e-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="b3d8e-133">Descrive come importare ed esportare un criterio.</span><span class="sxs-lookup"><span data-stu-id="b3d8e-133">Describes how to import and export a policy.</span></span>

 

 





