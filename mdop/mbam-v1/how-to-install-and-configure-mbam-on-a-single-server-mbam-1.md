---
title: Come installare e configurare MBAM in un server singolo
description: Come installare e configurare MBAM in un server singolo
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824096"
---
# <span data-ttu-id="1aafc-103">Come installare e configurare MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="1aafc-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="1aafc-104">Le procedure descritte in questo argomento descrivono l'installazione completa delle funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un singolo server.</span><span class="sxs-lookup"><span data-stu-id="1aafc-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="1aafc-105">Ogni funzionalità del server ha alcuni prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="1aafc-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="1aafc-106">Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="1aafc-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="1aafc-107">Inoltre, alcune caratteristiche includono anche informazioni che devono essere fornite durante il processo di installazione per la distribuzione corretta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1aafc-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="1aafc-108">Dovresti anche rivedere la [preparazione dell'ambiente per mbam 1,0 prima di](preparing-your-environment-for-mbam-10.md) iniziare la distribuzione di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="1aafc-109">**Nota**  Per ottenere i file di log della configurazione, è necessario installare MBAM usando il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="1aafc-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="1aafc-110">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1aafc-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="1aafc-111">I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che sta installando MBAM.</span><span class="sxs-lookup"><span data-stu-id="1aafc-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="1aafc-112">Per installare le funzionalità di MBAM server in un singolo server</span><span class="sxs-lookup"><span data-stu-id="1aafc-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="1aafc-113">I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1aafc-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="1aafc-114">**Nota**  Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1aafc-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="1aafc-115">Per avviare l'installazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="1aafc-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="1aafc-116">Avviare l'installazione guidata di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1aafc-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="1aafc-117">Fare clic su **Installa** nella pagina di benvenuto.</span><span class="sxs-lookup"><span data-stu-id="1aafc-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="1aafc-118">Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="1aafc-119">Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="1aafc-120">Le caratteristiche che verranno installate nello stesso computer devono essere installate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1aafc-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="1aafc-121">Deselezionare le caratteristiche che si desidera installare altrove.</span><span class="sxs-lookup"><span data-stu-id="1aafc-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="1aafc-122">È necessario installare le caratteristiche di MBAM nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="1aafc-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="1aafc-123">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="1aafc-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="1aafc-124">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="1aafc-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="1aafc-125">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="1aafc-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="1aafc-126">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="1aafc-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="1aafc-127">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="1aafc-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="1aafc-128">**Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="1aafc-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="1aafc-129">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="1aafc-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="1aafc-130">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="1aafc-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="1aafc-131">Dopo aver soddisfatto tutti i prerequisiti, l'installazione riprende.</span><span class="sxs-lookup"><span data-stu-id="1aafc-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="1aafc-132">Viene richiesto di configurare la sicurezza delle comunicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="1aafc-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="1aafc-133">MBAM può crittografare la comunicazione tra il database di ripristino e hardware, il server di amministrazione e monitoraggio e i client.</span><span class="sxs-lookup"><span data-stu-id="1aafc-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="1aafc-134">Se si decide di crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità che verrà usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="1aafc-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="1aafc-135">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="1aafc-136">La configurazione guidata MBAM visualizzerà le pagine di installazione per le caratteristiche selezionate.</span><span class="sxs-lookup"><span data-stu-id="1aafc-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="1aafc-137">Per distribuire le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="1aafc-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="1aafc-138">Nella finestra **Configura database hardware e ripristino** specificare l'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="1aafc-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="1aafc-139">È inoltre necessario specificare sia la posizione dei file di database che il percorso delle informazioni del log.</span><span class="sxs-lookup"><span data-stu-id="1aafc-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="1aafc-140">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="1aafc-141">Nella finestra **Configura database di conformità e controllo** specificare l'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="1aafc-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="1aafc-142">Specificare quindi la posizione dei file di database e il percorso delle informazioni del log.</span><span class="sxs-lookup"><span data-stu-id="1aafc-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="1aafc-143">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="1aafc-144">Nella finestra **report conformità e controllo** specificare l'istanza del servizio report che verrà usata e fornirà un account utente di dominio per l'accesso al database.</span><span class="sxs-lookup"><span data-stu-id="1aafc-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="1aafc-145">Dovrebbe trattarsi di un account utente a cui viene effettuato il provisioning specifico per questo uso.</span><span class="sxs-lookup"><span data-stu-id="1aafc-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="1aafc-146">L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="1aafc-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="1aafc-147">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="1aafc-148">Nella finestra **Configura il server di amministrazione e monitoraggio** immettere il **Binding della porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="1aafc-149">**Avviso**  Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.</span><span class="sxs-lookup"><span data-stu-id="1aafc-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="1aafc-150">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="1aafc-151">Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1aafc-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="1aafc-152">L'opzione Microsoft Updates non attiva gli aggiornamenti automatici in Windows.</span><span class="sxs-lookup"><span data-stu-id="1aafc-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="1aafc-153">Quando la configurazione guidata ha raccolto le informazioni necessarie sulle caratteristiche, l'installazione di MBAM è pronta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="1aafc-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="1aafc-154">Fare clic su **Torna** per tornare alla procedura guidata se si vogliono rivedere o modificare le impostazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="1aafc-155">Fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="1aafc-156">Fare clic su **Annulla** per uscire dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="1aafc-157">Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1aafc-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="1aafc-158">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="1aafc-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="1aafc-159">Dopo aver installato le funzionalità di MBAM server, è necessario aggiungere utenti ai ruoli di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1aafc-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="1aafc-160">Per altre informazioni, Vedi [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1aafc-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="1aafc-161">Per eseguire la configurazione post-installazione</span><span class="sxs-lookup"><span data-stu-id="1aafc-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="1aafc-162">Al termine della configurazione, è necessario aggiungere ruoli utente in modo da consentire agli utenti di accedere alle funzionalità nel sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1aafc-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="1aafc-163">Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti:</span><span class="sxs-lookup"><span data-stu-id="1aafc-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="1aafc-164">**Utenti di hardware MBAM**: i membri di questo gruppo locale possono accedere alla funzionalità hardware nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="1aafc-165">**Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le funzionalità TPM nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="1aafc-166">Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="1aafc-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="1aafc-167">**Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le funzionalità TPM nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="1aafc-168">Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità.</span><span class="sxs-lookup"><span data-stu-id="1aafc-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="1aafc-169">Per gestire gli utenti TPM, sono necessari solo il campo computer Domain e il nome computer.</span><span class="sxs-lookup"><span data-stu-id="1aafc-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="1aafc-170">Nel database di amministrazione e monitoraggio Server, conformità e controllo e nel computer che ospita i report di conformità e controllo aggiungere utenti al gruppo locale seguente per consentire loro di accedere alla funzionalità report nel sito Web di amministrazione di MBAM:</span><span class="sxs-lookup"><span data-stu-id="1aafc-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="1aafc-171">**Utenti di report mbam**: i membri di questo gruppo locale possono accedere alle funzionalità report nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="1aafc-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="1aafc-172">**Nota**  L'appartenenza a un utente o un gruppo di membri identici del gruppo di **utenti del report mbam** deve essere mantenuto in tutti i computer in cui sono installate le funzionalità di amministrazione e monitoraggio del server, il database di conformità e controllo e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="1aafc-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="1aafc-173">Per mantenere le appartenenze identiche in tutti i computer, è necessario creare un gruppo di sicurezza del dominio e aggiungere il gruppo di dominio a ogni gruppo di utenti del report MBAM locale.</span><span class="sxs-lookup"><span data-stu-id="1aafc-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="1aafc-174">Quando si esegue questa operazione, è possibile gestire le appartenenze ai gruppi usando il gruppo Domain.</span><span class="sxs-lookup"><span data-stu-id="1aafc-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="1aafc-175">Convalida dell'installazione della funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="1aafc-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="1aafc-176">Dopo aver completato l'installazione di MBAM, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM necessarie per la gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1aafc-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="1aafc-177">Usare la procedura seguente per verificare che il servizio MBAM sia funzionante:</span><span class="sxs-lookup"><span data-stu-id="1aafc-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="1aafc-178">Per convalidare l'installazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="1aafc-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="1aafc-179">In ogni server in cui è distribuita una caratteristica di MBAM aprire il **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="1aafc-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="1aafc-180">Fare clic su **programmi**e quindi su **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="1aafc-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="1aafc-181">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="1aafc-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="1aafc-182">Nota</span><span class="sxs-lookup"><span data-stu-id="1aafc-182">Note</span></span>**  
   <span data-ttu-id="1aafc-183">Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="1aafc-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="1aafc-184">Nel server in cui è installato il database di ripristino e hardware, aprire SQL Server Management Studio e verificare che il database **hardware e ripristino di mbam** sia installato.</span><span class="sxs-lookup"><span data-stu-id="1aafc-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="1aafc-185">Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database di verifica e conformità di mbam** .</span><span class="sxs-lookup"><span data-stu-id="1aafc-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="1aafc-186">Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con privilegi amministrativi e passare alla Home page del sito di SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="1aafc-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="1aafc-187">La posizione iniziale predefinita di un'istanza del sito di SQL Server Reporting Services si trova in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="1aafc-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="1aafc-188">Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1aafc-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="1aafc-189">Verificare che sia elencata una cartella denominata **report di conformità Malta** e che contenga cinque report e un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1aafc-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="1aafc-190">Nota</span><span class="sxs-lookup"><span data-stu-id="1aafc-190">Note</span></span>**  
   <span data-ttu-id="1aafc-191">Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="1aafc-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="1aafc-192">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**, selezionare **server Web (IIS)** e fare clic su **Gestione Internet Information Services (IIS)**</span><span class="sxs-lookup"><span data-stu-id="1aafc-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="1aafc-193">In **connessioni**passare a \* &lt; nomecomputer &gt; \*, selezionare **siti**e selezionare **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="1aafc-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="1aafc-194">Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.</span><span class="sxs-lookup"><span data-stu-id="1aafc-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="1aafc-195">Nel server in cui è installata la funzionalità di amministrazione e monitoraggio aprire un Web browser con privilegi amministrativi e quindi passare alle posizioni seguenti nel sito Web di MBAM per verificare che vengano caricati correttamente:</span><span class="sxs-lookup"><span data-stu-id="1aafc-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="1aafc-196">*http:// &lt; nomecomputer &gt; /default.aspx* e confermare ognuno dei collegamenti per gli spostamenti e i report</span><span class="sxs-lookup"><span data-stu-id="1aafc-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="1aafc-197">http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="1aafc-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="1aafc-198">http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="1aafc-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="1aafc-199">http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="1aafc-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="1aafc-200">Nota</span><span class="sxs-lookup"><span data-stu-id="1aafc-200">Note</span></span>**  
   <span data-ttu-id="1aafc-201">In genere, i servizi vengono installati nella porta predefinita 80 senza crittografia di rete.</span><span class="sxs-lookup"><span data-stu-id="1aafc-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="1aafc-202">Se i servizi sono installati in una porta diversa, modificare gli URL in modo da includere la porta appropriata.</span><span class="sxs-lookup"><span data-stu-id="1aafc-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="1aafc-203">Ad esempio, http://\* &lt; nomecomputer &gt; : &lt; Port &gt; \*/default.aspx o http:// <em> &lt; HostHeaderName &gt; / </em> default. aspx.</span><span class="sxs-lookup"><span data-stu-id="1aafc-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="1aafc-204">Se i servizi sono installati con la crittografia di rete, cambiare http://in https://.</span><span class="sxs-lookup"><span data-stu-id="1aafc-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="1aafc-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1aafc-205">Related topics</span></span>


[<span data-ttu-id="1aafc-206">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1aafc-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





