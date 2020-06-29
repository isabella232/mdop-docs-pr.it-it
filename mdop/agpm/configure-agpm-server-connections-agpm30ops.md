---
title: Configurare le connessioni server di Gestione avanzata Criteri di gruppo
description: Configurare le connessioni server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 6062b77b-2fd7-442c-ad1b-6f14419ebd5f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42f2ac4b219bed99db1ceae12859b992f4976db9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821186"
---
# <span data-ttu-id="ef504-103">Configurare le connessioni server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="ef504-104">Tutte le versioni di ogni oggetto Criteri di gruppo controllato sono archiviate in un archivio centrale, in modo che gli amministratori dei criteri di gruppo possano visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni GPO.</span><span class="sxs-lookup"><span data-stu-id="ef504-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="ef504-105">Un account utente con il ruolo Amministratore Gestione avanzata Criteri di gruppo (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management (Advanced Policy Manager) è necessario per completare queste procedure per la configurazione centralizzata dei percorsi di archiviazione per tutti gli amministratori dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ef504-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="ef504-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="ef504-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="ef504-107">Configurazione delle connessioni del server Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="ef504-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="ef504-108">In qualità di amministratore della gestione avanzata Criteri di gruppo, è possibile verificare che tutti gli amministratori dei criteri di raggruppamento si connettano allo stesso server Advanced Group Policy per la configurazione centralizzata.</span><span class="sxs-lookup"><span data-stu-id="ef504-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="ef504-109">Se l'ambiente richiede server Advanced Group Policy Management separati per alcuni o tutti i domini, configurare tali server aggiuntivi per Advanced Group Policy Management come eccezioni per l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ef504-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="ef504-110">Se non si configurano in modo centralizzato le connessioni del server Advanced Group Policy Management, ogni amministratore dei criteri di gruppo deve configurare manualmente il server Advanced Group Policy Management da visualizzare per ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="ef504-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="ef504-111">Configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="ef504-112">Configurare altre connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="ef504-113">Configurare manualmente una connessione al server Advanced Group Policy Management per l'account</span><span class="sxs-lookup"><span data-stu-id="ef504-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="ef504-114">Per configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="ef504-115">Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="ef504-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="ef504-116">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ef504-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="ef504-117">Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.</span><span class="sxs-lookup"><span data-stu-id="ef504-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="ef504-118">Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)**.</span><span class="sxs-lookup"><span data-stu-id="ef504-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="ef504-119">Nella finestra **Proprietà** selezionare la casella di controllo **abilitata** e digitare il nome completo del computer e la porta (ad esempio, server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="ef504-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="ef504-120">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef504-120">Click **OK**.</span></span> <span data-ttu-id="ef504-121">A meno che non si vogliano configurare altre connessioni del server Advanced Group Policy Management, chiudere la finestra **Editor gestione criteri di gruppo** e distribuire l'oggetto criteri.</span><span class="sxs-lookup"><span data-stu-id="ef504-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="ef504-122">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca. Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management è configurata per tutti gli amministratori dei criteri</span><span class="sxs-lookup"><span data-stu-id="ef504-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="ef504-123">Per configurare altre connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="ef504-124">Se non è stata configurata una connessione al server Advanced Group Policy Management, seguire la procedura precedente per configurare un server Advanced Group Policy Management per tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="ef504-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="ef504-125">Per configurare distinti server Advanced Group Policy Management per alcuni o tutti i domini (eseguendo l'override del server Advanced Group Policy Manager), nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ef504-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="ef504-126">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ef504-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

3.  <span data-ttu-id="ef504-127">Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e quindi **Advanced Group Policy**Management.</span><span class="sxs-lookup"><span data-stu-id="ef504-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="ef504-128">Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare server Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="ef504-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="ef504-129">Nella finestra **Proprietà** selezionare la casella di controllo **abilitata** e fare clic su **Mostra**.</span><span class="sxs-lookup"><span data-stu-id="ef504-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="ef504-130">Nella finestra **Mostra contenuto** :</span><span class="sxs-lookup"><span data-stu-id="ef504-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="ef504-131">Fai clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="ef504-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="ef504-132">Per **nome valore**Digitare il nome di dominio, ad esempio Server1.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ef504-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="ef504-133">Per **valore**Digitare il nome del server Advanced Group Policy Management e la porta da usare per il dominio, ad esempio server2.contoso.com:4600, e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef504-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="ef504-134">(Per impostazione predefinita, il servizio Advanced Group Policy Management ascolta la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="ef504-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="ef504-135">Per usare una porta diversa, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="ef504-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).)</span></span>

    4.  <span data-ttu-id="ef504-136">Ripetere l'impostazione per ogni dominio che non usa il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ef504-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="ef504-137">Fare clic su **OK** per chiudere le finestre **Mostra contenuto** e **proprietà** .</span><span class="sxs-lookup"><span data-stu-id="ef504-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="ef504-138">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="ef504-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="ef504-139">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca. Quando si aggiornano i criteri di gruppo, le nuove connessioni del server Advanced Group Policy Management sono configurate per tutti gli amministratori dei criteri</span><span class="sxs-lookup"><span data-stu-id="ef504-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="ef504-140">Se è stata configurata centralmente la connessione al server Advanced Group Policy Management, l'opzione per la configurazione manuale non è disponibile per tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ef504-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="ef504-141">Per configurare manualmente il server Advanced Group Policy Management da visualizzare per l'account</span><span class="sxs-lookup"><span data-stu-id="ef504-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="ef504-142">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="ef504-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ef504-143">Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .</span><span class="sxs-lookup"><span data-stu-id="ef504-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="ef504-144">Immettere il nome completo del computer per il server Advanced Group Policy Management che gestisce l'archivio usato per questo dominio, ad esempio server.contoso.com, e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600).</span><span class="sxs-lookup"><span data-stu-id="ef504-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="ef504-145">Fare clic su **applica**e quindi su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="ef504-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="ef504-146">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ef504-146">Additional considerations</span></span>

-   <span data-ttu-id="ef504-147">È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per eseguire le procedure per la configurazione centralizzata delle connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ef504-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="ef504-148">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="ef504-148">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

-   <span data-ttu-id="ef504-149">Il server Advanced Group Policy Management selezionato determina quali GPO vengono visualizzati nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="ef504-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="ef504-150">Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.</span><span class="sxs-lookup"><span data-stu-id="ef504-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="ef504-151">L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ef504-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ef504-152">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ef504-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="ef504-153">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="ef504-153">Additional references</span></span>

-   [<span data-ttu-id="ef504-154">Configurazione di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="ef504-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





