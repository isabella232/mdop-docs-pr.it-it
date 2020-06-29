---
title: Distribuzione di App-V 5.1 Sequencer e del client
description: Distribuzione di App-V 5.1 Sequencer e del client
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805824"
---
# <span data-ttu-id="11c0e-103">Distribuzione di App-V 5.1 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="11c0e-103">Deploying the App-V 5.1 Sequencer and Client</span></span>


<span data-ttu-id="11c0e-104">Il sequencer e il client di Microsoft Application Virtualization (App-V) 5,1 consentono agli amministratori di virtualizzare ed eseguire applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="11c0e-104">The Microsoft Application Virtualization (App-V) 5.1 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="11c0e-105">Distribuire il client</span><span class="sxs-lookup"><span data-stu-id="11c0e-105">Deploy the client</span></span>


<span data-ttu-id="11c0e-106">Il client App-V 5,1 è il componente che esegue un'applicazione virtualizzata in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11c0e-106">The App-V 5.1 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="11c0e-107">Il client consente agli utenti di interagire con le icone e fare doppio clic su tipi di file, in modo che possano avviare un'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="11c0e-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="11c0e-108">Il client può anche ottenere il contenuto dell'applicazione virtuale dal server di gestione.</span><span class="sxs-lookup"><span data-stu-id="11c0e-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="11c0e-109">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="11c0e-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-51gb18030.md)

[<span data-ttu-id="11c0e-110">Come disinstallare il client App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="11c0e-110">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)

[<span data-ttu-id="11c0e-111">Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="11c0e-111">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## <span data-ttu-id="11c0e-112">Impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="11c0e-112">Client Configuration Settings</span></span>


<span data-ttu-id="11c0e-113">Il client App-V 5,1 archivia la configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="11c0e-113">The App-V 5.1 client stores its configuration in the registry.</span></span> <span data-ttu-id="11c0e-114">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="11c0e-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="11c0e-115">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="11c0e-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="11c0e-116">Informazioni sulle impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="11c0e-116">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

## <span data-ttu-id="11c0e-117">Configurare il client tramite il modello ADMX e i criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="11c0e-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="11c0e-118">È possibile usare il modello Microsoft ADMX per configurare le impostazioni client per il client App-V 5,1 e il client Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="11c0e-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.1 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="11c0e-119">Il modello ADMX gestisce le configurazioni client comuni usando un'infrastruttura di criteri di gruppo esistente e include le impostazioni per la configurazione client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="11c0e-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.1 client configuration.</span></span>

<span data-ttu-id="11c0e-120">**Importante**  Puoi ottenere il modello ADMX App-V 5,1 dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="11c0e-120">**Important** You can obtain the App-V 5.1 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="11c0e-121">Dopo aver scaricato e installato il modello ADMX, eseguire la procedura seguente nel computer che verrà usato per gestire i criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="11c0e-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="11c0e-122">Si tratta in genere del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="11c0e-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="11c0e-123">Salvare il file con **estensione ADMX** nella directory seguente: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="11c0e-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="11c0e-124">Salvare il file con estensione **ADML** nella directory seguente: \*\*Windows \ \ PolicyDefinitions \ \ &lt; Language directory &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="11c0e-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="11c0e-125">Dopo aver completato la procedura descritta in precedenza, è possibile gestire le impostazioni di configurazione del client App-V 5,1 con la console **Gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="11c0e-125">After you have completed the preceding steps, you can manage the App-V 5.1 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="11c0e-126">Il client App-V 5,1 archivia anche la configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="11c0e-126">The App-V 5.1 client also stores its configuration in the registry.</span></span> <span data-ttu-id="11c0e-127">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="11c0e-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="11c0e-128">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="11c0e-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="11c0e-129">Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="11c0e-129">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="11c0e-130">Distribuire il client tramite la modalità di archiviazione contenuto condivisa</span><span class="sxs-lookup"><span data-stu-id="11c0e-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="11c0e-131">La modalità SCS (Shared Content Store) App-V 5,1 consente ai client SCS App-V 5,1 di eseguire applicazioni virtualizzate senza salvare localmente i dati del pacchetto associati.</span><span class="sxs-lookup"><span data-stu-id="11c0e-131">The App-V 5.1 Shared Content Store (SCS) mode enables the SCS App-V 5.1 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="11c0e-132">Tutti i dati del pacchetto virtualizzato necessari vengono trasmessi attraverso la rete; Devi quindi usare la modalità SCS solo in ambienti con una connessione veloce.</span><span class="sxs-lookup"><span data-stu-id="11c0e-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="11c0e-133">I Servizi Desktop remoto (RDS) e la versione standard del client App-V 5,1 sono supportati con la modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="11c0e-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.1 client are supported with SCS mode.</span></span>

<span data-ttu-id="11c0e-134">**Importante**  Se il client App-V 5,1 è configurato per l'esecuzione in modalità SCS, la posizione in cui vengono trasmessi i pacchetti App-V 5,1 deve essere disponibile, in caso contrario il pacchetto virtualizzato non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="11c0e-134">**Important** If the App-V 5.1 client is configured to run in the SCS mode, the location where the App-V 5.1 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="11c0e-135">Inoltre, non è consigliabile distribuire applicazioni virtualizzate nei computer che eseguono il client App-V 5,1 in modalità SCS su Internet.</span><span class="sxs-lookup"><span data-stu-id="11c0e-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.1 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="11c0e-136">Inoltre, il SCS non è una posizione fisica che contiene pacchetti virtualizzati.</span><span class="sxs-lookup"><span data-stu-id="11c0e-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="11c0e-137">Si tratta di una modalità che consente al client App-V 5,1 di trasmettere i dati del pacchetto virtualizzato necessario in tutta la rete.</span><span class="sxs-lookup"><span data-stu-id="11c0e-137">It is a mode that allows the App-V 5.1 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="11c0e-138">La modalità SCS è utile negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="11c0e-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="11c0e-139">Distribuzioni di Virtual Desktop Infrastructure (VDI)</span><span class="sxs-lookup"><span data-stu-id="11c0e-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="11c0e-140">Distribuzioni Remote Desktop Services (RDS)</span><span class="sxs-lookup"><span data-stu-id="11c0e-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="11c0e-141">Per usare SCS nell'ambiente, è necessario abilitare il client App-V 5,1 per l'esecuzione in modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="11c0e-141">To use SCS in your environment, you must enable the App-V 5.1 client to run in SCS mode.</span></span> <span data-ttu-id="11c0e-142">Questa impostazione deve essere specificata durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="11c0e-142">This setting should be specified during installation.</span></span> <span data-ttu-id="11c0e-143">Per impostazione predefinita, il client non è configurato per l'uso della modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="11c0e-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="11c0e-144">È consigliabile installare il client usando la procedura suggerita se si prevede di usare SCS.</span><span class="sxs-lookup"><span data-stu-id="11c0e-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="11c0e-145">Tuttavia, puoi configurare un client App-V 5,1 esistente per l'esecuzione in modalità SCS immettendo il comando PowerShell seguente nel computer che esegue il client App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="11c0e-145">However, you can configure an existing App-V 5.1 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.1 client:</span></span>

**<span data-ttu-id="11c0e-146">set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="11c0e-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="11c0e-147">Potrebbero verificarsi casi in cui l'amministratore carica alcune applicazioni virtuali nel computer che esegue il client App-V 5,1 in modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="11c0e-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.1 client in SCS mode.</span></span> <span data-ttu-id="11c0e-148">Questa operazione può essere eseguita con i comandi di PowerShell per aggiungere, pubblicare e montare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="11c0e-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="11c0e-149">Ad esempio, se un pacchetto è precaricato in tutti i computer, l'amministratore può aggiungere, pubblicare e montare il pacchetto usando i comandi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="11c0e-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="11c0e-150">Il pacchetto non eseguirebbe il flusso in tutta la rete perché sarebbe archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="11c0e-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="11c0e-151">Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="11c0e-151">How to Install the App-V 5.1 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## <span data-ttu-id="11c0e-152">Distribuire il sequencer</span><span class="sxs-lookup"><span data-stu-id="11c0e-152">Deploy the Sequencer</span></span>


<span data-ttu-id="11c0e-153">Sequencer è uno strumento usato per convertire le applicazioni standard in pacchetti virtuali per la distribuzione in computer che eseguono il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="11c0e-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="11c0e-154">Il sequencer aiuta a creare un processo di conversione semplice e prevedibile con modifiche minime ai flussi di lavoro di sequenziazione precedenti.</span><span class="sxs-lookup"><span data-stu-id="11c0e-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="11c0e-155">Inoltre, il Sequencer consente agli utenti di configurare più facilmente le applicazioni per abilitare le connessioni delle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="11c0e-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="11c0e-156">Per un elenco delle modifiche apportate all'App-V 5,1 sequencer, vedere [informazioni su App-v 5,1](about-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="11c0e-156">For a list of changes in the App-V 5.1 Sequencer, see [About App-V 5.1](about-app-v-51.md).</span></span>

[<span data-ttu-id="11c0e-157">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="11c0e-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> <span data-ttu-id="11c0e-158">Client e log sequenziatore di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="11c0e-158">App-V 5.1 Client and Sequencer logs</span></span>


<span data-ttu-id="11c0e-159">Puoi usare le informazioni del log sequencer di App-V 5,1 per risolvere i problemi relativi all'installazione e agli eventi operativi del sequencer durante l'uso di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="11c0e-159">You can use the App-V 5.1 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="11c0e-160">Le informazioni del log correlate al sequencer possono essere esaminate con il **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="11c0e-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="11c0e-161">Nella riga seguente viene visualizzato il percorso specifico per gli eventi correlati al sequencer:</span><span class="sxs-lookup"><span data-stu-id="11c0e-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="11c0e-162">**Visualizzatore eventi \ \ applicazioni e registri Servizi \ \ Microsoft \ \ App V**. Gli eventi correlati al sequencer sono presospesi con **appv \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="11c0e-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="11c0e-163">Gli eventi correlati al client sono presospesi con **appv \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="11c0e-163">Client-related events are prepended with **AppV\_Client**.</span></span>

## <span data-ttu-id="11c0e-164">Altre risorse per la distribuzione di Sequencer e client</span><span class="sxs-lookup"><span data-stu-id="11c0e-164">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="11c0e-165">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="11c0e-165">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="11c0e-166">Pianificazione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="11c0e-166">Planning for App-V 5.1</span></span>](planning-for-app-v-51.md)






 

 





