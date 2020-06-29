---
title: Come disinstallare i componenti MED-V
description: Come disinstallare i componenti MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804671"
---
# <span data-ttu-id="5fb97-103">Come disinstallare i componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="5fb97-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="5fb97-104">In alcuni casi potrebbe essere necessario disinstallare tutti o parte dei componenti di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="5fb97-105">Ad esempio, sono stati risolti tutti i problemi di compatibilità dei sistemi operativi delle applicazioni oppure si vuole distribuire un'area di lavoro MED-V diversa nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="5fb97-106">In genere è possibile configurare il sistema ESD (Electronic Software Distribution) per disinstallare i componenti MED-V usando un programma di installazione basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="5fb97-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="5fb97-107">In alternativa, è possibile disinstallare manualmente tutti i componenti MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="5fb97-108">**Importante**  Prima di poter disinstallare l'agente host MED-V, è necessario prima disinstallare qualsiasi area di lavoro MED-V installata.</span><span class="sxs-lookup"><span data-stu-id="5fb97-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="5fb97-109">Usare le procedure seguenti per disinstallare i componenti MED-V dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="5fb97-110">Per disinstallare MED-V usando un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="5fb97-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="5fb97-111">Usa il sistema ESD per distribuire uno script che richiama il programma eseguibile uninstall.exe per ogni area di lavoro MED-V che vuoi disinstallare.</span><span class="sxs-lookup"><span data-stu-id="5fb97-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="5fb97-112">Il file si trova in C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="5fb97-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="5fb97-113">Puoi impostare un contrassegno per eseguire automaticamente il programma eseguibile di disinstallazione in modo che gli utenti finali non siano a conoscenza della disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="5fb97-114">Creare un pacchetto per distribuire il file di installazione dell'agente host MED-V in ogni computer in cui è stata disinstallata un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="5fb97-115">Configurare il pacchetto per eseguire la disinstallazione in modalità invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="5fb97-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="5fb97-116">Il client ESD riconosce la disponibilità dei nuovi pacchetti e avvia la disinstallazione dei pacchetti per la definizione e i requisiti.</span><span class="sxs-lookup"><span data-stu-id="5fb97-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="5fb97-117">Per disinstallare manualmente un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="5fb97-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="5fb97-118">Nel computer host fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="5fb97-119">Nella finestra **programmi e funzionalità** selezionare l'area di lavoro MED-V che si vuole rimuovere e quindi fare clic su **Disinstalla**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="5fb97-120">L'area di lavoro MED-V è denominata "area di lavoro MED-V- &lt; *area di lavoro \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="5fb97-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="5fb97-121">&lt;Verrà visualizzata la configurazione guidata Area di *lavoro \ _name* &gt; **Setup Wizard** .</span><span class="sxs-lookup"><span data-stu-id="5fb97-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="5fb97-122">Nella **Configurazione guidata**fare clic su **Avanti**e quindi su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="5fb97-123">Se si preferisce, selezionare la casella di controllo per eliminare il disco VHD master e i dischi differenze creati da MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="5fb97-124">Questa operazione non è necessaria, ma libera lo spazio su disco dopo la fine della disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="5fb97-125">Fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-125">Click **Remove**.</span></span>

    <span data-ttu-id="5fb97-126">**Nota**  Se MED-V è attualmente in uso, viene visualizzata una finestra di dialogo che chiede se si vuole arrestarla.</span><span class="sxs-lookup"><span data-stu-id="5fb97-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="5fb97-127">Fare clic su **Sì** per continuare con la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="5fb97-128">Fare clic su **No** per annullare la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5fb97-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="5fb97-129">In alternativa, è possibile rimuovere un'area di lavoro MED-V eseguendo il `uninstall.exe` file, in genere disponibile in C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="5fb97-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="5fb97-130">Per disinstallare manualmente l'agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="5fb97-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="5fb97-131">Nel computer host Windows 7 fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="5fb97-132">Nella finestra **programmi e funzionalità** selezionare **agente host MED-V**e quindi fare clic su **Disinstalla**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="5fb97-133">Windows Installer rimuove l'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="5fb97-134">**Nota**  Se si prova a disinstallare l'agente host MED-V prima di disinstallare l'area di lavoro MED-V, viene visualizzata una finestra di dialogo che indica che è necessario prima disinstallare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="5fb97-135">Fai clic su **OK** per continuare.</span><span class="sxs-lookup"><span data-stu-id="5fb97-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="5fb97-136">Per disinstallare manualmente il Packager area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="5fb97-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="5fb97-137">Nel computer host fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="5fb97-138">Nella finestra **programmi e funzionalità** selezionare **Packager area di lavoro MED-V**e quindi fare clic su **Disinstalla**.</span><span class="sxs-lookup"><span data-stu-id="5fb97-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="5fb97-139">Windows Installer rimuove il Packager area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5fb97-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="5fb97-140">**Nota**  Puoi disinstallare il Packager area di lavoro MED-V in qualsiasi momento senza influire sulle aree di lavoro MED-V distribuite.</span><span class="sxs-lookup"><span data-stu-id="5fb97-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="5fb97-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5fb97-141">Related topics</span></span>


[<span data-ttu-id="5fb97-142">Distribuire i componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="5fb97-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





