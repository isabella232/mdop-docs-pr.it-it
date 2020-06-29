---
title: Delegare l'accesso a livello di dominio all'archivio
description: Delegare l'accesso a livello di dominio all'archivio
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818725"
---
# <span data-ttu-id="58c80-103">Delegare l'accesso a livello di dominio all'archivio</span><span class="sxs-lookup"><span data-stu-id="58c80-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="58c80-104">Configurare la delega per l'ambiente in modo che gli amministratori dei criteri di gruppo abbiano l'accesso e il controllo appropriati degli oggetti Criteri di gruppo nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="58c80-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="58c80-105">Per rendere più efficiente l'operazione, è possibile applicare le autorizzazioni di previsione.</span><span class="sxs-lookup"><span data-stu-id="58c80-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="58c80-106">È possibile concedere le autorizzazioni in modo che soddisfi le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="58c80-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="58c80-107">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="58c80-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="58c80-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="58c80-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="58c80-109">Per delegare l'accesso in modo che gli utenti e i gruppi dispongano delle autorizzazioni appropriate per tutti i GPO in un dominio</span><span class="sxs-lookup"><span data-stu-id="58c80-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="58c80-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="58c80-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="58c80-111">Fare clic sulla scheda **delega dominio** e configurare l'accesso a tutti i GPO nel dominio:</span><span class="sxs-lookup"><span data-stu-id="58c80-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="58c80-112">Per aggiungere l'accesso per un utente o un gruppo, fare clic sul pulsante **Aggiungi** , selezionare l'utente o il gruppo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="58c80-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="58c80-113">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare un ruolo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="58c80-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="58c80-114">Per rimuovere l'accesso per un utente o un gruppo, selezionare l'utente o il gruppo e fare clic sul pulsante **Rimuovi** .</span><span class="sxs-lookup"><span data-stu-id="58c80-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="58c80-115">Per modificare i ruoli e le autorizzazioni delegati a un utente o un gruppo, selezionare fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="58c80-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="58c80-116">Nella finestra di dialogo **autorizzazioni** selezionare l'utente o il gruppo, selezionare la casella di controllo relativa a ogni ruolo da assegnare all'utente o al gruppo e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="58c80-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="58c80-117">**Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.</span><span class="sxs-lookup"><span data-stu-id="58c80-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="58c80-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="58c80-118">Additional considerations</span></span>

-   <span data-ttu-id="58c80-119">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="58c80-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="58c80-120">In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="58c80-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="58c80-121">Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="58c80-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="58c80-122">In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="58c80-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="58c80-123">Le altre autorizzazioni devono essere delegate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="58c80-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="58c80-124">Agli editori deve essere concessa l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software Policy Group.</span><span class="sxs-lookup"><span data-stu-id="58c80-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="58c80-125">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="58c80-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="58c80-126">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="58c80-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="58c80-127">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="58c80-127">Additional references</span></span>

-   [<span data-ttu-id="58c80-128">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="58c80-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





