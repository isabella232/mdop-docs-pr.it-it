---
title: Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI
description: Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804269"
---
# Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI


Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate dalla virtualizzazione dell'esperienza utente. UE-V include un set di modelli di posizione standard per le impostazioni. Include anche lo strumento generatore di UE-V che consente di creare modelli di posizione delle impostazioni personalizzati. Dopo aver creato e distribuito i modelli di posizione delle impostazioni, è possibile gestire questi modelli usando PowerShell o WMI.

## Gestire i modelli di posizione delle impostazioni con WMI e PowerShell


Le funzionalità WMI e PowerShell di UE-V includono la possibilità di abilitare, disabilitare, registrare, aggiornare e annullare la registrazione dei modelli di posizione delle impostazioni. Usando queste funzionalità, puoi automatizzare il processo di registrazione, aggiornamento o annullamento della registrazione dei modelli con l'agente UE-V. È anche possibile registrare manualmente i modelli usando i comandi WMI e PowerShell. Usando queste funzionalità in combinazione con una soluzione elettronica di distribuzione del software, criteri di gruppo o un altro metodo di distribuzione automatizzato, ad esempio uno script, puoi automatizzare ulteriormente questo processo.

Per aggiornare, registrare o annullare la registrazione di un modello di posizione delle impostazioni, è necessario disporre delle autorizzazioni di amministratore. Le autorizzazioni di amministratore non sono necessarie per abilitare o disabilitare i modelli.

**Per gestire i modelli di posizione delle impostazioni con PowerShell**

1.  Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell. Per importare il modulo **Microsoft UE-V PowerShell** , digitare il comando seguente al prompt dei comandi di PowerShell.

    ``` syntax
    Import-module UEV
    ```

2.  Usare i cmdlet di PowerShell seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando di PowerShell</strong></th>
    <th align="left"><strong>Descrizione</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati nel computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Registro-UevTemplate</p></td>
    <td align="left"><p>Registra un modello di posizione delle impostazioni con UE-V. Una volta registrato un modello, UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Annullamento della registrazione-UevTemplate</p></td>
    <td align="left"><p>Annulla la registrazione di un modello di posizione delle impostazioni con UE-V. Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Aggiorna un modello di posizione delle impostazioni con una versione più recente del modello. Il nuovo modello deve avere una versione successiva rispetto a quella esistente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Disable-UevTemplate</p></td>
    <td align="left"><p>Disabilita un modello di posizione delle impostazioni per l'utente corrente del computer.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Abilita un modello di posizione delle impostazioni per l'utente corrente del computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Test-UevTemplate</p></td>
    <td align="left"><p>Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

Le funzionalità di PowerShell UE-V consentono di gestire un gruppo di modelli di impostazioni distribuiti nell'organizzazione. Per gestire un gruppo di modelli tramite PowerShell, eseguire le operazioni seguenti.

**Per gestire un gruppo di modelli di posizione delle impostazioni con PowerShell**

1.  Modificare o aggiornare i modelli di posizione delle impostazioni desiderati.

2.  Distribuire i modelli di posizione delle impostazioni desiderati in una cartella accessibile al computer locale.

3.  Nel computer locale aprire una finestra di Windows PowerShell con i diritti di amministratore.

4.  Importando il modulo Microsoft UE-V PowerShell, digitando il comando seguente.

    ``` syntax
    Import-module UEV
    ```

5.  Annulla la registrazione di tutte le versioni precedentemente registrate dei modelli digitando il comando seguente.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Verrà annullata la registrazione di tutti i modelli attivi nel computer.

6.  Registrare i modelli aggiornati digitando il comando seguente.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Verranno registrati tutti i modelli di posizione delle impostazioni presenti nella cartella modello specificata.

La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente. Gli amministratori possono usare queste interfacce per gestire i modelli di posizione delle impostazioni da Windows PowerShell e automatizzare le attività amministrative del modello.

**Per gestire i modelli di posizione delle impostazioni con WMI**

1.  Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.

2.  Usare i comandi WMI seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.

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
    <td align="left"><p>Get-WmiObject-spazio dei nomi root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, templateName, TemplateVersion, Enabled | Format-tabella-AutoSize</p></td>
    <td align="left"><p>Elenca tutti i modelli di posizione delle impostazioni registrati per il computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-percorso modello per gli argomenti &lt;&gt;</p></td>
    <td align="left"><p>Registra un modello di posizione delle impostazioni con UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ID modello per gli argomenti &lt;&gt;</p></td>
    <td align="left"><p>Annulla la registrazione di un modello di posizione delle impostazioni con UE-V. Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ID modello per gli argomenti &lt;&gt;</p></td>
    <td align="left"><p>Abilita un modello di posizione delle impostazioni con UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ID modello per gli argomenti &lt;&gt;</p></td>
    <td align="left"><p>Disabilita un modello di posizione delle impostazioni con UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-percorso del &lt; modello arguments&gt;</p></td>
    <td align="left"><p>Aggiorna un modello di posizione delle impostazioni con UE-V. Il nuovo modello deve avere una versione superiore a quella esistente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-percorso del &lt; modello arguments&gt;</p></td>
    <td align="left"><p>Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

**Come distribuire l'agente UE-V con PowerShell**

1.  Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.

    **Nota**  USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V. Le versioni dei file di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura. Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.

     

2.  Usare uno dei comandi di PowerShell seguenti per installare l'agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Argomenti correlati


[Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





