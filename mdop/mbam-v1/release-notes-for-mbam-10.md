---
title: Note sulla versione di MBAM 1.0
description: Note sulla versione di MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826026"
---
# <span data-ttu-id="1cf8f-103">Note sulla versione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1cf8f-103">Release Notes for MBAM 1.0</span></span>


**<span data-ttu-id="1cf8f-104">Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="1cf8f-105">Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1cf8f-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

<span data-ttu-id="1cf8f-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-106">These release notes contain information that is required to successfully install MBAM.</span></span> <span data-ttu-id="1cf8f-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="1cf8f-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-108">If there is a difference between these release notes and other MBAM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="1cf8f-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="1cf8f-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="1cf8f-110">About the Product Documentation</span></span>


<span data-ttu-id="1cf8f-111">Per informazioni sulla documentazione di MBAM, vedere la Home page di MBAM in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-111">For information about MBAM documentation, see the MBAM home page on Microsoft TechNet.</span></span>

<span data-ttu-id="1cf8f-112">Per ottenere una copia scaricabile della documentazione di MBAM, vedere nell' <https://go.microsoft.com/fwlink/p/?LinkId=225356> area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-112">To obtain a downloadable copy of the MBAM documentation, see <https://go.microsoft.com/fwlink/p/?LinkId=225356> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="1cf8f-113">Inviare commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="1cf8f-113">Provide Feedback</span></span>


<span data-ttu-id="1cf8f-114">Siamo interessati al feedback su MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-114">We are interested in your feedback on MBAM.</span></span> <span data-ttu-id="1cf8f-115">È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="1cf8f-115">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="1cf8f-116">**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-116">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="1cf8f-117">Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="1cf8f-117">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="1cf8f-118">Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="1cf8f-118">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="1cf8f-119">Problemi noti di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="1cf8f-119">Known Issues with MBAM 1.0</span></span>


<span data-ttu-id="1cf8f-120">Questa sezione contiene note sulla versione sui problemi noti relativi alla configurazione e all'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-120">This section contains release notes about the known issues with MBAM setup and installation.</span></span>

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a><span data-ttu-id="1cf8f-121">Se si seleziona l'opzione "usa un certificato per crittografare la comunicazione di rete" durante l'installazione, le connessioni a database esistenti e le applicazioni dipendenti possono interrompere il funzionamento</span><span class="sxs-lookup"><span data-stu-id="1cf8f-121">If you select the “Use a certificate to encrypt the network communication” option during Setup, existing database connections and dependent applications can stop functioning</span></span>

<span data-ttu-id="1cf8f-122">È possibile configurare MBAM per la **comunicazione di rete crittografata** dopo aver installato il database di ripristino e hardware o le caratteristiche del database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-122">You can configure MBAM for **Encrypted network communication** after you install either the Recovery and Hardware Database or the Compliance Status Database features.</span></span> <span data-ttu-id="1cf8f-123">Se si sceglie di configurare MBAM per la comunicazione di rete crittografata, MBAM setup Configura l'istanza del motore di database di SQL Server in modo da usare SSL (Secure Sockets Layer) per la comunicazione tra il database applicabile e il server di amministrazione e monitoraggio e le caratteristiche del server di report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-123">If you choose to configure MBAM for Encrypted network communication, MBAM Setup configures the instance of the SQL Server Database Engine to use Secure Sockets Layer (SSL) for communication between the applicable database and both the Administration and Monitoring Server and the Compliance and Audit Report Server features.</span></span>

-   <span data-ttu-id="1cf8f-124">Se l'istanza di motore di database di SQL Server non è già configurata per l'uso di SSL, la configurazione di MBAM lo configura per farlo.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-124">If the instance of the SQL Server Database Engine is not already configured to use SSL, MBAM Setup configures it to do so.</span></span> <span data-ttu-id="1cf8f-125">Questo può impedire alle applicazioni che provano di usare database non MBAM nell'istanza del motore di database di SQL Server di comunicare con i loro database.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-125">This can prevent applications that try to use non-MBAM databases on the instance of the SQL Server Database Engine from communicating with their databases.</span></span>

-   <span data-ttu-id="1cf8f-126">Se l'istanza di motore di database di SQL Server è già configurata per l'uso di SSL, è configurata per l'uso del certificato selezionato dall'utente durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-126">If the instance of the SQL Server Database Engine is already configured to use SSL, it is configured to use the certificate that the user selected during setup.</span></span> <span data-ttu-id="1cf8f-127">Se il certificato è diverso da quello già in uso, può impedire l'utilizzo di database di SQL Server nell'istanza del motore di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-127">If this certificate differs from the one that was already in use, it can prevent applications that use SQL Server databases on the instance of the SQL Server Database Engine from running.</span></span>

<span data-ttu-id="1cf8f-128">**Soluzione alternativa:** Nessuno</span><span class="sxs-lookup"><span data-stu-id="1cf8f-128">**WORKAROUND:** None</span></span>

### <span data-ttu-id="1cf8f-129">La configurazione di MBAM non riesce durante l'installazione quando si usa un account di amministratore locale</span><span class="sxs-lookup"><span data-stu-id="1cf8f-129">MBAM Setup fails during installation when you use a local Administrator account</span></span>

<span data-ttu-id="1cf8f-130">La configurazione di MBAM non riesce quando si usa un account di amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-130">MBAM Setup fails when you use a local Administrator account.</span></span> <span data-ttu-id="1cf8f-131">Il file di log contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cf8f-131">The log file contains the following information:</span></span>

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

<span data-ttu-id="1cf8f-132">**Soluzione alternativa:** Usare un account di dominio con credenziali amministrative nel computer server durante l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-132">**WORKAROUND:** Use a domain account with administrative credentials on the server computer when you install MBAM.</span></span>

### <span data-ttu-id="1cf8f-133">La configurazione di MBAM riconfigura l'istanza del motore di database di SQL Server per non usare SSL se selezioni "non crittografare le comunicazioni di rete"</span><span class="sxs-lookup"><span data-stu-id="1cf8f-133">MBAM Setup reconfigures the instance of the SQL Server Database Engine to not use SSL if you select “Do not encrypt network communication”</span></span>

<span data-ttu-id="1cf8f-134">Quando si installa il database di ripristino e hardware o il database dello stato di conformità, è possibile usare la configurazione per configurare MBAM selezionando **comunicazioni di rete crittografate**.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-134">When you install either the Recovery and Hardware Database or the Compliance Status Database, you can use Setup to configure MBAM by selecting **Encrypted network communication**.</span></span> <span data-ttu-id="1cf8f-135">Se si decide di non crittografare la comunicazione di rete, la configurazione di MBAM riconfigura l'istanza del motore di database di SQL Server in modo che non usi SSL.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-135">If you decide not to encrypt the network communication, MBAM Setup reconfigures the instance of the SQL Server Database Engine so that it does not use SSL.</span></span>

-   <span data-ttu-id="1cf8f-136">Se l'istanza di motore di database di SQL Server è già configurata per l'uso di SSL, la configurazione di MBAM Disabilita SSL nell'istanza del motore di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-136">If the instance of the SQL Server Database Engine is already configured to use SSL, MBAM Setup disables SSL on the instance of the SQL Server Database Engine.</span></span> <span data-ttu-id="1cf8f-137">Questo modifica la sicurezza delle comunicazioni tra le applicazioni che usano database non correlati ai database di MBAM nell'istanza di motore di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-137">This changes the communication security between the applications that use databases that are not related to MBAM databases on the instance of the SQL Server Database Engine.</span></span>

<span data-ttu-id="1cf8f-138">**Soluzione alternativa:** Nessuno</span><span class="sxs-lookup"><span data-stu-id="1cf8f-138">**WORKAROUND:** None</span></span>

### <span data-ttu-id="1cf8f-139">Prerequisiti mancanti per gli script di gestione Internet Information Services (IIS) e gli strumenti Web Server</span><span class="sxs-lookup"><span data-stu-id="1cf8f-139">Missing prerequisite for the Internet Information Services (IIS) Management Scripts and Tools web server feature</span></span>

<span data-ttu-id="1cf8f-140">La configurazione di MBAM dipende dagli script di gestione di IIS e dalle funzionalità del server Web degli strumenti, ma non è un prerequisito imposta.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-140">MBAM Setup is dependent on the IIS Management Scripts and Tools web server feature, but it is not an enforced prerequisite.</span></span> <span data-ttu-id="1cf8f-141">La configurazione del server consente di installare MBAM quando manca questa caratteristica.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-141">Server setup lets you install MBAM when this feature is missing.</span></span> <span data-ttu-id="1cf8f-142">In questo modo, tuttavia, il servizio di backup MBAM VSS Writer verrà avviato e quindi si arresta, perché non può individuare il provider di Strumentazione gestione Windows (WMI) e Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="1cf8f-142">However, this will cause the backup service MBAM VSS Writer to start and then stop, because it cannot locate the Windows Management Instrumentation (WMI) and the Internet Information Services (IIS) provider.</span></span> <span data-ttu-id="1cf8f-143">Non viene visualizzato alcun messaggio di errore per questa condizione, ad eccezione di quello che si verifica nel log eventi.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-143">There is no error message for this condition, except that which occurs in the event log.</span></span> <span data-ttu-id="1cf8f-144">L'installazione di MBAM senza gli script e gli strumenti di gestione di IIS fa in modo che le operazioni di backup non vengano eseguite per MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-144">Installation of MBAM without IIS Management Scripts and Tools causes the backup operations not to run for MBAM.</span></span>

<span data-ttu-id="1cf8f-145">**Soluzione alternativa:** Prima di avviare la configurazione di MBAM, assicurati che la funzionalità di gestione degli script e degli strumenti del server Web sia installata in IIS.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-145">**WORKAROUND:** Ensure that the IIS Management Scripts and Tools web server feature is installed before you start the MBAM Setup.</span></span>

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a><span data-ttu-id="1cf8f-146">La configurazione di MBAM smette di rispondere durante la fase "installazione delle caratteristiche selezionate" quando la configurazione è configurata per l'uso di un certificato</span><span class="sxs-lookup"><span data-stu-id="1cf8f-146">MBAM Setup stops responding during the “Installing selected features” phase when setup is configured to use a certificate</span></span>

<span data-ttu-id="1cf8f-147">La configurazione di MBAM smette di rispondere durante la fase di installazione delle **caratteristiche selezionate** .</span><span class="sxs-lookup"><span data-stu-id="1cf8f-147">MBAM Setup stops responding during the **Installing selected features** phase of setup.</span></span> <span data-ttu-id="1cf8f-148">Questo problema si verifica durante l'installazione del database di ripristino e hardware o del database dello stato di conformità, dopo aver selezionato l'opzione **Usa un certificato per crittografare la comunicazione di rete** .</span><span class="sxs-lookup"><span data-stu-id="1cf8f-148">This occurs during the installation of the Recovery and Hardware Database or the Compliance Status Database, after you select the **Use a certificate to encrypt the network communication** option.</span></span> <span data-ttu-id="1cf8f-149">Inoltre, la configurazione di MBAM smette di rispondere se l'istanza di motore di database di SQL Server non riesce ad accedere al certificato specificato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-149">Furthermore, the MBAM Setup stops responding if the instance of the SQL Server Database Engine cannot access the certificate that was specified during setup.</span></span>

<span data-ttu-id="1cf8f-150">**Soluzione alternativa:** Aggiornare le autorizzazioni per il certificato, in modo che il servizio Windows per l'istanza applicabile di motore di database di SQL Server possa accedere al certificato.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-150">**WORKAROUND:** Update the permissions on the certificate, so that the Windows service for the applicable instance of the SQL Server Database Engine can access the certificate.</span></span> <span data-ttu-id="1cf8f-151">È anche possibile modificare l'account in cui viene eseguita l'istanza del motore di database di SQL Server, in modo che il motore di database usi il certificato.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-151">You can also change the account under which the instance of the SQL Server Database Engine runs, for the database engine to use the certificate.</span></span> <span data-ttu-id="1cf8f-152">Per determinare le autorizzazioni per il certificato, digitare il comando seguente al prompt dei comandi: **certutil-v-Store My**</span><span class="sxs-lookup"><span data-stu-id="1cf8f-152">To determine the permissions for the certificate, type the following command at the command prompt: **certutil -v -store MY**</span></span>

### <span data-ttu-id="1cf8f-153">La configurazione di MBAM viene sospesa durante l'installazione di SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="1cf8f-153">MBAM Setup pauses when you install SQL Server Reporting Services</span></span>

<span data-ttu-id="1cf8f-154">Durante l'installazione di MBAM, quando si seleziona un'istanza di SQL Server Reporting Services (SSRS) e l'istanza di SSRS non è disponibile o è configurata in modo non corretto, la configurazione di MBAM potrebbe essere sospesa fino a un minuto mentre tenta di comunicare con l'istanza di SSRS.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-154">During MBAM installation, when you select an instance of SQL Server Reporting Services (SSRS) and SSRS instance is not available or it is configured incorrectly, the MBAM Setup might pause for up to one minute while it attempts to communicate with the SSRS instance.</span></span>

<span data-ttu-id="1cf8f-155">**Soluzione alternativa:** Attendere almeno un minuto per la configurazione di MBAM per riprendere mentre il programma di installazione tenta di contattare l'istanza di SSRS.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-155">**WORKAROUND:** Wait for at least one minute for MBAM Setup to resume while the Setup program attempts to contact the instance of SSRS.</span></span>

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a><span data-ttu-id="1cf8f-156">Il server di amministrazione e monitoraggio non viene eseguito dopo la configurazione</span><span class="sxs-lookup"><span data-stu-id="1cf8f-156">Administration and Monitoring Server does not run after setup</span></span>

<span data-ttu-id="1cf8f-157">Dopo la configurazione di MBAM installa correttamente la funzionalità di amministrazione e monitoraggio del server, MBAM Visualizza i messaggi di errore quando si tenta di accedere al sito Web dell'amministratore di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-157">After MBAM Setup successfully installs the Administration and Monitoring Server feature, MBAM displays error messages when you try to access the MBAM administrator website.</span></span> <span data-ttu-id="1cf8f-158">Questo problema si verifica per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cf8f-158">This issue occurs for one of the following reasons:</span></span>

-   <span data-ttu-id="1cf8f-159">Uno o più prerequisiti per l'amministrazione e il server di monitoraggio sono stati rimossi dopo l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-159">One or more prerequisites on the Administration and Monitoring Server were removed after the MBAM installation.</span></span>

-   <span data-ttu-id="1cf8f-160">Uno o più prerequisiti sono stati installati nel server e in seguito sono stati rimossi prima di eseguire la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-160">One or more prerequisites were installed on the server and later they were removed before running the MBAM Setup.</span></span>

<span data-ttu-id="1cf8f-161">**Soluzione alternativa:** Esaminare la documentazione di MBAM e verificare che siano installati tutti i prerequisiti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-161">**WORKAROUND:** Review the MBAM documentation and confirm that all MBAM prerequisites are installed.</span></span>

### <span data-ttu-id="1cf8f-162">Se si fa clic su collegamenti alla documentazione durante la configurazione, viene visualizzato un errore dell'applicazione dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="1cf8f-162">Clicking documentation links during Setup results in an application error after Setup is finished</span></span>

<span data-ttu-id="1cf8f-163">Quando si fa clic su un collegamento alla documentazione durante l'installazione e quindi si chiude il programma di installazione facendo clic su **Annulla** o **fine** dopo il completamento della configurazione, viene visualizzato un messaggio di errore dell'applicazione..</span><span class="sxs-lookup"><span data-stu-id="1cf8f-163">When you click a documentation link during setup and then close the Setup program by clicking **Cancel** or **Finish** after Setup has successfully finished, an application error message appears..</span></span> <span data-ttu-id="1cf8f-164">Il problema è causato da un errore di violazione di Access nell'utilità di pianificazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-164">The problem is caused by an access violation error in the Windows Task Scheduler.</span></span>

<span data-ttu-id="1cf8f-165">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-165">**WORKAROUND:** None.</span></span> <span data-ttu-id="1cf8f-166">Puoi ignorare questo errore.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-166">You can ignore this error.</span></span>

### <span data-ttu-id="1cf8f-167">Errore di installazione di MBAM non rimuove i nuovi database</span><span class="sxs-lookup"><span data-stu-id="1cf8f-167">Failed MBAM Setup does not remove new databases</span></span>

<span data-ttu-id="1cf8f-168">Se la configurazione di MBAM non riesce, la configurazione potrebbe non rimuovere i database appena creati.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-168">If the MBAM Setup fails, Setup might not remove the newly created databases.</span></span> <span data-ttu-id="1cf8f-169">Ciò può causare errori durante le installazioni successive.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-169">This can cause failures during subsequent installations.</span></span>

<span data-ttu-id="1cf8f-170">**Soluzione alternativa:** Scegliere un nome diverso per l'istanza del database durante l'installazione successiva.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-170">**WORKAROUND:** Choose a different name for the database instance during the subsequent installation.</span></span>

### <span data-ttu-id="1cf8f-171">La configurazione di MBAM non riconosce i certificati cluster di bilanciamento del carico di rete validi</span><span class="sxs-lookup"><span data-stu-id="1cf8f-171">MBAM Setup does not recognize valid network load-balancing cluster certificates</span></span>

<span data-ttu-id="1cf8f-172">Durante l'installazione di MBAM Administration e Monitoring Server, con l'opzione di crittografia della rete selezionata, il certificato del cluster non viene riconosciuto come certificato valido.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-172">During the MBAM Administration and Monitoring Server installation, with the network encryption option selected, the cluster certificate is not recognized as a valid certificate.</span></span> <span data-ttu-id="1cf8f-173">Viene riconosciuta come valida quando il certificato per la comunicazione con il database è installato, ma viene rifiutato per la comunicazione tramite il cluster di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-173">It is recognized as valid when the certificate for communication with the database is installed, but it is rejected for communication by the load-balancing cluster.</span></span>

<span data-ttu-id="1cf8f-174">**Soluzione alternativa:** Verificare che l'elenco di revoche di certificati associato al certificato sia accessibile oppure utilizzare un certificato che non richiede la convalida tramite il CRL.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-174">**WORKAROUND:** Confirm that the certificate revocation list (CRL) associated with the certificate is accessible, or use a certificate that does not require validation by using the CRL.</span></span>

## <span data-ttu-id="1cf8f-175">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="1cf8f-175">Release Notes Copyright Information</span></span>


<span data-ttu-id="1cf8f-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="1cf8f-177">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="1cf8f-177">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="1cf8f-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1cf8f-178">Related topics</span></span>


[<span data-ttu-id="1cf8f-179">Informazioni su MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1cf8f-179">About MBAM 1.0</span></span>](about-mbam-10.md)

 

 





