---
title: Eseguire il backup dell'archivio
description: Eseguire il backup dell'archivio
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819215"
---
# <span data-ttu-id="c1cf8-103">Eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="c1cf8-103">Back Up the Archive</span></span>


<span data-ttu-id="c1cf8-104">Per agevolare il ripristino dell'archivio per Advanced Group Policy Management (gestione avanzata Criteri di gruppo) in caso di emergenza, un amministratore della Advanced Group Policy (controllo completo) deve eseguire il backup dell'archivio di frequente.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="c1cf8-105">Per impostazione predefinita, l'archivio viene creato in%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="c1cf8-106">Tuttavia, è possibile specificare un percorso diverso durante la configurazione di Microsoft Advanced Group Policy Management-Server.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="c1cf8-107">Un account utente che ha accesso sia al server Advanced Group Policy Management, il computer in cui è installato il servizio Advanced Group Policy Management, sia alla cartella che contiene l'archivio è necessario per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="c1cf8-108">Per eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="c1cf8-108">To back up the archive</span></span>**

1.  <span data-ttu-id="c1cf8-109">Arrestare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-109">Stop the AGPM Service.</span></span> <span data-ttu-id="c1cf8-110">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="c1cf8-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="c1cf8-111">Eseguire il backup della cartella di archiviazione usando Esplora risorse, xcopy, Windows Server® backup o un altro strumento di backup.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="c1cf8-112">Assicurarsi di eseguire il backup dei file nascosti, di sistema e di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="c1cf8-113">Archiviare il backup dell'archivio in una posizione sicura.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="c1cf8-114">Riavviare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-114">Restart the AGPM Service.</span></span> <span data-ttu-id="c1cf8-115">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="c1cf8-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

<span data-ttu-id="c1cf8-116">**Nota**  Se un amministratore Advanced Group Policy Management fa eseguire il backup dell'archivio in modo non frequente, gli oggetti Criteri di gruppo nel backup dell'archivio non saranno correnti.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="c1cf8-117">Per fare in modo che il backup dell'archivio sia aggiornato, eseguire il backup dell'archivio nell'ambito della strategia di backup giornaliera dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c1cf8-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="c1cf8-118">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="c1cf8-118">Additional references</span></span>

-   [<span data-ttu-id="c1cf8-119">Ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="c1cf8-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="c1cf8-120">Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c1cf8-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="c1cf8-121">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="c1cf8-121">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





