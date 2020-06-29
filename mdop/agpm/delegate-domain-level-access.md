---
title: Delegare l'accesso a livello di dominio
description: Delegare l'accesso a livello di dominio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820996"
---
# <span data-ttu-id="4c816-103">Delegare l'accesso a livello di dominio</span><span class="sxs-lookup"><span data-stu-id="4c816-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="4c816-104">Configurare la delega per l'ambiente in modo che gli amministratori dei criteri di gruppo abbiano l'accesso e il controllo appropriati degli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4c816-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="4c816-105">È possibile applicare le autorizzazioni di previsione per rendere più efficienti le operazioni di gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4c816-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="4c816-106">È possibile concedere le autorizzazioni in modo che soddisfi le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="4c816-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="4c816-107">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="4c816-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="4c816-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="4c816-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4c816-109">Per delegare l'accesso in modo che utenti e gruppi dispongano delle autorizzazioni appropriate per tutti i GPO in un dominio</span><span class="sxs-lookup"><span data-stu-id="4c816-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="4c816-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="4c816-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4c816-111">Fare clic sulla scheda **delega del dominio** , quindi fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="4c816-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="4c816-112">Nella finestra di dialogo **autorizzazioni** fare clic sulla casella di controllo relativa a ogni ruolo da assegnare a un singolo utente e quindi fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="4c816-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="4c816-113">**Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.</span><span class="sxs-lookup"><span data-stu-id="4c816-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="4c816-114">Nella finestra di dialogo **impostazioni di sicurezza avanzate** selezionare un amministratore di criteri di gruppo e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="4c816-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="4c816-115">Per **applica su**, selezionare **questo oggetto e gli oggetti annidati**, configurare le autorizzazioni speciali oltre ai ruoli di Advanced Group Policy Management, quindi fare clic su **OK** nella finestra di dialogo **immissione** delle **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="4c816-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="4c816-116">Nella finestra di dialogo **impostazioni di sicurezza avanzate** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c816-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="4c816-117">Nella finestra di dialogo **autorizzazioni** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c816-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="4c816-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4c816-118">Additional considerations</span></span>

-   <span data-ttu-id="4c816-119">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="4c816-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4c816-120">In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="4c816-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="4c816-121">Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="4c816-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="4c816-122">In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="4c816-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="4c816-123">Imposta l'autorizzazione da applicare a **questo oggetto e agli oggetti annidati**.</span><span class="sxs-lookup"><span data-stu-id="4c816-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="4c816-124">Le altre autorizzazioni devono essere delegate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="4c816-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="4c816-125">Agli editori deve essere concessa l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software Policy Group.</span><span class="sxs-lookup"><span data-stu-id="4c816-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="4c816-126">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="4c816-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="4c816-127">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="4c816-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="4c816-128">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="4c816-128">Additional references</span></span>

-   [<span data-ttu-id="4c816-129">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="4c816-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





