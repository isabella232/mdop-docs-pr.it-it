---
title: Messaggi del registro eventi MED-V
description: Messaggi del registro eventi MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823076"
---
# Messaggi del registro eventi MED-V


I file di log per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 offrono informazioni dettagliate su come distribuire e gestire MED-V nell'organizzazione e consentire la verifica della funzionalità o la risoluzione dei problemi.

## ID evento


Di seguito è riportato un elenco di ID evento MED-V per risolvere i problemi che possono verificarsi durante la distribuzione o la gestione di MED-V.

### FTS

Mostra gli ID evento per la configurazione iniziale.

### ID evento 3066

Avviare l'operazione macchina virtuale non riuscita.

<a href="" id="description"></a>**Descrizione**  
Esiste un potenziale problema con il disco rigido virtuale (VHD) usato per creare un'area di lavoro MED-V.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che possa essere avviata.

### ID evento 3071

La preparazione della macchina virtuale non è riuscita.

<a href="" id="description"></a>**Descrizione**  
Si è verificato un problema con la configurazione per la prima volta che potrebbe essere stata causata da molti problemi diversi. Questi includono problemi di connettività di rete.

<a href="" id="solution"></a>**Soluzione**  
Riavviare l'agente host MED-V per eseguire nuovamente la configurazione per la prima volta.

### ID evento 3078

La preparazione della macchina virtuale non è riuscita.

<a href="" id="description"></a>**Descrizione**  
Un problema potenziale esiste con il VHD usato per creare un'area di lavoro MED-V.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che possa essere avviata.

### ID evento 3079

Riprovare la preparazione della macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
MED-V sta provando a preparare la macchina virtuale.

<a href="" id="solution"></a>**Soluzione**  
Non è richiesta alcuna azione. Consentire la configurazione del primo tempo.

### ID evento 3080

Il client è stato interrotto durante la preparazione della macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
MED-V si arresta in modo imprevisto quando tenta di preparare la macchina virtuale.

<a href="" id="solution"></a>**Soluzione**  
Avviare l'agente host MED-V e consentire il completamento della configurazione per la prima volta

### ID evento 3084

La macchina virtuale non è valida. È necessario eseguire di nuovo la configurazione per la prima volta.

<a href="" id="description"></a>**Descrizione**  
L'agente host MED-V ha rilevato un problema con la macchina virtuale.

<a href="" id="solution"></a>**Soluzione**  
Non è richiesta alcuna azione. Consentire la configurazione del primo tempo.

### ID evento 3099

Chiamata per avviare la macchina virtuale non riuscita.

<a href="" id="description"></a>**Descrizione**  
Esiste un potenziale problema con il VHD in uso per creare un'area di lavoro MED-V.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che sia possibile aprirla.

### Gestione VM

### ID evento 4022

Errore irreversibile VMManagerException durante l'esecuzione del comando su VM.

<a href="" id="description"></a>**Descrizione**  
L'utente finale ha provato a uscire da MED-V disconnettendosi o chiudendo l'host MED-V e l'impostazione di configurazione di VMTaskTimeout è stata superata.

<a href="" id="solution"></a>**Soluzione**  
Riavviare MED-V.

### ID evento 4028

Operazione VM scaduta.

<a href="" id="description"></a>**Descrizione**  
L'utente finale ha provato a uscire da MED-V disconnettendosi o chiudendo l'host e l'impostazione di configurazione VMTaskTimeout è stata superata.

<a href="" id="solution"></a>**Soluzione**  
Riavviare MED-V.

### ID evento 4038

Vmsal ha pubblicato un messaggio di errore per l'utente.

<a href="" id="description"></a>**Descrizione**  
Viene visualizzato un messaggio di errore per l'utente finale che indica che MED-V non ha potuto avviare l'applicazione virtuale.

<a href="" id="solution"></a>**Soluzione**  
Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC console e provare ad avviare l'applicazione a schermo intero.

### ID evento 4040

Riciclo delle aggiunte perché TerminalServices non viene inizializzato nel guest.

<a href="" id="description"></a>**Descrizione**  
MED-V ha riavviato la macchina virtuale perché i Servizi Desktop remoto non sono stati inizializzati nella macchina virtuale.

<a href="" id="solution"></a>**Soluzione**  
Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC Console.

### ID evento 4042

Non è riuscito a riciclare le aggiunte nell'ospite.

<a href="" id="description"></a>**Descrizione**  
MED-V non è riuscito a riciclare le aggiunte della macchina virtuale nella macchina virtuale.

<a href="" id="solution"></a>**Soluzione**  
Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC Console.

### ID evento 4043

Non è possibile reimpostare la password scaduta nella macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
L'utente finale non ha reimpostato la password nella macchina virtuale prima di essere scaduta. Di conseguenza, l'utente potrebbe non essere in grado di accedere alle risorse di rete o di salvare il lavoro.

<a href="" id="solution"></a>**Soluzione**  
Arrestare l'ospite MED-V e riavviarlo.

### Reindirizzamento URL

### ID evento 5005

Impossibile ottenere il nome VM dalla configurazione; non è possibile avviare il browser Guest.

<a href="" id="description"></a>**Descrizione**  
Il reindirizzamento degli URL non ha potuto ottenere il nome dell'area di lavoro MED-V dalla configurazione. Di conseguenza, non può informare Windows Virtual PC per aprire l'URL reindirizzato nel browser dell'area di lavoro MED-V.

<a href="" id="solution"></a>**Soluzione**  
Assicurarsi che il nome dell'area di lavoro MED-V sia impostato e che corrisponda a un nome di macchina virtuale nella &lt; *user* &gt; directory dei computer \\Virtual utente di C:\\Users\\. Il nome dell'area di lavoro MED-V si trova in HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Ad esempio, se l'utente è "Matt" e il nome dell'area di lavoro è "mattsworkspace", il valore di HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve essere "mattsworkspace" e dovrebbe essere presente un file denominato C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### ID evento 5006

Impossibile creare il server pipe.

<a href="" id="description"></a>**Descrizione**  
Il servizio di reindirizzamento degli URL non può creare il server pipe per comunicare con Internet Explorer.

<a href="" id="solution"></a>**Soluzione**  
Controllare i registri degli eventi di sistema per tentare di creare un file o una risorsa il cui percorso inizia in modo simile al seguente: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" e termina con il nome utente e il nome di dominio dell'utente. Se non è presente nel log eventi, riavviare il computer.

### ConfigMgr (ospite)

### ID evento 7001

I dati di configurazione della rete host non sono formattati correttamente.

<a href="" id="description"></a>**Descrizione**  
La configurazione di rete ricevuta dall'host è una stringa XML formattata in modo non corretto o le informazioni di rete restituite dall'host non possono essere scritte in un documento XML.

<a href="" id="solution"></a>**Soluzione**  
Riavviare il computer host e la macchina virtuale.

### ID evento 7005

È stata rilevata una modifica alla configurazione della rete host, ma non è stato possibile applicarla perché i dati di configurazione della rete host non sono stati formattati correttamente.

<a href="" id="description"></a>**Descrizione**  
Una modifica alla configurazione della rete host è stata comunicata alla macchina virtuale, ma non è stato possibile elaborarla nella macchina virtuale a causa di un errore. Questo errore potrebbe essere causato da dati formattati in modo non corretto o dall'impossibilità di impostare le informazioni nell'istanza di CCMNetworkAdapter di Strumentazione gestione Windows (WMI).

<a href="" id="solution"></a>**Soluzione**  
Riavviare l'host e la macchina virtuale.

### ConfigMgr (host)

### ID evento 8006

Impossibile trovare la macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
Windows Virtual PC 7 non è in grado di individuare la macchina virtuale. La macchina virtuale potrebbe essere stata eliminata, spostata, rimossa o l'accesso è stato negato.

<a href="" id="solution"></a>**Soluzione**  
Reinstallare la macchina virtuale.

### ID evento 8008

Non è stato possibile recuperare le informazioni di configurazione della rete della workstation.

<a href="" id="description"></a>**Descrizione**  
Non è stato possibile raccogliere informazioni di configurazione della rete dall'host MED-V, probabilmente a causa di un errore di chiamata di sistema in .NET Framework. Questo errore può verificarsi anche se le informazioni di rete restituite dall'host MED-V non possono essere scritte in un documento XML.

<a href="" id="solution"></a>**Soluzione**  
Riavviare la workstation host.

### ID evento 8010

I dati di configurazione della rete non possono essere impostati nella macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
Non è stato possibile comunicare l'indirizzo NAT (MED-V hostnetwork Address Translation) alla macchina virtuale, probabilmente perché la macchina virtuale è in uno stato difettoso o le aggiunte di Windows Virtual PC non sono state installate o abilitate.

<a href="" id="solution"></a>**Soluzione**  
Arrestare e riavviare la macchina virtuale. Inoltre, potrebbe essere necessario reinstallare la macchina virtuale.

### ID evento 8011

I dati di configurazione della rete non possono essere reimpostati nella macchina virtuale.

<a href="" id="description"></a>**Descrizione**  
La configurazione di hostnetwork MED-V (BRIDGEd) non può essere comunicata alla macchina virtuale, probabilmente perché la macchina virtuale è in uno stato difettoso o le aggiunte di Windows Virtual PC non sono state installate o abilitate.

<a href="" id="solution"></a>**Soluzione**  
Arrestare e riavviare la macchina virtuale. Inoltre, potrebbe essere necessario reinstallare la macchina virtuale.

### Reindirizzamento della stampante

### ID evento 9001

Errore di autorizzazione file.

<a href="" id="description"></a>**Descrizione**  
L'utente finale non è autorizzato ad accedere alla cartella richiesta per aprire o creare il file della stampante MED-V per la lettura.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni per la lettura e la scrittura. Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura. E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.

### ID evento 9002

Errore di autorizzazione file.

<a href="" id="description"></a>**Descrizione**  
L'utente finale non è autorizzato ad accedere alla cartella richiesta per aprire o creare il file della stampante MED-V per la scrittura.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni di lettura e scrittura. Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura. E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.

### ID evento 9004

Impossibile creare il percorso per l'archiviazione dei file della stampante MEDV.

<a href="" id="description"></a>**Descrizione**  
Il servizio di reindirizzamento della stampante non può accedere ai file o creare directory necessarie per archiviare le informazioni sulla stampante.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni per la lettura e la scrittura. Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura. E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.

### ID evento 9005

Impossibile ottenere il nome VM dalla configurazione; non è possibile avviare il programma di installazione Guest. Non è possibile aggiornare MED-V: non è stato rilevato alcun network host.

<a href="" id="description"></a>**Descrizione**  
Il servizio di reindirizzamento della stampante non è stato in grado di ottenere il nome dell'area di lavoro MED-V dalla configurazione MED-V e non può informare Windows Virtual PC di avviare il programma di installazione nell'guest MED-V.

<a href="" id="solution"></a>**Soluzione**  
Assicurarsi che il nome dell'area di lavoro MED-V sia impostato e che corrisponda a un nome di macchina virtuale nella &lt; *user* &gt; directory dei computer \\Virtual utente di C:\\Users\\. Il nome dell'area di lavoro MED-V si trova in HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Ad esempio, se l'utente è "Matt" e il nome dell'area di lavoro è "mattsworkspace", il valore di HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve essere "mattsworkspace" e dovrebbe essere presente un file denominato C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### Pubblicazione di applicazioni

### ID evento 10015

Si è verificato un errore di file System durante il processo di riconciliazione. Il processo di riconciliazione non elaborerà il &lt; *nome* del file &gt; , ma continuerà a elaborare qualsiasi altra modifica.

<a href="" id="description"></a>**Descrizione**  
Si è verificato un errore di I/O di accesso non autorizzato quando è stato creato o eliminato un collegamento.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile accedere al percorso del file e che l'utente disponga delle autorizzazioni per creare o eliminare il file specificato.

### ID evento 10021

&lt; *Errore di errore \ _information* &gt; per l'operazione operazione file &lt; *\ _name* &gt; il nome del file &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrizione**  
Si è verificato un errore di I/O di accesso non autorizzato quando è stato creato o eliminato un collegamento.

<a href="" id="solution"></a>**Soluzione**  
Verificare che sia possibile accedere al percorso del file e che l'utente disponga delle autorizzazioni per creare o eliminare il file specificato.

### Patch Guest

### ID evento 11001

Messaggio di utilizzo delle attività di risveglio Guest.

<a href="" id="description"></a>**Descrizione**  
MedvHost.exe con l'opzione/GuestWakeup è stata eseguita in modo non corretto oppure il comando è formattato in modo errato.

<a href="" id="solution"></a>**Soluzione**  
Verificare che il comando venga eseguito con il formato seguente:

Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *area di lavoro \ _name* &gt; " dove

&lt;*durata \ _in \ _minutes* &gt; è il numero di minuti che la macchina virtuale deve rimanere svegli (il valore predefinito è 240) e

&lt;*area di lavoro \ _name* &gt; è il nome della macchina virtuale che deve essere riattivata.

### ID evento 11002

Non è possibile aggiornare MED-V: non è stato rilevato alcun network host.

<a href="" id="description"></a>**Descrizione**  
Non è stato possibile completare la patch Guest perché non è stata rilevata una connessione di rete host.

<a href="" id="solution"></a>**Soluzione**  
Connettere l'host MED-V a una connessione di rete attiva prima di eseguire le patch Guest.

### ID evento 11003

Non è possibile aggiornare MED-V-host non in uso in un/C powerFailed per creare server pipe.

<a href="" id="description"></a>**Descrizione**  
L'aggiornamento delle patch Guest non può essere completato perché l'host sembra essere in funzione a batteria invece che da un cavo di alimentazione.

<a href="" id="solution"></a>**Soluzione**  
Connettere il computer host a un cavo di alimentazione prima di eseguire le patch Guest.

### Client UX

### ID evento 14003

Il messaggio di stato del vassoio seguente è stato troppo lungo e non è stato possibile visualizzarlo: &lt; *tray \ _status \ _message*&gt;

<a href="" id="description"></a>**Descrizione**  
In MED-V è stata creata una stringa non prevista troppo lunga per la descrizione comando vassoio o il messaggio Balloon. Di conseguenza, il messaggio visualizzato è stato troncato.

<a href="" id="solution"></a>**Soluzione**  
Si tratta di un errore raro che può verificarsi quando MED-V crea in modo casuale il testo della descrizione comando. Non esiste una soluzione.

### ID evento 14004

MED-V è stato interrotto a causa di un'eccezione non gestita.

<a href="" id="description"></a>**Descrizione**  
Un'eccezione non gestita ha causato l'arresto imprevisto di MED-V.

<a href="" id="solution"></a>**Soluzione**  
Riavviare MED-V.

### ID evento 14005

Il server ha tentato di creare mutex ma esiste già.

<a href="" id="description"></a>**Descrizione**  
Una seconda istanza di MedvHost.exe è bloccata in memoria.

<a href="" id="solution"></a>**Soluzione**  
Aprire TaskManager e terminare tutti i processi di MedvHost.exe.

### ID evento 14006

Errore durante la modifica o l'eliminazione del registro di valori del registro di sistema &lt; *_value* &gt; .

<a href="" id="description"></a>**Descrizione**  
MED-V non è in grado di modificare la voce specificata nel registro di sistema.

<a href="" id="solution"></a>**Soluzione**  
Assicurarsi di installare o disinstallare MED-V con credenziali amministrative.

### ID evento 14007

Il file specificato ( &lt; *nomefile* &gt; ) non è valido.

<a href="" id="description"></a>**Descrizione**  
Durante l'installazione o la disinstallazione, un file temporaneo danneggiato è stato passato all'host MED-V.

<a href="" id="solution"></a>**Soluzione**  
Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.

### ID evento 14008

File non trovato: &lt; *nomefile* &gt; .

<a href="" id="description"></a>**Descrizione**  
Durante l'installazione o la disinstallazione, non è stato trovato un percorso di un file temporaneo obbligatorio.

<a href="" id="solution"></a>**Soluzione**  
Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.

### ID evento 14009

Non è possibile leggere il nome del file del parametro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrizione**  
Durante il processo di installazione o disinstallazione, MED-V non è in grado di leggere un file temporaneo.

<a href="" id="solution"></a>**Soluzione**  
Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V. Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.

### ID evento 14010

Errore di deserializzazione del file di parametro &lt; *nomefile* &gt; .

<a href="" id="description"></a>**Descrizione**  
Durante il processo di installazione o disinstallazione, MED-V ha rilevato un file temporaneo danneggiato.

<a href="" id="solution"></a>**Soluzione**  
Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V. Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.

### ID evento 14011

Errore imprevisto che deserializza il nome del file del parametro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrizione**  
Durante il processo di installazione o disinstallazione, MED-V ha rilevato un file temporaneo danneggiato.

<a href="" id="solution"></a>**Soluzione**  
Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V. Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.

### ID evento 14012

Errore imprevisto quando i diritti delle impostazioni nella cartella cartella &lt; *\ _name* &gt; per il &lt; *nome*utente &gt; .

<a href="" id="description"></a>**Descrizione**  
Si verifica un errore quando MED-V non è in grado di impostare diritti e autorizzazioni per determinate cartelle durante l'installazione.

<a href="" id="solution"></a>**Soluzione**  
Verificare i diritti di amministratore per le cartelle seguenti:

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### ID evento 14013

Errore imprevisto durante la creazione di file di blocco.

<a href="" id="description"></a>**Descrizione**  
Si verifica un errore quando MED-V non è in grado di creare un file nella cartella @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante l'installazione.

<a href="" id="solution"></a>**Soluzione**  
Controlla i diritti di amministratore per la cartella MedvLock.

## Argomenti correlati


[Risoluzione dei problemi di MED-V](troubleshooting-med-vmedv2.md)

 

 





