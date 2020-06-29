---
title: Panoramica della distribuzione di MED-V 2.0
description: Panoramica della distribuzione di MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826106"
---
# <span data-ttu-id="1d00d-103">Panoramica della distribuzione di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="1d00d-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="1d00d-104">Questa sezione contiene informazioni generali e istruzioni su come installare e distribuire Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1d00d-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="1d00d-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="1d00d-105">Overview</span></span>


<span data-ttu-id="1d00d-106">MED-V 2,0 si basa su un modello di applicazione, in cui è possibile usare gli stessi metodi usati per distribuire le applicazioni per la distribuzione e la gestione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="1d00d-107">Una soluzione MED-V distribuita include due componenti: l'agente host MED-V e l'agente guest.</span><span class="sxs-lookup"><span data-stu-id="1d00d-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="1d00d-108">L'agente host MED-V è installato sul desktop di Windows 7 e l'agente guest MED-V viene installato in Windows XP all'interno dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="1d00d-109">MED-V include anche un Packager area di lavoro MED-V che fornisce le informazioni e gli strumenti necessari per la creazione e la configurazione delle aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="1d00d-110">Importante</span><span class="sxs-lookup"><span data-stu-id="1d00d-110">Important</span></span>**  
<span data-ttu-id="1d00d-111">MED-V supporta solo l'installazione di Packager area di lavoro MED-V, dell'agente host MED-V e dell'area di lavoro MED-V per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="1d00d-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="1d00d-112">L'installazione di MED-V per l'utente corrente selezionando **ALLUSERS = ""** causa errori nell'installazione dei componenti e nella configurazione dell'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="1d00d-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="1d00d-113">File di installazione di MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-113">The MED-V Installation Files</span></span>

<span data-ttu-id="1d00d-114">MED-V include i file di installazione seguenti, necessari per l'uso di MED-V:</span><span class="sxs-lookup"><span data-stu-id="1d00d-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="1d00d-115">File di installazione dell'agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="1d00d-116">Il file di installazione dell'agente host è denominato MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1d00d-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="1d00d-117">Questo file è distribuito e installato in ogni computer dell'utente finale pertinente nell'ambito della distribuzione a livello aziendale di MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="1d00d-118">File di installazione del Packager area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="1d00d-119">Il file di installazione del Packager area di lavoro MED-V è denominato MED-V\_WorkspacePackager\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1d00d-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="1d00d-120">Usare questo file per installare il Packager area di lavoro MED-V in un computer in cui sono presenti i diritti e le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="1d00d-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="1d00d-121">L'amministratore desktop usa il Packager area di lavoro MED-V per creare e gestire aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="1d00d-122">Nota</span><span class="sxs-lookup"><span data-stu-id="1d00d-122">Note</span></span>**  
<span data-ttu-id="1d00d-123">L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="1d00d-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="1d00d-124">Processo di distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="1d00d-125">Di seguito è riportata una panoramica di alto livello sul processo di installazione e distribuzione di MED-V:</span><span class="sxs-lookup"><span data-stu-id="1d00d-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="1d00d-126">Installare il Packager area di lavoro MED-V nel computer in cui sono presenti credenziali amministrative e che verrà usato per compilare i pacchetti dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="1d00d-127">Per altre informazioni, vedere [come installare il Packager area di lavoro MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="1d00d-128">Preparare l'immagine MED-V e creare i pacchetti dell'area di lavoro MED-v tramite Packager area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="1d00d-129">Per altre informazioni, vedere [operazioni per MED-V](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="1d00d-130">Distribuire i componenti MED-V necessari in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="1d00d-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="1d00d-131">I componenti necessari di MED-V sono Windows Virtual PC, l'agente host MED-V e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="1d00d-132">Importante</span><span class="sxs-lookup"><span data-stu-id="1d00d-132">Important</span></span>**  
<span data-ttu-id="1d00d-133">L'installazione dei componenti MED-V richiede le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="1d00d-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="1d00d-134">Se un utente finale sta installando MED-V, viene chiesto di immettere le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="1d00d-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="1d00d-135">In alternativa, le credenziali amministrative possono essere fornite nel contesto se si sta eseguendo l'installazione usando un sistema ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="1d00d-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="1d00d-136">Componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-136">The MED-V Components</span></span>

<span data-ttu-id="1d00d-137">I componenti MED-V distribuiti in tutta l'organizzazione sono conformi alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d00d-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="1d00d-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d00d-138">Windows Virtual PC</span></span>**

<span data-ttu-id="1d00d-139">Funzioni MED-V all'interno di immagini PC virtuali Windows per la soluzione di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="1d00d-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="1d00d-140">Sono necessari Windows Virtual PC e l'aggiornamento per Windows 7 (KB977206).</span><span class="sxs-lookup"><span data-stu-id="1d00d-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="1d00d-141">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="1d00d-142">File di installazione dell'agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="1d00d-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1d00d-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="1d00d-144">File di installazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="1d00d-145">I file di installazione dell'area di lavoro MED-V vengono creati quando si compila il pacchetto dell'area di lavoro MED-V che è costituito dai seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d00d-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="1d00d-146">Un programma eseguibile setup.exe che esegue l'installazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="1d00d-147">Un &lt; programma di installazione di MED-V \ _workspace \ _name &gt; . msi</span><span class="sxs-lookup"><span data-stu-id="1d00d-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="1d00d-148">Un &lt; VHD \ _filename &gt; file MEDV, che è il disco rigido virtuale compresso</span><span class="sxs-lookup"><span data-stu-id="1d00d-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="1d00d-149">File per le impostazioni di configurazione ( &lt; area di lavoro \ _name &gt; . reg e &lt; Workspace \ _name &gt; . ps1)</span><span class="sxs-lookup"><span data-stu-id="1d00d-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="1d00d-150">Per distribuire MED-V, copiare tutti i file di installazione necessari nel computer host o in una condivisione a cui è possibile accedere dal computer host.</span><span class="sxs-lookup"><span data-stu-id="1d00d-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="1d00d-151">Eseguire i file di installazione del componente per Windows Virtual PC, l'agente host MED-V e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="1d00d-152">Avviare quindi l'agente host MED-V per completare la prima configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="1d00d-153">È possibile eseguire l'installazione manualmente.</span><span class="sxs-lookup"><span data-stu-id="1d00d-153">You can perform the installation manually.</span></span> <span data-ttu-id="1d00d-154">Tuttavia, ti consigliamo di usare un metodo di distribuzione elettronica del software per automatizzare la distribuzione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="1d00d-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="1d00d-155">Per altre informazioni, vedere [come distribuire un'area di lavoro MED-V tramite un sistema di distribuzione elettronica del software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="1d00d-156">Nota</span><span class="sxs-lookup"><span data-stu-id="1d00d-156">Note</span></span>**  
<span data-ttu-id="1d00d-157">Per informazioni sugli argomenti della riga di comando disponibili per controllare le opzioni di installazione, vedere [Opzioni della riga di comando per i file di installazione di MED-V](command-line-options-for-med-v-installation-files.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="1d00d-158">Passaggi di distribuzione</span><span class="sxs-lookup"><span data-stu-id="1d00d-158">Deployment Steps</span></span>


<span data-ttu-id="1d00d-159">Quando si distribuisce MED-V in tutta l'organizzazione, sono presenti due considerazioni principali: installazione e configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="1d00d-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="1d00d-160">Installazione</span><span class="sxs-lookup"><span data-stu-id="1d00d-160">Installation</span></span>

1.  <span data-ttu-id="1d00d-161">**Windows Virtual PC** -durante l'installazione, MED-V controlla Windows Virtual PC e il relativo aggiornamento necessario per Windows 7 (KB977206).</span><span class="sxs-lookup"><span data-stu-id="1d00d-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="1d00d-162">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="1d00d-163">È possibile installare questi come parte delle installazioni di Windows 7 prima di installare MED-V oppure installarli come parte della distribuzione MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="1d00d-164">Tuttavia, MED-V non include un meccanismo per la distribuzione; devono essere distribuiti usando un sistema ESD (Electronic Software Distribution) o come parte dell'immagine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d00d-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="1d00d-165">Importante</span><span class="sxs-lookup"><span data-stu-id="1d00d-165">Important</span></span>**  
    <span data-ttu-id="1d00d-166">Quando si installano i componenti MED-V usando un file batch, è consigliabile specificare che Windows Virtual PC e Windows Virtual PC hotfix sono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="1d00d-167">Questo significa che Windows Update non causerà interferenze con il processo di installazione richiedendo un riavvio.</span><span class="sxs-lookup"><span data-stu-id="1d00d-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="1d00d-168">**Agente host MED-v** : installare l'agente host MED-v nel computer Windows 7 in cui verrà eseguito MED-v.</span><span class="sxs-lookup"><span data-stu-id="1d00d-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="1d00d-169">Questa operazione deve essere installata prima di installare l'area di lavoro MED-V e verificare che sia installato Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1d00d-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="1d00d-170">**Area di lavoro MED-v** : i file necessari per l'installazione vengono creati tramite il Packager area di lavoro MED-v, ovvero i file setup.exe, MEDV e MSI.</span><span class="sxs-lookup"><span data-stu-id="1d00d-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="1d00d-171">Per installare l'area di lavoro MED-V, eseguire setup.exe; Questo trigger gli altri file come richiesto.</span><span class="sxs-lookup"><span data-stu-id="1d00d-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="1d00d-172">L'installazione inserisce una voce nel registro di sistema sotto la chiave di esecuzione del computer locale per avviare l'agente host MED-V, che esegue sempre MED-V quando si avvia Windows.</span><span class="sxs-lookup"><span data-stu-id="1d00d-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="1d00d-173">Importante</span><span class="sxs-lookup"><span data-stu-id="1d00d-173">Important</span></span>**  
   <span data-ttu-id="1d00d-174">L'installazione dell'area di lavoro MED-V può essere eseguita in modo interattivo dall'utente finale o silenziosamente attraverso un sistema di distribuzione elettronica del software.</span><span class="sxs-lookup"><span data-stu-id="1d00d-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="1d00d-175">L'installazione dell'area di lavoro MED-V richiede le credenziali amministrative, pertanto gli utenti finali devono essere amministratori dei loro computer per installare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="1d00d-176">In alternativa, un sistema di distribuzione del software elettronico viene eseguito in genere nel contesto di sistema e dispone di autorizzazioni sufficienti.</span><span class="sxs-lookup"><span data-stu-id="1d00d-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="1d00d-177">Configurazione per la prima volta</span><span class="sxs-lookup"><span data-stu-id="1d00d-177">First Time Setup</span></span>

<span data-ttu-id="1d00d-178">Dopo aver installato MED-V e i componenti necessari, è necessario configurare MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="1d00d-179">La configurazione di MED-V è nota come configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="1d00d-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="1d00d-180">Usando il **Packager area di lavoro MED-V**puoi configurare la configurazione per la prima volta per l'esecuzione silenziosa o interattiva.</span><span class="sxs-lookup"><span data-stu-id="1d00d-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="1d00d-181">La configurazione per la prima volta di MED-V richiede agli utenti finali di immettere la propria password per l'autenticazione nell'area di lavoro MED-V, ma in caso contrario può essere quasi invisibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1d00d-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="1d00d-182">Le notifiche vengono visualizzate nell'area di notifica, ad esempio quando la configurazione per la prima volta è completa e le applicazioni sono pronte.</span><span class="sxs-lookup"><span data-stu-id="1d00d-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="1d00d-183">Di seguito sono riportate le azioni che si verificano durante la configurazione per la prima volta di MED-V:</span><span class="sxs-lookup"><span data-stu-id="1d00d-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="1d00d-184">Il disco rigido virtuale deve essere configurato.</span><span class="sxs-lookup"><span data-stu-id="1d00d-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="1d00d-185">La configurazione minima viene eseguita ed espande l'immagine di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d00d-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="1d00d-186">In genere, questo problema si verifica in una finestra nascosta, ma è possibile configurare MED-V per la visualizzazione durante questa configurazione.</span><span class="sxs-lookup"><span data-stu-id="1d00d-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="1d00d-187">Al termine della configurazione minima, è possibile eseguire i comandi che è necessario avere per la configurazione aggiuntiva, ad esempio l'installazione del software ESD o di altre applicazioni o la configurazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1d00d-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="1d00d-188">Queste operazioni possono essere chiamate nel file Sysprep. inf, ma non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="1d00d-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="1d00d-189">Per altre informazioni, vedere [configurazione di un'immagine PC virtuale Windows per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="1d00d-190">Ftscompletion.exe viene eseguito come ultimo passaggio della configurazione.</span><span class="sxs-lookup"><span data-stu-id="1d00d-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="1d00d-191">Questo processo completa la configurazione MED-V, aggiunge l'utente al gruppo RDP per consentire loro di accedere all'area di lavoro MED-V, copia i registri, segnala a MED-V che l'area di lavoro MED-V è pronta e quindi riavvia l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="1d00d-192">Questo processo può anche aggiungere l'utente come amministratore dell'area di lavoro MED-V se è stato configurato quando è stata creata l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d00d-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="1d00d-193">Ftscompletion.exe viene in genere chiamato tramite il file Sysprep, inf, ma può essere eseguito anche tramite un altro metodo, ad esempio uno script.</span><span class="sxs-lookup"><span data-stu-id="1d00d-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="1d00d-194">Tuttavia, Ftscompletion.exe deve essere l'ultima azione eseguita quando la workstation è configurata.</span><span class="sxs-lookup"><span data-stu-id="1d00d-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="1d00d-195">Per altre informazioni, vedere [configurazione di un'immagine PC virtuale Windows per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="1d00d-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="1d00d-196">Dopo aver riavviato l'area di lavoro MED-V Ftscompletion.exe, l'utente finale ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="1d00d-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="1d00d-197">Se non è stata salvata la password durante la configurazione per la prima volta, viene chiesto di nuovo.</span><span class="sxs-lookup"><span data-stu-id="1d00d-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="1d00d-198">L'area di lavoro MED-V viene quindi avviata e configurata per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1d00d-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="1d00d-199">La configurazione include l'applicazione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="1d00d-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="1d00d-200">È consigliabile applicare solo i criteri che hanno senso in un ambiente di compatibilità delle applicazioni per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d00d-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="1d00d-201">I criteri di personalizzazione desktop, ad esempio, in genere non devono essere applicati e devono essere disabilitati.</span><span class="sxs-lookup"><span data-stu-id="1d00d-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="1d00d-202">Per altre informazioni su come consentire solo i profili locali, vedere [impostazioni di criteri di gruppo per i profili utente mobili](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="1d00d-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="1d00d-203">Dopo aver completato la configurazione per la prima volta, l'utente finale riceverà una notifica che le applicazioni pubblicate sono pronte.</span><span class="sxs-lookup"><span data-stu-id="1d00d-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="1d00d-204">Sono quindi in grado di accedere alle applicazioni installate nell'area di lavoro MED-V dal menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="1d00d-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="1d00d-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d00d-205">Related topics</span></span>


[<span data-ttu-id="1d00d-206">Preparare l'ambiente di distribuzione per MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="1d00d-207">Distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="1d00d-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









