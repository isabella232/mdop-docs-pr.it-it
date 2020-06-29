---
title: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 2.5
description: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820195"
---
# <span data-ttu-id="8298c-103">Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 2.5</span><span class="sxs-lookup"><span data-stu-id="8298c-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="8298c-104">Questa guida dettagliata illustra le tecniche avanzate per la gestione dei criteri di gruppo tramite la console Gestione criteri di gruppo e la gestione avanzata Criteri di gruppo di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8298c-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="8298c-105">Advanced Group Policy Management aumenta le funzionalità di GPMC, fornendo:</span><span class="sxs-lookup"><span data-stu-id="8298c-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="8298c-106">Ruoli standard per la delega delle autorizzazioni per la gestione degli oggetti Criteri di gruppo (GPO) in più amministratori di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="8298c-107">Un archivio per consentire agli amministratori dei criteri di gruppo di creare e modificare i GPO offline prima di distribuirli in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="8298c-108">Possibilità di eseguire il rollback a qualsiasi versione precedente di un oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="8298c-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="8298c-109">Funzionalità check-in/check-out per gli oggetti Criteri di gruppo per garantire che gli amministratori dei criteri di raggruppamento non sovrascrivano inavvertitamente il lavoro dell'altro.</span><span class="sxs-lookup"><span data-stu-id="8298c-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="8298c-110">Panoramica degli scenari Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-110">AGPM scenario overview</span></span>


<span data-ttu-id="8298c-111">Per questo scenario, si utilizzerà un account utente distinto per ogni ruolo in Advanced Group Policy Management per dimostrare in che modo i criteri di gruppo possono essere gestiti in un ambiente con più amministratori di criteri di gruppo con livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="8298c-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="8298c-112">In particolare, verranno eseguite le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="8298c-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="8298c-113">L'uso di un account membro del gruppo Domain Admins consente di installare Advanced Group Policy Management e assegnare il ruolo di amministratore Advanced Group Policy Management a un account o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="8298c-114">Uso degli account a cui assegnare i ruoli di Advanced Group Policy Management, installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="8298c-115">Usando un account con il ruolo amministratore Advanced Group Policy Management, configura Advanced Group Policy Management e delega l'accesso a GPO assegnando ruoli ad altri account.</span><span class="sxs-lookup"><span data-stu-id="8298c-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="8298c-116">L'uso di un account con il ruolo di Editor richiede la creazione di un oggetto Criteri di tipo, che viene quindi approvato usando un account con il ruolo di approvazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="8298c-117">Con l'account dell'editor, controlla l'oggetto Criteri di ricerca dall'archivio, modifica il GPO, controlla l'oggetto Criteri di ricerca nell'archivio e Richiedi la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="8298c-118">Usando un account con il ruolo di approvazione, esaminare l'oggetto Criteri di controllo e distribuirlo nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="8298c-119">Usando un account con il ruolo di editor, crea un modello di GPO e usalo come punto di partenza per creare un nuovo GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="8298c-120">Uso di un account con il ruolo Approvatore, eliminare e ripristinare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processo di sviluppo degli oggetti Criteri di gruppo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="8298c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8298c-122">Requirements</span></span>


<span data-ttu-id="8298c-123">I computer in cui si vuole installare Advanced Group Policy Management devono soddisfare i requisiti seguenti ed è necessario creare account per l'uso in questo scenario.</span><span class="sxs-lookup"><span data-stu-id="8298c-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="8298c-124">Requisiti del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-124">AGPM Server requirements</span></span>

<span data-ttu-id="8298c-125">Advanced Group Policy Management Server 2.5 richiede WindowsVista® (versione a 32 bit) senza i Service Pack installati o Windows Server® 2003 (versione a 32 bit), nonché la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="8298c-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="8298c-126">È inoltre necessario essere un membro del gruppo Domain Admins per installare Advanced Group Policy Management Server.</span><span class="sxs-lookup"><span data-stu-id="8298c-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="8298c-127">È consigliabile installare Advanced Group Policy Management Server in un server membro o controller di dominio con la versione più recente di GPMC disponibile e supportata da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="8298c-128">Advanced Group Policy Management usa la GPMC per eseguire il backup e il ripristino degli oggetti Criteri di stato e le versioni più recenti di GPMC includono ulteriori impostazioni dei criteri non disponibili nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="8298c-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="8298c-129">Se la versione di GPMC nel server Advanced Group Policy Management è precedente alla versione nei computer usati dagli amministratori per gestire i criteri di gruppo, il server Advanced Group Policy Management non sarà in grado di archiviare le impostazioni dei criteri non disponibili nella versione precedente di GPMC.</span><span class="sxs-lookup"><span data-stu-id="8298c-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="8298c-130">In particolare, se il server Advanced Group Policy Management esegue Windows Server2003 e la versione di GPMC che lo ha accompagnato e i computer degli amministratori dei criteri di gruppo eseguono WindowsVista e la versione di GPMC che l'ha accompagnata, è comunque possibile gestire la maggior parte delle impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8298c-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="8298c-131">Tuttavia, le impostazioni dei criteri della GPMC in Windows Vista che non sono disponibili in GPMC in Windows Server 2003, ad esempio quelle correlate al reindirizzamento delle cartelle, alla rete wireless (IEEE 802,11) e alle stampanti distribuite, non possono essere archiviate dal server Advanced Group Policy Management, anche se gli amministratori possono configurarli usando Advanced Group Policy Management nei propri computer.</span><span class="sxs-lookup"><span data-stu-id="8298c-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="8298c-132">Se è necessario installare Advanced Group Policy Management in un computer con una versione precedente di GPMC che gli amministratori dei criteri di gruppo sono in esecuzione, vedere il riferimento alle impostazioni dei criteri di gruppo per informazioni dettagliate sulle impostazioni dei criteri disponibili con i sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="8298c-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="8298c-133">Per scaricare il riferimento alle impostazioni dei criteri di gruppo, vedere <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="8298c-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="8298c-134">**Nota**  Non è possibile eseguire la migrazione degli archivi da un server Advanced Group Policy Management o da un server GPOVault con Windows Server2003 a un server Advanced Group Policy che esegue WindowsVista.</span><span class="sxs-lookup"><span data-stu-id="8298c-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="8298c-135">Per Windows Server2003, se il server GPOVault è installato nel computer in cui si vuole installare Advanced Group Policy Management, è consigliabile non disinstallare il server GPOVault prima di iniziare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="8298c-136">L'installazione di Advanced Group Policy Management consente di disinstallare GPOVault server e trasferire automaticamente i dati di archivio di GPOVault esistenti in un archivio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="8298c-137">Requisiti client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-137">AGPM Client requirements</span></span>

<span data-ttu-id="8298c-138">Advanced Group Policy Management Client 2.5 richiede WindowsVista (versione a 32 bit) senza i Service Pack installati o Windows Server2003 (versione a 32 bit), nonché la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="8298c-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="8298c-139">Il client Advanced Group Policy Management può essere installato in un computer che utilizza Advanced Management Server.</span><span class="sxs-lookup"><span data-stu-id="8298c-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="8298c-140">Requisiti per lo scenario</span><span class="sxs-lookup"><span data-stu-id="8298c-140">Scenario requirements</span></span>

<span data-ttu-id="8298c-141">Prima di iniziare questo scenario, creare quattro account utente.</span><span class="sxs-lookup"><span data-stu-id="8298c-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="8298c-142">Durante lo scenario, verrà assegnato uno dei ruoli di Advanced Group Policy Management seguenti a ognuno di questi account: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore.</span><span class="sxs-lookup"><span data-stu-id="8298c-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="8298c-143">Questi account devono essere in grado di inviare e ricevere messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="8298c-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="8298c-144">Assegnare l'autorizzazione **collegamento GPO** agli account con l'amministratore di Advanced Group Policy Management, l'approvatore e i ruoli di editor facoltativi.</span><span class="sxs-lookup"><span data-stu-id="8298c-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="8298c-145">**Nota** 
 L'autorizzazione **collegamento GPO** viene assegnata ai membri di amministratori di dominio e amministratori aziendali per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8298c-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="8298c-146">Per assegnare l'autorizzazione **collegamento GPO** ad altri utenti o gruppi, ad esempio account con il ruolo di amministratore o approvatore della gestione avanzata, fare clic sul nodo per il dominio e quindi fare clic sulla scheda **delega** , selezionare **Collega oggetti Criteri**di gruppo, fare clic su **Aggiungi**e selezionare gli utenti o i gruppi a cui assegnare l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="8298c-147">Per questo scenario, è possibile eseguire azioni con account diversi.</span><span class="sxs-lookup"><span data-stu-id="8298c-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="8298c-148">È possibile accedere con ogni account come indicato oppure usare il comando **Esegui come** per avviare la GPMC con l'account indicato.</span><span class="sxs-lookup"><span data-stu-id="8298c-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="8298c-149">**Nota**  Per usare il comando **Esegui come** con GPMC in Windows Server2003, fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**, fare clic con il pulsante destro del mouse su **Gestione criteri di gruppo**e scegliere Esegui con **nome**.</span><span class="sxs-lookup"><span data-stu-id="8298c-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="8298c-150">Fare clic **sull'utente seguente** e immettere le credenziali per un account.</span><span class="sxs-lookup"><span data-stu-id="8298c-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="8298c-151">Per usare il comando **Esegui come** con GPMC in Windows Vista, fare clic sul pulsante **Start** , scegliere **Esegui**e digitare **runas/user:** <em> nel NomeDominio omeutente </em> **"mmc%windir%\\system32\\gpmc.msc"** e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="8298c-152">Quando richiesto, digitare la password per l'account.</span><span class="sxs-lookup"><span data-stu-id="8298c-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="8298c-153">Procedura per l'installazione e la configurazione di Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="8298c-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="8298c-154">Per installare e configurare Advanced Group Policy Management, è necessario completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="8298c-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="8298c-155">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="8298c-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="8298c-156">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="8298c-157">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="8298c-158">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="8298c-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="8298c-159">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="8298c-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="8298c-160">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="8298c-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="8298c-161">In questo passaggio verrà installato il server Advanced Group Policy Management nel server membro o controller di dominio che eseguirà il servizio Advanced Group Policy Management e si configurerà l'archivio.</span><span class="sxs-lookup"><span data-stu-id="8298c-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="8298c-162">Tutte le operazioni Advanced Group Policy Management vengono gestite tramite questo servizio Windows e vengono eseguite con le credenziali del servizio.</span><span class="sxs-lookup"><span data-stu-id="8298c-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="8298c-163">L'archivio gestito da un server Advanced Group Policy Management può essere ospitato in tale server o in un altro server della stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="8298c-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="8298c-164">Per installare Advanced Group Policy Management Server nel computer in cui è ospitato il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="8298c-165">Accedere con un account membro del gruppo Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="8298c-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="8298c-166">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-server**.</span><span class="sxs-lookup"><span data-stu-id="8298c-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="8298c-167">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="8298c-168">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="8298c-169">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="8298c-170">Il computer in cui è installato il server Advanced Group Policy Management ospita il servizio Advanced Group Policy Management e gestisce l'archivio.</span><span class="sxs-lookup"><span data-stu-id="8298c-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="8298c-171">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-171">Click **Next**.</span></span>

6.  <span data-ttu-id="8298c-172">Nella finestra di dialogo **percorso di archiviazione** selezionare un percorso per l'archivio relativo al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="8298c-173">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma è necessario selezionare una posizione con spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="8298c-174">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-174">Click **Next**.</span></span>

7.  <span data-ttu-id="8298c-175">Nella finestra di dialogo **account del servizio Advanced Group Policy Management** selezionare un account del servizio in cui verrà eseguito il servizio Advanced Group Policy Management e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="8298c-176">Nella finestra di dialogo **proprietario archivio** selezionare un account o un gruppo a cui assegnare inizialmente il ruolo amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="8298c-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="8298c-177">Questo amministratore della gestione avanzata Criteri di amministrazione può assegnare i ruoli e le autorizzazioni di Advanced Group Policy ad altri amministratori di criteri di gruppo, incluso il ruolo di amministratore Advanced</span><span class="sxs-lookup"><span data-stu-id="8298c-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="8298c-178">Per questo scenario, selezionare l'account da usare nel ruolo amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="8298c-179">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-179">Click **Next**.</span></span>

9.  <span data-ttu-id="8298c-180">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="8298c-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="8298c-181">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8298c-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="8298c-182">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="8298c-183">Per informazioni su come modificare le impostazioni per il servizio, vedere la guida per la gestione avanzata dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="8298c-184">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="8298c-185">Ogni amministratore dei criteri di gruppo, tutti gli utenti che creano, modifica, distribuisce, esamina o Elimina GPO, deve avere installato client Advanced Group Policy Management in computer che usano per gestire i GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="8298c-186">Per questo scenario, è possibile installare il client Advanced Group Policy in almeno un computer.</span><span class="sxs-lookup"><span data-stu-id="8298c-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="8298c-187">Non è necessario installare il client Advanced Group Policy Management nei computer degli utenti finali che non eseguono l'amministrazione dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="8298c-188">Per installare il client Advanced Group Policy Management nel computer di un amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8298c-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="8298c-189">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-client**.</span><span class="sxs-lookup"><span data-stu-id="8298c-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="8298c-190">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="8298c-191">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="8298c-192">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="8298c-193">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-193">Click **Next**.</span></span>

5.  <span data-ttu-id="8298c-194">Nella finestra di dialogo **server Advanced Group Policy Management** Digitare il nome completo del computer e la porta per il server Advanced Group Policy Management a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="8298c-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="8298c-195">La porta predefinita per il servizio Advanced Group Policy Management è 4600.</span><span class="sxs-lookup"><span data-stu-id="8298c-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="8298c-196">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8298c-196">Click **Next**.</span></span>

6.  <span data-ttu-id="8298c-197">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="8298c-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="8298c-198">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="8298c-199">La Advanced Group Policy Management archivia tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato, un GPO per cui Advanced Group Policy Management fornisce il controllo delle modifiche, in un archivio centrale, quindi gli amministratori dei criteri di gruppo possono visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="8298c-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="8298c-200">In questo passaggio si configura una connessione al server Advanced Group Policy Management e si assicura che tutti gli amministratori di criteri di gruppo si connettano allo stesso server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="8298c-201">Per informazioni sulla configurazione di più server Advanced Group Policy Management, vedere Guida per la gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="8298c-202">Per configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8298c-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="8298c-203">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con l'account utente selezionato come proprietario dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="8298c-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="8298c-204">Questo utente ha il ruolo di amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="8298c-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="8298c-205">Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e **Gestione criteri di gruppo** per aprire la **console Gestione criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="8298c-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="8298c-206">Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="8298c-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="8298c-207">Nella finestra **Editor oggetti Criteri di gruppo** fare clic **su configurazione utente**, **modelli amministrativi**e **componenti di Windows**.</span><span class="sxs-lookup"><span data-stu-id="8298c-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="8298c-208">Se **Advanced Group Policy Management** non è elencato in **componenti di Windows**:</span><span class="sxs-lookup"><span data-stu-id="8298c-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="8298c-209">Fare clic con il pulsante destro del mouse su **modelli amministrativi** e scegliere **Aggiungi/Rimuovi modelli**.</span><span class="sxs-lookup"><span data-stu-id="8298c-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="8298c-210">Fare clic su **Aggiungi**, selezionare **Advanced Group Policy Management. admx** o **Advanced Group Policy Management. adm**, fare clic su **Apri**e quindi su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="8298c-211">In **componenti di Windows**fare doppio clic su **Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="8298c-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="8298c-212">Nel riquadro dei dettagli fare doppio clic su **server Advanced Group Policy Management (tutti i domini)**.</span><span class="sxs-lookup"><span data-stu-id="8298c-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="8298c-213">Nella finestra delle **proprietà del server Advanced Group Policy Management (tutti i domini)** selezionare **abilitato** e digitare il nome completo del computer e la porta, ad esempio server.contoso.com:4600, per il server che ospita l'archivio.</span><span class="sxs-lookup"><span data-stu-id="8298c-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="8298c-214">La porta utilizzata dal servizio Advanced Group Policy Management è la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="8298c-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="8298c-215">Fare clic su **OK**e quindi chiudere la finestra **Editor oggetti Criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="8298c-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="8298c-216">Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management viene configurata per ogni amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8298c-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="8298c-217">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="8298c-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="8298c-218">In qualità di amministratore Advanced Group Policy Management (controllo completo), è possibile designare gli indirizzi di posta elettronica degli approvatori e degli amministratori della gestione avanzata dati a cui viene inviato un messaggio di posta elettronica contenente una richiesta quando un editor tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="8298c-219">Puoi anche determinare l'alias da cui vengono inviati questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="8298c-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="8298c-220">Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="8298c-221">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8298c-222">Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="8298c-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="8298c-223">Nel campo **da** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="8298c-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="8298c-224">Nel campo **a** Digitare l'indirizzo di posta elettronica per l'account utente a cui si vuole assegnare il ruolo di approvatore.</span><span class="sxs-lookup"><span data-stu-id="8298c-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="8298c-225">Nel campo **server SMTP** Digitare un server di posta SMTP valido.</span><span class="sxs-lookup"><span data-stu-id="8298c-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="8298c-226">Nei campi **nome utente** e **password** digitare le credenziali di un utente con accesso al servizio SMTP.</span><span class="sxs-lookup"><span data-stu-id="8298c-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="8298c-227">Fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="8298c-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="8298c-228">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="8298c-228">Step 5: Delegate access</span></span>

<span data-ttu-id="8298c-229">In qualità di amministratore Advanced Group Policy Management (controllo completo) deleghi l'accesso a livello di dominio a GPO, assegnando ruoli all'account di ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="8298c-230">**Nota**  È anche possibile delegare l'accesso a livello di GPO invece che a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="8298c-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="8298c-231">Per informazioni dettagliate, vedere Guida per la gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="8298c-232">**Importante**  Devi limitare l'appartenenza al gruppo proprietari creatori di criteri di gruppo, in modo che non possa essere usato per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8298c-233">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="8298c-234">Per delegare l'accesso a tutti i GPO in un dominio</span><span class="sxs-lookup"><span data-stu-id="8298c-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="8298c-235">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8298c-236">Nella scheda **delega del dominio** fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="8298c-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="8298c-237">Nella finestra di dialogo **autorizzazioni** :</span><span class="sxs-lookup"><span data-stu-id="8298c-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="8298c-238">Fare clic sull'account utente di un amministratore di criteri di gruppo e quindi selezionare la casella di controllo **approvatore** per assegnare il ruolo all'account.</span><span class="sxs-lookup"><span data-stu-id="8298c-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="8298c-239">Deselezionare la casella di controllo **Editor** .</span><span class="sxs-lookup"><span data-stu-id="8298c-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="8298c-240">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="8298c-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="8298c-241">Fare clic sull'account utente di un altro amministratore di criteri di gruppo e quindi selezionare la casella di controllo **Editor** per assegnare il ruolo all'account.</span><span class="sxs-lookup"><span data-stu-id="8298c-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="8298c-242">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="8298c-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="8298c-243">Fare clic su un terzo account e quindi selezionare la casella di controllo **revisore** per assegnare solo il ruolo di revisore all'account di tale amministratore dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="8298c-244">Deselezionare la casella di controllo **Editor** .</span><span class="sxs-lookup"><span data-stu-id="8298c-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="8298c-245">Fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="8298c-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="8298c-246">Nella finestra di dialogo **impostazioni di sicurezza avanzate** :</span><span class="sxs-lookup"><span data-stu-id="8298c-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="8298c-247">Selezionare un amministratore di criteri di gruppo e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="8298c-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="8298c-248">In **applica**a selezionare **questo oggetto e gli oggetti annidati**e quindi fare clic su **OK** nella finestra di dialogo **immissione** delle **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="8298c-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="8298c-249">Ripetere l'impostazione per ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="8298c-250">Nella finestra di dialogo **impostazioni di sicurezza avanzate** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="8298c-251">Nella finestra di dialogo **autorizzazioni** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="8298c-252">Procedura per la gestione dei GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-252">Steps for managing GPOs</span></span>


<span data-ttu-id="8298c-253">È necessario completare la procedura seguente per creare, modificare, rivedere e distribuire GPO tramite Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="8298c-254">Verrà inoltre creato un modello, eliminato un oggetto Criteri di stato e il ripristino di un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="8298c-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="8298c-255">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="8298c-256">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="8298c-257">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="8298c-258">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="8298c-259">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="8298c-260">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="8298c-261">In un ambiente con più amministratori di criteri di gruppo, coloro che hanno il ruolo di editor possono richiedere la creazione di nuovi GPO, ma tale richiesta deve essere approvata da un utente con il ruolo di approvatore perché la creazione di un nuovo GPO ha un impatto sull'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="8298c-262">In questo passaggio si utilizzerà un account con il ruolo di editor per richiedere la creazione di un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="8298c-263">Usando un account con il ruolo di approvatore, approvare la richiesta e completare la creazione di un GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="8298c-264">Per richiedere la creazione di un nuovo GPO gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="8298c-265">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="8298c-266">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8298c-267">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="8298c-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="8298c-268">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="8298c-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="8298c-269">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="8298c-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="8298c-270">Digitare **MioGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="8298c-271">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8298c-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="8298c-272">Fare clic su **Crea Live** in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="8298c-273">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="8298c-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="8298c-274">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-275">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="8298c-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="8298c-276">Per approvare la richiesta in sospeso per creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="8298c-277">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="8298c-278">Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con la richiesta dell'editor per creare un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8298c-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="8298c-279">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="8298c-280">Nella scheda **contenuto** fare clic sulla scheda **in sospeso** per visualizzare gli oggetti Criteri di stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8298c-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="8298c-281">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="8298c-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="8298c-282">Fare clic su **Sì** per confermare l'approvazione della creazione dell'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="8298c-283">Il GPO viene spostato nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="8298c-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="8298c-284">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="8298c-285">Puoi usare i GPO per configurare le impostazioni di computer o utenti e distribuirle a molti computer o utenti.</span><span class="sxs-lookup"><span data-stu-id="8298c-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="8298c-286">In questo passaggio si usa un account con il ruolo di editor per estrarre un oggetto Criteri di ricerca dall'archivio, modificare l'oggetto Criteri di stato offline, controllare l'oggetto Criteri di controllo modificato nell'archivio e richiedere la distribuzione del GPO all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="8298c-287">Per questo scenario, devi configurare un'impostazione nell'oggetto Criteri di ricerca per richiedere che la password abbia almeno otto caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="8298c-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="8298c-288">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="8298c-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="8298c-289">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8298c-290">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8298c-291">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="8298c-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="8298c-292">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="8298c-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="8298c-293">Digitare un commento da visualizzare nella **cronologia** del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="8298c-294">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-295">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="8298c-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="8298c-296">Per modificare l'oggetto Criteri di stato offline e configurare la lunghezza minima della password</span><span class="sxs-lookup"><span data-stu-id="8298c-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="8298c-297">Nella scheda **controllo** , fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **modifica** per aprire la finestra **Editor oggetti Criteri di gruppo** e apportare modifiche a una copia offline dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8298c-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="8298c-298">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="8298c-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="8298c-299">In **Configurazione computer**fare doppio clic su **impostazioni di Windows**, fare doppio clic su **impostazioni di sicurezza**, fare doppio clic su criteri **account**e quindi fare doppio clic su **criteri password**.</span><span class="sxs-lookup"><span data-stu-id="8298c-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="8298c-300">Nel riquadro dei dettagli fare doppio clic su **lunghezza minima password**.</span><span class="sxs-lookup"><span data-stu-id="8298c-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="8298c-301">Nella finestra Proprietà selezionare la casella di controllo **Definisci l'impostazione del criterio** , impostare il numero di caratteri su **8**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="8298c-302">Chiudere la finestra **Editor oggetti Criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="8298c-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="8298c-303">Per controllare l'oggetto Criteri di ricerca nell'archivio</span><span class="sxs-lookup"><span data-stu-id="8298c-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="8298c-304">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Archivia**.</span><span class="sxs-lookup"><span data-stu-id="8298c-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="8298c-305">Digitare un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="8298c-306">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-307">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.</span><span class="sxs-lookup"><span data-stu-id="8298c-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="8298c-308">Per richiedere la distribuzione del GPO all'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="8298c-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="8298c-309">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Distribuisci**.</span><span class="sxs-lookup"><span data-stu-id="8298c-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="8298c-310">Poiché questo account non è un approvatore o un amministratore della Advanced Group Policy Management, è necessario inviare una richiesta di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="8298c-311">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="8298c-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="8298c-312">Digitare un commento da visualizzare nella **cronologia** del GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="8298c-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="8298c-313">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-314">**MioGPO** viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="8298c-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="8298c-315">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="8298c-316">In questo passaggio si funge da approvatore, si creano report e si analizzano le impostazioni e le modifiche apportate alle impostazioni nell'oggetto Criteri di stato per determinare se è necessario approvarle.</span><span class="sxs-lookup"><span data-stu-id="8298c-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="8298c-317">Dopo aver valutato l'oggetto Criteri di gruppo, è necessario distribuirlo nell'ambiente di produzione e collegarlo a un dominio o a un'unità organizzativa in modo che abbia effetto quando i criteri di raggruppamento vengono aggiornati per i computer di tale dominio o OU.</span><span class="sxs-lookup"><span data-stu-id="8298c-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="8298c-318">Per rivedere le impostazioni nel GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="8298c-319">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="8298c-320">Qualsiasi amministratore di criteri di gruppo con il ruolo revisore, incluso in tutti gli altri ruoli, può rivedere le impostazioni di un oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="8298c-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="8298c-321">Aprire la posta in arrivo per l'account e tenere presente che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con una richiesta dell'editor per distribuire un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8298c-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="8298c-322">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="8298c-323">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="8298c-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="8298c-324">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="8298c-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="8298c-325">Esaminare le impostazioni della versione più recente di MioGPO:</span><span class="sxs-lookup"><span data-stu-id="8298c-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="8298c-326">Nella finestra **cronologia** fare clic con il pulsante destro del mouse sulla versione del GPO con il timestamp più recente, scegliere **Impostazioni**e quindi fare clic su **report HTML** per visualizzare un riepilogo delle impostazioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="8298c-327">Nel Web browser fare clic su **Mostra tutto** per visualizzare tutte le impostazioni nel GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="8298c-328">Chiudi il browser.</span><span class="sxs-lookup"><span data-stu-id="8298c-328">Close the browser.</span></span>

7.  <span data-ttu-id="8298c-329">Confrontare la versione più recente di MioGPO con la prima versione archiviata:</span><span class="sxs-lookup"><span data-stu-id="8298c-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="8298c-330">Nella finestra **cronologia** fare clic sulla versione del GPO con il timestamp più recente.</span><span class="sxs-lookup"><span data-stu-id="8298c-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="8298c-331">Premere **CTRL** e fare clic sulla versione più recente del GPO con uno stato di **check-in**.</span><span class="sxs-lookup"><span data-stu-id="8298c-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="8298c-332">Fare clic sul pulsante **differenze** .</span><span class="sxs-lookup"><span data-stu-id="8298c-332">Click the **Differences** button.</span></span> <span data-ttu-id="8298c-333">La sezione criteri **account/criteri password** è evidenziata in verde e preceduta da **\ [+ \]**, che indica che questa impostazione è configurata solo nella seconda versione dell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8298c-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="8298c-334">Fare clic su **criteri account/password**.</span><span class="sxs-lookup"><span data-stu-id="8298c-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="8298c-335">L'impostazione **lunghezza minima password** viene evidenziata anche in verde e preceduta da **\ [+ \]**, che indica che è configurata solo nella seconda versione del GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="8298c-336">Chiudere il Web browser.</span><span class="sxs-lookup"><span data-stu-id="8298c-336">Close the Web browser.</span></span>

**<span data-ttu-id="8298c-337">Per distribuire il GPO nell'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="8298c-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="8298c-338">Nella scheda **in sospeso** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="8298c-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="8298c-339">Digitare un commento da includere nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="8298c-340">Fai clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="8298c-340">Click **Yes**.</span></span> <span data-ttu-id="8298c-341">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-342">Il GPO viene distribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="8298c-343">Per collegare l'oggetto Criteri di gruppo a un dominio o un'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="8298c-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="8298c-344">In GPMC fare clic con il pulsante destro del mouse sul dominio o un'unità organizzativa a cui applicare il GPO configurato e quindi scegliere **collega un oggetto Criteri**di campo esistente.</span><span class="sxs-lookup"><span data-stu-id="8298c-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="8298c-345">Nella finestra di dialogo **Seleziona GPO** fare clic su **MioGPO**e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="8298c-346">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="8298c-347">In questo passaggio si usa un account con il ruolo di editor per creare un modello, una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO e quindi creare un nuovo GPO basato su tale modello.</span><span class="sxs-lookup"><span data-stu-id="8298c-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="8298c-348">I modelli sono utili per creare rapidamente più oggetti Criteri di gruppo che includono molte delle stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="8298c-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="8298c-349">Per creare un modello basato su un oggetto Criteri di lavoro esistente</span><span class="sxs-lookup"><span data-stu-id="8298c-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="8298c-350">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8298c-351">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8298c-352">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="8298c-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="8298c-353">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Salva come modello** per creare un modello che incorpora tutte le impostazioni attualmente in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="8298c-354">Digitare **MyTemplate** come nome per il modello e un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="8298c-355">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-356">Il nuovo modello viene visualizzato nella scheda **modelli** .</span><span class="sxs-lookup"><span data-stu-id="8298c-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="8298c-357">Per richiedere la creazione di un nuovo GPO gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8298c-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="8298c-358">Fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="8298c-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="8298c-359">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="8298c-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="8298c-360">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="8298c-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="8298c-361">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="8298c-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="8298c-362">Digitare **MioaltroGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="8298c-363">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8298c-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="8298c-364">Fare clic su **Crea Live**, in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="8298c-365">Per **da modello GPO**selezionare **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="8298c-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="8298c-366">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="8298c-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="8298c-367">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-368">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="8298c-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="8298c-369">Usare un account a cui è stato assegnato il ruolo di approvatore per approvare la richiesta in sospeso per creare il GPO come nel [passaggio 1: creare un oggetto Criteri](#bkmk-manage1)di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="8298c-370">MyTemplate incorpora tutte le impostazioni configurate in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="8298c-371">Poiché MioaltroGPO è stato creato con MyTemplate, contiene inizialmente tutte le impostazioni contenute in MioGPO nel momento in cui è stato creato MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="8298c-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="8298c-372">Puoi confermare questa operazione generando un report differenza per confrontare MioaltroGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="8298c-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="8298c-373">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="8298c-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="8298c-374">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8298c-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="8298c-375">Fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="8298c-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="8298c-376">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="8298c-377">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-378">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="8298c-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="8298c-379">Per modificare l'oggetto Criteri di stato offline e configurare la durata del blocco dell'account</span><span class="sxs-lookup"><span data-stu-id="8298c-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="8298c-380">Nella scheda **controllo** , fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **modifica** per aprire la finestra **Editor oggetti Criteri di gruppo** e apportare modifiche a una copia offline dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8298c-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="8298c-381">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="8298c-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="8298c-382">In **Configurazione computer**fare doppio clic su **impostazioni di Windows**, fare doppio clic su **impostazioni di sicurezza**, fare doppio clic su criteri **account**e quindi fare doppio clic su **criteri di blocco account**.</span><span class="sxs-lookup"><span data-stu-id="8298c-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="8298c-383">Nel riquadro dei dettagli fare doppio clic sulla **durata del blocco dell'account**.</span><span class="sxs-lookup"><span data-stu-id="8298c-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="8298c-384">Nella finestra Proprietà selezionare la casella di controllo **Definisci questa impostazione**, impostare la durata su **30** minuti e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="8298c-385">Chiudere la finestra **Editor oggetti Criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="8298c-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="8298c-386">Selezionare MioaltroGPO nell'archivio e richiedere la distribuzione come per MioGPO nel [passaggio 2: modificare un oggetto Criteri](#bkmk-manage2)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8298c-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="8298c-387">Puoi confrontare MioaltroGPO a MioGPO o a MyTemplate usando i report differenze.</span><span class="sxs-lookup"><span data-stu-id="8298c-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="8298c-388">Tutti gli account che includono il ruolo di revisore (amministratore della gestione avanzata Criteri di amministrazione \ [controllo completo \], approvatore, editor o revisore) possono generare report.</span><span class="sxs-lookup"><span data-stu-id="8298c-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="8298c-389">Per confrontare un oggetto Criteri di confronto a un altro GPO e a un modello</span><span class="sxs-lookup"><span data-stu-id="8298c-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="8298c-390">Per confrontare MioGPO e MioaltroGPO:</span><span class="sxs-lookup"><span data-stu-id="8298c-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="8298c-391">Nella scheda **controllata** fare clic su **MioGPO**.</span><span class="sxs-lookup"><span data-stu-id="8298c-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="8298c-392">Premere **CTRL** e quindi fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="8298c-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="8298c-393">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e fare clic su **report HTML**.</span><span class="sxs-lookup"><span data-stu-id="8298c-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="8298c-394">Per confrontare MioaltroGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="8298c-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="8298c-395">Nella scheda **controllata** fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="8298c-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="8298c-396">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e fare clic su **modello**.</span><span class="sxs-lookup"><span data-stu-id="8298c-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="8298c-397">Selezionare **MyTemplate** e **report HTML**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="8298c-398">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="8298c-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="8298c-399">In questo passaggio si funge da approvatore per eliminare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="8298c-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="8298c-400">Per eliminare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="8298c-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="8298c-401">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="8298c-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="8298c-402">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="8298c-403">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="8298c-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="8298c-404">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="8298c-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="8298c-405">Fare clic su **Elimina GPO da archiviazione e produzione** per eliminare sia la versione nell'archivio che la versione distribuita del GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="8298c-406">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="8298c-407">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-408">Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="8298c-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="8298c-409">Occasionalmente potresti scoprire dopo l'eliminazione di un GPO che è ancora necessario.</span><span class="sxs-lookup"><span data-stu-id="8298c-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="8298c-410">In questo passaggio si funge da approvatore per ripristinare un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="8298c-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="8298c-411">Per ripristinare un oggetto Criteri di stato eliminato</span><span class="sxs-lookup"><span data-stu-id="8298c-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="8298c-412">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare i GPO eliminati.</span><span class="sxs-lookup"><span data-stu-id="8298c-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="8298c-413">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="8298c-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="8298c-414">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8298c-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="8298c-415">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-416">L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .</span><span class="sxs-lookup"><span data-stu-id="8298c-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="8298c-417">**Nota**  Il ripristino di un GPO nell'archivio non viene automaticamente ridistribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="8298c-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="8298c-418">Per restituire il GPO all'ambiente di produzione, distribuire il GPO come nel [passaggio 3: rivedere e distribuire un oggetto Criteri di controllo](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="8298c-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="8298c-419">Dopo la modifica e la distribuzione di un oggetto Criteri di ricerca, potresti scoprire che le recenti modifiche apportate al GPO causano un problema.</span><span class="sxs-lookup"><span data-stu-id="8298c-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="8298c-420">In questo passaggio si funge da approvatore per eseguire il rollback a una versione precedente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="8298c-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="8298c-421">È possibile eseguire il rollback a qualsiasi versione nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="8298c-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="8298c-422">È possibile usare i commenti e le etichette per identificare le versioni valide note e quando sono state apportate modifiche specifiche.</span><span class="sxs-lookup"><span data-stu-id="8298c-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="8298c-423">Per eseguire il rollback a una versione precedente di un oggetto Criteri di controllo</span><span class="sxs-lookup"><span data-stu-id="8298c-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="8298c-424">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="8298c-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="8298c-425">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="8298c-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="8298c-426">Fare clic con il pulsante destro del mouse sulla versione da distribuire, scegliere **Distribuisci**e quindi fare clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="8298c-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="8298c-427">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8298c-428">Nella finestra **cronologia** fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="8298c-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="8298c-429">**Nota**  Per verificare che la versione ridistribuita sia la versione progettata, esaminare un report di differenza per le due versioni.</span><span class="sxs-lookup"><span data-stu-id="8298c-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="8298c-430">Nella finestra **cronologia** del GPO selezionare le due versioni, fare clic con il pulsante destro del mouse su di esse, scegliere **differenza**e quindi fare clic su **report HTML** o **report XML**.</span><span class="sxs-lookup"><span data-stu-id="8298c-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





