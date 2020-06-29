---
title: Come distribuire manualmente un'area di lavoro MED-V
description: Come distribuire manualmente un'area di lavoro MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827276"
---
# <span data-ttu-id="2028e-103">Come distribuire manualmente un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2028e-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="2028e-104">In alcuni casi potrebbe essere necessario distribuire manualmente l'area di lavoro MED-V, ad esempio se la società non usa un sistema di distribuzione del software elettronico per distribuire le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2028e-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="2028e-105">Questa sezione fornisce istruzioni su come distribuire manualmente un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2028e-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="2028e-106">Per distribuire manualmente un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2028e-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="2028e-107">Copiare tutte le applicazioni prerequisite e i file del pacchetto dell'area di lavoro MED-V in un'unità condivisa o in un DVD.</span><span class="sxs-lookup"><span data-stu-id="2028e-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="2028e-108">Di seguito è riportato un elenco delle applicazioni e dei file necessari.</span><span class="sxs-lookup"><span data-stu-id="2028e-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="2028e-109">**PC virtuale Windows**.</span><span class="sxs-lookup"><span data-stu-id="2028e-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="2028e-110">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="2028e-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="2028e-111">**Aggiunte e aggiornamenti di Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="2028e-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="2028e-112">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="2028e-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="2028e-113">**File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione).</span><span class="sxs-lookup"><span data-stu-id="2028e-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="2028e-114">Warning</span><span class="sxs-lookup"><span data-stu-id="2028e-114">Warning</span></span>**  
        <span data-ttu-id="2028e-115">Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="2028e-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="2028e-116">Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2028e-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="2028e-117">Installare gli elementi seguenti nell'ordine indicato.</span><span class="sxs-lookup"><span data-stu-id="2028e-117">Install the following in the order listed.</span></span> <span data-ttu-id="2028e-118">L'utente finale può eseguire questa attività manualmente oppure creare uno script per installare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2028e-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="2028e-119">Windows Virtual PC e le aggiunte e gli aggiornamenti di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="2028e-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="2028e-120">È necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="2028e-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="2028e-121">Agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="2028e-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="2028e-122">Nota</span><span class="sxs-lookup"><span data-stu-id="2028e-122">Note</span></span>**  
       <span data-ttu-id="2028e-123">Se è in corso, Internet Explorer deve essere riavviato prima che l'installazione dell'agente host MED-V possa terminare.</span><span class="sxs-lookup"><span data-stu-id="2028e-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="2028e-124">Completare la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="2028e-124">Complete first time setup.</span></span>

   <span data-ttu-id="2028e-125">Dopo l'installazione dell'area di lavoro MED-V, è possibile avviare MED-V.</span><span class="sxs-lookup"><span data-stu-id="2028e-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="2028e-126">Verrà avviata l'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="2028e-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="2028e-127">A questo punto è possibile avviare MED-V oppure avviare l'agente host MED-V in un secondo momento per completare la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="2028e-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="2028e-128">Per avviare l'agente host MED-V, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-v**.</span><span class="sxs-lookup"><span data-stu-id="2028e-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="2028e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2028e-129">Related topics</span></span>


[<span data-ttu-id="2028e-130">Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="2028e-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="2028e-131">Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7</span><span class="sxs-lookup"><span data-stu-id="2028e-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="2028e-132">Distribuzione del pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2028e-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)









