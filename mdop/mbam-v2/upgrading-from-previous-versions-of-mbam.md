---
title: Aggiornamento da versioni precedenti di MBAM
description: Aggiornamento da versioni precedenti di MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823806"
---
# <span data-ttu-id="cec18-103">Aggiornamento da versioni precedenti di MBAM</span><span class="sxs-lookup"><span data-stu-id="cec18-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="cec18-104">È possibile aggiornare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) a MBAM 2.0, con la topologia autonoma o di Configuration Manager, eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cec18-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="cec18-105">**Sostituzione del server sul posto manuale** -per aggiornare il server mbam, disinstallare manualmente mbam usando il programma di installazione o il pannello di controllo e quindi installare l'infrastruttura di MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="cec18-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="cec18-106">Non è necessario rimuovere i database.</span><span class="sxs-lookup"><span data-stu-id="cec18-106">You do not have to remove the databases.</span></span> <span data-ttu-id="cec18-107">La disinstallazione del server MBAM 1,0 lascia intatti i database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="cec18-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="cec18-108">Se specifichi gli stessi database che MBAM 1,0 stava usando, l'installazione di MBAM 2.0 mantiene i dati di MBAM 1,0 nei database e converte i database in modo che funzionino con MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="cec18-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="cec18-109">**Aggiornamento client distribuito** : se si usa la topologia di mbam autonoma, è possibile aggiornare gradualmente i client mbam dopo l'installazione dell'infrastruttura del Server MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="cec18-110">Il server MBAM 2,0 rileva la versione del client esistente ed esegue i passaggi necessari per eseguire l'aggiornamento al client 2,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="cec18-111">Dopo aver aggiornato l'infrastruttura server MBAM 2,0, i client MBAM 1,0 continuano a segnalare al server MBAM 2,0 con successo, i dati di recupero escrowing, ma la conformità sarà basata sui criteri in MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="cec18-112">È necessario aggiornare i client a MBAM 2,0 per avere i computer client con precisione segnalare la conformità con i criteri di MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="cec18-113">Puoi aggiornare i client al client MBAM 2,0 senza disinstallare il client precedente e il client inizierà a applicare i criteri di MBAM 2,0 e segnalarli.</span><span class="sxs-lookup"><span data-stu-id="cec18-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="cec18-114">Se si usa MBAM con Configuration Manager, è necessario aggiornare i client di MBAM 1,0 a MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="cec18-115">Aggiornamento di MBAM da un'architettura a due server</span><span class="sxs-lookup"><span data-stu-id="cec18-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="cec18-116">Usare le istruzioni seguenti per eseguire l'aggiornamento da una versione precedente di MBAM quando si usa un'architettura a due server, in cui un server ospita i componenti di Microsoft SQL Server e l'altro server ospita i siti Web e i servizi.</span><span class="sxs-lookup"><span data-stu-id="cec18-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="cec18-117">Per aggiornare MBAM da un'architettura a due server</span><span class="sxs-lookup"><span data-stu-id="cec18-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="cec18-118">Nel pannello di controllo del server con le caratteristiche di SQL Server selezionare **programmi e funzionalità**e quindi disinstallare l' **amministrazione e il monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="cec18-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="cec18-119">Il database di ripristino e il database di conformità e controllo restano invariati.</span><span class="sxs-lookup"><span data-stu-id="cec18-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="cec18-120">Eseguire **MBAMSetup.exe** per la versione MBAM 2,0, facoltativamente selezionare il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="cec18-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="cec18-121">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cec18-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="cec18-122">Nella pagina **Selezione topologia** selezionare la topologia di integrazione **autonoma** o **System Center Configuration Manager** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="cec18-123">Nella pagina **selezionare le caratteristiche da installare** deselezionare le caratteristiche server **self-service** e **amministrazione e monitoraggio server** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="cec18-124">Attendere che i controlli dei prerequisiti finiscano e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="cec18-125">Se viene rilevato un prerequisito mancante, risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="cec18-126">Nell' **account di fornitura usato per accedere alla pagina database mbam** , specificare il nome del computer per il server che ospiterà i siti e i servizi e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="cec18-127">Nella pagina **Configura database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cec18-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="cec18-128">Devi anche specificare la posizione in cui verranno individuati i file di database e le informazioni di log.</span><span class="sxs-lookup"><span data-stu-id="cec18-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="cec18-129">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="cec18-130">Nella pagina **Configura il database di conformità e controllo** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="cec18-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="cec18-131">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="cec18-132">Nella pagina **configurare i report di conformità e controllo** specificare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo e specificare un account utente di dominio e una password per accedere al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="cec18-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="cec18-133">Configurare la password per l'account per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="cec18-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="cec18-134">L'account utente può accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="cec18-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="cec18-135">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="cec18-136">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="cec18-137">Ciò non consente di attivare gli aggiornamenti automatici in Windows.</span><span class="sxs-lookup"><span data-stu-id="cec18-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="cec18-138">Se in precedenza si è scelto di usare Microsoft Update per questo prodotto o un altro prodotto, la pagina Microsoft Update non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="cec18-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="cec18-139">Nella pagina **Riepilogo installazione** esaminare le caratteristiche che verranno installate e quindi fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cec18-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="cec18-140">Per disinstallare le funzionalità di amministrazione e monitoraggio del server e per completare l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cec18-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="cec18-141">Nel computer che ospita le funzionalità di amministrazione e monitoraggio del server selezionare **programmi e funzionalità**nel pannello di controllo e quindi disinstallare mbam per rimuovere i siti e i servizi installati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="cec18-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="cec18-142">Eseguire la **MBAMSetup.exe** per la versione 2,0, facoltativamente selezionare il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="cec18-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="cec18-143">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cec18-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="cec18-144">Nella pagina **Selezione topologia** selezionare la topologia di integrazione **autonoma** o **System Center Configuration Manager** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="cec18-145">Nella pagina **selezionare le caratteristiche da installare** deselezionare le caratteristiche **del database di ripristino** e della **conformità e del database di controllo** e **conformità e controllo dei report** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="cec18-146">Attendere che i controlli dei prerequisiti finiscano e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="cec18-147">Se viene rilevato un prerequisito mancante, risolvere prima di tutto i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="cec18-148">Nella pagina **Configura sicurezza comunicazioni di rete** scegliere se usare la crittografia SSL (Secure Socket Layer) per i siti Web e i servizi.</span><span class="sxs-lookup"><span data-stu-id="cec18-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="cec18-149">Se si decide di crittografare la comunicazione, selezionare il certificato dell'autorità di certificazione (CA) da usare per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="cec18-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="cec18-150">**Nota**  Il certificato deve essere creato prima di questo passaggio per consentire di selezionarlo in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="cec18-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="cec18-151">Nella pagina **Configura il percorso della pagina database dello stato di conformità** specificare il nome dell'istanza di SQL Server e il nome del database in cui sono archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="cec18-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="cec18-152">Devi anche specificare la posizione in cui verranno individuati i file di database e le informazioni di log.</span><span class="sxs-lookup"><span data-stu-id="cec18-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="cec18-153">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="cec18-154">Nella pagina **Configura il percorso della pagina del database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui sono archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cec18-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="cec18-155">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="cec18-156">Nella pagina **configurare i report di conformità e controllo** immettere l'URL dell'istanza di report configurata nell'altro server.</span><span class="sxs-lookup"><span data-stu-id="cec18-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="cec18-157">Usare il pulsante **test** per verificare che sia possibile raggiungere il sito.</span><span class="sxs-lookup"><span data-stu-id="cec18-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="cec18-158">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="cec18-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="cec18-159">Nella pagina **Configura il portale self-service** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="cec18-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="cec18-160">**Nota**  Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="cec18-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="cec18-161">Nella pagina **Configura il server di amministrazione e monitoraggio** specificare la directory virtuale desiderata per il sito Web dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="cec18-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="cec18-162">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="cec18-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="cec18-163">Questo passaggio non consente di attivare gli aggiornamenti automatici in Windows.</span><span class="sxs-lookup"><span data-stu-id="cec18-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="cec18-164">Se in precedenza si è scelto di usare Microsoft Update per questo prodotto o un altro prodotto, la pagina Microsoft Update non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="cec18-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="cec18-165">Nella pagina **Riepilogo installazione** esaminare le caratteristiche che verranno installate e quindi fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cec18-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="cec18-166">Per verificare che l'aggiornamento sia stato eseguito correttamente, verifica che sia possibile raggiungere ogni sito da un altro computer del dominio.</span><span class="sxs-lookup"><span data-stu-id="cec18-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="cec18-167">Aggiornamento del client MBAM nei computer degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="cec18-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="cec18-168">Per aggiornare i computer degli utenti finali al client MBAM 2,0, eseguire **MbamClientSetup.exe** su ogni computer client.</span><span class="sxs-lookup"><span data-stu-id="cec18-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="cec18-169">Il programma di installazione aggiorna automaticamente il client al client MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cec18-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="cec18-170">È possibile installare il client MBAM tramite un sistema di distribuzione elettronica del software, strumenti come servizi di dominio Active Directory o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cec18-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="cec18-171">Per convalidare l'aggiornamento del client, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cec18-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="cec18-172">Attendere il completamento del ciclo di Reporting configurato e quindi avviare **SQL Server Management Studio** nel computer SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cec18-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="cec18-173">Nel computer SQL Server avviare **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="cec18-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="cec18-174">Verificare che la tabella **RecoveryAndHardwareCore. Machines** contenga una riga che mostra il nome del computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cec18-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="cec18-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cec18-175">Related topics</span></span>


[<span data-ttu-id="cec18-176">Distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="cec18-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





