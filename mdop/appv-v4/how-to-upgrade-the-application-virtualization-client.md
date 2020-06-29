---
title: Come aggiornare Application Virtualization Client
description: Come aggiornare Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816455"
---
# <span data-ttu-id="46073-103">Come aggiornare Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="46073-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="46073-104">Puoi usare le procedure seguenti per aggiornare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="46073-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="46073-105">È possibile aggiornare il client installando una nuova versione nella versione precedente installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="46073-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="46073-106">Quando si aggiornano i client, il software di installazione mantiene automaticamente e esegue la migrazione delle impostazioni dell'utente per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="46073-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="46073-107">Per eseguire il programma di installazione sono necessari diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="46073-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="46073-108">**Nota**  Durante l'aggiornamento a Application Virtualization (App-V) 4.5 o versioni successive, le autorizzazioni per la chiave del registro di sistema HKCU vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="46073-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="46073-109">Per questo motivo, gli utenti perderebbero le configurazioni utente impostate in precedenza, ad esempio le impostazioni della modalità disconnessa configurate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="46073-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="46073-110">Se l'utente non è stato limitato attivamente dalla configurazione del comportamento dell'interfaccia utente del client tramite un blocco delle autorizzazioni, l'utente può reimpostare queste preferenze dopo un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="46073-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="46073-111">**Importante**  Quando si esegue l'aggiornamento alla versione 4.6 o a una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="46073-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="46073-112">L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.</span><span class="sxs-lookup"><span data-stu-id="46073-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="46073-113">Per aggiornare il client Desktop Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="46073-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="46073-114">Chiudere tutte le applicazioni virtuali, fare clic con il pulsante destro del mouse sull'icona client desktop dell'App-V visualizzata nell'area di notifica desktop di Windows e scegliere **Exit** per arrestare il client esistente.</span><span class="sxs-lookup"><span data-stu-id="46073-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="46073-115">Dopo aver ottenuto il file di archivio del programma di installazione corretto e averlo salvato nel computer, fare doppio clic su di esso per espandere l'archivio.</span><span class="sxs-lookup"><span data-stu-id="46073-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="46073-116">Individuare il file setup.exe e fare doppio clic su setup.exe per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="46073-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="46073-117">La procedura guidata controlla che il sistema assicuri che sia installato tutto il software prerequisito e chiederà di installare una delle opzioni seguenti, se mancanti:</span><span class="sxs-lookup"><span data-stu-id="46073-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="46073-118">Microsoft VisualC + + 2005SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="46073-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="46073-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="46073-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="46073-120">Segnalazione errori applicazione Microsoft</span><span class="sxs-lookup"><span data-stu-id="46073-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="46073-121">**Nota**  Per la versione 4.6 e successive, la procedura guidata installerà anche il seguente requisito software:</span><span class="sxs-lookup"><span data-stu-id="46073-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="46073-122">Microsoft VisualC + + 2008SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="46073-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="46073-123">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="46073-123">Click **Install**.</span></span> <span data-ttu-id="46073-124">Lo stato di avanzamento dell'installazione viene visualizzato e lo stato viene modificato da **in sospeso** a **installazione**.</span><span class="sxs-lookup"><span data-stu-id="46073-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="46073-125">Lo stato di installazione viene modificato in **riuscito** Man mano che ogni passaggio viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="46073-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="46073-126">Quando viene visualizzata la finestra di dialogo **client di Application Virtualization Desktop** e viene visualizzato un messaggio che indica che è stata trovata una versione precedente del client nel computer, fare clic su **Avanti** per eseguire l'aggiornamento alla nuova versione.</span><span class="sxs-lookup"><span data-stu-id="46073-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="46073-127">Quando viene visualizzata la schermata del **contratto di licenza** , leggere il contratto di licenza e, se si è d'accordo, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="46073-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="46073-128">Quando la procedura guidata InstallShield Visualizza la schermata **pronto per l'aggiornamento della** finestra di dialogo programma, fare clic su **Aggiorna** per iniziare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46073-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="46073-129">La schermata successiva indica che il client è in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="46073-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="46073-130">**Avviso**  Se il programma client non è stato arrestato nel passaggio 1, è possibile che venga visualizzato un messaggio **di avviso in uso** .</span><span class="sxs-lookup"><span data-stu-id="46073-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="46073-131">In questo caso, fai clic con il pulsante destro del mouse sull'icona del client App-V visualizzata nell'area di notifica desktop e seleziona **Esci** per arrestare il client esistente.</span><span class="sxs-lookup"><span data-stu-id="46073-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="46073-132">Quindi fare clic su **Riprova** per continuare.</span><span class="sxs-lookup"><span data-stu-id="46073-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="46073-133">Quando l'installazione viene completata correttamente, verrà richiesto di riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="46073-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="46073-134">È necessario riavviare il computer per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="46073-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="46073-135">**Attenzione**  Se l'aggiornamento non riesce per qualsiasi motivo, sarà necessario riavviare il computer prima di riprovare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46073-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="46073-136">Per aggiornare l'Application Virtualization Client tramite la riga di comando</span><span class="sxs-lookup"><span data-stu-id="46073-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="46073-137">Se si esegue l'aggiornamento del client App-V tramite il programma setup.msi, verificare che sia stato installato il software necessario per i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="46073-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="46073-138">Importante</span><span class="sxs-lookup"><span data-stu-id="46073-138">Important</span></span>**  
    -   <span data-ttu-id="46073-139">Per la versione 4.6 e successive del client App-V, il programma setup.msi controlla il sistema e non riesce con un messaggio di errore che indica che l'installazione non può continuare se il software prerequisito non è installato.</span><span class="sxs-lookup"><span data-stu-id="46073-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="46073-140">Per App-V versione 4.6, i parametri della riga di comando non possono essere usati durante l'aggiornamento e verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="46073-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="46073-141">L'esempio della riga di comando seguente usa il file setup.msi per aggiornare il client App-V.</span><span class="sxs-lookup"><span data-stu-id="46073-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="46073-142">Sarà necessario usare il programma di installazione client corretto a seconda che si stia aggiornando il client Desktop App-V o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="46073-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="46073-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="46073-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="46073-144">**Importante**  Le virgolette sono obbligatorie solo quando il valore contiene uno spazio.</span><span class="sxs-lookup"><span data-stu-id="46073-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="46073-145">Per coerenza, tutte le istanze nell'esempio precedente vengono visualizzate come virgolette.</span><span class="sxs-lookup"><span data-stu-id="46073-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="46073-146">Per aggiornare l'Application Virtualization Client per Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="46073-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="46073-147">Seguire i criteri standard dell'organizzazione per l'installazione o l'aggiornamento delle applicazioni nel server Host sessione Desktop remoto (host RDSession).</span><span class="sxs-lookup"><span data-stu-id="46073-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="46073-148">Se il sistema fa parte di una farm, rimuovere l'host RDSession dalla server farm.</span><span class="sxs-lookup"><span data-stu-id="46073-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="46073-149">Per aggiornare il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario usare la riga di comando perché non è possibile aggiornare il client manualmente nell'host RDSession.</span><span class="sxs-lookup"><span data-stu-id="46073-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="46073-150">**Nota**  In App-V versione 4,6 e versioni successive, oltre a usare la riga di comando per aggiornare il client, è anche possibile usare una sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="46073-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="46073-151">Per avviare la sessione Desktop remoto non è necessario alcun parametro speciale.</span><span class="sxs-lookup"><span data-stu-id="46073-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="46073-152">Dopo il completamento dell'aggiornamento del client per Servizi Desktop remoto, riavviare e accedere all'host RDSession.</span><span class="sxs-lookup"><span data-stu-id="46073-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="46073-153">Dopo aver riavviato il sistema, aggiungere il server alla server farm.</span><span class="sxs-lookup"><span data-stu-id="46073-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="46073-154">**Attenzione**  Se l'aggiornamento non riesce per qualsiasi motivo, sarà necessario riavviare il computer prima di riprovare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46073-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="46073-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46073-155">Related topics</span></span>


[<span data-ttu-id="46073-156">Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="46073-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





