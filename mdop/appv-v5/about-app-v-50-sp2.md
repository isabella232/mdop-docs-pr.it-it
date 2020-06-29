---
title: Informazioni su App-V 5.0 SP2
description: Informazioni su App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814986"
---
# <span data-ttu-id="f6cc3-103">Informazioni su App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f6cc3-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="f6cc3-104">App-V 5.0 SP2 offre una piattaforma integrata migliorata, una virtualizzazione più flessibile e una gestione efficace per le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="f6cc3-105">Per altre informazioni, Vedi [Panoramica di App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="f6cc3-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="f6cc3-106">Modifiche apportate alla funzionalità standard App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f6cc3-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="f6cc3-107">Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="f6cc3-108">Supporto per Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f6cc3-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="f6cc3-109">App-V 5,0 include il supporto per Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f6cc3-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="f6cc3-110">App-V 5.0 SP2 ora supporta il reindirizzamento delle cartelle per la directory di roaming AppData dell'utente</span><span class="sxs-lookup"><span data-stu-id="f6cc3-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="f6cc3-111">App-V 5.0 SP2 supporta il roaming AppData (% AppData%) Reindirizzamento delle cartelle.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="f6cc3-112">Per altre informazioni, vedi la [pianificazione per usare il reindirizzamento delle cartelle con App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="f6cc3-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="f6cc3-113">Miglioramenti di aggiornamento del pacchetto e attività in sospeso</span><span class="sxs-lookup"><span data-stu-id="f6cc3-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="f6cc3-114">In App-V 5.0 SP2 non viene più richiesto di chiudere un'applicazione virtuale in esecuzione quando viene pubblicata una versione più recente del pacchetto o del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="f6cc3-115">Se un pacchetto o un gruppo di connessioni è in uso quando si prova a eseguire un'attività correlata, viene visualizzato un messaggio per indicare che l'oggetto è in uso e che l'operazione verrà tentata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="f6cc3-116">Le attività inserite in uno stato in sospeso verranno eseguite in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6cc3-117">Tipo di attività</span><span class="sxs-lookup"><span data-stu-id="f6cc3-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="f6cc3-118">Regola applicabile</span><span class="sxs-lookup"><span data-stu-id="f6cc3-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6cc3-119">Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</span><span class="sxs-lookup"><span data-stu-id="f6cc3-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6cc3-120">L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6cc3-121">Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</span><span class="sxs-lookup"><span data-stu-id="f6cc3-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6cc3-122">L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f6cc3-123">Quando un'attività viene inserita in uno stato in sospeso, il client App-V genera anche una chiave del registro di sistema per l'attività in sospeso, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6cc3-124">Attività basata su utenti o globale</span><span class="sxs-lookup"><span data-stu-id="f6cc3-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="f6cc3-125">Dove viene generata la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f6cc3-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6cc3-126">Attività basate sull'utente</span><span class="sxs-lookup"><span data-stu-id="f6cc3-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6cc3-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="f6cc3-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6cc3-128">Attività basate su base globale</span><span class="sxs-lookup"><span data-stu-id="f6cc3-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6cc3-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="f6cc3-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f6cc3-130">Virtualizzazione di Microsoft Office 2013 e Microsoft Office 2010 tramite App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="f6cc3-131">Usare il collegamento seguente per altre informazioni sugli scenari di Microsoft Office supportati da App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="f6cc3-132">Virtualizzazione di Microsoft Office 2013 per Application Virtualization (App-V) 5.0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="f6cc3-133">**Nota**  Questo documento si basa sulla creazione di un pacchetto di Microsoft Office 2013 App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="f6cc3-134">Fornisce tuttavia anche informazioni sugli scenari per Microsoft Office 2010 con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="f6cc3-135">Applicazione per l'interfaccia utente di gestione client di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="f6cc3-136">Nelle versioni precedenti di App-V 5,0 l'interfaccia utente di gestione client è stata fornita con l'installazione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="f6cc3-137">Con App-V 5.0 SP2 questo non è più il caso.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="f6cc3-138">Gli amministratori hanno ora la possibilità di distribuire l'interfaccia utente client App-V 5,0 come applicazione virtuale (usando tutte le configurazioni di distribuzione di App-V supportate) o come applicazione installata.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="f6cc3-139">Per altre informazioni, Vedi [applicazione di interfaccia utente client di Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="f6cc3-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="f6cc3-140">Assemblaggio e distribuzione automatica di assembly affiancati (SxS)</span><span class="sxs-lookup"><span data-stu-id="f6cc3-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="f6cc3-141">App-V 5.0 SP2 ora rileva automaticamente gli assembly side-by-Side (SxS) e la distribuzione nel computer che gestisce il client App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="f6cc3-142">Un assembly SxS consiste principalmente di dipendenze della fase di esecuzione di VC + + o MSXML.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="f6cc3-143">Nelle versioni precedenti di App-V le applicazioni virtuali che avevano dipendenze da Runtime di VC richiedevano che queste dipendenze fossero localmente nel computer che esegue il client App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="f6cc3-144">Ora sono supportate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="f6cc3-145">L'App-V 5,0 sequencer acquisisce automaticamente l'assembly SxS nel pacchetto, indipendentemente dal fatto che la fase di esecuzione di VC sia già stata installata nel computer in cui è in esecuzione Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="f6cc3-146">Il client App-V 5,0 installa automaticamente l'assembly SxS richiesto nel computer in cui è in esecuzione il client, come richiesto in fase di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="f6cc3-147">L'App-V 5,0 sequencer riporta la dipendenza di runtime VC usando il meccanismo di creazione di report Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="f6cc3-148">L'App-V 5,0 Sequencer consente ora di escludere la dipendenza di runtime VC in caso di dipendenza già disponibile nel computer che esegue il sequencer.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="f6cc3-149">Miglioramenti all'aggiornamento della pubblicazione</span><span class="sxs-lookup"><span data-stu-id="f6cc3-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="f6cc3-150">App-V 5,0 supporta diverse funzionalità aggiunte per migliorare l'esperienza complessiva di aggiornamento di un set di applicazioni per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="f6cc3-151">Nell'elenco seguente vengono visualizzati i miglioramenti dell'aggiornamento della pubblicazione:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="f6cc3-152">L'elenco seguente contiene altre informazioni su come abilitare i nuovi miglioramenti per l'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="f6cc3-153">**EnablePublishingRefreshUI** -Abilita la barra di stato aggiornamento pubblicazione per il computer che gestisce il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="f6cc3-154">**HideUI** -nasconde la barra di stato dell'aggiornamento della pubblicazione durante una sincronizzazione manuale.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="f6cc3-155">Impostazione nuova configurazione client</span><span class="sxs-lookup"><span data-stu-id="f6cc3-155">New Client Configuration Setting</span></span>

<span data-ttu-id="f6cc3-156">La nuova impostazione di configurazione client seguente è disponibile con App-V 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="f6cc3-157">**EnableDynamicVirtualization** -Abilita le estensioni della shell supportate, gli oggetti helper del browser e i controlli attivi X per essere virtualizzati ed eseguiti con le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="f6cc3-158">Per altre informazioni, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f6cc3-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="f6cc3-159">Estensioni della shell App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="f6cc3-160">App-V 5,0 SP2 ora supporta le estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="f6cc3-161">Per altre informazioni, vedi la sezione **supporto dell'estensione della shell App-v 5.0 SP2** per la [creazione e la gestione di applicazioni virtualizzate app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="f6cc3-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="f6cc3-162">Aggiornamenti della documentazione di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="f6cc3-163">App-V 5,0 SP2 fornisce la documentazione aggiornata per gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6cc3-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="f6cc3-164">Migrazione da una versione precedente</span><span class="sxs-lookup"><span data-stu-id="f6cc3-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="f6cc3-165">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f6cc3-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="f6cc3-166">[Informazioni sulla creazione di report su App-V 5,0](about-app-v-50-reporting.md) (sezione Domande frequenti)</span><span class="sxs-lookup"><span data-stu-id="f6cc3-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="f6cc3-167">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="f6cc3-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="f6cc3-168">App-V 5,0 fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="f6cc3-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="f6cc3-169">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="f6cc3-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="f6cc3-170">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="f6cc3-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="f6cc3-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6cc3-171">Related topics</span></span>


[<span data-ttu-id="f6cc3-172">Note sulla versione di App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f6cc3-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





