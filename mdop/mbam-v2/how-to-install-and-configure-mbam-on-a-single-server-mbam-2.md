---
title: Come installare e configurare MBAM in un server singolo
description: Come installare e configurare MBAM in un server singolo
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824066"
---
# <span data-ttu-id="248be-103">Come installare e configurare MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="248be-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="248be-104">Le procedure descritte in questo argomento descrivono come installare Microsoft BitLocker Administration and Monitoring (MBAM) nella topologia autonoma in un singolo server.</span><span class="sxs-lookup"><span data-stu-id="248be-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="248be-105">Usare la configurazione a server singolo solo in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="248be-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="248be-106">Per gli ambienti di produzione, usa due o più server.</span><span class="sxs-lookup"><span data-stu-id="248be-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="248be-107">Se si sta installando l'amministrazione e il monitoraggio di Microsoft BitLocker tramite la topologia di Configuration Manager, vedere [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="248be-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="248be-108">Il diagramma seguente mostra un esempio di architettura a server singolo.</span><span class="sxs-lookup"><span data-stu-id="248be-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="248be-109">Per una descrizione dei database e delle caratteristiche, vedere [architettura di alto livello per MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="248be-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![singola topologia di distribuzione di MBAM 2 server](images/mbam2-1-server.gif)

<span data-ttu-id="248be-111">Ogni funzionalità del server ha alcuni prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="248be-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="248be-112">Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="248be-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="248be-113">Inoltre, alcune caratteristiche includono anche informazioni che devono essere fornite durante il processo di installazione per la distribuzione corretta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="248be-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="248be-114">Dovresti anche rivedere [la preparazione dell'ambiente per mbam 2,0 prima di iniziare la distribuzione di](preparing-your-environment-for-mbam-20-mbam-2.md) mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="248be-115">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-115">Note</span></span>**  
<span data-ttu-id="248be-116">Per ottenere i file di log della configurazione, è necessario usare il pacchetto msiexec **/L** e l' &lt; &gt; opzione di posizione/l per installare mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="248be-117">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="248be-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="248be-118">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel server dell'utente che sta installando MBAM.</span><span class="sxs-lookup"><span data-stu-id="248be-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="248be-119">Per installare le funzionalità di MBAM server in un singolo server</span><span class="sxs-lookup"><span data-stu-id="248be-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="248be-120">I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.</span><span class="sxs-lookup"><span data-stu-id="248be-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="248be-121">Per avviare l'installazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="248be-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="248be-122">Nel server in cui si vuole installare MBAM eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="248be-123">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="248be-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="248be-124">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="248be-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="248be-125">Nella pagina **Selezione topologia** **selezionare la topologia autonoma** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="248be-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="248be-126">Nella pagina **selezionare le caratteristiche da installare** selezionare le caratteristiche che si desidera installare.</span><span class="sxs-lookup"><span data-stu-id="248be-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="248be-127">Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="248be-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="248be-128">Le caratteristiche da installare nello stesso computer devono essere installate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="248be-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="248be-129">Deselezionare le caselle di controllo relative a tutte le funzionalità che si desidera installare altrove.</span><span class="sxs-lookup"><span data-stu-id="248be-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="248be-130">È necessario installare le caratteristiche di MBAM nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="248be-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="248be-131">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="248be-131">Recovery Database</span></span>

    -   <span data-ttu-id="248be-132">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="248be-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="248be-133">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="248be-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="248be-134">Server self-service</span><span class="sxs-lookup"><span data-stu-id="248be-134">Self-Service Server</span></span>

    -   <span data-ttu-id="248be-135">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="248be-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="248be-136">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="248be-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="248be-137">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-137">Note</span></span>**  
    <span data-ttu-id="248be-138">La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="248be-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="248be-139">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="248be-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="248be-140">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="248be-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="248be-141">Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.</span><span class="sxs-lookup"><span data-stu-id="248be-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="248be-142">Nella pagina **Configura sicurezza comunicazioni di rete** scegliere se crittografare la comunicazione tra i servizi Web nel server di amministrazione e monitoraggio e nei client.</span><span class="sxs-lookup"><span data-stu-id="248be-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="248be-143">Se si decide di crittografare la comunicazione, selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="248be-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="248be-144">Il certificato deve essere creato prima di questo passaggio per consentire di selezionarlo in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="248be-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="248be-145">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-145">Note</span></span>**  
    <span data-ttu-id="248be-146">Questa pagina viene visualizzata solo se è stata selezionata la caratteristica portale self-service o amministrazione e monitoraggio server nella pagina **selezionare le caratteristiche da installare** .</span><span class="sxs-lookup"><span data-stu-id="248be-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="248be-147">Fare clic su **Avanti**e quindi passare al set di passaggi successivo per configurare le caratteristiche del server mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="248be-148">Per configurare le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="248be-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="248be-149">Nella pagina **Configura database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="248be-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="248be-150">È inoltre necessario specificare sia la posizione in cui si trovano i file di database che le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="248be-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="248be-151">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="248be-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="248be-152">Nella pagina **Configura il database di conformità e controllo** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="248be-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="248be-153">Devi anche specificare la posizione in cui si trovano i file di database e dove verranno individuate le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="248be-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="248be-154">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="248be-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="248be-155">Nella pagina **configurare i report di conformità e controllo** specificare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo e specificare un account utente di dominio e una password per accedere al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="248be-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="248be-156">Configurare la password per l'account per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="248be-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="248be-157">L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="248be-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="248be-158">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="248be-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="248be-159">Nella pagina **Configura il portale self-service** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="248be-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="248be-160">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-160">Note</span></span>**  
    <span data-ttu-id="248be-161">Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="248be-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="248be-162">Se si usa Windows Firewall, la porta verrà aperta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="248be-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="248be-163">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="248be-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="248be-164">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="248be-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="248be-165">Ciò non consente di attivare gli aggiornamenti automatici in Windows.</span><span class="sxs-lookup"><span data-stu-id="248be-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="248be-166">Nella pagina **Configura il server di amministrazione e monitoraggio** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il sito Web dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="248be-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="248be-167">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-167">Note</span></span>**  
    <span data-ttu-id="248be-168">Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="248be-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="248be-169">Se si usa Windows Firewall, la porta verrà aperta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="248be-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="248be-170">Nella pagina **Riepilogo installazione** esaminare l'elenco delle caratteristiche che verranno installate e fare clic su **Installa** per avviare l'installazione delle funzionalità di mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="248be-171">Fare clic su **Torna** per tornare alla procedura guidata se è necessario rivedere o modificare le impostazioni di installazione oppure fare clic su **Annulla** per uscire dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="248be-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="248be-172">Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="248be-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="248be-173">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="248be-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="248be-174">Dopo aver installato le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker, passare alla sezione successiva e completare la procedura per aggiungere utenti ai ruoli di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="248be-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="248be-175">Per altre informazioni sui ruoli, vedere [pianificazione dei ruoli di amministratore di MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="248be-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="248be-176">Per eseguire la configurazione post-installazione</span><span class="sxs-lookup"><span data-stu-id="248be-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="248be-177">Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti per consentire l'accesso alle funzionalità del sito Web di MBAM help desk:</span><span class="sxs-lookup"><span data-stu-id="248be-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="248be-178">**Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="248be-179">Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="248be-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="248be-180">**Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="248be-181">Per gli utenti di helpdesk avanzati, è necessario solo il campo **ID chiave** in recupero unità.</span><span class="sxs-lookup"><span data-stu-id="248be-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="248be-182">In Manage TPM sono necessari solo il campo **computer Domain** e il **nome computer** .</span><span class="sxs-lookup"><span data-stu-id="248be-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="248be-183">Nel server di amministrazione e monitoraggio aggiungere utenti al gruppo locale seguente per consentire loro di accedere alla funzionalità report nel sito Web amministrazione e monitoraggio di MBAM:</span><span class="sxs-lookup"><span data-stu-id="248be-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="248be-184">**Utenti di report mbam**: i membri di questo gruppo locale possono accedere alle funzionalità report nel sito Web amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="248be-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="248be-185">Marca il portale self-service con il nome della società, il testo dell'avviso e altre informazioni specifiche della società.</span><span class="sxs-lookup"><span data-stu-id="248be-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="248be-186">Per istruzioni, Vedi [come personalizzare il portale self-service](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="248be-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="248be-187">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-187">Note</span></span>**  
    <span data-ttu-id="248be-188">L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="248be-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="248be-189">Il modo consigliato per eseguire questa operazione consiste nel creare un gruppo di sicurezza del dominio e aggiungere il gruppo di dominio a ogni gruppo di utenti del report MBAM locale.</span><span class="sxs-lookup"><span data-stu-id="248be-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="248be-190">Quando si usa questo processo, gestire le appartenenze ai gruppi tramite il gruppo di domini.</span><span class="sxs-lookup"><span data-stu-id="248be-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="248be-191">Convalida dell'installazione della funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="248be-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="248be-192">Dopo aver completato l'installazione di amministrazione e monitoraggio di Microsoft BitLocker, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM necessarie per la gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="248be-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="248be-193">Usare la procedura seguente per verificare che il servizio MBAM sia funzionante.</span><span class="sxs-lookup"><span data-stu-id="248be-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="248be-194">Per convalidare l'installazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="248be-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="248be-195">In ogni server in cui è distribuita una caratteristica di MBAM aprire il **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="248be-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="248be-196">Selezionare **programmi**e quindi selezionare **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="248be-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="248be-197">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="248be-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="248be-198">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-198">Note</span></span>**  
   <span data-ttu-id="248be-199">Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="248be-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="248be-200">Nel server in cui è installato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di ripristino e hardware di mbam** sia installato.</span><span class="sxs-lookup"><span data-stu-id="248be-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="248be-201">Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database dello stato di conformità di mbam** .</span><span class="sxs-lookup"><span data-stu-id="248be-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="248be-202">Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="248be-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="248be-203">La posizione iniziale predefinita di un'istanza del sito di SQL Server Reporting Services si trova in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="248be-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="248be-204">Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="248be-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="248be-205">Verificare che una cartella report denominata amministrazione e monitoraggio di Microsoft BitLocker contenga un'origine dati denominata **MaltaDataSource** e che una cartella **en-US** contenga quattro report.</span><span class="sxs-lookup"><span data-stu-id="248be-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="248be-206">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-206">Note</span></span>**  
   <span data-ttu-id="248be-207">Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="248be-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="248be-208">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**.</span><span class="sxs-lookup"><span data-stu-id="248be-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="248be-209">Selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS).**</span><span class="sxs-lookup"><span data-stu-id="248be-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="248be-210">In **connessioni** passare a \* &lt; nomecomputer &gt; \*, selezionare **siti**e quindi selezionare **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="248be-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="248be-211">Verificare che **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.</span><span class="sxs-lookup"><span data-stu-id="248be-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="248be-212">Nel server in cui sono installate le funzionalità di amministrazione e monitoraggio e il portale self-service aprire un Web browser con credenziali amministrative e individuare le posizioni seguenti per verificare che vengano caricate correttamente:</span><span class="sxs-lookup"><span data-stu-id="248be-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="248be-213">*http:// &lt; hostname &gt; /helpdesk/default.aspx* e confermare tutti i collegamenti per l'esplorazione e i report</span><span class="sxs-lookup"><span data-stu-id="248be-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="248be-214">http:// &lt; hostname &gt; /selfservice&gt;/</span><span class="sxs-lookup"><span data-stu-id="248be-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="248be-215">http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="248be-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="248be-216">http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="248be-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="248be-217">http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="248be-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="248be-218">http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="248be-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="248be-219">Nota</span><span class="sxs-lookup"><span data-stu-id="248be-219">Note</span></span>**  
   <span data-ttu-id="248be-220">Si presuppone che le funzionalità del server siano installate nella porta predefinita senza crittografia di rete.</span><span class="sxs-lookup"><span data-stu-id="248be-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="248be-221">Se sono state installate le funzionalità del server in una porta o una directory virtuale diversa, modificare gli URL per includere la porta appropriata, ad esempio *http:// &lt; hostname &gt; : &lt; Port &gt; /helpdesk/default.asp*x o*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*</span><span class="sxs-lookup"><span data-stu-id="248be-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="248be-222">Se le funzionalità del server sono state installate con la crittografia di rete, cambiare http://in https://.</span><span class="sxs-lookup"><span data-stu-id="248be-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="248be-223">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="248be-223">Related topics</span></span>


[<span data-ttu-id="248be-224">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="248be-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









