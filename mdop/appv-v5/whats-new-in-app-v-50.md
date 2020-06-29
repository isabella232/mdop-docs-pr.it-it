---
title: Novità in App-V 5.0
description: Novità in App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804815"
---
# <span data-ttu-id="1e8ec-103">Novità in App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1e8ec-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="1e8ec-104">Questa sezione è dedicata agli utenti che hanno già familiarità con App-V e vogliono sapere cosa è cambiato in App-V 5,0 se non si ha già familiarità con App-V, è consigliabile iniziare leggendo [la pianificazione per l'app-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="1e8ec-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="1e8ec-105">Modifiche della funzionalità standard</span><span class="sxs-lookup"><span data-stu-id="1e8ec-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="1e8ec-106">Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per l'App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="1e8ec-107">Modifiche ai sistemi operativi supportati</span><span class="sxs-lookup"><span data-stu-id="1e8ec-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="1e8ec-108">Per altre informazioni, Vedi [configurazioni supportate in App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="1e8ec-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="1e8ec-109">Modifiche al sequencer</span><span class="sxs-lookup"><span data-stu-id="1e8ec-109">Changes to the sequencer</span></span>


<span data-ttu-id="1e8ec-110">Le sezioni seguenti contengono informazioni sulle modifiche apportate all'App-V 5,0 sequencer.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="1e8ec-111">Modifica specifica del sequencer</span><span class="sxs-lookup"><span data-stu-id="1e8ec-111">Specific change to the sequencer</span></span>

<span data-ttu-id="1e8ec-112">La tabella seguente mostra le informazioni sulle modifiche apportate all'App-V 5,0 sequencer</span><span class="sxs-lookup"><span data-stu-id="1e8ec-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1e8ec-113">Funzionalità sequenziatore</span><span class="sxs-lookup"><span data-stu-id="1e8ec-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="1e8ec-114">Funzionalità sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1e8ec-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-115">Riavviare l'elaborazione</span><span class="sxs-lookup"><span data-stu-id="1e8ec-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-116">Quando un'applicazione richiede un riavvio, è consigliabile consentire all'applicazione di riavviare il computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="1e8ec-117">Il computer in cui viene eseguito il sequencer verrà riavviato e il sequencer riprenderà in modalità di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-118">Specifica della directory dell'applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="1e8ec-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-119">La directory dell'applicazione virtuale è un parametro obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="1e8ec-120">Per ottenere risultati ottimali, deve corrispondere alla directory di installazione dell'applicazione Installer.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="1e8ec-121">Questo comporta una maggiore compatibilità delle prestazioni e delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-122">Modifica di tasti di scelta rapida/accordi</span><span class="sxs-lookup"><span data-stu-id="1e8ec-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-123">La pagina collegamenti/FTA si trova nella <strong> </strong> pagina di modifica avanzata dopo il completamento della procedura guidata di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-124">Scheda Cronologia modifiche</span><span class="sxs-lookup"><span data-stu-id="1e8ec-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-125">La scheda Cambia cronologia è stata rimossa per App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-126">Scheda OSD</span><span class="sxs-lookup"><span data-stu-id="1e8ec-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-127">La scheda OSD è stata rimossa per App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-128">Scheda Servizi virtuali</span><span class="sxs-lookup"><span data-stu-id="1e8ec-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-129">La scheda servizi virtuali è stata rimossa per App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-130">Scheda file/file system virtuale</span><span class="sxs-lookup"><span data-stu-id="1e8ec-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-131">Queste schede vengono combinate e consentono di modificare i file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-132">Scheda Distribuzione</span><span class="sxs-lookup"><span data-stu-id="1e8ec-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-133">Non sono più disponibili opzioni per configurare l'URL del server nei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="1e8ec-134">È necessario configurare ora l'uso della configurazione di distribuzione o del server di gestione.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-135">Strumento convertitore pacchetti</span><span class="sxs-lookup"><span data-stu-id="1e8ec-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-136">È ora possibile usare PowerShell per convertire i pacchetti creati in versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-137">Componente aggiuntivo/middleware</span><span class="sxs-lookup"><span data-stu-id="1e8ec-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-138">È possibile espandere i pacchetti padre quando si esegue la sequenziazione di un componente aggiuntivo o di un'applicazione middleware.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="1e8ec-139">I pacchetti di componenti aggiuntivi e middleware devono essere connessi con i gruppi di connessione in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-140">Output file</span><span class="sxs-lookup"><span data-stu-id="1e8ec-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-141">I file seguenti vengono creati con App-V 5,0, Windows Installer (. msi),. AppV, configurazione della distribuzione, configurazione utente e Report.XML.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-142">Descrittori di compressione/sicurezza/pacchetti MSI</span><span class="sxs-lookup"><span data-stu-id="1e8ec-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-143">La compressione e la creazione di un file di Windows Installer (con estensione msi) sono automatiche per tutti i pacchetti e non è più possibile ignorare i descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-144">Strumenti/opzioni</span><span class="sxs-lookup"><span data-stu-id="1e8ec-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-145">La finestra di diagnostica è stata rimossa, oltre a diverse altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-146">Unità di installazione</span><span class="sxs-lookup"><span data-stu-id="1e8ec-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-147">Un'unità di installazione non è più necessaria quando si installa un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1e8ec-148">Flusso di OOS</span><span class="sxs-lookup"><span data-stu-id="1e8ec-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e8ec-149">Se non viene eseguita l'ottimizzazione del flusso, i pacchetti vengono trasmessi in errore quando richiesto dai computer che eseguono il client App-V 5,0 finché non vengono avviati.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1e8ec-150">D: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="1e8ec-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="1e8ec-151">App-V 5,0 usa il file system nativo e non richiede più un D:.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1e8ec-152">Rilevamento degli errori di sequenziazione</span><span class="sxs-lookup"><span data-stu-id="1e8ec-152">Sequencing error detection</span></span>


<span data-ttu-id="1e8ec-153">Il sequencer App-V 5,0 può rilevare i problemi di sequenziazione comuni durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="1e8ec-154">La pagina del **report di installazione** alla fine della sequenziazione guidata Visualizza i messaggi di diagnostica categorizzati in **errori**, **avvisi**e **informazioni** in base alla gravità del problema.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="1e8ec-155">Per visualizzare informazioni più dettagliate su un evento, fare doppio clic sull'elemento che si vuole rivedere nel report.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="1e8ec-156">I problemi di sequenziazione e i suggerimenti su come risolvere i problemi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="1e8ec-157">Le informazioni contenute nel report di preparazione del sistema e nel report di installazione vengono riepilogate al termine della creazione di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="1e8ec-158">Nell'elenco seguente sono visualizzati i tipi di problemi disponibili nel report:</span><span class="sxs-lookup"><span data-stu-id="1e8ec-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="1e8ec-159">File esclusi.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-159">Excluded files.</span></span>

-   <span data-ttu-id="1e8ec-160">Informazioni sui driver.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-160">Driver information.</span></span>

-   <span data-ttu-id="1e8ec-161">Differenze di sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-161">COM+ system differences.</span></span>

-   <span data-ttu-id="1e8ec-162">Conflitti side-by-Side (SxS).</span><span class="sxs-lookup"><span data-stu-id="1e8ec-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="1e8ec-163">Estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-163">Shell Extensions.</span></span>

-   <span data-ttu-id="1e8ec-164">Informazioni sui servizi non supportati.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="1e8ec-165">DCOM.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-165">DCOM.</span></span>

## <span data-ttu-id="1e8ec-166">Gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="1e8ec-166">Connection Groups</span></span>


<span data-ttu-id="1e8ec-167">La funzionalità App-V in precedenza nota come **composizione della famiglia dinamica** viene ora definita **gruppi di connessioni** in App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="1e8ec-168">Per altre informazioni sull'uso dei gruppi di connessioni, vedere [gestire i gruppi di connessioni](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="1e8ec-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="1e8ec-169">Funzionalità di licenza e misurazione</span><span class="sxs-lookup"><span data-stu-id="1e8ec-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="1e8ec-170">La funzionalità applicazione e licenze è stata rimossa in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="1e8ec-171">Le posizioni effettive della licenza nell'ambiente dipendono dalla licenza specifica per il titolo del software e dai diritti di utilizzo concessi dalle condizioni di licenza associate.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="1e8ec-172">Cache di file e applicazioni</span><span class="sxs-lookup"><span data-stu-id="1e8ec-172">File and Application Cache</span></span>


<span data-ttu-id="1e8ec-173">Non è disponibile una cache di file o applicazioni con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="1e8ec-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e8ec-174">Related topics</span></span>


[<span data-ttu-id="1e8ec-175">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1e8ec-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





