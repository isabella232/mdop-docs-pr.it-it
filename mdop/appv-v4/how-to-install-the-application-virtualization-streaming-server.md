---
title: Come installare Application Virtualization Streaming Server
description: Come installare Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817326"
---
# <span data-ttu-id="2bd53-103">Come installare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="2bd53-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="2bd53-104">L'Application Virtualization Streaming Server pubblica le proprie applicazioni ai client.</span><span class="sxs-lookup"><span data-stu-id="2bd53-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="2bd53-105">In un ambiente con bilanciamento del carico, tipico delle distribuzioni di grandi dimensioni, tutti i server di un gruppo di server devono eseguire il flusso delle stesse applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2bd53-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="2bd53-106">Se i server di streaming di Application Virtualization sono in streaming di applicazioni diverse, assegnare i server a gruppi di server diversi.</span><span class="sxs-lookup"><span data-stu-id="2bd53-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="2bd53-107">In questo caso, potrebbe anche essere necessario aumentare la capacità di un gruppo di server.</span><span class="sxs-lookup"><span data-stu-id="2bd53-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="2bd53-108">Se è stato designato un computer di destinazione nella rete, con un account di accesso con privilegi amministrativi locali, è possibile usare la procedura seguente per installare l'Application Virtualization Streaming Server e assegnarlo al gruppo di server appropriato.</span><span class="sxs-lookup"><span data-stu-id="2bd53-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="2bd53-109">**Nota**  La procedura guidata per l'installazione può creare un record del gruppo di server, se non esiste, e un record dell'appartenenza all'Application Virtualization Streaming Server in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2bd53-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="2bd53-110">Dopo aver completato il processo di installazione, riavviare il server.</span><span class="sxs-lookup"><span data-stu-id="2bd53-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="2bd53-111">Per installare un Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="2bd53-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="2bd53-112">Verificare che nel computer di destinazione non siano installate versioni precedenti di Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="2bd53-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="2bd53-113">**Importante**  Verificare che App-V Management Server non sia installato nel computer in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="2bd53-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="2bd53-114">I due prodotti non possono essere installati nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="2bd53-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="2bd53-115">Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="2bd53-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="2bd53-116">Nella pagina di **benvenuto** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="2bd53-117">Nella pagina **contratto di licenza** per accettare le condizioni di licenza selezionare **Accetto i termini e le condizioni**di licenza e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="2bd53-118">Nella pagina **informazioni cliente** specificare il **nome utente** e l'organizzazione e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="2bd53-119">Nella pagina **percorso di installazione** fare clic su **Sfoglia**, specificare il percorso in cui si vuole installare il server di streaming e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="2bd53-120">Nella pagina **modalità di sicurezza della connessione** selezionare il certificato desiderato nell'elenco a discesa e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="2bd53-121">**Nota**  L'impostazione **modalità di connessione sicura** richiede al server di eseguire il provisioning di un certificato server da un'infrastruttura a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="2bd53-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="2bd53-122">Se nel server non è installato un certificato del server, questa opzione non è disponibile e non può essere selezionata.</span><span class="sxs-lookup"><span data-stu-id="2bd53-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="2bd53-123">È necessario concedere all'account del servizio di rete l'accesso in lettura al certificato in uso.</span><span class="sxs-lookup"><span data-stu-id="2bd53-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="2bd53-124">Nella pagina di **configurazione della porta TCP** , per usare la porta standard (554), selezionare **Usa porta predefinita (554)**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="2bd53-125">Per specificare una porta personalizzata, selezionare **Usa porta personalizzata**, specificare il numero di porta nel campo specificato e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="2bd53-126">**Nota**  Quando si installa il server in uno scenario non sicuro, è possibile usare la porta predefinita (554) oppure definire una porta personalizzata.</span><span class="sxs-lookup"><span data-stu-id="2bd53-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="2bd53-127">Nella pagina **radice contenuto** specificare la posizione nel computer di destinazione in cui verranno salvati i file SFT e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="2bd53-128">**Nota**  Se la porta HTTP o RTSP per il server di streaming delle applicazioni virtuali è già allocata, verrà richiesto di selezionare una nuova porta.</span><span class="sxs-lookup"><span data-stu-id="2bd53-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="2bd53-129">Specificare la porta desiderata e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="2bd53-130">Nella schermata **Impostazioni avanzate** immettere le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bd53-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="2bd53-131">Connessioni client max</span><span class="sxs-lookup"><span data-stu-id="2bd53-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="2bd53-132">Timeout connessione (sec)</span><span class="sxs-lookup"><span data-stu-id="2bd53-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="2bd53-133">Dimensioni del pool di thread RTSP</span><span class="sxs-lookup"><span data-stu-id="2bd53-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="2bd53-134">Timeout RTSP (sec)</span><span class="sxs-lookup"><span data-stu-id="2bd53-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="2bd53-135">Numero di processi principali</span><span class="sxs-lookup"><span data-stu-id="2bd53-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="2bd53-136">Timeout di base (sec)</span><span class="sxs-lookup"><span data-stu-id="2bd53-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="2bd53-137">Abilitare l'autenticazione utente</span><span class="sxs-lookup"><span data-stu-id="2bd53-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="2bd53-138">Abilitare l'autorizzazione dell'utente</span><span class="sxs-lookup"><span data-stu-id="2bd53-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="2bd53-139">Dimensioni blocco cache (KB)</span><span class="sxs-lookup"><span data-stu-id="2bd53-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="2bd53-140">Dimensioni massime della cache (MB)</span><span class="sxs-lookup"><span data-stu-id="2bd53-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="2bd53-141">**Nota**  App-V Streaming Server usa le autorizzazioni di file system NTFS per controllare l'accesso alle applicazioni sotto la condivisione di contenuto.</span><span class="sxs-lookup"><span data-stu-id="2bd53-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="2bd53-142">USA **Abilita l'autenticazione utente** e **Abilita l'autorizzazione dell'utente** per controllare se il server controlla e applica gli elenchi di controllo di accesso (ACL) o meno.</span><span class="sxs-lookup"><span data-stu-id="2bd53-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="2bd53-143">Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="2bd53-144">Nella schermata di **installazione guidata completata** , per chiudere la procedura guidata, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="2bd53-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="2bd53-145">**Importante**  L'installazione può richiedere diversi minuti per terminare.</span><span class="sxs-lookup"><span data-stu-id="2bd53-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="2bd53-146">Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando che l'installazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="2bd53-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="2bd53-147">Non è necessario riavviare il computer quando viene richiesto.</span><span class="sxs-lookup"><span data-stu-id="2bd53-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="2bd53-148">Per ottimizzare le prestazioni del sistema, è comunque consigliabile un riavvio.</span><span class="sxs-lookup"><span data-stu-id="2bd53-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="2bd53-149">Ripetere i passaggi da 1 a 12 per ogni server delle applicazioni virtuali che è necessario installare.</span><span class="sxs-lookup"><span data-stu-id="2bd53-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="2bd53-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bd53-150">Related topics</span></span>


[<span data-ttu-id="2bd53-151">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="2bd53-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





