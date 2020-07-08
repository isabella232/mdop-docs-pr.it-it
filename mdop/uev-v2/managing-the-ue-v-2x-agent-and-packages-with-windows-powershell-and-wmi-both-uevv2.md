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
# Gestione dell'agente e dei pacchetti UE-V 2. x con Windows PowerShell e WMI


È possibile usare Strumentazione gestione Windows (WMI) e Windows PowerShell per gestire la configurazione e la sincronizzazione degli agenti Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1. Per un elenco completo dei cmdlet di PowerShell di UE-V, Vedi informazioni di [riferimento sui cmdlet di UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Per distribuire l'agente UE-V tramite Windows PowerShell**

1.  Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.

    **Nota**  
    USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V. I pacchetti di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura. Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.



2.  Usare uno dei comandi di Windows PowerShell seguenti per installare l'agente UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Per configurare l'agente UE-V tramite Windows PowerShell**

1. Aprire una finestra di Windows PowerShell. Per gestire le impostazioni del computer che interessano tutti gli utenti del computer usando il parametro *computer* , aprire la finestra con un account con diritti di amministratore.

2. Usare i comandi di Windows PowerShell seguenti per configurare l'agente.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Comando di Windows PowerShell</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Ottiene le impostazioni effettive dell'agente UE-V. Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Ottiene i valori delle impostazioni dell'agente UE-V solo per l'utente corrente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Ottiene i valori delle impostazioni di configurazione dell'agente UE-V per tutti gli utenti del computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Ottiene i dettagli per ogni impostazione di configurazione. Visualizza il punto in cui è configurata l'impostazione o se usa il valore predefinito. Viene visualizzato se l'impostazione corrente è valida.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Imposta il testo visualizzato nel centro impostazioni società per il collegamento alla guida.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Imposta l'URL del collegamento nel centro impostazioni società per il collegamento della guida. Può essere usato qualsiasi protocollo URL.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per non sincronizzare le app di Windows per tutti gli utenti del computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per non sincronizzare le app di Windows per l'utente del computer corrente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per visualizzare la notifica al primo esecuzione dell'agente per tutti gli utenti del computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per non visualizzare la notifica la prima volta che l'agente viene eseguito per tutti gli utenti nel computer.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per inviare una notifica a tutti gli utenti del computer quando la sincronizzazione delle impostazioni viene ritardata.</p>
   <p>Usa il <em> </em> parametro DisableSettingsImportNotify per disabilitare la notifica.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per avvisare l'utente corrente quando la sincronizzazione delle impostazioni viene ritardata.</p>
   <p>Usa il <em> </em> parametro DisableSettingsImportNotify per disabilitare la notifica.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per sincronizzare tutte le app di Windows che non sono esplicitamente disabilitate dall'elenco delle app di Windows per tutti gli utenti del computer. Per altre informazioni, vedere &quot; Get-UevAppxPackage &quot; nella sezione <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI </a> .</p>
   <p>Usa il <em> </em> parametro DisableSyncUnlistedWindows8Apps per configurare l'agente UE-V per sincronizzare solo le app di Windows esplicitamente abilitate dall'elenco delle app di Windows.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per sincronizzare tutte le app di Windows che non sono esplicitamente disabilitate dall'elenco delle app di Windows per l'utente corrente nel computer. Per altre informazioni, vedere &quot; Get-UevAppxPackage &quot; nella sezione <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI </a> .</p>
   <p>Usa il <em> </em> parametro DisableSyncUnlistedWindows8Apps per configurare l'agente UE-V per sincronizzare solo le app di Windows esplicitamente abilitate dall'elenco delle app di Windows.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Disabilita la versione UE-V per tutti gli utenti del computer.</p>
   <p>Usa il <em> </em> parametro EnableSync per abilitare o riattivare.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Disabilita UE-V per l'utente corrente nel computer.</p>
   <p>Usa il <em> </em> parametro EnableSync per abilitare o riattivare.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Abilita l'icona UE-V nell'area di notifica per tutti gli utenti del computer.</p>
   <p>Usa il <em> </em> parametro DisableTrayIcon per disabilitare l'icona.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge la soglia definita per tutti gli utenti del computer. Imposta la dimensione del pacchetto soglia in byte.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge la soglia definita. Imposta la soglia di avviso per le dimensioni del pacchetto per l'utente corrente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Specifica il tempo in secondi prima che l'utente venga avvisato per tutti gli utenti del computer</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Specifica l'ora in secondi prima dell'invio della notifica per l'utente corrente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Definisce un percorso di archiviazione delle impostazioni per ogni computer per tutti gli utenti del computer.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Definisce una posizione di archiviazione delle impostazioni per utente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Imposta il percorso del catalogo dei modelli di impostazioni per tutti gli utenti del computer.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Imposta il metodo di sincronizzazione per tutti gli utenti del computer: SyncProvider o None.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Imposta il metodo di sincronizzazione per l'utente corrente: SyncProvider o None.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Imposta il timeout della sincronizzazione in millisecondi per tutti gli utenti del computer</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Impostare il timeout della sincronizzazione per l'utente corrente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Cancella l'impostazione specificata per tutti gli utenti nel computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Cancella l'impostazione specificata solo per l'utente corrente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Esporta la configurazione del computer UE-V in un file di migrazione delle impostazioni. L'estensione del nome file deve essere. UEV.</p>
   <p>Il <code>Export</code> cmdlet Esporta tutte le impostazioni dell'agente UE-V che possono essere configurate con il <em> </em> parametro computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Importa la configurazione di computer UE-V da un file di migrazione delle impostazioni. L'estensione del nome file deve essere. UEV.</p></td>
   </tr>
   </tbody>
   </table>



**Per esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V tramite Windows PowerShell**

1.  Aprire una finestra di Windows PowerShell come amministratore.

2.  Usare i comandi di Windows PowerShell seguenti per configurare l'agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando di Windows PowerShell</strong></p></td>
    <td align="left"><p><strong>Descrizione</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Estrae le impostazioni da un file di pacchetto del calcolatore Microsoft e le converte in un formato leggibile in XML.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Repair-UevTemplateIndex</p></td>
    <td align="left"><p>Ripristina l'indice dei modelli di posizione delle impostazioni di UE-V.</p></td>
    </tr>
    </tbody>
    </table>



**Per configurare l'agente UE-V tramite WMI**

1.  La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente. Gli amministratori possono usare questa interfaccia per configurare l'agente UE-V alla riga di comando e automatizzare le attività di configurazione tipiche.

    Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.

2.  Usare i comandi WMI seguenti per configurare l'agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Visualizza le impostazioni attive dell'agente UE-V. Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Visualizza la configurazione dell'agente UE-V definita per un utente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Visualizza la configurazione dell'agente UE-V definita per un computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Visualizza i dettagli per ogni elemento di configurazione.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Definisce un percorso di archiviazione delle impostazioni per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Definisce una posizione di archiviazione delle impostazioni per utente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Imposta il timeout della sincronizzazione in millisecondi per tutti gli utenti del computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Configura l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita. Impostare la dimensione del file del pacchetto soglia in byte per tutti gli utenti del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Imposta il metodo di sincronizzazione per tutti gli utenti del computer: SyncProvider o None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Per abilitare una specifica impostazione per computer, deselezionare l'impostazione e usare <em> $null </em> come valore di impostazione. Usare UserConfiguration per le impostazioni per utente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Per disabilitare una specifica impostazione per computer, deselezionare l'impostazione e usare <em> $null </em> come valore di impostazione. Usare la configurazione utente per le impostazioni per utente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Aggiorna una specifica impostazione per computer. Per cancellare l'impostazione, usare <em> $null </em> come valore dell'impostazione.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Aggiorna una specifica impostazione per utente per tutti gli utenti del computer. Per cancellare l'impostazione, usare <em> $null </em> come valore dell'impostazione.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**Per esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V tramite WMI**

1.  In UE-V è disponibile il set di comandi WMI seguente. Gli amministratori possono usare questa interfaccia per esportare un pacchetto o ripristinare i modelli UE-V.

2.  Usare i comandi WMI seguenti.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando WMI</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Estrae le impostazioni da un file di pacchetto e le converte in un formato leggibile in XML.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Ripristina l'indice dei modelli di posizione delle impostazioni di UE-V. Deve essere eseguito come amministratore.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Argomenti correlati


[Amministrazione di UE-V 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









