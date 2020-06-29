---
title: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 3.0
description: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 3.0
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822506"
---
# <span data-ttu-id="06566-103">Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 3.0</span><span class="sxs-lookup"><span data-stu-id="06566-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="06566-104">È possibile usare Microsoft Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo, garantendo un controllo completo delle modifiche e una gestione avanzata per gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="06566-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="06566-105">Con Advanced Group Policy Management è possibile:</span><span class="sxs-lookup"><span data-stu-id="06566-105">With AGPM you can:</span></span>

-   <span data-ttu-id="06566-106">Eseguire la modifica offline degli oggetti Criteri di controllo, in modo da poterli creare e testare prima della distribuzione in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="06566-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="06566-107">Mantenere più versioni di un oggetto Criteri di gruppo in un archivio centrale, in modo da poter eseguire il rollback se si verifica un problema.</span><span class="sxs-lookup"><span data-stu-id="06566-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="06566-108">Condividere la responsabilità per la modifica, l'approvazione e la revisione degli oggetti Criteri di gruppo tra più utenti tramite delega basata sui ruoli.</span><span class="sxs-lookup"><span data-stu-id="06566-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="06566-109">Eliminare il pericolo che più amministratori di criteri di gruppo sovrascrivano il lavoro reciproco usando una funzionalità di archiviazione/estrazione per gli oggetti Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="06566-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="06566-110">Analizza le modifiche apportate a un oggetto Criteri di confronto a un altro GPO o a un'altra versione dello stesso GPO usando la segnalazione delle differenze.</span><span class="sxs-lookup"><span data-stu-id="06566-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="06566-111">Semplificare la creazione di nuovi GPO usando i modelli di GPO, archiviando le impostazioni standard da usare come punti di partenza per i nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="06566-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="06566-112">Advanced Group Policy Management aggiunge una cartella di **controllo delle modifiche** in ogni dominio visualizzato in GPMC, oltre a una scheda **cronologia** per ogni collegamento a criteri di gruppo e criteri di raggruppamento visualizzato in GPMC.</span><span class="sxs-lookup"><span data-stu-id="06566-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="06566-113">Panoramica di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="06566-114">Procedure consigliate per il controllo della versione</span><span class="sxs-lookup"><span data-stu-id="06566-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="06566-115">Elenco di controllo: Amministrare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="06566-116">Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="06566-117">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="06566-118">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="06566-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="06566-119">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="06566-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="06566-120">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="06566-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="06566-121">Risoluzione dei problemi di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="06566-122">Interfaccia utente: Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="06566-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





