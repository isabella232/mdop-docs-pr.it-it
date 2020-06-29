---
title: Metodi di sincronizzazione per UE-V 2.x
description: Metodi di sincronizzazione per UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823576"
---
# <span data-ttu-id="57eea-103">Metodi di sincronizzazione per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="57eea-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="57eea-104">L'agente Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 consente di sincronizzare le impostazioni dell'applicazione e di Windows degli utenti con la posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="57eea-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="57eea-105">La configurazione del *metodo di sincronizzazione* definisce il modo in cui l'agente UE-V carica e Scarica tali impostazioni nella posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="57eea-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="57eea-106">UE-V 2. x introduce una nuova SyncMethod denominata *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="57eea-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="57eea-107">Per altre informazioni sugli eventi trigger che avviano la sincronizzazione delle impostazioni dell'applicazione e di Windows, vedere [sincronizzazione degli eventi trigger per UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="57eea-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="57eea-108">Configurazione di SyncMethod</span><span class="sxs-lookup"><span data-stu-id="57eea-108">SyncMethod Configuration</span></span>


<span data-ttu-id="57eea-109">Questa tabella illustra le modifiche apportate a SyncMethod da UE-V v 1.0 a v 2.0 a v 2.1, nonché le impostazioni per ogni configurazione:</span><span class="sxs-lookup"><span data-stu-id="57eea-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="57eea-110">Configurazione di SyncMethod</span><span class="sxs-lookup"><span data-stu-id="57eea-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="57eea-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="57eea-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="57eea-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="57eea-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="57eea-113">V 2.1 e V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="57eea-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="57eea-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57eea-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57eea-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="57eea-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-116">n/d</span><span class="sxs-lookup"><span data-stu-id="57eea-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-117">Default</span><span class="sxs-lookup"><span data-stu-id="57eea-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-118">Default</span><span class="sxs-lookup"><span data-stu-id="57eea-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-119">Le modifiche alle impostazioni per un'applicazione specifica o per le impostazioni desktop di Windows globali vengono salvate localmente in una cartella della cache.</span><span class="sxs-lookup"><span data-stu-id="57eea-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="57eea-120">Queste modifiche vengono quindi sincronizzate con il percorso di archiviazione delle impostazioni quando si verifica un evento trigger di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="57eea-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="57eea-121">La modifica delle modifiche consente di salvare le modifiche locali nel percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="57eea-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="57eea-122">Questa impostazione predefinita è lo standard Gold per i computer.</span><span class="sxs-lookup"><span data-stu-id="57eea-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="57eea-123">Questa opzione consente di sincronizzare l'impostazione e il timeout dopo un breve ritardo per verificare che l'avvio dell'applicazione o del sistema operativo non venga ritardato per un lungo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="57eea-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="57eea-124">Questa funzionalità è legata anche all'attività programmata: applicazione di controllo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="57eea-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="57eea-125">L'amministratore controlla la frequenza dell'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="57eea-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="57eea-126">Per impostazione predefinita, i computer sincronizzano le impostazioni ogni 30 minuti dopo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="57eea-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57eea-127">OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="57eea-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-128">Default</span><span class="sxs-lookup"><span data-stu-id="57eea-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-129">Deprecato</span><span class="sxs-lookup"><span data-stu-id="57eea-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-130">Deprecato</span><span class="sxs-lookup"><span data-stu-id="57eea-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-131">Si comporta come SyncProvider in V 2.0.</span><span class="sxs-lookup"><span data-stu-id="57eea-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="57eea-132">Se i file offline sono abilitati e la cartella viene bloccata, l'UE-V sbloccare questa cartella e la sincronizzazione direttamente con la directory centrale SMB.</span><span class="sxs-lookup"><span data-stu-id="57eea-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="57eea-133">Nota: </strong> in V 1.0 se si vuole usare l'UE-v in modalità disconnessa corpnet (aka che viaggia con un portatile), la guida consiste nell'usare i file offline per verificare che le impostazioni siano in roaming.</span><span class="sxs-lookup"><span data-stu-id="57eea-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="57eea-134">È stato ricevuto un sufficiente feedback dei clienti che l'attivazione di file offline è un blocco aziendale non banale.</span><span class="sxs-lookup"><span data-stu-id="57eea-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="57eea-135">Quindi in UE-V 2 abbiamo creato un motore di sincronizzazione strettamente accoppiato per memorizzare nella cache i dati localmente e sincronizzare le impostazioni con il server centrale.</span><span class="sxs-lookup"><span data-stu-id="57eea-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="57eea-136">Questa area di funzionalità non sostituisce i file offline o il reindirizzamento delle cartelle.</span><span class="sxs-lookup"><span data-stu-id="57eea-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="57eea-137">UE-V 2 non funziona bene con le cartelle offline in modo che le indicazioni non consentiranno di impostare il percorso di archiviazione delle impostazioni su una cartella offline o CSC bloccata.</span><span class="sxs-lookup"><span data-stu-id="57eea-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57eea-138">External</span><span class="sxs-lookup"><span data-stu-id="57eea-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-139">n/d</span><span class="sxs-lookup"><span data-stu-id="57eea-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-140">n/d</span><span class="sxs-lookup"><span data-stu-id="57eea-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-141">Supportato</span><span class="sxs-lookup"><span data-stu-id="57eea-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-142">Nuovo in UE-V 2,1, questo metodo di configurazione specifica che se le impostazioni UE-V vengono scritte in una cartella locale nel computer utente, è possibile usare qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, cartelle di lavoro, SharePoint o Dropbox, per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.</span><span class="sxs-lookup"><span data-stu-id="57eea-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57eea-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="57eea-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-144">Sì</span><span class="sxs-lookup"><span data-stu-id="57eea-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-145">Sì</span><span class="sxs-lookup"><span data-stu-id="57eea-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-146">Sì</span><span class="sxs-lookup"><span data-stu-id="57eea-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="57eea-147">Questa impostazione di configurazione è progettata principalmente per l'infrastruttura VDI (Virtual Desktop Infrastructure) e per l'esperienza di applicazione in streaming.</span><span class="sxs-lookup"><span data-stu-id="57eea-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="57eea-148">Questa impostazione deve essere usata nelle caselle di Windows Server usate in un Data Center, dove la connessione sarà sempre disponibile.</span><span class="sxs-lookup"><span data-stu-id="57eea-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="57eea-149">Tutte le modifiche apportate alle impostazioni vengono salvate direttamente nel server.</span><span class="sxs-lookup"><span data-stu-id="57eea-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="57eea-150">Se la connessione di rete al percorso di archiviazione delle impostazioni non è disponibile, le modifiche apportate alle impostazioni vengono memorizzate nella cache del dispositivo e vengono sincronizzate la volta successiva che il provider di sincronizzazione viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57eea-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="57eea-151">Se il percorso di archiviazione delle impostazioni non viene trovato e il profilo utente viene rimosso da un ambiente VDI in pool durante la disconnessione, le modifiche alle impostazioni andranno perse e l'utente dovrà riapplicare la modifica quando il computer potrà raggiungere di nuovo il percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="57eea-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="57eea-152">Le app e il sistema operativo aspetteranno indefinitamente che la posizione sia presente.</span><span class="sxs-lookup"><span data-stu-id="57eea-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="57eea-153">Ciò potrebbe causare il caricamento dell'app o il tempo di accesso del sistema operativo per aumentare in modo significativo se la posizione non viene trovata.</span><span class="sxs-lookup"><span data-stu-id="57eea-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="57eea-154">Puoi configurare il metodo di sincronizzazione in questi modi:</span><span class="sxs-lookup"><span data-stu-id="57eea-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="57eea-155">Quando si [distribuisce l'agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) tramite un parametro della riga di comando o in uno script batch</span><span class="sxs-lookup"><span data-stu-id="57eea-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="57eea-156">Impostazioni di [criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="57eea-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="57eea-157">Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) per UE-V</span><span class="sxs-lookup"><span data-stu-id="57eea-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="57eea-158">Dopo l'installazione dell'agente UE-V, usare [Windows PowerShell o Strumentazione gestione Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="57eea-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="57eea-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57eea-159">Related topics</span></span>


[<span data-ttu-id="57eea-160">Distribuire le funzionalità necessarie per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="57eea-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="57eea-161">Distribuire le funzionalità necessarie per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="57eea-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="57eea-162">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="57eea-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





