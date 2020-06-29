---
title: Attività dell'editor
description: Attività dell'editor
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820406"
---
# <span data-ttu-id="ff6d4-103">Attività dell'editor</span><span class="sxs-lookup"><span data-stu-id="ff6d4-103">Performing Editor Tasks</span></span>


<span data-ttu-id="ff6d4-104">In Advanced Group Policy Management, un editor è una persona autorizzata da un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per modificare gli oggetti Criteri di gruppo e creare modelli di GPO.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="ff6d4-105">Inoltre, un editor può richiedere che venga creato, eliminato o ripristinato un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="ff6d4-106">Un responsabile approvazione deve approvare la richiesta per l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="ff6d4-107">Un editor può esportare un oggetto Criteri di campo in un file in modo che possa essere copiato in un dominio in un'altra foresta e importare un oggetto Criteri di stato copiato da un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="ff6d4-108">**Importante**  Verificare di essere connessi all'archivio centrale per gli oggetti Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="ff6d4-109">Per altre informazioni, vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ff6d4-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="ff6d4-110">Creazione o controllo di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="ff6d4-111">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="ff6d4-112">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="ff6d4-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="ff6d4-113">Richiedere la distribuzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="ff6d4-114">Creazione di un modello e impostazione di un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="ff6d4-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="ff6d4-115">Eliminazione o ripristino di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ff6d4-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="ff6d4-116">**Nota**  Poiché il ruolo dell'Editor include le autorizzazioni per il ruolo di revisore, un editor può anche rivedere le impostazioni e confrontare i GPO.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="ff6d4-117">Per altre informazioni, vedere [esecuzione di attività di revisore](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6d4-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="ff6d4-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ff6d4-118">Additional considerations</span></span>

<span data-ttu-id="ff6d4-119">Per impostazione predefinita, per il ruolo dell'editor vengono fornite le autorizzazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff6d4-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="ff6d4-120">Contenuto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="ff6d4-120">List Contents</span></span>

-   <span data-ttu-id="ff6d4-121">Impostazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="ff6d4-121">Read Settings</span></span>

-   <span data-ttu-id="ff6d4-122">Modificare le impostazioni</span><span class="sxs-lookup"><span data-stu-id="ff6d4-122">Edit Settings</span></span>

-   <span data-ttu-id="ff6d4-123">Esporta GPO</span><span class="sxs-lookup"><span data-stu-id="ff6d4-123">Export GPO</span></span>

-   <span data-ttu-id="ff6d4-124">Importa oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="ff6d4-124">Import GPO</span></span>

-   <span data-ttu-id="ff6d4-125">Creare un modello</span><span class="sxs-lookup"><span data-stu-id="ff6d4-125">Create Template</span></span>

 

 





