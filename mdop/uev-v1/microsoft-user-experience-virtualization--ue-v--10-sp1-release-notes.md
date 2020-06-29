---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804263"
---
# <span data-ttu-id="ccc8d-103">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ccc8d-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="ccc8d-104">Per cercare le note sulla versione di Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="ccc8d-105">Prima di installare UE-V, leggere accuratamente queste note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="ccc8d-106">Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="ccc8d-107">Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ccc8d-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="ccc8d-109">Problemi noti di UE-V</span><span class="sxs-lookup"><span data-stu-id="ccc8d-109">UE-V known issues</span></span>


<span data-ttu-id="ccc8d-110">Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="ccc8d-111">Le impostazioni del registro di sistema non riescono a eseguire la sincronizzazione tra App-V e le applicazioni native nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="ccc8d-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="ccc8d-112">Quando un computer dispone di un'applicazione disponibile sia con l'applicazione Application Virtualization (App-V) che con un'applicazione di installazione nativa installata con un Windows Installer (file con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="ccc8d-113">SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="ccc8d-114">La sincronizzazione delle impostazioni di Windows 8 non riesce quando la condivisione di rete è esterna al dominio dell'utente</span><span class="sxs-lookup"><span data-stu-id="ccc8d-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="ccc8d-115">Quando Windows® 8 tenta la sincronizzazione delle impostazioni del sistema operativo, synchrnization non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretti**.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="ccc8d-116">Questo errore può indicare che la condivisione di rete è esterna al dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="ccc8d-117">Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="ccc8d-118">Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="ccc8d-119">SOLUZIONE alternativa: usare le condivisioni di rete dello stesso dominio Active Directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="ccc8d-120">.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-120">.</span></span>

### <span data-ttu-id="ccc8d-121">Firma di posta elettronica in roaming per Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="ccc8d-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="ccc8d-122">UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="ccc8d-123">Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte/inoltri non vengono visualizzate in roaming.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="ccc8d-124">Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-V non esegue il roaming.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="ccc8d-125">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="ccc8d-126">Le impostazioni di sincronizzazione non vengono sincronizzate nell'intervallo previsto durante l'uso in modalità di collegamento lento</span><span class="sxs-lookup"><span data-stu-id="ccc8d-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="ccc8d-127">In condizioni normali i percorsi di archiviazione delle impostazioni devono essere disponibili tramite una connessione di rete a collegamento veloce.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="ccc8d-128">In modalità di collegamento lento la sincronizzazione si verificherà solo su base periodica.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="ccc8d-129">Per impostazione predefinita, la pianificazione della sincronizzazione della modalità di collegamento lenta è impostata su ogni 360 minuti.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="ccc8d-130">SOLUZIONE alternativa: per cambiare la frequenza della sincronizzazione in background per i computer in modalità di collegamento lento, è possibile configurare i criteri di gruppo per i criteri di sincronizzazione in background per **i file offline**.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="ccc8d-131">I caratteri speciali non vengono sincronizzati</span><span class="sxs-lookup"><span data-stu-id="ccc8d-131">Special characters do not synchronize</span></span>

<span data-ttu-id="ccc8d-132">Alcuni caratteri, ad esempio i simboli di valuta, non vengono sincronizzati tra i computer Windows 7 e Windows 8 che eseguono l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="ccc8d-133">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="ccc8d-134">UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="ccc8d-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="ccc8d-135">È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="ccc8d-136">Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="ccc8d-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="ccc8d-137">UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="ccc8d-138">Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="ccc8d-139">UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="ccc8d-140">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="ccc8d-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="ccc8d-141">I file MSI non sono localizzati</span><span class="sxs-lookup"><span data-stu-id="ccc8d-141">MSI’s are not localized</span></span>

<span data-ttu-id="ccc8d-142">UE-V 1,0 SP1 include un programma di configurazione localizzato per l'agente UE-V e per il generatore di UE-V.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="ccc8d-143">Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="ccc8d-144">Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="ccc8d-145">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="ccc8d-145">WORKAROUND: None</span></span>

### <span data-ttu-id="ccc8d-146">Altre cartelle della condivisione con il percorso di archiviazione delle impostazioni non sono disponibili in modalità di connessione lenta</span><span class="sxs-lookup"><span data-stu-id="ccc8d-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="ccc8d-147">Le condivisioni dell'archivio delle impostazioni non devono trovarsi in una condivisione di rete usata per altre cartelle che devono sempre essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="ccc8d-148">Quando la condivisione di rete che ospita il percorso di archiviazione dell'impostazione entra in modalità di connessione lenta, l'unica cartella disponibile è la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="ccc8d-149">Le altre cartelle della condivisione non sono disponibili in modalità di connessione lenta.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="ccc8d-150">Soluzione alternativa: None</span><span class="sxs-lookup"><span data-stu-id="ccc8d-150">Workaround: None</span></span>

### <span data-ttu-id="ccc8d-151">Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming</span><span class="sxs-lookup"><span data-stu-id="ccc8d-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="ccc8d-152">Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="ccc8d-153">SOLUZIONE alternativa: le favicon verranno visualizzate con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="ccc8d-154">I percorsi delle impostazioni dei file sono archiviati nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ccc8d-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="ccc8d-155">Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="ccc8d-156">I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="ccc8d-157">SOLUZIONE alternativa: usare il reindirizzamento delle cartelle o altre tecnologie per assicurarsi che tutti i file a cui si fa riferimento come percorsi di impostazioni file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni si aggirano.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="ccc8d-158">I percorsi di archiviazione delle impostazioni lunghe possono causare un errore</span><span class="sxs-lookup"><span data-stu-id="ccc8d-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="ccc8d-159">Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="ccc8d-160">I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="ccc8d-161">UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="ccc8d-162">Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello).</span><span class="sxs-lookup"><span data-stu-id="ccc8d-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="ccc8d-163">Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:</span><span class="sxs-lookup"><span data-stu-id="ccc8d-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="ccc8d-164">Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="ccc8d-165">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="ccc8d-166">UE-V Agent ritardi al logout o all'accesso</span><span class="sxs-lookup"><span data-stu-id="ccc8d-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="ccc8d-167">Se si verifica un accesso o un logout prima che i file offline abbiano stabilito che un collegamento lento è in posizione, la disconnessione o l'accesso potrebbero essere ritardati.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="ccc8d-168">La funzionalità file offline può richiedere fino a tre minuti per rilevare lo stato corrente della rete.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="ccc8d-169">Se l'accesso o l'arresto si verifica prima che i file offline abbiano determinato che il computer è connesso a un collegamento lento, il pacchetto di impostazioni UE-V verrà inviato al server invece della cache locale.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="ccc8d-170">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="ccc8d-171">Conflitto di impostazioni quando si prova a eseguire il roaming delle impostazioni del sistema operativo in Windows 8</span><span class="sxs-lookup"><span data-stu-id="ccc8d-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="ccc8d-172">In Windows 8 se la sincronizzazione dell'account Microsoft è abilitata insieme a UE-V per le impostazioni del sistema operativo, le impostazioni applicate potrebbero non essere coerenti.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="ccc8d-173">SOLUZIONE alternativa: eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccc8d-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="ccc8d-174">Disabilitare la sincronizzazione dell'account Microsoft se si usa UE-V per aggirare le impostazioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ccc8d-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="ccc8d-175">Disabilitare UE-V per le impostazioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ccc8d-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="ccc8d-176">Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ccc8d-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="ccc8d-177">Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici per le impostazioni locali si aggirano solo tra le versioni del sistema operativo di Windows.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="ccc8d-178">Ad esempio, i caratteri di valuta verranno spostati solo da Windows 7 a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="ccc8d-179">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="ccc8d-179">WORKAROUND: None</span></span>

 

 





