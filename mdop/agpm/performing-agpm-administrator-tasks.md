---
title: Attività di amministrazione per Gestione avanzata Criteri di gruppo
description: Attività di amministrazione per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820476"
---
# <span data-ttu-id="72b1a-103">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="72b1a-104">Un amministratore Advanced Group Policy Management (controllo completo) configura le opzioni a livello di dominio e delega le autorizzazioni per i responsabili approvazione, gli editor, i revisori e altri amministratori della gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="72b1a-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="72b1a-105">Per impostazione predefinita, un amministratore della Advanced Group Policy Management è un utente con controllo completo (tutte le autorizzazioni avanzate di gestione dei criteri di gruppo \ [Advanced Group Policy Manager \]) e pertanto può eseguire anche attività associate a qualsiasi ruolo.</span><span class="sxs-lookup"><span data-stu-id="72b1a-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="72b1a-106">In un ambiente in cui più persone sviluppano oggetti Criteri di gruppo, è possibile scegliere se tutti gli utenti avanzati di gestione dei criteri di gruppo eseguono le stesse attività e hanno lo stesso livello di accesso o se gli amministratori della tecnologia avanzata delegano le autorizzazioni agli editor che apportano modifiche a GPO e agli approvatori che distribuiscono GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="72b1a-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="72b1a-107">Gli amministratori della gestione avanzata possono configurare le autorizzazioni per soddisfare le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="72b1a-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="72b1a-108">Configurare la connessione al server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="72b1a-109">Configurare la notifica di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="72b1a-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="72b1a-110">Delegare l'accesso a livello di dominio</span><span class="sxs-lookup"><span data-stu-id="72b1a-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="72b1a-111">Delegare l'accesso a un singolo oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="72b1a-112">Configurare registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="72b1a-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="72b1a-113">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="72b1a-114">Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="72b1a-115">Modificare il percorso di archiviazione</span><span class="sxs-lookup"><span data-stu-id="72b1a-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="72b1a-116">Modificare l'account del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="72b1a-117">Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="72b1a-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="72b1a-118">Inoltre, poiché il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli, un amministratore della Advanced Group Policy Management può eseguire le attività normalmente associate a qualsiasi altro ruolo.</span><span class="sxs-lookup"><span data-stu-id="72b1a-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="72b1a-119">[Esecuzione di attività di approvazione](performing-approver-tasks.md), ad esempio la creazione, la distribuzione o l'eliminazione di GPO</span><span class="sxs-lookup"><span data-stu-id="72b1a-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="72b1a-120">[Esecuzione di attività dell'editor](performing-editor-tasks.md), ad esempio la modifica, la ridenominazione, l'etichettatura o l'importazione di GPO, la creazione di modelli o l'impostazione di un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="72b1a-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="72b1a-121">[Esecuzione di attività di revisore](performing-reviewer-tasks.md), ad esempio la revisione delle impostazioni e il confronto degli oggetti Criteri di lavoro</span><span class="sxs-lookup"><span data-stu-id="72b1a-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="72b1a-122">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="72b1a-122">Additional considerations</span></span>

<span data-ttu-id="72b1a-123">Per impostazione predefinita, il ruolo amministratore Advanced Group Policy Management ha il controllo completo, tutte le autorizzazioni per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="72b1a-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="72b1a-124">Contenuto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="72b1a-124">List Contents</span></span>

-   <span data-ttu-id="72b1a-125">Impostazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="72b1a-125">Read Settings</span></span>

-   <span data-ttu-id="72b1a-126">Modificare le impostazioni</span><span class="sxs-lookup"><span data-stu-id="72b1a-126">Edit Settings</span></span>

-   <span data-ttu-id="72b1a-127">Creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="72b1a-127">Create GPO</span></span>

-   <span data-ttu-id="72b1a-128">Distribuire un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="72b1a-128">Deploy GPO</span></span>

-   <span data-ttu-id="72b1a-129">Elimina GPO</span><span class="sxs-lookup"><span data-stu-id="72b1a-129">Delete GPO</span></span>

-   <span data-ttu-id="72b1a-130">Opzioni di modifica</span><span class="sxs-lookup"><span data-stu-id="72b1a-130">Modify Options</span></span>

-   <span data-ttu-id="72b1a-131">Modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="72b1a-131">Modify Security</span></span>

-   <span data-ttu-id="72b1a-132">Creare un modello</span><span class="sxs-lookup"><span data-stu-id="72b1a-132">Create Template</span></span>

<span data-ttu-id="72b1a-133">Le autorizzazioni **modifica opzioni** e **modifica sicurezza** sono univoche per il ruolo di amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="72b1a-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





