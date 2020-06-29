---
title: Elenco di controllo per creare, modificare e distribuire un GPO
description: Elenco di controllo per creare, modificare e distribuire un GPO
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819115"
---
# <span data-ttu-id="79ae8-103">Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="79ae8-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="79ae8-104">In un ambiente in cui più persone modificano gli oggetti Criteri di gruppo (GPO), un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori, sia come gruppi che come singoli.</span><span class="sxs-lookup"><span data-stu-id="79ae8-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="79ae8-105">Di seguito è riportato un processo di sviluppo GPO tipico per un editor e un responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="79ae8-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79ae8-106">Attività</span><span class="sxs-lookup"><span data-stu-id="79ae8-106">Task</span></span></th>
<th align="left"><span data-ttu-id="79ae8-107">Riferimento</span><span class="sxs-lookup"><span data-stu-id="79ae8-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79ae8-108">Editor richiede la creazione di un nuovo GPO o un responsabile dell'approvazione crea un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="79ae8-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="79ae8-109">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="79ae8-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="79ae8-110">Creare un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="79ae8-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79ae8-111">L'approvatore approva la creazione del GPO se richiesto da un editor.</span><span class="sxs-lookup"><span data-stu-id="79ae8-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="79ae8-112">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="79ae8-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79ae8-113">Editor estrae una copia del GPO dall'archivio, quindi nessun altro può modificare l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="79ae8-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="79ae8-114">Editor apporta modifiche al GPO e quindi controlla l'oggetto Criteri di controllo modificato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="79ae8-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="79ae8-115">Modificare un oggetto Criteri di gruppo offline</span><span class="sxs-lookup"><span data-stu-id="79ae8-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79ae8-116">Editor richiede la distribuzione del GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="79ae8-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="79ae8-117">Richiedere la distribuzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="79ae8-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79ae8-118">I revisori, ad esempio i responsabili approvazione o gli editori, analizzano l'oggetto Criteri di tipo.</span><span class="sxs-lookup"><span data-stu-id="79ae8-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="79ae8-119">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="79ae8-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79ae8-120">L'approvatore approva e distribuisce il GPO nell'ambiente di produzione o rifiuta il GPO.</span><span class="sxs-lookup"><span data-stu-id="79ae8-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="79ae8-121">Approvare o rifiutare un'azione in sospeso</span><span class="sxs-lookup"><span data-stu-id="79ae8-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





