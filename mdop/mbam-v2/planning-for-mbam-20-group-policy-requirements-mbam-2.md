---
title: Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0
description: Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804521"
---
# Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0


Per gestire i computer client di amministrazione e monitoraggio di Microsoft BitLocker, è necessario prendere in considerazione i tipi di protezioni di BitLocker che si desidera supportare nell'organizzazione e quindi configurare le impostazioni di criteri di gruppo corrispondenti che si desidera applicare. Questo argomento descrive le impostazioni dei criteri di gruppo disponibili per l'uso quando si usa l'amministrazione e il monitoraggio di Microsoft BitLocker per gestire la crittografia unità BitLocker nell'organizzazione.

MBAM supporta i seguenti tipi di protezioni per BitLocker per le unità del sistema operativo: Trusted Platform Module (TPM), TPM + PIN, TPM + chiavetta USB e TPM + PIN + chiave USB, password, password numerica e agente di recupero dati. La protezione tramite password è supportata solo per i dispositivi Windows to go e per i dispositivi Windows 8 che non dispongono di un TPM. MBAM supporta la chiave TPM + USB e la chiave di protezione TPM + PIN + USB solo quando il volume del sistema operativo viene crittografato prima dell'installazione di MBAM.

MBAM supporta i seguenti tipi di protezioni BitLocker per le unità dati fisse: password, sblocco automatico, password numerica e agente di recupero dati.

La protezione con password numerica viene applicata automaticamente come parte della crittografia del volume e non deve essere configurata.

**Importante**  
Le impostazioni dell'oggetto Criteri di gruppo (GPO) di crittografia unità BitLocker di Windows predefinite non vengono usate da MBAM e possono causare un comportamento conflittuale se sono abilitate. Per abilitare MBAM per la gestione di BitLocker, è necessario definire le impostazioni dei criteri di gruppo di MBAM solo dopo l'installazione del modello di criteri di gruppo di mbam.



I pin di avvio avanzati possono contenere caratteri, ad esempio lettere maiuscole e minuscole e numeri. A differenza di BitLocker, MBAM non supporta l'uso di simboli e spazi per i PIN avanzati.

Installare il modello dei criteri di gruppo di MBAM in un computer in grado di eseguire la console Gestione criteri di gruppo o la tecnologia MDOP avanzata di gestione dei criteri di gruppo. Per modificare le impostazioni degli oggetti Criteri di gruppo che abilitano le funzionalità di mbam, devi prima installare il modello mbam Policy Group, aprire GPMC o Advanced Group Policy Management per modificare il GPO applicabile e quindi passare al nodo GPO seguente: criteri di **configurazione dei computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker).**

Il nodo GPO di MDOP MBAM (BitLocker Management) contiene quattro impostazioni dei criteri globali e quattro nodi di impostazioni GPO figlio: gestione client, unità fisse, unità del sistema operativo e unità rimovibile. Le sezioni seguenti includono definizioni di criteri e impostazioni dei criteri suggerite per aiutarti a pianificare i requisiti per l'impostazione dei criteri GPO di MBAM.

**Nota**  
Per altre informazioni sulla configurazione delle impostazioni degli oggetti Criteri di ricerca minime consigliate per consentire a MBAM di gestire la crittografia BitLocker, vedere [come modificare le impostazioni dei GPO di mbam 2,0](how-to-edit-mbam-20-gpo-settings-mbam-2.md).



## Definizioni di criteri globali


Questa sezione descrive le definizioni di criteri globali di mbam disponibili nel nodo GPO seguente: criteri di **configurazione dei computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazione di criteri suggeriti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Scegliere il metodo di crittografia unità e la forza di cifratura</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configura questo criterio per usare un metodo di crittografia specifico e un livello di codifica.</p>
<p>Quando questo criterio non è configurato, BitLocker usa il metodo di crittografia predefinito di AES 128 bit con il diffusore o il metodo di crittografia specificato dallo script di configurazione.</p></td>
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
<p>Quando questo criterio non è configurato, per specificare un certificato viene usato un identificatore di oggetto predefinito 1.3.6.1.4.1.311.67.1.1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Specificare gli identificatori univoci per l'organizzazione</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per l'uso di un agente di recupero dati basato su certificati o del lettore BitLocker to go.</p>
<p>Quando questo criterio non è configurato, il <strong> campo di identificazione </strong> non viene usato.</p>
<p>Se la società richiede misure di sicurezza più elevate, è consigliabile configurare <strong> il </strong> campo di identificazione per assicurarsi che tutti i dispositivi USB dispongano di questo set di campi e che siano allineati con questa impostazione di criteri di gruppo.</p></td>
</tr>
</tbody>
</table>



## Definizioni dei criteri di gestione client


Questa sezione descrive le definizioni dei criteri di gestione dei client per l'amministrazione e il monitoraggio di Microsoft BitLocker disponibili nel nodo GPO seguente: criteri di **configurazione dei computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)** \\ **Client Management**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazioni dei criteri suggerite</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurare i servizi MBAM</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<ul>
<li><p><strong>Endpoint del servizio di recupero e hardware di MBAM </strong> . Usare questa impostazione per abilitare la gestione della crittografia BitLocker client. Immettere una posizione di endpoint simile all'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selezionare informazioni di ripristino di BitLocker da archiviare </strong> . Questa impostazione consente di configurare il servizio di recupero chiavi per eseguire il backup delle informazioni di ripristino di BitLocker. Consente inoltre di configurare il servizio di segnalazione dello stato per la raccolta dei report di conformità e controllo. Il criterio fornisce un metodo amministrativo per il recupero dei dati crittografati da BitLocker per evitare la perdita di dati a causa della mancanza di informazioni chiave. Il rapporto di stato e l'attività di ripristino delle chiavi verranno inviate automaticamente e silenziosamente alla posizione del server di report configurata.</p>
<p>Se non si configura o se si disabilita questa impostazione, le informazioni relative al ripristino della chiave non verranno salvate e il rapporto di stato e l'attività di ripristino delle chiavi non verranno segnalate al server. Quando questa impostazione è impostata su <strong> password di ripristino e pacchetto di tasti </strong> , la password di ripristino e il pacchetto di chiave verranno automaticamente e silenziosamente configurati nel percorso del server di recupero chiavi configurato.</p></li>
<li><p><strong>Immettere il controllo della frequenza di stato del client in pochi minuti </strong> . Questa impostazione del criterio gestisce la frequenza con cui il client controlla i criteri e lo stato di protezione di BitLocker nel computer client. Questo criterio gestisce anche la frequenza con cui lo stato di conformità del client viene salvato nel server. Il client controlla i criteri e lo stato di protezione di BitLocker nel computer client e esegue anche il backup della chiave di ripristino client in corrispondenza della frequenza configurata.</p>
<p>Imposta questa frequenza in base al requisito impostato dalla tua società per verificare con frequenza lo stato di conformità del computer e con quale frequenza eseguire il backup della chiave di ripristino del client.</p></li>
<li><p><strong>Endpoint del servizio Segnalazione stato di MBAM </strong> . È necessario configurare questa impostazione per abilitare la gestione della crittografia BitLocker client di MBAM. Immettere una posizione di endpoint simile all'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare i criteri di esenzione dall'utente</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri consente di configurare un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono che indicherà a un utente di richiedere un'esenzione dalla crittografia BitLocker.</p>
<p>Se si abilita questa impostazione per i criteri e si fornisce un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono, gli utenti vedranno una finestra di dialogo che fornisce istruzioni su come richiedere un'esenzione dalla protezione di BitLocker. Per altre informazioni sull'abilitazione delle esenzioni crittografiche di BitLocker per gli utenti, vedere <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> come gestire le esenzioni di crittografia degli utenti di BitLocker </a> .</p>
<p>Se si disattiva o non si configura questa impostazione per i criteri, le istruzioni per la richiesta di esenzione non verranno presentate agli utenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>L'esenzione dall'utente è gestita per utente, non per computer. Se più utenti accedono allo stesso computer e un utente non è esonerato, il computer verrà crittografato.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare il programma Analisi utilizzo software</p></td>
<td align="left"><p>Questa impostazione dei criteri consente di configurare il modo in cui gli utenti di MBAM possono partecipare al programma Analisi utilizzo software. Questo programma raccoglie informazioni sull'hardware del computer e su come gli utenti usano MBAM senza interrompere il lavoro. Le informazioni consentono a Microsoft di identificare le caratteristiche di MBAM da migliorare. Microsoft non userà queste informazioni per identificare o contattare gli utenti di MBAM.</p>
<p>Se si abilita questa impostazione, gli utenti saranno in grado di partecipare al programma Analisi utilizzo software.</p>
<p>Se si disabilita questa impostazione, gli utenti non saranno in grado di partecipare al programma Analisi utilizzo software.</p>
<p>Se non si configura questa impostazione, gli utenti avranno l'opzione di partecipare al programma Analisi utilizzo software.</p></td>
</tr>
</tbody>
</table>



## Definizioni di criteri di unità fisse


In questa sezione vengono illustrate le definizioni dei criteri di unità fisse per l'amministrazione e il monitoraggio di Microsoft BitLocker disponibili nel nodo GPO seguente: criteri di **configurazione dei computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)** \\ **unità fissa**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazione di criteri suggeriti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni di crittografia unità dati fisse</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione dei criteri consente di gestire se le unità fisse devono essere crittografate.</p>
<p>Se il volume del sistema operativo è necessario per essere crittografato, selezionare l' <strong> opzione Abilita l'unità dati fissa di sblocco automatico </strong> .</p>
<p>Quando si Abilita questo criterio, non è necessario disabilitare la <strong> configurazione dell'uso della password per i criteri delle unità dati fisse, </strong> a meno che non sia consentito o richiesto l'uso di auto-Unlock per le unità dati fisse.</p>
<p>Se si richiede l'uso di sblocco automatico per le unità dati fisse, è necessario configurare i volumi del sistema operativo da crittografare.</p>
<p>Se si abilita questa impostazione per i criteri, gli utenti devono inserire tutte le unità fisse in protezione BitLocker e le unità verranno crittografate.</p>
<p>Se non si configura questa impostazione, gli utenti non sono tenuti a inserire unità fisse in protezione BitLocker. Se applichi questo criterio dopo aver crittografato le unità dati fisse, l'agente MBAM decrittografa le unità fisse crittografate.</p>
<p>Se si disabilita questa impostazione, gli utenti non saranno in grado di inserire le unità dati fisse in protezione BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negare l'accesso in scrittura alle unità fisse non protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri determina se la protezione di BitLocker è necessaria affinché le unità fisse siano scrivibili in un computer. Questa impostazione dei criteri viene applicata quando si attiva BitLocker.</p>
<p>Quando il criterio non è configurato, tutte le unità dati fisse nel computer vengono montate con l'accesso in lettura e scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso a dischi fissi protetti da BitLocker da versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire alle unità fisse con il file system FAT di essere sbloccate e visualizzate nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Quando il criterio è abilitato o non configurato, le unità fisse formattate con il file system FAT possono essere sbloccate e il loro contenuto può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2. Questi sistemi operativi hanno accesso in sola lettura alle unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità fisse formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità fisse</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Usare questo criterio per specificare se è necessaria una password per sbloccare le unità dati fisse protette da BitLocker.</p>
<p>Se si abilita questa impostazione, gli utenti possono configurare una password che soddisfi i requisiti definiti. BitLocker consentirà agli utenti di sbloccare un'unità con qualsiasi protezione disponibile nell'unità.</p>
<p>Queste impostazioni vengono applicate quando si attiva BitLocker, non quando si sblocca un volume.</p>
<p>Se si disabilita questa impostazione, gli utenti non possono usare una password.</p>
<p>Quando il criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati fissa </strong> , selezionare <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password desiderata </strong> .</p>
<p>Se si disabilita questa impostazione, gli utenti non possono usare una password.</p>
<p>Se non si configura questa impostazione, le password saranno supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperati i dischi fissi protetti da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando il criterio non è configurato, l'agente di ripristino dei dati di BitLocker è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory. MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Definizioni dei criteri unità del sistema operativo


Questa sezione descrive le definizioni dei criteri di unità del sistema operativo per l'amministrazione e il monitoraggio di Microsoft BitLocker disponibili nel nodo GPO seguente: criteri di **configurazione dei computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)** \\ **drive del sistema operativo**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazione di criteri suggeriti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni di crittografia unità del sistema operativo</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione dei criteri consente di gestire se l'unità del sistema operativo deve essere crittografata.</p>
<p>Per una maggiore sicurezza, è consigliabile disabilitare le impostazioni dei criteri seguenti nelle <strong> impostazioni di sistema/Power Management/Sleep </strong> quando si abilitano con TPM + PIN Protector:</p>
<ul>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (collegato)</p></li>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (sulla batteria)</p></li>
</ul>
<p>Se si esegue Microsoft Windows 8 o versione successiva e si vuole usare BitLocker in un computer senza un TPM, selezionare la casella di <strong> controllo Consenti BitLocker senza un TPM compatibile </strong> . In questa modalità è necessaria una password per l'avvio. Se si dimentica la password, è necessario usare una delle opzioni di ripristino di BitLocker per accedere all'unità.</p>
<p>In un computer con un TPM compatibile è possibile usare due tipi di metodi di autenticazione all'avvio per ottenere una protezione aggiuntiva per i dati crittografati. All'avvio del computer, può usare solo il TPM per l'autenticazione oppure può richiedere l'immissione di un PIN (Personal Identification Number).</p>
<p>Se si abilita questa impostazione per i criteri, gli utenti devono inserire l'unità del sistema operativo in protezione BitLocker e l'unità verrà crittografata.</p>
<p>Se si disabilita questo criterio, gli utenti non saranno in grado di inserire l'unità del sistema operativo in protezione BitLocker. Se si applica questo criterio dopo che l'unità del sistema operativo è stata crittografata, l'unità verrà decrittografata.</p>
<p>Se non si configura questo criterio, non è necessario che l'unità del sistema operativo venga inserita in protezione BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare il profilo di convalida della piattaforma TPM</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di configurare il modo in cui l'hardware di sicurezza TPM in un computer protegge la chiave di crittografia BitLocker. Questa impostazione non si applica se nel computer non è presente un TPM compatibile o se BitLocker è già stato attivato con la protezione TPM.</p>
<p>Quando questa impostazione di criterio non è configurata, il TPM usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui è possibile recuperare le unità del sistema operativo protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando questo criterio non è configurato, l'agente recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Definizioni dei criteri unità rimovibili


Questa sezione descrive le definizioni dei criteri di unità rimovibili per l'amministrazione e il monitoraggio di Microsoft BitLocker disponibili nel nodo GPO seguente: criteri di **configurazione del computer** \\ **Policies** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **drive rimovibile**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome criterio</th>
<th align="left">Panoramica e impostazione di criteri suggeriti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controllare l'uso di BitLocker su unità rimovibili</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questo criterio Controlla l'uso di BitLocker su unità dati rimovibili.</p>
<p>Abilitare l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> per consentire agli utenti di eseguire la configurazione guidata BitLocker in un'unità dati rimovibile.</p>
<p>Consentire agli <strong> utenti di sospendere e decrittografare l'opzione BitLocker in unità dati rimovibili </strong> per consentire agli utenti di rimuovere la crittografia unità BitLocker dall'unità o di sospendere la crittografia durante l'esecuzione della manutenzione.</p>
<p>Quando questo criterio è abilitato e l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> è selezionata, il client mbam Salva le informazioni di ripristino sulle unità rimovibili nel server di ripristino di mbam Key e consente agli utenti di recuperare l'unità se la password è perduta.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negare l'accesso in scrittura alle unità rimovibili non protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire solo l'accesso in scrittura alle unità protette da BitLocker.</p>
<p>Quando questo criterio è abilitato, tutte le unità dati rimovibili nel computer richiedono la crittografia prima che sia consentita l'accesso in scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso alle unità rimovibili protette da BitLocker dalle versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire alle unità fisse che il file system FAT venga sbloccato e visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Quando questo criterio non è configurato, le unità dati rimovibili formattate con il file system FAT possono essere sbloccate nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2 e il loro contenuto può essere visualizzato. Questi sistemi operativi hanno accesso in sola lettura alle unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità rimovibili formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità dati rimovibili</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per configurare la protezione con password sulle unità dati rimovibili.</p>
<p>Quando questo criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e che richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, è possibile abilitare questo criterio e verificare <strong> Richiedi password per l'unità dati rimovibili </strong> , selezionare <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password preferita </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperate le unità rimovibili protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Se impostato su <strong> non configurato </strong> , l'agente di recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Prerequisiti per la distribuzione di MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)









