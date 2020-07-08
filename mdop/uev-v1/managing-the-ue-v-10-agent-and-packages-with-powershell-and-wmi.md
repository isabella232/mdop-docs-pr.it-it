---
title: Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI
description: Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819296"
---
# Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI


È possibile usare WMI e PowerShell per gestire il comportamento della configurazione e della sincronizzazione dell'agente Microsoft Experience (UE-V).

**Come distribuire l'agente UE-V con PowerShell**

1.  Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.

    **Nota**  
    USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V. Le versioni dei file di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura. Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.



2.  Usare uno dei comandi di PowerShell seguenti per installare l'agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Come configurare l'agente UE-V con PowerShell**

1.  Usare un account con diritti di amministratore per aprire una finestra di PowerShell. Importare il modulo di PowerShell UE-V usando il comando seguente.

    ``` syntax
    Import-module UEV
    ```

2.  Usare i comandi di PowerShell seguenti per configurare l'agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando di PowerShell</strong></p></td>
    <td align="left"><p><strong>Descrizione</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Visualizzare le impostazioni effettive dell'agente UE-V. Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Visualizzare i valori delle impostazioni dell'agente UE-V solo per l'utente corrente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-computer</p></td>
    <td align="left"><p>Visualizzare i valori delle impostazioni di configurazione dell'agente UE-V per tutti gli utenti del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-computer- &lt; percorso di SettingsStoragePath per _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definire una posizione di archiviazione delle impostazioni per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; path to _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definire una posizione di archiviazione delle impostazioni per utente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-computer- &lt; timeout di SyncTimeoutInMilliseconds in millisecondi&gt;</p></td>
    <td align="left"><p>Impostare il timeout della sincronizzazione in millisecondi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser- &lt; timeout di SyncTimeoutInMilliseconds in millisecondi&gt;</p></td>
    <td align="left"><p>Impostare il timeout della sincronizzazione per l'utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-computer- &lt; dimensione MaxPackageSizeInBytes in byte&gt;</p></td>
    <td align="left"><p>Configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita. Impostare la dimensione del pacchetto soglia in byte.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; dimensione in byte&gt;</p></td>
    <td align="left"><p>Impostare la soglia di avviso dimensione pacchetto per l'utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-computer- &lt; percorso di SettingsTemplateCatalogPath per il catalogo&gt;</p></td>
    <td align="left"><p>Impostare il percorso del catalogo dei modelli di impostazioni.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-computer-metodo di sincronizzazione di SyncMethod &lt;&gt;</p></td>
    <td align="left"><p>Impostare il metodo di sincronizzazione: OfflineFiles o None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-metodo di sincronizzazione di SyncMethod &lt;&gt;</p></td>
    <td align="left"><p>Imposta il metodo di sincronizzazione per l'utente corrente: OfflineFiles o None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-computer-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Abilitare la notifica in caso di ritardo dell'importazione delle impostazioni utente.</p>
    <p>Usare-DisableSettingsImportNotify per disabilitare la notifica.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Abilitare la notifica per l'utente corrente quando l'importazione delle impostazioni utente viene ritardata.</p>
    <p>Usare-DisableSettingsImportNotify per disabilitare la notifica.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-computer-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Specificare l'ora in secondi prima della notifica dell'utente</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Specificare l'ora in secondi prima della notifica per l'utente corrente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-computer-DisableSync</p></td>
    <td align="left"><p>Disabilitare UE-V per tutti gli utenti del computer.</p>
    <p>Usare-EnableSync per abilitare o riattivare.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Disabilitare UE-V per l'utente corrente nel computer.</p>
    <p>Usare-EnableSync per abilitare o riattivare.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration- &lt; Nome impostazione computer&gt;</p></td>
    <td align="left"><p>Deselezionare un'impostazione specifica per tutti gli utenti del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration-CurrentComputerUser- &lt; Nome impostazione&gt;</p></td>
    <td align="left"><p>Deselezionare un'impostazione specifica per l'utente corrente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>&lt;File di migrazione delle impostazioni di Export-UevConfiguration&gt;</p></td>
    <td align="left"><p>Esportare la configurazione del computer UE-V in un file di migrazione delle impostazioni. L'estensione del file deve essere ". UEV".</p>
    <p>Il cmdlet Export Esporta tutte le impostazioni dell'agente UE-V che possono essere configurate con il parametro-computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>&lt;File di migrazione delle impostazioni di import-UevConfiguration&gt;</p></td>
    <td align="left"><p>Importare la configurazione di computer UE-V da un file di migrazione delle impostazioni (file con estensione UEV).</p></td>
    </tr>
    </tbody>
    </table>



**Come esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V con PowerShell**

1.  Aprire una finestra di PowerShell come amministratore. Importare il modulo di PowerShell UE-V con il comando seguente.

    ``` syntax
    Import-module UEV
    ```

2.  Usare i comandi di PowerShell seguenti per configurare l'agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando di PowerShell</strong></p></td>
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



**Come configurare l'agente UE-V con WMI**

1.  La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente. Gli amministratori possono usare questa interfaccia per configurare l'agente UE-V dalla riga di comando e automatizzare le attività di configurazione tipiche.

    Usare un account con diritti di amministratore per aprire una finestra di PowerShell.

2.  Usare i comandi WMI seguenti per configurare l'agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando di PowerShell</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-configurazione dello spazio dei nomi root\Microsoft\UEV</p>
    <p></p></td>
    <td align="left"><p>Visualizzare le impostazioni attive dell'agente UE-V. Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-spazio dei nomi root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>Visualizzare la configurazione dell'agente UE-V definita per l'utente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Visualizzare la configurazione dell'agente UE-V definita per il computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Definire una posizione di archiviazione delle impostazioni per computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Definire una posizione di archiviazione delle impostazioni per utente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Impostare il timeout della sincronizzazione in millisecondi.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita. Impostare la dimensione del file del pacchetto soglia in byte.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncMethod = &lt; sync_method&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Impostare il metodo di sincronizzazione: OfflineFiles o None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Aggiornare una specifica impostazione per computer. Per cancellare l'impostazione, usare $null come valore dell'impostazione.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</p>
    <p>$config. Inserire ()</p></td>
    <td align="left"><p>Aggiornare una specifica impostazione per utente. Per cancellare l'impostazione, usare $null come valore dell'impostazione.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Argomenti correlati


[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)









