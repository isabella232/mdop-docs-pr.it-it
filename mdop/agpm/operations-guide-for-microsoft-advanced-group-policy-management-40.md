---
title: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 4.0
description: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 4.0
author: dansimp
ms.assetid: 0bafeba3-20a9-4360-be5d-03f786df11ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b51956c319f1b0a77e4a4bdf71090be4f322236e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820485"
---
# <span data-ttu-id="3156e-103">Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 4.0</span><span class="sxs-lookup"><span data-stu-id="3156e-103">Operations Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="3156e-104">È possibile usare Microsoft Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3156e-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="3156e-105">Advanced Group Policy Management offre un controllo completo delle modifiche e una gestione migliorata degli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3156e-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="3156e-106">Usando Advanced Group Policy Management puoi eseguire queste attività:</span><span class="sxs-lookup"><span data-stu-id="3156e-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="3156e-107">Eseguire la modifica offline degli oggetti Criteri di controllo in modo da poterli creare e testare prima di distribuirli in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="3156e-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="3156e-108">Gestire più versioni di un oggetto Criteri di gruppo in un archivio centrale in modo da poter eseguire il rollback se si verifica un problema.</span><span class="sxs-lookup"><span data-stu-id="3156e-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="3156e-109">Condividere la responsabilità per la modifica, l'approvazione e la revisione degli oggetti Criteri di gruppo tra più utenti tramite delega basata sui ruoli.</span><span class="sxs-lookup"><span data-stu-id="3156e-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="3156e-110">Eliminare il pericolo che più amministratori di criteri di gruppo sovrascrivano l'un l'altro tramite la funzionalità check-in e check-out per i GPO.</span><span class="sxs-lookup"><span data-stu-id="3156e-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="3156e-111">Analizza le modifiche apportate a un oggetto Criteri di confronto a un altro GPO o a un'altra versione dello stesso GPO usando la segnalazione delle differenze.</span><span class="sxs-lookup"><span data-stu-id="3156e-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="3156e-112">Semplificare la creazione di nuovi GPO usando i modelli di GPO, archiviando le impostazioni dei criteri comuni e le impostazioni delle preferenze da usare come punti di partenza per i nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="3156e-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="3156e-113">Delegare l'accesso all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="3156e-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="3156e-114">Cercare gli oggetti Criteri di ricerca con attributi specifici e filtrare l'elenco dei GPO visualizzati.</span><span class="sxs-lookup"><span data-stu-id="3156e-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="3156e-115">Esportare un oggetto Criteri di controllo in un file in modo da poterlo copiare da un dominio in una foresta di test in un dominio in una foresta di produzione.</span><span class="sxs-lookup"><span data-stu-id="3156e-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="3156e-116">Advanced Group Policy Management aggiunge una cartella di **controllo delle modifiche** in ogni dominio visualizzato in GPMC, oltre a una scheda **cronologia** per ogni collegamento a criteri di gruppo e criteri di raggruppamento visualizzato in GPMC.</span><span class="sxs-lookup"><span data-stu-id="3156e-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="3156e-117">Panoramica di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="3156e-118">Procedure consigliate per il controllo della versione</span><span class="sxs-lookup"><span data-stu-id="3156e-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="3156e-119">Elenco di controllo: Amministrare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="3156e-120">Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="3156e-121">Cercare e filtrare l'elenco di oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="3156e-122">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="3156e-123">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="3156e-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="3156e-124">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="3156e-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="3156e-125">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="3156e-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="3156e-126">Risoluzione dei problemi relativi a Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="3156e-127">Interfaccia utente: Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3156e-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





