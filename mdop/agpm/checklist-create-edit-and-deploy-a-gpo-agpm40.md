---
title: Elenco di controllo per creare, modificare e distribuire un GPO
description: Elenco di controllo per creare, modificare e distribuire un GPO
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819105"
---
# <span data-ttu-id="884a5-103">Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="884a5-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="884a5-104">In un ambiente in cui più persone modificano gli oggetti Criteri di gruppo tramite Advanced Group Policy Management (Advanced criteri di gruppo), un amministratore della gestione avanzata (controllo completo) delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori sia come gruppi che come singoli.</span><span class="sxs-lookup"><span data-stu-id="884a5-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="884a5-105">Di seguito è riportato un processo di sviluppo GPO tipico per un editor e un responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="884a5-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="884a5-106">Attività</span><span class="sxs-lookup"><span data-stu-id="884a5-106">Task</span></span></th>
<th align="left"><span data-ttu-id="884a5-107">Riferimento</span><span class="sxs-lookup"><span data-stu-id="884a5-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="884a5-108">Editor richiede la creazione di un nuovo oggetto Criteri di stato o un responsabile dell'approvazione crea un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="884a5-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="884a5-109">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="884a5-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="884a5-110">Creare un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="884a5-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="884a5-111">L'approvatore approva la creazione del GPO se richiesto da un editor.</span><span class="sxs-lookup"><span data-stu-id="884a5-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="884a5-112">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="884a5-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="884a5-113">Editor estrae una copia del GPO dall'archivio in modo che nessun altro possa modificare l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="884a5-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="884a5-114">Editor apporta modifiche al GPO e quindi controlla l'oggetto Criteri di controllo modificato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="884a5-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="884a5-115">Modificare un oggetto Criteri di gruppo offline</span><span class="sxs-lookup"><span data-stu-id="884a5-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="884a5-116">Se si sviluppa in una foresta di test, editor Esporta il GPO in un file, trasferisce il file nella foresta di produzione e importa il file.</span><span class="sxs-lookup"><span data-stu-id="884a5-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="884a5-117">Inoltre, un editor può collegare l'oggetto Criteri di gruppo a un'unità organizzativa che contiene computer e utenti di test.</span><span class="sxs-lookup"><span data-stu-id="884a5-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="884a5-118">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="884a5-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="884a5-119">Editor richiede la distribuzione del GPO nell'ambiente di produzione del dominio.</span><span class="sxs-lookup"><span data-stu-id="884a5-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="884a5-120">Richiedere la distribuzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="884a5-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="884a5-121">I revisori, ad esempio i responsabili approvazione o gli editori, analizzano l'oggetto Criteri di tipo.</span><span class="sxs-lookup"><span data-stu-id="884a5-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="884a5-122">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="884a5-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="884a5-123">L'approvatore approva e distribuisce il GPO nell'ambiente di produzione del dominio o rifiuta il GPO.</span><span class="sxs-lookup"><span data-stu-id="884a5-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="884a5-124">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="884a5-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="884a5-125">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="884a5-125">Additional references</span></span>

[<span data-ttu-id="884a5-126">Gestione avanzata Criteri di gruppo 4.0</span><span class="sxs-lookup"><span data-stu-id="884a5-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





