---
title: Modificare il percorso di archiviazione
description: Modificare il percorso di archiviazione
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820495"
---
# <span data-ttu-id="10fad-103">Modificare il percorso di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10fad-103">Modify the Archive Path</span></span>


<span data-ttu-id="10fad-104">Il percorso di archiviazione è la posizione dell'archivio relativo al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="10fad-105">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o in un altro server della stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="10fad-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="10fad-106">Il percorso di archiviazione e l'account del servizio Advanced Group Policy Management vengono configurati durante l'installazione del server Advanced Group Policy Management e possono essere modificati successivamente tramite installazione **applicazioni** nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="10fad-107">Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="10fad-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="10fad-108">Per modificare il percorso di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10fad-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="10fad-109">Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server, fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare clic su **Aggiungi o Rimuovi programmi**.</span><span class="sxs-lookup"><span data-stu-id="10fad-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="10fad-110">Fare clic su **Microsoft Advanced Group Policy Management-Server**e quindi su **Cambia**.</span><span class="sxs-lookup"><span data-stu-id="10fad-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="10fad-111">Fare clic su **Avanti**e quindi su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="10fad-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="10fad-112">Seguire le istruzioni visualizzate per configurare le impostazioni per il servizio Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="10fad-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="10fad-113">Per il percorso di archiviazione, immettere un nuovo percorso per l'archivio relativo al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="10fad-114">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="10fad-115">Immettere le credenziali per l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="10fad-116">**Importante**  La modifica dell'installazione Cancella le credenziali per l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="10fad-117">È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.</span><span class="sxs-lookup"><span data-stu-id="10fad-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="10fad-118">L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà.</span><span class="sxs-lookup"><span data-stu-id="10fad-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="10fad-119">Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10fad-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="10fad-120">Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.</span><span class="sxs-lookup"><span data-stu-id="10fad-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="10fad-121">Per il proprietario dell'archivio, immettere le credenziali di un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="10fad-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="10fad-122">Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="10fad-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="10fad-123">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="10fad-123">Additional references</span></span>

-   [<span data-ttu-id="10fad-124">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="10fad-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





