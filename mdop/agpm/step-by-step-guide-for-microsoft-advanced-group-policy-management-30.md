---
title: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0
description: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818326"
---
# <span data-ttu-id="ccdf2-103">Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0</span><span class="sxs-lookup"><span data-stu-id="ccdf2-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="ccdf2-104">Questa guida dettagliata illustra le tecniche avanzate per la gestione dei criteri di gruppo tramite la console Gestione criteri di gruppo e la gestione avanzata Criteri di gruppo di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="ccdf2-105">Advanced Group Policy Management aumenta le funzionalità di GPMC, fornendo:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="ccdf2-106">Ruoli standard per la delega delle autorizzazioni per la gestione degli oggetti Criteri di gruppo (GPO) in più amministratori di criteri di gruppo, nonché la possibilità di delegare l'accesso a GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="ccdf2-107">Un archivio per consentire agli amministratori dei criteri di gruppo di creare e modificare i GPO offline prima di distribuirli in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="ccdf2-108">Possibilità di ripristinare una versione precedente di un GPO nell'archivio e limitare il numero di versioni archiviate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="ccdf2-109">Funzionalità check-in/check-out per gli oggetti Criteri di gruppo per garantire che gli amministratori dei criteri di raggruppamento non sovrascrivano inavvertitamente il lavoro dell'altro.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="ccdf2-110">Panoramica degli scenari Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-110">AGPM scenario overview</span></span>


<span data-ttu-id="ccdf2-111">Per questo scenario, si utilizzerà un account utente distinto per ogni ruolo in Advanced Group Policy Management per dimostrare in che modo i criteri di gruppo possono essere gestiti in un ambiente con più amministratori di criteri di gruppo con livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="ccdf2-112">In particolare, verranno eseguite le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="ccdf2-113">L'uso di un account membro del gruppo Domain Admins consente di installare Advanced Group Policy Management e assegnare il ruolo di amministratore Advanced Group Policy Management a un account o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="ccdf2-114">Uso degli account a cui assegnare i ruoli di Advanced Group Policy Management, installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="ccdf2-115">Usando un account con il ruolo amministratore Advanced Group Policy Management, configura Advanced Group Policy Management e delega l'accesso a GPO assegnando ruoli ad altri account.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="ccdf2-116">L'uso di un account con il ruolo di Editor richiede la creazione di un oggetto Criteri di tipo, che viene quindi approvato usando un account con il ruolo di approvazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="ccdf2-117">Con l'account dell'editor, controlla l'oggetto Criteri di ricerca dall'archivio, modifica il GPO, controlla l'oggetto Criteri di ricerca nell'archivio e Richiedi la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="ccdf2-118">Usando un account con il ruolo di approvazione, esaminare l'oggetto Criteri di controllo e distribuirlo nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="ccdf2-119">Usando un account con il ruolo di editor, crea un modello di GPO e usalo come punto di partenza per creare un nuovo GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="ccdf2-120">Uso di un account con il ruolo Approvatore, eliminare e ripristinare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processo di sviluppo degli oggetti Criteri di gruppo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="ccdf2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccdf2-122">Requirements</span></span>


<span data-ttu-id="ccdf2-123">I computer in cui si vuole installare Advanced Group Policy Management devono soddisfare i requisiti seguenti ed è necessario creare account per l'uso in questo scenario.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="ccdf2-124">**Nota**  Se è installato Advanced Group Policy Management 2,5 e si esegue l'aggiornamento da Windows Server® 2003 a Windows Server2008 o WindowsVista® senza i Service Pack installati in WindowsVista con Service Pack1, è necessario aggiornare il sistema operativo prima di poter eseguire l'aggiornamento a Advanced Group Policy Management 3.0.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="ccdf2-125">Requisiti del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-125">AGPM Server requirements</span></span>

<span data-ttu-id="ccdf2-126">Advanced Group Policy Management 3.0 richiede Windows Server2008 o WindowsVista con il servizio Pack1 e la GPMC dagli strumenti di amministrazione del server remoto installati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="ccdf2-127">Sono supportate entrambe le versioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="ccdf2-128">Prima di installare Advanced Group Policy Management Server, è necessario essere un membro del gruppo Domain Admins e le caratteristiche di Windows seguenti devono essere presenti, se non diversamente specificato:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="ccdf2-129">GPMC</span><span class="sxs-lookup"><span data-stu-id="ccdf2-129">GPMC</span></span>

    -   <span data-ttu-id="ccdf2-130">Windows Server 2008: la GPMC viene installata automaticamente da Advanced Group Policy Management se non è presente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="ccdf2-131">Windows Vista: prima di installare Advanced Group Policy Management, è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ccdf2-132">Per altre informazioni, vedi <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="ccdf2-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="ccdf2-133">.NET Framework 3.5</span></span>

<span data-ttu-id="ccdf2-134">Le funzionalità di Windows seguenti sono richieste dal server Advanced Group Policy Management e verranno installate automaticamente se non presenti:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="ccdf2-135">Attivazione di WCF; Attivazione non HTTP</span><span class="sxs-lookup"><span data-stu-id="ccdf2-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="ccdf2-136">Servizio Attivazione dei processi Windows</span><span class="sxs-lookup"><span data-stu-id="ccdf2-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="ccdf2-137">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="ccdf2-137">Process Model</span></span>

    -   <span data-ttu-id="ccdf2-138">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="ccdf2-138">.NET Environment</span></span>

    -   <span data-ttu-id="ccdf2-139">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="ccdf2-139">Configuration APIs</span></span>

### <span data-ttu-id="ccdf2-140">Requisiti client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-140">AGPM Client requirements</span></span>

<span data-ttu-id="ccdf2-141">Advanced Group Policy Management 3.0 richiede Windows Server2008 o WindowsVista con Service Pack 1 e GPMC dagli strumenti di amministrazione del server remoto installati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="ccdf2-142">Sono supportate entrambe le versioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="ccdf2-143">Il client Advanced Group Policy Management può essere installato in un computer che utilizza Advanced Management Server.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="ccdf2-144">Le funzionalità di Windows seguenti sono richieste dal client Advanced Group Policy Management e verranno installate automaticamente se non presenti, se non diversamente specificato:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="ccdf2-145">GPMC</span><span class="sxs-lookup"><span data-stu-id="ccdf2-145">GPMC</span></span>

    -   <span data-ttu-id="ccdf2-146">Windows Server 2008: la GPMC viene installata automaticamente da Advanced Group Policy Management se non è presente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="ccdf2-147">Windows Vista: prima di installare Advanced Group Policy Management, è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="ccdf2-148">Per altre informazioni, vedi <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="ccdf2-149">.NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="ccdf2-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="ccdf2-150">Requisiti per lo scenario</span><span class="sxs-lookup"><span data-stu-id="ccdf2-150">Scenario requirements</span></span>

<span data-ttu-id="ccdf2-151">Prima di iniziare questo scenario, creare quattro account utente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="ccdf2-152">Durante lo scenario, verrà assegnato uno dei ruoli di Advanced Group Policy Management seguenti a ognuno di questi account: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="ccdf2-153">Questi account devono essere in grado di inviare e ricevere messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="ccdf2-154">Assegnare l'autorizzazione **collegamento GPO** agli account con l'amministratore di Advanced Group Policy Management, l'approvatore e i ruoli di editor facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="ccdf2-155">**Nota** 
 L'autorizzazione **collegamento GPO** viene assegnata ai membri di amministratori di dominio e amministratori aziendali per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="ccdf2-156">Per assegnare l'autorizzazione **collegamento GPO** ad altri utenti o gruppi, ad esempio account con il ruolo di amministratore o approvatore della gestione avanzata, fare clic sul nodo per il dominio e quindi fare clic sulla scheda **delega** , selezionare **Collega oggetti Criteri**di gruppo, fare clic su **Aggiungi**e selezionare gli utenti o i gruppi a cui assegnare l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="ccdf2-157">Procedura per l'installazione e la configurazione di Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="ccdf2-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="ccdf2-158">Per installare e configurare Advanced Group Policy Management, è necessario completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="ccdf2-159">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="ccdf2-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="ccdf2-160">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="ccdf2-161">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="ccdf2-162">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="ccdf2-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="ccdf2-163">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="ccdf2-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="ccdf2-164">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="ccdf2-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="ccdf2-165">In questo passaggio verrà installato il server Advanced Group Policy Management nel server membro o controller di dominio che eseguirà il servizio Advanced Group Policy Management e si configurerà l'archivio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="ccdf2-166">Tutte le operazioni Advanced Group Policy Management vengono gestite tramite questo servizio Windows e vengono eseguite con le credenziali del servizio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="ccdf2-167">L'archivio gestito da un server Advanced Group Policy Management può essere ospitato in tale server o in un altro server della stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="ccdf2-168">Per installare Advanced Group Policy Management Server nel computer in cui è ospitato il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="ccdf2-169">Accedere con un account membro del gruppo Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="ccdf2-170">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-server**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="ccdf2-171">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="ccdf2-172">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="ccdf2-173">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="ccdf2-174">Il computer in cui è installato il server Advanced Group Policy Management ospita il servizio Advanced Group Policy Management e gestisce l'archivio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="ccdf2-175">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-175">Click **Next**.</span></span>

6.  <span data-ttu-id="ccdf2-176">Nella finestra di dialogo **percorso di archiviazione** selezionare un percorso per l'archivio relativo al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="ccdf2-177">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma è necessario selezionare una posizione con spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="ccdf2-178">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-178">Click **Next**.</span></span>

7.  <span data-ttu-id="ccdf2-179">Nella finestra di dialogo **account del servizio Advanced Group Policy Management** selezionare un account del servizio in cui verrà eseguito il servizio Advanced Group Policy Management e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="ccdf2-180">Nella finestra di dialogo **proprietario archivio** selezionare un account o un gruppo a cui assegnare inizialmente il ruolo amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="ccdf2-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="ccdf2-181">Questo amministratore della gestione avanzata Criteri di amministrazione può assegnare i ruoli e le autorizzazioni di Advanced Group Policy ad altri amministratori di criteri di gruppo, incluso il ruolo di amministratore Advanced</span><span class="sxs-lookup"><span data-stu-id="ccdf2-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="ccdf2-182">Per questo scenario, selezionare l'account da usare nel ruolo amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="ccdf2-183">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-183">Click **Next**.</span></span>

9.  <span data-ttu-id="ccdf2-184">Nella finestra di dialogo **configurazione porta** Digitare una porta in cui deve essere ascoltato il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="ccdf2-185">Non deselezionare la casella **di controllo Aggiungi eccezione alla porta al firewall** a meno che non si configuri manualmente le eccezioni della porta o non si usi regole per configurare le eccezioni della porta.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="ccdf2-186">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-186">Click **Next**.</span></span>

10. <span data-ttu-id="ccdf2-187">Nella finestra di dialogo **lingue** selezionare una o più lingue di visualizzazione da installare per il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="ccdf2-188">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="ccdf2-189">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="ccdf2-190">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="ccdf2-191">Per informazioni su come modificare le impostazioni per il servizio, vedere la guida per la gestione avanzata dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="ccdf2-192">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="ccdf2-193">Ogni amministratore dei criteri di gruppo, tutti gli utenti che creano, modifica, distribuisce, esamina o Elimina GPO, deve avere installato client Advanced Group Policy Management in computer che usano per gestire i GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="ccdf2-194">Per questo scenario, è possibile installare il client Advanced Group Policy in almeno un computer.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="ccdf2-195">Non è necessario installare il client Advanced Group Policy Management nei computer degli utenti finali che non eseguono l'amministrazione dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="ccdf2-196">Per installare il client Advanced Group Policy Management nel computer di un amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ccdf2-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="ccdf2-197">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-client**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="ccdf2-198">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="ccdf2-199">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="ccdf2-200">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="ccdf2-201">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-201">Click **Next**.</span></span>

5.  <span data-ttu-id="ccdf2-202">Nella finestra di dialogo **server Advanced Group Policy Management** Digitare il nome completo del computer per il server Advanced Group Policy Management e la porta a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="ccdf2-203">La porta predefinita per il servizio Advanced Group Policy Management è 4600.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="ccdf2-204">Non deselezionare la casella di controllo **Consenti Microsoft Management Console tramite il firewall** a meno che tu non configuri manualmente le eccezioni della porta o usi regole per configurare le eccezioni della porta.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="ccdf2-205">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-205">Click **Next**.</span></span>

6.  <span data-ttu-id="ccdf2-206">Nella finestra di dialogo **lingue** selezionare una o più lingue di visualizzazione da installare per il client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="ccdf2-207">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="ccdf2-208">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="ccdf2-209">La Advanced Group Policy Management archivia tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato, un GPO per cui Advanced Group Policy Management fornisce il controllo delle modifiche, in un archivio centrale, quindi gli amministratori dei criteri di gruppo possono visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="ccdf2-210">In questo passaggio si configura una connessione al server Advanced Group Policy Management e si assicura che tutti gli amministratori di criteri di gruppo si connettano allo stesso server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="ccdf2-211">Per informazioni sulla configurazione di più server Advanced Group Policy Management, vedere Guida per la gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="ccdf2-212">Per configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ccdf2-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="ccdf2-213">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con l'account utente selezionato come proprietario dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="ccdf2-214">Questo utente ha il ruolo di amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="ccdf2-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="ccdf2-215">Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e **Gestione criteri di gruppo** per aprire la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="ccdf2-216">Modificare un GPO applicato a tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="ccdf2-217">Nella finestra **Editor gestione criteri di gruppo** fare doppio clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="ccdf2-218">Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="ccdf2-219">Nella finestra **Proprietà** selezionare **abilitato** e digitare il nome completo del computer e la porta, ad esempio **Server.contoso.com:4600**, per il server che ospita l'archivio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="ccdf2-220">Per impostazione predefinita, il servizio Advanced Group Policy Management usa la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="ccdf2-221">Fare clic su **OK**e quindi chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="ccdf2-222">Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management viene configurata per ogni amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ccdf2-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="ccdf2-223">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="ccdf2-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="ccdf2-224">In qualità di amministratore Advanced Group Policy Management (controllo completo), è possibile designare gli indirizzi di posta elettronica degli approvatori e degli amministratori della gestione avanzata dati a cui viene inviato un messaggio di posta elettronica contenente una richiesta quando un editor tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="ccdf2-225">Puoi anche determinare l'alias da cui vengono inviati questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="ccdf2-226">Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="ccdf2-227">Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="ccdf2-228">Nel campo **da indirizzo di posta elettronica** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="ccdf2-229">Nel campo **indirizzo di posta elettronica** Digitare l'indirizzo di posta elettronica per l'account utente a cui si vuole assegnare il ruolo di approvatore.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="ccdf2-230">Nel campo **server SMTP** Digitare un server di posta SMTP valido.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="ccdf2-231">Nei campi **nome utente** e **password** digitare le credenziali di un utente con accesso al servizio SMTP.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="ccdf2-232">Fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="ccdf2-233">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="ccdf2-233">Step 5: Delegate access</span></span>

<span data-ttu-id="ccdf2-234">In qualità di amministratore Advanced Group Policy Management (controllo completo) deleghi l'accesso a livello di dominio a GPO, assegnando ruoli all'account di ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="ccdf2-235">**Nota**  È anche possibile delegare l'accesso a livello di GPO invece che a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="ccdf2-236">Per informazioni dettagliate, vedere Guida per la gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="ccdf2-237">**Importante**  Devi limitare l'appartenenza al gruppo proprietari creatori di criteri di gruppo, in modo che non possa essere usato per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ccdf2-238">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="ccdf2-239">Per delegare l'accesso a tutti i GPO in un dominio</span><span class="sxs-lookup"><span data-stu-id="ccdf2-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="ccdf2-240">Nella scheda **delega del dominio** fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da responsabile approvazione e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="ccdf2-241">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo **approvatore** per assegnare il ruolo all'account e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="ccdf2-242">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="ccdf2-243">Fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da Editor e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="ccdf2-244">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo di **Editor** per assegnare il ruolo all'account e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="ccdf2-245">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="ccdf2-246">Fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da revisore e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="ccdf2-247">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo **revisore** per assegnare solo il ruolo all'account.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="ccdf2-248">Procedura per la gestione dei GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-248">Steps for managing GPOs</span></span>


<span data-ttu-id="ccdf2-249">È necessario completare la procedura seguente per creare, modificare, rivedere e distribuire GPO tramite Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="ccdf2-250">Verrà inoltre creato un modello, eliminato un oggetto Criteri di stato e il ripristino di un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="ccdf2-251">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="ccdf2-252">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="ccdf2-253">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="ccdf2-254">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="ccdf2-255">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="ccdf2-256">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="ccdf2-257">In un ambiente con più amministratori di criteri di gruppo, coloro che hanno il ruolo di editor possono richiedere la creazione di nuovi GPO, ma tale richiesta deve essere approvata da un utente con il ruolo di approvatore perché la creazione di un nuovo GPO ha un impatto sull'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="ccdf2-258">In questo passaggio si utilizzerà un account con il ruolo di editor per richiedere la creazione di un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="ccdf2-259">Usando un account con il ruolo di approvatore, approvare la richiesta e completare la creazione di un GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="ccdf2-260">Per richiedere la creazione di un nuovo GPO gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="ccdf2-261">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="ccdf2-262">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ccdf2-263">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="ccdf2-264">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="ccdf2-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="ccdf2-265">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="ccdf2-266">Digitare **MioGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="ccdf2-267">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="ccdf2-268">Fare clic su **Crea Live** in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="ccdf2-269">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="ccdf2-270">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-271">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="ccdf2-272">Per approvare la richiesta in sospeso per creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="ccdf2-273">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="ccdf2-274">Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con la richiesta dell'editor per creare un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="ccdf2-275">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="ccdf2-276">Nella scheda **contenuto** fare clic sulla scheda **in sospeso** per visualizzare gli oggetti Criteri di stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="ccdf2-277">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="ccdf2-278">Fare clic su **Sì** per confermare l'approvazione della creazione dell'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="ccdf2-279">Il GPO viene spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="ccdf2-280">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="ccdf2-281">Puoi usare i GPO per configurare le impostazioni di computer o utenti e distribuirle a molti computer o utenti.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="ccdf2-282">In questo passaggio si usa un account con il ruolo di editor per estrarre un oggetto Criteri di ricerca dall'archivio, modificare l'oggetto Criteri di stato offline, controllare l'oggetto Criteri di controllo modificato nell'archivio e richiedere la distribuzione del GPO all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="ccdf2-283">Per questo scenario, devi configurare un'impostazione nell'oggetto Criteri di ricerca per richiedere che la password abbia almeno otto caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="ccdf2-284">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="ccdf2-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="ccdf2-285">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ccdf2-286">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ccdf2-287">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="ccdf2-288">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="ccdf2-289">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="ccdf2-290">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-291">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="ccdf2-292">Per modificare l'oggetto Criteri di stato offline e configurare la lunghezza minima della password</span><span class="sxs-lookup"><span data-stu-id="ccdf2-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="ccdf2-293">Nella scheda **controllata** fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **modifica** per aprire la finestra **Editor gestione criteri di gruppo** e apportare modifiche a una copia offline dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="ccdf2-294">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="ccdf2-295">In **Configurazione computer**fare doppio clic su **criteri**, **impostazioni di Windows**, **impostazioni di sicurezza**, criteri **account**e **criteri password**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="ccdf2-296">Nel riquadro dei dettagli fare doppio clic su **lunghezza minima password**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="ccdf2-297">Nella finestra Proprietà selezionare la casella di controllo **Definisci l'impostazione del criterio** , impostare il numero di caratteri su **8**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="ccdf2-298">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="ccdf2-299">Per controllare l'oggetto Criteri di ricerca nell'archivio</span><span class="sxs-lookup"><span data-stu-id="ccdf2-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="ccdf2-300">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Archivia**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="ccdf2-301">Digitare un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="ccdf2-302">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-303">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="ccdf2-304">Per richiedere la distribuzione del GPO all'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="ccdf2-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="ccdf2-305">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Distribuisci**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="ccdf2-306">Poiché questo account non è un approvatore o un amministratore della Advanced Group Policy Management, è necessario inviare una richiesta di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="ccdf2-307">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="ccdf2-308">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="ccdf2-309">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-310">**MioGPO** viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="ccdf2-311">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="ccdf2-312">In questo passaggio si funge da approvatore, si creano report e si analizzano le impostazioni e le modifiche apportate alle impostazioni nell'oggetto Criteri di stato per determinare se è necessario approvarle.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="ccdf2-313">Dopo aver valutato l'oggetto Criteri di gruppo, è necessario distribuirlo nell'ambiente di produzione e collegarlo a un dominio o a un'unità organizzativa in modo che abbia effetto quando i criteri di raggruppamento vengono aggiornati per i computer di tale dominio o OU.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="ccdf2-314">Per rivedere le impostazioni nel GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="ccdf2-315">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="ccdf2-316">Qualsiasi amministratore di criteri di gruppo con il ruolo revisore, incluso in tutti gli altri ruoli, può rivedere le impostazioni di un oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="ccdf2-317">Aprire la posta in arrivo per l'account e tenere presente che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con una richiesta dell'editor per distribuire un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="ccdf2-318">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="ccdf2-319">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="ccdf2-320">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="ccdf2-321">Esaminare le impostazioni della versione più recente di MioGPO:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="ccdf2-322">Nella finestra **cronologia** fare clic con il pulsante destro del mouse sulla versione del GPO con il timestamp più recente, scegliere **Impostazioni**e quindi fare clic su **report HTML** per visualizzare un riepilogo delle impostazioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="ccdf2-323">Nel Web browser fare clic su **Mostra tutto** per visualizzare tutte le impostazioni nel GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="ccdf2-324">Chiudi il browser.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-324">Close the browser.</span></span>

7. <span data-ttu-id="ccdf2-325">Confrontare la versione più recente di MioGPO con la prima versione archiviata:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="ccdf2-326">Nella finestra **cronologia** fare clic sulla versione del GPO con l'indicatore di data e ora più recente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="ccdf2-327">Premere CTRL e fare clic sulla versione più recente del GPO per cui la **versione del computer** non è \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="ccdf2-328">Fare clic sul pulsante **differenze** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-328">Click the **Differences** button.</span></span> <span data-ttu-id="ccdf2-329">La sezione criteri **account/criteri password** è evidenziata in verde e preceduta da **\ [+ \]**, che indica che questa impostazione è configurata solo nella seconda versione dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="ccdf2-330">Fare clic su **criteri account/password**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="ccdf2-331">L'impostazione **lunghezza minima password** viene evidenziata anche in verde e preceduta da **\ [+ \]**, che indica che è configurata solo nella seconda versione del GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="ccdf2-332">Chiudere il Web browser.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-332">Close the Web browser.</span></span>

**<span data-ttu-id="ccdf2-333">Per distribuire il GPO nell'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="ccdf2-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="ccdf2-334">Nella scheda **in sospeso** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="ccdf2-335">Digitare un commento da includere nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="ccdf2-336">Fai clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-336">Click **Yes**.</span></span> <span data-ttu-id="ccdf2-337">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-338">Il GPO viene distribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="ccdf2-339">Per collegare l'oggetto Criteri di gruppo a un dominio o un'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="ccdf2-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="ccdf2-340">In GPMC fare clic con il pulsante destro del mouse sul dominio o un'unità organizzativa a cui applicare il GPO configurato e quindi scegliere **collega un oggetto Criteri**di campo esistente.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="ccdf2-341">Nella finestra di dialogo **Seleziona GPO** fare clic su **MioGPO**e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="ccdf2-342">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="ccdf2-343">In questo passaggio si usa un account con il ruolo di editor per creare un modello, una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO e quindi creare un nuovo GPO basato su tale modello.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="ccdf2-344">I modelli sono utili per creare rapidamente più oggetti Criteri di gruppo che includono molte delle stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="ccdf2-345">Per creare un modello basato su un oggetto Criteri di lavoro esistente</span><span class="sxs-lookup"><span data-stu-id="ccdf2-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="ccdf2-346">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ccdf2-347">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ccdf2-348">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="ccdf2-349">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Salva come modello** per creare un modello che incorpora tutte le impostazioni attualmente in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="ccdf2-350">Digitare **MyTemplate** come nome per il modello e un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="ccdf2-351">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-352">Il nuovo modello viene visualizzato nella scheda **modelli** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="ccdf2-353">Per richiedere la creazione di un nuovo GPO gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ccdf2-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="ccdf2-354">Fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="ccdf2-355">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="ccdf2-356">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="ccdf2-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="ccdf2-357">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="ccdf2-358">Digitare **MioaltroGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="ccdf2-359">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="ccdf2-360">Fare clic su **Crea Live**, in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="ccdf2-361">Per **da modello GPO**selezionare **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="ccdf2-362">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="ccdf2-363">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-364">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="ccdf2-365">Usare un account a cui è stato assegnato il ruolo di approvatore per approvare la richiesta in sospeso per creare il GPO come nel [passaggio 1: creare un oggetto Criteri](#bkmk-manage1)di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="ccdf2-366">MyTemplate incorpora tutte le impostazioni configurate in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="ccdf2-367">Poiché MioaltroGPO è stato creato con MyTemplate, contiene inizialmente tutte le impostazioni contenute in MioGPO nel momento in cui è stato creato MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="ccdf2-368">Puoi confermare questa operazione generando un report differenza per confrontare MioaltroGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="ccdf2-369">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="ccdf2-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="ccdf2-370">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="ccdf2-371">Fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="ccdf2-372">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="ccdf2-373">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-374">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="ccdf2-375">Per modificare l'oggetto Criteri di stato offline e configurare la durata del blocco dell'account</span><span class="sxs-lookup"><span data-stu-id="ccdf2-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="ccdf2-376">Nella scheda **controllata** fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **modifica** per aprire la finestra **Editor gestione criteri di gruppo** e apportare modifiche a una copia offline dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="ccdf2-377">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="ccdf2-378">In **Configurazione computer**fare doppio clic su **criteri**, **impostazioni di Windows**, **impostazioni di sicurezza**, criteri **account**e criteri di **blocco degli account**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="ccdf2-379">Nel riquadro dei dettagli fare doppio clic sulla **durata del blocco dell'account**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="ccdf2-380">Nella finestra Proprietà selezionare la casella di controllo **Definisci questa impostazione**, impostare la durata su **30** minuti e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="ccdf2-381">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="ccdf2-382">Selezionare MioaltroGPO nell'archivio e richiedere la distribuzione come per MioGPO nel [passaggio 2: modificare un oggetto Criteri](#bkmk-manage2)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="ccdf2-383">Puoi confrontare MioaltroGPO a MioGPO o a MyTemplate usando i report differenze.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="ccdf2-384">Tutti gli account che includono il ruolo di revisore (amministratore della gestione avanzata Criteri di amministrazione \ [controllo completo \], approvatore, editor o revisore) possono generare report.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="ccdf2-385">Per confrontare un oggetto Criteri di confronto a un altro GPO e a un modello</span><span class="sxs-lookup"><span data-stu-id="ccdf2-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="ccdf2-386">Per confrontare MioGPO e MioaltroGPO:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="ccdf2-387">Nella scheda **controllata** fare clic su **MioGPO**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="ccdf2-388">Premere CTRL e quindi fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="ccdf2-389">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e fare clic su **report HTML**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="ccdf2-390">Per confrontare MioaltroGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="ccdf2-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="ccdf2-391">Nella scheda **controllata** fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="ccdf2-392">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e fare clic su **modello**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="ccdf2-393">Selezionare **MyTemplate** e **report HTML**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="ccdf2-394">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="ccdf2-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="ccdf2-395">In questo passaggio si funge da approvatore per eliminare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="ccdf2-396">Per eliminare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="ccdf2-397">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="ccdf2-398">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="ccdf2-399">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="ccdf2-400">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="ccdf2-401">Fare clic su **Elimina GPO da archiviazione e produzione** per eliminare sia la versione nell'archivio che la versione distribuita del GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="ccdf2-402">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="ccdf2-403">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-404">Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="ccdf2-405">Occasionalmente potresti scoprire dopo l'eliminazione di un GPO che è ancora necessario.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="ccdf2-406">In questo passaggio si funge da approvatore per ripristinare un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="ccdf2-407">Per ripristinare un oggetto Criteri di stato eliminato</span><span class="sxs-lookup"><span data-stu-id="ccdf2-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="ccdf2-408">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare i GPO eliminati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="ccdf2-409">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="ccdf2-410">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="ccdf2-411">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-412">L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .</span><span class="sxs-lookup"><span data-stu-id="ccdf2-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="ccdf2-413">**Nota**  Il ripristino di un GPO nell'archivio non viene automaticamente ridistribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="ccdf2-414">Per restituire il GPO all'ambiente di produzione, distribuire il GPO come nel [passaggio 3: rivedere e distribuire un oggetto Criteri di controllo](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="ccdf2-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="ccdf2-415">Dopo la modifica e la distribuzione di un oggetto Criteri di ricerca, potresti scoprire che le recenti modifiche apportate al GPO causano un problema.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="ccdf2-416">In questo passaggio si funge da approvatore per eseguire il rollback a una versione precedente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="ccdf2-417">È possibile eseguire il rollback a qualsiasi versione nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="ccdf2-418">È possibile usare i commenti e le etichette per identificare le versioni valide note e quando sono state apportate modifiche specifiche.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="ccdf2-419">Per eseguire il rollback a una versione precedente di un oggetto Criteri di controllo</span><span class="sxs-lookup"><span data-stu-id="ccdf2-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="ccdf2-420">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="ccdf2-421">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="ccdf2-422">Fare clic con il pulsante destro del mouse sulla versione da distribuire, scegliere **Distribuisci**e quindi fare clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="ccdf2-423">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ccdf2-424">Nella finestra **cronologia** fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="ccdf2-425">**Nota**  Per verificare che la versione ridistribuita sia la versione progettata, esaminare un report di differenza per le due versioni.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="ccdf2-426">Nella finestra **cronologia** del GPO selezionare le due versioni, fare clic con il pulsante destro del mouse su di esse, scegliere **differenza**e quindi fare clic su **report HTML** o **report XML**.</span><span class="sxs-lookup"><span data-stu-id="ccdf2-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





