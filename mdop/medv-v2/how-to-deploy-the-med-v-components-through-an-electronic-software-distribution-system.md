---
title: Come distribuire i componenti MED-V con un sistema di distribuzione elettronica del software
description: Come distribuire i componenti MED-V con un sistema di distribuzione elettronica del software
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824855"
---
# <span data-ttu-id="cc479-103">Come distribuire i componenti MED-V con un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="cc479-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="cc479-104">Un sistema di distribuzione elettronica del software può aiutare a trasferire in modo efficiente il software a molti computer tramite connessioni di rete lente o veloci.</span><span class="sxs-lookup"><span data-stu-id="cc479-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="cc479-105">La sezione seguente contiene informazioni e istruzioni utili per distribuire i componenti di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 in tutta l'organizzazione usando un sistema di distribuzione del software.</span><span class="sxs-lookup"><span data-stu-id="cc479-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="cc479-106">Nota</span><span class="sxs-lookup"><span data-stu-id="cc479-106">Note</span></span>**  
<span data-ttu-id="cc479-107">Indipendentemente dalla soluzione di distribuzione del software che si usa, è necessario avere familiarità con i requisiti della soluzione specifica.</span><span class="sxs-lookup"><span data-stu-id="cc479-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="cc479-108">Se si usa System Center Configuration Manager 2007 R2 o una versione successiva, vedere la [raccolta documenti di Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) nella raccolta tecnica Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="cc479-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="cc479-109">Importante</span><span class="sxs-lookup"><span data-stu-id="cc479-109">Important</span></span>**  
<span data-ttu-id="cc479-110">Se si usa System Center Configuration Manager 2007 SP2 e le aree di lavoro MED-V sono configurate per l'uso in modalità **NAT** , le macchine virtuali vengono classificate come client basati su Internet e non riescono a trovare i punti di distribuzione più vicini da cui scaricare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="cc479-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="cc479-111">L' [hotfix per migliorare le funzionalità per le VM gestite da Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) aggiunge nuove funzionalità alle macchine virtuali gestite da Med-v e configurate per l'uso in modalità **NAT** .</span><span class="sxs-lookup"><span data-stu-id="cc479-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="cc479-112">La nuova funzionalità consente alle macchine virtuali di accedere ai punti di distribuzione più vicini.</span><span class="sxs-lookup"><span data-stu-id="cc479-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="cc479-113">Di conseguenza, l'amministratore può gestire la macchina virtuale e il computer host nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="cc479-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="cc479-114">Questo hotfix deve essere installato per primo nel server del sito e quindi nel client.</span><span class="sxs-lookup"><span data-stu-id="cc479-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="cc479-115">L'aggiornamento è pubblicamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="cc479-115">The update is publicly available.</span></span> <span data-ttu-id="cc479-116">Tuttavia, potrebbe essere richiesto di accettare un contratto per i servizi Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc479-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="cc479-117">Seguire le istruzioni sulle pagine Web successive per recuperare questo hotfix.</span><span class="sxs-lookup"><span data-stu-id="cc479-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="cc479-118">Nota</span><span class="sxs-lookup"><span data-stu-id="cc479-118">Note</span></span>**  
<span data-ttu-id="cc479-119">È necessario installare Packager area di lavoro MED-V e creare le aree di lavoro MED-V prima di poter distribuire i componenti MED-V tramite il sistema di distribuzione del software.</span><span class="sxs-lookup"><span data-stu-id="cc479-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="cc479-120">Per altre informazioni su come preparare un'immagine e per creare le aree di lavoro MED-V, vedere [operazioni per MED-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="cc479-121">Per distribuire i componenti MED-V usando un sistema di distribuzione del software</span><span class="sxs-lookup"><span data-stu-id="cc479-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="cc479-122">Definire un gruppo di computer e utenti nel sistema di distribuzione elettronica del software come set di destinazione di computer/utenti.</span><span class="sxs-lookup"><span data-stu-id="cc479-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="cc479-123">Creare pacchetti per ogni file di installazione di Microsoft che deve essere distribuito.</span><span class="sxs-lookup"><span data-stu-id="cc479-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="cc479-124">Di seguito sono riportati i file necessari e l'ordine in cui devono essere installati:</span><span class="sxs-lookup"><span data-stu-id="cc479-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="cc479-125">**Windows Virtual PC** -se non è già installato (è necessario riavviare il computer).</span><span class="sxs-lookup"><span data-stu-id="cc479-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="cc479-126">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="cc479-127">**Aggiunte e aggiornamenti di Windows Virtual PC** , se non sono già installati.</span><span class="sxs-lookup"><span data-stu-id="cc479-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="cc479-128">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="cc479-129">**File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione).</span><span class="sxs-lookup"><span data-stu-id="cc479-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="cc479-130">Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="cc479-131">Warning</span><span class="sxs-lookup"><span data-stu-id="cc479-131">Warning</span></span>**  
        <span data-ttu-id="cc479-132">Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="cc479-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="cc479-133">Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cc479-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="cc479-134">**Programma di installazione dell'area di lavoro MED-v, VHD e configurazione eseguibile** -creato nel **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="cc479-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="cc479-135">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="cc479-136">Importante</span><span class="sxs-lookup"><span data-stu-id="cc479-136">Important</span></span>**  
        <span data-ttu-id="cc479-137">Il file del disco rigido virtuale compresso (con estensione MEDV) e il programma eseguibile di installazione (setup.exe) devono trovarsi nella stessa cartella della versione di installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="cc479-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="cc479-138">Installare quindi il programma di installazione dell'area di lavoro MED-V eseguendo setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cc479-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="cc479-139">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="cc479-139">Tip</span></span>**  
        <span data-ttu-id="cc479-140">Poiché i problemi che possono verificarsi durante l'installazione di MED-V da un percorso di rete, è consigliabile copiare i file di configurazione dell'area di lavoro MED-V localmente e quindi eseguire setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cc479-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="cc479-141">Configurare i pacchetti da eseguire in modalità silenziosa (non è necessaria alcuna interazione con l'utente).</span><span class="sxs-lookup"><span data-stu-id="cc479-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="cc479-142">L'uso della modalità silenziosa Elimina il prompt per chiudere Internet Explorer se è in corso e il prompt per avviare l'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="cc479-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="cc479-143">Entrambe le azioni vengono eseguite quando il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="cc479-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="cc479-144">Nota</span><span class="sxs-lookup"><span data-stu-id="cc479-144">Note</span></span>**  
    <span data-ttu-id="cc479-145">L'installazione di Windows Virtual PC richiede di riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="cc479-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="cc479-146">È possibile creare un singolo processo di installazione e installare tutti i componenti contemporaneamente se si elimina il riavvio e si ignorano i prerequisiti necessari per l'installazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="cc479-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="cc479-147">Puoi eseguire questa operazione anche usando gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="cc479-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="cc479-148">Per un esempio di questi argomenti, vedere [installare i componenti MED-V usando un file batch](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="cc479-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="cc479-149">MED-V viene avviato automaticamente all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="cc479-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="cc479-150">Installare MED-V e i relativi componenti prima di installare Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="cc479-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="cc479-151">Vedere il file batch di esempio più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="cc479-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="cc479-152">Importante</span><span class="sxs-lookup"><span data-stu-id="cc479-152">Important</span></span>**  
    <span data-ttu-id="cc479-153">Selezionare l'opzione **Ignore \ _PREREQUISITES** come illustrato nel file batch di esempio in modo che i componenti MED-V possano essere installati prima dei componenti di VPC necessari.</span><span class="sxs-lookup"><span data-stu-id="cc479-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="cc479-154">Installare i componenti MED-V in questo ordine per consentire il riavvio singolo.</span><span class="sxs-lookup"><span data-stu-id="cc479-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="cc479-155">Identificare eventuali altri requisiti necessari per l'installazione e per il sistema di distribuzione del software, ad esempio piattaforme di destinazione e spazio su disco gratuito.</span><span class="sxs-lookup"><span data-stu-id="cc479-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="cc479-156">Assegnare i pacchetti al set di destinazione di computer/utenti.</span><span class="sxs-lookup"><span data-stu-id="cc479-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="cc479-157">Man mano che i computer sono in funzione, il client del sistema di distribuzione del software riconosce che sono disponibili nuovi pacchetti e inizia a installare i pacchetti per la definizione e i requisiti.</span><span class="sxs-lookup"><span data-stu-id="cc479-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="cc479-158">Le installazioni devono essere eseguite sequenzialmente in modalità invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="cc479-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="cc479-159">È consigliabile eseguire questa operazione come singolo processo che non richiede un riavvio fino a quando non vengono installati tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cc479-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="cc479-160">Una volta completate le installazioni, riavviare i computer aggiornati.</span><span class="sxs-lookup"><span data-stu-id="cc479-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="cc479-161">A seconda del sistema di distribuzione del software, è possibile pianificare il riavvio del computer o gli utenti finali possono riavviare i computer manualmente durante il normale lavoro.</span><span class="sxs-lookup"><span data-stu-id="cc479-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="cc479-162">Dopo il riavvio del computer, MED-V viene avviato automaticamente dopo l'accesso di un utente finale.</span><span class="sxs-lookup"><span data-stu-id="cc479-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="cc479-163">Quando si avvia MED-V per la prima volta, viene eseguita la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="cc479-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="cc479-164">La prima volta che viene avviata la configurazione e potrebbero essere necessari alcuni minuti per terminare, a seconda delle dimensioni del disco rigido virtuale specificato e del numero di criteri applicati all'area di lavoro MED-V all'avvio.</span><span class="sxs-lookup"><span data-stu-id="cc479-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="cc479-165">L'utente finale può tenere traccia dello stato di avanzamento guardando l'icona MED-V nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="cc479-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="cc479-166">Per altre informazioni sulla configurazione per la prima volta, vedere [Panoramica della distribuzione di MED-V 2,0](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cc479-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="cc479-167">Per installare i componenti MED-V usando un file batch</span><span class="sxs-lookup"><span data-stu-id="cc479-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="cc479-168">Eseguire l'installazione in un prompt dei comandi con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="cc479-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="cc479-169">Distribuire ogni componente in una singola directory.</span><span class="sxs-lookup"><span data-stu-id="cc479-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="cc479-170">Se viene eseguito da una condivisione di rete, è necessario un tempo più lungo per decomprimere il file con estensione MEDV.</span><span class="sxs-lookup"><span data-stu-id="cc479-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="cc479-171">Come procedura consigliata, specificare che Windows Virtual PC e Windows Virtual PC hotfix vengono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="cc479-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="cc479-172">Questo significa che Windows Update non causerà interferenze con il processo di installazione richiedendo un riavvio.</span><span class="sxs-lookup"><span data-stu-id="cc479-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="cc479-173">Riavviare il computer dopo il completamento del file batch.</span><span class="sxs-lookup"><span data-stu-id="cc479-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="cc479-174">Dopo il riavvio, all'utente viene richiesto di eseguire la configurazione per la prima volta e completare la configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="cc479-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="cc479-175">L'esempio seguente, con gli argomenti specificati, Mostra come installare i componenti MED-V di 64 bit in un singolo processo:</span><span class="sxs-lookup"><span data-stu-id="cc479-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cc479-176">Argomento</span><span class="sxs-lookup"><span data-stu-id="cc479-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="cc479-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc479-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cc479-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="cc479-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc479-179">Impedisce l'installazione di Windows Virtual PC e dell'aggiornamento di Windows Virtual PC da riavviare il computer host.</span><span class="sxs-lookup"><span data-stu-id="cc479-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cc479-180">/quiet</span><span class="sxs-lookup"><span data-stu-id="cc479-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc479-181">Installa i componenti MED-V in modalità non interattiva senza interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cc479-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cc479-182">/Qn</span><span class="sxs-lookup"><span data-stu-id="cc479-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc479-183">Installa i componenti MED-V senza un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cc479-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cc479-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="cc479-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc479-185">Viene installata senza controllare Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="cc479-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cc479-186">Nota</span><span class="sxs-lookup"><span data-stu-id="cc479-186">Note</span></span></strong><br/><p><span data-ttu-id="cc479-187">Specificare questo argomento solo se si sta installando Windows Virtual PC come parte di questa installazione.</span><span class="sxs-lookup"><span data-stu-id="cc479-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cc479-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="cc479-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc479-189">Impone l'installazione dell'area di lavoro MED-V e impedisce eventuali richieste che potrebbero generare.</span><span class="sxs-lookup"><span data-stu-id="cc479-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cc479-190">Esempio</span><span class="sxs-lookup"><span data-stu-id="cc479-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="cc479-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc479-191">Related topics</span></span>


[<span data-ttu-id="cc479-192">Panoramica della distribuzione di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="cc479-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="cc479-193">Distribuire i componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="cc479-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









