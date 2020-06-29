---
title: Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0
description: Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804227"
---
# Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0


La gestione dei client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker richiede l'applicazione di impostazioni di criteri di gruppo personalizzate. In questo argomento vengono illustrate le opzioni dei criteri disponibili per l'oggetto Criteri di gruppo quando si usa MBAM per gestire la crittografia unità BitLocker nell'organizzazione.

**Importante**  
MBAM non usa le impostazioni GPO predefinite per la crittografia unità BitLocker di Windows. Se le impostazioni predefinite sono abilitate, possono causare un comportamento conflittuale. Per abilitare MBAM per la gestione di BitLocker, è necessario definire le impostazioni dei criteri GPO dopo l'installazione del modello di criteri di gruppo di MBAM.



Dopo aver installato il modello dei criteri di gruppo di MBAM, è possibile visualizzare e modificare le impostazioni dei criteri GPO personalizzati di MBAM che consentono a MBAM di gestire la crittografia BitLocker dell'organizzazione. Il modello di criteri di gruppo di MBAM deve essere installato in un computer in grado di eseguire la console Gestione criteri di gruppo o la tecnologia MDOP avanzata per la gestione dei criteri di gruppo. Per modificare quindi il GPO applicabile, aprire GPMC o Advanced Group Policy Management e quindi passare al nodo GPO seguente: **Configurazione computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**.

Il nodo GPO MDOP MBAM (BitLocker Management) contiene rispettivamente quattro impostazioni di criteri globali e quattro nodi di impostazione GPO figlio. Le quattro impostazioni dei criteri globali del GPO sono: gestione client, unità fisse, unità del sistema operativo e unità rimovibile. Le sezioni seguenti includono definizioni di criteri e impostazioni dei criteri suggerite per pianificare i requisiti per l'impostazione di criteri GPO di MBAM.

**Nota**  
Per altre informazioni sulla configurazione delle impostazioni GPO minime consigliate per consentire a MBAM di gestire la crittografia BitLocker, vedere [come modificare le impostazioni del GPO di mbam 1,0](how-to-edit-mbam-10-gpo-settings.md).



## Definizioni di criteri globali


Questa sezione descrive le definizioni dei criteri globali di mbam, che possono essere trovate nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**.

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


In questa sezione vengono illustrate le definizioni dei criteri di gestione dei client per mbam, disponibile nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **Client Management**.

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
<li><p><strong>Endpoint del servizio di recupero e hardware di MBAM </strong> . Questa è la prima impostazione di criteri che è necessario configurare per abilitare la gestione della crittografia BitLocker client di MBAM. Per questa impostazione, immettere la posizione dell'endpoint simile all'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration e Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selezionare informazioni di ripristino di BitLocker da archiviare </strong> . Questa impostazione dei criteri consente di configurare il servizio di recupero chiavi per eseguire il backup delle informazioni di ripristino di BitLocker. Consente inoltre di configurare il servizio di segnalazione dello stato per la raccolta dei report di conformità e controllo. Il criterio fornisce un metodo amministrativo per il recupero dei dati crittografati da BitLocker per evitare perdite di dati dovute alla mancanza di informazioni chiave. Il rapporto di stato e l'attività di ripristino delle chiavi verranno inviate automaticamente e silenziosamente alla posizione del server di report configurata.</p>
<p>Se non si configura o se si disabilita questa impostazione, le informazioni relative al ripristino della chiave non verranno salvate e il rapporto di stato e l'attività di ripristino delle chiavi non verranno segnalate al server. Quando questa impostazione è impostata su <strong> password di ripristino e pacchetto di tasti </strong> , la password di ripristino e il pacchetto di chiave verranno automaticamente e silenziosamente configurati nel percorso del server di recupero chiavi configurato.</p></li>
<li><p><strong>Immettere il client che controlla la frequenza dello stato in minuti </strong> . Questa impostazione del criterio gestisce la frequenza con cui il client controlla i criteri di protezione di BitLocker e lo stato nel computer client. Questo criterio gestisce anche la frequenza con cui lo stato di conformità del client viene salvato nel server. Il client controlla i criteri e lo stato di protezione di BitLocker nel computer client e esegue anche il backup della chiave di ripristino client in corrispondenza della frequenza configurata.</p>
<p>Imposta questa frequenza in base al requisito stabilito dalla tua società per verificare con quante volte si controlla lo stato di conformità del computer e con quale frequenza eseguire il backup della chiave di ripristino del client.</p></li>
<li><p><strong>Endpoint del servizio Segnalazione stato di MBAM </strong> . Questa è la seconda impostazione di criteri che è necessario configurare per abilitare la gestione della crittografia BitLocker client di MBAM. Per questa impostazione, immettere la posizione dell'endpoint usando l'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. SVC </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Consentire il controllo della compatibilità hardware</p></td>
<td align="left"><p>Configurazione consigliata: <strong> abilitata</strong></p>
<p>Questa impostazione consente di gestire la verifica della compatibilità hardware prima di abilitare la protezione BitLocker sulle unità dei computer client MBAM.</p>
<p>È consigliabile abilitare questa opzione per i criteri se l'organizzazione ha hardware o computer meno recenti che non supportano il TPM (Trusted Platform Module). Se uno di questi criteri è vero, abilitare la verifica della compatibilità hardware per verificare che MBAM venga applicato solo ai modelli di computer che supportano BitLocker. Se tutti i computer dell'organizzazione supportano BitLocker, non è necessario distribuire la compatibilità hardware ed è possibile impostare questo criterio su <strong> non configurato </strong> .</p>
<p>Se si abilita questa impostazione, il modello del computer viene convalidato con l'elenco compatibilità hardware una volta ogni 24 ore, prima che il criterio consenta la protezione di BitLocker in un'unità del computer.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Prima di abilitare questa impostazione, verificare di avere configurato l'impostazione dell' <strong> endpoint di servizio hardware e ripristino </strong> di mbam nelle <strong> Opzioni di configurazione dei criteri di servizi mbam </strong> .</p>
</div>
<div>

</div>
<p>Se si disattiva o non si configura l'impostazione di questo criterio, il modello di computer non viene convalidato rispetto all'elenco compatibilità hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare i criteri di esenzione dall'utente</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri consente di configurare un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono che indicherà a un utente di richiedere un'esenzione dalla crittografia BitLocker.</p>
<p>Se si abilita questa impostazione per i criteri e si specifica un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono, gli utenti vedranno una finestra di dialogo con le istruzioni su come richiedere un'esenzione dalla protezione di BitLocker. Per altre informazioni su come abilitare le esenzioni per la crittografia BitLocker per gli utenti, vedere <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> come gestire le esenzioni di crittografia di BitLocker dell'utente </a> .</p>
<p>Se si disattiva o non si configura l'impostazione di questo criterio, le istruzioni su come applicare una richiesta di esenzione non verranno presentate agli utenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>L'esenzione dall'utente è gestita per utente, non per computer. Se più utenti accedono allo stesso computer e un utente non è esonerato, il computer verrà crittografato.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Definizioni di criteri di unità fisse


Questa sezione descrive le definizioni dei criteri di unità fisse per mbam, che si trova nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**  \\  **unità fissa**.

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
<td align="left"><p>Configurazione consigliata: <strong> abilitata </strong> e selezionare la <strong> casella di controllo Attiva unità dati fisse di sblocco automatico </strong> se è necessario crittografare il volume del sistema operativo.</p>
<p>Questa impostazione consente di controllare se crittografare o meno le unità fisse.</p>
<p>Quando si Abilita questo criterio, non disabilitare la <strong> configurazione dell'uso della password per i criteri delle unità dati fisse </strong> .</p>
<p>Se la <strong> casella di controllo Abilita l'auto-sblocco dei dati fissi </strong> è selezionata, il volume del sistema operativo deve essere crittografato.</p>
<p>Se si abilita questa impostazione, gli utenti devono inserire tutte le unità fisse in protezione BitLocker, in modo da crittografare le unità.</p>
<p>Se non si configura questo criterio o se si disabilita questo criterio, gli utenti non sono tenuti a inserire unità fisse in protezione BitLocker.</p>
<p>Se si disattiva questo criterio, l'agente MBAM decrittografa eventuali unità fisse crittografate.</p>
<p>Se non è necessario crittografare il volume del sistema operativo, deselezionare la <strong> casella di controllo attiva l'unità dati fissa di sblocco automatico </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negare l'autorizzazione "Scrivi" alle unità fisse che non sono protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione dei criteri determina se la protezione di BitLocker è necessaria per le unità fisse in un computer in modo che siano scrivibili. Questa impostazione dei criteri viene applicata quando si attiva BitLocker.</p>
<p>Quando il criterio non è configurato, tutte le unità fisse nel computer vengono montate con le autorizzazioni di lettura/scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso a dischi fissi protetti da BitLocker da versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per sbloccare e visualizzare le unità fisse formattate con il file system FAT (file allocation table) nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Questi sistemi operativi hanno le autorizzazioni di sola lettura per le unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità fisse formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità fisse</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per configurare la protezione con password in unità fisse.</p>
<p>Quando il criterio non è configurato, le password saranno supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati fissa </strong> , selezionare <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password desiderata </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperati i dischi fissi protetti da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando questo criterio non è configurato, l'agente di recupero dati di BitLocker è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory. MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Definizioni dei criteri unità del sistema operativo


Questa sezione descrive le definizioni dei criteri di unità del sistema operativo per mbam, disponibile nel nodo GPO seguente: **configurazione del computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **drive del sistema operativo**.

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
<p>Questa impostazione dei criteri determina se l'unità del sistema operativo verrà crittografata.</p>
<p>Configurare questo criterio per eseguire le operazioni seguenti:</p>
<ul>
<li><p>Applicare la protezione BitLocker per l'unità del sistema operativo.</p></li>
<li><p>Configurare l'utilizzo del PIN per usare un PIN TPM (Trusted Platform Module) per la protezione del sistema operativo.</p></li>
<li><p>Configurare i pin di avvio avanzati per consentire caratteri come lettere maiuscole e minuscole e numeri. MBAM non supporta l'uso di simboli e spazi per i PIN avanzati, anche se BitLocker supporta simboli e spazi.</p></li>
</ul>
<p>Se si abilita questa impostazione, è necessario che gli utenti proteggano l'unità del sistema operativo tramite BitLocker.</p>
<p>Se non si configura o se si disattiva l'impostazione, gli utenti non sono tenuti a proteggere l'unità del sistema operativo tramite BitLocker.</p>
<p>Se si disattiva questo criterio, l'agente MBAM decrittografa il volume del sistema operativo se è crittografato.</p>
<p>Quando è abilitata, questa impostazione del criterio richiede agli utenti di proteggere il sistema operativo tramite la protezione BitLocker e l'unità è crittografata. In base ai requisiti di crittografia, è possibile selezionare il metodo di protezione per l'unità del sistema operativo.</p>
<p>Per i requisiti di sicurezza più elevati, usare TPM + PIN, consentire i PIN avanzati e impostare la lunghezza minima del PIN su otto caratteri.</p>
<p>Quando questo criterio è abilitato con TPM + PIN Protector, è possibile considerare la possibilità di disabilitare i criteri seguenti in <strong> </strong>  /  <strong> </strong>  /  <strong> Impostazioni Sleep di Power Management </strong> :</p>
<ul>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (collegato)</p></li>
<li><p>Consentire stati di standby (S1-S3) durante il sonno (sulla batteria)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare il profilo di convalida della piattaforma TPM</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Questa impostazione consente di configurare il modo in cui l'hardware di sicurezza TPM in un computer protegge la chiave di crittografia BitLocker. Questa impostazione non si applica se il computer non ha un TPM compatibile o se BitLocker ha già abilitato la protezione TPM.</p>
<p>Quando questo criterio non è configurato, il TPM usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere come recuperare le unità del sistema operativo protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando questo criterio non è configurato, l'agente di recupero dati è consentita e le informazioni di ripristino non vengono sostenute in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Definizioni dei criteri unità rimovibili


Questa sezione descrive le definizioni dei criteri di unità rimovibili per mbam, disponibile nel nodo GPO seguente: **configurazione del computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **drive rimovibile**.

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
<p>Abilitare l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> per consentire agli utenti di eseguire la configurazione guidata di BitLocker in un'unità dati rimovibile.</p>
<p>Consentire agli <strong> utenti di sospendere e decrittografare l'opzione BitLocker in unità dati rimovibili </strong> per consentire agli utenti di rimuovere la crittografia unità BitLocker dall'unità o di sospendere la crittografia durante l'esecuzione della manutenzione.</p>
<p>Quando questo criterio è abilitato e l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> è selezionata, il client mbam Salva le informazioni di ripristino sulle unità rimovibili nel server di ripristino di mbam Key e consente agli utenti di recuperare l'unità se la password è perduta.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Rifiutare le autorizzazioni di scrittura per le unità rimovibili non protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per consentire le autorizzazioni di sola scrittura per le unità protette da BitLocker.</p>
<p>Quando questo criterio è abilitato, tutte le unità dati rimovibili nel computer richiedono la crittografia prima che siano consentite le autorizzazioni di scrittura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consentire l'accesso alle unità rimovibili protette da BitLocker dalle versioni precedenti di Windows</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per sbloccare e visualizzare le unità fisse formattate con il file System (FAT) nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p>
<p>Questi sistemi operativi hanno le autorizzazioni di sola lettura per le unità protette da BitLocker.</p>
<p>Quando il criterio è disabilitato, le unità rimovibili formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare l'uso della password per le unità dati rimovibili</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>Abilitare questo criterio per configurare la protezione con password sulle unità dati rimovibili.</p>
<p>Quando questo criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e richiedono solo otto caratteri.</p>
<p>Per una maggiore sicurezza, è possibile abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati rimovibili </strong> , selezionare <strong> Richiedi complessità password </strong> e quindi impostare la <strong> lunghezza minima della password preferita </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scegliere il modo in cui possono essere recuperate le unità rimovibili protette da BitLocker</p></td>
<td align="left"><p>Configurazione consigliata: <strong> non configurata</strong></p>
<p>È possibile configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</p>
<p>Quando il criterio è impostato su <strong> non configurato </strong> , l'agente di recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</p>
<p>L'operazione MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Preparazione dell'ambiente per MBAM 1.0](preparing-your-environment-for-mbam-10.md)









