---
title: Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio
description: Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818766"
---
# <span data-ttu-id="66de8-103">Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio</span><span class="sxs-lookup"><span data-stu-id="66de8-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="66de8-104">In qualità di amministratore Advanced Group Policy Management (controllo completo), puoi delegare la gestione di un oggetto Criteri di gruppo controllato nell'archivio in modo che i gruppi e gli editori selezionati possano modificarlo, i revisori possono rivederlo e i responsabili approvazione possono approvarlo.</span><span class="sxs-lookup"><span data-stu-id="66de8-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="66de8-105">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="66de8-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="66de8-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="66de8-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="66de8-107">Per delegare la gestione di un oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="66de8-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="66de8-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="66de8-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="66de8-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare:</span><span class="sxs-lookup"><span data-stu-id="66de8-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="66de8-110">Per aggiungere l'accesso per un utente o un gruppo, fare clic sul pulsante **Aggiungi** , selezionare l'utente o il gruppo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="66de8-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="66de8-111">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare un ruolo e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="66de8-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="66de8-112">Per rimuovere l'accesso per un utente o un gruppo, selezionare l'utente o il gruppo e fare clic sul pulsante **Rimuovi** .</span><span class="sxs-lookup"><span data-stu-id="66de8-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="66de8-113">**Nota**  Se un utente o un gruppo eredita l'accesso a livello di dominio, il pulsante **Rimuovi** non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="66de8-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="66de8-114">È possibile modificare l'accesso a livello di dominio nella scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="66de8-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="66de8-115">Per modificare i ruoli e le autorizzazioni delegati a un utente o un gruppo, fare clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="66de8-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="66de8-116">Nella finestra di dialogo **autorizzazioni** selezionare l'utente o il gruppo, selezionare la casella di controllo relativa a ogni ruolo da assegnare all'utente o al gruppo, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="66de8-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="66de8-117">**Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.</span><span class="sxs-lookup"><span data-stu-id="66de8-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="66de8-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="66de8-118">Additional considerations</span></span>

-   <span data-ttu-id="66de8-119">Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="66de8-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="66de8-120">In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.</span><span class="sxs-lookup"><span data-stu-id="66de8-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="66de8-121">Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="66de8-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="66de8-122">In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="66de8-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="66de8-123">Le altre autorizzazioni devono essere delegate in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="66de8-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="66de8-124">Gli editor devono avere l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software criteri di Group.</span><span class="sxs-lookup"><span data-stu-id="66de8-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="66de8-125">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="66de8-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="66de8-126">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="66de8-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="66de8-127">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="66de8-127">Additional references</span></span>

-   [<span data-ttu-id="66de8-128">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="66de8-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 





