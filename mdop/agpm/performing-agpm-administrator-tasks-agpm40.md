---
title: Attività di amministrazione per Gestione avanzata Criteri di gruppo
description: Attività di amministrazione per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822416"
---
# <span data-ttu-id="10627-103">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="10627-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="10627-104">Gestione avanzata Criteri di gruppo consente a un amministratore Advanced Group Policy Management (controllo completo) di configurare le opzioni a livello di dominio e di delegare le autorizzazioni per i responsabili approvazione, gli editor, i revisori e gli amministratori dell'organizzazione avanzata.</span><span class="sxs-lookup"><span data-stu-id="10627-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="10627-105">Per impostazione predefinita, un amministratore Advanced Group Policy Management è un utente che ha il controllo completo, tutte le autorizzazioni di Advanced Group Policy Management, e che può quindi eseguire attività associate a qualsiasi ruolo.</span><span class="sxs-lookup"><span data-stu-id="10627-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="10627-106">In un ambiente in cui più persone sviluppano oggetti Criteri di gruppo (GPO) è possibile scegliere di consentire a tutti gli amministratori dei criteri di gruppo di eseguire le stesse attività e di avere lo stesso livello di accesso.</span><span class="sxs-lookup"><span data-stu-id="10627-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="10627-107">In alternativa, puoi scegliere di consentire agli amministratori della gestione avanzata di delegare le autorizzazioni agli editor che possono modificare gli oggetti Criteri di gruppo e agli approvatori che distribuiscono GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="10627-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="10627-108">Gli amministratori della gestione avanzata possono configurare le autorizzazioni per soddisfare le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="10627-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="10627-109">[Configurazione della gestione dei criteri di gruppo avanzati](configuring-advanced-group-policy-management-agpm40.md): configurare la connessione e la notifica tramite posta elettronica del server Advanced Group Policy Management, delegare l'accesso ai GPO nell'ambiente di produzione e configurare la registrazione e la traccia per la risoluzione</span><span class="sxs-lookup"><span data-stu-id="10627-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="10627-110">[Gestione dell'archivio](managing-the-archive-agpm40.md): delegare l'accesso ai GPO nell'archivio, limitare il numero di versioni di ogni GPO archiviato, importare un oggetto Criteri di un altro dominio ed eseguire il backup e il ripristino dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="10627-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="10627-111">[Gestione del servizio Advanced Group Policy Management](managing-the-agpm-service-agpm40.md): arrestare e avviare il servizio Advanced Group Policy Management o modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management o la porta in cui viene ascoltato il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10627-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="10627-112">[Trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive-agpm40.md): trasferire il servizio Advanced Group Policy Management, l'archivio o entrambi in un server diverso.</span><span class="sxs-lookup"><span data-stu-id="10627-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="10627-113">**Nota**  Poiché il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli, un amministratore Advanced Group Policy Management può eseguire le attività in genere associate a qualsiasi altro ruolo.</span><span class="sxs-lookup"><span data-stu-id="10627-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="10627-114">[Esecuzione di attività di approvazione](performing-approver-tasks-agpm40.md), ad esempio la creazione, la distribuzione o l'eliminazione di GPO</span><span class="sxs-lookup"><span data-stu-id="10627-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="10627-115">[Esecuzione di attività dell'editor](performing-editor-tasks-agpm40.md), ad esempio la modifica, la ridenominazione, l'etichettatura o l'importazione di GPO, la creazione di modelli o l'impostazione di un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="10627-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="10627-116">[Esecuzione di attività di revisore](performing-reviewer-tasks-agpm40.md), ad esempio la revisione delle impostazioni e il confronto degli oggetti Criteri di lavoro</span><span class="sxs-lookup"><span data-stu-id="10627-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="10627-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="10627-117">Additional considerations</span></span>

<span data-ttu-id="10627-118">Per impostazione predefinita, il ruolo amministratore Advanced Group Policy Management ha il controllo completo, tutte le autorizzazioni per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="10627-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="10627-119">Contenuto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="10627-119">List Contents</span></span>

-   <span data-ttu-id="10627-120">Impostazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="10627-120">Read Settings</span></span>

-   <span data-ttu-id="10627-121">Modificare le impostazioni</span><span class="sxs-lookup"><span data-stu-id="10627-121">Edit Settings</span></span>

-   <span data-ttu-id="10627-122">Creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="10627-122">Create GPO</span></span>

-   <span data-ttu-id="10627-123">Distribuire un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="10627-123">Deploy GPO</span></span>

-   <span data-ttu-id="10627-124">Elimina GPO</span><span class="sxs-lookup"><span data-stu-id="10627-124">Delete GPO</span></span>

-   <span data-ttu-id="10627-125">Esporta GPO</span><span class="sxs-lookup"><span data-stu-id="10627-125">Export GPO</span></span>

-   <span data-ttu-id="10627-126">Importa oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="10627-126">Import GPO</span></span>

-   <span data-ttu-id="10627-127">Creare un modello</span><span class="sxs-lookup"><span data-stu-id="10627-127">Create Template</span></span>

-   <span data-ttu-id="10627-128">Opzioni di modifica</span><span class="sxs-lookup"><span data-stu-id="10627-128">Modify Options</span></span>

-   <span data-ttu-id="10627-129">Modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="10627-129">Modify Security</span></span>

<span data-ttu-id="10627-130">Le autorizzazioni **modifica opzioni** e **modifica sicurezza** sono univoche per il ruolo di amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="10627-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





