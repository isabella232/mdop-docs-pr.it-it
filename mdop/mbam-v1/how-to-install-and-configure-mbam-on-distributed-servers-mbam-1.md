---
title: Come installare e configurare MBAM su server distribuiti
description: Come installare e configurare MBAM su server distribuiti
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825656"
---
# <span data-ttu-id="054b2-103">Come installare e configurare MBAM su server distribuiti</span><span class="sxs-lookup"><span data-stu-id="054b2-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="054b2-104">Le procedure descritte in questo argomento descrivono l'installazione completa delle funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker nei server distribuiti.</span><span class="sxs-lookup"><span data-stu-id="054b2-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="054b2-105">Ogni funzionalità del server ha alcuni prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="054b2-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="054b2-106">Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="054b2-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="054b2-107">Alcune funzionalità richiedono inoltre di specificare determinate informazioni durante il processo di installazione per la distribuzione corretta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="054b2-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="054b2-108">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-108">Note</span></span>**  
<span data-ttu-id="054b2-109">Per ottenere i file di log della configurazione, è necessario installare MBAM usando il pacchetto **msiexec** e l'opzione di \*\* &lt; posizione &gt; /l\*\* .</span><span class="sxs-lookup"><span data-stu-id="054b2-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="054b2-110">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="054b2-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="054b2-111">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che esegue l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="054b2-112">Distribuire le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="054b2-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="054b2-113">I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="054b2-114">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-114">Note</span></span>**  
<span data-ttu-id="054b2-115">Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="054b2-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="054b2-116">Per distribuire le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="054b2-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="054b2-117">Avviare l'installazione guidata di MBAM e fare clic su **Installa** nella pagina di benvenuto.</span><span class="sxs-lookup"><span data-stu-id="054b2-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="054b2-118">Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="054b2-119">Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="054b2-120">Deselezionare le caratteristiche che si desidera installare altrove.</span><span class="sxs-lookup"><span data-stu-id="054b2-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="054b2-121">Le caratteristiche che si desidera installare nello stesso computer devono essere installate tutte contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="054b2-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="054b2-122">Le caratteristiche di MBAM devono essere installate nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="054b2-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="054b2-123">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="054b2-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="054b2-124">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="054b2-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="054b2-125">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="054b2-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="054b2-126">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="054b2-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="054b2-127">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="054b2-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="054b2-128">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-128">Note</span></span>**  
    <span data-ttu-id="054b2-129">La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="054b2-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="054b2-130">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="054b2-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="054b2-131">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="054b2-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="054b2-132">Se sono soddisfatte tutte le condizioni preliminari, verrà ripresa l'installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="054b2-133">La configurazione guidata MBAM visualizzerà le pagine di installazione per le caratteristiche selezionate.</span><span class="sxs-lookup"><span data-stu-id="054b2-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="054b2-134">Nelle sezioni seguenti vengono descritte le procedure di installazione per ogni funzionalità.</span><span class="sxs-lookup"><span data-stu-id="054b2-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="054b2-135">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-135">Note</span></span>**  
    <span data-ttu-id="054b2-136">In genere, ogni funzionalità viene installata in un server separato.</span><span class="sxs-lookup"><span data-stu-id="054b2-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="054b2-137">Se si vogliono installare più funzionalità in un singolo server, è possibile modificare o eliminare alcuni dei passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="054b2-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="054b2-138">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="054b2-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="054b2-139">Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="054b2-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="054b2-140">Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="054b2-141">Fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="054b2-142">Fare clic su **Annulla** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="054b2-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="054b2-143">Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.</span><span class="sxs-lookup"><span data-stu-id="054b2-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="054b2-144">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="054b2-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="054b2-145">Aggiungere utenti ai ruoli appropriati di MBAM, dopo aver installato le funzionalità del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="054b2-146">Per altre informazioni, Vedi [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="054b2-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="054b2-147">Configurazione post-installazione</span><span class="sxs-lookup"><span data-stu-id="054b2-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="054b2-148">Dopo aver completato la configurazione di MBAM, è necessario aggiungere ruoli utente prima che gli utenti possano accedere alle funzionalità nel sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="054b2-149">Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti.</span><span class="sxs-lookup"><span data-stu-id="054b2-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="054b2-150">**Utenti di hardware MBAM**: i membri di questo gruppo locale possono accedere alla funzionalità hardware nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="054b2-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="054b2-151">**Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere alle funzionalità TPM (Trusted Platform Modules) nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="054b2-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="054b2-152">Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="054b2-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="054b2-153">**Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le funzionalità TPM nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="054b2-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="054b2-154">Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità.</span><span class="sxs-lookup"><span data-stu-id="054b2-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="054b2-155">In Manage TPM sono necessari solo il campo computer Domain e il nome computer.</span><span class="sxs-lookup"><span data-stu-id="054b2-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="054b2-156">Nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo aggiungere utenti al gruppo locale seguente per consentire l'accesso alla funzionalità report nel sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="054b2-157">**Utenti di report mbam**: i membri di questo gruppo locale possono accedere ai report nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="054b2-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="054b2-158">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-158">Note</span></span>**  
    <span data-ttu-id="054b2-159">L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="054b2-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="054b2-160">Convalidare l'installazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="054b2-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="054b2-161">Quando l'installazione della funzionalità di MBAM server è completa, devi verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM.</span><span class="sxs-lookup"><span data-stu-id="054b2-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="054b2-162">Usare la procedura seguente per verificare che il servizio MBAM sia funzionante.</span><span class="sxs-lookup"><span data-stu-id="054b2-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="054b2-163">Per convalidare un'installazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="054b2-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="054b2-164">In ogni server, in cui è distribuita una caratteristica di MBAM, aprire il **Pannello di controllo**, fare clic su **programmi**e quindi su **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="054b2-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="054b2-165">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="054b2-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="054b2-166">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-166">Note</span></span>**  
   <span data-ttu-id="054b2-167">Per convalidare l'installazione di MBAM, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="054b2-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="054b2-168">Nel server in cui è installato il database di ripristino e hardware, aprire SQL Server Management Studio e verificare che il database **hardware e ripristino di mbam** sia installato.</span><span class="sxs-lookup"><span data-stu-id="054b2-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="054b2-169">Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il database **dello stato di conformità di mbam** .</span><span class="sxs-lookup"><span data-stu-id="054b2-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="054b2-170">Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con privilegi amministrativi e passare alla Home page del sito di SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="054b2-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="054b2-171">La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è disponibile in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="054b2-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="054b2-172">Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="054b2-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="054b2-173">Verificare che sia elencata una cartella denominata **report di conformità Malta** e che contenga cinque report e un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="054b2-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="054b2-174">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-174">Note</span></span>**  
   <span data-ttu-id="054b2-175">Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="054b2-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="054b2-176">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**, selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="054b2-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="054b2-177">In **connessioni** passare a \* &lt; nomecomputer &gt; \*, fare clic su **siti**e quindi su **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="054b2-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="054b2-178">Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.</span><span class="sxs-lookup"><span data-stu-id="054b2-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="054b2-179">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio aprire un Web browser con privilegi amministrativi e passare alle posizioni seguenti nel sito Web di MBAM per verificare che vengano caricati correttamente:</span><span class="sxs-lookup"><span data-stu-id="054b2-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="054b2-180">*http:// &lt; nomecomputer &gt; /default.aspx* e confermare ognuno dei collegamenti per gli spostamenti e i report</span><span class="sxs-lookup"><span data-stu-id="054b2-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="054b2-181">http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="054b2-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="054b2-182">http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="054b2-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="054b2-183">http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="054b2-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="054b2-184">Nota</span><span class="sxs-lookup"><span data-stu-id="054b2-184">Note</span></span>**  
   <span data-ttu-id="054b2-185">In genere, i servizi vengono installati nella porta predefinita 80 senza crittografia di rete.</span><span class="sxs-lookup"><span data-stu-id="054b2-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="054b2-186">Se i servizi sono installati in una porta diversa, modificare gli URL in modo da includere la porta appropriata.</span><span class="sxs-lookup"><span data-stu-id="054b2-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="054b2-187">Ad esempio, http://\* &lt; nomecomputer &gt; : &lt; porta &gt; \*/default.aspx o http:// <em> &lt; HostHeaderName &gt; / </em> default. aspx</span><span class="sxs-lookup"><span data-stu-id="054b2-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="054b2-188">Se i servizi sono stati installati con la crittografia di rete, cambiare http://in https://.</span><span class="sxs-lookup"><span data-stu-id="054b2-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="054b2-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="054b2-189">Related topics</span></span>


[<span data-ttu-id="054b2-190">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="054b2-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









