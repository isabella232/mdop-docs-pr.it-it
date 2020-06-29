---
title: Attività del responsabile approvazione
description: Attività del responsabile approvazione
author: dansimp
ms.assetid: 9f711824-191b-4b4b-a1c6-a3b2116006a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e4a848608a3be1dbb0632f0145b4fc1d1bc631
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820475"
---
# <span data-ttu-id="300fc-103">Attività del responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="300fc-103">Performing Approver Tasks</span></span>


<span data-ttu-id="300fc-104">Un responsabile approvazione è una persona autorizzata da un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per creare, distribuire ed eliminare oggetti Criteri di gruppo e per approvare o rifiutare le richieste (in genere dagli editor) per creare, distribuire o eliminare GPO.</span><span class="sxs-lookup"><span data-stu-id="300fc-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="300fc-105">**Importante**  Verificare di essere connessi all'archivio centrale per gli oggetti Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="300fc-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="300fc-106">Per altre informazioni, vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="300fc-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

 

-   [<span data-ttu-id="300fc-107">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="300fc-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm30ops.md)

-   [<span data-ttu-id="300fc-108">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="300fc-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

-   [<span data-ttu-id="300fc-109">Archiviare un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="300fc-109">Check In a GPO</span></span>](check-in-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="300fc-110">Distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="300fc-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="300fc-111">Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="300fc-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="300fc-112">Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="300fc-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

<span data-ttu-id="300fc-113">**Nota**  Prima di approvare un GPO, un responsabile approvazione dovrebbe rivedere le impostazioni dei criteri che contiene.</span><span class="sxs-lookup"><span data-stu-id="300fc-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="300fc-114">Il ruolo Approvatore include le autorizzazioni per il ruolo di revisore, in modo che un responsabile approvazione possa rivedere le impostazioni dei criteri e confrontare i GPO.</span><span class="sxs-lookup"><span data-stu-id="300fc-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="300fc-115">Per altre informazioni, vedere [esecuzione di attività di revisore](performing-reviewer-tasks-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="300fc-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md) for more information.</span></span>

 

### <span data-ttu-id="300fc-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="300fc-116">Additional considerations</span></span>

<span data-ttu-id="300fc-117">Per impostazione predefinita, per il ruolo di responsabile approvazione vengono fornite le autorizzazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="300fc-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="300fc-118">Contenuto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="300fc-118">List Contents</span></span>

-   <span data-ttu-id="300fc-119">Impostazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="300fc-119">Read Settings</span></span>

-   <span data-ttu-id="300fc-120">Creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="300fc-120">Create GPO</span></span>

-   <span data-ttu-id="300fc-121">Distribuire un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="300fc-121">Deploy GPO</span></span>

-   <span data-ttu-id="300fc-122">Elimina GPO</span><span class="sxs-lookup"><span data-stu-id="300fc-122">Delete GPO</span></span>

<span data-ttu-id="300fc-123">Inoltre, un responsabile approvazione ha il controllo completo sugli oggetti GPO che ha creato o controllato.</span><span class="sxs-lookup"><span data-stu-id="300fc-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





