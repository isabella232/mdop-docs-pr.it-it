---
title: Modificare il servizio Gestione avanzata Criteri di gruppo
description: Modificare il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820505"
---
# <span data-ttu-id="65322-103">Modificare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="65322-103">Modify the AGPM Service</span></span>


<span data-ttu-id="65322-104">Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.</span><span class="sxs-lookup"><span data-stu-id="65322-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="65322-105">Se questo servizio viene arrestato o disabilitato, i client Advanced Group Policy Management non possono eseguire operazioni tramite il server.</span><span class="sxs-lookup"><span data-stu-id="65322-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="65322-106">È possibile modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management e la porta in cui è in ascolto il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="65322-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="65322-107">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="65322-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="65322-108">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="65322-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="65322-109">Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="65322-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="65322-110">È inoltre necessario specificare le credenziali per l'account del servizio Advanced Group Policy Management per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="65322-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="65322-111">Per modificare il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="65322-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="65322-112">Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server:</span><span class="sxs-lookup"><span data-stu-id="65322-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed:</span></span>

    -   <span data-ttu-id="65322-113">Per WindowsServer2008, fare clic su **Start**, **Pannello di controllo**e **programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="65322-113">For WindowsServer2008, click **Start**, **Control Panel**, and **Programs and Features**.</span></span>

    -   <span data-ttu-id="65322-114">Per WindowsVista, fare clic su **Start**, **Pannello di controllo**, **programmi** **e programmi e funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="65322-114">For WindowsVista, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="65322-115">Fare clic con il pulsante destro del mouse su **Microsoft Advanced Group Policy Management-Server**e quindi scegliere **Cambia**.</span><span class="sxs-lookup"><span data-stu-id="65322-115">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="65322-116">Fare clic su **Avanti**e quindi su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="65322-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="65322-117">Seguire le istruzioni per configurare il servizio Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="65322-117">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="65322-118">Nella finestra di dialogo **percorso di archiviazione** immettere una nuova posizione per l'archivio relativo al server Advanced Group Policy Management oppure confermare il percorso di archiviazione corrente e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="65322-118">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="65322-119">**Importante**  Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="65322-119">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="65322-120">Nella finestra di dialogo **account di servizio Advanced Group Policy Management** immettere le credenziali per un account del servizio in cui verrà eseguito il servizio Advanced Group Policy Management e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="65322-120">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="65322-121">**Importante**  La modifica dell'installazione Cancella le credenziali per l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="65322-121">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="65322-122">È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.</span><span class="sxs-lookup"><span data-stu-id="65322-122">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="65322-123">L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà e sarà concesso **accedere come** autorizzazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="65322-123">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="65322-124">Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="65322-124">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="65322-125">Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.</span><span class="sxs-lookup"><span data-stu-id="65322-125">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="65322-126">Nella finestra di dialogo **proprietario archivio** immettere il nome utente di un amministratore Advanced Group Policy Management (controllo completo) o di un gruppo di amministratori Advanced Group Policy Management, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="65322-126">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="65322-127">**Nota**  La modifica dell'installazione Cancella le credenziali per il proprietario dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="65322-127">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="65322-128">È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.</span><span class="sxs-lookup"><span data-stu-id="65322-128">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="65322-129">Nella finestra di dialogo **configurazione porta** Digitare una nuova porta in cui il servizio Advanced Group Policy Management deve ascoltare o confermare la porta attualmente selezionata e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="65322-129">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="65322-130">**Nota**  Per impostazione predefinita, il servizio Advanced Policy Management è in ascolto sulla porta 4600.</span><span class="sxs-lookup"><span data-stu-id="65322-130">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="65322-131">Se si configurano manualmente le eccezioni della porta o si hanno regole per la configurazione delle eccezioni della porta, è possibile deselezionare la casella **di controllo Aggiungi eccezione porta al firewall** .</span><span class="sxs-lookup"><span data-stu-id="65322-131">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="65322-132">Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="65322-132">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="65322-133">Se è stata modificata la porta in cui è in ascolto il servizio Advanced Group Policy Management, modificare la porta nella connessione del server Advanced Group Policy Management per ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="65322-133">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="65322-134">Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="65322-134">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).)</span></span>

7.  <span data-ttu-id="65322-135">Ripetere la procedura per ogni server Advanced Group Policy Management a cui applicare le modifiche alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="65322-135">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="65322-136">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="65322-136">Additional references</span></span>

-   [<span data-ttu-id="65322-137">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="65322-137">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 




