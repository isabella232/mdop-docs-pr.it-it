---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1
author: dansimp
ms.assetid: 79a36c77-fa0c-4651-8028-4a79763a2fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0677dda93f2c2dc60ec627ae0c3f4bd8c199db6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825276"
---
# <span data-ttu-id="f9784-103">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="f9784-103">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>


<span data-ttu-id="f9784-104">Per cercare le note sulla versione di Microsoft User Experience Virtualization (UE-V) 2,0, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="f9784-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="f9784-105">Prima di installare UE-V, leggere accuratamente queste note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="f9784-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="f9784-106">Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f9784-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="f9784-107">Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="f9784-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="f9784-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="f9784-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="f9784-109">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="f9784-109">Providing feedback</span></span>


<span data-ttu-id="f9784-110">Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti.</span><span class="sxs-lookup"><span data-stu-id="f9784-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="f9784-111">Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="f9784-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="f9784-112">Problemi noti di UE-V</span><span class="sxs-lookup"><span data-stu-id="f9784-112">UE-V known issues</span></span>


<span data-ttu-id="f9784-113">Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="f9784-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="f9784-114">I modelli di posizione delle impostazioni UE-V per Skype causano un arresto anomalo di Skype</span><span class="sxs-lookup"><span data-stu-id="f9784-114">UE-V settings location templates for Skype cause Skype to crash</span></span>

<span data-ttu-id="f9784-115">Quando un utente genera un modello di posizione di impostazioni valido per l'applicazione desktop Skype, lo registra e quindi avvia l'applicazione desktop Skype, Skype si arresta in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="f9784-115">When a user generates a valid settings location template for the Skype desktop application, registers it, and then launches the Skype desktop application, Skype crashes.</span></span> <span data-ttu-id="f9784-116">Nel registro eventi applicazione viene registrato un ACCESS \ _VIOLATION.</span><span class="sxs-lookup"><span data-stu-id="f9784-116">An ACCESS\_VIOLATION is recorded in the Application Event Log.</span></span>

<span data-ttu-id="f9784-117">SOLUZIONE alternativa: rimuovere o annullare la registrazione del modello Skype per consentire l'utilizzo di Skype.</span><span class="sxs-lookup"><span data-stu-id="f9784-117">WORKAROUND: Remove or unregister the Skype template to allow Skype to work again.</span></span>

### <span data-ttu-id="f9784-118">Gli script esistenti per le installazioni silent di UE-V potrebbero non riuscire</span><span class="sxs-lookup"><span data-stu-id="f9784-118">Existing scripts for silent installations of UE-V may fail</span></span>

<span data-ttu-id="f9784-119">Due modifiche apportate al programma di installazione di UE-V possono causare errori durante l'installazione di UE-v 2,1 per le versioni precedenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-119">Two changes made to the UE-V installer can cause silent installation scripts that worked for previous versions of UE-V to fail when installing UE-V 2.1.</span></span> <span data-ttu-id="f9784-120">Il primo è un nuovo requisito che gli utenti devono accettare le condizioni di licenza e accettare o rifiutare la partecipazione al programma Customer Experience Improvement Program (analisi utilizzo software), anche durante un'installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="f9784-120">The first is a new requirement that users must accept the license terms and agree to or decline participation in the Customer Experience Improvement Program (CEIP), even during a silent installation.</span></span> <span data-ttu-id="f9784-121">L'uso del parametro/q non è più sufficiente per indicare l'accettazione delle condizioni di licenza e dell'accordo per partecipare a analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="f9784-121">Using the /q parameter is no longer sufficient to indicate acceptance of the license terms and agreement to participate in CEIP.</span></span>

<span data-ttu-id="f9784-122">In secondo luogo, il programma di installazione forza il riavvio del computer dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-122">Second, the installer now forces a computer restart after installing the UE-V Agent.</span></span> <span data-ttu-id="f9784-123">Ciò può causare un errore di installazione dello script se non si prevede che il riavvio (ad esempio, installa l'agente UE-V prima di tutto e quindi installa immediatamente il generatore).</span><span class="sxs-lookup"><span data-stu-id="f9784-123">This can cause an install script to fail if it is not expecting the restart (for example, it installs the UE-V Agent first and then immediately installs the generator).</span></span>

<span data-ttu-id="f9784-124">SOLUZIONE alternativa: il programma di installazione di UE-V (con estensione msi) include due nuovi parametri della riga di comando che supportano le installazioni silent.</span><span class="sxs-lookup"><span data-stu-id="f9784-124">WORKAROUND: The UE-V installer (.msi) has two new command-line parameters that support silent installations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f9784-125">Parametro</span><span class="sxs-lookup"><span data-stu-id="f9784-125">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f9784-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9784-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f9784-127">/ACCEPTLICENSETERMS = true</span><span class="sxs-lookup"><span data-stu-id="f9784-127">/ACCEPTLICENSETERMS=True</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f9784-128">Imposta questo parametro su <strong> true </strong> per installare la versione UE-V in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="f9784-128">Set this parameter to <strong>True</strong> to install UE-V silently.</span></span> <span data-ttu-id="f9784-129">L'aggiunta di questo parametro implica che l'utente accetti le condizioni di licenza UE-V trovate (per impostazione predefinita) qui:%programmi%\Microsoft User Experience Virtualization\Agent</span><span class="sxs-lookup"><span data-stu-id="f9784-129">Adding this parameter implies that the user accepts the UE-V license terms, which are found (by default) here: %ProgramFiles%\Microsoft User Experience Virtualization\Agent</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f9784-130">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="f9784-130">/NORESTART</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f9784-131">Questo parametro impedisce il riavvio obbligatorio dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-131">This parameter prevents the mandatory restart after the UE-V agent is installed.</span></span> <span data-ttu-id="f9784-132">Un codice restituito di 3010 indica che è necessario un riavvio prima di usare UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-132">A return code of 3010 indicates that a restart is required prior to using UE-V.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f9784-133">Le impostazioni del registro di sistema non vengono sincronizzate tra App-V e le applicazioni native nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="f9784-133">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="f9784-134">Quando un computer ha un'applicazione installata sia tramite Application Virtualization (App-V) che localmente con un file di Windows Installer (con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.</span><span class="sxs-lookup"><span data-stu-id="f9784-134">When a computer has an application that is installed through both Application Virtualization (App-V) and locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="f9784-135">SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.</span><span class="sxs-lookup"><span data-stu-id="f9784-135">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="f9784-136">Risultati imprevedibili con Office 2010 e Office 2013 installati</span><span class="sxs-lookup"><span data-stu-id="f9784-136">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="f9784-137">Quando un utente ha installato sia Office 2010 che Office 2013, tutte le impostazioni comuni tra le due versioni di Office sono in roaming da UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-137">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="f9784-138">In questo modo, le dimensioni del pacchetto di Office 2010 possono essere abbastanza grandi o causare conflitti imprevedibili con 2013, in particolare se si usa Office 365.</span><span class="sxs-lookup"><span data-stu-id="f9784-138">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="f9784-139">SOLUZIONE alternativa: installare solo una versione di Office o limitare le impostazioni sincronizzate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-139">WORKAROUND: Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="f9784-140">La disinstallazione e la reinstallazione dell'app di Windows 8 ripristinano le impostazioni sullo stato iniziale</span><span class="sxs-lookup"><span data-stu-id="f9784-140">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="f9784-141">Durante l'uso della sincronizzazione delle impostazioni di UE-V per un'app di Windows 8, se l'utente disinstalla l'app e quindi reinstalla l'app, le impostazioni dell'app ripristinano i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f9784-141">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="f9784-142">Questo avviene perché la disinstallazione rimuove la copia locale (memorizzata nella cache) delle impostazioni dell'app, ma non rimuove il pacchetto di impostazioni locali UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-142"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="f9784-143">Quando l'app viene reinstallata e avviata, UE-V raccoglie le impostazioni dell'app che sono state reimpostate per impostazione predefinita e quindi carica le impostazioni predefinite nella posizione di archiviazione centrale.</span><span class="sxs-lookup"><span data-stu-id="f9784-143"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="f9784-144">Altri computer che eseguono l'app scaricano le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="f9784-144"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="f9784-145">Questo comportamento è identico al comportamento delle applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="f9784-145"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="f9784-146">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="f9784-146">WORKAROUND: None.</span></span>

### <span data-ttu-id="f9784-147">UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="f9784-147">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="f9784-148">È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f9784-148">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="f9784-149">Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui.</span><span class="sxs-lookup"><span data-stu-id="f9784-149">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="f9784-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="f9784-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="f9784-151">UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica.</span><span class="sxs-lookup"><span data-stu-id="f9784-151">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="f9784-152">Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f9784-152">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="f9784-153">UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f9784-153">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="f9784-154">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="f9784-154">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="f9784-155">I file MSI non sono localizzati</span><span class="sxs-lookup"><span data-stu-id="f9784-155">MSI’s are not localized</span></span>

<span data-ttu-id="f9784-156">UE-V 2,0 include un programma di configurazione localizzato sia per l'agente UE-V che per il generatore di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9784-156">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="f9784-157">Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="f9784-157">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="f9784-158">Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f9784-158">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="f9784-159">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="f9784-159">WORKAROUND: None</span></span>

### <span data-ttu-id="f9784-160">Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming</span><span class="sxs-lookup"><span data-stu-id="f9784-160">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="f9784-161">Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="f9784-161">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="f9784-162">SOLUZIONE alternativa: le favicon verranno visualizzate con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f9784-162">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="f9784-163">I percorsi delle impostazioni dei file sono archiviati nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f9784-163">File settings paths are stored in registry</span></span>

<span data-ttu-id="f9784-164">Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f9784-164">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="f9784-165">I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="f9784-165">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="f9784-166">SOLUZIONE alternativa: usare il reindirizzamento delle cartelle o altre tecnologie per assicurarsi che tutti i file a cui si fa riferimento come percorsi di impostazioni file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni si aggirano.</span><span class="sxs-lookup"><span data-stu-id="f9784-166">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="f9784-167">I percorsi di archiviazione delle impostazioni lunghe possono causare un errore</span><span class="sxs-lookup"><span data-stu-id="f9784-167">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="f9784-168">Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9784-168">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="f9784-169">I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f9784-169">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="f9784-170">UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9784-170">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="f9784-171">Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="f9784-171">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="f9784-172">Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:</span><span class="sxs-lookup"><span data-stu-id="f9784-172">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="f9784-173">Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.</span><span class="sxs-lookup"><span data-stu-id="f9784-173">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="f9784-174">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="f9784-174">WORKAROUND: None.</span></span>

### <span data-ttu-id="f9784-175">Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f9784-175">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="f9784-176">Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici delle impostazioni locali (ad esempio, lingua e opzioni internazionali) verranno spostati solo tra le versioni del sistema operativo di Windows.</span><span class="sxs-lookup"><span data-stu-id="f9784-176">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="f9784-177">Ad esempio, i caratteri di valuta non verranno spostati tra Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9784-177">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="f9784-178">SOLUZIONE alternativa: None</span><span class="sxs-lookup"><span data-stu-id="f9784-178">WORKAROUND: None</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="f9784-179">L'agente UE-V 1 genera errori durante l'uso di modelli UE-V 2</span><span class="sxs-lookup"><span data-stu-id="f9784-179">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="f9784-180">Se un modello di posizione delle impostazioni dell'UE-V 2 viene distribuito in un computer installato con un agente UE-V 1, alcune impostazioni non riescono a eseguire la sincronizzazione tra i computer e l'agente segnala gli errori nel log eventi.</span><span class="sxs-lookup"><span data-stu-id="f9784-180">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="f9784-181">SOLUZIONE alternativa: quando si esegue la migrazione da UE-V 1 a UE-V 2 ed è probabile che i computer che eseguono la versione precedente dell'agente creino un catalogo UE-V 2,0 separato per supportare l'agente e i modelli di UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="f9784-181">WORKAROUND: When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="f9784-182">Aggiornamenti rapidi e articoli della Knowledge base per UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="f9784-182">Hotfixes and Knowledge Base articles for UE-V 2.1</span></span>


<span data-ttu-id="f9784-183">Questa sezione contiene gli hotfix e gli articoli della KB per la versione UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="f9784-183">This section contains hotfixes and KB articles for UE-V 2.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="f9784-184">Articolo KB</span><span class="sxs-lookup"><span data-stu-id="f9784-184">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="f9784-185">Title</span><span class="sxs-lookup"><span data-stu-id="f9784-185">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="f9784-186">Link</span><span class="sxs-lookup"><span data-stu-id="f9784-186">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-187">3018608</span><span class="sxs-lookup"><span data-stu-id="f9784-187">3018608</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-188">UE-V 2,1-TemplateConsole.exe si arresta in modo anomalo quando mancano le classi WMI di UE-V</span><span class="sxs-lookup"><span data-stu-id="f9784-188">UE-V 2.1 - TemplateConsole.exe crashes when UE-V WMI classes are missing</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)"><span data-ttu-id="f9784-189">support.microsoft.com/kb/3018608/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-189">support.microsoft.com/kb/3018608/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-190">2903501</span><span class="sxs-lookup"><span data-stu-id="f9784-190">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-191">UE-V: compatibilità con l'esperienza utente per la virtualizzazione (UE-V) con i profili utente</span><span class="sxs-lookup"><span data-stu-id="f9784-191">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="f9784-192">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-192">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-193">2770042</span><span class="sxs-lookup"><span data-stu-id="f9784-193">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-194">Impostazioni del registro di sistema UE-V</span><span class="sxs-lookup"><span data-stu-id="f9784-194">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="f9784-195">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-195">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-196">2847017</span><span class="sxs-lookup"><span data-stu-id="f9784-196">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-197">Impostazioni UE-V replicate da Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9784-197">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="f9784-198">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-198">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-199">2769631</span><span class="sxs-lookup"><span data-stu-id="f9784-199">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-200">Come ripristinare un'installazione di UE-V danneggiata</span><span class="sxs-lookup"><span data-stu-id="f9784-200">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="f9784-201">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-201">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-202">2850989</span><span class="sxs-lookup"><span data-stu-id="f9784-202">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-203">La migrazione dei profili MAPI con Microsoft UE-V non è supportata</span><span class="sxs-lookup"><span data-stu-id="f9784-203">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="f9784-204">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-204">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-205">2769586</span><span class="sxs-lookup"><span data-stu-id="f9784-205">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-206">UE-V aggira le cartelle vuote e le chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f9784-206">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="f9784-207">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-207">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-208">2782997</span><span class="sxs-lookup"><span data-stu-id="f9784-208">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-209">Come abilitare la registrazione di debug in Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="f9784-209">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="f9784-210">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-210">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-211">2769570</span><span class="sxs-lookup"><span data-stu-id="f9784-211">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-212">UE-V non aggiorna il tema nelle sessioni RDS o VDI</span><span class="sxs-lookup"><span data-stu-id="f9784-212">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="f9784-213">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-213">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-214">2850582</span><span class="sxs-lookup"><span data-stu-id="f9784-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-215">Come usare la virtualizzazione dell'esperienza utente Microsoft con le applicazioni App-V</span><span class="sxs-lookup"><span data-stu-id="f9784-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="f9784-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f9784-217">3041879</span><span class="sxs-lookup"><span data-stu-id="f9784-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-218">Versioni di file correnti per la virtualizzazione dell'esperienza utente Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9784-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="f9784-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f9784-220">2843592</span><span class="sxs-lookup"><span data-stu-id="f9784-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="f9784-221">Informazioni sulla virtualizzazione dell'esperienza utente e disponibilità elevata</span><span class="sxs-lookup"><span data-stu-id="f9784-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="f9784-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="f9784-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 






 

 





