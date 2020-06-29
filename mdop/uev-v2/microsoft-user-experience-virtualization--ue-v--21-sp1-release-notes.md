---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1
author: dansimp
ms.assetid: 561988c4-cc5c-4e15-970b-16e942c8f2ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/30/2017
ms.openlocfilehash: 974914421c61c829b5a32e336bddf8ea1addf514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825535"
---
# Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1


Per cercare le note sulla versione di Microsoft User Experience Virtualization 2,1 SP1, premere CTRL + F.

Prima di installare UE-V, leggere accuratamente queste note sulla versione. Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto. Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Commenti e suggerimenti


Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti. Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemi noti di UE-V


Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente 2,1 SP1.

### I modelli di posizione delle impostazioni UE-V per Skype causano un arresto anomalo di Skype

Quando un utente genera un modello di posizione di impostazioni valido per l'applicazione desktop Skype, lo registra e quindi avvia l'applicazione desktop Skype, Skype si arresta in modo anomalo. Nel registro eventi applicazione viene registrato un ACCESS \ _VIOLATION.

SOLUZIONE alternativa: rimuovere o annullare la registrazione del modello Skype per consentire l'utilizzo di Skype.

### Gli script esistenti per le installazioni silent di UE-V potrebbero non riuscire

Due modifiche apportate al programma di installazione di UE-V possono causare errori durante l'installazione di UE-V 2,1 SP1, che ha funzionato per le versioni precedenti di UE-V. Il primo è un nuovo requisito che gli utenti devono accettare le condizioni di licenza e accettare o rifiutare la partecipazione al programma Customer Experience Improvement Program (analisi utilizzo software), anche durante un'installazione invisibile all'utente. L'uso del parametro/q non è più sufficiente per indicare l'accettazione delle condizioni di licenza e dell'accordo per partecipare a analisi utilizzo software.

In secondo luogo, il programma di installazione forza il riavvio del computer dopo l'installazione dell'agente UE-V. Ciò può causare un errore di installazione dello script se non si prevede che il riavvio (ad esempio, installa l'agente UE-V prima di tutto e quindi installa immediatamente il generatore).

SOLUZIONE alternativa: il programma di installazione di UE-V (con estensione msi) include due nuovi parametri della riga di comando che supportano le installazioni silent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>/ACCEPTLICENSETERMS = true</strong></p></td>
<td align="left"><p>Imposta questo parametro su <strong> true </strong> per installare la versione UE-V in modo invisibile all'utente. L'aggiunta di questo parametro implica che l'utente accetti le condizioni di licenza UE-V trovate (per impostazione predefinita) qui:%programmi%\Microsoft User Experience Virtualization\Agent</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/NORESTART</strong></p></td>
<td align="left"><p>Questo parametro impedisce il riavvio obbligatorio dopo l'installazione dell'agente UE-V. Un codice restituito di 3010 indica che è necessario un riavvio prima di usare UE-V.</p></td>
</tr>
</tbody>
</table>

 

### Le impostazioni del registro di sistema non vengono sincronizzate tra App-V e le applicazioni native nello stesso computer

Quando un computer ha un'applicazione installata sia tramite Application Virtualization (App-V) che localmente con un file di Windows Installer (con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.

SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.

### Risultati imprevedibili con Office 2010 e Office 2013 installati

Quando un utente ha installato sia Office 2010 che Office 2013, tutte le impostazioni comuni tra le due versioni di Office sono in roaming da UE-V. In questo modo, le dimensioni del pacchetto di Office 2010 possono essere abbastanza grandi o causare conflitti imprevedibili con 2013, in particolare se si usa Office 365.

SOLUZIONE alternativa: installare solo una versione di Office o limitare le impostazioni sincronizzate da UE-V.

### La disinstallazione e la reinstallazione dell'app di Windows 8 ripristinano le impostazioni sullo stato iniziale

Durante l'uso della sincronizzazione delle impostazioni di UE-V per un'app di Windows 8, se l'utente disinstalla l'app e quindi reinstalla l'app, le impostazioni dell'app ripristinano i valori predefiniti.Questo avviene perché la disinstallazione rimuove la copia locale (memorizzata nella cache) delle impostazioni dell'app, ma non rimuove il pacchetto di impostazioni locali UE-V.Quando l'app viene reinstallata e avviata, UE-V raccoglie le impostazioni dell'app che sono state reimpostate per impostazione predefinita e quindi carica le impostazioni predefinite nella posizione di archiviazione centrale.Altri computer che eseguono l'app scaricano le impostazioni predefinite.Questo comportamento è identico al comportamento delle applicazioni desktop.

SOLUZIONE alternativa: None.

### UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office

È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit. Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica. Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit. UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.

SOLUZIONE alternativa: None

### <a href="" id="msi-s-are-not-localized"></a>I file MSI non sono localizzati

UE-V include un programma di configurazione localizzato sia per l'agente UE-V che per il generatore di UE-V. Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese. Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.

SOLUZIONE alternativa: None

### Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming

Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.

SOLUZIONE alternativa: le favicon verranno visualizzate con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.

### I percorsi delle impostazioni dei file sono archiviati nel registro di sistema

Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema. I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.

SOLUZIONE alternativa: usare il reindirizzamento delle cartelle o altre tecnologie per assicurarsi che tutti i file a cui si fa riferimento come percorsi di impostazioni file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni si aggirano.

### I percorsi di archiviazione delle impostazioni lunghe possono causare un errore

Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni. I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione. UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni. Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello) +. pkgx. Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.

SOLUZIONE alternativa: None.

### Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo

Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici delle impostazioni locali (ad esempio, lingua e opzioni internazionali) verranno spostati solo tra le versioni del sistema operativo di Windows. Ad esempio, i caratteri di valuta non verranno spostati tra Windows 7 e Windows 8.

SOLUZIONE alternativa: None

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>L'agente UE-V 1 genera errori durante l'uso di modelli UE-V 2

Se un modello di posizione delle impostazioni dell'UE-V 2 viene distribuito in un computer installato con un agente UE-V 1, alcune impostazioni non riescono a eseguire la sincronizzazione tra i computer e l'agente segnala gli errori nel log eventi.

SOLUZIONE alternativa: quando si esegue la migrazione da UE-V 1 a UE-V 2 ed è probabile che i computer che eseguono la versione precedente dell'agente creino un catalogo UE-V 2. x separato per supportare l'agente e i modelli di UE-V 2. x.

### Ritardo di disconnessione UE-V

Occasionalmente durante la disconnessione, UE-V richiede molto tempo per la sincronizzazione delle impostazioni. In genere, questo problema è dovuto a una rete a latenza elevata o a un uso non corretto del file System Distrubuted (DFS).
Per il supporto DFS, vedere [l'istruzione del supporto Microsoft intorno ai dati del profilo utente replicati](https://support.microsoft.com/kb/2533009) per ulteriori dettagli.

SOLUZIONE alternativa: a partire da HF03, è stata introdotta una nuova chiave del registro di sistema che indica che il ritardo di disconnessione massimo può essere specificato \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval

Per ulteriori informazioni [, vedere Impostazioni del registro di sistema UE-V.](https://support.microsoft.com/kb/2770042)

## Aggiornamenti rapidi e articoli della Knowledge base per UE-V 2,1 SP1


Questa sezione contiene gli aggiornamenti rapidi e gli articoli della KB per la versione UE-V 2,1 SP1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Articolo KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>3018608</p></td>
<td align="left"><p>UE-V 2,1-TemplateConsole.exe si arresta in modo anomalo quando mancano le classi WMI di UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)">support.microsoft.com/kb/3018608/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-V: compatibilità con l'esperienza utente per la virtualizzazione (UE-V) con i profili utente</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>Impostazioni del registro di sistema UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Impostazioni UE-V replicate da Internet Explorer</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Come ripristinare un'installazione di UE-V danneggiata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850989</p></td>
<td align="left"><p>La migrazione dei profili MAPI con Microsoft UE-V non è supportata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V aggira le cartelle vuote e le chiavi del registro di sistema</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Come abilitare la registrazione di debug in Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V non aggiorna il tema nelle sessioni RDS o VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Come usare la virtualizzazione dell'esperienza utente Microsoft con le applicazioni App-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Versioni di file correnti per la virtualizzazione dell'esperienza utente Microsoft</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Informazioni sulla virtualizzazione dell'esperienza utente e disponibilità elevata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 






 

 





