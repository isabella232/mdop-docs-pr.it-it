---
title: Risoluzione dei problemi di Gestione avanzata Criteri di gruppo
description: Risoluzione dei problemi di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818255"
---
# <span data-ttu-id="f8158-103">Risoluzione dei problemi di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f8158-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="f8158-104">In questa sezione sono elencati alcuni problemi comuni che possono verificarsi quando si usa Advanced Group Policy Management per gestire gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8158-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="f8158-105">Quali problemi si verificano?</span><span class="sxs-lookup"><span data-stu-id="f8158-105">What problems are you having?</span></span>


-   [<span data-ttu-id="f8158-106">Non è possibile accedere a un archivio</span><span class="sxs-lookup"><span data-stu-id="f8158-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="f8158-107">Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi</span><span class="sxs-lookup"><span data-stu-id="f8158-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="f8158-108">Non è possibile modificare la connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="f8158-109">Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO</span><span class="sxs-lookup"><span data-stu-id="f8158-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="f8158-110">Non è possibile usare un nome di GPO specifico</span><span class="sxs-lookup"><span data-stu-id="f8158-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="f8158-111">Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="f8158-112">Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="f8158-113">Il servizio Advanced Group Policy Management non si avvia</span><span class="sxs-lookup"><span data-stu-id="f8158-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="f8158-114">L'installazione del software di criteri di gruppo non riesce ad installare</span><span class="sxs-lookup"><span data-stu-id="f8158-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="f8158-115">Non è possibile accedere a un archivio</span><span class="sxs-lookup"><span data-stu-id="f8158-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="f8158-116">**Causa**: non è stato selezionato il server e la porta corretti per l'archivio.</span><span class="sxs-lookup"><span data-stu-id="f8158-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="f8158-117">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-117">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-118">Se si è un amministratore della Advanced Group Policy Management: vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="f8158-119">Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata.</span><span class="sxs-lookup"><span data-stu-id="f8158-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="f8158-120">Vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="f8158-121">**Causa**: il servizio di gestione dei criteri di gruppo avanzato non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f8158-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="f8158-122">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-122">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-123">Se si è un amministratore della Advanced Group Policy Management: avviare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f8158-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="f8158-124">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="f8158-125">Se non si è un amministratore della Advanced Group Policy Management: contattare un amministratore della Advanced Group Policy per assistenza.</span><span class="sxs-lookup"><span data-stu-id="f8158-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="f8158-126">Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi</span><span class="sxs-lookup"><span data-stu-id="f8158-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="f8158-127">**Causa**: diversi amministratori dei criteri di gruppo hanno selezionato diversi server Advanced Group Policy Management per lo stesso archivio.</span><span class="sxs-lookup"><span data-stu-id="f8158-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="f8158-128">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-128">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-129">Se si è un amministratore della Advanced Group Policy Management: vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="f8158-130">Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata.</span><span class="sxs-lookup"><span data-stu-id="f8158-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="f8158-131">Vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="f8158-132">Non è possibile modificare la connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="f8158-133">**Causa**: se le impostazioni nella scheda **server Advanced Group Policy Management** non sono disponibili, il server Advanced Group Policy Management è stato configurato centralmente usando un modello amministrativo.</span><span class="sxs-lookup"><span data-stu-id="f8158-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="f8158-134">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-134">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-135">Se si è un amministratore della Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy** Management non sono disponibili, vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="f8158-136">Se non si è un amministratore di Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy** Management non sono disponibili, non è necessario modificare il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f8158-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="f8158-137">Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO</span><span class="sxs-lookup"><span data-stu-id="f8158-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="f8158-138">**Causa**: non è stato assegnato un ruolo con le autorizzazioni necessarie per eseguire l'attività o le attività.</span><span class="sxs-lookup"><span data-stu-id="f8158-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="f8158-139">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-139">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-140">Se si è un amministratore della Advanced Group Policy Management: vedere delegare accesso a [livello di dominio](delegate-domain-level-access.md) e [delegare l'accesso a un singolo GPO](delegate-access-to-an-individual-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="f8158-141">Le autorizzazioni Advanced Group Policy Management verranno sovrapposte dal dominio a tutti i GPO attualmente presenti nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="f8158-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="f8158-142">Man mano che i nuovi amministratori dei criteri di gruppo vengono aggiunti a livello di dominio, le autorizzazioni devono essere impostate per applicare l' **oggetto e gli oggetti annidati**.</span><span class="sxs-lookup"><span data-stu-id="f8158-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="f8158-143">Per informazioni dettagliate sui ruoli che possono eseguire un'attività e sulle autorizzazioni necessarie per eseguire un'attività, vedere la guida relativa all'attività.</span><span class="sxs-lookup"><span data-stu-id="f8158-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="f8158-144">Se non si è un amministratore di Advanced Group Policy Management e si richiedono ulteriori ruoli o autorizzazioni: contattare un amministratore della Advanced Group Policy per assistenza.</span><span class="sxs-lookup"><span data-stu-id="f8158-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="f8158-145">Tieni presente che, se sei un editor, puoi iniziare il processo di creazione di un GPO, distribuire un GPO o eliminare un GPO dall'ambiente di produzione, ma un approvatore o un amministratore della Advanced Group Policy Management deve approvare la tua richiesta.</span><span class="sxs-lookup"><span data-stu-id="f8158-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="f8158-146">Non è possibile usare un nome di GPO specifico</span><span class="sxs-lookup"><span data-stu-id="f8158-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="f8158-147">**Causa**: il nome del GPO è già in uso o manca l'autorizzazione per elencare il GPO.</span><span class="sxs-lookup"><span data-stu-id="f8158-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="f8158-148">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-148">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-149">Se il nome del GPO viene visualizzato nella scheda **controllata** **, non controllata o** **in sospeso** , scegliere un altro nome.</span><span class="sxs-lookup"><span data-stu-id="f8158-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="f8158-150">Se un oggetto Criteri di gruppo distribuito viene rinominato ma non ancora ridistribuito, verrà visualizzato sotto il nome precedente nell'ambiente di produzione, quindi il vecchio nome è ancora in uso.</span><span class="sxs-lookup"><span data-stu-id="f8158-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="f8158-151">Ridistribuire il GPO per aggiornarne il nome nell'ambiente di produzione e rilasciare tale nome per l'uso da parte di un altro GPO.</span><span class="sxs-lookup"><span data-stu-id="f8158-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="f8158-152">Se il nome del GPO non viene visualizzato nella scheda **controllato**, non controllata o **in sospeso** , potrebbe mancare l'autorizzazione per elencare l'oggetto Criteri di **controllo**.</span><span class="sxs-lookup"><span data-stu-id="f8158-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="f8158-153">Per richiedere l'autorizzazione, contattare un amministratore della Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f8158-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="f8158-154">Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="f8158-155">**Causa**: non è stato fornito un server di posta elettronica SMTP valido e un indirizzo di posta elettronica oppure non è stata eseguita alcuna azione che genera una notifica tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f8158-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="f8158-156">**Soluzione**:</span><span class="sxs-lookup"><span data-stu-id="f8158-156">**Solution**:</span></span>

    -   <span data-ttu-id="f8158-157">Se si è un amministratore della Advanced Group Policy Management: per le notifiche tramite posta elettronica relative alle azioni in sospeso da inviare da Advanced Group Policy Management, un amministratore Advanced Group Policy Management deve specificare un server di posta elettronica SMTP valido e gli indirizzi di posta elettronica per i responsabili approvazione nella scheda **delega** Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="f8158-158">Le notifiche tramite posta elettronica vengono generate solo quando un editor, un revisore o un altro amministratore di criteri di gruppo che non dispone delle autorizzazioni necessarie per creare, distribuire o eliminare un GPO invia una richiesta di una di queste azioni.</span><span class="sxs-lookup"><span data-stu-id="f8158-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="f8158-159">Non esiste una notifica automatica di approvazione o rifiuto di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="f8158-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="f8158-160">Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f8158-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="f8158-161">**Causa**: per impostazione predefinita, la porta su cui è in ascolto il servizio Advanced Group Policy Management è la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="f8158-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="f8158-162">**Soluzione**: se la porta 4600 non è disponibile per il servizio Advanced Group Policy Management, modificare ogni file di indice di archivio per usare un'altra porta e quindi aggiornare il server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8158-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="f8158-163">Per altre informazioni, vedere [modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management](modify-the-port-on-which-the-agpm-service-listens.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="f8158-164">Il servizio Advanced Group Policy Management non si avvia</span><span class="sxs-lookup"><span data-stu-id="f8158-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="f8158-165">**Causa**: sono state modificate le impostazioni per il servizio Advanced Group Policy Management nel sistema operativo in strumenti e **Servizi** **amministrativi** .</span><span class="sxs-lookup"><span data-stu-id="f8158-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="f8158-166">**Soluzione**: modificare le impostazioni per **Microsoft Advanced Group Policy Management-Server** in **aggiungere o rimuovere programmi**.</span><span class="sxs-lookup"><span data-stu-id="f8158-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="f8158-167">Per altre informazioni, vedere [modificare l'account del servizio Advanced Group Policy Management](modify-the-agpm-service-account.md).</span><span class="sxs-lookup"><span data-stu-id="f8158-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="f8158-168">L'installazione del software di criteri di gruppo non riesce ad installare</span><span class="sxs-lookup"><span data-stu-id="f8158-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="f8158-169">**Causa**: Advanced Group Policy Management mantiene l'integrità dei pacchetti di installazione del software di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8158-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="f8158-170">Anche se i GPO vengono modificati offline, vengono mantenuti i collegamenti tra i pacchetti e le informazioni client memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="f8158-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="f8158-171">Questo comportamento è da progettazione.</span><span class="sxs-lookup"><span data-stu-id="f8158-171">This is by design.</span></span>

-   <span data-ttu-id="f8158-172">**Soluzione**: quando si modifica un oggetto Criteri di gruppo in modalità offline con Advanced Group Policy Management, configurare qualsiasi aggiornamento del software di un pacchetto in un altro GPO per fare riferimento al GPO distribuito, non alla copia selezionata.</span><span class="sxs-lookup"><span data-stu-id="f8158-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="f8158-173">L'editor deve avere l'autorizzazione di **lettura** per l'oggetto Criteri di ricerca distribuito.</span><span class="sxs-lookup"><span data-stu-id="f8158-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





