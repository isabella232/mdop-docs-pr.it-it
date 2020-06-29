---
title: Delegare l'accesso all'ambiente di produzione
description: Delegare l'accesso all'ambiente di produzione
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818726"
---
# <span data-ttu-id="6d0c3-103">Delegare l'accesso all'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="6d0c3-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="6d0c3-104">In Advanced Group Policy Management, è possibile modificare l'accesso agli oggetti Criteri di gruppo nell'ambiente di produzione del dominio, sostituendo eventuali autorizzazioni esistenti per tali oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-104">In Advanced Group Policy Management (AGPM), you can change access to Group Policy Objects (GPOs) in the production environment of the domain, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="6d0c3-105">È possibile configurare le autorizzazioni a livello di dominio per consentire o impedire agli utenti di modificare, eliminare o modificare la sicurezza degli oggetti Criteri di gruppo nell'ambiente di produzione quando non usano la cartella di **controllo delle modifiche** nella console di gestione dei criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="6d0c3-106">Nota</span><span class="sxs-lookup"><span data-stu-id="6d0c3-106">Note</span></span>**  
-   <span data-ttu-id="6d0c3-107">La modifica del modo in cui l'accesso all'ambiente di produzione viene delegata non influisce sulla possibilità degli utenti di collegare GPO.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-107">Changing how access to the production environment is delegated does not affect users' ability to link GPOs.</span></span>

-   <span data-ttu-id="6d0c3-108">Quando gli oggetti Criteri di controllo vengono controllati o distribuiti, è possibile accedere ad altri account, ad eccezione di quelli con autorizzazioni di **lettura** e **applicazione** .</span><span class="sxs-lookup"><span data-stu-id="6d0c3-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="6d0c3-109">Per completare questa procedura è necessario un account utente con il ruolo di amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-109">A user account that has either the role of AGPM Administrator (Full Control) or the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="6d0c3-110">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="6d0c3-111">Per cambiare l'accesso a GPO nell'ambiente di produzione del dominio</span><span class="sxs-lookup"><span data-stu-id="6d0c3-111">To change access to GPOs in the production environment of the domain</span></span>**

1.  <span data-ttu-id="6d0c3-112">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6d0c3-113">Fare clic sulla scheda **Delega produzione** .</span><span class="sxs-lookup"><span data-stu-id="6d0c3-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="6d0c3-114">Per aggiungere le autorizzazioni per un utente o un gruppo che non ha accesso all'ambiente di produzione oppure per sostituire le autorizzazioni per un utente o un gruppo a cui è associato l'accesso:</span><span class="sxs-lookup"><span data-stu-id="6d0c3-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="6d0c3-115">Fare clic su **Aggiungi**, selezionare un utente o un gruppo e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="6d0c3-116">Selezionare le autorizzazioni per delegare l'utente o il gruppo per l'ambiente di produzione e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="6d0c3-117">Per rimuovere tutte le autorizzazioni per l'ambiente di produzione per un utente o un gruppo, selezionare l'utente o il gruppo, fare clic su **Rimuovi**e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="6d0c3-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="6d0c3-118">Additional considerations</span></span>

-   <span data-ttu-id="6d0c3-119">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="6d0c3-120">In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="6d0c3-121">Le autorizzazioni per l'account del servizio Advanced Group Policy Management non possono essere modificate nella scheda **Delega produzione** .</span><span class="sxs-lookup"><span data-stu-id="6d0c3-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="6d0c3-122">Per impostazione predefinita, gli account seguenti dispongono delle autorizzazioni per i GPO nell'ambiente di produzione:</span><span class="sxs-lookup"><span data-stu-id="6d0c3-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6d0c3-123">Account</span><span class="sxs-lookup"><span data-stu-id="6d0c3-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="6d0c3-124">Autorizzazioni predefinite per gli oggetti Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="6d0c3-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6d0c3-125">&lt;Account del servizio Advanced Group Policy Management&gt;</span><span class="sxs-lookup"><span data-stu-id="6d0c3-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-126">Modificare le impostazioni, eliminare, modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="6d0c3-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6d0c3-127">Utenti autenticati</span><span class="sxs-lookup"><span data-stu-id="6d0c3-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-128">Leggere, applicare</span><span class="sxs-lookup"><span data-stu-id="6d0c3-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6d0c3-129">Amministratori di dominio</span><span class="sxs-lookup"><span data-stu-id="6d0c3-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-130">Modificare le impostazioni, eliminare, modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="6d0c3-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6d0c3-131">Amministratori aziendali</span><span class="sxs-lookup"><span data-stu-id="6d0c3-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-132">Modificare le impostazioni, eliminare, modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="6d0c3-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6d0c3-133">Controller di dominio aziendale</span><span class="sxs-lookup"><span data-stu-id="6d0c3-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-134">Read</span><span class="sxs-lookup"><span data-stu-id="6d0c3-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6d0c3-135">Sistema</span><span class="sxs-lookup"><span data-stu-id="6d0c3-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6d0c3-136">Modificare le impostazioni, eliminare, modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="6d0c3-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="6d0c3-137">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="6d0c3-138">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6d0c3-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="6d0c3-139">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="6d0c3-139">Additional references</span></span>

-   [<span data-ttu-id="6d0c3-140">Configurazione di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6d0c3-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





