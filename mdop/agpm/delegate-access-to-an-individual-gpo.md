---
title: Delegare l'accesso a un singolo oggetto Criteri di gruppo
description: Delegare l'accesso a un singolo oggetto Criteri di gruppo
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818735"
---
# <span data-ttu-id="e389a-103">Delegare l'accesso a un singolo oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e389a-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="e389a-104">In qualità di amministratore Advanced Group Policy Management (controllo completo), puoi delegare la gestione di un oggetto Criteri di gruppo controllato, quindi i gruppi e gli editori selezionati possono modificarlo, i revisori possono rivederlo e i responsabili approvazione possono approvarlo.</span><span class="sxs-lookup"><span data-stu-id="e389a-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="e389a-105">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di gruppi di criteri avanzati.</span><span class="sxs-lookup"><span data-stu-id="e389a-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e389a-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e389a-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e389a-107">Per delegare la gestione di un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="e389a-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="e389a-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="e389a-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e389a-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare.</span><span class="sxs-lookup"><span data-stu-id="e389a-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="e389a-110">Fare clic sul pulsante **Aggiungi** , selezionare gli utenti o i gruppi a cui consentire l'accesso e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e389a-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="e389a-111">Per personalizzare le autorizzazioni per ogni utente o gruppo, fare clic sul pulsante **Avanzate** nella scheda **Sommario** e selezionare autorizzazioni ruolo per consentire o negare.</span><span class="sxs-lookup"><span data-stu-id="e389a-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="e389a-112">Per un controllo più dettagliato, fare clic su **Avanzate** nella finestra di dialogo **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="e389a-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="e389a-113">Fare clic su **applica**e quindi su **OK** nella finestra di dialogo **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="e389a-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="e389a-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e389a-114">Additional considerations</span></span>

-   <span data-ttu-id="e389a-115">Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="e389a-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e389a-116">In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.</span><span class="sxs-lookup"><span data-stu-id="e389a-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="e389a-117">Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="e389a-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="e389a-118">In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e389a-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="e389a-119">Imposta l'autorizzazione da applicare a **questo oggetto e agli oggetti annidati**.</span><span class="sxs-lookup"><span data-stu-id="e389a-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="e389a-120">Le altre autorizzazioni devono essere delegate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="e389a-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="e389a-121">Gli editor devono avere l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software criteri di Group.</span><span class="sxs-lookup"><span data-stu-id="e389a-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="e389a-122">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="e389a-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="e389a-123">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e389a-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="e389a-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="e389a-124">Additional references</span></span>

-   [<span data-ttu-id="e389a-125">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e389a-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





