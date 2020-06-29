---
title: Risoluzione dei problemi di MED-V
description: Risoluzione dei problemi di MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825865"
---
# <span data-ttu-id="34b32-103">Risoluzione dei problemi di MED-V</span><span class="sxs-lookup"><span data-stu-id="34b32-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="34b32-104">Questa sezione contiene informazioni utili per risolvere i problemi generali di Microsoft Enterprise Desktop Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="34b32-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="34b32-105">Se si modifica la risoluzione dell'host e quindi si massimizza l'area di lavoro MED-V, il desktop viene visualizzato in nero</span><span class="sxs-lookup"><span data-stu-id="34b32-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="34b32-106">Quando si lavora in modalità desktop completo, se si modifica la risoluzione dell'host e quindi si ingrandisce la finestra dell'area di lavoro MED-V, il desktop viene visualizzato in nero e l'area di lavoro MED-V potrebbe non rispondere.</span><span class="sxs-lookup"><span data-stu-id="34b32-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="34b32-107">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-107">Solution</span></span>

<span data-ttu-id="34b32-108">Arrestare e quindi avviare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="34b32-109">L'avvio di un'area di lavoro MED-V con una scheda di rete è disabilitata e in seguito l'abilitazione della scheda non ripristina la connettività di rete</span><span class="sxs-lookup"><span data-stu-id="34b32-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="34b32-110">Se si configura un'area di lavoro MED-V in modalità Bridge e quindi si avvia l'area di lavoro MED-V mentre una scheda di rete è disabilitata, se l'adapter viene abilitato in seguito, la connettività di rete tramite tale adapter non viene ripristinata.</span><span class="sxs-lookup"><span data-stu-id="34b32-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="34b32-111">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-111">Solution</span></span>

<span data-ttu-id="34b32-112">Arrestare e quindi avviare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="34b32-113">Un'immagine può essere usata da un solo utente Windows per computer</span><span class="sxs-lookup"><span data-stu-id="34b32-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="34b32-114">Un'immagine dell'area di lavoro MED-V può essere usata solo dall'utente di Windows che ha scaricato o importato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="34b32-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="34b32-115">Questo utente è l'unico utente a parte gli amministratori che hanno le autorizzazioni per la cartella in cui si trovano le immagini scaricate.</span><span class="sxs-lookup"><span data-stu-id="34b32-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="34b32-116">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-116">Solution</span></span>

<span data-ttu-id="34b32-117">Modificare manualmente l'elenco di controllo di accesso (ACL) nell'archivio immagini.</span><span class="sxs-lookup"><span data-stu-id="34b32-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="34b32-118">Durante l'installazione di MED-V tramite Configuration Manager con i diritti degli utenti abilitati, la disinstallazione non riesce</span><span class="sxs-lookup"><span data-stu-id="34b32-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="34b32-119">Se MED-V viene installato con Microsoft System Center Configuration Manager e la modalità di esecuzione del pacchetto è impostata su diritti degli utenti, la disinstallazione non riesce con un messaggio di errore che indica che solo gli utenti amministrativi possono disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="34b32-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-120">Solution</span></span>

<span data-ttu-id="34b32-121">Quando si crea un pacchetto di Configuration Manager per MED-V, impostare la modalità di esecuzione su diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="34b32-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="34b32-122">Quando si installa MED-V usando un sistema di distribuzione aziendale, in cui l'installazione è configurata per l'esecuzione del client dopo l'installazione, non è possibile eseguire il client</span><span class="sxs-lookup"><span data-stu-id="34b32-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="34b32-123">Se MED-V viene installato usando un sistema di distribuzione aziendale e il pacchetto di installazione è configurato per l'esecuzione del client MED-V dopo l'installazione, dopo che il client è in esecuzione con l'account di sistema, non è possibile vedere che il client è in esecuzione (eccetto nell'area di notifica) e non è possibile interagire con esso.</span><span class="sxs-lookup"><span data-stu-id="34b32-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="34b32-124">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-124">Solution</span></span>

<span data-ttu-id="34b32-125">Quando si installa MED-V usando un sistema di distribuzione aziendale, usare il parametro *Start \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="34b32-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="34b32-126">Impossibile avviare l'immagine di test MED-V</span><span class="sxs-lookup"><span data-stu-id="34b32-126">MED-V test image fails to start</span></span>


<span data-ttu-id="34b32-127">Se un'immagine di test MED-V non viene avviata, non si recupererà mai e tutti gli avvii futuri non riusciranno con il messaggio di errore "Impossibile caricare GINA".</span><span class="sxs-lookup"><span data-stu-id="34b32-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="34b32-128">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-128">Solution</span></span>

<span data-ttu-id="34b32-129">Elimina l'immagine di test esistente e quindi ricreala di nuovo.</span><span class="sxs-lookup"><span data-stu-id="34b32-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="34b32-130">Dopo aver tentato di partecipare a un dominio con le credenziali errate, l'immagine non riesce mai a partecipare al dominio</span><span class="sxs-lookup"><span data-stu-id="34b32-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="34b32-131">Se è presente un errore di configurazione nel blocco predefinito di join Domain, che fa parte dello script di configurazione iniziale della macchina virtuale, l'area di lavoro MED-V non riesce quando si tenta di partecipare a un dominio.</span><span class="sxs-lookup"><span data-stu-id="34b32-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="34b32-132">Dopo il corretto errore di configurazione, l'immagine inclusa nell'area di lavoro MED-V non può accedere al dominio.</span><span class="sxs-lookup"><span data-stu-id="34b32-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="34b32-133">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-133">Solution</span></span>

<span data-ttu-id="34b32-134">Se l'immagine è stata distribuita, ridistribuire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="34b32-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="34b32-135">Se l'immagine è un'immagine di test, ricrea l'immagine.</span><span class="sxs-lookup"><span data-stu-id="34b32-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="34b32-136">MED-V non supporta più monitor</span><span class="sxs-lookup"><span data-stu-id="34b32-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="34b32-137">MED-V non supporta la visualizzazione delle applicazioni pubblicate su più monitor.</span><span class="sxs-lookup"><span data-stu-id="34b32-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="34b32-138">Le applicazioni pubblicate e altre finestre client potrebbero essere visualizzate nella schermata sbagliata e, a volte, dopo la disconnessione di una schermata, MED-V tenterà di inviare lo schermo al monitor in modo che il monitor connesso venga visualizzato in bianco.</span><span class="sxs-lookup"><span data-stu-id="34b32-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="34b32-139">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-139">Solution</span></span>

<span data-ttu-id="34b32-140">Scollegare la schermata aggiuntiva e riavviare il client.</span><span class="sxs-lookup"><span data-stu-id="34b32-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="34b32-141">Impossibile avviare l'area di lavoro MED-V se l'host si arresta in modo anomalo durante l'avvio dell'area di lavoro MED V</span><span class="sxs-lookup"><span data-stu-id="34b32-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="34b32-142">Se l'host si arresta in modo anomalo durante il processo di avvio dell'area di lavoro MED-V e viene visualizzato un messaggio di errore che indica che l'elemento radice non è presente, l'area di lavoro MED-V potrebbe aggiungere dati a un file di configurazione della macchina virtuale (VMC) vuoto, in modo che il processo di avvio non riesca.</span><span class="sxs-lookup"><span data-stu-id="34b32-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="34b32-143">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-143">Solution</span></span>

<span data-ttu-id="34b32-144">Sostituire il file VMC vuoto con un file VMC dall'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="34b32-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="34b32-145">La tastiera non risponde nelle finestre delle applicazioni pubblicate</span><span class="sxs-lookup"><span data-stu-id="34b32-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="34b32-146">In un'area di lavoro MED-V, se si preme il tasto Windows quando un'applicazione pubblicata è in stato attivo, la tastiera non risponde più nelle finestre delle applicazioni pubblicate.</span><span class="sxs-lookup"><span data-stu-id="34b32-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="34b32-147">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-147">Solution</span></span>

<span data-ttu-id="34b32-148">Premere il tasto Windows mentre è attiva un'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="34b32-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="34b32-149">Un'area di lavoro Domain MED-V non aggiorna le credenziali di dominio</span><span class="sxs-lookup"><span data-stu-id="34b32-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="34b32-150">Quando si usa un'area di lavoro MED-V persistente in un ambiente di dominio, se si modifica la password del dominio, il client MED-V non aggiorna le credenziali del dominio dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="34b32-151">Quando un'applicazione pubblicata cerca di accedere a una risorsa di rete, viene visualizzato un messaggio di errore che informa che le credenziali sono scadute.</span><span class="sxs-lookup"><span data-stu-id="34b32-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="34b32-152">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-152">Solution</span></span>

<span data-ttu-id="34b32-153">Riavviare il sistema operativo di area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="34b32-154">Le finestre delle applicazioni pubblicate ingrandite coprono la barra delle applicazioni host</span><span class="sxs-lookup"><span data-stu-id="34b32-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="34b32-155">Se si massimizza una finestra dell'applicazione pubblicata a schermo intero, potrebbe essere relativa alla barra delle applicazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="34b32-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="34b32-156">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-156">Solution</span></span>

<span data-ttu-id="34b32-157">Effettua una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="34b32-157">Do one of the following:</span></span>

<span data-ttu-id="34b32-158">Ridurre a icona la finestra dell'applicazione pubblicata per ottenere l'accesso all'area di notifica e riavviare lo spazio di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="34b32-159">Ridurre a icona la finestra dell'applicazione pubblicata e quindi ripristinare lo stato ingrandito della finestra.</span><span class="sxs-lookup"><span data-stu-id="34b32-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="34b32-160">L'aggiunta di utenti o gruppi in Gestione configurazione server MED-V non funziona</span><span class="sxs-lookup"><span data-stu-id="34b32-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="34b32-161">Quando si aggiungono utenti o gruppi nella finestra di dialogo **Seleziona utenti o gruppi** , gli utenti o i gruppi selezionati non vengono aggiunti all'elenco di controllo di Access in Gestione configurazione server MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="34b32-162">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-162">Solution</span></span>

<span data-ttu-id="34b32-163">Aggiungere utenti o gruppi tramite la finestra di dialogo **Immetti nomi utente o di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="34b32-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="34b32-164">Per informazioni dettagliate, vedere [come installare e configurare il componente server MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span><span class="sxs-lookup"><span data-stu-id="34b32-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="34b32-165">MED-V non funziona nei computer con Windows Virtual PC per Windows 7 installato</span><span class="sxs-lookup"><span data-stu-id="34b32-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="34b32-166">MED-V richiede Windows Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="34b32-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="34b32-167">Non è possibile installare Windows Virtual PC per Windows7 e Virtual PC2007 SP1 nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="34b32-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="34b32-168">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-168">Solution</span></span>

<span data-ttu-id="34b32-169">Disinstallare Virtual PC per Windows7 prima di installare Virtual PC2007 SP1 e MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="34b32-170">MED-V non supporta le immagini di Virtual PC e modalità WindowsXP</span><span class="sxs-lookup"><span data-stu-id="34b32-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="34b32-171">MED-V 1.0 SP1 non supporta le immagini create da Windows Virtual PC per Windows7.</span><span class="sxs-lookup"><span data-stu-id="34b32-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="34b32-172">Se si usa un'immagine PC virtuale per Windows7, il client non riesce durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="34b32-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="34b32-173">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-173">Solution</span></span>

<span data-ttu-id="34b32-174">Creare immagini MED-V tramite Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="34b32-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="34b32-175">Windows Firewall blocca l'attività di rete Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="34b32-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="34b32-176">Per impostazione predefinita, Windows Firewall blocca l'attività di rete Virtual PC2007 SP1 e, quando si avvia Virtual PC2007 SP1 nel computer client, viene visualizzato un messaggio di firewall che blocca la sequenza di avvio e tutto l'accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="34b32-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="34b32-177">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-177">Solution</span></span>

<span data-ttu-id="34b32-178">Aggiornare l'eccezione del firewall usando criteri di gruppo prima che l'utente finale usi MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="34b32-179">Quando si aggiorna il client viene visualizzato un messaggio di errore</span><span class="sxs-lookup"><span data-stu-id="34b32-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="34b32-180">Quando si esegue l'aggiornamento del client da MED-V 1.0 a MED-V 1.0 SP1, potrebbe essere visualizzato un messaggio che informa che non è stata definita alcuna area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="34b32-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="34b32-181">Soluzione</span><span class="sxs-lookup"><span data-stu-id="34b32-181">Solution</span></span>

<span data-ttu-id="34b32-182">Chiudere il client e riavviarlo.</span><span class="sxs-lookup"><span data-stu-id="34b32-182">Close the client and restart it.</span></span>

## <span data-ttu-id="34b32-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34b32-183">Related topics</span></span>


[<span data-ttu-id="34b32-184">Note sulla versione di MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="34b32-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="34b32-185">Note sulla versione di MED-V 1.0 SP1 e SP2</span><span class="sxs-lookup"><span data-stu-id="34b32-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





