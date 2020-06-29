---
title: Ripristinare l'archivio da un backup
description: Ripristinare l'archivio da un backup
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818396"
---
# <span data-ttu-id="f2768-103">Ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="f2768-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="f2768-104">Se si verifica un problema di emergenza e l'archivio per Advanced Group Policy Management è danneggiato o distrutto, un amministratore della gestione avanzata Criteri di gruppo (controllo completo) può ripristinare l'archivio da una copia di backup preparata in anticipo e quindi importare dall'ambiente di produzione del dominio eventuali oggetti Criteri di gruppo che non sono presenti nell'archivio o per i quali la versione in produzione è più aggiornata di quella dell'archivio</span><span class="sxs-lookup"><span data-stu-id="f2768-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment of the domain any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="f2768-105">Per informazioni su come ripristinare un backup di archivio in un altro server, vedere [trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f2768-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

<span data-ttu-id="f2768-106">Per completare questa procedura è necessario un account utente che abbia accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management) e alla cartella che contiene l'archivio.</span><span class="sxs-lookup"><span data-stu-id="f2768-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="f2768-107">Per ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="f2768-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="f2768-108">Arrestare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f2768-108">Stop the AGPM Service.</span></span> <span data-ttu-id="f2768-109">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f2768-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="f2768-110">Rimuovere l'archivio esistente.</span><span class="sxs-lookup"><span data-stu-id="f2768-110">Remove the existing archive.</span></span> <span data-ttu-id="f2768-111">Per impostazione predefinita, la cartella di archiviazione è%ProgramData%\\Microsoft\\AGPM, ma l'amministratore della gestione avanzata Criteri di gruppo che ha installato Microsoft Advanced Group Policy Management-Server potrebbe avere immesso una posizione diversa durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f2768-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="f2768-112">Creare nuovamente la cartella di archiviazione configurando il percorso di archiviazione, l'account del servizio Advanced Group Policy Management, il proprietario dell'archivio e la porta di ascolto.</span><span class="sxs-lookup"><span data-stu-id="f2768-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="f2768-113">Non è necessario usare gli stessi valori usati durante l'installazione originale.</span><span class="sxs-lookup"><span data-stu-id="f2768-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="f2768-114">Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f2768-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

4.  <span data-ttu-id="f2768-115">Copiare il contenuto del backup dell'archivio nella cartella di archiviazione, copiando le sottocartelle e i file per verificare che tutte le sottocartelle e i file ereditino le autorizzazioni della cartella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f2768-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="f2768-116">Prestare attenzione a non sovrascrivere la cartella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f2768-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="f2768-117">Se non si è certi che un GPO nel backup dell'archivio sia più attuale della copia di tale oggetto in produzione, generare un report di differenza e confrontarne le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f2768-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="f2768-118">Per altre informazioni, vedere [identificare le differenze tra GPO, versioni GPO o modelli](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f2768-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span></span>

6.  <span data-ttu-id="f2768-119">Riavviare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f2768-119">Restart the AGPM Service.</span></span> <span data-ttu-id="f2768-120">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f2768-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

### <span data-ttu-id="f2768-121">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="f2768-121">Additional references</span></span>

-   [<span data-ttu-id="f2768-122">Eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="f2768-122">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="f2768-123">Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f2768-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="f2768-124">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="f2768-124">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





