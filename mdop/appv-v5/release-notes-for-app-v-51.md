---
title: Note sulla versione per App-V 5.1
description: Note sulla versione per App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804881"
---
# <span data-ttu-id="bac27-103">Note sulla versione per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="bac27-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="bac27-104">Di seguito sono riportati i problemi noti di Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="bac27-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="bac27-105">Si verifica un errore durante l'aggiornamento della pubblicazione tra App-V 5,0 SP3 Management Server e client App-V 5,1 in Windows 10</span><span class="sxs-lookup"><span data-stu-id="bac27-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="bac27-106">Quando si sincronizzano i pacchetti dal server di gestione SP3 App-V 5,0 a un client App-V 5,1 in Windows 10, viene generato un errore durante l'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="bac27-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="bac27-107">Questo errore si verifica perché il server App-V 5,0 SP3 non comprende il sistema operativo Windows 10 specificato nell'URL di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="bac27-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="bac27-108">Il problema è risolto per il server di pubblicazione App-V 5,1, ma non viene convertito in versioni di App-V 5,0 SP3 o versione precedente.</span><span class="sxs-lookup"><span data-stu-id="bac27-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="bac27-109">**Soluzione alternativa**: aggiornare il server di gestione di App-v 5,0 al server di gestione di App-v 5,1 per i client Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bac27-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="bac27-110">Le configurazioni personalizzate non vengono applicate per i pacchetti che verranno pubblicati globalmente se impostati tramite il server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="bac27-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="bac27-111">Se si assegna un pacchetto a un gruppo di annunci che contiene gli account del computer e si applica una configurazione personalizzata a tale gruppo usando App-V Server, la configurazione personalizzata non verrà applicata a tali computer.</span><span class="sxs-lookup"><span data-stu-id="bac27-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="bac27-112">Il client App-V 5,1 pubblicherà i pacchetti assegnati a un account del computer a livello globale.</span><span class="sxs-lookup"><span data-stu-id="bac27-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="bac27-113">Tuttavia, archivia i file di configurazione personalizzati per ogni utente nel profilo di ogni utente.</span><span class="sxs-lookup"><span data-stu-id="bac27-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="bac27-114">I pacchetti pubblicati globalmente non avranno accesso a questa configurazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bac27-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="bac27-115">**Soluzione alternativa**: eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bac27-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="bac27-116">Assegnare il pacchetto ai gruppi che contengono solo gli account utente.</span><span class="sxs-lookup"><span data-stu-id="bac27-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="bac27-117">In questo modo, la configurazione personalizzata del pacchetto verrà archiviata nel profilo di ogni utente e verrà applicata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bac27-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="bac27-118">Creare un file di configurazione della distribuzione personalizzato e applicarlo al pacchetto nel client usando il cmdlet Add-AppvClientPackage con il parametro – DynamicDeploymentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bac27-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="bac27-119">Per altre informazioni, vedere [informazioni sulla configurazione dinamica di App-V 5,1](about-app-v-51-dynamic-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="bac27-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="bac27-120">Creare un nuovo pacchetto con la configurazione personalizzata usando l'App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="bac27-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="bac27-121">File del server non eliminati dopo l'installazione del nuovo App-V 5,1 server</span><span class="sxs-lookup"><span data-stu-id="bac27-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="bac27-122">Se si disinstalla il server App-V 5,0 SP1 e quindi si installa il server App-V 5,1, l'installazione non riesce, viene installata la versione errata del server di gestione e viene restituito un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="bac27-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="bac27-123">Il problema si verifica perché i file del server non vengono eliminati quando si disinstalla l'App-V 5,0 SP1, quindi il processo di installazione esegue un aggiornamento anziché una nuova installazione.</span><span class="sxs-lookup"><span data-stu-id="bac27-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="bac27-124">**Soluzione alternativa**: eliminare la chiave del registro di sistema prima di iniziare l'installazione di App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="bac27-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="bac27-125">In HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall individuare ed eliminare la chiave GUID di installazione che contiene il valore DWORD "DisplayName" con i dati di valore "Microsoft Application Virtualization (App-V) Server".</span><span class="sxs-lookup"><span data-stu-id="bac27-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="bac27-126">Questa è l'unica chiave che deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="bac27-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="bac27-127">Le associazioni di tipi di file aggiunte manualmente non vengono salvate correttamente</span><span class="sxs-lookup"><span data-stu-id="bac27-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="bac27-128">Le associazioni di tipi di file aggiunte manualmente a un pacchetto dell'applicazione con i tasti di scelta rapida e la scheda accordi alla fine della procedura guidata di aggiornamento delle applicazioni non vengono salvate correttamente.</span><span class="sxs-lookup"><span data-stu-id="bac27-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="bac27-129">Non saranno disponibili per il client App-V o per il sequencer durante l'aggiornamento del pacchetto salvato.</span><span class="sxs-lookup"><span data-stu-id="bac27-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="bac27-130">**Soluzione alternativa**: per aggiungere un'associazione di tipi di file, aprire il pacchetto per la modifica ed eseguire la procedura guidata di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bac27-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="bac27-131">Durante il passaggio di installazione, aggiungere la nuova associazione del tipo di file tramite il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bac27-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="bac27-132">Il sequencer rileverà la nuova associazione nel registro di sistema e la aggiungerà al registro virtuale del pacchetto, dove sarà disponibile per il client.</span><span class="sxs-lookup"><span data-stu-id="bac27-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="bac27-133">Quando si esegue lo streaming di pacchetti nella modalità SCS (Shared Content Store) a un client gestito anche da AppLocker, nel disco locale vengono scritti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="bac27-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="bac27-134">Per ridurre la quantità di dati scritti nel disco locale di un client, è possibile abilitare la modalità SCS nel client App-V 5,1 per trasmettere il contenuto di un pacchetto su richiesta.</span><span class="sxs-lookup"><span data-stu-id="bac27-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="bac27-135">Tuttavia, se AppLocker gestisce un'applicazione all'interno del pacchetto, alcuni dati potrebbero essere scritti nel disco locale del client che altrimenti non verranno scritti.</span><span class="sxs-lookup"><span data-stu-id="bac27-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="bac27-136">**Soluzione alternativa**: None</span><span class="sxs-lookup"><span data-stu-id="bac27-136">**Workaround**: None</span></span>

## <span data-ttu-id="bac27-137">Nella finestra di dialogo Aggiungi pacchetto della console di gestione il pulsante Sfoglia non è disponibile quando si usa Chrome o Firefox</span><span class="sxs-lookup"><span data-stu-id="bac27-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="bac27-138">Nella pagina pacchetti della console di gestione, se si fa clic su **Aggiungi o aggiorna** nell'angolo in basso a destra, viene visualizzata la finestra di dialogo **Aggiungi pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="bac27-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="bac27-139">Se si accede alla console di gestione usando Chrome o Firefox come browser, non sarà possibile passare alla posizione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bac27-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="bac27-140">**Soluzione alternativa**: digitare o copiare e incollare il percorso del pacchetto nel campo **Aggiungi pacchetto** di input.</span><span class="sxs-lookup"><span data-stu-id="bac27-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="bac27-141">Se la console di gestione ha accesso a questo percorso, sarà possibile aggiungere il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bac27-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="bac27-142">Se il pacchetto si trova in una condivisione di rete, è possibile passare alla posizione usando Esplora file eseguendo questa procedura:</span><span class="sxs-lookup"><span data-stu-id="bac27-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="bac27-143">Tenendo premuto **MAIUSC**, fare clic con il pulsante destro del mouse sul file del pacchetto</span><span class="sxs-lookup"><span data-stu-id="bac27-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="bac27-144">Selezionare **copia come percorso**</span><span class="sxs-lookup"><span data-stu-id="bac27-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="bac27-145">Incollare il percorso nel campo di input della finestra di dialogo **Aggiungi pacchetto**</span><span class="sxs-lookup"><span data-stu-id="bac27-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="bac27-146">L'aggiornamento di App-V Management Server a 5,1 talvolta non riesce con il messaggio "si è verificato un errore di database"</span><span class="sxs-lookup"><span data-stu-id="bac27-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="bac27-147">Se si installa il server di gestione SP1 App-V 5,0 e quindi si prova a eseguire l'aggiornamento a App-V 5,1 server quando più gruppi di connessioni sono configurati e abilitati, viene visualizzato l'errore seguente: "si è verificato un errore di database.</span><span class="sxs-lookup"><span data-stu-id="bac27-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="bac27-148">Motivo: "nome di colonna non valido" PackageOptional ".</span><span class="sxs-lookup"><span data-stu-id="bac27-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="bac27-149">Nome di colonna non valido "VersionOptional". "</span><span class="sxs-lookup"><span data-stu-id="bac27-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="bac27-150">**Soluzione alternativa**: eseguire questo comando nel database SQL:</span><span class="sxs-lookup"><span data-stu-id="bac27-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="bac27-151">dove "AppVManagement" è il nome del database.</span><span class="sxs-lookup"><span data-stu-id="bac27-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="bac27-152">Gli utenti non possono aprire un pacchetto in un gruppo di connessioni pubblicato dall'utente se si aggiunge o si rimuove un pacchetto facoltativo</span><span class="sxs-lookup"><span data-stu-id="bac27-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="bac27-153">Negli ambienti in cui è in uso il client RDS o con più utenti simultanei per ogni computer, gli utenti connessi non possono aprire applicazioni in pacchetti che si trovano in un gruppo di connessioni pubblicato dall'utente se un pacchetto facoltativo viene aggiunto o rimosso dal gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="bac27-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="bac27-154">**Soluzione alternativa**: gli utenti disconnettersi e quindi eseguire il log-in.</span><span class="sxs-lookup"><span data-stu-id="bac27-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="bac27-155">Il messaggio di errore viene visualizzato erroneamente quando il gruppo di connessioni viene pubblicato solo per l'utente</span><span class="sxs-lookup"><span data-stu-id="bac27-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="bac27-156">Quando si esegue Repair-AppvClientConnectionGroup, viene visualizzato il messaggio di errore seguente, anche quando il gruppo di connessioni viene pubblicato solo all'utente: "Internal App-V Integration Error: pacchetto non integrato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bac27-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="bac27-157">Assicurati che il pacchetto venga aggiunto al computer e pubblicato nell'utente. "</span><span class="sxs-lookup"><span data-stu-id="bac27-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="bac27-158">**Soluzione alternativa**: eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bac27-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="bac27-159">Pubblicare tutti i pacchetti in un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="bac27-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="bac27-160">Il problema si verifica quando il gruppo di connessioni da riparare contiene pacchetti mancanti o non disponibili per l'utente, ovvero non pubblicati a livello globale o per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bac27-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="bac27-161">Tuttavia, il ripristino funzionerà se sono disponibili tutti i pacchetti del gruppo di connessioni, quindi assicurati che tutti i pacchetti vengano pubblicati.</span><span class="sxs-lookup"><span data-stu-id="bac27-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="bac27-162">Ripristinare i pacchetti singolarmente usando il comando Repair-AppvClientPackage invece del comando Repair-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="bac27-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="bac27-163">Determinare i pacchetti disponibili per gli utenti e quindi eseguire il comando Repair-AppvClientPackage una volta per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bac27-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="bac27-164">Usare i cmdlet di PowerShell per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bac27-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="bac27-165">Ottenere tutti i pacchetti in un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="bac27-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="bac27-166">Verificare se ogni pacchetto è attualmente pubblicato.</span><span class="sxs-lookup"><span data-stu-id="bac27-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="bac27-167">Se il pacchetto è attualmente pubblicato, eseguire Repair-AppvClientPackage su tale pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bac27-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="bac27-168">Icone non visualizzate correttamente in sequencer</span><span class="sxs-lookup"><span data-stu-id="bac27-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="bac27-169">Le icone nella scheda associazioni e tipi di file non vengono visualizzate correttamente quando si modifica un pacchetto in App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="bac27-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="bac27-170">Questo problema si verifica quando le dimensioni delle icone non sono 16x16 o 32x32.</span><span class="sxs-lookup"><span data-stu-id="bac27-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="bac27-171">**Soluzione alternativa**: usare solo le icone 16x16 o 32x32.</span><span class="sxs-lookup"><span data-stu-id="bac27-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="bac27-172">Lo script InsertVersionInfo. SQL non è più necessario per il database di gestione</span><span class="sxs-lookup"><span data-stu-id="bac27-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="bac27-173">Lo script InsertVersionInfo. SQL non è necessario per le versioni del database di gestione di App-V più avanti rispetto all'App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bac27-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="bac27-174">Lo script Permissions. SQL deve essere aggiornato in base al **passaggio 2** nell' [articolo 3031340 della KB](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="bac27-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="bac27-175">**Importante** 
 Il **passaggio 1** non è necessario per le versioni di App-v successive all'app-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bac27-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="bac27-176">Microsoft Visual Studio 2012 non è supportato</span><span class="sxs-lookup"><span data-stu-id="bac27-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="bac27-177">App-V 5,1 non supporta Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="bac27-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="bac27-178">**Soluzione alternativa**: None</span><span class="sxs-lookup"><span data-stu-id="bac27-178">**Workaround**: None</span></span>

## <span data-ttu-id="bac27-179">Limitazioni del nome del file dell'applicazione per il sequencer App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="bac27-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="bac27-180">Il sequencer App-V 5. x non può sequenziare le applicazioni con nomi di file corrispondenti "CO_ &lt; x &gt; " dove x è un numero qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="bac27-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="bac27-181">Verrà generato l'errore 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="bac27-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="bac27-182">**Soluzione alternativa**: usare un nome di file diverso</span><span class="sxs-lookup"><span data-stu-id="bac27-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="bac27-183">Errore "file non trovato" intermittente durante il montaggio di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="bac27-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="bac27-184">Occasionalmente, quando si monta un pacchetto, viene generato un errore "file non trovato" (0x80070002).</span><span class="sxs-lookup"><span data-stu-id="bac27-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="bac27-185">In genere, questo problema si verifica quando una cartella in un pacchetto di App-V contiene molti file (ad esempio 20.000 o più).</span><span class="sxs-lookup"><span data-stu-id="bac27-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="bac27-186">In questo modo, il flusso può richiedere più tempo del previsto e il timeout genera l'errore "file non trovato".</span><span class="sxs-lookup"><span data-stu-id="bac27-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="bac27-187">**Soluzione alternativa**: a partire da HF06, è stata introdotta una nuova chiave del registro di sistema per consentire l'estensione del periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="bac27-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="bac27-188">Percorso</span><span class="sxs-lookup"><span data-stu-id="bac27-188">Path</span></span></td>
<td align="left"><span data-ttu-id="bac27-189">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</span><span class="sxs-lookup"><span data-stu-id="bac27-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="bac27-190">Impostazione</span><span class="sxs-lookup"><span data-stu-id="bac27-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="bac27-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="bac27-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="bac27-192">TipoDati</span><span class="sxs-lookup"><span data-stu-id="bac27-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="bac27-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="bac27-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="bac27-194">Unità</span><span class="sxs-lookup"><span data-stu-id="bac27-194">Units</span></span></td>
<td align="left"><span data-ttu-id="bac27-195">Secondi</span><span class="sxs-lookup"><span data-stu-id="bac27-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="bac27-196">Default</span><span class="sxs-lookup"><span data-stu-id="bac27-196">Default</span></span></td>
<td align="left"><span data-ttu-id="bac27-197">5</span><span class="sxs-lookup"><span data-stu-id="bac27-197">5</span></span><br />
<strong><span data-ttu-id="bac27-198">Nota </strong> : questo valore è l'impostazione predefinita se la chiave del registro di sistema non è definita o &lt; viene specificato un valore = 5.</span><span class="sxs-lookup"><span data-stu-id="bac27-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="bac27-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bac27-199">Related topics</span></span>


[<span data-ttu-id="bac27-200">Informazioni su App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="bac27-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 





