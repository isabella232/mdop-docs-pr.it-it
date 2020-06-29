---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825285"
---
# <span data-ttu-id="a77d9-103">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="a77d9-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="a77d9-104">Per cercare le note sulla versione di Microsoft User Experience Virtualization (UE-V) 2,0, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="a77d9-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="a77d9-105">Prima di installare UE-V, leggere accuratamente queste note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="a77d9-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="a77d9-106">Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a77d9-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="a77d9-107">Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="a77d9-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="a77d9-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="a77d9-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="a77d9-109">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="a77d9-109">Providing feedback</span></span>


<span data-ttu-id="a77d9-110">Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti.</span><span class="sxs-lookup"><span data-stu-id="a77d9-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="a77d9-111">Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="a77d9-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="a77d9-112">Problemi noti di UE-V</span><span class="sxs-lookup"><span data-stu-id="a77d9-112">UE-V known issues</span></span>


<span data-ttu-id="a77d9-113">Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="a77d9-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="a77d9-114">Le impostazioni del registro di sistema non vengono sincronizzate tra App-V e le applicazioni native nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="a77d9-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="a77d9-115">Quando un computer dispone di un'applicazione installata sia tramite Application Virtualization (App-V) che in locale con un file di Windows Installer (con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.</span><span class="sxs-lookup"><span data-stu-id="a77d9-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="a77d9-116">**Soluzione alternativa:** Per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.</span><span class="sxs-lookup"><span data-stu-id="a77d9-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="a77d9-117">Le impostazioni non vengono sincronizzate quando la condivisione di rete è esterna al dominio dell'utente</span><span class="sxs-lookup"><span data-stu-id="a77d9-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="a77d9-118">Quando Windows® 8 tenta la sincronizzazione delle impostazioni del sistema operativo, la sincronizzazione non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretto**.</span><span class="sxs-lookup"><span data-stu-id="a77d9-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="a77d9-119">Questo errore può indicare che la condivisione di rete si trova all'esterno del dominio dell'utente o di un dominio con una relazione di trust con tale dominio.</span><span class="sxs-lookup"><span data-stu-id="a77d9-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="a77d9-120">Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="a77d9-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="a77d9-121">Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente o di un dominio attendibile del dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a77d9-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="a77d9-122">**Soluzione alternativa:** Usare le condivisioni di rete dello stesso dominio Active Directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a77d9-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="a77d9-123">Risultati imprevedibili con Office 2010 e Office 2013 installati</span><span class="sxs-lookup"><span data-stu-id="a77d9-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="a77d9-124">Quando un utente ha installato sia Office 2010 che Office 2013, tutte le impostazioni comuni tra le due versioni di Office sono in roaming da UE-V.</span><span class="sxs-lookup"><span data-stu-id="a77d9-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="a77d9-125">In questo modo, le dimensioni del pacchetto di Office 2010 possono essere abbastanza grandi o causare conflitti imprevedibili con 2013, in particolare se si usa Office 365.</span><span class="sxs-lookup"><span data-stu-id="a77d9-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="a77d9-126">**Soluzione alternativa:** Installare solo una versione di Office o limitare le impostazioni sincronizzate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="a77d9-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="a77d9-127">La disinstallazione e la reinstallazione dell'app di Windows 8 ripristinano le impostazioni sullo stato iniziale</span><span class="sxs-lookup"><span data-stu-id="a77d9-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="a77d9-128">Durante l'uso della sincronizzazione delle impostazioni di UE-V per un'app di Windows 8, se l'utente disinstalla l'app e quindi reinstalla l'app, le impostazioni dell'app ripristinano i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a77d9-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="a77d9-129">Questo avviene perché la disinstallazione rimuove la copia locale (memorizzata nella cache) delle impostazioni dell'app, ma non rimuove il pacchetto di impostazioni locali UE-V.</span><span class="sxs-lookup"><span data-stu-id="a77d9-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="a77d9-130">Quando l'app viene reinstallata e avviata, UE-V raccoglie le impostazioni dell'app che sono state reimpostate per impostazione predefinita e quindi carica le impostazioni predefinite nella posizione di archiviazione centrale.</span><span class="sxs-lookup"><span data-stu-id="a77d9-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="a77d9-131">Altri computer che eseguono l'app scaricano le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="a77d9-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="a77d9-132">Questo comportamento è identico al comportamento delle applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="a77d9-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="a77d9-133">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="a77d9-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="a77d9-134">Firma di posta elettronica in roaming per Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="a77d9-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="a77d9-135">UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a77d9-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="a77d9-136">Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte o gli inoltri non vengono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="a77d9-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="a77d9-137">Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-V non esegue il roaming.</span><span class="sxs-lookup"><span data-stu-id="a77d9-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="a77d9-138">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="a77d9-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="a77d9-139">UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="a77d9-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="a77d9-140">È consigliabile installare la versione a 64 bit di Microsoft Office per i computer moderni.</span><span class="sxs-lookup"><span data-stu-id="a77d9-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="a77d9-141">Per determinare la versione di cui si ha bisogno, [fare clic qui](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="a77d9-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="a77d9-142">UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica.</span><span class="sxs-lookup"><span data-stu-id="a77d9-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="a77d9-143">Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a77d9-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="a77d9-144">UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a77d9-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="a77d9-145">**Soluzione alternativa:** Nessuno</span><span class="sxs-lookup"><span data-stu-id="a77d9-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="a77d9-146">I file MSI non sono localizzati</span><span class="sxs-lookup"><span data-stu-id="a77d9-146">MSI’s are not localized</span></span>

<span data-ttu-id="a77d9-147">UE-V 2,0 include un programma di configurazione localizzato sia per l'agente UE-V che per il generatore di UE-V.</span><span class="sxs-lookup"><span data-stu-id="a77d9-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="a77d9-148">Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="a77d9-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="a77d9-149">Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a77d9-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="a77d9-150">**Soluzione alternativa:** Nessuno</span><span class="sxs-lookup"><span data-stu-id="a77d9-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="a77d9-151">Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming</span><span class="sxs-lookup"><span data-stu-id="a77d9-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="a77d9-152">Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="a77d9-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="a77d9-153">**Soluzione alternativa:** I favicon verranno visualizzati con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a77d9-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="a77d9-154">I percorsi delle impostazioni dei file sono archiviati nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a77d9-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="a77d9-155">Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a77d9-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="a77d9-156">I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="a77d9-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="a77d9-157">**Soluzione alternativa:** Usa il reindirizzamento delle cartelle o altre tecnologie per assicurarti che tutti i file a cui si fa riferimento come percorsi delle impostazioni dei file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni sono in roaming.</span><span class="sxs-lookup"><span data-stu-id="a77d9-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="a77d9-158">I percorsi di archiviazione delle impostazioni lunghe possono causare un errore</span><span class="sxs-lookup"><span data-stu-id="a77d9-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="a77d9-159">Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a77d9-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="a77d9-160">I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a77d9-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="a77d9-161">UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a77d9-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="a77d9-162">Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="a77d9-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="a77d9-163">Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:</span><span class="sxs-lookup"><span data-stu-id="a77d9-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="a77d9-164">Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.</span><span class="sxs-lookup"><span data-stu-id="a77d9-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="a77d9-165">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="a77d9-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="a77d9-166">Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a77d9-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="a77d9-167">Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici delle impostazioni locali (ad esempio, lingua e opzioni internazionali) verranno spostati solo tra le versioni del sistema operativo di Windows.</span><span class="sxs-lookup"><span data-stu-id="a77d9-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="a77d9-168">Ad esempio, i caratteri di valuta non verranno spostati tra Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a77d9-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="a77d9-169">**Soluzione alternativa:** Nessuno</span><span class="sxs-lookup"><span data-stu-id="a77d9-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="a77d9-170">Le app di Windows 8 non sincronizzano le impostazioni quando l'app viene riavviata dopo la chiusura in modo imprevisto</span><span class="sxs-lookup"><span data-stu-id="a77d9-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="a77d9-171">Se un'app di Windows 8 si chiude in modo imprevisto subito dopo l'avvio, le impostazioni per l'applicazione potrebbero non essere sincronizzate quando l'applicazione viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="a77d9-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="a77d9-172">**Soluzione alternativa:** Chiudere l'app di Windows 8, chiudere e riavviare l'applicazione UevAppMonitor.exe (può usare TaskManager) e quindi riavviare l'app di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a77d9-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="a77d9-173">L'agente UE-V 1 genera errori durante l'uso di modelli UE-V 2</span><span class="sxs-lookup"><span data-stu-id="a77d9-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="a77d9-174">Se un modello di posizione delle impostazioni dell'UE-V 2 viene distribuito in un computer installato con un agente UE-V 1, alcune impostazioni non riescono a eseguire la sincronizzazione tra i computer e l'agente segnala gli errori nel log eventi.</span><span class="sxs-lookup"><span data-stu-id="a77d9-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="a77d9-175">**Soluzione alternativa:** Quando si esegue la migrazione da UE-V 1 a UE-V 2 ed è probabile che i computer che eseguono la versione precedente dell'agente creino un catalogo UE-V 2,0 separato per supportare l'agente e i modelli di UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="a77d9-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="a77d9-176">Aggiornamenti rapidi e articoli della Knowledge base per UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="a77d9-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="a77d9-177">Questa sezione contiene gli hotfix e gli articoli della KB per la versione UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="a77d9-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="a77d9-178">Articolo KB</span><span class="sxs-lookup"><span data-stu-id="a77d9-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="a77d9-179">Title</span><span class="sxs-lookup"><span data-stu-id="a77d9-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="a77d9-180">Link</span><span class="sxs-lookup"><span data-stu-id="a77d9-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-181">2927019</span><span class="sxs-lookup"><span data-stu-id="a77d9-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-182">Pacchetto hotfix 1 per Microsoft User Experience Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="a77d9-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="a77d9-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="a77d9-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-184">2903501</span><span class="sxs-lookup"><span data-stu-id="a77d9-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-185">UE-V: compatibilità con l'esperienza utente per la virtualizzazione (UE-V) con i profili utente</span><span class="sxs-lookup"><span data-stu-id="a77d9-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="a77d9-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-187">2770042</span><span class="sxs-lookup"><span data-stu-id="a77d9-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-188">Impostazioni del registro di sistema UE-V</span><span class="sxs-lookup"><span data-stu-id="a77d9-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="a77d9-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-190">2847017</span><span class="sxs-lookup"><span data-stu-id="a77d9-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-191">Impostazioni UE-V replicate da Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a77d9-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="a77d9-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-193">2930271</span><span class="sxs-lookup"><span data-stu-id="a77d9-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-194">Informazioni sulle limitazioni delle firme di Outlook in roaming in Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="a77d9-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="a77d9-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-196">2769631</span><span class="sxs-lookup"><span data-stu-id="a77d9-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-197">Come ripristinare un'installazione di UE-V danneggiata</span><span class="sxs-lookup"><span data-stu-id="a77d9-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="a77d9-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-199">2850989</span><span class="sxs-lookup"><span data-stu-id="a77d9-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-200">La migrazione dei profili MAPI con Microsoft UE-V non è supportata</span><span class="sxs-lookup"><span data-stu-id="a77d9-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="a77d9-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-202">2769586</span><span class="sxs-lookup"><span data-stu-id="a77d9-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-203">UE-V aggira le cartelle vuote e le chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a77d9-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="a77d9-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-205">2782997</span><span class="sxs-lookup"><span data-stu-id="a77d9-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-206">Come abilitare la registrazione di debug in Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="a77d9-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="a77d9-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-208">2769570</span><span class="sxs-lookup"><span data-stu-id="a77d9-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-209">UE-V non aggiorna il tema nelle sessioni RDS o VDI</span><span class="sxs-lookup"><span data-stu-id="a77d9-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="a77d9-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-211">2901856</span><span class="sxs-lookup"><span data-stu-id="a77d9-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-212">Le impostazioni dell'applicazione non vengono sincronizzate dopo la forza di un riavvio in un computer con supporto UE-V</span><span class="sxs-lookup"><span data-stu-id="a77d9-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="a77d9-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-214">2850582</span><span class="sxs-lookup"><span data-stu-id="a77d9-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-215">Come usare la virtualizzazione dell'esperienza utente Microsoft con le applicazioni App-V</span><span class="sxs-lookup"><span data-stu-id="a77d9-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="a77d9-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a77d9-217">3041879</span><span class="sxs-lookup"><span data-stu-id="a77d9-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-218">Versioni di file correnti per la virtualizzazione dell'esperienza utente Microsoft</span><span class="sxs-lookup"><span data-stu-id="a77d9-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="a77d9-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a77d9-220">2843592</span><span class="sxs-lookup"><span data-stu-id="a77d9-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="a77d9-221">Informazioni sulla virtualizzazione dell'esperienza utente e disponibilità elevata</span><span class="sxs-lookup"><span data-stu-id="a77d9-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="a77d9-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="a77d9-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





