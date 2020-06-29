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
# Gestire il backup e il ripristino amministrativi in UE-V 2. x


In qualità di amministratore di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, è possibile ripristinare lo stato originale delle impostazioni dell'applicazione e di Windows. E nuovo in UE-V 2,1 è anche possibile ripristinare altre impostazioni quando un utente adotta un nuovo dispositivo.

## Ripristinare le impostazioni in UE-V 2,1 o UE-V 2,1 SP1 quando un utente adotta un nuovo dispositivo


Per ripristinare le impostazioni quando un utente adotta un nuovo dispositivo, è possibile inserire un modello di posizione di impostazioni nel profilo di **backup** o **roaming (impostazione predefinita)** usando il cmdlet Set-UevTemplateProfile di PowerShell. In questo modo, le impostazioni del computer vengono sincronizzate con il nuovo computer, oltre alle impostazioni utente. I modelli assegnati al profilo di backup vengono backup per il dispositivo e configurati in base al dispositivo. Per le impostazioni di backup di un modello, usare il cmdlet seguente in Windows PowerShell:

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;TemplateID &gt; è l'ID modello UE-V

-   &lt;il backup &gt; può essere un backup o un roaming

Quando si sostituisce il dispositivo UE-V di un utente, ripristina automaticamente le impostazioni se il dominio, il nome utente e l'utente del dispositivo corrispondono. Tutti i dati sincronizzati e quelli di backup vengono ripristinati automaticamente nel dispositivo.

È anche possibile usare il nuovo cmdlet di PowerShell, Restore-UevBackup, per ripristinare le impostazioni da un dispositivo diverso. Per clonare i pacchetti di impostazioni per il nuovo dispositivo, usare il cmdlet seguente in Windows PowerShell:

``` syntax
Restore-UevBackup –Machine <MachineName>
```

dove &lt; MachineName &gt; è il nome del computer del dispositivo.

I modelli come il modello Office 2013 che includono molte applicazioni possono essere inclusi nel profilo roamed (predefinito) o backup. Le singole app in una serie di modelli seguono il gruppo. I modelli di Office 2013 in-box includono sia le impostazioni di solo roaming che di backup. Le impostazioni solo backup non possono essere incluse in un profilo roaming.

Nell'ambito della funzionalità backup/ripristino, l'opzione UE-V ha aggiunto l' **Ultima nota positiva (LKG)** alle opzioni per il rollback delle impostazioni. In questa versione è possibile eseguire il rollback delle impostazioni originali o LKG. Le impostazioni di LKG consentono agli utenti di eseguire il rollback a un punto intermedio e stabile in anticipo rispetto allo stato pre-UE-V delle impostazioni.

### Come eseguire il backup/ripristino dei modelli con UE-V

Questi sono i componenti principali per il backup e il ripristino di UE-V:

-   Profili modello

-   Posizione dei pacchetti di impostazioni nel modello di posizione di archiviazione delle impostazioni

-   Trigger di backup

-   Ripristino delle impostazioni

**Profili modello**

Un profilo modello UE-V viene definito quando il modello viene registrato nel dispositivo o dopo la registrazione tramite l'utilità di configurazione di PowerShell/WMI. I tipi di profilo includono:

-   Roaming (impostazione predefinita)

-   Backup

-   Backuponly

Tutti i modelli sono inclusi nel profilo roaming quando sono registrati, se non diversamente specificato. Questi modelli sincronizzano le impostazioni con tutti i dispositivi abilitati per l'UE-V con il modello corrispondente abilitato.

I modelli possono essere aggiunti al profilo di backup con PowerShell o WMI usando il cmdlet Set-UevTemplateProfile. Modelli nel profilo di backup eseguire il backup di queste impostazioni nella posizione di archiviazione delle impostazioni in una directory di nome dispositivo speciale. Le impostazioni specificate sono supportate in questa posizione.

I modelli designati in modo indesiderato includono le impostazioni specifiche del dispositivo che non devono essere sincronizzate, a meno che non vengano esplicitamente ripristinate. Queste impostazioni sono archiviate nella stessa posizione del pacchetto di impostazioni specifiche del dispositivo nella posizione di archiviazione delle impostazioni come impostazioni di backedup. Questi modelli hanno un identificatore speciale incorporato nel modello che specifica che deve essere incluso nel profilo.

**Posizione dei pacchetti di impostazioni nel modello di posizione di archiviazione delle impostazioni**

Le impostazioni del profilo mobile sono archiviate nel percorso di archiviazione delle impostazioni. I modelli assegnati al backup o al profilo backuponly archiviano le impostazioni nella posizione di archiviazione delle impostazioni in una directory di nome dispositivo speciale. Ogni dispositivo con modelli in questi profili ha il proprio nome di dispositivo. UE-V non pulisce queste directory.

**Trigger di backup**

Il backup viene attivato dagli stessi eventi che attivano una sincronizzazione UE-V.

**Ripristino delle impostazioni**

Il ripristino del dispositivo di un utente ripristina le impostazioni del modello attualmente registrato dalla cartella di backup di un altro dispositivo e tutte le impostazioni sincronizzate con il computer corrente. Le impostazioni vengono ripristinate in due modi:

-   **Ripristino automatico**

    Se il percorso di archiviazione delle impostazioni UE-V dell'utente, il dominio e il nome del computer corrispondono all'utente corrente, tutte le impostazioni per l'utente vengono sincronizzate, con solo le impostazioni più recenti applicate. Se un utente accede a un nuovo dispositivo per la prima volta e questi criteri vengono soddisfatti, i dati delle impostazioni vengono applicati a tale dispositivo.

    **Nota**  
    L'accessibilità e le impostazioni desktop di Windows richiedono che l'utente riacceda a Windows per l'applicazione.



-   **Ripristino manuale**

    Se vuoi aiutare gli utenti a ripristinare un dispositivo durante l'aggiornamento, puoi scegliere di usare il cmdlet Restore-UevBackup. Questo comando fa sì che le impostazioni dell'utente vengano scaricate dalla posizione di archiviazione delle impostazioni.

## Ripristinare lo stato originale dell'applicazione e delle impostazioni di Windows


I comandi WMI e Windows PowerShell consentono di ripristinare le impostazioni dell'applicazione e di Windows nei valori delle impostazioni presenti nel computer la prima volta che l'applicazione è stata avviata dopo l'installazione dell'agente UE-V. Questa azione di ripristino viene eseguita in base alle impostazioni per applicazione o Windows. Le impostazioni vengono ripristinate la volta successiva che l'applicazione viene eseguita o le impostazioni vengono ripristinate quando l'utente accede al sistema operativo.

**Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con Windows PowerShell per UE-V 2. x**

1.  Aprire la finestra di Windows PowerShell.

2.  Immettere il cmdlet di Windows PowerShell seguente per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet di Windows PowerShell</strong></th>
    <th align="left"><strong>Descrizione</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows.</p></td>
    </tr>
    </tbody>
    </table>



**Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con WMI**

1.  Aprire una finestra di Windows PowerShell.

2.  Immettere il comando WMI seguente per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando WMI</strong></th>
    <th align="left"><strong>Descrizione</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## Argomenti correlati


[Amministrazione di UE-V 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









