---
title: Informazioni su MBAM 2.5
description: Informazioni su MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824215"
---
# Informazioni su MBAM 2.5


Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 offre un'interfaccia amministrativa semplificata per la crittografia unità BitLocker. BitLocker offre una protezione avanzata per il furto di dati o l'esposizione ai dati per i computer persi o rubati. BitLocker crittografa tutti i dati archiviati nei volumi e nelle unità del sistema operativo Windows e nelle unità dati configurate.

## Panoramica di MBAM


MBAM 2,5 ha le caratteristiche seguenti:

-   Consente agli amministratori di automatizzare il processo di crittografia dei volumi nei computer client in tutta l'organizzazione.

-   Consente agli addetti alla sicurezza di determinare rapidamente lo stato di conformità dei singoli computer o anche dell'organizzazione stessa.

-   Fornisce Reporting centralizzato e gestione hardware con Microsoft System Center Configuration Manager.

-   Riduce il carico di lavoro nell'help desk per aiutare gli utenti finali con le richieste di chiavi di ripristino e PIN di BitLocker.

-   Consente agli utenti finali di recuperare i dispositivi crittografati in modo indipendente usando il portale self-service.

-   Consente agli addetti alla sicurezza di controllare facilmente l'accesso per recuperare le informazioni chiave.

-   Consente agli utenti di Windows Enterprise di continuare a lavorare ovunque con la garanzia che i loro dati aziendali siano protetti.

MBAM applica le opzioni dei criteri di crittografia di BitLocker impostate per l'organizzazione, monitora la conformità dei computer client con tali criteri e segnala lo stato di crittografia dei computer dell'organizzazione e dell'individuo. Inoltre, MBAM consente di accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambiano i record del BIOS o del boot.

I gruppi seguenti potrebbero essere interessati all'uso di MBAM per gestire BitLocker:

-   Amministratori, professionisti IT per la sicurezza e responsabili della conformità che hanno la responsabilità di garantire che i dati riservati non vengano divulgati senza autorizzazione

-   Amministratori responsabili della sicurezza dei computer in uffici remoti o succursali

-   Amministratori responsabili per i computer client che eseguono Windows

**Nota**  BitLocker non è spiegato in dettaglio in questa documentazione di MBAM. Per altre informazioni, vedere [Panoramica della crittografia unità BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>Novità di MBAM 2,5


Questa sezione descrive le nuove caratteristiche di MBAM 2,5.

### Supporto per Microsoft SQL Server 2014

MBAM aggiunge il supporto per Microsoft SQL Server 2014, oltre allo stesso software supportato nelle versioni precedenti di MBAM.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> Modelli di criteri di gruppo di MBAM scaricati separatamente

I modelli dei criteri di gruppo di MBAM devono essere scaricati separatamente dall'installazione di MBAM. Nelle versioni precedenti di MBAM, il programma di installazione di MBAM includeva un modello di criteri di MBAM, che conteneva gli oggetti Criteri di gruppo specifici per MBAM che definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker. Questi GPO sono stati rimossi dal programma di installazione di MBAM. Ora scarichi i GPO da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation prima di iniziare l'installazione del client mbam. È possibile copiare i modelli di criteri di gruppo in qualsiasi server o workstation in cui è in esecuzione una versione supportata del sistema operativo Windows Server o Windows.

**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente. Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di crittografia unità BitLocker.

 

I file di modello che è necessario copiare in un server o una workstation sono i seguenti:

-   BitLockerManagement. adml

-   BitLockerManagement. admx

-   BitLockerUserManagement. adml

-   BitLockerUserManagement. admx

Copiare i file del modello nella posizione più adatta alle proprie esigenze. Per i file specifici della lingua, che devono essere copiati in una cartella specifica della lingua, è necessaria la console Gestione criteri di gruppo per visualizzare i file.

- Per installare i file del modello localmente in un server o una workstation, copiare i file in uno dei percorsi seguenti.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo di file</th>
  <th align="left">Percorso del file</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>lingua indipendente (con estensione ADMX)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>linguaggio specifico (con estensione adml)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (ad esempio, il file specifico della lingua inglese degli Stati Uniti verrà archiviato in <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

- Per rendere i modelli disponibili per tutti gli amministratori dei criteri di gruppo in un dominio, copiare i file in una delle posizioni seguenti in un controller di dominio.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo di file</th>
  <th align="left">Posizione del file del controller di dominio</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>Lingua indipendente (con estensione ADMX)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>Linguaggio specifico (con estensione adml)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (ad esempio, il file specifico della lingua inglese degli Stati Uniti verrà archiviato in <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-us)</p></td>
  </tr>
  </tbody>
  </table>

     

Per altre informazioni sui file di modello, vedere [gestione dettagliata dei file ADMX di criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=392818).

### Possibilità di applicare criteri di crittografia nel sistema operativo e nelle unità dati fisse

MBAM 2.5 consente di applicare criteri di crittografia nel sistema operativo e nelle unità dati fisse per i computer dell'organizzazione e limitare il numero di giorni in cui gli utenti finali possono richiedere il rinvio del requisito per conformarsi ai criteri di crittografia di MBAM.

Per consentire la configurazione dell'imposizione dei criteri di crittografia, è stata aggiunta una nuova impostazione di criteri di gruppo, denominata impostazioni per l'applicazione di criteri di crittografia, per le unità di sistema operativo e le unità dati fisse. Questo criterio è descritto nella tabella seguente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Impostazione di Criteri di gruppo</th>
<th align="left">Descrizione</th>
<th align="left">Nodo Criteri di gruppo usato per configurare questa impostazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni per l'applicazione dei criteri di crittografia (unità del sistema operativo)</p></td>
<td align="left"><p>Per questa impostazione, usare l'opzione <strong> Configura il numero di giorni del periodo di tolleranza per la mancata conformità per le unità del sistema operativo </strong> per configurare un periodo di tolleranza.</p>
<p>Il periodo di tolleranza specifica il numero di giorni in cui gli utenti finali possono rinviare la conformità con i criteri di MBAM per l'unità del sistema operativo dopo che l'unità è stata rilevata come non conforme.</p>
<p>Dopo la scadenza del periodo di tolleranza configurato, gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione.</p>
<p>Se è necessaria l'interazione dell'utente, ad esempio se si usa il modulo TPM (Trusted Platform Module) + PIN o con una password Protector, viene visualizzata una finestra di dialogo e gli utenti non possono chiuderlo finché non vengono fornite le informazioni richieste. Se il Protector è solo TPM, la crittografia inizia immediatamente in background senza l'input dell'utente.</p>
<p>Gli utenti non possono richiedere esenzioni tramite la crittografia guidata BitLocker. Devono invece contattare il proprio help desk o usare qualsiasi processo che l'organizzazione usa per le richieste di esenzione.</p></td>
<td align="left"><p>Criteri di configurazione del computer &gt; &gt; modelli amministrativi di &gt; Windows Components &gt; MDOP mbam (BitLocker Management) &gt; drive del sistema operativo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni per l'applicazione dei criteri di crittografia (unità dati fisse)</p></td>
<td align="left"><p>Per questa impostazione, usare l'opzione <strong> Configura il numero di giorni di periodo di tolleranza per le unità fisse per la </strong> configurazione di un periodo di tolleranza.</p>
<p>Il periodo di tolleranza specifica il numero di giorni in cui gli utenti finali possono rinviare la conformità con i criteri di MBAM per l'unità fissa dopo che l'unità è stata rilevata come non conforme.</p>
<p>Il periodo di tolleranza inizia quando l'unità fissa viene determinata come non conforme. Se si usa il comando di sblocco automatico, il criterio non verrà applicato finché l'unità del sistema operativo non è conforme. Tuttavia, se non si usa l'opzione di sblocco automatico, la crittografia dell'unità dati fisse può iniziare prima che l'unità del sistema operativo sia completamente crittografata.</p>
<p>Dopo la scadenza del periodo di tolleranza configurato, gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione. Se è necessaria l'interazione dell'utente, viene visualizzata una finestra di dialogo e gli utenti non possono chiuderlo finché non vengono fornite le informazioni richieste.</p></td>
<td align="left"><p>Criteri di configurazione del computer &gt; &gt; modelli amministrativi di &gt; Windows Components &gt; MDOP mbam (Gestione BitLocker) &gt; unità fissa</p></td>
</tr>
</tbody>
</table>

 

### Possibilità di specificare un URL nella configurazione guidata unità BitLocker per selezionare i criteri di sicurezza

Una nuova impostazione di criteri di gruppo, **specificare l'URL del collegamento ai criteri di sicurezza**, consente di configurare un URL che verrà presentato agli utenti finali come collegamento denominato **criteri di sicurezza aziendale**. Questo link verrà visualizzato quando MBAM richiede agli utenti di crittografare un volume.

Se si abilita questa impostazione, è possibile configurare l'URL per il collegamento ai **criteri di sicurezza aziendali** . Se si disattiva o non si configura questa impostazione per i criteri, il collegamento **criteri di sicurezza aziendali** non viene visualizzato agli utenti.

La nuova impostazione di criteri di gruppo è disponibile nel nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management) &gt; Client Management**.

### Supporto per le chiavi di ripristino conformi FIPS

MBAM 2.5 supporta le chiavi di ripristino di BitLocker conformi alla Federal Information Processing Standard (FIPS) nei dispositivi che gestiscono il sistema operativo Windows 8.1. La chiave di ripristino non è conforme FIPS nelle versioni precedenti di Windows. Questo miglioramento migliora il processo di ripristino delle unità in organizzazioni che richiedono la conformità FIPS perché consente agli utenti finali di usare il portale self-service o il sito Web di amministrazione e monitoraggio (Help desk) per recuperare i propri dischi se dimenticano il PIN o la password o si bloccano i propri computer. La nuova funzionalità di conformità FIPS non si estende ai protettori delle password.

Per abilitare la conformità FIPS nell'organizzazione, è necessario configurare le impostazioni dei criteri di gruppo FIPS (Federal Information Processing Standard). Per istruzioni sulla configurazione, vedere [impostazioni dei criteri di gruppo di BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

Per i computer client che eseguono i sistemi operativi Windows8 o Windows7 senza l' [hotfix installato di BitLocker](https://support.microsoft.com/kb/3015477), gli amministratori IT continueranno a usare la protezione DRA per gli agenti di recupero dati in ambienti conformi allo standard FIPS. Per informazioni su DRA, vedere [uso di agenti di recupero dati con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

Vedere [pacchetto hotfix 2 per l'amministrazione e il monitoraggio di bitlocker 2,5](https://support.microsoft.com/kb/3015477) per scaricare e installare i computer hotfix per Windows 7 e Windows 8.

### Supporto per distribuzioni ad alta disponibilità

MBAM supporta i seguenti scenari ad alta disponibilità, oltre alle topologie di integrazione standard di due server e gestione configurazione:

-   Gruppi di disponibilità di SQL Server AlwaysOn

-   Clustering di SQL Server

-   Bilanciamento del carico di rete (NLB)

-   Mirroring di SQL Server

-   Backup del servizio Copia Shadow del volume (VSS)

Per altre informazioni su queste funzionalità, vedere [pianificazione per MBAM 2,5 disponibilità elevata](planning-for-mbam-25-high-availability.md).

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>La gestione dei ruoli per il sito Web di amministrazione e monitoraggio è cambiata

In MBAM 2.5 è necessario creare gruppi di sicurezza in Active Directory Domain Services (aggiunge) per gestire i ruoli che prevedono i diritti di accesso al sito Web di amministrazione e monitoraggio. I ruoli consentono agli utenti che si trovano in gruppi di sicurezza specifici di eseguire attività diverse nel sito Web, ad esempio la visualizzazione di report o l'assistenza agli utenti finali per recuperare unità crittografate. Nelle versioni precedenti di MBAM i ruoli venivano gestiti tramite gruppi locali.

In MBAM 2.5, il termine "Roles" sostituisce il termine "ruoli di amministratore", usato nelle versioni precedenti di MBAM. Inoltre, in MBAM 2.5 il ruolo "MBAM System Administrators" è stato rimosso.

Nella tabella seguente sono elencati i gruppi di sicurezza che è necessario creare in servizi di dominio Active Directory. Puoi usare qualsiasi nome per i gruppi di sicurezza.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ruolo</th>
<th align="left">Diritti di accesso per questo ruolo nel sito Web di amministrazione e monitoraggio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>Consente di accedere alle aree Gestisci TPM e recupero unità del sito Web di amministrazione e monitoraggio di MBAM. Gli utenti che hanno accesso a queste aree devono compilare tutti i campi quando usano un'area qualsiasi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>Consente di accedere ai report nel sito Web amministrazione e monitoraggio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Advanced helpdesk utenti</p></td>
<td align="left"><p>Consente di accedere a tutte le aree del sito Web di amministrazione e monitoraggio. Gli utenti di questo gruppo devono immettere solo la chiave di ripristino, non il dominio e il nome utente dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità. Se un utente è un membro del gruppo di utenti di MBAM helpdesk e il gruppo di utenti dell'helpdesk Advanced di mbam, le autorizzazioni di gruppo degli utenti del helpdesk avanzato di mbam eseguono l'override delle autorizzazioni del gruppo utenti di MBAM helpdesk.</p></td>
</tr>
</tbody>
</table>

 

Dopo aver creato i gruppi di sicurezza in Aggiungi, assegnare utenti e/o gruppi al gruppo di sicurezza appropriato per consentire il livello di accesso corrispondente al sito Web di amministrazione e monitoraggio. Per consentire agli utenti con ogni ruolo di accedere al sito Web di amministrazione e monitoraggio, è necessario specificare ogni gruppo di sicurezza anche quando si configura il sito Web di amministrazione e monitoraggio.

### Cmdlet di Windows PowerShell per la configurazione delle funzionalità di MBAM server

I cmdlet di Windows PowerShell per MBAM 2.5 consentono di configurare e gestire le caratteristiche del server MBAM. Ogni funzionalità include un cmdlet di Windows PowerShell corrispondente che puoi usare per abilitare o disabilitare le funzionalità o per ottenere informazioni sulla funzionalità.

Per i prerequisiti e i prerequisiti per l'uso di Windows PowerShell, vedere [configurazione delle funzionalità del server di MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

**Per caricare la Guida di MBAM 2,5 per i cmdlet di Windows PowerShell dopo l'installazione del software del server MBAM**

1.  Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).

2.  Digitare **Update-Guida-modulo Microsoft. mbam**.

La Guida di Windows PowerShell per MBAM è disponibile nei formati seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato della Guida di Windows PowerShell</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</p></td>
<td align="left"><p>Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni della sezione precedente su come caricare la Guida di Windows PowerShell per MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>In TechNet come pagine Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nell'area download come file di Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nell'area download come file PDF</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### Supporto per pin ASCII e avanzati e possibilità di impedire i caratteri sequenziali e ripetuti

**Consenti PIN avanzati per l'impostazione di criteri di gruppo di avvio**

L'impostazione di criteri di gruppo consente di configurare i **PIN avanzati per l'avvio**e di stabilire se usare i pin di avvio avanzati con BitLocker. I pin di avvio avanzati consentono agli utenti di immettere qualsiasi tasto su una tastiera completa, incluse lettere maiuscole e minuscole, simboli, numeri e spazi. Se si abilita questa impostazione per i criteri, tutti i nuovi PIN di avvio di BitLocker impostati saranno PIN avanzati. Se si disattiva o non si configura questa impostazione dei criteri, non è possibile usare i PIN avanzati.

Non tutti i computer supportano l'immissione di PIN avanzati nell'ambiente PXE (pre-boot Execution Environment). Prima di abilitare questa impostazione di criteri di gruppo per l'organizzazione, eseguire un controllo di sistema durante il processo di configurazione di BitLocker per verificare che il BIOS del computer supporti l'uso della tastiera completa in PXE. Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

**Richiedere la casella di controllo pin solo ASCII**

L'impostazione **Consenti i PIN avanzati per i criteri di gruppo di avvio** contiene anche una casella di controllo **Richiedi solo i pin ASCII** . Se i computer dell'organizzazione non supportano l'uso della tastiera completa in PXE, è possibile abilitare l'impostazione Consenti i **PIN avanzati per** i criteri di gruppo di avvio e quindi selezionare la casella di controllo **Richiedi solo i pin ASCII** per richiedere che i PIN avanzati usino solo caratteri ASCII stampabili.

**Applicazione forzata di caratteri non sequenziali e non ripetitivi**

MBAM 2.5 impedisce agli utenti finali di creare pin costituiti da numeri ripetitivi (ad esempio 1111) o numeri sequenziali (ad esempio 1234). Se gli utenti finali provano a immettere una password che contiene tre o più numeri ripetuti o sequenziali, la crittografia guidata unità BitLocker Visualizza un messaggio di errore e impedisce agli utenti di immettere un PIN con i caratteri vietati.

### Aggiunta del certificato DRA al report di conformità del computer BitLocker

Un nuovo tipo di protezione, il certificato DRA (Data Recovery Agent), è stato aggiunto al report conformità computer di BitLocker in Gestione configurazione. Questo tipo di protezione si applica alle unità del sistema operativo e viene visualizzato nella sezione **volumi computer** nella colonna **tipi di protezione** .

### Supporto per distribuzioni di supporto per più insiemi di strutture

MBAM 2,5 supporta i seguenti tipi di distribuzioni con più foreste:

-   Singola foresta con un singolo dominio

-   Singola foresta con un solo albero e più domini

-   Foresta singola con più alberi e spazi dei nomi disgiunti

-   Più foreste in una topologia di foresta centrale

-   Più foreste in una topologia di foresta di risorse

Non è disponibile alcun supporto per la migrazione delle foreste (passando da singola a multipla, multipla a singola, risorsa in tutta la foresta e così via) o aggiornamento o downgrade.

I prerequisiti per la distribuzione di MBAM nelle distribuzioni con più foreste sono i seguenti:

-   La foresta deve essere in uso nelle versioni supportate di Windows Server.

-   È necessario un trust bidirezionale o unidirezionale. I trust unidirezionali richiedono che il dominio del server si fidi del dominio del client. In altre parole, il dominio del server è puntato sul dominio del client.

### Supporto di MBAM client per dischi rigidi crittografati

MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667. Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata. Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .

## Come ottenere le tecnologie MDOP


MBAM fa parte del Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte del programma Microsoft Software Assurance. Per altre informazioni sul programma Microsoft Software Assurance e su come acquisire il MDOP, vedere [come si ottiene MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## <a href="" id="---------mbam-2-5-release-notes"></a> Note sulla versione di MBAM 2,5


Per altre informazioni e notizie aggiornate che non sono incluse in questa documentazione, vedere note sulla [versione per MBAM 2,5](release-notes-for-mbam-25.md).

## Hai un suggerimento per MBAM?
- Inviare il proprio feedback [qui](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Argomenti correlati


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

 

 





