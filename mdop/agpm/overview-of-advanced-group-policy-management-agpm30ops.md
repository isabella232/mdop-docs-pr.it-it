---
title: Panoramica di Gestione avanzata Criteri di gruppo
description: Panoramica di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822495"
---
# <span data-ttu-id="d67f4-103">Panoramica di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d67f4-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="d67f4-104">È possibile usare Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo per offrire un controllo di modifica completo e una gestione migliorata per gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d67f4-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="d67f4-105">Sviluppo di oggetti Criteri di gruppo con il controllo delle modifiche</span><span class="sxs-lookup"><span data-stu-id="d67f4-105">Group Policy object development with change control</span></span>


<span data-ttu-id="d67f4-106">Con Advanced Group Policy Management è possibile archiviare una copia di ogni oggetto Criteri di gruppo in un archivio centrale in modo che gli amministratori dei criteri di raggruppamento possano visualizzarlo e modificarlo offline senza influire immediatamente sulla versione distribuita del GPO.</span><span class="sxs-lookup"><span data-stu-id="d67f4-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="d67f4-107">Inoltre, Advanced Group Policy Management archivia una copia di ogni versione di ogni GPO controllato nell'archivio in modo da poter eseguire il rollback a una versione precedente, se necessario.</span><span class="sxs-lookup"><span data-stu-id="d67f4-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="d67f4-108">I termini "Archivia" e "Estrai" vengono usati proprio come in una raccolta (o in applicazioni che includono controllo delle modifiche, controllo della versione o controllo del codice sorgente per lo sviluppo della programmazione).</span><span class="sxs-lookup"><span data-stu-id="d67f4-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="d67f4-109">Per usare un libro che si trova in una raccolta, è possibile estrarlo dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d67f4-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="d67f4-110">Nessun altro utente può usarlo mentre è estratto. Dopo aver completato il libro, è possibile archiviarlo di nuovo nella raccolta, in modo che altri utenti possano usarlo.</span><span class="sxs-lookup"><span data-stu-id="d67f4-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="d67f4-111">Quando si sviluppano GPO tramite Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="d67f4-111">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="d67f4-112">Crea un nuovo oggetto Criteri di controllo controllato o controlla un oggetto Criteri di controllo precedentemente non controllato.</span><span class="sxs-lookup"><span data-stu-id="d67f4-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="d67f4-113">Consulta il GPO, in modo che tu e solo tu possa cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="d67f4-113">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="d67f4-114">Modificare l'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="d67f4-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="d67f4-115">Archiviare il GPO modificato in modo che altri utenti possano modificarlo o in modo che possa essere distribuito.</span><span class="sxs-lookup"><span data-stu-id="d67f4-115">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="d67f4-116">Esaminare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="d67f4-116">Review the changes.</span></span>

6.  <span data-ttu-id="d67f4-117">Distribuire il GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="d67f4-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="d67f4-118">Delega basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="d67f4-118">Role-based delegation</span></span>


<span data-ttu-id="d67f4-119">Advanced Group Policy Management offre una delega basata sui ruoli completa e di facile utilizzo per la gestione dell'accesso ai GPO nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="d67f4-119">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="d67f4-120">Le autorizzazioni a livello di dominio consentono agli amministratori della gestione avanzata di fornire l'accesso a singoli domini senza consentire l'accesso ad altri domini.</span><span class="sxs-lookup"><span data-stu-id="d67f4-120">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="d67f4-121">La delega basata su GPO consente agli amministratori della Advanced Group Policy di fornire l'accesso a GPO specifici senza fornire accesso a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="d67f4-121">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="d67f4-122">In Advanced Group Policy Management sono presenti ruoli definiti in modo specifico: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore.</span><span class="sxs-lookup"><span data-stu-id="d67f4-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="d67f4-123">Il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli.</span><span class="sxs-lookup"><span data-stu-id="d67f4-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="d67f4-124">Per impostazione predefinita, solo i responsabili approvazione hanno la possibilità di distribuire GPO nell'ambiente di produzione, proteggendo l'ambiente dagli errori degli editori meno esperti.</span><span class="sxs-lookup"><span data-stu-id="d67f4-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="d67f4-125">Anche per impostazione predefinita, tutti i ruoli includono il ruolo revisore e quindi la possibilità di visualizzare le impostazioni GPO nei report.</span><span class="sxs-lookup"><span data-stu-id="d67f4-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="d67f4-126">Tuttavia, Advanced Group Policy Management offre a un amministratore della Advanced Group Policy la flessibilità di personalizzare l'accesso degli oggetti Criteri di gestione per soddisfare le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d67f4-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="d67f4-127">Delega in un ambiente di amministrazione di più criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d67f4-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="d67f4-128">In un ambiente in cui più persone modificano gli oggetti Criteri di gruppo, un amministratore della gestione avanzata delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori, come gruppi o come singoli utenti.</span><span class="sxs-lookup"><span data-stu-id="d67f4-128">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="d67f4-129">Per un processo di sviluppo GPO tipico per un editor e un responsabile approvazione, vedere [elenco di controllo: creare, modificare e distribuire un oggetto Criteri](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d67f4-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="d67f4-130">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d67f4-130">Additional references</span></span>

-   [<span data-ttu-id="d67f4-131">Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 3.0</span><span class="sxs-lookup"><span data-stu-id="d67f4-131">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





