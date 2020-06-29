---
title: Come installare il server di gestione di Application Virtualization
description: Come installare il server di gestione di Application Virtualization
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817365"
---
# <span data-ttu-id="00f43-103">Come installare il server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="00f43-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="00f43-104">L'Application Virtualization Management Server pubblica le proprie applicazioni ai client.</span><span class="sxs-lookup"><span data-stu-id="00f43-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="00f43-105">In un ambiente con bilanciamento del carico, tipico delle distribuzioni di grandi dimensioni, tutti i server di un gruppo di server devono eseguire il flusso delle stesse applicazioni.</span><span class="sxs-lookup"><span data-stu-id="00f43-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="00f43-106">Se i server di gestione della virtualizzazione dell'applicazione devono pubblicare applicazioni diverse, assegnare i server a gruppi di server diversi.</span><span class="sxs-lookup"><span data-stu-id="00f43-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="00f43-107">In questo caso, potresti anche dover aumentare la capacità di un gruppo di server.</span><span class="sxs-lookup"><span data-stu-id="00f43-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="00f43-108">Se è stato designato un computer di destinazione nella rete, con un account di accesso con privilegi di amministratore locale, è possibile usare la procedura seguente per installare l'Application Virtualization Management Server e assegnarlo al gruppo di server appropriato.</span><span class="sxs-lookup"><span data-stu-id="00f43-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="00f43-109">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-109">Note</span></span>**  
<span data-ttu-id="00f43-110">La procedura guidata di installazione può creare un record di gruppo di server, se non esiste, nonché un record dell'appartenenza dell'Application Virtualization Management Server in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="00f43-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="00f43-111">Dopo aver completato il processo di installazione, riavviare il server.</span><span class="sxs-lookup"><span data-stu-id="00f43-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="00f43-112">Per installare un Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="00f43-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="00f43-113">Verificare e, se necessario, disinstallare le versioni precedenti del server di gestione della virtualizzazione delle applicazioni installate nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="00f43-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="00f43-114">Per aprire l' **installazione guidata di Microsoft Application Virtualization Management Server** , passare alla posizione del programma Application virtualization System **setup.exe** nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file di **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="00f43-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="00f43-115">Nella pagina di **benvenuto** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="00f43-116">Nella pagina **contratto di licenza** leggere il contratto di licenza e, per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**.</span><span class="sxs-lookup"><span data-stu-id="00f43-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="00f43-117">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-117">Click **Next**.</span></span>

5.  <span data-ttu-id="00f43-118">Nella pagina **registrazione delle informazioni** è necessario immettere il nome utente e l' **organizzazione**.</span><span class="sxs-lookup"><span data-stu-id="00f43-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="00f43-119">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-119">Click **Next**.</span></span>

6.  <span data-ttu-id="00f43-120">Nella pagina **tipo di installazione** selezionare **personalizzato**.</span><span class="sxs-lookup"><span data-stu-id="00f43-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="00f43-121">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-121">Click **Next**.</span></span> <span data-ttu-id="00f43-122">Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **Application Virtualization Server**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="00f43-123">Attenzione</span><span class="sxs-lookup"><span data-stu-id="00f43-123">Caution</span></span>**  
    <span data-ttu-id="00f43-124">Se un componente è già installato nel computer, quando lo si deseleziona nella finestra di **configurazione personalizzata** , il componente viene disinstallato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="00f43-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="00f43-125">Nella pagina **database di configurazione** selezionare un server di database dall'elenco dei server disponibili o aggiungere un server selezionando **Usa il nome host seguente** e specificando il **nome del server** e i dati del numero di **porta** .</span><span class="sxs-lookup"><span data-stu-id="00f43-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="00f43-126">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-126">Click **Next**.</span></span>

    **<span data-ttu-id="00f43-127">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-127">Note</span></span>**  
    <span data-ttu-id="00f43-128">L'Application Virtualization Management Server non supporta SQL con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="00f43-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="00f43-129">Nella pagina **modalità di sicurezza della connessione** selezionare il certificato desiderato nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="00f43-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="00f43-130">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-130">Click **Next**.</span></span>

   **<span data-ttu-id="00f43-131">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-131">Note</span></span>**  
   <span data-ttu-id="00f43-132">L'impostazione **modalità di connessione sicura** richiede al server di eseguire il provisioning di un certificato server da un'infrastruttura a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="00f43-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="00f43-133">Se nel server non è installato un certificato del server, questa opzione non è disponibile e non può essere selezionata.</span><span class="sxs-lookup"><span data-stu-id="00f43-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="00f43-134">È necessario concedere all'account del servizio di rete l'accesso in lettura al certificato in uso.</span><span class="sxs-lookup"><span data-stu-id="00f43-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="00f43-135">Nella pagina di **configurazione della porta TCP** , per usare la porta predefinita (554), selezionare **Usa porta predefinita (554)**.</span><span class="sxs-lookup"><span data-stu-id="00f43-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="00f43-136">Per specificare una porta personalizzata, selezionare **Usa porta personalizzata** e specificare il numero di porta che verrà usato.</span><span class="sxs-lookup"><span data-stu-id="00f43-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="00f43-137">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-137">Click **Next**.</span></span>

   **<span data-ttu-id="00f43-138">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-138">Note</span></span>**  
   <span data-ttu-id="00f43-139">Quando si installa il server in un ambiente non sicuro, è possibile usare la porta predefinita (554) oppure definire una porta personalizzata.</span><span class="sxs-lookup"><span data-stu-id="00f43-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="00f43-140">Nella pagina del **gruppo amministratore** specificare il nome del gruppo di sicurezza autorizzato per la gestione del server in **nome gruppo**.</span><span class="sxs-lookup"><span data-stu-id="00f43-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="00f43-141">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-141">Click **Next**.</span></span> <span data-ttu-id="00f43-142">Confermare il gruppo specificato e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="00f43-143">Nella pagina del **gruppo provider predefinito** specificare il nome del gruppo di provider predefinito e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="00f43-144">Nella pagina **percorso contenuto** specificare la posizione nel computer di destinazione in cui verranno salvati i file SFT e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="00f43-145">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-145">Note</span></span>**  
   <span data-ttu-id="00f43-146">Se la porta HTTP o RTSP per il server di gestione è già allocata, verrà richiesto di scegliere una nuova porta.</span><span class="sxs-lookup"><span data-stu-id="00f43-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="00f43-147">Selezionare la porta desiderata e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="00f43-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="00f43-148">Nella pagina **pronto per l'installazione del programma** , per installare Application Virtualization Management Server, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="00f43-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="00f43-149">Nota</span><span class="sxs-lookup"><span data-stu-id="00f43-149">Note</span></span>**  
   <span data-ttu-id="00f43-150">Se quando si prova a completare questo passaggio viene visualizzato l'errore 25120, è necessario abilitare **gli strumenti e gli script di gestione di**IIS.</span><span class="sxs-lookup"><span data-stu-id="00f43-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="00f43-151">Per abilitare questa funzionalità di Windows, aprire il pannello di controllo **programmi e funzionalità** , selezionare **attiva o disattiva le funzionalità di Windows**e passare a **Internet Information Services.**</span><span class="sxs-lookup"><span data-stu-id="00f43-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="00f43-152">In **strumenti di gestione Web**abilitare **gli script e gli strumenti di gestione di IIS**.</span><span class="sxs-lookup"><span data-stu-id="00f43-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="00f43-153">Nella schermata di **installazione guidata completata** , per chiudere la procedura guidata, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="00f43-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="00f43-154">Importante</span><span class="sxs-lookup"><span data-stu-id="00f43-154">Important</span></span>**  
   <span data-ttu-id="00f43-155">L'installazione può richiedere alcuni minuti per terminare.</span><span class="sxs-lookup"><span data-stu-id="00f43-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="00f43-156">Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando che l'installazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="00f43-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="00f43-157">Quando richiesto, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="00f43-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="00f43-158">Tuttavia, per ottimizzare le prestazioni del sistema, è consigliabile un riavvio.</span><span class="sxs-lookup"><span data-stu-id="00f43-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="00f43-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00f43-159">Related topics</span></span>


[<span data-ttu-id="00f43-160">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="00f43-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









