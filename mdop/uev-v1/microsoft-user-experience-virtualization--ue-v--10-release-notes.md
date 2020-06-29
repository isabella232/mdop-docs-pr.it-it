---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804264"
---
# <span data-ttu-id="0c897-103">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="0c897-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="0c897-104">Per eseguire ricerche nelle note sulla versione di Microsoft User Experience Virtualization (UE-V), premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="0c897-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="0c897-105">Prima di installare UE-V, leggere accuratamente queste note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="0c897-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="0c897-106">Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0c897-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="0c897-107">Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="0c897-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="0c897-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="0c897-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="0c897-109">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="0c897-109">Providing feedback</span></span>


<span data-ttu-id="0c897-110">Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti.</span><span class="sxs-lookup"><span data-stu-id="0c897-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="0c897-111">Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="0c897-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="0c897-112">Problemi noti di UE-V</span><span class="sxs-lookup"><span data-stu-id="0c897-112">UE-V known issues</span></span>


<span data-ttu-id="0c897-113">Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="0c897-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="0c897-114">Le impostazioni del registro di sistema non riescono a eseguire la sincronizzazione tra App-V e le applicazioni native nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="0c897-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="0c897-115">Quando un computer dispone di un'applicazione disponibile sia con l'applicazione Application Virtualization (App-V) che con un'applicazione di installazione nativa (installata con un file MSI), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.</span><span class="sxs-lookup"><span data-stu-id="0c897-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="0c897-116">SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.</span><span class="sxs-lookup"><span data-stu-id="0c897-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="0c897-117">La sincronizzazione delle impostazioni di Windows 8 non riesce con errore: "Boost:: filesystem:: exists:: nome utente o password non corretto"</span><span class="sxs-lookup"><span data-stu-id="0c897-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="0c897-118">La sincronizzazione delle impostazioni del sistema operativo Windows® 8 non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretti**.</span><span class="sxs-lookup"><span data-stu-id="0c897-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="0c897-119">Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="0c897-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="0c897-120">Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c897-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="0c897-121">In caso contrario, potrebbe verificarsi l'errore seguente: "nome utente o password errati".</span><span class="sxs-lookup"><span data-stu-id="0c897-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="0c897-122">SOLUZIONE alternativa: usare le condivisioni di rete dello stesso dominio Active Directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c897-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="0c897-123">.</span><span class="sxs-lookup"><span data-stu-id="0c897-123">.</span></span>

### <span data-ttu-id="0c897-124">Firma di posta elettronica in roaming per Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="0c897-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="0c897-125">UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0c897-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="0c897-126">Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte/inoltri non lo sono.</span><span class="sxs-lookup"><span data-stu-id="0c897-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="0c897-127">Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-Vdoes non è in roaming.</span><span class="sxs-lookup"><span data-stu-id="0c897-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="0c897-128">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="0c897-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="0c897-129">Le impostazioni di sincronizzazione non vengono sincronizzate nell'intervallo previsto durante l'uso in modalità di collegamento lento</span><span class="sxs-lookup"><span data-stu-id="0c897-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="0c897-130">In condizioni normali i percorsi di archiviazione delle impostazioni devono essere disponibili tramite una connessione di rete a collegamento veloce.</span><span class="sxs-lookup"><span data-stu-id="0c897-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="0c897-131">In modalità di collegamento lento la sincronizzazione si verificherà solo su base periodica.</span><span class="sxs-lookup"><span data-stu-id="0c897-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="0c897-132">Per impostazione predefinita, la pianificazione della sincronizzazione della modalità di collegamento lenta è impostata su ogni 360 minuti.</span><span class="sxs-lookup"><span data-stu-id="0c897-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="0c897-133">SOLUZIONE alternativa: per cambiare la frequenza della sincronizzazione in background per i computer in modalità di collegamento lento, è possibile configurare i criteri di gruppo per i criteri di sincronizzazione in background per **i file offline**.</span><span class="sxs-lookup"><span data-stu-id="0c897-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="0c897-134">I caratteri speciali non vengono sincronizzati</span><span class="sxs-lookup"><span data-stu-id="0c897-134">Special characters do not synchronize</span></span>

<span data-ttu-id="0c897-135">Alcuni caratteri, ad esempio i simboli di valuta, non vengono sincronizzati tra i computer Windows 7 e Windows 8 che eseguono l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="0c897-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="0c897-136">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="0c897-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="0c897-137">UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="0c897-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="0c897-138">È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0c897-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="0c897-139">Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui.</span><span class="sxs-lookup"><span data-stu-id="0c897-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="0c897-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="0c897-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="0c897-141">UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica.</span><span class="sxs-lookup"><span data-stu-id="0c897-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="0c897-142">Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0c897-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="0c897-143">UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0c897-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="0c897-144">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="0c897-144">WORKAROUND: None</span></span>

### <span data-ttu-id="0c897-145">Altre cartelle della condivisione con il percorso di archiviazione delle impostazioni non sono disponibili in modalità di connessione lenta</span><span class="sxs-lookup"><span data-stu-id="0c897-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="0c897-146">Le condivisioni dell'archivio delle impostazioni non devono trovarsi in una condivisione di rete usata per altre cartelle che devono sempre essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c897-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="0c897-147">Quando la condivisione di rete che ospita il percorso di archiviazione dell'impostazione entra in modalità di connessione lenta, l'unica cartella disponibile è la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0c897-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="0c897-148">Le altre cartelle della condivisione non sono disponibili in modalità di connessione lenta.</span><span class="sxs-lookup"><span data-stu-id="0c897-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="0c897-149">Soluzione alternativa: None</span><span class="sxs-lookup"><span data-stu-id="0c897-149">Workaround: None</span></span>

### <span data-ttu-id="0c897-150">Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming</span><span class="sxs-lookup"><span data-stu-id="0c897-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="0c897-151">Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="0c897-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="0c897-152">SOLUZIONE alternativa: le favicon verranno visualizzate con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0c897-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="0c897-153">I percorsi delle impostazioni dei file sono archiviati nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0c897-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="0c897-154">Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0c897-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="0c897-155">I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="0c897-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="0c897-156">SOLUZIONE alternativa: usare il reindirizzamento delle cartelle o altre tecnologie per assicurarsi che tutti i file a cui si fa riferimento come percorsi di impostazioni file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni si aggirano.</span><span class="sxs-lookup"><span data-stu-id="0c897-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="0c897-157">I percorsi più lunghi di 260 caratteri non sono supportati</span><span class="sxs-lookup"><span data-stu-id="0c897-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="0c897-158">I percorsi di archiviazione delle impostazioni con più di 260 caratteri non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0c897-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="0c897-159">La copia dei pacchetti di impostazioni UE-V in percorsi di archiviazione delle impostazioni che superano i 260 caratteri non riesce e genera il messaggio di eccezione seguente nel log eventi operativo UE-V: **\ [Boost:: filesystem:: Copy \ _file: il sistema non riesce a trovare il percorso specificato \]**.</span><span class="sxs-lookup"><span data-stu-id="0c897-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="0c897-160">Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="0c897-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="0c897-161">I percorsi delle impostazioni dei file con più di 260 caratteri non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="0c897-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="0c897-162">Le impostazioni dei file a cui si fa riferimento nei modelli di posizione delle impostazioni di UE-V non possono essere posizionate in un percorso di directory che supera i 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0c897-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="0c897-163">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="0c897-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="0c897-164">UE-V Agent ritardi al logout o all'accesso</span><span class="sxs-lookup"><span data-stu-id="0c897-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="0c897-165">Se si verifica un accesso o un logout prima che i file offline abbiano stabilito che un collegamento lento è in posizione, la disconnessione o l'accesso potrebbero essere ritardati.</span><span class="sxs-lookup"><span data-stu-id="0c897-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="0c897-166">La funzionalità file offline può richiedere fino a tre minuti per rilevare lo stato corrente della rete.</span><span class="sxs-lookup"><span data-stu-id="0c897-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="0c897-167">Se l'accesso o l'arresto si verifica prima che i file offline abbiano determinato che il computer è connesso a un collegamento lento, il pacchetto di impostazioni UE-V verrà inviato al server invece della cache locale.</span><span class="sxs-lookup"><span data-stu-id="0c897-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="0c897-168">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="0c897-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="0c897-169">Conflitto di impostazioni quando si prova a eseguire il roaming delle impostazioni del sistema operativo in Windows 8</span><span class="sxs-lookup"><span data-stu-id="0c897-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="0c897-170">In Windows 8 se la sincronizzazione dell'account Microsoft è abilitata insieme a UE-V per le impostazioni del sistema operativo, le impostazioni applicate potrebbero non essere coerenti.</span><span class="sxs-lookup"><span data-stu-id="0c897-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="0c897-171">SOLUZIONE alternativa: eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c897-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="0c897-172">Disabilitare la sincronizzazione dell'account Microsoft se si usa UE-V per aggirare le impostazioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0c897-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="0c897-173">Disabilitare UE-V per le impostazioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0c897-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="0c897-174">Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0c897-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="0c897-175">Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici per le impostazioni locali si aggirano solo tra le versioni del sistema operativo di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c897-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="0c897-176">Ad esempio, i caratteri di valuta verranno spostati solo da Windows 7 a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c897-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="0c897-177">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="0c897-177">WORKAROUND: None</span></span>

### <span data-ttu-id="0c897-178">I segnalibri di Internet Explorer non vengono visualizzati in Internet Explorer SmartBar</span><span class="sxs-lookup"><span data-stu-id="0c897-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="0c897-179">Quando i segnalibri di Internet Explorer si spostano da un computer a un altro, l'indice nel secondo computer non può essere aggiornato, quindi quando si digita la barra degli indirizzi, il favorito non viene visualizzato come risultato di ricerca nel computer 2.</span><span class="sxs-lookup"><span data-stu-id="0c897-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="0c897-180">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="0c897-180">WORKAROUND: None</span></span>

 

 





