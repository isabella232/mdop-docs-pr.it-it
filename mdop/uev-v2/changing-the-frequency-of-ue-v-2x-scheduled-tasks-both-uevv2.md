---
title: Modifica della frequenza delle attività pianificate di UE-V 2. x
description: Modifica della frequenza delle attività pianificate di UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824426"
---
# <span data-ttu-id="f7626-103">Modifica della frequenza delle attività pianificate di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f7626-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="f7626-104">Il programma di installazione dell'agente Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, AgentSetup.exe, crea le attività pianificate seguenti durante l'installazione dell'agente UE-V:</span><span class="sxs-lookup"><span data-stu-id="f7626-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="f7626-105">Monitorare le impostazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f7626-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="f7626-106">Applicazione controller di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="f7626-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="f7626-107">Sincronizzare le impostazioni alla disconnessione</span><span class="sxs-lookup"><span data-stu-id="f7626-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="f7626-108">Aggiornamento automatico del modello</span><span class="sxs-lookup"><span data-stu-id="f7626-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="f7626-109">Raccolta di dati analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="f7626-110">Caricare i dati di analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-110">Upload CEIP Data</span></span>**

<span data-ttu-id="f7626-111">**Nota**  Ad eccezione della raccolta di dati di analisi utilizzo software, queste attività devono rimanere abilitate perché l'UE-V non può funzionare senza di essi.</span><span class="sxs-lookup"><span data-stu-id="f7626-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="f7626-112">Queste attività pianificate non possono essere configurate con gli strumenti UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="f7626-113">Gli amministratori che vogliono modificare l'attività pianificata per questi elementi possono creare uno script che usa le opzioni della riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="f7626-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="f7626-114">Per altre informazioni su Schtasks.exe, vedere [come usare schtasks, exe per pianificare le attività in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="f7626-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="f7626-115">Per altre informazioni su</span><span class="sxs-lookup"><span data-stu-id="f7626-115">For more information about</span></span>

## <span data-ttu-id="f7626-116">Attività pianificate UE-V</span><span class="sxs-lookup"><span data-stu-id="f7626-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="f7626-117">Le attività pianificate seguenti sono incluse in UE-V 2 con i comandi di configurazione delle attività pianificate di esempio.</span><span class="sxs-lookup"><span data-stu-id="f7626-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="f7626-118">Raccolta di dati analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-118">Collect CEIP Data</span></span>

<span data-ttu-id="f7626-119">Se al momento dell'installazione l'utente o l'amministratore sceglie di partecipare al programma Customer Experience Improvement Program (analisi utilizzo software), UE-V raccoglie i dati per migliorare il prodotto nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="f7626-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="f7626-120">Questa attività pianificata viene eseguita solo all'accesso.</span><span class="sxs-lookup"><span data-stu-id="f7626-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="f7626-121">L'attività di **dati Collect analisi utilizzo software** esegue la UevSqmSession.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-122">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-123">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-124">Dati di \Microsoft\UE-V\Collect analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-125">Accesso</span><span class="sxs-lookup"><span data-stu-id="f7626-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f7626-126">Monitorare le impostazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f7626-126">Monitor Application Settings</span></span>

<span data-ttu-id="f7626-127">L'attività **monitora le impostazioni dell'applicazione** viene usata per sincronizzare le impostazioni per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="f7626-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="f7626-128">Viene eseguito all'accesso ma viene ritardato di 30 secondi per non influire negativamente sull'accesso.</span><span class="sxs-lookup"><span data-stu-id="f7626-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="f7626-129">L'attività monitora lo stato dell'applicazione esegue il file UevAppMonitor.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-130">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-131">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-132">Stato applicazione \Microsoft\UE-V\Monitor</span><span class="sxs-lookup"><span data-stu-id="f7626-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-133">Accesso</span><span class="sxs-lookup"><span data-stu-id="f7626-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f7626-134">Applicazione controller di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="f7626-134">Sync Controller Application</span></span>

<span data-ttu-id="f7626-135">L'attività dell' **applicazione controller di sincronizzazione** viene usata per avviare il controller di sincronizzazione per sincronizzare le impostazioni dal computer alla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f7626-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="f7626-136">Per impostazione predefinita, l'attività viene eseguita ogni 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="f7626-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="f7626-137">In quel momento, le impostazioni locali vengono sincronizzate con il percorso di archiviazione delle impostazioni e le impostazioni aggiornate nella posizione di archiviazione delle impostazioni vengono sincronizzate con il computer.</span><span class="sxs-lookup"><span data-stu-id="f7626-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="f7626-138">L'applicazione controller di sincronizzazione esegue la Microsoft.Uev.SyncController.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="f7626-139">**Nota:** Come per l'attività di **monitoraggio delle impostazioni dell'applicazione** , questa attività viene eseguita all'accesso, ma viene ritardata di 30 secondi per non influire negativamente sull'accesso.</span><span class="sxs-lookup"><span data-stu-id="f7626-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-140">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-141">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-142">Applicazione controller \Microsoft\UE-V\Sync</span><span class="sxs-lookup"><span data-stu-id="f7626-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-143">Accesso e ogni 30 minuti da allora in poi</span><span class="sxs-lookup"><span data-stu-id="f7626-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f7626-144">Ad esempio, il comando seguente configura l'agente per la sincronizzazione delle impostazioni ogni 15 minuti anziché i 30 minuti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f7626-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="f7626-145">Sincronizzare le impostazioni alla disconnessione</span><span class="sxs-lookup"><span data-stu-id="f7626-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="f7626-146">L'attività **Sincronizza impostazioni a disconnessione** viene usata per avviare un'applicazione all'accesso che controlla la sincronizzazione delle applicazioni alla disconnessione per l'UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="f7626-147">L'attività Sincronizza impostazioni a disconnessione esegue il file Microsoft.Uev.SyncController.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-148">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-149">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-150">Impostazioni di \Microsoft\UE-V\Synchronize alla disconnessione</span><span class="sxs-lookup"><span data-stu-id="f7626-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-151">Accesso</span><span class="sxs-lookup"><span data-stu-id="f7626-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f7626-152">Aggiornamento automatico del modello</span><span class="sxs-lookup"><span data-stu-id="f7626-152">Template Auto Update</span></span>

<span data-ttu-id="f7626-153">L'attività di **aggiornamento automatico del modello** controlla il catalogo di modelli di impostazioni per nuovi, aggiornati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="f7626-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="f7626-154">Questa attività viene eseguita solo se il SettingsTemplateCatalog è configurato.</span><span class="sxs-lookup"><span data-stu-id="f7626-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="f7626-155">L'attività di **aggiornamento automatico del modello** esegue il file ApplySettingsCatalog.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-156">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-157">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-158">Aggiornamento automatico di \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="f7626-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-159">Avvio del sistema e a 3:30 AM ogni giorno, in un momento casuale in una finestra di 1 ora</span><span class="sxs-lookup"><span data-stu-id="f7626-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f7626-160">**Esempio:** Con il comando seguente viene configurato l'agente UE-V per controllare l'archivio di catalogo dei modelli di impostazioni ogni ora.</span><span class="sxs-lookup"><span data-stu-id="f7626-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="f7626-161">Caricare i dati di analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-161">Upload CEIP Data</span></span>

<span data-ttu-id="f7626-162">L'attività di **dati upload analisi utilizzo software** viene eseguita durante l'installazione se l'utente o l'amministratore ha scelto di partecipare al programma Customer Experience Improvement Program (analisi utilizzo software).</span><span class="sxs-lookup"><span data-stu-id="f7626-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="f7626-163">Questa attività carica i dati nei server analisi utilizzo software in cui vengono usati i dati per migliorare il prodotto per le versioni future di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="f7626-164">Questa attività pianificata viene eseguita all'accesso e ogni 4 ore dopo.</span><span class="sxs-lookup"><span data-stu-id="f7626-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="f7626-165">L'attività di **dati upload analisi utilizzo software** esegue il file UevSqmUploader.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7626-166">Nome attività</span><span class="sxs-lookup"><span data-stu-id="f7626-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="f7626-167">Evento predefinito</span><span class="sxs-lookup"><span data-stu-id="f7626-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7626-168">Dati di \Microsoft\UE-V\Upload analisi utilizzo software</span><span class="sxs-lookup"><span data-stu-id="f7626-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-169">All'accesso e ogni 4 ore</span><span class="sxs-lookup"><span data-stu-id="f7626-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7626-170">Dettagli delle attività pianificate UE-V 2</span><span class="sxs-lookup"><span data-stu-id="f7626-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="f7626-171">Il grafico seguente fornisce informazioni aggiuntive sulle attività pianificate per la versione UE-V 2:</span><span class="sxs-lookup"><span data-stu-id="f7626-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f7626-172">Nome attività </strong> (nome file)</span><span class="sxs-lookup"><span data-stu-id="f7626-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f7626-173">Frequenza predefinita</span><span class="sxs-lookup"><span data-stu-id="f7626-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f7626-174">Interruttore di alimentazione</span><span class="sxs-lookup"><span data-stu-id="f7626-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f7626-175">Solo inattività</span><span class="sxs-lookup"><span data-stu-id="f7626-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f7626-176">Connessione di rete</span><span class="sxs-lookup"><span data-stu-id="f7626-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f7626-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7626-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f7626-178">Monitorare le impostazioni dell'applicazione </strong> (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-179">Avvia 30 secondi dopo l'accesso e continua fino alla disconnessione.</span><span class="sxs-lookup"><span data-stu-id="f7626-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-180">No</span><span class="sxs-lookup"><span data-stu-id="f7626-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-181">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-182">N/D</span><span class="sxs-lookup"><span data-stu-id="f7626-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-183">Sincronizza le impostazioni per le app di Windows (AppX).</span><span class="sxs-lookup"><span data-stu-id="f7626-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f7626-184">Applicazione controller di sincronizzazione </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-185">All'accesso e ogni 30 minuti da allora in poi.</span><span class="sxs-lookup"><span data-stu-id="f7626-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-186">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-187">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-188">Solo se la rete è connessa</span><span class="sxs-lookup"><span data-stu-id="f7626-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-189">Avvia il controller di sincronizzazione che sincronizza le impostazioni locali con il percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f7626-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f7626-190">Sincronizzare le impostazioni alla disconnessione </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-191">Viene eseguito all'accesso e quindi attende la disconnessione per la sincronizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f7626-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-192">No</span><span class="sxs-lookup"><span data-stu-id="f7626-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-193">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-194">N/D</span><span class="sxs-lookup"><span data-stu-id="f7626-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-195">Avviare un'applicazione all'accesso che controlla la sincronizzazione delle applicazioni a fine sessione.</span><span class="sxs-lookup"><span data-stu-id="f7626-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f7626-196">Aggiornamento automatico del modello </strong> (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-197">Viene eseguito all'accesso iniziale e alle 3:30 ogni giorno da allora in poi.</span><span class="sxs-lookup"><span data-stu-id="f7626-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-198">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-199">No</span><span class="sxs-lookup"><span data-stu-id="f7626-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-200">N/D</span><span class="sxs-lookup"><span data-stu-id="f7626-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-201">Controlla il catalogo del modello di impostazioni per i modelli nuovi, aggiornati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="f7626-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="f7626-202">Questa attività viene eseguita solo se è configurato SettingsTemplateCatalog.</span><span class="sxs-lookup"><span data-stu-id="f7626-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f7626-203">Raccogliere dati di analisi utilizzo software </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-204">Al servizio avvia accesso</span><span class="sxs-lookup"><span data-stu-id="f7626-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-205">No</span><span class="sxs-lookup"><span data-stu-id="f7626-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-206">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-207">N/D</span><span class="sxs-lookup"><span data-stu-id="f7626-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-208">Se l'utente o l'amministratore opta per il programma Analisi utilizzo software (Customer Experience Improvement Program), questa attività raccoglie i dati che consentono di migliorare le versioni future di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f7626-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f7626-209">Caricare i dati di analisi utilizzo software </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="f7626-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-210">Viene eseguito all'accesso e alle 4:00 ogni giorno da allora in poi.</span><span class="sxs-lookup"><span data-stu-id="f7626-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-211">No</span><span class="sxs-lookup"><span data-stu-id="f7626-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-212">Sì</span><span class="sxs-lookup"><span data-stu-id="f7626-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-213">Solo se la rete è connessa</span><span class="sxs-lookup"><span data-stu-id="f7626-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7626-214">Se l'utente o l'amministratore opta per il programma Analisi utilizzo software (Customer Experience Improvement Program), questa attività carica i dati nei server di analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="f7626-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f7626-215">Legenda</span><span class="sxs-lookup"><span data-stu-id="f7626-215">Legend</span></span>**

-   <span data-ttu-id="f7626-216">**Power Toggle** : l'utilità di pianificazione ottimizza il consumo di energia quando non viene collegata all'alimentazione CA.</span><span class="sxs-lookup"><span data-stu-id="f7626-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="f7626-217">Se il computer passa all'alimentazione a batteria, l'attività potrebbe arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="f7626-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="f7626-218">**Solo inattivo** : l'attività smetterà di funzionare se il computer cessa di essere inattivo.</span><span class="sxs-lookup"><span data-stu-id="f7626-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="f7626-219">Per impostazione predefinita, l'attività non viene riavviata quando il computer è di nuovo inattivo.</span><span class="sxs-lookup"><span data-stu-id="f7626-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="f7626-220">L'attività verrà invece riavviata nel trigger di attività successiva.</span><span class="sxs-lookup"><span data-stu-id="f7626-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="f7626-221">**Connessione di rete** : le attività contrassegnate come "Sì" vengono eseguite solo se il computer dispone di una connessione di rete disponibile.</span><span class="sxs-lookup"><span data-stu-id="f7626-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="f7626-222">Le attività contrassegnate come "N/d" vengono eseguite indipendentemente dalla connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="f7626-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="f7626-223">Come gestire le attività pianificate</span><span class="sxs-lookup"><span data-stu-id="f7626-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="f7626-224">Per trovare le attività pianificate, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7626-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="f7626-225">Aprire "Pianifica attività" nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f7626-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="f7626-226">Passare a: utilità di pianificazione- &gt; raccolta utilità di pianificazione- &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="f7626-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="f7626-227">Selezionare l'attività programmata che si vuole gestire e configurare nel riquadro dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="f7626-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="f7626-228">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="f7626-228">Additional information</span></span>

<span data-ttu-id="f7626-229">Le informazioni aggiuntive seguenti si applicano alle attività pianificate di UE-V:</span><span class="sxs-lookup"><span data-stu-id="f7626-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="f7626-230">i programmi di sequenza delle attività si trovano nella cartella di installazione dell'agente UE-V, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f7626-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="f7626-231">L'attività programmata del controller di sincronizzazione è il componente cruciale quando l'opzione UE-V SyncMethod è impostata su "SyncProvider" (configurazione predefinita di UE-V 2).</span><span class="sxs-lookup"><span data-stu-id="f7626-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="f7626-232">Questa attività pianificata mantiene la sincronizzazione di SettingsSToragePath con le versioni localmente memorizzate nella cache dei file del pacchetto di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f7626-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="f7626-233">Se gli utenti si lamentano che le impostazioni non vengono sincronizzate abbastanza spesso, è possibile ridurre l'impostazione di un'attività pianificata su un minimo di 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="f7626-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="f7626-234">Se necessario, è anche possibile aumentare i 30 minuti predefiniti per un importo superiore.</span><span class="sxs-lookup"><span data-stu-id="f7626-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="f7626-235">Se gli utenti si lamentano che le impostazioni non vengono sincronizzate abbastanza velocemente per l'accesso, è possibile rimuovere l'impostazione di ritardo per l'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="f7626-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="f7626-236">(È possibile trovare l'impostazione ritardo nella finestra di dialogo **Modifica trigger** )</span><span class="sxs-lookup"><span data-stu-id="f7626-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="f7626-237">Non è necessario disabilitare l'attività programmata di aggiornamento automatico del modello se si usa un altro metodo per sincronizzare i modelli dei client (ad esempio criteri di gruppo o previsioni di gestione configurazione).</span><span class="sxs-lookup"><span data-stu-id="f7626-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="f7626-238">Se si esce dal valore della proprietà SettingsTemplateCatalog, viene impedito a UE-V di controllare il catalogo delle impostazioni per i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f7626-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="f7626-239">Questa attività pianificata viene eseguita ApplySettingsCatalog.exe e verrà essenzialmente restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f7626-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="f7626-240">L'attività programmata per le impostazioni dell'applicazione di monitoraggio aggiornerà le impostazioni di app di Windows (AppX) in tempo reale, in base ai trigger di impostazione di programmi app di Windows incorporati in ogni app.</span><span class="sxs-lookup"><span data-stu-id="f7626-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="f7626-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7626-241">Related topics</span></span>


[<span data-ttu-id="f7626-242">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f7626-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="f7626-243">Distribuire UE-V 2. x per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="f7626-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





