---
title: Come creare un ambiente di test
description: Come creare un ambiente di test
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827286"
---
# <span data-ttu-id="5d5e4-103">Come creare un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="5d5e4-103">How to Create a Test Environment</span></span>


<span data-ttu-id="5d5e4-104">Di seguito sono riportati alcuni passaggi e istruzioni utili per creare un ambiente di test che è possibile usare per testare il pacchetto dell'area di lavoro MED-V localmente prima di distribuirlo in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="5d5e4-105">Questa sezione fornisce indicazioni su come creare un ambiente di test, manualmente o usando un sistema di distribuzione elettronica del software.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="5d5e4-106">Per creare un ambiente di test usando un ESD</span><span class="sxs-lookup"><span data-stu-id="5d5e4-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="5d5e4-107">Usa il metodo aziendale di distribuzione del software in tutta l'organizzazione per distribuire i componenti necessari seguenti in un computer di test.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="5d5e4-108">Installarle nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="5d5e4-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="5d5e4-109">**Windows Virtual PC** -se non è già installato.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="5d5e4-110">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="5d5e4-111">**Aggiunte e aggiornamenti di Windows Virtual PC**, se non sono già installati.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="5d5e4-112">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="5d5e4-113">**File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="5d5e4-114">Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="5d5e4-115">**Programma di installazione dell'area di lavoro MED-v, VHD e configurazione eseguibile** -creato nel **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="5d5e4-116">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="5d5e4-117">**Importante**  Il programma eseguibile e la configurazione del disco rigido virtuale devono essere nella stessa cartella di installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="5d5e4-118">Installare quindi il programma di installazione dell'area di lavoro MED-V eseguendo setup.exe.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="5d5e4-119">Dopo aver installato tutti i componenti nel computer di test, eseguire l'agente host MED-V per iniziare la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="5d5e4-120">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="5d5e4-121">**Nota**  Se non è possibile eseguire fisicamente l'agente host MED-V nel computer di test, viene avviata automaticamente la prima volta che il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="5d5e4-122">La prima volta che viene avviata la configurazione e può richiedere dieci minuti o più per terminare.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="5d5e4-123">Per informazioni su come testare le impostazioni di configurazione quando è in esecuzione la configurazione iniziale, vedere [come verificare le impostazioni di configurazione per la prima volta](how-to-verify-first-time-setup-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="5d5e4-124">Per creare manualmente un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="5d5e4-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="5d5e4-125">Installare l'agente host MED-V in un ambiente di test locale che include prerequisiti MED-V, ad esempio Windows Virtual PC con aggiunte e aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="5d5e4-126">Per informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="5d5e4-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="5d5e4-127">Copiare i file dell'area di lavoro MED-V nell'ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="5d5e4-128">I file dell'area di lavoro MED-V si trovano nella cartella di destinazione specificata nel **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="5d5e4-129">**Importante**  Il programma eseguibile e la configurazione del disco rigido virtuale devono trovarsi nella stessa cartella dell'ambiente di test di installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="5d5e4-130">Installare l'area di lavoro MED-V eseguendo setup.exe.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="5d5e4-131">Avviare la configurazione per la prima volta eseguendo l'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="5d5e4-132">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="5d5e4-133">La prima volta che viene avviata la configurazione e può richiedere diversi minuti per il completamento, a seconda delle dimensioni del VHD specificato.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="5d5e4-134">Ora si è pronti per testare le diverse impostazioni per la configurazione, la pubblicazione delle applicazioni e il reindirizzamento degli URL specificati per l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="5d5e4-135">**Nota**  Per impostazione predefinita, MED-V esegue l'override dei criteri di blocco dello schermo nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="5d5e4-136">Tuttavia, questo non pone un problema di sicurezza perché il computer host rispetta ancora i criteri di blocco dello schermo.</span><span class="sxs-lookup"><span data-stu-id="5d5e4-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="5d5e4-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d5e4-137">Related topics</span></span>


[<span data-ttu-id="5d5e4-138">Come verificare le impostazioni della prima configurazione</span><span class="sxs-lookup"><span data-stu-id="5d5e4-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="5d5e4-139">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="5d5e4-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="5d5e4-140">Come verificare il reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="5d5e4-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





