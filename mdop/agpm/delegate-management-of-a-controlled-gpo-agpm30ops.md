---
title: Delegare la gestione di un oggetto Criteri di gruppo controllato
description: Delegare la gestione di un oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818716"
---
# <span data-ttu-id="cee5b-103">Delegare la gestione di un oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="cee5b-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="cee5b-104">Un responsabile approvazione può delegare la gestione di un oggetto Criteri di gruppo controllato creato dall'approvatore.</span><span class="sxs-lookup"><span data-stu-id="cee5b-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="cee5b-105">Come un amministratore Advanced Group Policy Management (controllo completo), l'approvatore può delegare l'accesso a un oggetto Criteri di questo tipo in modo che gli editor selezionati possano modificarlo, i revisori possono rivederlo e altri responsabili approvazione possono approvarlo.</span><span class="sxs-lookup"><span data-stu-id="cee5b-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="cee5b-106">Per impostazione predefinita, un responsabile approvazione non può delegare l'accesso ai GPO creati da un altro amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="cee5b-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="cee5b-107">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cee5b-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="cee5b-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="cee5b-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="cee5b-109">Per delegare la gestione di un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="cee5b-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="cee5b-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="cee5b-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="cee5b-111">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare:</span><span class="sxs-lookup"><span data-stu-id="cee5b-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="cee5b-112">Per aggiungere l'accesso per un utente o un gruppo, fare clic sul pulsante **Aggiungi** , selezionare l'utente o il gruppo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee5b-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="cee5b-113">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare un ruolo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee5b-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="cee5b-114">Per rimuovere l'accesso per un utente o un gruppo, selezionare l'utente o il gruppo e quindi fare clic sul pulsante **Rimuovi** .</span><span class="sxs-lookup"><span data-stu-id="cee5b-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="cee5b-115">**Nota**  Se un utente o un gruppo eredita l'accesso a livello di dominio, il pulsante **Rimuovi** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="cee5b-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="cee5b-116">È possibile modificare l'accesso a livello di dominio nella scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="cee5b-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="cee5b-117">Per modificare i ruoli e le autorizzazioni delegati a un utente o un gruppo, fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="cee5b-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="cee5b-118">Nella finestra di dialogo **autorizzazioni** selezionare l'utente o il gruppo, selezionare la casella di controllo relativa a ogni ruolo da assegnare all'utente o al gruppo e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee5b-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="cee5b-119">**Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.</span><span class="sxs-lookup"><span data-stu-id="cee5b-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="cee5b-120">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="cee5b-120">Additional considerations</span></span>

-   <span data-ttu-id="cee5b-121">Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="cee5b-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="cee5b-122">In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.</span><span class="sxs-lookup"><span data-stu-id="cee5b-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="cee5b-123">Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="cee5b-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="cee5b-124">In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cee5b-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="cee5b-125">Le altre autorizzazioni devono essere delegate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="cee5b-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="cee5b-126">Gli editor devono avere l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software criteri di Group.</span><span class="sxs-lookup"><span data-stu-id="cee5b-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="cee5b-127">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="cee5b-127">Additional references</span></span>

-   [<span data-ttu-id="cee5b-128">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cee5b-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





