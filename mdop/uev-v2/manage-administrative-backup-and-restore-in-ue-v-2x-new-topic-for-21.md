---
title: Gestire il backup e il ripristino amministrativi in UE-V 2. x
description: Gestire il backup e il ripristino amministrativi in UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827386"
---
# <span data-ttu-id="f8a42-103">Gestire il backup e il ripristino amministrativi in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f8a42-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="f8a42-104">In qualità di amministratore di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, è possibile ripristinare lo stato originale delle impostazioni dell'applicazione e di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="f8a42-105">E nuovo in UE-V 2,1 è anche possibile ripristinare altre impostazioni quando un utente adotta un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="f8a42-106">Ripristinare le impostazioni in UE-V 2,1 o UE-V 2,1 SP1 quando un utente adotta un nuovo dispositivo</span><span class="sxs-lookup"><span data-stu-id="f8a42-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="f8a42-107">Per ripristinare le impostazioni quando un utente adotta un nuovo dispositivo, è possibile inserire un modello di posizione di impostazioni nel profilo di **backup** o **roaming (impostazione predefinita)** usando il cmdlet Set-UevTemplateProfile di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8a42-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="f8a42-108">In questo modo, le impostazioni del computer vengono sincronizzate con il nuovo computer, oltre alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="f8a42-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="f8a42-109">I modelli assegnati al profilo di backup vengono backup per il dispositivo e configurati in base al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="f8a42-110">Per le impostazioni di backup di un modello, usare il cmdlet seguente in Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f8a42-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="f8a42-111">&lt;TemplateID &gt; è l'ID modello UE-V</span><span class="sxs-lookup"><span data-stu-id="f8a42-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="f8a42-112">&lt;il backup &gt; può essere un backup o un roaming</span><span class="sxs-lookup"><span data-stu-id="f8a42-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="f8a42-113">Quando si sostituisce il dispositivo UE-V di un utente, ripristina automaticamente le impostazioni se il dominio, il nome utente e l'utente del dispositivo corrispondono.</span><span class="sxs-lookup"><span data-stu-id="f8a42-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="f8a42-114">Tutti i dati sincronizzati e quelli di backup vengono ripristinati automaticamente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="f8a42-115">È anche possibile usare il nuovo cmdlet di PowerShell, Restore-UevBackup, per ripristinare le impostazioni da un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="f8a42-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="f8a42-116">Per clonare i pacchetti di impostazioni per il nuovo dispositivo, usare il cmdlet seguente in Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f8a42-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="f8a42-117">dove &lt; MachineName &gt; è il nome del computer del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="f8a42-118">I modelli come il modello Office 2013 che includono molte applicazioni possono essere inclusi nel profilo roamed (predefinito) o backup.</span><span class="sxs-lookup"><span data-stu-id="f8a42-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="f8a42-119">Le singole app in una serie di modelli seguono il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="f8a42-120">I modelli di Office 2013 in-box includono sia le impostazioni di solo roaming che di backup.</span><span class="sxs-lookup"><span data-stu-id="f8a42-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="f8a42-121">Le impostazioni solo backup non possono essere incluse in un profilo roaming.</span><span class="sxs-lookup"><span data-stu-id="f8a42-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="f8a42-122">Nell'ambito della funzionalità backup/ripristino, l'opzione UE-V ha aggiunto l' **Ultima nota positiva (LKG)** alle opzioni per il rollback delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a42-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="f8a42-123">In questa versione è possibile eseguire il rollback delle impostazioni originali o LKG.</span><span class="sxs-lookup"><span data-stu-id="f8a42-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="f8a42-124">Le impostazioni di LKG consentono agli utenti di eseguire il rollback a un punto intermedio e stabile in anticipo rispetto allo stato pre-UE-V delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a42-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="f8a42-125">Come eseguire il backup/ripristino dei modelli con UE-V</span><span class="sxs-lookup"><span data-stu-id="f8a42-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="f8a42-126">Questi sono i componenti principali per il backup e il ripristino di UE-V:</span><span class="sxs-lookup"><span data-stu-id="f8a42-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="f8a42-127">Profili modello</span><span class="sxs-lookup"><span data-stu-id="f8a42-127">Template profiles</span></span>

-   <span data-ttu-id="f8a42-128">Posizione dei pacchetti di impostazioni nel modello di posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="f8a42-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="f8a42-129">Trigger di backup</span><span class="sxs-lookup"><span data-stu-id="f8a42-129">Backup trigger</span></span>

-   <span data-ttu-id="f8a42-130">Ripristino delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="f8a42-130">How settings are restored</span></span>

**<span data-ttu-id="f8a42-131">Profili modello</span><span class="sxs-lookup"><span data-stu-id="f8a42-131">Template Profiles</span></span>**

<span data-ttu-id="f8a42-132">Un profilo modello UE-V viene definito quando il modello viene registrato nel dispositivo o dopo la registrazione tramite l'utilità di configurazione di PowerShell/WMI.</span><span class="sxs-lookup"><span data-stu-id="f8a42-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="f8a42-133">I tipi di profilo includono:</span><span class="sxs-lookup"><span data-stu-id="f8a42-133">The profile types include:</span></span>

-   <span data-ttu-id="f8a42-134">Roaming (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8a42-134">Roaming (default)</span></span>

-   <span data-ttu-id="f8a42-135">Backup</span><span class="sxs-lookup"><span data-stu-id="f8a42-135">Backup</span></span>

-   <span data-ttu-id="f8a42-136">Backuponly</span><span class="sxs-lookup"><span data-stu-id="f8a42-136">BackupOnly</span></span>

<span data-ttu-id="f8a42-137">Tutti i modelli sono inclusi nel profilo roaming quando sono registrati, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="f8a42-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="f8a42-138">Questi modelli sincronizzano le impostazioni con tutti i dispositivi abilitati per l'UE-V con il modello corrispondente abilitato.</span><span class="sxs-lookup"><span data-stu-id="f8a42-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="f8a42-139">I modelli possono essere aggiunti al profilo di backup con PowerShell o WMI usando il cmdlet Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="f8a42-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="f8a42-140">Modelli nel profilo di backup eseguire il backup di queste impostazioni nella posizione di archiviazione delle impostazioni in una directory di nome dispositivo speciale.</span><span class="sxs-lookup"><span data-stu-id="f8a42-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="f8a42-141">Le impostazioni specificate sono supportate in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="f8a42-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="f8a42-142">I modelli designati in modo indesiderato includono le impostazioni specifiche del dispositivo che non devono essere sincronizzate, a meno che non vengano esplicitamente ripristinate.</span><span class="sxs-lookup"><span data-stu-id="f8a42-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="f8a42-143">Queste impostazioni sono archiviate nella stessa posizione del pacchetto di impostazioni specifiche del dispositivo nella posizione di archiviazione delle impostazioni come impostazioni di backedup.</span><span class="sxs-lookup"><span data-stu-id="f8a42-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="f8a42-144">Questi modelli hanno un identificatore speciale incorporato nel modello che specifica che deve essere incluso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="f8a42-145">Posizione dei pacchetti di impostazioni nel modello di posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="f8a42-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="f8a42-146">Le impostazioni del profilo mobile sono archiviate nel percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a42-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="f8a42-147">I modelli assegnati al backup o al profilo backuponly archiviano le impostazioni nella posizione di archiviazione delle impostazioni in una directory di nome dispositivo speciale.</span><span class="sxs-lookup"><span data-stu-id="f8a42-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="f8a42-148">Ogni dispositivo con modelli in questi profili ha il proprio nome di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="f8a42-149">UE-V non pulisce queste directory.</span><span class="sxs-lookup"><span data-stu-id="f8a42-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="f8a42-150">Trigger di backup</span><span class="sxs-lookup"><span data-stu-id="f8a42-150">Backup trigger</span></span>**

<span data-ttu-id="f8a42-151">Il backup viene attivato dagli stessi eventi che attivano una sincronizzazione UE-V.</span><span class="sxs-lookup"><span data-stu-id="f8a42-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="f8a42-152">Ripristino delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="f8a42-152">How settings are restored</span></span>**

<span data-ttu-id="f8a42-153">Il ripristino del dispositivo di un utente ripristina le impostazioni del modello attualmente registrato dalla cartella di backup di un altro dispositivo e tutte le impostazioni sincronizzate con il computer corrente.</span><span class="sxs-lookup"><span data-stu-id="f8a42-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="f8a42-154">Le impostazioni vengono ripristinate in due modi:</span><span class="sxs-lookup"><span data-stu-id="f8a42-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="f8a42-155">Ripristino automatico</span><span class="sxs-lookup"><span data-stu-id="f8a42-155">Automatic restore</span></span>**

    <span data-ttu-id="f8a42-156">Se il percorso di archiviazione delle impostazioni UE-V dell'utente, il dominio e il nome del computer corrispondono all'utente corrente, tutte le impostazioni per l'utente vengono sincronizzate, con solo le impostazioni più recenti applicate.</span><span class="sxs-lookup"><span data-stu-id="f8a42-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="f8a42-157">Se un utente accede a un nuovo dispositivo per la prima volta e questi criteri vengono soddisfatti, i dati delle impostazioni vengono applicati a tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="f8a42-158">Nota</span><span class="sxs-lookup"><span data-stu-id="f8a42-158">Note</span></span>**  
    <span data-ttu-id="f8a42-159">L'accessibilità e le impostazioni desktop di Windows richiedono che l'utente riacceda a Windows per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8a42-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="f8a42-160">Ripristino manuale</span><span class="sxs-lookup"><span data-stu-id="f8a42-160">Manual Restore</span></span>**

    <span data-ttu-id="f8a42-161">Se vuoi aiutare gli utenti a ripristinare un dispositivo durante l'aggiornamento, puoi scegliere di usare il cmdlet Restore-UevBackup.</span><span class="sxs-lookup"><span data-stu-id="f8a42-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="f8a42-162">Questo comando fa sì che le impostazioni dell'utente vengano scaricate dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f8a42-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="f8a42-163">Ripristinare lo stato originale dell'applicazione e delle impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="f8a42-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="f8a42-164">I comandi WMI e Windows PowerShell consentono di ripristinare le impostazioni dell'applicazione e di Windows nei valori delle impostazioni presenti nel computer la prima volta che l'applicazione è stata avviata dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f8a42-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="f8a42-165">Questa azione di ripristino viene eseguita in base alle impostazioni per applicazione o Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="f8a42-166">Le impostazioni vengono ripristinate la volta successiva che l'applicazione viene eseguita o le impostazioni vengono ripristinate quando l'utente accede al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f8a42-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="f8a42-167">Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con Windows PowerShell per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f8a42-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="f8a42-168">Aprire la finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8a42-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="f8a42-169">Immettere il cmdlet di Windows PowerShell seguente per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="f8a42-170">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8a42-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="f8a42-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8a42-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="f8a42-172">Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="f8a42-173">Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con WMI</span><span class="sxs-lookup"><span data-stu-id="f8a42-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="f8a42-174">Aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8a42-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="f8a42-175">Immettere il comando WMI seguente per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="f8a42-176">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="f8a42-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="f8a42-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8a42-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="f8a42-178">Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a42-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="f8a42-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8a42-179">Related topics</span></span>


[<span data-ttu-id="f8a42-180">Amministrazione di UE-V 2. x con Windows PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="f8a42-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="f8a42-181">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f8a42-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









