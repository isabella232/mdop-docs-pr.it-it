---
title: Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate
description: Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804882"
---
# Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate


È possibile eseguire un'applicazione installata localmente in un ambiente virtuale, insieme alle applicazioni virtualizzate tramite Microsoft Application Virtualization (App-V). Se si vuole eseguire questa operazione, è possibile:

-   Si vuole installare ed eseguire un'applicazione localmente nei computer client, ma si vuole virtualizzare ed eseguire plug-in specifici che funzionano con quell'applicazione locale.

-   Risoluzione dei problemi relativi a un pacchetto client App-V e si vuole aprire un'applicazione locale nell'ambiente virtuale App-V.

Usa uno dei metodi seguenti per aprire un'applicazione locale all'interno dell'ambiente virtuale App-V:

-   [Chiave del registro di sistema RunVirtual](#bkmk-runvirtual-regkey)

-   [Cmdlet di PowerShell Get-AppvClientPackage](#bkmk-get-appvclientpackage-posh)

-   [Opzione della riga di comando/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [Opzione hook della riga di comando/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Ogni metodo compie essenzialmente la stessa attività, ma alcuni metodi possono essere più adatti per alcune applicazioni rispetto ad altri, a seconda che l'applicazione virtualizzata sia già in esecuzione.

## <a href="" id="bkmk-runvirtual-regkey"></a>Chiave del registro di sistema RunVirtual


Per aggiungere un'applicazione installata localmente a un pacchetto o a un ambiente virtuale di un gruppo di connessioni, è possibile aggiungere una sottochiave alla chiave del registro di sistema `RunVirtual` nell'editor del registro di sistema, come descritto nelle sezioni seguenti.

Per gestire questa chiave del registro di sistema non è disponibile alcuna impostazione di criteri di gruppo, quindi è necessario usare System Center Configuration Manager o un altro sistema ESD (Electronic Software Distribution) oppure modificare manualmente il registro.

### <a href="" id="bkmk-"></a>Metodi supportati per la pubblicazione di pacchetti quando si usa RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione App-V</th>
<th align="left">Metodi di pubblicazione supportati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Pubblicato a livello globale o all'utente</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 tramite App-V 5,0 SP2</p></td>
<td align="left"><p>Pubblicato solo a livello globale</p></td>
</tr>
</tbody>
</table>

 

### Procedura per creare la sottochiave

1.  Usando le informazioni nella tabella seguente, creare una nuova chiave del registro di sistema usando il nome del file eseguibile, ad esempio **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Metodo di pubblicazione del pacchetto</th>
    <th align="left">Dove creare la chiave del registro di sistema</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Pubblicazione globale</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Esempio </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Pubblicato per l'utente</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Esempio </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Il gruppo di connessioni può contenere:</p>
    <ul>
    <li><p>Pacchetti pubblicati solo a livello globale o solo per l'utente</p></li>
    <li><p>Pacchetti pubblicati globalmente e all'utente</p></li>
    </ul></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE o HKEY_CURRENT_USER chiave, ma tutte le operazioni seguenti devono essere vere:</p>
    <ul>
    <li><p>Se si vogliono includere più pacchetti nell'ambiente virtuale, è necessario includerli in un gruppo di connessioni abilitato.</p></li>
    <li><p>Creare una sola sottochiave per uno dei pacchetti nel gruppo di connessioni. Se ad esempio è presente un pacchetto pubblicato globalmente e un altro pacchetto pubblicato per l'utente, è possibile creare una sottochiave per uno di questi pacchetti, ma non entrambe. Anche se crei una sottochiave per solo uno dei pacchetti, tutti i pacchetti nel gruppo connessione, oltre all'applicazione locale, saranno disponibili nell'ambiente virtuale.</p></li>
    <li><p>La chiave in cui si crea la sottochiave deve corrispondere al metodo di pubblicazione usato per il pacchetto.</p>
    <p>Ad esempio, se il pacchetto è stato pubblicato per l'utente, è necessario creare la sottochiave in <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Imposta il valore della sottochiave del nuovo registro di sistema su PackageId e VersionId del pacchetto, separando i valori con un carattere di sottolineatura.

    **Sintassi**: &lt; PackageID &gt; \ _ &lt; VersionId&gt;

    **Esempio**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    L'applicazione nell'esempio precedente produrrebbe un file di esportazione del registro di sistema (file con estensione reg) simile al seguente:

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Cmdlet di PowerShell Get-AppvClientPackage


Puoi usare il cmdlet **Start-AppVVirtualProcess** per recuperare il nome del pacchetto e quindi avviare un processo nell'ambiente virtuale del pacchetto specificato. Questo metodo consente di avviare qualsiasi comando nel contesto di un pacchetto di App-V, indipendentemente dal fatto che il pacchetto sia attualmente in esecuzione.

Usa la sintassi di esempio seguente e Sostituisci il nome del pacchetto per il ** &lt; pacchetto &gt; **:

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Se non si conosce il nome esatto del pacchetto, è possibile usare la riga di comando **Get-AppvClientPackage \ * executable\\** <em> , dove ** </em> eseguibile* è il nome dell'applicazione, ad esempio: Get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>Opzione della riga di comando/appvpid: &lt; PID&gt;


Puoi applicare l'opzione **/appvpid: &lt; PID &gt; ** a qualsiasi comando, che consente di eseguire il comando in un processo virtuale selezionato specificando il relativo ID processo (PID). L'uso di questo metodo avvia il nuovo eseguibile nello stesso ambiente App-V di un eseguibile già in uso.

Esempio: `cmd.exe /appvpid:8108`

Per trovare l'ID processo (PID) del processo App-V, eseguire il comando **tasklist.exe** da un prompt dei comandi con privilegi elevati.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>Opzione hook della riga di comando/appvve: &lt; GUID&gt;


Questa opzione consente di eseguire un comando locale nell'ambiente virtuale di un pacchetto di App-V. Diversamente dall'opzione **/appvid** , in cui l'ambiente virtuale deve essere già in funzione, questa opzione consente di avviare l'ambiente virtuale.

Sintassi `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Esempio: `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Per ottenere il GUID del pacchetto e il GUID della versione dell'applicazione, eseguire il cmdlet **Get-AppvClientPackage** . Concatenare l'opzione **/appvve** con la seguente:

-   I due punti

-   GUID del pacchetto del pacchetto desiderato

-   Un carattere di sottolineatura

-   ID versione del pacchetto desiderato

Se non si conosce il nome esatto del pacchetto, usare la riga di comando **Get-AppvClientPackage \ * executable\\** <em> , dove **eseguibile </em> * è il nome dell'applicazione, ad esempio Get-AppvClientPackage \ * Word \ *.

Questo metodo consente di avviare qualsiasi comando nel contesto di un pacchetto di App-V, indipendentemente dal fatto che il pacchetto sia attualmente in esecuzione.






## Argomenti correlati


[Documentazione tecnica per App-V 5.0](technical-reference-for-app-v-50.md)

 

 





