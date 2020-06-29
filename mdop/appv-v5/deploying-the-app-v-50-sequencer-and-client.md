---
title: Distribuzione di App-V 5.0 Sequencer e del client
description: Distribuzione di App-V 5.0 Sequencer e del client
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805847"
---
# <span data-ttu-id="a5d29-103">Distribuzione di App-V 5.0 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="a5d29-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="a5d29-104">Il sequencer e il client App-V 5,0 consentono agli amministratori di virtualizzare ed eseguire applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="a5d29-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="a5d29-105">Distribuire il client</span><span class="sxs-lookup"><span data-stu-id="a5d29-105">Deploy the client</span></span>


<span data-ttu-id="a5d29-106">Il client App-V 5,0 è il componente che esegue un'applicazione virtualizzata in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a5d29-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="a5d29-107">Il client consente agli utenti di interagire con le icone e fare doppio clic su tipi di file, in modo che possano avviare un'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="a5d29-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="a5d29-108">Il client può anche ottenere il contenuto dell'applicazione virtuale dal server di gestione.</span><span class="sxs-lookup"><span data-stu-id="a5d29-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="a5d29-109">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="a5d29-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="a5d29-110">Come disinstallare il client App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a5d29-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="a5d29-111">Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="a5d29-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="a5d29-112">Impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="a5d29-112">Client Configuration Settings</span></span>


<span data-ttu-id="a5d29-113">Il client App-V 5,0 archivia la configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5d29-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="a5d29-114">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="a5d29-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="a5d29-115">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5d29-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a5d29-116">Informazioni sulle impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="a5d29-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="a5d29-117">Configurare il client tramite il modello ADMX e i criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a5d29-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="a5d29-118">È possibile usare il modello Microsoft ADMX per configurare le impostazioni client per il client App-V 5,0 e il client Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a5d29-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="a5d29-119">Il modello ADMX gestisce le configurazioni client comuni usando un'infrastruttura di criteri di gruppo esistente e include le impostazioni per la configurazione client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a5d29-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="a5d29-120">**Importante**  Puoi ottenere il modello ADMX App-V 5,0 dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5d29-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="a5d29-121">Dopo aver scaricato e installato il modello ADMX, eseguire la procedura seguente nel computer che verrà usato per gestire i criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a5d29-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="a5d29-122">Si tratta in genere del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a5d29-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="a5d29-123">Salvare il file con **estensione ADMX** nella directory seguente: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a5d29-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="a5d29-124">Salvare il file con estensione **ADML** nella directory seguente: \*\*Windows \ \ PolicyDefinitions \ \ &lt; Language directory &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="a5d29-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="a5d29-125">Dopo aver completato la procedura descritta in precedenza, è possibile gestire le impostazioni di configurazione del client App-V 5,0 con la console **Gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="a5d29-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="a5d29-126">Il client App-V 5,0 archivia anche la configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5d29-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="a5d29-127">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="a5d29-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="a5d29-128">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5d29-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a5d29-129">Come modificare la configurazione del client App-V 5.0 usando il modello ADMX e Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a5d29-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="a5d29-130">Distribuire il client tramite la modalità di archiviazione contenuto condivisa</span><span class="sxs-lookup"><span data-stu-id="a5d29-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="a5d29-131">La modalità SCS (Shared Content Store) App-V 5,0 consente ai client SCS App-V 5,0 di eseguire applicazioni virtualizzate senza salvare localmente i dati del pacchetto associati.</span><span class="sxs-lookup"><span data-stu-id="a5d29-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="a5d29-132">Tutti i dati del pacchetto virtualizzato necessari vengono trasmessi attraverso la rete; Devi quindi usare la modalità SCS solo in ambienti con una connessione veloce.</span><span class="sxs-lookup"><span data-stu-id="a5d29-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="a5d29-133">I Servizi Desktop remoto (RDS) e la versione standard del client App-V 5,0 sono supportati con la modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="a5d29-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="a5d29-134">**Importante**  Se il client App-V 5,0 è configurato per l'esecuzione in modalità SCS, la posizione in cui vengono trasmessi i pacchetti App-V 5,0 deve essere disponibile, in caso contrario il pacchetto virtualizzato non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="a5d29-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="a5d29-135">Inoltre, non è consigliabile distribuire applicazioni virtualizzate nei computer che eseguono il client App-V 5,0 in modalità SCS su Internet.</span><span class="sxs-lookup"><span data-stu-id="a5d29-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="a5d29-136">Inoltre, il SCS non è una posizione fisica che contiene pacchetti virtualizzati.</span><span class="sxs-lookup"><span data-stu-id="a5d29-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="a5d29-137">Si tratta di una modalità che consente al client App-V 5,0 di trasmettere i dati del pacchetto virtualizzato necessario in tutta la rete.</span><span class="sxs-lookup"><span data-stu-id="a5d29-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="a5d29-138">La modalità SCS è utile negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5d29-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="a5d29-139">Distribuzioni di Virtual Desktop Infrastructure (VDI)</span><span class="sxs-lookup"><span data-stu-id="a5d29-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="a5d29-140">Distribuzioni Remote Desktop Services (RDS)</span><span class="sxs-lookup"><span data-stu-id="a5d29-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="a5d29-141">Per usare SCS nell'ambiente, è necessario abilitare il client App-V 5,0 per l'esecuzione in modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="a5d29-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="a5d29-142">Questa impostazione deve essere specificata durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a5d29-142">This setting should be specified during installation.</span></span> <span data-ttu-id="a5d29-143">Per impostazione predefinita, il client non è configurato per l'uso della modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="a5d29-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="a5d29-144">È consigliabile installare il client usando la procedura suggerita se si prevede di usare SCS.</span><span class="sxs-lookup"><span data-stu-id="a5d29-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="a5d29-145">Tuttavia, puoi configurare un client App-V 5,0 esistente per l'esecuzione in modalità SCS immettendo il comando PowerShell seguente nel computer che esegue il client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="a5d29-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="a5d29-146">set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="a5d29-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="a5d29-147">Potrebbero verificarsi casi in cui l'amministratore carica alcune applicazioni virtuali nel computer che esegue il client App-V 5,0 in modalità SCS.</span><span class="sxs-lookup"><span data-stu-id="a5d29-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="a5d29-148">Questa operazione può essere eseguita con i comandi di PowerShell per aggiungere, pubblicare e montare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a5d29-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="a5d29-149">Ad esempio, se un pacchetto è precaricato in tutti i computer, l'amministratore può aggiungere, pubblicare e montare il pacchetto usando i comandi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5d29-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="a5d29-150">Il pacchetto non eseguirebbe il flusso in tutta la rete perché sarebbe archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="a5d29-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="a5d29-151">Come installare il client App-V 5.0 per la modalità SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="a5d29-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="a5d29-152">Distribuire il sequencer</span><span class="sxs-lookup"><span data-stu-id="a5d29-152">Deploy the Sequencer</span></span>


<span data-ttu-id="a5d29-153">Sequencer è uno strumento usato per convertire le applicazioni standard in pacchetti virtuali per la distribuzione in computer che eseguono il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a5d29-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="a5d29-154">Il sequencer aiuta a creare un processo di conversione semplice e prevedibile con modifiche minime ai flussi di lavoro di sequenziazione precedenti.</span><span class="sxs-lookup"><span data-stu-id="a5d29-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="a5d29-155">Inoltre, il Sequencer consente agli utenti di configurare più facilmente le applicazioni per abilitare le connessioni delle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="a5d29-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="a5d29-156">Per un elenco delle modifiche apportate all'App-V 5,0 sequencer, vedere [novità di App-v 5,0](whats-new-in-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="a5d29-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="a5d29-157">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="a5d29-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="a5d29-158">Client e log sequenziatore di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a5d29-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="a5d29-159">Puoi usare le informazioni del log sequencer di App-V 5,0 per risolvere i problemi relativi all'installazione e agli eventi operativi del sequencer durante l'uso di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a5d29-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="a5d29-160">Le informazioni del log correlate al sequencer possono essere esaminate con il **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="a5d29-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="a5d29-161">Nella riga seguente viene visualizzato il percorso specifico per gli eventi correlati al sequencer:</span><span class="sxs-lookup"><span data-stu-id="a5d29-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="a5d29-162">**Visualizzatore eventi \ \ applicazioni e registri Servizi \ \ Microsoft \ \ App V**. Gli eventi correlati al sequencer sono presospesi con **appv \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="a5d29-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="a5d29-163">Gli eventi correlati al client sono presospesi con **appv \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="a5d29-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="a5d29-164">In App-V 5,0 SP3 sono stati consolidati alcuni log.</span><span class="sxs-lookup"><span data-stu-id="a5d29-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="a5d29-165">Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="a5d29-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="a5d29-166">Altre risorse per la distribuzione di Sequencer e client</span><span class="sxs-lookup"><span data-stu-id="a5d29-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="a5d29-167">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a5d29-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="a5d29-168">Pianificazione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a5d29-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 





