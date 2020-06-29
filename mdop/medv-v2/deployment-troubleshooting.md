---
title: Risoluzione dei problemi relativi alla distribuzione
description: Risoluzione dei problemi relativi alla distribuzione
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822896"
---
# <span data-ttu-id="c7152-103">Risoluzione dei problemi relativi alla distribuzione</span><span class="sxs-lookup"><span data-stu-id="c7152-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="c7152-104">Questo argomento include informazioni utili per risolvere i problemi di distribuzione in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7152-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="c7152-105">Risoluzione dei problemi relativi alla distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="c7152-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="c7152-106">Il problema seguente può verificarsi quando si distribuisce MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="c7152-107">La soluzione consente di risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="c7152-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="c7152-108">Si verificano problemi se si installa MED-V solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c7152-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="c7152-109">MED-V supporta solo l'installazione di Packager area di lavoro MED-V, dell'agente host MED-V e dell'area di lavoro MED-V per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c7152-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="c7152-110">L'installazione per l'utente corrente causa solo errori nell'installazione dei componenti e nella configurazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="c7152-111">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c7152-111">Solution</span></span>**

<span data-ttu-id="c7152-112">Non usare mai l'opzione **ALLUSERS = ""** quando si installano i componenti MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="c7152-113">MED-V richiede l'uso esclusivo dello stack di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c7152-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="c7152-114">Solo uno stack di virtualizzazione può essere eseguito alla volta in un computer.</span><span class="sxs-lookup"><span data-stu-id="c7152-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="c7152-115">Windows Virtual PC deve usare lo stack virtuale e MED-V dipende da Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c7152-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="c7152-116">Di conseguenza, se tenti di distribuire o usare MED-V quando sono in esecuzione altre applicazioni che usano lo stack virtuale, MED-V non può essere eseguito o installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c7152-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="c7152-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c7152-117">Solution</span></span>**

<span data-ttu-id="c7152-118">Chiudere qualsiasi applicazione in esecuzione che usa lo stack di virtualizzazione prima di installare o eseguire MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="c7152-119">I tasti di scelta rapida rimangono dopo la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="c7152-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="c7152-120">Per impostazione predefinita, quando si disinstalla MED-V, i tasti di scelta rapida nel menu **Start** dell'utente finale vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="c7152-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="c7152-121">Tuttavia, in alcune situazioni, ad esempio per gli utenti finali che usano profili mobili, le scelte rapide da usare per le applicazioni pubblicate in MED-V restano nel menu **Start** dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="c7152-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="c7152-122">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c7152-122">Solution</span></span>**

<span data-ttu-id="c7152-123">Per eliminare manualmente i tasti di scelta rapida rimanenti nel menu **Start** , fare clic con il pulsante destro del mouse sui tasti di scelta rapida e quindi scegliere **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="c7152-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="c7152-124">Disabilitare l'impostazione di criteri di gruppo dei messaggi di accesso nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="c7152-125">Se il messaggio di accesso a Windows XP è abilitato nell'area di lavoro MED-V, l'utente finale deve eseguire l'accesso ogni volta che vuole aprire un'applicazione virtuale MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7152-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="c7152-126">In questo modo, viene creata un'esperienza utente scadente.</span><span class="sxs-lookup"><span data-stu-id="c7152-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="c7152-127">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c7152-127">Solution</span></span>**

<span data-ttu-id="c7152-128">Disabilitare le impostazioni di criteri di gruppo seguenti nella macchina virtuale MED-V:</span><span class="sxs-lookup"><span data-stu-id="c7152-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="c7152-129">Accesso interattivo: testo del messaggio per gli utenti che tentano l'accesso</span><span class="sxs-lookup"><span data-stu-id="c7152-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="c7152-130">Accesso interattivo: titolo del messaggio per gli utenti che tentano l'accesso</span><span class="sxs-lookup"><span data-stu-id="c7152-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="c7152-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7152-131">Related topics</span></span>


[<span data-ttu-id="c7152-132">Risoluzione dei problemi relativi alle operazioni</span><span class="sxs-lookup"><span data-stu-id="c7152-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 





