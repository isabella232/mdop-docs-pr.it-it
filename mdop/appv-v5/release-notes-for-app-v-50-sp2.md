---
title: Note sulla versione di App-V 5.0 SP2
description: Note sulla versione di App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804894"
---
# <span data-ttu-id="7fb82-103">Note sulla versione di App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fb82-103">Release Notes for App-V 5.0 SP2</span></span>


**<span data-ttu-id="7fb82-104">Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="7fb82-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="7fb82-105">Leggere accuratamente queste note sulla versione prima di installare App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fb82-105">Read these release notes thoroughly before you install App-V 5.0 SP2.</span></span>

<span data-ttu-id="7fb82-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fb82-106">These release notes contain information that is required to successfully install App-V 5.0 SP2.</span></span> <span data-ttu-id="7fb82-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb82-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="7fb82-108">Se sono presenti differenze tra queste note sulla versione e altre documentazioni di App-V 5,0, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="7fb82-108">If there are differences between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="7fb82-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb82-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="7fb82-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="7fb82-110">About the Product Documentation</span></span>


<span data-ttu-id="7fb82-111">Per informazioni sulla documentazione di App-V 5,0, vedere la Home page di App-V 5,0 in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="7fb82-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="7fb82-112">Inviare commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="7fb82-112">Provide Feedback</span></span>


<span data-ttu-id="7fb82-113">Siamo interessati a ricevere commenti e suggerimenti su App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7fb82-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="7fb82-114">È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="7fb82-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="7fb82-115">**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7fb82-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="7fb82-116">Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="7fb82-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="7fb82-117">Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="7fb82-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="7fb82-118">Problemi noti del pacchetto hotfix 4 per Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fb82-118">Known Issues with Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>


### <span data-ttu-id="7fb82-119">I pacchetti smettono di funzionare dopo la disinstallazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fb82-119">Packages stop working after you uninstall Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>

<span data-ttu-id="7fb82-120">Pacchetti pubblicati quando il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 viene applicato smette di funzionare quando viene rimosso il pacchetto hotfix 4 per Application Virtualization 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fb82-120">Packages published when Hotfix Package 4 for Application Virtualization 5.0 SP2 is applied stop working when Hotfix Package 4 for Application Virtualization 5.0 SP2 is removed.</span></span>

<span data-ttu-id="7fb82-121">SOLUZIONE</span><span class="sxs-lookup"><span data-stu-id="7fb82-121">WORKAROUND:</span></span>

<span data-ttu-id="7fb82-122">Se la cartella seguente esiste, è necessario eliminarla:</span><span class="sxs-lookup"><span data-stu-id="7fb82-122">If the following folder exists, then you must delete it:</span></span>

<span data-ttu-id="7fb82-123">**% LocalAppData%**  \\  **Microsoft**  \\  **Appv**  \\  **Client**  \\  **VFS**  \\  \*\* &lt; ID &gt; pacchetto\*\* per ogni pacchetto pubblicato.</span><span class="sxs-lookup"><span data-stu-id="7fb82-123">**%localappdata%** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **VFS** \\ **&lt;package ID&gt;** for each package that was published.</span></span>

<span data-ttu-id="7fb82-124">**Nota**  Per eliminare la cartella, è necessario disporre di privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="7fb82-124">**Note** You must have elevated privileges to delete this folder.</span></span>

 

<span data-ttu-id="7fb82-125">Per usare uno script, per ogni account utente nel computer e per ogni ID pacchetto pubblicato dopo l'installazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="7fb82-125">To use a script, for each user account on the computer and for each package id that was published after installing Hotfix Package 4 for Application Virtualization 5.0 SP2:</span></span>

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   <span data-ttu-id="7fb82-126">I tasti di scelta rapida rimarranno con le sessioni utente anche dopo l'eliminazione della cartella dalla directory nella sezione precedente, quindi è possibile fare clic sul collegamento per eseguire di nuovo l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fb82-126">The shortcuts will remain with the user sessions even after deleting the folder from the directory in the previous section, so you can click on the shortcut to run the application again.</span></span> <span data-ttu-id="7fb82-127">Non è necessario pubblicare di nuovo l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fb82-127">There is no need to re-publish the application.</span></span>

-   <span data-ttu-id="7fb82-128">Questo problema si verifica sia per i pacchetti pubblicati dall'utente che per quelli a livello globale, ad esempio Microsoft Office2013.</span><span class="sxs-lookup"><span data-stu-id="7fb82-128">This issue happens for both user published packaged and globally published packages for example, Microsoft Office2013.</span></span> <span data-ttu-id="7fb82-129">La cartella deve essere eliminata per entrambi i tipi di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7fb82-129">The folder must be deleted for both types of packages.</span></span>

-   <span data-ttu-id="7fb82-130">Non è necessario eliminare la cartella VFS nei dati dell'app roaming (**% AppData%**).</span><span class="sxs-lookup"><span data-stu-id="7fb82-130">You do not need to delete the VFS folder in the Roaming app data (**%appdata%**).</span></span> <span data-ttu-id="7fb82-131">Solo la **% LocalAppData%** deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="7fb82-131">Only the **%localappdata%** must be deleted.</span></span>

### <span data-ttu-id="7fb82-132">Punti di integrazione di Microsoft Office nella posizione errata del file System</span><span class="sxs-lookup"><span data-stu-id="7fb82-132">Microsoft Office integration points to wrong file system location</span></span>

<span data-ttu-id="7fb82-133">Punti di integrazione di Microsoft Office nella posizione errata del file System (Groove.exe messaggio di errore).</span><span class="sxs-lookup"><span data-stu-id="7fb82-133">Microsoft Office integration points to wrong file system location (Groove.exe error message).</span></span>

<span data-ttu-id="7fb82-134">SOLUZIONE</span><span class="sxs-lookup"><span data-stu-id="7fb82-134">WORKAROUND:</span></span>

<span data-ttu-id="7fb82-135">Usare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fb82-135">Use one of the following methods:</span></span>

1.  <span data-ttu-id="7fb82-136">Eliminare il collegamento nella cartella di avvio dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7fb82-136">Delete the shortcut in the start-up folder after upgrade.</span></span>

2.  <span data-ttu-id="7fb82-137">Modificare il collegamento nella cartella di avvio con uno script.</span><span class="sxs-lookup"><span data-stu-id="7fb82-137">Change the shortcut in the start-up folder using a script.</span></span>

3.  <span data-ttu-id="7fb82-138">Usa il file di configurazione della distribuzione per specificare la destinazione di collegamento alla radice di integrazione.</span><span class="sxs-lookup"><span data-stu-id="7fb82-138">Use the deployment configuration file to specify the shortcut target to the integration root.</span></span>

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> <span data-ttu-id="7fb82-139">Pacchetto hotfix 4 per il programma di installazione di Application Virtualization 5,0 SP2 può richiedere molto tempo</span><span class="sxs-lookup"><span data-stu-id="7fb82-139">Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can take a long time</span></span>

<span data-ttu-id="7fb82-140">Il pacchetto hotfix 4 per il programma di installazione di Application Virtualization 5,0 SP2 può richiedere molto tempo a seconda del numero di file archiviati nella cache del pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="7fb82-140">The Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can potentially take a long time depending on how many files are stored in the existing package cache.</span></span>

<span data-ttu-id="7fb82-141">L'aggiornamento dei descrittori di sicurezza dei pacchetti associati durante il pacchetto di hotfix 4 per l'installazione di Application Virtualization 5,0 SP2 ha un impatto significativo sul tempo necessario per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7fb82-141">Updating associated package security descriptors during the Hotfix Package 4 for Application Virtualization 5.0 SP2 installation has a significant impact on how long it takes the installation will take.</span></span> <span data-ttu-id="7fb82-142">In precedenza, l'installazione è stata standard in Duration.</span><span class="sxs-lookup"><span data-stu-id="7fb82-142">Previously, the installation install was standard in duration.</span></span> <span data-ttu-id="7fb82-143">Tuttavia, ora dipende dal numero di file che sono stati inscenati nella cache del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7fb82-143">However, it now depends on how many files you have staged in the package cache.</span></span>

<span data-ttu-id="7fb82-144">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="7fb82-144">WORKAROUND: None</span></span>

### <span data-ttu-id="7fb82-145">La disinstallazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2 non riesce se è in uso il pacchetto JIT-V</span><span class="sxs-lookup"><span data-stu-id="7fb82-145">Uninstalling Hotfix Package 4 for Application Virtualization 5.0 SP2 fails if JIT-V package is in use</span></span>

<span data-ttu-id="7fb82-146">Se si installa il pacchetto di hotfix 4 per Application Virtualization 5,0 SP2 e quindi si prova a disinstallare l'hotfix quando viene usata la virtualizzazione JIT (just-in-Time), l'operazione non riesce se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fb82-146">If you install Hotfix Package 4 for Application Virtualization 5.0 SP2 and then try to uninstall the hotfix when just-in-time virtualization (JIT-V) is being used, the operation will fail if all of the following conditions are true:</span></span>

-   <span data-ttu-id="7fb82-147">È stato installato usando un file di Windows Installer (con estensione msi) e quindi si applicano gli aggiornamenti usando un file di patch di Microsoft Installer (con estensione msp).</span><span class="sxs-lookup"><span data-stu-id="7fb82-147">You installed by using a Windows Installer file (.msi), and then you apply updates by using a Microsoft Installer Patch File (.msp).</span></span>

-   <span data-ttu-id="7fb82-148">Si prova a disinstallare un aggiornamento usando l'elemento Aggiungi o Rimuovi programmi nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="7fb82-148">You try to uninstall an update by using the Add or Remove Programs item in Control Panel.</span></span>

-   <span data-ttu-id="7fb82-149">Nel computer è in uso un pacchetto abilitato per V JIT.</span><span class="sxs-lookup"><span data-stu-id="7fb82-149">A JIT-V-enabled package is running on the computer.</span></span>

<span data-ttu-id="7fb82-150">SOLUZIONE alternativa: completare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="7fb82-150">WORKAROUND: Complete the following steps:</span></span>

1.  <span data-ttu-id="7fb82-151">Aprire Windows PowerShell ed eseguire i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fb82-151">Open Windows PowerShell and run the following commands:</span></span>

    -   **<span data-ttu-id="7fb82-152">Import-Module appvclient</span><span class="sxs-lookup"><span data-stu-id="7fb82-152">Import-module appvclient</span></span>**

    -   **<span data-ttu-id="7fb82-153">Get-AppvClientPackage | Stop-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="7fb82-153">Get-AppvClientPackage | Stop-AppvClientPackage</span></span>**

2.  <span data-ttu-id="7fb82-154">Disinstallare l'aggiornamento usando Aggiungi o Rimuovi programmi.</span><span class="sxs-lookup"><span data-stu-id="7fb82-154">Uninstall the update using Add or Remove Programs.</span></span>

## <span data-ttu-id="7fb82-155">Problemi noti di App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fb82-155">Known Issues with App-V 5.0 SP2</span></span>


### <a href="" id="bkmk-folderredirection"></a><span data-ttu-id="7fb82-156">Il reindirizzamento delle cartelle client App-V a volte non riesce a trasferire i file da% AppData% a% LocalAppData%</span><span class="sxs-lookup"><span data-stu-id="7fb82-156">App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%</span></span>

<span data-ttu-id="7fb82-157">Quando% AppData% è una cartella di rete condivisa configurata per il reindirizzamento delle cartelle, le modifiche apportate agli utenti finali a AppData (roaming) possono essere perse quando si cambia computer o quando il loro AppData locale viene deselezionato quando si disconnette e quindi si riattiva.</span><span class="sxs-lookup"><span data-stu-id="7fb82-157">When %AppData% is a shared network folder that you have configured for folder redirection, the changes that end users make to AppData (Roaming) can be lost when they switch computers or when their local AppData is cleared when they log off and then log back on.</span></span> <span data-ttu-id="7fb82-158">Questo errore si verifica perché la chiave del registro di sistema (AppDataTime), che indica l'ultimo caricamento noto, esce dalla sincronizzazione con il AppData memorizzato nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="7fb82-158">This error occurs because the registry key (AppDataTime), which indicates the last known upload, gets out of synchronization with the local cached AppData.</span></span>

<span data-ttu-id="7fb82-159">SOLUZIONE alternativa: eliminare manualmente la chiave del registro di sistema seguente per ogni pacchetto pertinente quando un utente finale effettua l'accesso o la disattivazione:</span><span class="sxs-lookup"><span data-stu-id="7fb82-159">WORKAROUND: Manually delete the following registry key for each relevant package when an end user logs on or off:</span></span>

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

<span data-ttu-id="7fb82-160">La prima volta che gli utenti finali avviano un'applicazione nel pacchetto dopo l'accesso, App-V impone il download della compressione% AppData%, anche se% LocalAppData% è già aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7fb82-160">The first time that end users start an application in the package after they log in, App-V forces a download of the zipped %AppData%, even if %LocalAppData% is already up to date.</span></span>

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> <span data-ttu-id="7fb82-161">App-V 5,0 Service Pack 2 (App-V 5,0 SP2) non include una nuova versione di App-V Server</span><span class="sxs-lookup"><span data-stu-id="7fb82-161">App-V 5.0 Service Pack 2 (App-V 5.0 SP2) does not include a new version of the App-V Server</span></span>

<span data-ttu-id="7fb82-162">App-V 5.0 SP2 non include una nuova versione del server App-V.</span><span class="sxs-lookup"><span data-stu-id="7fb82-162">App-V 5.0SP2 does not include a new version of the App-V Server.</span></span> <span data-ttu-id="7fb82-163">Se si distribuiscono client App-V 5,0 SP2 che usano Windows 8,1 nell'ambiente e si prevede di gestire i client con l'infrastruttura App-V, è necessario installare il [pacchetto hotfix 2 per Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span><span class="sxs-lookup"><span data-stu-id="7fb82-163">If you deploy App-V 5.0 SP2 clients running Windows 8.1 in your environment and plan to manage the clients using the App-V infrastructure, you must install [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span></span> <span data-ttu-id="7fb82-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span><span class="sxs-lookup"><span data-stu-id="7fb82-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span></span>

<span data-ttu-id="7fb82-165">Se si esegue e si gestiscono client App-V 5,0 SP2 con uno dei metodi seguenti, non è necessario alcun aggiornamento client:</span><span class="sxs-lookup"><span data-stu-id="7fb82-165">If you are running and managing App-V 5.0 SP2 clients using any of the following methods no client update is required:</span></span>

-   <span data-ttu-id="7fb82-166">Modalità autonoma</span><span class="sxs-lookup"><span data-stu-id="7fb82-166">Standalone mode.</span></span>

-   <span data-ttu-id="7fb82-167">Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7fb82-167">Configuration Manager.</span></span>

-   <span data-ttu-id="7fb82-168">ESD di terze parti.</span><span class="sxs-lookup"><span data-stu-id="7fb82-168">Third party ESD.</span></span>

<span data-ttu-id="7fb82-169">Il client App-V 5,0 SP2 è completamente compatibile con Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7fb82-169">The App-V 5.0 SP2 client is fully compatible with Windows 8.1</span></span>

<span data-ttu-id="7fb82-170">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="7fb82-170">WORKAROUND: None.</span></span>

## <span data-ttu-id="7fb82-171">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="7fb82-171">Release Notes Copyright Information</span></span>


<span data-ttu-id="7fb82-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="7fb82-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="7fb82-173">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="7fb82-173">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="7fb82-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fb82-174">Related topics</span></span>


[<span data-ttu-id="7fb82-175">Informazioni su App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fb82-175">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

 

 





