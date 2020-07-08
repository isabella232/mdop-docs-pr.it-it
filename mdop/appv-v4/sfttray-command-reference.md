---
title: Riferimento ai comandi SFTTRAY
description: Riferimento ai comandi SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815355"
---
# Riferimento ai comandi SFTTRAY


L'applicazione Microsoft Application Virtualization (App-V) Client Tray, sfttray.exe, è l'elemento principale dell'interfaccia utente del client App-V con cui gli utenti interagiranno durante l'uso normale. Questo programma controlla lo streaming e l'avvio di tutte le applicazioni virtuali e si accede facendo clic con il pulsante destro del mouse sull'icona visualizzata nell'area di notifica per visualizzare il menu delle funzioni client. Il menu consente all'utente di caricare le applicazioni, avviare un aggiornamento della pubblicazione, annullare una richiesta o cambiare il client in modalità offline. L'utente può anche chiudere l'applicazione Tray Application Virtualization Client e tutte le applicazioni attive facendo clic su **Esci**.

Per impostazione predefinita, l'icona viene visualizzata ogni volta che si avvia un'applicazione virtuale, anche se è possibile controllare questo comportamento usando i comandi di SFTTRAY. L'applicazione Application Virtualization Client Tray Visualizza anche una barra di stato per ogni applicazione avviata, nonché i messaggi di stato sulle applicazioni attive. Facendo clic sulla barra di stato viene visualizzato un messaggio che consente di annullare il caricamento o l'avvio di un'applicazione.

## Comandi di SFTTRAY


L'elenco dei comandi e delle opzioni della riga di comando può essere visualizzato eseguendo il comando seguente da una finestra di comando.

**Nota**  
Esiste una sola istanza del client di virtualizzazione delle applicazioni per ogni contesto utente, quindi se si avvia un nuovo comando SFTTRAY, verrà passato al programma già in uso.



`Sfttray.exe /?`

### Utilizzo dei comandi

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### Opzioni della riga di comando

Le opzioni della riga di comando di SFTTRAY sono descritte nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Opzione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/HIDE</p></td>
<td align="left"><p>Nasconde l'icona di SFTTRAY nell'area di notifica di Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOW</p></td>
<td align="left"><p>Visualizza l'icona di SFTTRAY nell'area di notifica di Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QUIET</p></td>
<td align="left"><p>Supporta l'utilizzo non presidiato impedendo la visualizzazione di finestre di messaggio che richiedono la conferma dell'utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; alternativo-exe&gt;</p></td>
<td align="left"><p>Usato con/LAUNCH per specificare che è necessario avviare un programma eseguibile nell'ambiente virtuale quando un'applicazione virtuale viene avviata al posto del file di destinazione specificato nell'OSD.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Ad esempio, USA "SFTTRAY.EXE/EXE REGEDIT.EXE/LAUNCH &lt; app &gt; " per consentire di esaminare il registro di sistema dell'ambiente virtuale in cui è in corso l'applicazione.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;App/Launch &gt; [ &lt; argomenti &gt; ]</p></td>
<td align="left"><p>Avvia un'applicazione virtuale. Specificare il nome e la versione di un'applicazione o il percorso di un file OSD. Facoltativamente, gli argomenti della riga di comando possono essere passati all'applicazione virtuale.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Usa il comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" per ottenere un elenco dei nomi e delle versioni delle applicazioni virtuali disponibili.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/LOAD</p></td>
<td align="left"><p>Carica o importa un'applicazione virtuale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>Carica tutte le applicazioni nella cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>Avvia un aggiornamento della pubblicazione per tutte le applicazioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ID univoco di/LAUNCHRESULT&gt;</p></td>
<td align="left"><p>Restituisce il codice del risultato dell'avvio al processo che avvia sfttray.exe usando un evento globale e un file mappato alla memoria basato sul nome radice specificato per l'ID univoco. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTFILE &lt; SFT&gt;</p></td>
<td align="left"><p>Opzione facoltativa usata con/LOAD per specificare il percorso del file SFT dell'applicazione. Se specificato, l'applicazione viene importata piuttosto che caricata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/EXIT</p></td>
<td align="left"><p>Chiude il programma SFTTRAY e tutte le applicazioni virtuali attive e rimuove l'icona dall'area di notifica di Windows.</p></td>
</tr>
</tbody>
</table>



**Nota**  
¹ il parametro della riga di comando */LAUNCHRESULT* fornisce un mezzo per il processo che avvia sfttray.exe per specificare il nome radice per un evento globale e un file mappato alla memoria usato per restituire il codice del risultato di avvio al processo. Il nome dell'identificatore univoco dovrebbe iniziare con "SFT-" per evitare che il nome dell'evento venga virtualizzato quando il processo di avvio viene richiamato all'interno di un ambiente virtuale. L'area di mapping della memoria sarà di 64 bit in dimensioni.

Per usare questo parametro, il processo di avvio crea un evento con il nome " &lt; ID univoco &gt; -risultato \ _event", un file mappato in memoria con il nome " &lt; ID univoco &gt; -risultato \ _value" e, facoltativamente, un evento con il nome " &lt; id univoco &gt; -Shutdown \ _event" e quindi il processo di avvio viene avviato sfttray.exe e attende l'evento per essere segnalato. Dopo che l'evento " &lt; ID univoco &gt; -risultato \ _event" viene segnalato, il processo di avvio recupera il codice restituito a 64 bit dall'area mappata alla memoria.

Se l'evento facoltativo " &lt; ID univoco &gt; -shutdown \ _event" esiste quando l'applicazione virtuale viene chiusa, sfttray.exe si apre e segnala l'evento. Il processo di avvio attende questo evento di arresto se deve determinare quando l'applicazione virtuale viene chiusa.











