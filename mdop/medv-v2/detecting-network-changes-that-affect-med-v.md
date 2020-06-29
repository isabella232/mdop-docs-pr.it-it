---
title: Rilevamento delle modifiche di rete che influiscono su MED-V
description: Rilevamento delle modifiche di rete che influiscono su MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823375"
---
# <span data-ttu-id="bfab0-103">Rilevamento delle modifiche di rete che influiscono su MED-V</span><span class="sxs-lookup"><span data-stu-id="bfab0-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="bfab0-104">La soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di configurare l'ambiente per rilevare alcune modifiche di rete che potrebbero verificarsi dopo la distribuzione delle aree di lavoro MED-V e che possono influire su MED-V.</span><span class="sxs-lookup"><span data-stu-id="bfab0-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="bfab0-105">La caratteristica include un componente in uso nel sistema operativo guest notificato delle modifiche alla configurazione della rete nel computer host.</span><span class="sxs-lookup"><span data-stu-id="bfab0-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="bfab0-106">Consente a un utente non Microsoft ESD o a un'altra applicazione che viene eseguita nel guest di risolvere gli stessi endpoint di rete a cui si risolvono gli host ESD o l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfab0-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="bfab0-107">**Nota**  Questa caratteristica è disponibile solo se la macchina virtuale è configurata per la modalità NAT (Network Address Translation).</span><span class="sxs-lookup"><span data-stu-id="bfab0-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="bfab0-108">Se la macchina virtuale è configurata per la modalità a BRIDGE, non vengono generate indicazioni per la modifica.</span><span class="sxs-lookup"><span data-stu-id="bfab0-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="bfab0-109">In questa sezione vengono fornite informazioni e istruzioni per facilitare il monitoraggio delle modifiche apportate alla rete che possono influire su MED-V.</span><span class="sxs-lookup"><span data-stu-id="bfab0-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="bfab0-110">Per rilevare le modifiche di rete per MED-V</span><span class="sxs-lookup"><span data-stu-id="bfab0-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="bfab0-111">Dopo aver distribuito le aree di lavoro MED-V, è possibile monitorare le modifiche apportate a determinate configurazioni di rete preformando le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="bfab0-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="bfab0-112">Creare un file MOF (Managed Object Format) che cercherà le modifiche alla configurazione della rete che si desidera monitorare.</span><span class="sxs-lookup"><span data-stu-id="bfab0-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="bfab0-113">Il codice seguente mostra un esempio del file MOF che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="bfab0-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="bfab0-114">Compilare il file MOF.</span><span class="sxs-lookup"><span data-stu-id="bfab0-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="bfab0-115">Installare il file MOF nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="bfab0-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="bfab0-116">Dopo aver installato il file MOF, è possibile creare un abbonamento agli eventi che sottoscrive gli eventi di creazione, modifica o eliminazione di Strumentazione gestione Windows (WMI) per la classe **CCM \ _NetworkAdapters** .</span><span class="sxs-lookup"><span data-stu-id="bfab0-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="bfab0-117">In questo articolo vengono rilevate le modifiche seguenti all'host:</span><span class="sxs-lookup"><span data-stu-id="bfab0-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="bfab0-118">Ci sono modifiche di configurazione alla rete, ad esempio le modifiche apportate all'indirizzo IP o alla scheda di rete?</span><span class="sxs-lookup"><span data-stu-id="bfab0-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="bfab0-119">La rete è disponibile o non disponibile?</span><span class="sxs-lookup"><span data-stu-id="bfab0-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="bfab0-120">La configurazione della rete è stata cambiata dalla modalità BRIDGEd alla modalità NAT?</span><span class="sxs-lookup"><span data-stu-id="bfab0-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="bfab0-121">La configurazione della rete è stata modificata dalla modalità NAT alla modalità BRIDGEd?</span><span class="sxs-lookup"><span data-stu-id="bfab0-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="bfab0-122">Un componente MED-V nell'host monitora la rete per queste modifiche e quindi segnala l'ospite della modifica.</span><span class="sxs-lookup"><span data-stu-id="bfab0-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="bfab0-123">Un componente del Guest crea un'istanza WMI per monitorare l'area di lavoro MED-V per queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="bfab0-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="bfab0-124">L'abbonamento a un evento creato fornisce una notifica tramite il sistema WMI quando si verifica una o più di queste modifiche alla rete, ovvero creazione, modifica o eliminazione.</span><span class="sxs-lookup"><span data-stu-id="bfab0-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="bfab0-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfab0-125">Related topics</span></span>


[<span data-ttu-id="bfab0-126">Monitorare le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="bfab0-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="bfab0-127">Gestire le impostazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="bfab0-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





