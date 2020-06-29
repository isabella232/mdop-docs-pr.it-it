---
title: Gestione dell'archivio
description: Gestione dell'archivio
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820556"
---
# <span data-ttu-id="dd72d-103">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="dd72d-103">Managing the Archive</span></span>


<span data-ttu-id="dd72d-104">In gestione avanzata Criteri di gruppo, come amministratore Advanced Group Policy Management (controllo completo), puoi gestire l'accesso all'archivio e avere l'opzione di limitare il numero di versioni di ogni oggetto Criteri di gruppo archiviato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="dd72d-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="dd72d-105">Puoi delegare l'accesso a GPO nell'archivio a livello di dominio o a livello di GPO.</span><span class="sxs-lookup"><span data-stu-id="dd72d-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="dd72d-106">È inoltre possibile eseguire il backup dell'archivio in modo da poterlo recuperare se si verifica un disastro.</span><span class="sxs-lookup"><span data-stu-id="dd72d-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="dd72d-107">In qualità di amministratore della Advanced Group Policy Management, è possibile esportare un oggetto Criteri di campo in un file, copiare il file in un'altra foresta e quindi importare il GPO in un dominio della foresta.</span><span class="sxs-lookup"><span data-stu-id="dd72d-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="dd72d-108">A differenza di un editor, è possibile importare le impostazioni dei criteri da un backup del GPO direttamente in un nuovo oggetto Criteri di controllo durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="dd72d-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="dd72d-109">Per informazioni su come esportare un oggetto Criteri di ricerca, vedere [esportare un oggetto Criteri di ricerca in un file](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="dd72d-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="dd72d-110">Delegare l'accesso a livello di dominio all'archivio</span><span class="sxs-lookup"><span data-stu-id="dd72d-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="dd72d-111">Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio</span><span class="sxs-lookup"><span data-stu-id="dd72d-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="dd72d-112">Limitare le versioni degli oggetti Criteri di gruppo archiviate</span><span class="sxs-lookup"><span data-stu-id="dd72d-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="dd72d-113">Importare un oggetto Criteri di gruppo da un file</span><span class="sxs-lookup"><span data-stu-id="dd72d-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="dd72d-114">Eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="dd72d-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="dd72d-115">Ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="dd72d-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="dd72d-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="dd72d-116">Additional references</span></span>

-   <span data-ttu-id="dd72d-117">Per informazioni su come delegare l'accesso ai GPO nell'ambiente di produzione, vedere [delega dell'accesso all'ambiente di produzione](delegate-access-to-the-production-environment-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="dd72d-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="dd72d-118">Per informazioni su come trasferire l'archivio, vedere [trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="dd72d-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="dd72d-119">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="dd72d-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





