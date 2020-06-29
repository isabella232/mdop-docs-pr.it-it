---
title: Come installare e configurare MBAM su server distribuiti
description: Come installare e configurare MBAM su server distribuiti
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824056"
---
# <span data-ttu-id="af2c0-103">Come installare e configurare MBAM su server distribuiti</span><span class="sxs-lookup"><span data-stu-id="af2c0-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="af2c0-104">Le procedure descritte in questo argomento descrivono come installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 nella topologia autonoma nei server distribuiti.</span><span class="sxs-lookup"><span data-stu-id="af2c0-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="af2c0-105">Per visualizzare un diagramma dell'architettura consigliata, insieme a una descrizione dei database e delle caratteristiche, vedere [distribuzione dell'infrastruttura del server MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="af2c0-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="af2c0-106">Per installare l'amministrazione e il monitoraggio di Microsoft BitLocker con la topologia di Configuration Manager, vedere [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="af2c0-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="af2c0-107">Ogni funzionalità del server ha alcuni prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="af2c0-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="af2c0-108">Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="af2c0-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="af2c0-109">Alcune funzionalità richiedono inoltre di specificare determinate informazioni durante il processo di installazione per la distribuzione corretta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="af2c0-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="af2c0-110">Devi anche rivedere la [pianificazione per la distribuzione di mbam 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) prima di avviare la distribuzione di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="af2c0-111">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-111">Note</span></span>**  
<span data-ttu-id="af2c0-112">Per ottenere i file di log della configurazione, è necessario usare il pacchetto msiexec e **/L** l' &lt; &gt; opzione di posizione/l per installare mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="af2c0-113">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="af2c0-114">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel server dell'utente che sta installando MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="af2c0-115">Distribuzione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="af2c0-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="af2c0-116">I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="af2c0-117">Per avviare l'installazione guidata di MBAM server</span><span class="sxs-lookup"><span data-stu-id="af2c0-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="af2c0-118">Nel server in cui si vuole installare l'amministrazione e il monitoraggio di Microsoft BitLocker, eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="af2c0-119">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="af2c0-120">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="af2c0-121">Nella pagina **Selezione topologia** **selezionare la topologia autonoma** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="af2c0-122">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-122">Note</span></span>**  
    <span data-ttu-id="af2c0-123">Se si vuole installare MBAM con la topologia integrata di Configuration Manager, vedere la pagina relativa alla [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="af2c0-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="af2c0-124">Selezionare le caratteristiche che si desidera installare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-124">Select the features that you want to install.</span></span> <span data-ttu-id="af2c0-125">Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="af2c0-126">Deselezionare le caratteristiche che si desidera installare altrove.</span><span class="sxs-lookup"><span data-stu-id="af2c0-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="af2c0-127">Le caratteristiche che verranno installate nello stesso computer devono essere installate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="af2c0-128">È necessario installare le caratteristiche di MBAM nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="af2c0-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="af2c0-129">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="af2c0-129">Recovery Database</span></span>

    -   <span data-ttu-id="af2c0-130">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="af2c0-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="af2c0-131">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="af2c0-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="af2c0-132">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="af2c0-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="af2c0-133">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="af2c0-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="af2c0-134">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="af2c0-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="af2c0-135">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-135">Note</span></span>**  
    <span data-ttu-id="af2c0-136">La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="af2c0-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="af2c0-137">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="af2c0-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="af2c0-138">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="af2c0-139">Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.</span><span class="sxs-lookup"><span data-stu-id="af2c0-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="af2c0-140">Per installare il database di ripristino</span><span class="sxs-lookup"><span data-stu-id="af2c0-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="af2c0-141">Nella pagina **Configura database di ripristino** specificare i nomi dei computer in cui verrà eseguita la funzionalità di amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="af2c0-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="af2c0-142">Dopo la distribuzione della funzionalità di amministrazione e monitoraggio del server, usa il proprio account di dominio per connettersi al database.</span><span class="sxs-lookup"><span data-stu-id="af2c0-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="af2c0-143">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="af2c0-144">Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="af2c0-145">È inoltre necessario specificare sia la posizione in cui si trova il database, sia dove verranno individuate le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="af2c0-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="af2c0-146">Fare clic su **Avanti** per continuare con la configurazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="af2c0-147">Per installare il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="af2c0-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="af2c0-148">Nella pagina **Configura il database di conformità e controllo** specificare l'account utente che verrà usato per accedere al database per i report.</span><span class="sxs-lookup"><span data-stu-id="af2c0-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="af2c0-149">Specificare i nomi di computer dei computer in cui verranno eseguiti il server di amministrazione e monitoraggio e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="af2c0-150">Una volta distribuiti l'amministrazione e il monitoraggio e il server dei report di conformità e controllo, questi usano gli account di dominio per connettersi ai database.</span><span class="sxs-lookup"><span data-stu-id="af2c0-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="af2c0-151">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-151">Note</span></span>**  
    <span data-ttu-id="af2c0-152">Se si sta installando il database di conformità e controllo senza la caratteristica conformità e rapporti di controllo, è necessario aggiungere un'eccezione nel computer di database di conformità e controllo per abilitare il traffico in ingresso nella porta di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af2c0-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="af2c0-153">Il numero di porta predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="af2c0-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="af2c0-154">Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="af2c0-155">Devi anche specificare la posizione in cui verranno individuate le informazioni sul database e sul log.</span><span class="sxs-lookup"><span data-stu-id="af2c0-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="af2c0-156">Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af2c0-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="af2c0-157">Per installare i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="af2c0-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="af2c0-158">Nella pagina **configura report di conformità e controllo** specificare il nome dell'istanza di SQL Server remoto, ad esempio nomeserver, in &lt; &gt; cui è stato installato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="af2c0-159">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-159">Note</span></span>**  
    <span data-ttu-id="af2c0-160">Se si installano i report di conformità e controllo senza il server di amministrazione e monitoraggio, è necessario aggiungere un'eccezione nel computer del report di conformità e controllo per abilitare il traffico in ingresso nella porta del server di report (la porta predefinita è 80).</span><span class="sxs-lookup"><span data-stu-id="af2c0-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="af2c0-161">Specificare il nome del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="af2c0-162">Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM, anche se è possibile modificare il nome quando si installa il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="af2c0-163">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="af2c0-164">Selezionare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="af2c0-165">Specificare un account utente di dominio e una password per accedere al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="af2c0-166">Configurare la password per l'account per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="af2c0-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="af2c0-167">L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="af2c0-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="af2c0-168">Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af2c0-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="af2c0-169">Per installare il portale self-service</span><span class="sxs-lookup"><span data-stu-id="af2c0-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="af2c0-170">Nella pagina **Configura il portale self-service** è possibile facoltativamente crittografare la comunicazione tra il portale self-service e i server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="af2c0-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="af2c0-171">Se si sceglie l'opzione per crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="af2c0-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="af2c0-172">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="af2c0-173">Specificare l'istanza remota di SQL Server, ad esempio \* &lt; NomeServer &gt; \*, in cui è stato installato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="af2c0-174">Specificare il nome del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="af2c0-175">Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="af2c0-176">È tuttavia possibile modificare il nome quando si installa il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="af2c0-177">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="af2c0-178">Specificare l'istanza remota di SQL Server, ad esempio \* &lt; NomeServer &gt; \*, in cui è stato installato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="af2c0-179">Specificare il nome del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="af2c0-180">Per impostazione predefinita, il nome del database è **mbam Recovery and hardware**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="af2c0-181">È tuttavia possibile modificare il nome durante l'installazione della caratteristica del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="af2c0-182">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="af2c0-183">Immettere il **numero di porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="af2c0-184">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-184">Note</span></span>**  
    <span data-ttu-id="af2c0-185">Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="af2c0-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="af2c0-186">Se si usa Windows Firewall, la porta verrà aperta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="af2c0-187">Per registrare facoltativamente un nome dell'entità servizio (SPN) per il portale self-service, selezionare **registra SPN (Service Principal Name) di questo computer con Active Directory (obbligatorio per l'autenticazione di Windows)**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="af2c0-188">Se si seleziona questa casella di controllo, MBAM Setup non tenterà di registrare i nomi SPN esistenti ed è possibile registrare manualmente l'SPN prima o dopo l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="af2c0-189">Per istruzioni su come registrare manualmente l'SPN, vedere [registrazione manuale di SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="af2c0-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="af2c0-190">Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af2c0-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="af2c0-191">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="af2c0-192">Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="af2c0-193">Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="af2c0-194">Fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="af2c0-195">Fare clic su **Annulla** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="af2c0-196">Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="af2c0-197">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="af2c0-198">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-198">Note</span></span>**  
    <span data-ttu-id="af2c0-199">Per configurare il portale self-service dopo averlo installato, personalizzare il portale self-service con il nome della società e altre informazioni specifiche della società, vedere [come personalizzare il portale self-service](how-to-brand-the-self-service-portal.md) per le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="af2c0-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="af2c0-200">Se i computer client hanno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, è stata completata l'installazione del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="af2c0-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="af2c0-201">Se i computer client non hanno accesso alla rete CDN Microsoft, completare i passaggi della sezione successiva per configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile.</span><span class="sxs-lookup"><span data-stu-id="af2c0-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="af2c0-202">Per configurare il portale self-service quando gli utenti finali non riescono ad accedere alla rete di distribuzione dei contenuti Microsoft</span><span class="sxs-lookup"><span data-stu-id="af2c0-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="af2c0-203">Se i computer client hanno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, viene completata l'installazione del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="af2c0-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="af2c0-204">Se i computer client non hanno accesso alla rete CDN Microsoft, completare i passaggi rimanenti in questa sezione per configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile.</span><span class="sxs-lookup"><span data-stu-id="af2c0-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="af2c0-205">Scaricare i quattro file JavaScript da Microsoft CDN:</span><span class="sxs-lookup"><span data-stu-id="af2c0-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="af2c0-206">jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="af2c0-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="af2c0-207">MicrosoftAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="af2c0-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="af2c0-208">MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="af2c0-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="af2c0-209">MicrosoftMvcValidation.js-</span><span class="sxs-lookup"><span data-stu-id="af2c0-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="af2c0-210">Copiare i file JavaScript nella directory **Scripts** del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="af2c0-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="af2c0-211">Questa directory si trova in <em> &lt; mbam self-service install directory &gt; \\ </em> self service Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="af2c0-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="af2c0-212">Aprire **Gestione Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="af2c0-213">Espandere i **siti** &gt; **di amministrazione e monitoraggio di Microsoft BitLocker**ed evidenziare **selfservice**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="af2c0-214">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-214">Note</span></span>**  
   <span data-ttu-id="af2c0-215">*Selfservice* è il nome della directory virtuale predefinita.</span><span class="sxs-lookup"><span data-stu-id="af2c0-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="af2c0-216">Se si è scelto un nome diverso per questa directory durante l'installazione, ricordarsi di sostituire *selfservice* nelle rimanenti istruzioni con il nome scelto.</span><span class="sxs-lookup"><span data-stu-id="af2c0-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="af2c0-217">Nel riquadro centrale fare doppio clic su **Impostazioni applicazione**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="af2c0-218">Per ogni elemento dell'elenco seguente modificare le impostazioni dell'applicazione per fare riferimento alla nuova posizione sostituendo &lt; directory virtuale &gt; con/selfservice/(o il nome scelto durante l'installazione).</span><span class="sxs-lookup"><span data-stu-id="af2c0-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="af2c0-219">Il percorso della directory virtuale, ad esempio, sarà simile a/selfservice/scripts/jquery-1.7.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="af2c0-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="af2c0-220">jQueryPath:/ &lt; directory virtuale &gt; /script/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="af2c0-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="af2c0-221">MicrosoftAjaxPath:/ &lt; directory virtuale &gt; /script/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="af2c0-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="af2c0-222">MicrosoftMvcAjaxPath:/ &lt; directory virtuale &gt; /script/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="af2c0-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="af2c0-223">MicrosoftMvcValidationPath:/ &lt; directory virtuale &gt; /script/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="af2c0-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="af2c0-224">Per installare la funzionalità di amministrazione e monitoraggio del server</span><span class="sxs-lookup"><span data-stu-id="af2c0-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="af2c0-225">MBAM può crittografare le comunicazioni tra i servizi Web e i server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="af2c0-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="af2c0-226">Se si sceglie l'opzione per crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="af2c0-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="af2c0-227">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="af2c0-228">Specificare l'istanza remota di SQL Server, ad esempio \* &lt; NomeServer &gt; \*, in cui è stato installato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="af2c0-229">Specificare il nome del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="af2c0-230">Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="af2c0-231">È tuttavia possibile modificare il nome quando si installa il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="af2c0-232">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="af2c0-233">Specificare l'istanza remota di SQL Server, ad esempio \* &lt; NomeServer &gt; \*, in cui è stato installato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="af2c0-234">Specificare il nome del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="af2c0-235">Per impostazione predefinita, il nome del database è **mbam Recovery and hardware**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="af2c0-236">È tuttavia possibile modificare il nome durante l'installazione della caratteristica del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="af2c0-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="af2c0-237">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="af2c0-238">Specificare l'URL per la "Home" del sito di SQL Server Reporting Services (SRS).</span><span class="sxs-lookup"><span data-stu-id="af2c0-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="af2c0-239">La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è:</span><span class="sxs-lookup"><span data-stu-id="af2c0-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="af2c0-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer</span><span class="sxs-lookup"><span data-stu-id="af2c0-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="af2c0-241">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-241">Note</span></span>**  
   <span data-ttu-id="af2c0-242">Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL è simile al seguente: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="af2c0-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="af2c0-243">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="af2c0-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="af2c0-244">Immettere il **numero di porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="af2c0-245">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-245">Note</span></span>**  
    <span data-ttu-id="af2c0-246">Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="af2c0-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="af2c0-247">Se si usa Windows Firewall, la porta verrà aperta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="af2c0-248">Per registrare facoltativamente un nome dell'entità servizio (SPN) per il portale self-service, selezionare **registra SPN (Service Principal Name) di questo computer con Active Directory (obbligatorio per l'autenticazione di Windows)**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="af2c0-249">Se si seleziona questa casella di controllo, MBAM Setup non tenterà di registrare i nomi SPN esistenti ed è possibile registrare manualmente l'SPN prima o dopo l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="af2c0-250">Per istruzioni su come registrare manualmente l'SPN, vedere [registrazione manuale di SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="af2c0-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="af2c0-251">Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af2c0-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="af2c0-252">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="af2c0-253">Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="af2c0-254">Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="af2c0-255">Fare clic su **Installa** per eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="af2c0-256">Fare clic su **Annulla** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="af2c0-257">Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="af2c0-258">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="af2c0-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="af2c0-259">Per eseguire la configurazione post-installazione</span><span class="sxs-lookup"><span data-stu-id="af2c0-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="af2c0-260">Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti per consentire loro di accedere alle funzionalità del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="af2c0-261">**Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="af2c0-262">Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="af2c0-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="af2c0-263">**Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="af2c0-264">Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità.</span><span class="sxs-lookup"><span data-stu-id="af2c0-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="af2c0-265">In **Manage TPM**sono necessari solo il campo **computer Domain** e il **nome computer** .</span><span class="sxs-lookup"><span data-stu-id="af2c0-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="af2c0-266">Nel server che ospita il server di amministrazione e monitoraggio e il database di conformità e controllo e nel server che ospita i report di conformità e controllo, aggiungere utenti al gruppo locale seguente per consentire loro l'accesso alla funzionalità report nel sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="af2c0-267">**Utenti di report mbam**: i membri di questo gruppo locale possono accedere ai report nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="af2c0-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="af2c0-268">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-268">Note</span></span>**  
    <span data-ttu-id="af2c0-269">L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="af2c0-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="af2c0-270">Convalida dell'installazione della funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="af2c0-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="af2c0-271">Quando l'installazione delle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker è stata completata, è consigliabile verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM.</span><span class="sxs-lookup"><span data-stu-id="af2c0-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="af2c0-272">Usare la procedura seguente per verificare che il servizio di amministrazione e monitoraggio di Microsoft BitLocker sia funzionale.</span><span class="sxs-lookup"><span data-stu-id="af2c0-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="af2c0-273">Per convalidare un'installazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="af2c0-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="af2c0-274">In ogni server in cui è distribuita una caratteristica di MBAM, aprire il **Pannello di controllo**, selezionare **programmi**e quindi selezionare **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="af2c0-275">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="af2c0-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="af2c0-276">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-276">Note</span></span>**  
   <span data-ttu-id="af2c0-277">Per convalidare l'installazione di MBAM, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="af2c0-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="af2c0-278">Nel server in cui è installato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di ripristino e hardware di mbam** sia installato.</span><span class="sxs-lookup"><span data-stu-id="af2c0-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="af2c0-279">Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database dello stato di conformità di mbam** .</span><span class="sxs-lookup"><span data-stu-id="af2c0-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="af2c0-280">Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="af2c0-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="af2c0-281">La posizione Home predefinita di un'istanza del sito di SQL Server Reporting Services è disponibile all'indirizzo http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="af2c0-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="af2c0-282">Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af2c0-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="af2c0-283">Verificare che una cartella report denominata **amministrazione e monitoraggio di Microsoft BitLocker** contenga un'origine dati denominata **MaltaDataSource** e che una cartella **en-US** contenga quattro report.</span><span class="sxs-lookup"><span data-stu-id="af2c0-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="af2c0-284">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-284">Note</span></span>**  
   <span data-ttu-id="af2c0-285">Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="af2c0-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="af2c0-286">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="af2c0-287">Selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="af2c0-288">In **connessioni**passare a \* &lt; nomecomputer &gt; \*, selezionare **siti**e selezionare **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="af2c0-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="af2c0-289">Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.</span><span class="sxs-lookup"><span data-stu-id="af2c0-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="af2c0-290">Nel server in cui sono installate le funzionalità di amministrazione e monitoraggio e il portale self-service, aprire un Web browser con credenziali amministrative e individuare le posizioni seguenti per verificare che vengano caricate correttamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="af2c0-291">Nota</span><span class="sxs-lookup"><span data-stu-id="af2c0-291">Note</span></span>**  
   <span data-ttu-id="af2c0-292">Gli URL che terminano con ". svc" non visualizzano un sito Web.</span><span class="sxs-lookup"><span data-stu-id="af2c0-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="af2c0-293">Il successo è indicato dal messaggio "la pubblicazione dei metadati per questo servizio è attualmente disabilitata" o dal codice simile alle informazioni.</span><span class="sxs-lookup"><span data-stu-id="af2c0-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="af2c0-294">Se viene visualizzato un altro messaggio di errore o se non è possibile trovare la pagina, la pagina non è stata caricata correttamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="af2c0-295">Verificare che ogni pagina venga caricata correttamente.</span><span class="sxs-lookup"><span data-stu-id="af2c0-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="af2c0-296">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af2c0-296">Related topics</span></span>


[<span data-ttu-id="af2c0-297">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="af2c0-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









