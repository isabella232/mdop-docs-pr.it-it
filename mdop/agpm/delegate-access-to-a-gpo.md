---
title: Delegare l'accesso a un oggetto Criteri di gruppo
description: Delegare l'accesso a un oggetto Criteri di gruppo
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818785"
---
# <span data-ttu-id="30d26-103">Delegare l'accesso a un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="30d26-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="30d26-104">Un responsabile approvazione può delegare la gestione di un oggetto Criteri di gruppo controllato **creato dall'approvatore**.</span><span class="sxs-lookup"><span data-stu-id="30d26-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="30d26-105">Come un amministratore Advanced Group Policy Management (controllo completo), l'approvatore può delegare l'accesso a un oggetto Criteri di questo tipo, quindi gli editor selezionati possono modificarlo, i revisori possono rivederlo e altri responsabili approvazione possono approvarlo.</span><span class="sxs-lookup"><span data-stu-id="30d26-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="30d26-106">Per impostazione predefinita, un responsabile approvazione non può delegare l'accesso ai GPO creati da un altro amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="30d26-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="30d26-107">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di gruppi di criteri avanzati.</span><span class="sxs-lookup"><span data-stu-id="30d26-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="30d26-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="30d26-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="30d26-109">Per delegare la gestione di un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="30d26-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="30d26-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="30d26-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="30d26-111">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare.</span><span class="sxs-lookup"><span data-stu-id="30d26-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="30d26-112">Fare clic sul pulsante **Aggiungi** , selezionare gli utenti o i gruppi a cui consentire l'accesso e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="30d26-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="30d26-113">Per personalizzare le autorizzazioni per ogni, fare clic sul pulsante **Avanzate** nella scheda **Sommario** e selezionare autorizzazioni ruolo per consentire o negare.</span><span class="sxs-lookup"><span data-stu-id="30d26-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="30d26-114">Per un controllo più dettagliato, fare clic su **Avanzate** nella finestra di dialogo **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="30d26-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="30d26-115">Fare clic su **applica**e quindi su **OK** nella finestra di dialogo **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="30d26-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="30d26-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="30d26-116">Additional considerations</span></span>

-   <span data-ttu-id="30d26-117">Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="30d26-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="30d26-118">In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.</span><span class="sxs-lookup"><span data-stu-id="30d26-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="30d26-119">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="30d26-119">Additional references</span></span>

-   [<span data-ttu-id="30d26-120">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="30d26-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





