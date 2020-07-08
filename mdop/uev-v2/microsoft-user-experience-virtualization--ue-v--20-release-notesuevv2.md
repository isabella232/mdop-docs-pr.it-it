---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825285"
---
# Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0


Per cercare le note sulla versione di Microsoft User Experience Virtualization (UE-V) 2,0, premere CTRL + F.

Prima di installare UE-V, leggere accuratamente queste note sulla versione. Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto. Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Commenti e suggerimenti


Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti. Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemi noti di UE-V


Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente.

### Le impostazioni del registro di sistema non vengono sincronizzate tra App-V e le applicazioni native nello stesso computer

Quando un computer dispone di un'applicazione installata sia tramite Application Virtualization (App-V) che in locale con un file di Windows Installer (con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.

**Soluzione alternativa:** Per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a>Le impostazioni non vengono sincronizzate quando la condivisione di rete è esterna al dominio dell'utente

Quando Windows® 8 tenta la sincronizzazione delle impostazioni del sistema operativo, la sincronizzazione non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretto**. Questo errore può indicare che la condivisione di rete si trova all'esterno del dominio dell'utente o di un dominio con una relazione di trust con tale dominio. Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**. Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente o di un dominio attendibile del dominio dell'utente.

**Soluzione alternativa:** Usare le condivisioni di rete dello stesso dominio Active Directory dell'utente.

### Risultati imprevedibili con Office 2010 e Office 2013 installati

Quando un utente ha installato sia Office 2010 che Office 2013, tutte le impostazioni comuni tra le due versioni di Office sono in roaming da UE-V. In questo modo, le dimensioni del pacchetto di Office 2010 possono essere abbastanza grandi o causare conflitti imprevedibili con 2013, in particolare se si usa Office 365.

**Soluzione alternativa:** Installare solo una versione di Office o limitare le impostazioni sincronizzate da UE-V.

### La disinstallazione e la reinstallazione dell'app di Windows 8 ripristinano le impostazioni sullo stato iniziale

Durante l'uso della sincronizzazione delle impostazioni di UE-V per un'app di Windows 8, se l'utente disinstalla l'app e quindi reinstalla l'app, le impostazioni dell'app ripristinano i valori predefiniti.Questo avviene perché la disinstallazione rimuove la copia locale (memorizzata nella cache) delle impostazioni dell'app, ma non rimuove il pacchetto di impostazioni locali UE-V.Quando l'app viene reinstallata e avviata, UE-V raccoglie le impostazioni dell'app che sono state reimpostate per impostazione predefinita e quindi carica le impostazioni predefinite nella posizione di archiviazione centrale.Altri computer che eseguono l'app scaricano le impostazioni predefinite.Questo comportamento è identico al comportamento delle applicazioni desktop.

**Soluzione alternativa:** Nessuno.

### Firma di posta elettronica in roaming per Outlook 2010

UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi. Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte o gli inoltri non vengono sincronizzate. Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-V non esegue il roaming.

**Soluzione alternativa:** Nessuno.

### UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office

È consigliabile installare la versione a 64 bit di Microsoft Office per i computer moderni. Per determinare la versione di cui si ha bisogno, [fare clic qui](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions). UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica. Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit. UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.

**Soluzione alternativa:** Nessuno

### <a href="" id="msi-s-are-not-localized"></a>I file MSI non sono localizzati

UE-V 2,0 include un programma di configurazione localizzato sia per l'agente UE-V che per il generatore di UE-V. Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese. Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.

**Soluzione alternativa:** Nessuno

### Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming

Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.

**Soluzione alternativa:** I favicon verranno visualizzati con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.

### I percorsi delle impostazioni dei file sono archiviati nel registro di sistema

Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema. I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.

**Soluzione alternativa:** Usa il reindirizzamento delle cartelle o altre tecnologie per assicurarti che tutti i file a cui si fa riferimento come percorsi delle impostazioni dei file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni sono in roaming.

### I percorsi di archiviazione delle impostazioni lunghe possono causare un errore

Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni. I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione. UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni. Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello) +. pkgx. Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.

**Soluzione alternativa:** Nessuno.

### Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo

Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici delle impostazioni locali (ad esempio, lingua e opzioni internazionali) verranno spostati solo tra le versioni del sistema operativo di Windows. Ad esempio, i caratteri di valuta non verranno spostati tra Windows 7 e Windows 8.

**Soluzione alternativa:** Nessuno

### Le app di Windows 8 non sincronizzano le impostazioni quando l'app viene riavviata dopo la chiusura in modo imprevisto

Se un'app di Windows 8 si chiude in modo imprevisto subito dopo l'avvio, le impostazioni per l'applicazione potrebbero non essere sincronizzate quando l'applicazione viene riavviata.

**Soluzione alternativa:** Chiudere l'app di Windows 8, chiudere e riavviare l'applicazione UevAppMonitor.exe (può usare TaskManager) e quindi riavviare l'app di Windows 8.

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>L'agente UE-V 1 genera errori durante l'uso di modelli UE-V 2

Se un modello di posizione delle impostazioni dell'UE-V 2 viene distribuito in un computer installato con un agente UE-V 1, alcune impostazioni non riescono a eseguire la sincronizzazione tra i computer e l'agente segnala gli errori nel log eventi.

**Soluzione alternativa:** Quando si esegue la migrazione da UE-V 1 a UE-V 2 ed è probabile che i computer che eseguono la versione precedente dell'agente creino un catalogo UE-V 2,0 separato per supportare l'agente e i modelli di UE-V 2,0.

## Aggiornamenti rapidi e articoli della Knowledge base per UE-V 2,0


Questa sezione contiene gli hotfix e gli articoli della KB per la versione UE-V 2,0.

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
<td align="left"><p>2927019</p></td>
<td align="left"><p>Pacchetto hotfix 1 per Microsoft User Experience Virtualization 2,0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)">support.microsoft.com/kb/2927019</a></p></td>
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
<td align="left"><p>2930271</p></td>
<td align="left"><p>Informazioni sulle limitazioni delle firme di Outlook in roaming in Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)">support.microsoft.com/kb/2930271/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Come ripristinare un'installazione di UE-V danneggiata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2850989</p></td>
<td align="left"><p>La migrazione dei profili MAPI con Microsoft UE-V non è supportata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V aggira le cartelle vuote e le chiavi del registro di sistema</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Come abilitare la registrazione di debug in Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V non aggiorna il tema nelle sessioni RDS o VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2901856</p></td>
<td align="left"><p>Le impostazioni dell'applicazione non vengono sincronizzate dopo la forza di un riavvio in un computer con supporto UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)">support.microsoft.com/kb/2901856/EN-US</a></p></td>
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

 

 

 





