---
title: Configurare la connessione al server di Gestione avanzata Criteri di gruppo
description: Configurare la connessione al server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818915"
---
# <span data-ttu-id="0e0f7-103">Configurare la connessione al server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="0e0f7-104">Advanced Group Policy Management consente di archiviare tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato in un archivio centrale, in modo che gli amministratori dei criteri di gruppo possano visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni GPO.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="0e0f7-105">Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie per la gestione dei criteri di raggruppamento avanzati è necessario per completare queste procedure per la configurazione centralizzata dei percorsi di archiviazione per tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="0e0f7-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="0e0f7-107">Configurazione della connessione del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="0e0f7-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="0e0f7-108">In qualità di amministratore Advanced Group Policy Management (controllo completo), è possibile verificare che tutti gli amministratori dei criteri di gruppo si connettano allo stesso server Advanced Group Policy configurando centralmente l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="0e0f7-109">Se l'ambiente richiede server Advanced Group Policy Management separati per alcuni o tutti i domini, configurare tali server aggiuntivi per Advanced Group Policy Management come eccezioni per l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="0e0f7-110">Se non si configurano in modo centralizzato le connessioni del server Advanced Group Policy Management, ogni amministratore dei criteri di gruppo deve configurare manualmente il server Advanced Group Policy Management da visualizzare per ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="0e0f7-111">Configurare un server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="0e0f7-112">Configurare altri server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="0e0f7-113">Configurare manualmente un server Advanced Group Policy Management per l'account</span><span class="sxs-lookup"><span data-stu-id="0e0f7-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="0e0f7-114">Per configurare un server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="0e0f7-115">Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="0e0f7-116">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="0e0f7-117">Nell' **Editor oggetti Criteri di gruppo**fare clic su **Configurazione utente**, **modelli amministrativi**e **componenti di Windows**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="0e0f7-118">Se **Advanced Group Policy Management** non è elencato in **componenti di Windows**:</span><span class="sxs-lookup"><span data-stu-id="0e0f7-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="0e0f7-119">Fare clic con il pulsante destro del mouse su **modelli amministrativi** e scegliere **Aggiungi/Rimuovi modelli**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="0e0f7-120">Fare clic su **Aggiungi**, selezionare **Advanced Group Policy Management. admx** o **Advanced Group Policy Management. adm**, fare clic su **Apri**e quindi su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="0e0f7-121">In **componenti di Windows**fare doppio clic su **Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="0e0f7-122">Nel riquadro dei dettagli fare doppio clic su **server Advanced Group Policy Management (tutti i domini)**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="0e0f7-123">Nella finestra delle **proprietà del server Advanced Group Policy Management (tutti i domini)** selezionare la casella di controllo **abilitata** e digitare il nome completo del computer e la porta (ad esempio, server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="0e0f7-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="0e0f7-124">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-124">Click **OK**.</span></span> <span data-ttu-id="0e0f7-125">A meno che non si vogliano configurare altre connessioni del server Advanced Group Policy Management, chiudere l' **Editor oggetti Criteri di gruppo** e distribuire il GPO.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="0e0f7-126">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management è configurata per tutti gli amministratori dei criteri</span><span class="sxs-lookup"><span data-stu-id="0e0f7-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="0e0f7-127">Per configurare altri server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="0e0f7-128">Se non è stata configurata una connessione al server Advanced Group Policy Management, seguire la procedura precedente per configurare un server Advanced Group Policy Management per tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="0e0f7-129">Per configurare distinti server Advanced Group Policy Management per alcuni o tutti i domini (eseguendo l'override del server Advanced Group Policy Manager), nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="0e0f7-130">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="0e0f7-131">In **Configurazione utente** nell' **Editor oggetti Criteri di gruppo**fare doppio clic su **modelli amministrativi**, **componenti di Windows**e quindi **Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="0e0f7-132">Nel riquadro dei dettagli fare doppio clic su **server Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="0e0f7-133">Nella finestra delle **proprietà del server Advanced Group Policy Management** selezionare la casella di controllo **abilitata** e fare clic su **Mostra**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="0e0f7-134">Nella finestra **Mostra contenuto** :</span><span class="sxs-lookup"><span data-stu-id="0e0f7-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="0e0f7-135">Fai clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="0e0f7-136">Per **nome valore**Digitare il nome di dominio, ad esempio Server1.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="0e0f7-137">Per **valore**Digitare il nome del server Advanced Group Policy Management e la porta da usare per il dominio, ad esempio server2.contoso.com:4600, e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="0e0f7-138">(Per impostazione predefinita, il servizio Advanced Group Policy Management ascolta la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="0e0f7-139">Per usare una porta diversa, vedere [modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="0e0f7-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="0e0f7-140">Ripetere l'impostazione per ogni dominio che non usa il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="0e0f7-141">Fare clic su **OK** per chiudere le finestre **Mostra contenuto** e **proprietà del server Advanced Group Policy Management** .</span><span class="sxs-lookup"><span data-stu-id="0e0f7-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="0e0f7-142">Chiudere l' **Editor oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="0e0f7-143">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Quando si aggiornano i criteri di gruppo, le nuove connessioni del server Advanced Group Policy Management sono configurate per tutti gli amministratori dei criteri</span><span class="sxs-lookup"><span data-stu-id="0e0f7-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="0e0f7-144">Se la connessione al server Advanced Group Policy Management è stata configurata in modo centralizzato, l'opzione manualmente non è disponibile per tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="0e0f7-145">Per configurare manualmente il server Advanced Group Policy Management da visualizzare per l'account</span><span class="sxs-lookup"><span data-stu-id="0e0f7-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="0e0f7-146">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="0e0f7-147">Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .</span><span class="sxs-lookup"><span data-stu-id="0e0f7-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="0e0f7-148">Immettere il nome completo del computer per il server Advanced Group Policy Management che gestisce l'archivio usato per questo dominio, ad esempio server.contoso.com, e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600).</span><span class="sxs-lookup"><span data-stu-id="0e0f7-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="0e0f7-149">Fare clic su **applica**e quindi su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="0e0f7-150">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0e0f7-150">Additional considerations</span></span>

-   <span data-ttu-id="0e0f7-151">È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per eseguire le procedure per la configurazione centralizzata delle connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="0e0f7-152">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="0e0f7-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="0e0f7-153">Il server Advanced Group Policy Management selezionato determina quali GPO vengono visualizzati nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="0e0f7-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="0e0f7-154">Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="0e0f7-155">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione dell'accesso a GPO da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="0e0f7-156">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="0e0f7-157">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="0e0f7-157">Additional references</span></span>

-   [<span data-ttu-id="0e0f7-158">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0e0f7-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





