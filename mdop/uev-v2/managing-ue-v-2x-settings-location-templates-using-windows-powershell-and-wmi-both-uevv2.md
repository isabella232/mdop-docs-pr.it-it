---
title: Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI
description: Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804558"
---
# Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usano i modelli di posizione delle impostazioni XML per definire le impostazioni che l'utente ha acquisito e si applica alla virtualizzazione. UE-V include un set di modelli di posizione standard per le impostazioni. Include anche lo strumento generatore di UE-V che consente di creare modelli di posizione delle impostazioni personalizzati. Dopo aver creato e distribuito i modelli di posizione delle impostazioni, è possibile gestire questi modelli usando Windows PowerShell e Strumentazione gestione Windows (WMI). Per un elenco completo dei cmdlet di PowerShell di UE-V, Vedi informazioni di [riferimento sui cmdlet di UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Gestire i modelli di posizione delle impostazioni di UE-V 2 con Windows PowerShell


Le caratteristiche di WMI e Windows PowerShell di UE-V includono la possibilità di abilitare, disabilitare, registrare, aggiornare e annullare la registrazione dei modelli di posizione delle impostazioni. Usando queste funzionalità, puoi automatizzare il processo di registrazione, aggiornamento o annullamento della registrazione dei modelli con l'agente UE-V. È anche possibile registrare manualmente i modelli usando i comandi WMI e Windows PowerShell. Usando queste funzionalità in combinazione con una soluzione elettronica di distribuzione del software, criteri di gruppo o un altro metodo di distribuzione automatizzato, ad esempio uno script, puoi automatizzare ulteriormente questo processo.

Per aggiornare, registrare o annullare la registrazione di un modello di posizione delle impostazioni, è necessario disporre delle autorizzazioni di amministratore. Le autorizzazioni di amministratore non sono necessarie per abilitare, disabilitare o elencare i modelli.

***<em>Per gestire i modelli di posizione delle impostazioni tramite Windows PowerShellell</em>***

1.  Usare un account con diritti di amministratore per aprire un prompt dei comandi di Windows PowerShell.

2.  Usare i cmdlet di Windows PowerShell seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati nel computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui il nome dell'applicazione o il nome del modello contiene una &lt; stringa &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui l'ID modello contiene una &lt; stringa &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui il nome dell'applicazione o del modello o l'ID modello contiene una &lt; stringa &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Ottiene il nome delle informazioni sul programma e sulla versione, che dipendono dall'ID modello.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Ottiene l'elenco effettivo delle app di Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Ottiene l'elenco delle app di Windows configurate per il computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Ottiene l'elenco delle app di Windows configurate per l'utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra uno o più modelli di posizione delle impostazioni con UE-V usando percorsi relativi e/o caratteri jolly nei percorsi di file. Dopo aver registrato un modello, l'UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra uno o più modelli di posizione delle impostazioni con UE-V usando i percorsi letterali, in cui nessun carattere può essere interpretato come caratteri jolly. Dopo aver registrato un modello, l'UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Annulla la registrazione di un modello di posizione delle impostazioni con UE-V. Quando un modello non viene registrato, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Annulla la registrazione di tutti i modelli di posizione delle impostazioni con UE-V. Quando un modello non viene registrato, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Aggiorna uno o più modelli di posizione delle impostazioni con una versione più recente del modello. Usare percorsi relativi e/o caratteri jolly nei percorsi di file. Il nuovo modello deve essere una versione più recente rispetto al modello esistente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Aggiorna uno o più modelli di posizione delle impostazioni con una versione più recente del modello. Usare percorsi completi per i file modello, in cui nessun carattere può essere interpretato come caratteri jolly. Il nuovo modello deve essere una versione più recente rispetto al modello esistente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Rimuove l'app di Windows dall'elenco delle app di Windows utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Rimuove tutte le app di Windows dall'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Rimuove tutte le app di Windows dall'elenco delle app di Windows utente corrente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Disabilita un modello di posizione delle impostazioni per l'utente corrente del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Disabilita una o più app di Windows nell'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Disabilita una o più app di Windows nell'elenco app utente corrente di Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Abilita un modello di posizione delle impostazioni per l'utente corrente del computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Consente di abilitare una o più app di Windows nell'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Consente di abilitare una o più app di Windows nell'elenco app utente corrente di Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina se uno o più modelli di posizione delle impostazioni sono conformi allo schema XML. Può usare percorsi relativi e caratteri jolly.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina se uno o più modelli di posizione delle impostazioni sono conformi allo schema XML. Il percorso deve essere un percorso completo del file del modello, ma non include caratteri jolly.</p></td>
    </tr>
    </tbody>
    </table>



Le funzionalità di Windows PowerShell UE-V consentono di gestire un gruppo di modelli di impostazioni distribuiti nell'organizzazione. Usare la procedura seguente per gestire un gruppo di modelli tramite Windows PowerShell.

**Per gestire un gruppo di modelli di posizione delle impostazioni tramite Windows PowerShell**

1.  Modificare o aggiornare i modelli di posizione delle impostazioni desiderati.

2.  Se si vogliono modificare o aggiornare i modelli di posizione delle impostazioni, distribuire i modelli di posizione delle impostazioni in una cartella accessibile al computer locale.

3.  Nel computer locale aprire una finestra di Windows PowerShell con i diritti di amministratore.

4.  Annulla la registrazione di tutte le versioni precedentemente registrate dei modelli digitando il comando seguente.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Questo comando Annulla la registrazione di tutti i modelli attivi nel computer.

5.  Registrare i modelli aggiornati digitando il comando seguente.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Questo comando registra tutti i modelli di posizione delle impostazioni che si trovano nella cartella modello specificata.

### <a href="" id="win8applist"></a>Elenco delle app di Windows

Elencando un'app di Windows nell'elenco delle app di Windows, devi specificare se l'app è abilitata o disabilitata per la sincronizzazione delle impostazioni. Le app sono identificate nell'elenco in base al nome della famiglia di pacchetti e se la sincronizzazione delle impostazioni deve essere abilitata o disabilitata per l'app. Quando si usano queste impostazioni insieme all'impostazione predefinita per il comportamento di sincronizzazione non elencata, è possibile controllare se le app di Windows sono sincronizzate.

Per visualizzare il nome della famiglia di pacchetti delle app di Windows installate, in un prompt dei comandi di Windows PowerShell immettere:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Per visualizzare un elenco di app di Windows che possono sincronizzare le impostazioni in un computer con il nome della famiglia di pacchetti, lo stato abilitato e l'origine abilitata, al prompt dei comandi di Windows PowerShell immettere: `Get-UevAppxPackage`

**Definizioni delle proprietà Get-UevAppxPackage**

<a href="" id="displayname"></a>**DisplayName**  
Nome visualizzato all'utente nell'applicazione centro impostazioni società. La `DisplayName` proprietà è derivata dalla `PackageFamilyName` Proprietà.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Nome del pacchetto installato per l'utente corrente.

<a href="" id="enabled"></a>**Abilitato**  
Definisce se le impostazioni per l'app sono configurate per la sincronizzazione.

<a href="" id="enabledsource"></a>**EnabledSource**  
La posizione in cui viene impostata la configurazione che Abilita o Disabilita l'app. I valori possibili sono: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*e *PolicyUser*.

<a href="" id="notset"></a>**NotSet**  
Il criterio non è configurato per sincronizzare l'app.

<a href="" id="localmachine"></a>**LocalMachine**  
Lo stato Enabled viene impostato nella sezione computer locale del registro di sistema.

<a href="" id="localuser"></a>**LocalUser**  
Lo stato Enabled viene impostato nella sezione utente corrente del registro di sistema.

<a href="" id="policymachine"></a>**PolicyMachine**  
Lo stato Enabled viene impostato nella sezione Policy della sezione computer locale del registro di sistema.

Per ottenere l'elenco configurato dall'utente delle app di Windows, al prompt dei comandi di Windows PowerShell immetti: `Get-UevAppxPackage –CurrentComputerUser`

Per ottenere l'elenco configurato dal computer delle app di Windows, al prompt dei comandi di Windows PowerShell immetti: `Get-UevAppxPackage –Computer`

Per i parametri, CurrentComputerUser o computer, il cmdlet restituisce un elenco delle app di Windows configurate dall'utente o a livello di computer.

**Definizioni delle proprietà**

<a href="" id="displayname"></a>**DisplayName**  
Nome visualizzato all'utente nell'applicazione centro impostazioni società. La `DisplayName` proprietà è derivata dalla `PackageFamilyName` Proprietà.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
Nome del pacchetto installato per l'utente corrente.

<a href="" id="enabled"></a>**Abilitato**  
Definisce se le impostazioni per l'app sono configurate per la sincronizzazione per l'opzione specificata, ovvero l' **utente** o il **computer**.

<a href="" id="installed"></a>**Installato**  
True se l'app, ovvero PackageFamilyName, è installata per l'utente corrente.

### Gestire i modelli di posizione delle impostazioni di UE-V 2 tramite WMI

La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente. Gli amministratori possono usare queste interfacce per gestire i modelli di posizione delle impostazioni da Windows PowerShell e automatizzare le attività amministrative del modello.

**Per gestire i modelli di posizione delle impostazioni tramite WMI**

1.  Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.

2.  Usare i comandi WMI seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati per il computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Ottiene il nome delle informazioni sul programma e sulla versione, che dipendono dal nome del modello.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Ottiene l'elenco effettivo delle app di Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-spazio dei nomi root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Ottiene l'elenco delle app di Windows configurate per il computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Ottiene l'elenco delle app di Windows configurate per l'utente corrente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Registra un modello di posizione delle impostazioni con UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Annulla la registrazione di un modello di posizione delle impostazioni con UE-V. Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Aggiorna un modello di posizione delle impostazioni con UE-V. Il nuovo modello deve essere una versione più recente rispetto a quella esistente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows utente corrente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Disabilita uno o più modelli di posizione delle impostazioni con UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Disabilita una o più app di Windows nell'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Disabilita una o più app di Windows nell'elenco app utente corrente di Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Abilita un modello di posizione delle impostazioni con UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Abilita le app di Windows nell'elenco delle app di Windows per computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Abilita le app di Windows nell'elenco app utente corrente di Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Distribuzione dell'agente UE-V con Windows PowerShell

**Come distribuire l'agente UE-V tramite Windows PowerShell**

1.  Organizzare il pacchetto di installazione dell'agente UE-V in una condivisione di rete accessibile.

    **Nota**  
    USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V. I pacchetti di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura. Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.



2.  Usare uno dei comandi di Windows PowerShell seguenti per installare l'agente UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Hai un suggerimento per l'UE-V**? Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **È stato ottenuto un problema UE-V**? Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Argomenti correlati


[Amministrazione di UE-V 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









