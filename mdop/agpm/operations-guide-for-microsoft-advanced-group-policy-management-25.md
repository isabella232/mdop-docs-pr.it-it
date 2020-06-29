---
title: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 2.5
description: Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 2.5
author: dansimp
ms.assetid: 005f0bb5-789f-42a9-bcaf-7e8c31a8df66
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c0ae04e0e8dcf62d3ea840de28a9248827ec62e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822515"
---
# <span data-ttu-id="cc565-103">Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 2.5</span><span class="sxs-lookup"><span data-stu-id="cc565-103">Operations Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="cc565-104">È possibile usare Microsoft Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo, garantendo un controllo completo delle modifiche e una gestione avanzata per gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="cc565-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

<span data-ttu-id="cc565-105">Con Advanced Group Policy Management è possibile:</span><span class="sxs-lookup"><span data-stu-id="cc565-105">With AGPM you can:</span></span>

-   <span data-ttu-id="cc565-106">Eseguire la modifica offline degli oggetti Criteri di controllo, in modo da poterli creare e testare prima della distribuzione in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="cc565-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="cc565-107">Mantenere più versioni di un oggetto Criteri di gruppo in un archivio centrale, in modo da poter eseguire il rollback se si verifica un problema.</span><span class="sxs-lookup"><span data-stu-id="cc565-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="cc565-108">Condividere la responsabilità per la modifica, l'approvazione e la revisione degli oggetti Criteri di gruppo tra più utenti tramite delega basata sui ruoli.</span><span class="sxs-lookup"><span data-stu-id="cc565-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="cc565-109">Eliminare il pericolo che più amministratori di criteri di gruppo sovrascrivano il lavoro reciproco usando una funzionalità di archiviazione/estrazione per gli oggetti Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="cc565-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="cc565-110">Analizza le modifiche apportate a un oggetto Criteri di confronto a un altro GPO o a un'altra versione dello stesso GPO usando la segnalazione delle differenze.</span><span class="sxs-lookup"><span data-stu-id="cc565-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="cc565-111">Semplificare la creazione di nuovi GPO usando i modelli di GPO, archiviando le impostazioni standard da usare come punti di partenza per i nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="cc565-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="cc565-112">Advanced Group Policy Management aggiunge un nodo di **controllo delle modifiche** in ogni dominio visualizzato in GPMC, nonché le schede **cronologia** ed **estensioni** per ogni collegamento di criteri di gruppo e GPO visualizzato in GPMC.</span><span class="sxs-lookup"><span data-stu-id="cc565-112">AGPM adds a **Change Control** node under each domain displayed in the GPMC, as well as **History** and **Extensions** tabs for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="cc565-113">Panoramica di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc565-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management.md)

-   [<span data-ttu-id="cc565-114">Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc565-114">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="cc565-115">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc565-115">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="cc565-116">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="cc565-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="cc565-117">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="cc565-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="cc565-118">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="cc565-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="cc565-119">Risoluzione dei problemi di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc565-119">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="cc565-120">Interfaccia utente: Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cc565-120">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





