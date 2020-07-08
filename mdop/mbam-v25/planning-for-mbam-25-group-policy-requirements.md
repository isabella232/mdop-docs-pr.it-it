---
title: Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5
description: Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823766"
---
# Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5


Usare le informazioni seguenti per determinare i tipi di protezioni di BitLocker che è possibile usare per gestire i computer client di amministrazione e monitoraggio di Microsoft BitLocker nell'organizzazione.

## Tipi di protezioni BitLocker supportate da MBAM


MBAM supporta i seguenti tipi di protezioni BitLocker.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di unità o di volume</th>
<th align="left">Protezioni BitLocker supportate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Volumi del sistema operativo</p></td>
<td align="left"><ul>
<li><p><strong>Trusted Platform Module (TPM)</strong></p></li>
<li><p><strong>TPM + PIN</strong></p></li>
<li><p><strong>TPM + chiave USB </strong> -supportato solo quando il volume del sistema operativo è crittografato prima che mbam sia installato</p></li>
<li><p><strong>TPM + PIN + tasto USB </strong> - supportato solo quando il volume del sistema operativo è crittografato prima che mbam sia installato</p></li>
<li><p><strong>Password </strong> - supportata solo per i dispositivi Windows to go, le unità dati fisse e i dispositivi Windows 8, Windows 8,1 e Windows 10 che non dispongono di un TPM</p></li>
<li><p><strong>La password numerica </strong> - viene applicata automaticamente come parte della crittografia del volume e non deve essere configurata tranne in modalità FIPS in Windows 7</p></li>
<li><p><strong>Agente recupero dati (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Unità dati fisse</p></td>
<td align="left"><ul>
<li><p><strong>Password</strong></p></li>
<li><p><strong>Sblocco automatico</strong></p></li>
<li><p><strong>La password numerica </strong> - viene applicata automaticamente come parte della crittografia del volume e non deve essere configurata tranne in modalità FIPS in Windows 7</p></li>
<li><p><strong>Agente recupero dati (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità rimovibili</p></td>
<td align="left"><ul>
<li><p><strong>Password</strong></p></li>
<li><p><strong>Sblocco automatico</strong></p></li>
<li><p><strong>La password numerica </strong> - viene applicata automaticamente come parte della crittografia del volume e non deve essere configurata</p></li>
<li><p><strong>Agente recupero dati (DRA)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### Supporto per i criteri BitLocker di crittografia dello spazio usato

In MBAM 2,5 SP1, se si Abilita la crittografia dello spazio usato tramite criteri di gruppo di BitLocker, il client MBAM lo onora.

Questa impostazione di criteri di gruppo è denominata **Applica tipo di crittografia unità sulle unità del sistema operativo** e si trova nel nodo GPO seguente: **configurazione di computer** &gt; **modelli amministrativi** &gt; **componenti di Windows** &gt; **unità BitLocker Drive** &gt; **System**Encryption. Se si Abilita questo criterio e si seleziona il tipo di crittografia come **solo spazio usato**per la crittografia, mbam consentirà di rispettare i criteri e BitLocker crittografa solo lo spazio su disco usato nel volume.

## Come ottenere i modelli di criteri di gruppo di MBAM e modificare le impostazioni


Quando si è pronti per configurare le impostazioni dei criteri di gruppo di MBAM desiderate, eseguire le operazioni seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Procedura da seguire</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiare i modelli dei criteri di gruppo di MBAM <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> per ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX) </a> e installarli in un computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare le impostazioni dei criteri di gruppo che si desidera utilizzare nell'organizzazione.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>



## Descrizioni delle impostazioni dei criteri di gruppo di MBAM


Il nodo GPO di **MDOP (BitLocker Management)** contiene quattro impostazioni dei criteri globali e quattro nodi figlio GPO: **gestione client**, **unità fisse**, **unità del sistema operativo**e **unità rimovibile**. Le sezioni seguenti descrivono e suggeriscono le impostazioni per le impostazioni dei criteri di gruppo di MBAM.

**Importante**  
Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente. MBAM configura automaticamente le impostazioni in questo nodo quando si configurano le impostazioni nel nodo **MDOP mbam (BitLocker Management)** .



### Definizioni di criteri di gruppo globali

Questa sezione descrive le definizioni di criteri di gruppo globali di MBAM nel nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (Gestione BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni di criteri di gruppo consigliate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Scegliere il metodo di crittografia unità e la forza di cifratura</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Configura questo criterio per usare un metodo di crittografia specifico e un livello di codifica.</p>
<p>Quando questo criterio non è configurato, BitLocker usa il metodo di crittografia predefinito: AES 128 bit con il diffusore.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Un problema relativo al report di conformità del computer BitLocker consente di visualizzare &quot; sconosciuto &quot; per il livello di codifica, anche se si usa il valore predefinito. Per risolvere il problema, verificare che l'impostazione sia abilitata e impostare un valore per la forza di cifratura.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128-bit con diffusore-solo per Windows 7</p></li>
<li><p>AES 128 per Windows 8, Windows 8,1 e Windows 10</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Impedire la sovrascrittura della memoria al riavvio</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per migliorare le prestazioni di riavvio senza sovrascrivere i segreti di BitLocker in memoria al riavvio.</p>
<p>Quando questo criterio non è configurato, i segreti di BitLocker vengono rimossi dalla memoria quando il computer viene riavviato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Convalidare la regola di utilizzo del certificato smart card</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per l'uso della protezione BitLocker basata su certificati smartcard.</p>
<p>Quando questo criterio non è configurato, viene usato l'identificatore di oggetto predefinito 1.3.6.1.4.1.311.67.1.1 per specificare un certificato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Specificare gli identificatori univoci per l'organizzazione</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per l'uso di un agente di recupero dati basato su certificati o del lettore BitLocker to go.</p>
<p>Quando questo criterio non è configurato, il <strong> campo di identificazione </strong> non viene usato.</p>
<p>Se la società richiede misure di sicurezza più elevate, è possibile configurare il <strong> </strong> campo di identificazione per assicurarsi che tutti i dispositivi USB abbiano questo set di campi e che siano allineati con questa impostazione di criteri di gruppo.</p></td>
</tr>
</tbody>
</table>



### Definizioni di criteri di gruppo per la gestione dei client

Questa sezione descrive le definizioni dei criteri di gestione dei client per mbam presso il nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)** &gt; **Client Management**.

È possibile impostare le stesse impostazioni dei criteri di gruppo per le topologie di integrazione di System Center Configuration Manager autonomo e di sistema, con una sola eccezione: disabilitare l'impostazione di ** &gt; endpoint del servizio Reporting Services** mbam per la configurazione dei servizi per l'utente se si usa la topologia di integrazione di Configuration Manager, come indicato nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni di criteri di gruppo consigliate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurare i servizi MBAM</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<ul>
<li><p><strong>Endpoint del servizio di recupero e hardware di MBAM </strong> . Usare questa impostazione per abilitare la gestione della crittografia BitLocker client. Immettere una posizione dell'endpoint simile all'esempio seguente: <strong> http (s):// </strong><em> &lt; mbam Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; la porta il servizio Web è associato a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selezionare informazioni di ripristino di BitLocker da archiviare </strong> . Questa impostazione consente di configurare il servizio di recupero chiavi per eseguire il backup delle informazioni di ripristino di BitLocker. Consente inoltre di configurare un servizio di segnalazione dello stato per la raccolta di report. Il criterio fornisce un metodo amministrativo per il recupero dei dati crittografati da BitLocker per evitare la perdita di dati a causa della mancanza di informazioni chiave. Il rapporto di stato e l'attività di ripristino della chiave vengono inviati automaticamente e silenziosamente alla posizione del server di report configurata.</p>
<p>Se non si configura questa impostazione del criterio o se la si disattiva, le informazioni relative al ripristino della chiave non vengono salvate e il rapporto sullo stato e l'attività di ripristino della chiave non vengono segnalati al server. Quando questa impostazione è impostata su <strong> password di ripristino e pacchetto di tasti </strong> , la password di ripristino e il pacchetto di chiavi vengono automaticamente e silenziosamente configurati nel percorso del server di recupero chiavi configurato.</p></li>
<li><p><strong>Immettere il controllo della frequenza di stato del client in pochi minuti </strong> . Questa impostazione del criterio gestisce la frequenza con cui il client controlla i criteri e lo stato di protezione di BitLocker nel computer client. Questo criterio gestisce anche la frequenza con cui lo stato di conformità del client viene salvato nel server. Il client controlla i criteri e lo stato di protezione di BitLocker nel computer client e esegue anche il backup della chiave di ripristino client in corrispondenza della frequenza configurata.</p>
<p>Imposta questa frequenza in base al requisito impostato dalla tua società per controllare con quale frequenza verificare lo stato di conformità del computer e con quale frequenza eseguire il backup della chiave di ripristino del client.</p></li>
<li><p><strong>Endpoint del servizio Segnalazione stato di MBAM:</strong></p>
<p><strong>Per MBAM in una topologia autonoma </strong> : è necessario configurare questa impostazione per abilitare la gestione della crittografia BitLocker client.</p>
<p>Immettere una posizione dell'endpoint simile all'esempio seguente:</p>
<p><strong>http (s):// </strong><em> &lt; mbam amministrazione e monitoraggio del server nome &gt; </em><strong> : </strong><em> &lt; la porta il servizio Web è associato a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc</strong></p>
<p><strong>Per MBAM nella topologia di integrazione di Configuration Manager </strong> : disabilitare questa impostazione.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare i criteri di esenzione dall'utente</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri consente di configurare un indirizzo del sito Web, un indirizzo di posta elettronica o un numero di telefono che indica a un utente di richiedere un'esenzione dalla crittografia BitLocker.</p>
<p>Se si abilita questa impostazione per i criteri e si specifica un indirizzo del sito Web, un indirizzo di posta elettronica o un numero di telefono, gli utenti vedranno una finestra di dialogo con istruzioni su come richiedere un'esenzione dalla protezione di BitLocker. Per altre informazioni sull'abilitazione delle esenzioni crittografiche di BitLocker per gli utenti, vedere <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> come gestire le esenzioni di crittografia degli utenti di BitLocker </a> .</p>
<p>Se si disattiva o non si configura questa impostazione per i criteri, le istruzioni per la richiesta di esenzione non vengono visualizzate agli utenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>L'esenzione dall'utente è gestita per utente, non per computer. Se più utenti accedono allo stesso computer e un utente non è esonerato, il computer viene crittografato.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare il programma Analisi utilizzo software</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione dei criteri consente di configurare il modo in cui gli utenti di MBAM possono partecipare al programma Analisi utilizzo software. Questo programma raccoglie informazioni sull'hardware del computer e su come gli utenti usano MBAM senza interrompere il lavoro. Le informazioni consentono a Microsoft di identificare le caratteristiche di MBAM da migliorare. Microsoft non usa queste informazioni per identificare o contattare gli utenti di MBAM.</p>
<p>Se si abilita questa impostazione, gli utenti possono partecipare al programma Analisi utilizzo software.</p>
<p>Se si disabilita questa impostazione, gli utenti non potranno partecipare al programma Analisi utilizzo software.</p>
<p>Se non si configura questa impostazione, gli utenti hanno la possibilità di partecipare al programma Analisi utilizzo software.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Specificare l'URL per il collegamento ai criteri di sicurezza</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Usare questa impostazione per specificare un URL visualizzato per gli utenti finali come collegamento denominato &quot; criteri di sicurezza aziendali. &quot; Il collegamento punta ai criteri di sicurezza interni della società e fornisce agli utenti finali informazioni sui requisiti di crittografia. Il collegamento viene visualizzato quando gli utenti vengono richiesti da MBAM per crittografare un'unità.</p>
<p>Se si abilita questa impostazione per i criteri, è possibile configurare l'URL per il collegamento ai criteri di sicurezza.</p>
<p>Se si disattiva o non si configura questa impostazione, il collegamento ai criteri di sicurezza non viene visualizzato agli utenti.</p></td>
</tr>
</tbody>
</table>



### Definizioni di criteri di gruppo unità fisse

In questa sezione vengono illustrate le definizioni dei criteri di unità fisse per l'amministrazione e il monitoraggio di Microsoft BitLocker presso il nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (Gestione BitLocker)** &gt; **unità fissa**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni di criteri di gruppo consigliate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni di crittografia unità dati fisse</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione dei criteri consente di controllare se le unità dati fisse devono essere crittografate.</p>
<p>Se il volume del sistema operativo è necessario per essere crittografato, fare clic su <strong> Attiva unità dati fisse di sblocco automatico </strong> .</p>
<p>Quando si Abilita questo criterio, non è necessario disabilitare la <strong> configurazione dell'uso della password per i criteri delle unità dati fisse, a </strong> meno che non si stia abilitando o richiedendo l'uso di sblocco automatico per le unità dati fisse.</p>
<p>Se è necessario usare l'opzione di sblocco automatico per le unità dati fisse, è necessario configurare i volumi del sistema operativo da crittografare.</p>
<p>Se si abilita questa impostazione, gli utenti dovranno inserire tutte le unità dati fisse in protezione BitLocker e le unità dati verranno crittografate.</p>
<p>Se non si configura questa impostazione, gli utenti non sono tenuti a inserire unità dati fisse in protezione BitLocker. Se applichi questo criterio dopo aver crittografato le unità dati fisse, l'agente MBAM decrittografa le unità dati fisse crittografate.</p>
<p>Se si disabilita questa impostazione, gli utenti non possono inserire le unità dati fisse in protezione BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negare l'accesso in scrittura alle unità fisse non protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri determina se la protezione di BitLocker è necessaria per le unità dati fisse per la scrittura in un computer. Questa impostazione dei criteri viene applicata quando si attiva BitLocker.</p>
<p>Quando il criterio non è configurato, tutte le unità dati fisse nel computer vengono montate con l'autorizzazione di lettura/scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso a dischi fissi protetti da BitLocker da versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio in modo che le unità fisse con il file system FAT possano essere sbloccate e visualizzate nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Quando il criterio è abilitato o non configurato, le unità fisse formattate con il file system FAT possono essere sbloccate e il loro contenuto può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2. Questi sistemi operativi hanno l'autorizzazione di sola lettura per le unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità fisse formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità fisse</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Usare questo criterio per specificare se è necessaria una password per sbloccare le unità dati fisse protette da BitLocker.</p>
<p>Se si abilita questa impostazione, gli utenti possono configurare una password che soddisfi i requisiti definiti. BitLocker consente agli utenti di sbloccare un'unità con qualsiasi protezione disponibile nell'unità.</p>
<p>Queste impostazioni vengono applicate quando si attiva BitLocker, non quando si sblocca un volume.</p>
<p>Se si disabilita questa impostazione, gli utenti non possono usare una password.</p>
<p>Quando il criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, abilitare questo criterio e quindi selezionare <strong> Richiedi password per l'unità dati fissa </strong> , fare clic su <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password </strong> desiderata.</p>
<p>Se si disabilita questa impostazione, gli utenti non possono usare una password.</p>
<p>Se non si configura questa impostazione, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperati i dischi fissi protetti da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando il criterio non è configurato, l'agente di ripristino dei dati di BitLocker è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory. MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni per l'applicazione dei criteri di crittografia</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Usa questa impostazione per configurare il numero di giorni in cui le unità dati fisse possono rimanere conforme finché non vengono costrette a rispettare i criteri di MBAM. Gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione dopo il periodo di tolleranza. Il periodo di tolleranza viene avviato quando l'unità dati fissa viene determinata come non conforme. Tuttavia, i criteri di unità dati fissi non vengono applicati finché l'unità del sistema operativo non è conforme.</p>
<p>Se il periodo di tolleranza scade e l'unità dati fissa non è ancora conforme, gli utenti non hanno la possibilità di rinviare o richiedere un'esenzione. Se il processo di crittografia richiede l'input dell'utente, viene visualizzata una finestra di dialogo che gli utenti non possono chiudere fino a quando non forniscano le informazioni richieste.</p>
<p>Immettere <strong> 0 </strong> nella finestra <strong> Configura il numero di giorni di tolleranza per le unità fisse per </strong> forzare il processo di crittografia a iniziare immediatamente dopo la scadenza del periodo di tolleranza per l'unità del sistema operativo.</p>
<p>Se si disattiva o non si configura questa impostazione, gli utenti non saranno costretti a rispettare i criteri di MBAM.</p>
<p>Se non è necessaria alcuna interazione con l'utente per aggiungere un Protector, la crittografia inizia in background dopo la scadenza del periodo di tolleranza.</p></td>
</tr>
</tbody>
</table>



### Definizioni dei criteri di gruppo unità del sistema operativo

In questa sezione vengono illustrate le definizioni dei criteri di unità del sistema operativo per l'amministrazione e il monitoraggio di Microsoft BitLocker presso il nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)** &gt; **drive del sistema operativo**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni di criteri di gruppo consigliate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni di crittografia unità del sistema operativo</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione dei criteri consente di gestire se l'unità del sistema operativo deve essere crittografata.</p>
<p>Per una maggiore sicurezza, valutare la possibilità di disabilitare le impostazioni dei criteri seguenti nelle <strong> impostazioni di sospensione del sistema </strong> &gt; <strong> Power Management </strong> &gt; <strong> </strong> quando si abilitano con TPM + PIN Protector:</p>
<ul>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (collegato)</p></li>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (sulla batteria)</p></li>
</ul>
<p>Se si esegue Microsoft Windows 8 o versione successiva e si vuole usare BitLocker in un computer senza un TPM, selezionare la casella di <strong> controllo Consenti BitLocker senza un TPM compatibile </strong> . In questa modalità è necessaria una password per l'avvio. Se si dimentica la password, è necessario usare una delle opzioni di ripristino di BitLocker per accedere all'unità.</p>
<p>In un computer con un TPM compatibile è possibile usare due tipi di metodi di autenticazione all'avvio per ottenere una protezione aggiuntiva per i dati crittografati. All'avvio del computer, può usare solo il TPM per l'autenticazione oppure può richiedere l'immissione di un PIN (Personal Identification Number).</p>
<p>Se si abilita questa impostazione, gli utenti devono inserire l'unità del sistema operativo in protezione BitLocker e l'unità viene quindi crittografata.</p>
<p>Se si disabilita questo criterio, gli utenti non possono inserire l'unità del sistema operativo in protezione BitLocker. Se applichi questo criterio dopo che l'unità del sistema operativo è stata crittografata, l'unità viene decrittografata.</p>
<p>Se non si configura questo criterio, non è necessario che l'unità del sistema operativo venga inserita in protezione BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Consentire i PIN avanzati per l'avvio</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Usare questa impostazione per specificare se usare i pin di avvio avanzati con BitLocker. I pin di avvio avanzati consentono l'uso di caratteri che includono lettere maiuscole e minuscole, simboli, numeri e spazi. Questa impostazione dei criteri viene applicata quando si attiva BitLocker.</p>
<p>Se si abilita questa impostazione per i criteri, tutti i nuovi PIN di avvio di BitLocker consentiranno all'utente finale di creare PIN avanzati. Tuttavia, non tutti i computer possono supportare i PIN avanzati nell'ambiente di pre-avvio. Consigliamo vivamente agli amministratori di valutare se i loro sistemi sono compatibili con questa caratteristica prima di abilitarne l'uso.</p>
<p>Selezionare la <strong> casella di controllo Richiedi i pin solo ASCII </strong> per rendere più compatibili i PIN avanzati con i computer che limitano il tipo o il numero di caratteri che possono essere immessi nell'ambiente di pre-avvio.</p>
<p>Se si disattiva o non si configura questa impostazione, i PIN avanzati non vengono usati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui è possibile recuperare le unità del sistema operativo protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando questo criterio non è configurato, l'agente recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso di password per le unità del sistema operativo</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Usare questa impostazione per impostare i vincoli per le password usate per sbloccare le unità del sistema operativo protette da BitLocker. Se le protezioni non TPM sono consentite per le unità del sistema operativo, è possibile eseguire il provisioning di una password, applicare requisiti di complessità alla password e configurare una lunghezza minima per la password. Per rendere effettive le impostazioni dei requisiti di complessità, è necessario abilitare la password di impostazione dei criteri di gruppo per &quot; soddisfare i requisiti &quot; di complessità nella configurazione del computer criteri per la &gt; password dell'account delle impostazioni di sicurezza di Windows &gt; &gt; &gt; .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Queste impostazioni vengono applicate quando si attiva BitLocker, non quando si sblocca un volume. BitLocker consente di sbloccare un'unità con qualsiasi protezione disponibile nell'unità.</p>
</div>
<div>

</div>
<p>Se si abilita questa impostazione, gli utenti possono configurare una password che soddisfi i requisiti definiti. Per applicare requisiti di complessità alla password, fare clic su <strong> Richiedi complessità password </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare il profilo di convalida della piattaforma TPM per le configurazioni del firmware basate su BIOS</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di configurare in che modo l'hardware di sicurezza TPM (Trusted Platform Module) di computer&#39;s protegge la chiave di crittografia BitLocker. Questa impostazione non si applica se nel computer non è presente un TPM compatibile o se BitLocker è già stato attivato con la protezione TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Questa impostazione di criteri di gruppo si applica solo ai computer con configurazioni BIOS o a computer con firmware UEFI con un modulo di servizio compatibilità (CSM) abilitato. I computer che usano una configurazione del firmware UEFI nativa archiviano valori diversi nei registri di configurazione della piattaforma (PCRs). Usare il &quot; profilo di convalida della piattaforma TPM per le configurazioni del firmware UEFI nativo per &quot; configurare il profilo PCR TPM per i computer che usano il firmware UEFI nativo.</p>
</div>
<div>

</div>
<p>Se si abilita questa impostazione per i criteri prima di attivare BitLocker, è possibile configurare i componenti di avvio convalidati dal TPM prima di sbloccare l'accesso all'unità del sistema operativo crittografata con BitLocker. Se uno di questi componenti cambia mentre la protezione di BitLocker è attiva, il TPM non rilascia la chiave di crittografia per sbloccare l'unità e il computer visualizza invece la console di ripristino di BitLocker e richiede di specificare la password di ripristino o il tasto di ripristino per sbloccare l'unità.</p>
<p>Se si disattiva o non si configura questa impostazione per i criteri, BitLocker usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare il profilo di convalida della piattaforma TPM</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di configurare in che modo l'hardware di sicurezza TPM (Trusted Platform Module) di computer&#39;s protegge la chiave di crittografia BitLocker. Questa impostazione non si applica se nel computer non è presente un TPM compatibile o se BitLocker è già stato attivato con la protezione TPM.</p>
<p>Se si abilita questa impostazione per i criteri prima di attivare BitLocker, è possibile configurare i componenti di avvio convalidati dal TPM prima di sbloccare l'accesso all'unità del sistema operativo crittografata con BitLocker. Se uno di questi componenti cambia mentre la protezione di BitLocker è attiva, il TPM non rilascia la chiave di crittografia per sbloccare l'unità e il computer visualizza invece la console di ripristino di BitLocker e richiede di specificare la password di ripristino o il tasto di ripristino per sbloccare l'unità.</p>
<p>Se si disattiva o non si configura questa impostazione per i criteri, BitLocker usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare il profilo di convalida della piattaforma TPM per le configurazioni del firmware UEFI Native</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di configurare in che modo l'hardware di sicurezza TPM (Trusted Platform Module) di computer&#39;s protegge la chiave di crittografia BitLocker. Questa impostazione non si applica se nel computer non è presente un TPM compatibile o se BitLocker è già stato attivato con la protezione TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Questa impostazione di criteri di gruppo si applica solo ai computer con una configurazione del firmware UEFI nativa.</p>
</div>
<div>

</div>
<p>Se si abilita questa impostazione per i criteri prima di attivare BitLocker, è possibile configurare i componenti di avvio convalidati dal TPM prima di sbloccare l'accesso all'unità del sistema operativo crittografata con BitLocker. Se uno di questi componenti cambia mentre la protezione di BitLocker è attiva, il TPM non rilascia la chiave di crittografia per sbloccare l'unità e il computer visualizza invece la console di ripristino di BitLocker e richiede di specificare la password di ripristino o il tasto di ripristino per sbloccare l'unità.</p>
<p>Se si disattiva o non si configura questa impostazione per i criteri, BitLocker usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ripristinare i dati di convalida della piattaforma dopo il ripristino di BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Usare questa impostazione per controllare se i dati di convalida della piattaforma vengono aggiornati quando si avvia Windows dopo il ripristino di BitLocker.</p>
<p>Se si abilita questa impostazione, i dati di convalida della piattaforma vengono aggiornati quando si avvia Windows dopo il ripristino di BitLocker. Se si disabilita questa impostazione, i dati di convalida della piattaforma non vengono aggiornati quando si avvia Windows dopo il ripristino di BitLocker. Se non si configura questa impostazione, i dati di convalida della piattaforma vengono aggiornati quando si avvia Windows dopo il ripristino di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usare il profilo di convalida dei dati di configurazione avanzata</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di scegliere le impostazioni specifiche dei dati di configurazione del boot (BCD) per verificare durante la convalida della piattaforma.</p>
<p>Se si abilita questa impostazione per i criteri, è possibile aggiungere altre impostazioni, rimuovere le impostazioni predefinite o entrambe. Se si disabilita questa impostazione, il computer viene ripristinato in un profilo BCD simile al profilo BCD predefinito usato da Windows 7. Se non si configura questa impostazione del criterio, il computer verifica le impostazioni predefinite di Windows BCD.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Quando BitLocker usa l'avvio sicuro per la convalida della piattaforma e dell'integrità dei dati di configurazione di avvio (BCD), come definito dai &quot; criteri Consenti avvio sicuro per la convalida &quot; dell'integrità, i &quot; criteri di profilo di convalida dei dati di configurazione dell'avvio avanzati &quot; vengono ignorati.</p>
</div>
<div>

</div>
<p>L'impostazione che controlla il debug di avvio (0x16000010) viene sempre convalidata e non ha alcun effetto se è inclusa nei campi forniti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni per l'applicazione dei criteri di crittografia</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Usare questa impostazione per configurare il numero di giorni in cui gli utenti possono rinviare l'applicazione dei criteri di MBAM per l'unità del proprio sistema operativo. Il periodo di tolleranza inizia quando il sistema operativo viene rilevato per la prima volta come non conforme. Dopo la scadenza del periodo di tolleranza, gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione.</p>
<p>Se il processo di crittografia richiede l'input dell'utente, viene visualizzata una finestra di dialogo che gli utenti non possono chiudere fino a quando non forniscano le informazioni richieste.</p>
<p>Se si disattiva o non si configura questa impostazione, gli utenti non saranno costretti a rispettare i criteri di MBAM.</p>
<p>Se non è necessaria alcuna interazione con l'utente per aggiungere un Protector, la crittografia inizia in background dopo la scadenza del periodo di tolleranza.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare il messaggio di ripristino e l'URL di pre-avvio</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questa impostazione per la configurazione di un messaggio di ripristino personalizzato o per specificare un URL che viene quindi visualizzato nella schermata di ripristino di BitLocker pre-boot quando l'unità del sistema operativo è bloccata. Questa impostazione è disponibile solo nei computer client che eseguono Windows 10.</p>
<p>Quando questo criterio è abilitato, è possibile selezionare una di queste opzioni per il messaggio di ripristino di pre-avvio:</p>
<ul>
<li><p><strong>Usare il messaggio di ripristino personalizzato </strong> : selezionare questa opzione per includere un messaggio personalizzato nella schermata di ripristino di BitLocker di pre-avvio. Nella <strong> casella opzione messaggio di ripristino personalizzato </strong> digitare il messaggio che si vuole visualizzare. Se si vuole anche specificare un URL di ripristino, includerlo come parte del messaggio di ripristino personalizzato.</p></li>
<li><p><strong>Usare l'URL di ripristino personalizzato </strong> : selezionare questa opzione per sostituire l'URL predefinito visualizzato nella schermata di ripristino di BitLocker di pre-avvio. Nella <strong> casella dell'opzione URL di ripristino personalizzato </strong> digitare l'URL che si vuole visualizzare.</p></li>
<li><p><strong>Usare l'URL e il messaggio </strong> di ripristino predefiniti: selezionare questa opzione per visualizzare il messaggio e l'URL di ripristino di BitLocker predefiniti nella schermata di ripristino di BitLocker di pre-avvio. Se in precedenza è stato configurato un URL o un messaggio di ripristino personalizzato e si vuole ripristinare il messaggio predefinito, è necessario abilitare questo criterio e selezionare l' <strong> opzione Usa messaggio di ripristino predefinito e URL </strong> .</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Non tutti i caratteri e le lingue sono supportati in pre-boot. È consigliabile verificare che i caratteri usati per il messaggio o l'URL personalizzato vengano visualizzati correttamente nella schermata di ripristino di BitLocker pre-boot.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### Definizioni di criteri di gruppo unità rimovibili

Questa sezione descrive le definizioni dei criteri di gruppo delle unità rimovibili per l'amministrazione e il monitoraggio di Microsoft BitLocker presso il nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)** &gt; **drive rimovibile**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni di criteri di gruppo consigliate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controllare l'uso di BitLocker su unità rimovibili</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questo criterio Controlla l'uso di BitLocker su unità dati rimovibili.</p>
<p>Fare clic su <strong> Consenti agli utenti di applicare la protezione BitLocker sulle unità dati rimovibili </strong> per consentire agli utenti di eseguire la configurazione guidata BitLocker in un'unità dati rimovibile.</p>
<p>Fare clic su <strong> Consenti agli utenti di sospendere e decrittografare BitLocker in unità dati rimovibili </strong> per consentire agli utenti di rimuovere la crittografia unità BitLocker dall'unità o di sospendere la crittografia durante l'esecuzione della manutenzione.</p>
<p>Quando questo criterio è abilitato e si fa clic su <strong> Consenti agli utenti di applicare la protezione BitLocker sulle unità dati rimovibili </strong> , il client mbam Salva le informazioni di ripristino sulle unità rimovibili nel server di ripristino di mbam Key e consente agli utenti di recuperare l'unità se la password è perduta.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negare l'accesso in scrittura alle unità rimovibili non protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire solo le autorizzazioni di scrittura per le unità protette da BitLocker.</p>
<p>Quando questo criterio è abilitato, tutte le unità dati rimovibili nel computer richiedono la crittografia prima che sia consentita l'autorizzazione di scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso alle unità rimovibili protette da BitLocker dalle versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire alle unità fisse che il file system FAT venga sbloccato e visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Quando questo criterio non è configurato, le unità rimovibili formattate con il file system FAT possono essere sbloccate nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2 e il loro contenuto può essere visualizzato. Questi sistemi operativi hanno l'autorizzazione di sola lettura per le unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità rimovibili formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità dati rimovibili</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per configurare la protezione con password sulle unità dati rimovibili.</p>
<p>Quando questo criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, è possibile abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati rimovibili </strong> , fare clic su <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password preferita </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperate le unità rimovibili protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando è impostato su <strong> non configurato </strong> , l'agente di recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>




## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Prerequisiti per la distribuzione di MBAM 2.5](mbam-25-deployment-prerequisites.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






