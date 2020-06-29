---
title: Valori del Registro di sistema del client App-V
description: Valori del Registro di sistema del client App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819806"
---
# Valori del Registro di sistema del client App-V


Il client Microsoft Application Virtualization (App-V) archivia la propria configurazione nel registro di sistema. Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client. È anche possibile configurare molte azioni client modificando le voci del registro di sistema. Questo argomento elenca tutte le chiavi del registro di sistema di Application Virtualization (App-V) e spiega i loro usi.

**Importante**  
In un computer che utilizza un sistema operativo a 64 bit, le chiavi e i valori descritti nelle sezioni seguenti saranno in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.



## Chiave di configurazione


La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dati (esempi)</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Client desktop Microsoft Application Virtualization</p></td>
<td align="left"><p>Non modificare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>Non modificare. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Driver </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>Se il valore di questo tasto è presente, contiene il nome del driver che ha causato un errore di interruzione l'ultima volta che è stato avviato il core. Dopo aver risolto l'errore di interruzione, è necessario eliminare questo valore di chiave in modo che sftlist possa iniziare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>InstallPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Default = C:\Programmi\Microsoft Application Virtualization Client</p></td>
<td align="left"><p>Posizione in cui è installato il client. Non modificare. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFileName </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Impostazione predefinita = CSIDL_COMMON_APPDATA virtualizzazione \Microsoft\Application Client\sftlog.txt</p></td>
<td align="left"><p>Il percorso e il nome del file di log del client.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si esegue una versione precedente rispetto a App-V 4,6, SP1 e si modifica il nome o il percorso del file di log, è necessario riavviare il servizio sftlist affinché la modifica abbia effetto.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMinSeverity </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 4, informazioni</p></td>
<td align="left"><p>Controlla i messaggi scritti nel log. Il valore indica una soglia di ciò che viene registrato, ossia tutto il valore minore o uguale a quello viene registrato. Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</p>
<p>Intervallo di valori: 0x0 = None, 0x1 = critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (default), 0x5 = verbose.</p>
<p>Il livello di log è configurabile dalla console client Application Virtualization (App-V) e dal prompt dei comandi. Al prompt dei comandi il comando sftlist.exe/Verboselog aumenterà il livello di log in dettaglio. Per altre informazioni sui dettagli della riga di comando, vedere</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 4</p></td>
<td align="left"><p>Definisce il numero di copie di backup del file di log che vengono mantenute quando viene reimpostato. L'intervallo valido è 0-9999. Il valore predefinito è 4. Un valore pari a 0 indica che non verranno mantenute copie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMaxSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 256</p></td>
<td align="left"><p>Definisce la dimensione massima in megabyte (MB) che il file di log può aumentare prima di essere reimpostato. La dimensione predefinita è 256 MB. Quando questa dimensione viene raggiunta, viene forzata una reimpostazione del log per il successivo tentativo di scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0x4 (App-V 4,5)</p>
<p>Impostazione predefinita = 0x3 (App-V 4,6)</p></td>
<td align="left"><p>Indica il livello di registrazione in cui i messaggi di log vengono scritti nel log eventi di NT. Il valore indica una soglia di ciò che viene registrato, ovvero tutto ciò che è uguale o minore di quel valore viene registrato. Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</p>
<p>Intervallo di valori</p>
<p>0x0 = None</p>
<p>0x1 = Critical</p>
<p>0x2 = Errore</p>
<p>0x3 = avviso</p>
<p>0x4 = informazioni (impostazione predefinita)</p>
<p>0x5 = verbose</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Indica se lo streaming da file verrà abilitato indipendentemente dal modo in cui il client è stato configurato con il parametro APPLICATIONSOURCEROOT. Se impostato su FALSE, il trasporto non consentirà lo streaming da file, anche se l'OSD HREF o il parametro APPLICATIONSOURCEROOT contiene un percorso di file.</p>
<p>0x0 = false (impostazione predefinita)</p>
<p>0x1 = true</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>file://\uncserver\share\prodapps</p>
<p>file://\uncserver\share</p></td>
<td align="left"><p>Consente a un amministratore o a un sistema ESD (Electronic Software Distribution) di garantire il caricamento delle applicazioni in base allo schema di gestione della topologia. Usa questo valore di chiave per eseguire l'override della BASE di codice OSD per l'elemento HREF, ad esempio la posizione di origine, per un'applicazione. La radice dell'origine dell'applicazione supporta gli URL e i formati di percorso UNC (Universal Naming Convention).</p>
<p>Il formato corretto per il percorso URL è protocollo://nomeserver: [porta] [/path] [/], dove porta e percorso sono facoltativi. Se non viene specificata una porta, viene usata la porta predefinita per il protocollo. Viene sostituita solo la parte protocollo://Server: Port dell'URL OSD. </p>
<p>Il formato corretto per il percorso UNC è \computername\sharefolder [Folder] [], dove cartella è facoltativa. Il nome del computer può essere un nome di dominio completo (FQDN) o un indirizzo IP e cartellacondivisione può essere una lettera di unità. Viene sostituita solo la parte \computername\sharefolder o lettera dell'unità del percorso OSD. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\NomeCartella</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Consente a un amministratore di specificare una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione sequenziata durante la pubblicazione. I formati accettabili per OSDSourceRoot includono percorsi UNC e URL (http o HTTPS).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\NomeCartella</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Consente a un amministratore di specificare una posizione di origine per il recupero di file di icona per un pacchetto di applicazione sequenziata durante la pubblicazione. I formati accettabili per IconSourceRoot includono percorsi UNC e URL (http o HTTPS).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 5</p></td>
<td align="left"><p>Autoload è un parametro di configurazione dei criteri di runtime client che consente al client di trasmettere automaticamente in background il blocco di funzionalità secondario di un'applicazione virtualizzata. I trigger di autoload sono contrassegni per indicare gli eventi che avviano il caricamento automatico delle applicazioni. Autoload USA in modo implicito lo streaming in background per consentire il caricamento completo dell'applicazione nella cache. Il blocco di funzionalità principale verrà caricato per primo e i blocchi di funzionalità rimanenti verranno caricati in background per abilitare le operazioni in primo piano, ad esempio l'interazione dell'utente con le applicazioni, e per ottenere prestazioni percepite ottimali.</p>
<p>Valori della maschera di bit:</p>
<p>(0) mai: nessun bit viene impostato (il valore è 0), non viene eseguito il caricamento automatico, perché non sono impostati trigger.</p>
<p>(1) OnLaunch: il caricamento inizia quando un utente avvia un'applicazione.</p>
<p>(2) OnRefresh: il caricamento inizia quando viene pubblicata l'applicazione. Questo problema si verifica ogni volta che il record del pacchetto viene aggiunto o aggiornato, ad esempio quando si verifica un aggiornamento della pubblicazione.</p>
<p>(4) OnLogin: il caricamento inizia quando un utente effettua l'accesso.</p>
<p>(5) OnLaunch e OnLogin: default.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Indica cosa verrà caricato automaticamente quando si verificherà un trigger di caricamento automatico specifico. Valori della maschera di bit:</p>
<p>(0) None: nessun caricamento automatico, indipendentemente dai trigger che possono essere impostati.</p>
<p>(1) PreviouslyUsed (impostazione predefinita): se è abilitato un trigger di caricamento automatico, caricare solo i pacchetti in cui almeno un'applicazione nel pacchetto è stata usata in precedenza, ovvero avviata o prememorizzata nella cache.</p>
<p>(2) tutti: se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto (per pacchetto) o tutti i pacchetti (impostati per il client) verranno caricate automaticamente, indipendentemente dal fatto che siano state o meno avviate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Indica che l'autorizzazione è sempre necessaria, indipendentemente dal fatto che un'applicazione sia già nella cache. Valori possibili:</p>
<p>0 = false: provare sempre a connettersi al server. Se non è possibile stabilire una connessione al server, il client consente comunque all'utente di avviare un'applicazione precedentemente caricata nella cache.</p>
<p>1 = true (impostazione predefinita): l'applicazione deve sempre essere autorizzata all'avvio. Per le applicazioni in streaming RTSP, il token di autorizzazione utente viene inviato al server per l'autorizzazione. Per le applicazioni basate su file, gli ACL dei file controllano se un utente può accedere all'applicazione.</p>
<p>Riavviare il servizio sftlist affinché la modifica abbia effetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>AppData</p></td>
<td align="left"><p>Posizione in cui sono archiviate la cache delle icone e le impostazioni utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>Directory da usare per i dati globali di App-V, incluse le cache per i file OSD, i file di icone, le informazioni di collegamento e le risorse SystemGuard, ad esempio i file ini.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 o 1 </p></td>
<td align="left"><p>Default = 0: il valore 0 indica che il client cerca di intercettare le eccezioni di programma interne in modo che altre applicazioni utente possano recuperare e continuare quando si verifica un arresto anomalo. Il valore 1 indica che il client consente di eseguire le eccezioni del programma interno in modo che possano essere acquisite in un debugger.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>Timeout in secondi per le richieste interne di IPC tra core e front-end. Non modificare. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>10</p></td>
<td align="left"><p>Questo valore viene usato per indicare quanto tempo dopo l'avvio che un programma può arrestare e non generare messaggi di errore quando è in corso un'altra applicazione nella stessa suite. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 60000</p></td>
<td align="left"><p>Definisce il periodo di tempo in millisecondi che il client aspetterà mentre prova a serializzare l'avvio del programma nella stessa suite. Se il client esce in timeout, l'avvio del programma continuerà ma non verrà serializzato. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>Timeout predefinito in secondi per gli script nel file OSD se WAIT = TRUE. È possibile specificare i timeout per ogni script con TIMEOUT anziché WAIT. Un valore pari a 0 indica che non ci sono attese e 0xFFFFFFFF significa attendere per sempre. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p></p></td>
<td align="left"><p>Se, in HKLM o HKCU, questo valore contiene un percorso valido per un file di log, SFTTray scriverà in questo log quando si avviano programmi, si arresta, non si avvia e si immette o si esce dalla modalità disconnessa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) errori di avvio del log e attività di entrata e uscita della modalità disconnessa.</p>
<p>0x1F (31) registra tutto.</p>
<p>0x0 (0) registra Nothing. </p></td>
<td align="left"><p>Specifica quale dei cinque eventi vengono registrati (valori della maschera di scelta):</p>
<p>1 per l'avvio del programma</p>
<p>2 per gli errori di errore di avvio</p>
<p>4 per gli arresti</p>
<p>8 per l'immissione della modalità disconnessa</p>
<p>16 per uscire dalla modalità disconnessa per riconnettersi a un server</p>
<p>Aggiungere qualsiasi combinazione di questi numeri per attivare i rispettivi messaggi. Il valore predefinito è 0x1F se non è presente nel registro di sistema. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 3000</p></td>
<td align="left"><p>Specifica in millisecondi il tempo di attesa del cassetto quando si prova a scrivere nel log del record di avvio se un altro processo lo usa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>d:\files; C:\Documents and settings\user1\SFTs </p></td>
<td align="left"><p>Un elenco delimitato da un punto e virgola fino a cinque directory per cercare i file portatili SFT prima di richiedere all'utente di selezionare una directory. La barra rovesciata finale nei percorsi è facoltativa. Questo valore non è presente per impostazione predefinita e deve essere impostato manualmente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>Valido solo in HKCU. L'ultima posizione in cui l'utente ha esplorato durante la ricerca di un file SFT per l'importazione di pacchetti. Imposta automaticamente se SFT viene trovato correttamente. Questo viene usato per le importazioni successive quando si prova a individuare automaticamente i file SFT.</p></td>
</tr>
</tbody>
</table>



## Chiave condivisa


La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controlla i valori condivisi tra i componenti App-V. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave condivisa.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DumpPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Impostazione predefinita = C:\ </p></td>
<td align="left"><p>Percorso predefinito per creare file di dump quando si genera un minidump in un'eccezione. Questo valore predefinito è C:\ Se non specificato. Il programma di installazione client imposta questa chiave per la &lt; directory dei dati globali di virtualizzazione dell'app &gt; \Dumps. Il programma di installazione sequencer imposta questa chiave nella directory di installazione. </p></td>
</tr>
<tr class="even">
<td align="left"><p>DumpPathSizeLimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>Specifica la quantità totale massima di spazio su disco in megabyte che può essere usata per archiviare i minidump. Impostazione predefinita = 1000 MB.</p></td>
</tr>
</tbody>
</table>



## Chiave di rete


La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controlla diversi parametri correlati alla rete. Questa chiave viene usata principalmente dall'agente di trasporto di rete. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave di rete.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Online</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Abilita o Disabilita la modalità offline. Se impostato su 0, il client non comunica con i server di gestione App-V o i server di pubblicazione. Nelle operazioni disconnesse, il client può avviare un'applicazione caricata anche quando non è connessa a un server di gestione di App-V. In modalità offline il client non tenta di connettersi a un server di gestione di App-V o a un server di pubblicazione. È necessario consentire le operazioni disconnesse per poter funzionare offline. Il valore predefinito è 1 abilitato (online) e 0 è disabilitato (offline).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Abilita o Disabilita l'operazione disconnessa. Il valore predefinito è 1 abilitato e 0 è disabilitato. Quando le operazioni disconnesse sono abilitate, il client App-V può avviare un'applicazione caricata anche quando non è connessa a un server di gestione di App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1000</p></td>
<td align="left"><p>Questo valore specifica il timeout della connessione TCP in millisecondi per determinare quando andare in modalità operazioni disconnesse. Questo valore può essere usato per eseguire l'override di ConnectTimeout predefinito di 20 secondi (timeout di App-V Connect per le transazioni di rete) o del timeout TCP del sistema di circa 25 secondi. Questo porta rapidamente il client in modalità operativa disconnessa. Applicato alla connessione successiva.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1 </p></td>
<td align="left"><p>Applicabile solo se AllowDisconnectedOperation è 1, Enabled. Questo valore determina se sarà previsto un limite di tempo per quanto tempo il client sarà autorizzato ad operare nelle operazioni disconnesse. 1 = limitato. 0 = illimitato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 129600</p></td>
<td align="left"><p>Indica il numero di minuti in cui un'applicazione può essere usata in modalità operativa disconnessa.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>I valori validi sono 1-999999 in giorni espressi in minuti (1-1439998560 minuti). Il valore predefinito è 90 giorni o 129.600 minuti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocollo</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 8</p></td>
<td align="left"><p>Protocollo predefinito da usare (TCP o SSL). Finestra di dialogo Configura in opzioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Timeout di lettura per le transazioni di rete in pochi secondi. Non modificare.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Timeout di scrittura per le transazioni di rete, in secondi. Non modificare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Connettere il timeout per le transazioni di rete in pochi secondi. Non modificare.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>Numero di volte in cui provare a ristabilire una sessione eliminata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>15</p></td>
<td align="left"><p>Il numero di secondi di attesa tra i tentativi di ristabilire una sessione eliminata.</p></td>
</tr>
</tbody>
</table>



## Chiave http


La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controlla i parametri correlati al flusso HTTP. Questa chiave viene usata principalmente dall'agente di trasporto di rete. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave http.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Controlla il comportamento del flusso HTTP quando è possibile stabilire una connessione al server HTTP e il file di pacchetto non esiste più nel server HTTP. Se il valore non esiste o non è impostato su 1, il client App-V non consente di avviare un'applicazione precedentemente caricata nella cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Se questo valore è impostato su 1, il client App-V consente di avviare un'applicazione precedentemente caricata nella cache.</p></td>
</tr>
</tbody>
</table>



## Chiave del file System


I valori contenuti in HKEY \ _LOCAL \ _MACHINE tasto \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controllano i parametri del file System per App-V. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave AppFS.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>Dimensioni massime in megabyte di file di cache del file System. Se si modifica questo valore nel registro di sistema, è necessario impostare lo stato su 0 e riavviare. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Utenti\Pubblica\Documenti\SoftGrid Client\sftfs.FSD </p></td>
<td align="left"><p>Posizione del file della cache del file System. Se si modifica questo valore nel registro di sistema, è necessario lasciarlo lo stesso e riavviare o impostare lo stato su 0 e riavviare. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LetteraUnità </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>D: </p></td>
<td align="left"><p>Unità in cui verrà montato il file System App-V, se disponibile. Questo valore viene impostato dal listener o dal programma di installazione e viene letto dal file System. </p></td>
</tr>
<tr class="even">
<td align="left"><p>Stato </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>Stato del file System. Impostato su 0 e riavvia per cancellare completamente la cache del file System. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Percorso per collegamenti simbolici, impostato in HKCU. Non modificare (usare la directory dati in configurazione per cambiare). </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Spazio di archiviazione di C:\Utenti\Pubblica\Documenti\SoftGrid Client\AppFS </p></td>
<td align="left"><p>Percorso per i dati del file System globale. Non modificare. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 90 </p></td>
<td align="left"><p>Specifica la percentuale massima del file di cache del file System che può essere bloccata. Non modificare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>La caratteristica gestione dello spazio della cache del file System usa un algoritmo LRU (least used) ed è abilitato per impostazione predefinita. Se lo spazio necessario per un nuovo pacchetto supererà lo spazio disponibile nella cache, il client App-V utilizzerà questa caratteristica per determinare i pacchetti esistenti che possono essere eliminati dalla cache per creare spazio per il nuovo pacchetto. Il client elimina il pacchetto con la data di accesso ultimo meno recente, se è precedente al valore specificato nel valore del registro di sistema MinPkgAge. I valori sono 0 (disabilitato) e 1 (impostazione predefinita, abilitato).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Per determinare quando il pacchetto può essere selezionato per l'eliminazione, imposta il valore del registro di sistema su uguale al numero minimo di giorni che vuoi trascorrere dopo l'ultimo accesso al pacchetto. I pacchetti che sono stati usati più di recente non vengono eliminati.</p></td>
</tr>
</tbody>
</table>



## Tasto autorizzazioni


Per impedire agli utenti di commettere errori, gli amministratori possono usare la chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions per controllare l'accesso ad alcune azioni per gli utenti non amministrativi, ad esempio per impedire agli utenti di scaricare accidentalmente programmi. Gli utenti con diritti amministrativi possono concedersi una qualsiasi di queste autorizzazioni. Nei sistemi condivisi, ad esempio in un server Host sessione Desktop remoto (in precedenza Terminal Server), prestare particolare attenzione quando si concedono autorizzazioni aggiuntive agli utenti, perché alcune di queste autorizzazioni consentiranno agli utenti di controllare le applicazioni usate da tutti gli utenti del sistema. I valori possibili per queste impostazioni sono 1 (Consenti) e 0 (non consentito).

Le impostazioni del tasto autorizzazioni controllano tutte le interfacce che abilitano le azioni denominate. Questo include la finestra di dialogo Opzioni, SFTTray e SFTMime. Queste impostazioni non influiscono sugli amministratori. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave delle autorizzazioni.

Nome tipo dati (esempi) Descrizione ChangeFSDrive

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di selezionare una lettera di unità diversa da usare come unità di file System.

ChangeCacheSize

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di modificare le dimensioni della cache.

ChangeLogSettings

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di modificare il livello di log, modificarne la posizione e reimpostarlo tramite l'interfaccia utente.

AddApp

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di aggiungere applicazioni in modo esplicito. Questo non ha alcun effetto sulle applicazioni aggiunte tramite l'aggiornamento della pubblicazione né impedisce agli utenti di avviare (e quindi aggiungere in modo implicito) applicazioni che non sono già state aggiunte. I valori sono 0 o 1.

LoadApp 

DWORD 

0

Non consente a un utente di caricare un'applicazione. Questa è l'impostazione predefinita per gli host sessione Desktop remoto. Se si è un utente per dispositivi mobili, è consigliabile caricare completamente le applicazioni nella cache per usarle durante l'operazione disconnessa o la modalità offline. Per eseguire il flusso delle applicazioni dall'App-V Management Server o dall'App-V Streaming Server, è necessario essere connessi a un server per caricare le applicazioni.

1

Consente a un utente di caricare un'applicazione. Questa è l'impostazione predefinita per i desktop di Windows. 

UnloadApp 

DWORD 

0

Non consente a un utente di scaricare un'applicazione. Quando carichi o scarichi un pacchetto, tutte le applicazioni nel pacchetto vengono caricate o rimosse dalla cache.

1

Consente a un utente di scaricare un'applicazione. 

LockApp 

DWORD 

0

Non consente a un utente di bloccare e sbloccare un'applicazione. Questa è l'impostazione predefinita per gli host sessione Desktop remoto. Non è possibile rimuovere un'applicazione bloccata dalla cache per creare spazio per le nuove applicazioni. Per rimuovere un'applicazione bloccata dalla cache di App-V desktop o client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario sbloccarla.

1

Consente a un utente di bloccare e sbloccare un'applicazione. Questa è l'impostazione predefinita per i desktop di Windows. 

ManageTypes 

DWORD 

0

Non consente a un utente di aggiungere, modificare o rimuovere le associazioni di tipi di file solo per l'utente. Questa è l'impostazione predefinita per gli host sessione Desktop remoto. 

1

Consente a un utente di aggiungere, modificare e rimuovere associazioni di tipi di file solo per l'utente e non a livello globale. Questa è l'impostazione predefinita per i desktop di Windows. 

RefreshServer 

DWORD 

0

Non consente a un utente di attivare l'aggiornamento delle impostazioni MIME. Questa è l'impostazione predefinita per gli host sessione Desktop remoto. 

1

Consente a un utente di attivare un aggiornamento delle impostazioni MIME. Questa è l'impostazione predefinita per i desktop di Windows. 

UpdateOSDFile

DWORD

Impostazione predefinita = 0

Il valore 1 consente a un utente di usare un file OSD modificato.

ImportApp 

DWORD 

0

Non consente a un utente di importare applicazioni nella cache. La differenza tra il caricamento e l'importazione è che quando viene attivato un carico, il client ottiene il pacchetto dalla posizione attualmente configurata contenuta nell'URL OSD, ASR o override. Quando si usa l'importazione, è necessario specificare una posizione in cui ottenere il pacchetto. 

1

Consente a un utente di importare applicazioni nella cache. 

ChangeRefreshSettings

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di modificare le impostazioni di aggiornamento per i server (aggiornare l'accesso e l'aggiornamento periodico). Ciò non implica che l'utente possa modificare altre impostazioni del server (path, host e così via).

ManageServers

DWORD

Impostazione predefinita = 0

Il valore 1 consente all'utente di aggiungere, modificare e rimuovere server, ad eccezione della modifica delle impostazioni di aggiornamento, che è controllata dall'autorizzazione ChangeRefreshSettings.

PublishShortcut

DWORD

Impostazione predefinita = 0

Il valore 1 consente agli utenti di pubblicare i collegamenti tramite l'interfaccia utente. Questo non ha alcun effetto sui collegamenti pubblicati durante l'aggiornamento della pubblicazione.

ViewAllApplications

DWORD

Impostazione predefinita = 0

Il valore 1 Visualizza tutte le applicazioni tramite l'interfaccia utente. in caso contrario, verranno visualizzate solo le applicazioni dell'utente.

RepairApp

DWORD

Impostazione predefinita = 1

Il valore 1 consente all'utente di usare l'azione di ripristino sulle applicazioni in SFTMime o nella console di gestione client. Quando si ripristina un'applicazione, si rimuovono le impostazioni utente personalizzate e si ripristinano le impostazioni predefinite. Questa azione non modifica né elimina i collegamenti o le associazioni di tipi di file e non rimuove l'applicazione dalla cache.

ClearApp

DWORD

Impostazione predefinita = 1

Il valore 1 consente all'utente di usare l'azione Cancella sulle applicazioni in SFTMime o nella console di gestione client. Quando si deseleziona un'applicazione dalla console, non è più possibile usare tale applicazione. Tuttavia, l'applicazione rimane nella cache ed è ancora disponibile per altri utenti nello stesso sistema. Dopo un aggiornamento della pubblicazione, le applicazioni deselezionate diventeranno di nuovo disponibili.

DeleteApp

DWORD

Impostazione predefinita = 0

Il valore 1 consente all'utente di usare l'azione Elimina sulle applicazioni in SFTMime o nella console di gestione client. Quando si elimina un'applicazione, l'applicazione selezionata non sarà più disponibile per gli utenti di tale client. I tasti di scelta rapida e le associazioni di tipi di file vengono eliminati e l'applicazione viene eliminata dalla cache. Tuttavia, se un'altra applicazione fa riferimento ai dati nella cache del file System o ai dati delle impostazioni per l'applicazione selezionata, questi elementi non verranno eliminati.

Dopo un aggiornamento della pubblicazione, le applicazioni eliminate diventeranno di nuovo disponibili.

ToggleOfflineMode

DWORD

Il valore 1 consente agli utenti di selezionare l'esecuzione del client in modalità offline. In modalità offline l'Application Virtualization Client può avviare un'applicazione caricata anche quando non è connessa a un Application Virtualization Server.



## Impostazioni personalizzate


La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contiene valori specifici per i componenti front-end. Tutte le impostazioni personalizzate vengono archiviate come stringhe. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave CustomSettings.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 30 </p></td>
<td align="left"><p>Ora in secondi che l'area di notifica di Application Virtualization visualizzerà i messaggi di errore, ad esempio &quot; Avvia non riuscito &quot; . Valore minimo di 1. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 10 </p></td>
<td align="left"><p>Ora in secondi che l'area di notifica di appvmed visualizzerà i messaggi di successo, ad esempio &quot; Word launched &quot; o &quot; Excel Shut down &quot; . Se 0, questi messaggi verranno soppressi. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>0 = Mostra il vassoio quando le applicazioni virtualizzate sono in uso.</p>
<p>1 = Mostra sempre il vassoio.</p>
<p>2 = non mostrare mai il vassoio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Quando è presente e impostato su un valore pari a 1, le applicazioni di aggiornamento delle voci di menu vengono visualizzate nel menu vassoio ed è accessibile dall'utente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Quando è presente e impostato su un valore pari a 1, consente di visualizzare le applicazioni di caricamento delle voci di menu nel menu vassoio ed è accessibile dall'utente.</p></td>
</tr>
</tbody>
</table>



## Impostazioni per la creazione di report


La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contiene valori specifici per la creazione di report in un server di gestione di App-V. La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave per la creazione di report.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati (esempi) </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 20</p></td>
<td align="left"><p>Questo valore specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report. Le dimensioni si applicano alla cache in memoria. Quando viene raggiunto il limite, il file di log verrà ribaltato. Quando viene aggiunto un nuovo record (nella parte inferiore dell'elenco), uno o più record meno recenti (inizio elenco) verranno eliminati per creare spazio. Un avviso verrà registrato nel log del client e nel log eventi la prima volta che si verificherà e non verrà più registrato fino a quando la cache non sarà stata cancellata e il log si riempirà di nuovo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DataBlockSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 65536</p></td>
<td align="left"><p>Questo valore specifica la dimensione massima in byte da trasmettere al server contemporaneamente durante l'aggiornamento della pubblicazione, per evitare errori di trasmissione permanenti quando il log ha raggiunto una dimensione significativa. Il valore predefinito è 65536. Quando si trasmettono i dati del report sul server, un blocco di record dell'applicazione, minore o uguale alla dimensione del blocco in byte di dati XML, verrà rimosso dalla cache e inviato al server. Ogni blocco avrà i dati generali del client e i dati dell'elenco globale dei pacchetti preceduto e questi non verranno fattorizzati nei calcoli delle dimensioni dei blocchi. il potenziale esiste per un elenco di pacchetti estremamente grande per provocare errori di trasmissione su connessioni a larghezza di banda ridotta o inaffidabili.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Riferimento per Application Virtualization Client](application-virtualization-client-reference.md)









