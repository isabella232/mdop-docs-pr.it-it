---
title: Risoluzione dei problemi di Gestione avanzata Criteri di gruppo
description: Risoluzione dei problemi di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: f7ece97c-e9f8-4b18-8c7a-a615c98d5c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4815378a17a7c083501cfd7772e62415ec285237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820176"
---
# <span data-ttu-id="46467-103">Risoluzione dei problemi di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="46467-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="46467-104">In questa sezione vengono elencati i problemi comuni che possono verificarsi quando si usa Gestione criteri di gruppo avanzati per gestire gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="46467-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="46467-105">Per diagnosticare i problemi non elencati in questo articolo, potrebbe essere utile per un amministratore Advanced Group Policy Management (controllo completo) usare la registrazione e la traccia.</span><span class="sxs-lookup"><span data-stu-id="46467-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="46467-106">Per altre informazioni, vedere [configurare la registrazione e la traccia](configure-logging-and-tracing-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md).</span></span>

**<span data-ttu-id="46467-107">Nota</span><span class="sxs-lookup"><span data-stu-id="46467-107">Note</span></span>**  
-   <span data-ttu-id="46467-108">Per informazioni su come ripristinare una versione precedente di un GPO in caso di problemi, vedere [eseguire il rollback a una versione precedente di un oggetto Criteri](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="46467-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span></span>

-   <span data-ttu-id="46467-109">Per informazioni su come recuperare da un disastro ripristinando l'archivio completo da un backup, vedere [ripristinare l'archivio da un backup](restore-the-archive-from-a-backup.md).</span><span class="sxs-lookup"><span data-stu-id="46467-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup.md).</span></span>

 

## <span data-ttu-id="46467-110">Quali problemi si verificano?</span><span class="sxs-lookup"><span data-stu-id="46467-110">What problems are you having?</span></span>


-   [<span data-ttu-id="46467-111">Non è possibile accedere a un archivio</span><span class="sxs-lookup"><span data-stu-id="46467-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="46467-112">Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi</span><span class="sxs-lookup"><span data-stu-id="46467-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="46467-113">Non è possibile modificare la connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="46467-114">Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO</span><span class="sxs-lookup"><span data-stu-id="46467-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="46467-115">Non è possibile usare un nome di GPO specifico</span><span class="sxs-lookup"><span data-stu-id="46467-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="46467-116">Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="46467-117">Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="46467-118">Il servizio Advanced Group Policy Management non si avvia</span><span class="sxs-lookup"><span data-stu-id="46467-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="46467-119">L'installazione del software di criteri di gruppo non riesce ad installare</span><span class="sxs-lookup"><span data-stu-id="46467-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="46467-120">Si è verificato un errore quando è stato ripristinato l'archivio in un nuovo server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="46467-121">Non è possibile accedere a un archivio</span><span class="sxs-lookup"><span data-stu-id="46467-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="46467-122">**Causa**: non è stato selezionato il server e la porta corretti per l'archivio.</span><span class="sxs-lookup"><span data-stu-id="46467-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="46467-123">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-123">**Solution**:</span></span>

    -   <span data-ttu-id="46467-124">Se si è un amministratore Advanced Group Policy Management: vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="46467-125">Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata.</span><span class="sxs-lookup"><span data-stu-id="46467-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="46467-126">Vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

-   <span data-ttu-id="46467-127">**Causa**: il servizio Advanced Group Policy Management non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="46467-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="46467-128">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-128">**Solution**:</span></span>

    -   <span data-ttu-id="46467-129">Se si è un amministratore della Advanced Group Policy Management: avviare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="46467-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="46467-130">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

    -   <span data-ttu-id="46467-131">Se non si è un amministratore della Advanced Group Policy Management: contattare un amministratore della Advanced Group Policy per assistenza.</span><span class="sxs-lookup"><span data-stu-id="46467-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="46467-132">Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi</span><span class="sxs-lookup"><span data-stu-id="46467-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="46467-133">**Causa**: diversi amministratori dei criteri di gruppo hanno selezionato diversi server Advanced Group Policy Management per lo stesso archivio.</span><span class="sxs-lookup"><span data-stu-id="46467-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="46467-134">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-134">**Solution**:</span></span>

    -   <span data-ttu-id="46467-135">Se si è un amministratore Advanced Group Policy Management: vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="46467-136">Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata.</span><span class="sxs-lookup"><span data-stu-id="46467-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="46467-137">Vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="46467-138">Non è possibile modificare la connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="46467-139">**Causa**: se le impostazioni nella scheda **server Advanced Group Policy Management** non sono disponibili, il server Advanced Group Policy Management è stato configurato centralmente usando un modello amministrativo.</span><span class="sxs-lookup"><span data-stu-id="46467-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="46467-140">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-140">**Solution**:</span></span>

    -   <span data-ttu-id="46467-141">Se si è un amministratore Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy Management** non sono disponibili, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="46467-142">Se non si è un amministratore di Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy** Management non sono disponibili, non è necessario modificare il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="46467-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="46467-143">Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO</span><span class="sxs-lookup"><span data-stu-id="46467-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="46467-144">**Causa**: non è stato assegnato un ruolo con le autorizzazioni necessarie per eseguire l'attività o le attività.</span><span class="sxs-lookup"><span data-stu-id="46467-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="46467-145">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-145">**Solution**:</span></span>

    -   <span data-ttu-id="46467-146">Se si è un amministratore della Advanced Group Policy Management: vedere [delegare l'accesso a livello di dominio all'archivio](delegate-domain-level-access-to-the-archive-agpm30ops.md) e [delegare l'accesso a un singolo GPO nell'archivio](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md).</span></span> <span data-ttu-id="46467-147">Le autorizzazioni Advanced Group Policy Management verranno sovrapposte dal dominio a tutti i GPO attualmente presenti nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="46467-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="46467-148">Per informazioni dettagliate sui ruoli che possono eseguire un'attività e le autorizzazioni necessarie per eseguire un'attività, vedere la guida relativa all'attività.</span><span class="sxs-lookup"><span data-stu-id="46467-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="46467-149">Se non si è un amministratore di Advanced Group Policy Management e si richiedono ulteriori ruoli o autorizzazioni: contattare un amministratore della Advanced Group Policy per assistenza.</span><span class="sxs-lookup"><span data-stu-id="46467-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="46467-150">Tenere presente che, se si è un editor, è possibile iniziare il processo di creazione di un GPO, distribuire un GPO o eliminare un GPO dall'ambiente di produzione, ma un approvatore o un amministratore della Advanced Group Policy Management deve approvare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="46467-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="46467-151">Non è possibile usare un nome di GPO specifico</span><span class="sxs-lookup"><span data-stu-id="46467-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="46467-152">**Causa**: il nome del GPO è già in uso o manca l'autorizzazione per elencare il GPO.</span><span class="sxs-lookup"><span data-stu-id="46467-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="46467-153">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-153">**Solution**:</span></span>

    -   <span data-ttu-id="46467-154">Se il nome del GPO viene visualizzato nella scheda **controllata** **, non controllata o** **in sospeso** , scegliere un altro nome.</span><span class="sxs-lookup"><span data-stu-id="46467-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="46467-155">Se un oggetto Criteri di gruppo distribuito viene rinominato ma non ancora ridistribuito, verrà visualizzato sotto il nome precedente nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="46467-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment.</span></span> <span data-ttu-id="46467-156">Di conseguenza, il vecchio nome viene ancora usato.</span><span class="sxs-lookup"><span data-stu-id="46467-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="46467-157">Ridistribuire il GPO per aggiornarne il nome nell'ambiente di produzione e rilasciare tale nome per l'uso da parte di un altro GPO.</span><span class="sxs-lookup"><span data-stu-id="46467-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="46467-158">Se il nome del GPO non viene visualizzato nella scheda **controllato**, non controllata o **in sospeso** , potrebbe mancare l'autorizzazione per elencare l'oggetto Criteri di **controllo**.</span><span class="sxs-lookup"><span data-stu-id="46467-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="46467-159">Per richiedere l'autorizzazione, contattare un amministratore della Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="46467-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="46467-160">Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="46467-161">**Causa**: non è stato fornito un server di posta elettronica SMTP valido e un indirizzo di posta elettronica oppure non è stata eseguita alcuna azione che genera una notifica tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="46467-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="46467-162">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="46467-162">**Solution**:</span></span>

    -   <span data-ttu-id="46467-163">Se si è un amministratore della Advanced Group Policy Management: per le notifiche tramite posta elettronica relative alle azioni in sospeso da inviare da Advanced Group Policy Management, un amministratore Advanced Group Policy Management deve specificare un server di posta elettronica SMTP valido e gli indirizzi di posta elettronica per i responsabili approvazione nella scheda **delega** Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

    -   <span data-ttu-id="46467-164">Le notifiche tramite posta elettronica vengono generate solo quando un editor, un revisore o un altro amministratore di criteri di gruppo che non dispone delle autorizzazioni necessarie per creare, distribuire o eliminare un GPO invia una richiesta di una di queste azioni.</span><span class="sxs-lookup"><span data-stu-id="46467-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="46467-165">Non esiste una notifica automatica di approvazione o rifiuto di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="46467-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="46467-166">Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="46467-167">**Causa**: per impostazione predefinita, la porta su cui è in ascolto il servizio Advanced Group Policy Management è la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="46467-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="46467-168">**Soluzione**: se la porta 4600 non è disponibile per il servizio Advanced Group Policy Management, modificare la configurazione della porta nel server Advanced Group Policy Management per usare un'altra porta e quindi aggiornare la porta nella connessione del server Advanced Group Policy Management per i client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="46467-169">Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="46467-170">Il servizio Advanced Group Policy Management non si avvia</span><span class="sxs-lookup"><span data-stu-id="46467-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="46467-171">**Causa**: sono state modificate le impostazioni per il servizio Advanced Group Policy Management nel sistema operativo in strumenti e **Servizi** **amministrativi** .</span><span class="sxs-lookup"><span data-stu-id="46467-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="46467-172">**Soluzione**: modificare le impostazioni per **Microsoft Advanced Group Policy Management-Server** in **programmi e funzionalità** nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="46467-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="46467-173">Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="46467-174">L'installazione del software di criteri di gruppo non riesce ad installare</span><span class="sxs-lookup"><span data-stu-id="46467-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="46467-175">**Causa**: Advanced Group Policy Management mantiene l'integrità dei pacchetti di installazione del software di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="46467-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="46467-176">Anche se i GPO vengono modificati offline, vengono mantenuti i collegamenti tra i pacchetti oltre alle informazioni memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="46467-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="46467-177">Questo comportamento è da progettazione.</span><span class="sxs-lookup"><span data-stu-id="46467-177">This is by design.</span></span>

-   <span data-ttu-id="46467-178">**Soluzione**: quando si modifica un oggetto Criteri di gruppo in modalità offline con Advanced Group Policy Management, configurare qualsiasi aggiornamento del software di un pacchetto in un altro GPO per fare riferimento al GPO distribuito, non alla copia selezionata.</span><span class="sxs-lookup"><span data-stu-id="46467-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="46467-179">L'editor deve avere l'autorizzazione di **lettura** per l'oggetto Criteri di ricerca distribuito.</span><span class="sxs-lookup"><span data-stu-id="46467-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="46467-180">Si è verificato un errore quando è stato ripristinato l'archivio in un nuovo server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="46467-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="46467-181">**Causa**: per motivi di sicurezza, la crittografia che protegge la password immessa nella scheda **delega del dominio** fa sì che la password non riesca se l'archivio viene spostato in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="46467-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="46467-182">**Soluzione**: immettere di nuovo e confermare la password nella scheda **delega del dominio** . Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="46467-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

 

 





