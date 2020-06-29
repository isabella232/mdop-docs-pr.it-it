---
title: Come installare MBAM con Configuration Manager
description: Come installare MBAM con Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825126"
---
# <span data-ttu-id="ab693-103">Come installare MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ab693-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="ab693-104">Questa sezione descrive i passaggi per installare MBAM con Configuration Manager usando la configurazione consigliata, illustrata in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ab693-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="ab693-105">I passaggi sono suddivisi nelle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab693-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="ab693-106">Installare e configurare MBAM nel server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ab693-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="ab693-107">Installare i database di ripristino e controllo nel server di database</span><span class="sxs-lookup"><span data-stu-id="ab693-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="ab693-108">Installare le caratteristiche del server di amministrazione e monitoraggio nel server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="ab693-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="ab693-109">Prima di iniziare l'installazione, verificare di aver modificato o creato i file MOF necessari.</span><span class="sxs-lookup"><span data-stu-id="ab693-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="ab693-110">Per istruzioni, vedere [come creare o modificare i file MOF](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ab693-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="ab693-111">**Importante**  Se si usa un'istanza di SQL Server Reporting Services (SSRS) non predefinita, è necessario avviare la configurazione di MBAM usando la riga di comando seguente per specificare l'istanza denominata SSRS:</span><span class="sxs-lookup"><span data-stu-id="ab693-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="ab693-112">Per installare MBAM nel server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ab693-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="ab693-113">Nel server Configuration Manager eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="ab693-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="ab693-114">**Nota**  Per ottenere i file di log di configurazione, è necessario usare il pacchetto msiexec e l'opzione **/l** &lt; location &gt; per installare Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ab693-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="ab693-115">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ab693-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="ab693-116">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel computer dell'utente che sta installando Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ab693-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="ab693-117">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="ab693-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="ab693-118">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="ab693-119">Nella pagina **Selezione topologia** selezionare **integrazione di System Center Configuration Manager**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="ab693-120">Nella pagina **selezionare le caratteristiche da installare** selezionare **System Center Configuration Manager Integration**.</span><span class="sxs-lookup"><span data-stu-id="ab693-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="ab693-121">**Nota**  Nella pagina **Verifica prerequisiti** fare clic su **Avanti** dopo che l'installazione guidata controlla i prerequisiti per l'installazione e conferma che non sono mancanti.</span><span class="sxs-lookup"><span data-stu-id="ab693-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="ab693-122">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti.**</span><span class="sxs-lookup"><span data-stu-id="ab693-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="ab693-123">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="ab693-124">L'uso di Microsoft Updates non consente di attivare gli aggiornamenti automatici in Windows.</span><span class="sxs-lookup"><span data-stu-id="ab693-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="ab693-125">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="ab693-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="ab693-126">Nella pagina **Riepilogo installazione** esaminare l'elenco delle caratteristiche che verranno installate e fare clic su **Installa** per avviare l'installazione delle funzionalità di mbam.</span><span class="sxs-lookup"><span data-stu-id="ab693-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="ab693-127">Fare clic su **Torna** per tornare alla procedura guidata se è necessario rivedere o modificare le impostazioni di installazione oppure fare clic su **Annulla** per uscire dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="ab693-128">Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ab693-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="ab693-129">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="ab693-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="ab693-130">Per installare i database di ripristino e controllo nel server di database</span><span class="sxs-lookup"><span data-stu-id="ab693-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="ab693-131">Nel server database eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="ab693-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="ab693-132">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="ab693-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="ab693-133">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="ab693-134">Nella pagina **Selezione topologia** selezionare la topologia di **integrazione di System Center Configuration Manager** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="ab693-135">Dall'elenco delle caratteristiche da installare selezionare database di **ripristino** e **database di controllo**e deselezionare le caratteristiche rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ab693-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="ab693-136">**Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="ab693-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="ab693-137">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="ab693-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="ab693-138">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="ab693-139">Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.</span><span class="sxs-lookup"><span data-stu-id="ab693-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="ab693-140">Nella pagina **Configura database di ripristino** specificare i nomi dei computer in cui verrà eseguita la funzionalità di amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="ab693-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="ab693-141">Dopo la distribuzione della funzionalità di amministrazione e monitoraggio del server, usa il proprio account di dominio per connettersi al database.</span><span class="sxs-lookup"><span data-stu-id="ab693-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="ab693-142">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="ab693-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="ab693-143">Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ab693-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="ab693-144">È inoltre necessario specificare sia la posizione in cui si trova il database, sia dove verranno individuate le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="ab693-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="ab693-145">Fare clic su **Avanti** per continuare con l'installazione guidata di mbam setup.</span><span class="sxs-lookup"><span data-stu-id="ab693-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="ab693-146">Nella pagina **Configura database di controllo** specificare l'account utente che verrà usato per accedere al database per i report.</span><span class="sxs-lookup"><span data-stu-id="ab693-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="ab693-147">Specificare i nomi di computer dei computer in cui verranno eseguiti il server di amministrazione e monitoraggio e i report di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab693-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="ab693-148">Dopo la distribuzione delle funzionalità Amministrazione e monitoraggio e report di controllo, gli account di dominio verranno usati per la connessione ai database.</span><span class="sxs-lookup"><span data-stu-id="ab693-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="ab693-149">**Nota**  Se si sta installando il database di controllo senza la caratteristica rapporti di controllo, è necessario aggiungere un'eccezione nel computer del database di controllo per abilitare il traffico in ingresso nella porta di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab693-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="ab693-150">Il numero di porta predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="ab693-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="ab693-151">Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab693-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="ab693-152">Devi anche specificare la posizione in cui verranno individuate le informazioni sul database e sul log.</span><span class="sxs-lookup"><span data-stu-id="ab693-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="ab693-153">Fare clic su **Installa** per avviare l'installazione e quindi fare clic su **fine** per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="ab693-154">Per installare le funzionalità di amministrazione e monitoraggio del server nel server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="ab693-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="ab693-155">Nel server di amministrazione e monitoraggio eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="ab693-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="ab693-156">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="ab693-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="ab693-157">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="ab693-158">Nella pagina **Selezione topologia** selezionare la topologia di **integrazione di System Center Configuration Manager** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="ab693-159">Dall'elenco delle caratteristiche da installare selezionare **amministrazione e monitoraggio del server** e del **portale self-service**e deselezionare le caratteristiche rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ab693-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="ab693-160">**Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="ab693-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="ab693-161">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="ab693-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="ab693-162">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="ab693-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="ab693-163">Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.</span><span class="sxs-lookup"><span data-stu-id="ab693-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="ab693-164">Installare il portale self-service seguendo la procedura descritta nella sezione **per installare il portale self-service** in [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ab693-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="ab693-165">**Nota**  Se i computer client non avranno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, completare i passaggi descritti in **per configurare il portale self-service quando gli utenti finali non possono accedere alla sezione della rete di distribuzione dei contenuti Microsoft** [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) per configurare il portale self-service per fare riferimento ai file JavaScript da un'origine accessibile.</span><span class="sxs-lookup"><span data-stu-id="ab693-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="ab693-166">Installare le funzionalità di amministrazione e monitoraggio del server eseguendo la procedura descritta nella sezione **per installare la caratteristica del server di amministrazione e monitoraggio** in [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ab693-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="ab693-167">Fare clic su **fine** per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ab693-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="ab693-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab693-168">Related topics</span></span>


[<span data-ttu-id="ab693-169">Come convalidare l'installazione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ab693-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="ab693-170">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ab693-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





