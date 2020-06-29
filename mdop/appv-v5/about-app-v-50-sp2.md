---
title: Informazioni su App-V 5.0 SP2
description: Informazioni su App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814986"
---
# Informazioni su App-V 5.0 SP2


App-V 5.0 SP2 offre una piattaforma integrata migliorata, una virtualizzazione più flessibile e una gestione efficace per le applicazioni virtualizzate. Per altre informazioni, Vedi [Panoramica di App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .

## Modifiche apportate alla funzionalità standard App-V 5.0 SP2


Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per App-V 5.0 SP2.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Supporto per Windows Server 2012 R2 e Windows 8,1

App-V 5,0 include il supporto per Windows Server 2012 R2 e Windows 8,1

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> App-V 5.0 SP2 ora supporta il reindirizzamento delle cartelle per la directory di roaming AppData dell'utente

App-V 5.0 SP2 supporta il roaming AppData (% AppData%) Reindirizzamento delle cartelle. Per altre informazioni, vedi la [pianificazione per usare il reindirizzamento delle cartelle con App-V](planning-to-use-folder-redirection-with-app-v.md).

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>Miglioramenti di aggiornamento del pacchetto e attività in sospeso

In App-V 5.0 SP2 non viene più richiesto di chiudere un'applicazione virtuale in esecuzione quando viene pubblicata una versione più recente del pacchetto o del gruppo di connessioni. Se un pacchetto o un gruppo di connessioni è in uso quando si prova a eseguire un'attività correlata, viene visualizzato un messaggio per indicare che l'oggetto è in uso e che l'operazione verrà tentata in un secondo momento.

Le attività inserite in uno stato in sospeso verranno eseguite in base alle regole seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di attività</th>
<th align="left">Regola applicabile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</p></td>
</tr>
</tbody>
</table>

 

Quando un'attività viene inserita in uno stato in sospeso, il client App-V genera anche una chiave del registro di sistema per l'attività in sospeso, come indicato di seguito:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività basata su utenti o globale</th>
<th align="left">Dove viene generata la chiave del registro di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basate sull'utente</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basate su base globale</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

### Virtualizzazione di Microsoft Office 2013 e Microsoft Office 2010 tramite App-V 5,0

Usare il collegamento seguente per altre informazioni sugli scenari di Microsoft Office supportati da App-V 5,0.

[Virtualizzazione di Microsoft Office 2013 per Application Virtualization (App-V) 5.0](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**Nota**  Questo documento si basa sulla creazione di un pacchetto di Microsoft Office 2013 App-V 5,0. Fornisce tuttavia anche informazioni sugli scenari per Microsoft Office 2010 con App-V 5,0.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> Applicazione per l'interfaccia utente di gestione client di App-V 5,0

Nelle versioni precedenti di App-V 5,0 l'interfaccia utente di gestione client è stata fornita con l'installazione del client App-V 5,0. Con App-V 5.0 SP2 questo non è più il caso. Gli amministratori hanno ora la possibilità di distribuire l'interfaccia utente client App-V 5,0 come applicazione virtuale (usando tutte le configurazioni di distribuzione di App-V supportate) o come applicazione installata.

Per altre informazioni, Vedi [applicazione di interfaccia utente client di Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .

### Assemblaggio e distribuzione automatica di assembly affiancati (SxS)

App-V 5.0 SP2 ora rileva automaticamente gli assembly side-by-Side (SxS) e la distribuzione nel computer che gestisce il client App-V 5.0 SP2. Un assembly SxS consiste principalmente di dipendenze della fase di esecuzione di VC + + o MSXML. Nelle versioni precedenti di App-V le applicazioni virtuali che avevano dipendenze da Runtime di VC richiedevano che queste dipendenze fossero localmente nel computer che esegue il client App-V 5.0 SP2.

Ora sono supportate le funzionalità seguenti:

-   L'App-V 5,0 sequencer acquisisce automaticamente l'assembly SxS nel pacchetto, indipendentemente dal fatto che la fase di esecuzione di VC sia già stata installata nel computer in cui è in esecuzione Sequencer.

-   Il client App-V 5,0 installa automaticamente l'assembly SxS richiesto nel computer in cui è in esecuzione il client, come richiesto in fase di pubblicazione.

-   L'App-V 5,0 sequencer riporta la dipendenza di runtime VC usando il meccanismo di creazione di report Sequencer.

-   L'App-V 5,0 Sequencer consente ora di escludere la dipendenza di runtime VC in caso di dipendenza già disponibile nel computer che esegue il sequencer.

### Miglioramenti all'aggiornamento della pubblicazione

App-V 5,0 supporta diverse funzionalità aggiunte per migliorare l'esperienza complessiva di aggiornamento di un set di applicazioni per un utente specifico.

Nell'elenco seguente vengono visualizzati i miglioramenti dell'aggiornamento della pubblicazione:

L'elenco seguente contiene altre informazioni su come abilitare i nuovi miglioramenti per l'aggiornamento della pubblicazione.

-   **EnablePublishingRefreshUI** -Abilita la barra di stato aggiornamento pubblicazione per il computer che gestisce il client App-V 5,0.

-   **HideUI** -nasconde la barra di stato dell'aggiornamento della pubblicazione durante una sincronizzazione manuale.

### Impostazione nuova configurazione client

La nuova impostazione di configurazione client seguente è disponibile con App-V 5,0 SP2:

**EnableDynamicVirtualization** -Abilita le estensioni della shell supportate, gli oggetti helper del browser e i controlli attivi X per essere virtualizzati ed eseguiti con le applicazioni virtuali.

Per altre informazioni, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings.md).

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> Estensioni della shell App-V 5,0

App-V 5,0 SP2 ora supporta le estensioni della shell.

Per altre informazioni, vedi la sezione **supporto dell'estensione della shell App-v 5.0 SP2** per la [creazione e la gestione di applicazioni virtualizzate app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).

## <a href="" id="---------app-v-5-0-documentation-updates"></a> Aggiornamenti della documentazione di App-V 5,0


App-V 5,0 SP2 fornisce la documentazione aggiornata per gli scenari seguenti:

-   [Migrazione da una versione precedente](migrating-from-a-previous-version-app-v-50.md)

-   [Informazioni su App-V 5.0](about-app-v-50.md)

-   [Informazioni sulla creazione di report su App-V 5,0](about-app-v-50-reporting.md) (sezione Domande frequenti)

## Come ottenere le tecnologie MDOP


App-V 5,0 fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .






## Argomenti correlati


[Note sulla versione di App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md)

 

 





