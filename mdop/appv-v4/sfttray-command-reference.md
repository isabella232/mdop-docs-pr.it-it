---
title: Riferimento ai comandi SFTTRAY
description: Riferimento ai comandi SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815355"
---
# <span data-ttu-id="4cacb-103">Riferimento ai comandi SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="4cacb-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="4cacb-104">L'applicazione Microsoft Application Virtualization (App-V) Client Tray, sfttray.exe, è l'elemento principale dell'interfaccia utente del client App-V con cui gli utenti interagiranno durante l'uso normale.</span><span class="sxs-lookup"><span data-stu-id="4cacb-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="4cacb-105">Questo programma controlla lo streaming e l'avvio di tutte le applicazioni virtuali e si accede facendo clic con il pulsante destro del mouse sull'icona visualizzata nell'area di notifica per visualizzare il menu delle funzioni client.</span><span class="sxs-lookup"><span data-stu-id="4cacb-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="4cacb-106">Il menu consente all'utente di caricare le applicazioni, avviare un aggiornamento della pubblicazione, annullare una richiesta o cambiare il client in modalità offline.</span><span class="sxs-lookup"><span data-stu-id="4cacb-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="4cacb-107">L'utente può anche chiudere l'applicazione Tray Application Virtualization Client e tutte le applicazioni attive facendo clic su **Esci**.</span><span class="sxs-lookup"><span data-stu-id="4cacb-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="4cacb-108">Per impostazione predefinita, l'icona viene visualizzata ogni volta che si avvia un'applicazione virtuale, anche se è possibile controllare questo comportamento usando i comandi di SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="4cacb-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="4cacb-109">L'applicazione Application Virtualization Client Tray Visualizza anche una barra di stato per ogni applicazione avviata, nonché i messaggi di stato sulle applicazioni attive.</span><span class="sxs-lookup"><span data-stu-id="4cacb-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="4cacb-110">Facendo clic sulla barra di stato viene visualizzato un messaggio che consente di annullare il caricamento o l'avvio di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cacb-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="4cacb-111">Comandi di SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="4cacb-111">SFTTRAY Commands</span></span>


<span data-ttu-id="4cacb-112">L'elenco dei comandi e delle opzioni della riga di comando può essere visualizzato eseguendo il comando seguente da una finestra di comando.</span><span class="sxs-lookup"><span data-stu-id="4cacb-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="4cacb-113">Nota</span><span class="sxs-lookup"><span data-stu-id="4cacb-113">Note</span></span>**  
<span data-ttu-id="4cacb-114">Esiste una sola istanza del client di virtualizzazione delle applicazioni per ogni contesto utente, quindi se si avvia un nuovo comando SFTTRAY, verrà passato al programma già in uso.</span><span class="sxs-lookup"><span data-stu-id="4cacb-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="4cacb-115">Utilizzo dei comandi</span><span class="sxs-lookup"><span data-stu-id="4cacb-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="4cacb-116">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="4cacb-116">Command-Line Switches</span></span>

<span data-ttu-id="4cacb-117">Le opzioni della riga di comando di SFTTRAY sono descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4cacb-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4cacb-118">Opzione</span><span class="sxs-lookup"><span data-stu-id="4cacb-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="4cacb-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cacb-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-120">/HIDE</span><span class="sxs-lookup"><span data-stu-id="4cacb-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-121">Nasconde l'icona di SFTTRAY nell'area di notifica di Windows.</span><span class="sxs-lookup"><span data-stu-id="4cacb-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cacb-122">/SHOW</span><span class="sxs-lookup"><span data-stu-id="4cacb-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-123">Visualizza l'icona di SFTTRAY nell'area di notifica di Windows.</span><span class="sxs-lookup"><span data-stu-id="4cacb-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-124">/QUIET</span><span class="sxs-lookup"><span data-stu-id="4cacb-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-125">Supporta l'utilizzo non presidiato impedendo la visualizzazione di finestre di messaggio che richiedono la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4cacb-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cacb-126">/EXE &lt; alternativo-exe&gt;</span><span class="sxs-lookup"><span data-stu-id="4cacb-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-127">Usato con/LAUNCH per specificare che è necessario avviare un programma eseguibile nell'ambiente virtuale quando un'applicazione virtuale viene avviata al posto del file di destinazione specificato nell'OSD.</span><span class="sxs-lookup"><span data-stu-id="4cacb-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4cacb-128">Nota</span><span class="sxs-lookup"><span data-stu-id="4cacb-128">Note</span></span></strong><br/><p><span data-ttu-id="4cacb-129">Ad esempio, USA "SFTTRAY.EXE/EXE REGEDIT.EXE/LAUNCH &lt; app &gt; " per consentire di esaminare il registro di sistema dell'ambiente virtuale in cui è in corso l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cacb-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-130">&lt;App/Launch &gt; [ &lt; argomenti &gt; ]</span><span class="sxs-lookup"><span data-stu-id="4cacb-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-131">Avvia un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cacb-131">Starts a virtual application.</span></span> <span data-ttu-id="4cacb-132">Specificare il nome e la versione di un'applicazione o il percorso di un file OSD.</span><span class="sxs-lookup"><span data-stu-id="4cacb-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="4cacb-133">Facoltativamente, gli argomenti della riga di comando possono essere passati all'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cacb-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4cacb-134">Nota</span><span class="sxs-lookup"><span data-stu-id="4cacb-134">Note</span></span></strong><br/><p><span data-ttu-id="4cacb-135">Usa il comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" per ottenere un elenco dei nomi e delle versioni delle applicazioni virtuali disponibili.</span><span class="sxs-lookup"><span data-stu-id="4cacb-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cacb-136">/LOAD</span><span class="sxs-lookup"><span data-stu-id="4cacb-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-137">Carica o importa un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cacb-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="4cacb-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-139">Carica tutte le applicazioni nella cache.</span><span class="sxs-lookup"><span data-stu-id="4cacb-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cacb-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="4cacb-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-141">Avvia un aggiornamento della pubblicazione per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4cacb-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-142">&lt;ID univoco di/LAUNCHRESULT&gt;</span><span class="sxs-lookup"><span data-stu-id="4cacb-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-143">Restituisce il codice del risultato dell'avvio al processo che avvia sfttray.exe usando un evento globale e un file mappato alla memoria basato sul nome radice specificato per l'ID univoco. ¹</span><span class="sxs-lookup"><span data-stu-id="4cacb-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4cacb-144">/SFTFILE &lt; SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="4cacb-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-145">Opzione facoltativa usata con/LOAD per specificare il percorso del file SFT dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cacb-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="4cacb-146">Se specificato, l'applicazione viene importata piuttosto che caricata.</span><span class="sxs-lookup"><span data-stu-id="4cacb-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4cacb-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="4cacb-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="4cacb-148">Chiude il programma SFTTRAY e tutte le applicazioni virtuali attive e rimuove l'icona dall'area di notifica di Windows.</span><span class="sxs-lookup"><span data-stu-id="4cacb-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="4cacb-149">Nota</span><span class="sxs-lookup"><span data-stu-id="4cacb-149">Note</span></span>**  
<span data-ttu-id="4cacb-150">¹ il parametro della riga di comando */LAUNCHRESULT* fornisce un mezzo per il processo che avvia sfttray.exe per specificare il nome radice per un evento globale e un file mappato alla memoria usato per restituire il codice del risultato di avvio al processo.</span><span class="sxs-lookup"><span data-stu-id="4cacb-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="4cacb-151">Il nome dell'identificatore univoco dovrebbe iniziare con "SFT-" per evitare che il nome dell'evento venga virtualizzato quando il processo di avvio viene richiamato all'interno di un ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cacb-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="4cacb-152">L'area di mapping della memoria sarà di 64 bit in dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4cacb-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="4cacb-153">Per usare questo parametro, il processo di avvio crea un evento con il nome " &lt; ID univoco &gt; -risultato \ _event", un file mappato in memoria con il nome " &lt; ID univoco &gt; -risultato \ _value" e, facoltativamente, un evento con il nome " &lt; id univoco &gt; -Shutdown \ _event" e quindi il processo di avvio viene avviato sfttray.exe e attende l'evento per essere segnalato.</span><span class="sxs-lookup"><span data-stu-id="4cacb-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="4cacb-154">Dopo che l'evento " &lt; ID univoco &gt; -risultato \ _event" viene segnalato, il processo di avvio recupera il codice restituito a 64 bit dall'area mappata alla memoria.</span><span class="sxs-lookup"><span data-stu-id="4cacb-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="4cacb-155">Se l'evento facoltativo " &lt; ID univoco &gt; -shutdown \ _event" esiste quando l'applicazione virtuale viene chiusa, sfttray.exe si apre e segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="4cacb-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="4cacb-156">Il processo di avvio attende questo evento di arresto se deve determinare quando l'applicazione virtuale viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="4cacb-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











