---
title: Gestione dell'agente e dei pacchetti UE-V 2. x con Windows PowerShell e WMI
description: Gestione dell'agente e dei pacchetti UE-V 2. x con Windows PowerShell e WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826805"
---
# <span data-ttu-id="a3ff4-103">Gestione dell'agente e dei pacchetti UE-V 2. x con Windows PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="a3ff4-104">È possibile usare Strumentazione gestione Windows (WMI) e Windows PowerShell per gestire la configurazione e la sincronizzazione degli agenti Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="a3ff4-105">Per un elenco completo dei cmdlet di PowerShell di UE-V, Vedi informazioni di [riferimento sui cmdlet di UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="a3ff4-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="a3ff4-106">Per distribuire l'agente UE-V tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3ff4-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="a3ff4-107">Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="a3ff4-108">Nota</span><span class="sxs-lookup"><span data-stu-id="a3ff4-108">Note</span></span>**  
    <span data-ttu-id="a3ff4-109">USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="a3ff4-110">I pacchetti di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="a3ff4-111">Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="a3ff4-112">Usare uno dei comandi di Windows PowerShell seguenti per installare l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="a3ff4-113">Per configurare l'agente UE-V tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3ff4-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="a3ff4-114">Aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="a3ff4-115">Per gestire le impostazioni del computer che interessano tutti gli utenti del computer usando il parametro *computer* , aprire la finestra con un account con diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="a3ff4-116">Usare i comandi di Windows PowerShell seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a3ff4-117">Comando di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3ff4-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="a3ff4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ff4-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-119">Ottiene le impostazioni effettive dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="a3ff4-120">Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-121">Ottiene i valori delle impostazioni dell'agente UE-V solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-122">Ottiene i valori delle impostazioni di configurazione dell'agente UE-V per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-123">Ottiene i dettagli per ogni impostazione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="a3ff4-124">Visualizza il punto in cui è configurata l'impostazione o se usa il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="a3ff4-125">Viene visualizzato se l'impostazione corrente è valida.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-126">Imposta il testo visualizzato nel centro impostazioni società per il collegamento alla guida.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-127">Imposta l'URL del collegamento nel centro impostazioni società per il collegamento della guida.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="a3ff4-128">Può essere usato qualsiasi protocollo URL.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-129">Configura l'agente UE-V per non sincronizzare le app di Windows per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-130">Configura l'agente UE-V per non sincronizzare le app di Windows per l'utente del computer corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-131">Configura l'agente UE-V per visualizzare la notifica al primo esecuzione dell'agente per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-132">Configura l'agente UE-V per non visualizzare la notifica la prima volta che l'agente viene eseguito per tutti gli utenti nel computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-133">Configura l'agente UE-V per inviare una notifica a tutti gli utenti del computer quando la sincronizzazione delle impostazioni viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="a3ff4-134">Usa il <em> </em> parametro DisableSettingsImportNotify per disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-135">Configura l'agente UE-V per avvisare l'utente corrente quando la sincronizzazione delle impostazioni viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="a3ff4-136">Usa il <em> </em> parametro DisableSettingsImportNotify per disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-137">Configura l'agente UE-V per sincronizzare tutte le app di Windows che non sono esplicitamente disabilitate dall'elenco delle app di Windows per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="a3ff4-138">Per altre informazioni, vedere &quot; Get-UevAppxPackage &quot; nella sezione <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="a3ff4-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="a3ff4-139">Usa il <em> </em> parametro DisableSyncUnlistedWindows8Apps per configurare l'agente UE-V per sincronizzare solo le app di Windows esplicitamente abilitate dall'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-140">Configura l'agente UE-V per sincronizzare tutte le app di Windows che non sono esplicitamente disabilitate dall'elenco delle app di Windows per l'utente corrente nel computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="a3ff4-141">Per altre informazioni, vedere &quot; Get-UevAppxPackage &quot; nella sezione <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="a3ff4-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="a3ff4-142">Usa il <em> </em> parametro DisableSyncUnlistedWindows8Apps per configurare l'agente UE-V per sincronizzare solo le app di Windows esplicitamente abilitate dall'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-143">Disabilita la versione UE-V per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="a3ff4-144">Usa il <em> </em> parametro EnableSync per abilitare o riattivare.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-145">Disabilita UE-V per l'utente corrente nel computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="a3ff4-146">Usa il <em> </em> parametro EnableSync per abilitare o riattivare.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-147">Abilita l'icona UE-V nell'area di notifica per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="a3ff4-148">Usa il <em> </em> parametro DisableTrayIcon per disabilitare l'icona.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-149">Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge la soglia definita per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="a3ff4-150">Imposta la dimensione del pacchetto soglia in byte.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-151">Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge la soglia definita.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="a3ff4-152">Imposta la soglia di avviso per le dimensioni del pacchetto per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-153">Specifica il tempo in secondi prima che l'utente venga avvisato per tutti gli utenti del computer</span><span class="sxs-lookup"><span data-stu-id="a3ff4-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-154">Specifica l'ora in secondi prima dell'invio della notifica per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-155">Definisce un percorso di archiviazione delle impostazioni per ogni computer per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-156">Definisce una posizione di archiviazione delle impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-157">Imposta il percorso del catalogo dei modelli di impostazioni per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-158">Imposta il metodo di sincronizzazione per tutti gli utenti del computer: SyncProvider o None.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-159">Imposta il metodo di sincronizzazione per l'utente corrente: SyncProvider o None.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-160">Imposta il timeout della sincronizzazione in millisecondi per tutti gli utenti del computer</span><span class="sxs-lookup"><span data-stu-id="a3ff4-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-161">Impostare il timeout della sincronizzazione per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-162">Cancella l'impostazione specificata per tutti gli utenti nel computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-163">Cancella l'impostazione specificata solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-164">Esporta la configurazione del computer UE-V in un file di migrazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="a3ff4-165">L'estensione del nome file deve essere. UEV.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="a3ff4-166">Il <code>Export</code> cmdlet Esporta tutte le impostazioni dell'agente UE-V che possono essere configurate con il <em> </em> parametro computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="a3ff4-167">Importa la configurazione di computer UE-V da un file di migrazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="a3ff4-168">L'estensione del nome file deve essere. UEV.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="a3ff4-169">Per esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3ff4-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="a3ff4-170">Aprire una finestra di Windows PowerShell come amministratore.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="a3ff4-171">Usare i comandi di Windows PowerShell seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="a3ff4-172">Comando di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3ff4-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="a3ff4-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ff4-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a3ff4-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="a3ff4-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-175">Estrae le impostazioni da un file di pacchetto del calcolatore Microsoft e le converte in un formato leggibile in XML.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a3ff4-176">Repair-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="a3ff4-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-177">Ripristina l'indice dei modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="a3ff4-178">Per configurare l'agente UE-V tramite WMI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="a3ff4-179">La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="a3ff4-180">Gli amministratori possono usare questa interfaccia per configurare l'agente UE-V alla riga di comando e automatizzare le attività di configurazione tipiche.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="a3ff4-181">Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="a3ff4-182">Usare i comandi WMI seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="a3ff4-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ff4-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-184">Visualizza le impostazioni attive dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="a3ff4-185">Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-186">Visualizza la configurazione dell'agente UE-V definita per un utente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-187">Visualizza la configurazione dell'agente UE-V definita per un computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-188">Visualizza i dettagli per ogni elemento di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="a3ff4-189">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="a3ff4-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-190">Definisce un percorso di archiviazione delle impostazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-191">Definisce una posizione di archiviazione delle impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-192">Imposta il timeout della sincronizzazione in millisecondi per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-193">Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="a3ff4-194">Impostare la dimensione del file del pacchetto soglia in byte per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-195">Imposta il metodo di sincronizzazione per tutti gli utenti del computer: SyncProvider o None.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-196">Per abilitare una specifica impostazione per computer, deselezionare l'impostazione e usare <em> $null </em> come valore di impostazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="a3ff4-197">Usare UserConfiguration per le impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-198">Per disabilitare una specifica impostazione per computer, deselezionare l'impostazione e usare <em> $null </em> come valore di impostazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="a3ff4-199">Usare la configurazione utente per le impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-200">Aggiorna una specifica impostazione per computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="a3ff4-201">Per cancellare l'impostazione, usare <em> $null </em> come valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="a3ff4-202">$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</span><span class="sxs-lookup"><span data-stu-id="a3ff4-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-203">Aggiorna una specifica impostazione per utente per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="a3ff4-204">Per cancellare l'impostazione, usare <em> $null </em> come valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="a3ff4-205">Per esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V tramite WMI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="a3ff4-206">In UE-V è disponibile il set di comandi WMI seguente.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="a3ff4-207">Gli amministratori possono usare questa interfaccia per esportare un pacchetto o ripristinare i modelli UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="a3ff4-208">Usare i comandi WMI seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a3ff4-209">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="a3ff4-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ff4-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-211">Estrae le impostazioni da un file di pacchetto e le converte in un formato leggibile in XML.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="a3ff4-212">Ripristina l'indice dei modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="a3ff4-213">Deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="a3ff4-214">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3ff4-214">Related topics</span></span>


[<span data-ttu-id="a3ff4-215">Amministrazione di UE-V 2. x con Windows PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="a3ff4-216">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="a3ff4-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









