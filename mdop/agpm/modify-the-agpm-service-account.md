---
title: Modificare l'account del servizio Gestione avanzata Criteri di gruppo
description: Modificare l'account del servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820525"
---
# <span data-ttu-id="cc367-103">Modificare l'account del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc367-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="cc367-104">Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.</span><span class="sxs-lookup"><span data-stu-id="cc367-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="cc367-105">Se questo servizio viene arrestato o disabilitato, i client Advanced Group Policy Management non possono eseguire operazioni tramite il server.</span><span class="sxs-lookup"><span data-stu-id="cc367-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="cc367-106">Il percorso di archiviazione e l'account del servizio Advanced Group Policy Management vengono configurati durante l'installazione del server Advanced Group Policy Management e possono essere modificati successivamente tramite installazione **applicazioni** nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="cc367-107">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cc367-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="cc367-108">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="cc367-109">Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="cc367-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="cc367-110">**Importante**  L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà e sarà concesso **accedere come** autorizzazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="cc367-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="cc367-111">Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="cc367-112">Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.</span><span class="sxs-lookup"><span data-stu-id="cc367-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="cc367-113">Per modificare l'account del servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="cc367-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="cc367-114">Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server, fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare clic su **Aggiungi o Rimuovi programmi**.</span><span class="sxs-lookup"><span data-stu-id="cc367-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="cc367-115">Fare clic su **Microsoft Advanced Group Policy Management-Server**e quindi su **Cambia**.</span><span class="sxs-lookup"><span data-stu-id="cc367-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="cc367-116">Fare clic su **Avanti**e quindi su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="cc367-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="cc367-117">Seguire le istruzioni visualizzate per configurare le impostazioni per il servizio Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="cc367-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="cc367-118">Per il percorso di archiviazione, confermare o modificare il percorso dell'archivio relativo al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="cc367-119">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="cc367-120">Immettere nuove credenziali per l'account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cc367-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="cc367-121">Per il proprietario dell'archivio, immettere le credenziali di un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="cc367-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="cc367-122">Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="cc367-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="cc367-123">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="cc367-123">Additional references</span></span>

-   [<span data-ttu-id="cc367-124">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc367-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





