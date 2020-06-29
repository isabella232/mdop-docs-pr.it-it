---
title: Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo
description: Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822535"
---
# <span data-ttu-id="e4295-103">Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e4295-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="e4295-104">Se si sostituisce il server Advanced Group Policy Management e il server in cui è ospitato l'archivio, è necessario trasferire il servizio Advanced Group Policy Management e l'archivio.</span><span class="sxs-lookup"><span data-stu-id="e4295-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="e4295-105">Se si preferisce, è possibile trasferire il servizio Advanced Group Policy Management e l'archivio separatamente.</span><span class="sxs-lookup"><span data-stu-id="e4295-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="e4295-106">Nota</span><span class="sxs-lookup"><span data-stu-id="e4295-106">Note</span></span>**  
-   <span data-ttu-id="e4295-107">Il server Advanced Group Policy Management è il computer che ospita il servizio Advanced Policy Management e il computer in cui è installato Microsoft Advanced Group Policy Management-Server.</span><span class="sxs-lookup"><span data-stu-id="e4295-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="e4295-108">Per impostazione predefinita, l'archivio è ospitato nel server Advanced Group Policy Management, ma è possibile specificare un percorso di archiviazione per ospitarlo in un altro server.</span><span class="sxs-lookup"><span data-stu-id="e4295-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="e4295-109">Per completare questa procedura è necessario un account utente che sia membro del gruppo Domain Admins e che abbia accesso ai nuovi server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e4295-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="e4295-110">È inoltre necessario specificare le credenziali per l'account del servizio Advanced Group Policy Management che verrà usato dal nuovo server Advanced Group Policy Management per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="e4295-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="e4295-111">Per trasferire il servizio Advanced Group Policy Management e l'archivio in un server o server diverso</span><span class="sxs-lookup"><span data-stu-id="e4295-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="e4295-112">Eseguire il backup dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="e4295-112">Back up the archive.</span></span> <span data-ttu-id="e4295-113">Per altre informazioni, vedere [eseguire il backup dell'archivio](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="e4295-114">Trasferire il servizio Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="e4295-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="e4295-115">Arrestare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e4295-115">Stop the AGPM Service.</span></span> <span data-ttu-id="e4295-116">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="e4295-117">Installare Microsoft Advanced Group Policy Management-Server nel nuovo server che ospiterà il servizio Advanced Group Policy Manager.</span><span class="sxs-lookup"><span data-stu-id="e4295-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="e4295-118">Durante questo processo, devi specificare il nuovo percorso di archiviazione, la posizione dell'archivio in relazione al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e4295-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="e4295-119">Per altre informazioni, vedere [Guida dettagliata per Microsoft Advanced Group Policy management 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) ( https://go.microsoft.com/fwlink/?LinkId=153505) e [Guida alla pianificazione per Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) ( https://go.microsoft.com/fwlink/?LinkId=156883) .</span><span class="sxs-lookup"><span data-stu-id="e4295-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="e4295-120">Un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) deve configurare la connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo che utilizzeranno il nuovo server Advanced Group Policy Management e rimuovere la connessione per il vecchio server Advanced Group Policy Management oppure ogni amministratore di criteri di gruppo deve configurare manualmente la nuova connessione al server Advanced Group Policy Management per lo snap-in del computer.</span><span class="sxs-lookup"><span data-stu-id="e4295-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="e4295-121">Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="e4295-122">**Nota**  Come procedura consigliata, è consigliabile disinstallare Microsoft Advanced Group Policy Management-Server dal server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e4295-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="e4295-123">In questo modo, il servizio Advanced Group Policy Management non può essere riavviato involontariamente sul server e potrebbe causare confusione se le connessioni del server Advanced Group Policy Management restano.</span><span class="sxs-lookup"><span data-stu-id="e4295-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="e4295-124">Copiare l'archivio dal backup al nuovo server che ospiterà l'archivio.</span><span class="sxs-lookup"><span data-stu-id="e4295-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="e4295-125">Per altre informazioni, vedere [ripristinare l'archivio da un backup](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="e4295-126">**Importante**  Se l'archivio è stato spostato senza spostare contemporaneamente il servizio Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="e4295-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="e4295-127">È necessario modificare il percorso di archiviazione in base al nuovo percorso dell'archivio in relazione al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e4295-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="e4295-128">Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="e4295-129">È necessario immettere di nuovo e confermare la password nella scheda **delega del dominio** . Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e4295-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="e4295-130">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="e4295-130">Additional references</span></span>

-   [<span data-ttu-id="e4295-131">Eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="e4295-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="e4295-132">Ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="e4295-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="e4295-133">Configurare le connessioni server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e4295-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="e4295-134">Modificare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e4295-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="e4295-135">[Guida dettagliata per Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="e4295-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="e4295-136">[Guida alla pianificazione per Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="e4295-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="e4295-137">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e4295-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





