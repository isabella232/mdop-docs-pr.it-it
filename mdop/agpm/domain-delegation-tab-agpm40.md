---
title: Scheda Delega dominio
description: Scheda Delega dominio
author: dansimp
ms.assetid: 5be5841e-92fb-4af6-aa68-0ae50f8d5141
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5f3b5c3b7d8799b383ab48870fcccad0b0c3f73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818636"
---
# <span data-ttu-id="38e4a-103">Scheda Delega dominio</span><span class="sxs-lookup"><span data-stu-id="38e4a-103">Domain Delegation Tab</span></span>


<span data-ttu-id="38e4a-104">La scheda **delega del dominio** nel riquadro **Cambia controllo** fornisce un elenco di amministratori dei criteri di gruppo con accesso a livello di dominio all'archivio e indica i ruoli di ognuno.</span><span class="sxs-lookup"><span data-stu-id="38e4a-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="38e4a-105">Questa scheda consente inoltre agli amministratori della gestione avanzata Criteri di amministrazione (controllo completo) di configurare le autorizzazioni a livello di dominio per editor, responsabili approvazione, revisori e altri amministratori della gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38e4a-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="38e4a-106">Nella scheda **delega del dominio** sono presenti due sezioni, ovvero la configurazione della notifica tramite posta elettronica e la delega basata sui ruoli per Advanced Group Policy Management a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="38e4a-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="38e4a-107">Configurazione della notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="38e4a-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="38e4a-108">La sezione notifica tramite posta elettronica di questa scheda identifica i responsabili approvazione che riceveranno una notifica quando le operazioni sono in sospeso in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="38e4a-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="38e4a-109">Impostazione</span><span class="sxs-lookup"><span data-stu-id="38e4a-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="38e4a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38e4a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="38e4a-111">Dall'indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="38e4a-111">From e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-112">L'alias Advanced Group Policy Management da cui viene inviata una notifica agli approvatori.</span><span class="sxs-lookup"><span data-stu-id="38e4a-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="38e4a-113">In un ambiente con più domini può essere lo stesso alias nell'ambiente o in un altro alias per ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="38e4a-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="38e4a-114">A indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="38e4a-114">To e-mail address</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-115">Elenco delimitato da virgole di indirizzi di posta elettronica degli approvatori a cui inviare la notifica</span><span class="sxs-lookup"><span data-stu-id="38e4a-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="38e4a-116">Server SMTP</span><span class="sxs-lookup"><span data-stu-id="38e4a-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-117">Nome del server di posta elettronica, ad esempio mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="38e4a-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="38e4a-118">Nome utente</span><span class="sxs-lookup"><span data-stu-id="38e4a-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-119">Un utente con accesso al server SMTP</span><span class="sxs-lookup"><span data-stu-id="38e4a-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="38e4a-120">Password</span><span class="sxs-lookup"><span data-stu-id="38e4a-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-121">Password dell'utente per l'autenticazione nel server SMTP</span><span class="sxs-lookup"><span data-stu-id="38e4a-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="38e4a-122">Conferma password</span><span class="sxs-lookup"><span data-stu-id="38e4a-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-123">Confermare la password dell'utente</span><span class="sxs-lookup"><span data-stu-id="38e4a-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="38e4a-124">Delega basata sui ruoli a livello di dominio</span><span class="sxs-lookup"><span data-stu-id="38e4a-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="38e4a-125">La sezione delega basata sui ruoli di questa scheda Visualizza e consente a un amministratore Advanced Group Policy Management di delegare le autorizzazioni consentite, negate e ereditate per ogni gruppo e utente nel dominio con accesso all'archivio.</span><span class="sxs-lookup"><span data-stu-id="38e4a-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="38e4a-126">Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni a livello di dominio usando i ruoli Advanced Group Policy Management (editor, approvatore, revisore e amministratore della gestione avanzata) o una combinazione personalizzata di autorizzazioni per ogni amministratore dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38e4a-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="38e4a-127">Button</span><span class="sxs-lookup"><span data-stu-id="38e4a-127">Button</span></span></th>
<th align="left"><span data-ttu-id="38e4a-128">Effetto</span><span class="sxs-lookup"><span data-stu-id="38e4a-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="38e4a-129">Aggiungi</span><span class="sxs-lookup"><span data-stu-id="38e4a-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-130">Aggiungere una nuova voce al descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="38e4a-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="38e4a-131">Gli utenti o i gruppi di Active Directory possono essere aggiunti come amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38e4a-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="38e4a-132">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="38e4a-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-133">Rimuovere gli amministratori dei criteri di gruppo selezionati dall'elenco di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="38e4a-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="38e4a-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38e4a-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-135">Visualizzare le proprietà per gli amministratori dei criteri di gruppo selezionati.</span><span class="sxs-lookup"><span data-stu-id="38e4a-135">Display the properties for the selected Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="38e4a-136">Avanzate</span><span class="sxs-lookup"><span data-stu-id="38e4a-136">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="38e4a-137">Aprire l' <strong> Editor elenco di controllo di Access </strong> .</span><span class="sxs-lookup"><span data-stu-id="38e4a-137">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="38e4a-138">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="38e4a-138">Additional considerations</span></span>

-   <span data-ttu-id="38e4a-139">Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks-agpm40.md), esecuzione di attività dell' [Editor](performing-editor-tasks-agpm40.md), esecuzione di [attività di approvazione](performing-approver-tasks-agpm40.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="38e4a-139">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="38e4a-140">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="38e4a-140">Additional references</span></span>

-   [<span data-ttu-id="38e4a-141">Interfaccia utente: Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="38e4a-141">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="38e4a-142">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="38e4a-142">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





