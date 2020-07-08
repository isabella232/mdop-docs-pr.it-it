---
title: Distribuire le funzionalità necessarie per UE-V 2.x
description: Distribuire le funzionalità necessarie per UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824666"
---
# Distribuire le funzionalità necessarie per UE-V 2.x


Tutte le distribuzioni Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 richiedono queste funzionalità

-   [Distribuire una posizione di archiviazione delle impostazioni](#ssl) accessibile agli utenti finali.

    Si tratta di una condivisione di rete standard che consente di archiviare e recuperare le impostazioni dell'utente.

-   [Scegliere il metodo di configurazione per UE-V](#config)

    La versione UE-V può essere distribuita e configurata usando strumenti di gestione comuni, tra cui criteri di gruppo, Configuration Manager o infrastruttura di gestione di Windows e PowerShell.

-   [Distribuire un agente UE-V](#agent) da installare in tutti i computer che sincronizzano le impostazioni.

    Questo monitora le applicazioni registrate e il sistema operativo per tutte le modifiche delle impostazioni e sincronizza le impostazioni tra i computer.

Gli argomenti in questa sezione illustrano come distribuire queste funzionalità.

## <a href="" id="ssl"></a>Distribuire una posizione di archiviazione delle impostazioni di UE-V


UE-V richiede una posizione in cui archiviare le impostazioni utente nei file di pacchetto delle impostazioni. È possibile configurare la posizione di archiviazione delle impostazioni in uno dei modi seguenti:

-   Creare un percorso di archiviazione delle impostazioni personalizzato

-   Usare Active Directory esistente per la posizione di archiviazione delle impostazioni

Se non si crea una posizione di archiviazione delle impostazioni, l'agente UE-V utilizzerà Active Directory (AD) per impostazione predefinita.

**Nota**  
Per quanto riguarda la [pianificazione delle prestazioni e della capacità](https://technet.microsoft.com/library/dn458932.aspx#capacity) e per ridurre i problemi di latenza della rete, creare posizioni di archiviazione delle impostazioni nelle stesse reti locali in cui risiedono i computer degli utenti. È consigliabile 20 MB di spazio su disco per ogni utente per la posizione di archiviazione delle impostazioni.



### Creare una posizione di archiviazione delle impostazioni di UE-V

Prima di definire la posizione di archiviazione delle impostazioni, è necessario creare una directory radice con autorizzazioni di lettura/scrittura per gli utenti che archiviano le impostazioni della condivisione. L'agente UE-V crea cartelle specifiche dell'utente nella directory radice.

La posizione di archiviazione delle impostazioni viene definita impostando l'opzione di configurazione SettingsStoragePath, che può essere configurata utilizzando uno di questi metodi:

-   Quando si [distribuisce l'agente UE-V](#agent) tramite un parametro della riga di comando o in uno script batch

-   Impostazioni di [criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)

-   Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) per UE-V

-   Dopo l'installazione dell'agente UE-V, usare [Windows PowerShell o Strumentazione gestione Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)

Il percorso deve trovarsi in un percorso UNC (Universal Naming Convention) del server e condividere. Ad esempio, **\\\\Server\\Settingsshare\\**. Questa opzione di configurazione supporta l'uso di variabili per abilitare scenari di sincronizzazione specifici. Ad esempio, puoi usare le `%username%\%computername%` variabili per mantenere l'esperienza delle impostazioni degli utenti finali in questi scenari:

-   Utenti finali che usano più computer fisici nell'organizzazione

-   Computer aziendali usati da più utenti finali

L'agente UE-V crea in modo dinamico un percorso di archiviazione delle impostazioni specifico dell'utente, con una cartella di sistema nascosta denominata `SettingsPackages` , in base all'impostazione di configurazione di **SettingsStoragePath**. L'agente legge e scrive le impostazioni in questa posizione, come definito dai modelli di posizione delle impostazioni UE-V registrati.

**Le impostazioni di UE-V sono determinate dalla regola "ultima scrittura WINS":** Se la posizione di archiviazione delle impostazioni è uguale per l'utente con più computer gestiti, un agente UE-V legge e scrive nella posizione delle impostazioni in modo indipendente dagli agenti in uso in altri computer. Le ultime impostazioni e i valori scritti sono quelli applicati quando l'agente successivo legge il percorso di archiviazione delle impostazioni.

**Distribuire il percorso di archiviazione delle impostazioni:** Seguire questa procedura per definire la posizione di archiviazione delle impostazioni invece di usare il servizio Active Directory esistente. È consigliabile limitare l'accesso alla condivisione di archiviazione delle impostazioni agli utenti che lo richiedono, come illustrato nelle tabelle seguenti.

**Per distribuire la condivisione di rete UE-V**

1.  Creare un nuovo gruppo di sicurezza per gli utenti di UE-V.

2.  Creare una nuova cartella nel computer situato in posizione centrale in cui sono archiviati i pacchetti di impostazioni UE-V e quindi concedere agli utenti di UE-V l'accesso con le autorizzazioni di gruppo alla cartella. L'amministratore che supporta UE-V deve disporre delle autorizzazioni per questa cartella condivisa.

3.  Impostare le autorizzazioni SMB (Server Message Block) di livello di condivisione seguenti per la cartella della posizione di archiviazione delle impostazioni.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Autorizzazioni consigliate</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
    <td align="left"><p>Controllo completo</p></td>
    </tr>
    </tbody>
    </table>



4.  Impostare le autorizzazioni di file system NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Autorizzazioni consigliate</strong></th>
    <th align="left"><strong>Cartella</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creatore/proprietario</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Solo sottocartelle e file</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
    <td align="left"><p>Cartella di elenco/dati letti, creare cartelle/accodare dati</p></td>
    <td align="left"><p>Solo questa cartella</p></td>
    </tr>
    </tbody>
    </table>



Con questa configurazione, l'agente UE-V crea e protegge una cartella Settingspackage mentre viene eseguita nel contesto dell'utente e concede a ogni utente l'autorizzazione per creare cartelle per l'archiviazione delle impostazioni. Gli utenti ricevono il controllo completo nella cartella Settingspackage, mentre altri utenti non possono accedervi.

**Nota**  
Se si crea la condivisione di archiviazione delle impostazioni in un computer che esegue un sistema operativo Windows Server, configurare UE-V per verificare che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni. Per abilitare questa ulteriore sicurezza, specificare questa impostazione nell'editor del registro di sistema di Windows Server:

1.  Aggiungere una chiave **reg \ _DWORD** del registro di sistema denominata **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Impostare il valore della chiave del registro di sistema su *1*.



### Usare Active Directory con UE-V 2. x

L'agente UE-V usa Active Directory (AD) per impostazione predefinita se una posizione di archiviazione delle impostazioni non è altrimenti definita. In questi casi, l'agente UE-V crea dinamicamente la cartella di archiviazione delle impostazioni sotto la radice della Home directory di ogni utente. Tuttavia, se è stata configurata un'impostazione di directory personalizzata in AD, viene usata invece quella directory.

## <a href="" id="config"></a>Scegliere il metodo di configurazione per UE-V 2. x


Si vuole individuare il metodo di configurazione che verrà usato per gestire la versione UE-V dopo la distribuzione, poiché questo sarà il metodo di configurazione usato per distribuire l'agente UE-V. In genere, si tratta del metodo di configurazione già usato nell'ambiente, ad esempio Windows PowerShell o Configuration Manager.

Puoi configurare la versione UE-V prima, durante o dopo l'installazione dell'agente UE-V, a seconda del metodo di configurazione che usi.

-   [Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)**:** è possibile usare l'infrastruttura di criteri di gruppo esistente per configurare UE-v prima o dopo la distribuzione di agenti UE-v. Il modello ADMX di criteri di gruppo di UE-V consente la gestione centralizzata delle opzioni di configurazione dell'agente UE-V comuni e include le impostazioni per la configurazione della sincronizzazione UE-V.

    **Installazione dei modelli ADMX di criteri di gruppo di UE-V:** I modelli ADMX di criteri di gruppo per la versione UE-V configurano le impostazioni di sincronizzazione per l'agente UE-V e consentono la gestione centralizzata delle impostazioni di configurazione dell'agente UE-V comuni usando un'infrastruttura di criteri di gruppo esistente.

    I sistemi operativi supportati per il controller di dominio che distribuisce gli oggetti Criteri di gruppo includono i seguenti:

    Windows Server2008 R2

    Windows Server 2012 e Windows Server 2012 R2

-   [Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** il pacchetto di configurazione UE-v consente di usare la caratteristica Impostazioni conformità di System Center Configuration Manager 2012 SP1 o versioni successive per applicare configurazioni coerenti tra i siti in cui sono installati i sistemi UE-v e Configuration Manager.

-   [Windows PowerShell e WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** è possibile usare comandi con script per Windows PowerShell e Strumentazione gestione Windows (WMI) per modificare le configurazioni dopo l'installazione dell'agente UE-V.

    **Nota**  
    La modifica del registro di sistema può causare la perdita di dati o il computer non risponde. Ti consigliamo di usare altri metodi di configurazione.



-   **Installazione da riga di comando o da script batch:** I parametri usati quando si [distribuisce l'agente UE-v](#agent) configurano molte impostazioni UE-v. I sistemi di distribuzione elettronica del software, ad esempio System Center 2012 Configuration Manager, usano questi parametri per configurare i loro client quando distribuiscono e installano il software dell'agente UE-V.

## <a href="" id="agent"></a>Distribuire l'agente UE-V 2. x


L'agente UE-V è il nucleo di una distribuzione UE-V e deve essere eseguito in ogni computer che USA UE-V per sincronizzare le impostazioni dell'applicazione e di Windows.

**File di installazione dell'agente UE-V:** Un singolo file di installazione, AgentSetup.exe, installa l'agente UE-V nei sistemi operativi 32 bit e 64 bit. Vengono inoltre forniti AgentSetupx86.msi o AgentSetupx64.msi file di Windows Installer specifici dell'architettura e, poiché sono più piccoli, potrebbero semplificare le distribuzioni di agente. I [parametri della riga di comando per il programma di installazione di AgentSetup.exe](#params) sono supportati anche per l'installazione di Windows Installer.

**Importante**  
Durante l'installazione o la disinstallazione dell'agente UE-V, è possibile usare il file AgentSetup.exe o il &lt; &gt; file Arch. msi di AgentSetup, ma non entrambi. Lo stesso file deve essere usato per disinstallare l'agente UE-V usato per installare l'agente UE-V.



### Per distribuire l'agente UE-V

Puoi usare i metodi seguenti per distribuire l'agente UE-V:

-   Un sistema di soluzioni Electronic Software Distribution (ESD), ad esempio Configuration Manager, che può installare un file di Windows Installer (con estensione msi).

-   Uno script di installazione che fa riferimento al file di Windows Installer (con estensione msi) archiviato centralmente in una condivisione.

-   Programma di installazione eseguito manualmente nel computer.

Usare la procedura seguente per distribuire l'agente UE-V da una condivisione di rete.

**Per installare e configurare l'agente UE-V da una condivisione di rete**

1.  Eseguire il file di installazione dell'agente UE-V AgentSetup.exe in una condivisione di rete a cui gli utenti hanno l'autorizzazione di lettura.

2.  Distribuire uno script nei computer degli utenti che installano l'agente UE-V. Lo script deve specificare la posizione di archiviazione delle impostazioni.

**Opzioni di distribuzione:** Assicurarsi di usare il formato di variabile corretto quando si installa l'agente UE-V. La tabella seguente contiene esempi di opzioni di distribuzione per l'uso dei file AgentSetup.exe o Windows Installer (con estensione msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo di distribuzione</strong></th>
<th align="left"><strong>Descrizione della distribuzione</strong></th>
<th align="left"><strong>Esempio</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prompt dei comandi</p></td>
<td align="left"><p>Quando si installa l'agente UE-V al prompt dei comandi, usare il <em> formato di variabile% ^ nomeutente% </em> . Se sono necessarie le virgolette a causa di spazi nel percorso di archiviazione delle impostazioni, usare un file di script batch per la distribuzione.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script batch</p></td>
<td align="left"><p>Quando si installa l'agente UE-V da un file di script batch, usare il formato di variabile%% <em> nomeutente%% </em> . Se si usa questo metodo di installazione, è necessario sfuggire alla variabile con i caratteri%%. Senza questo carattere, lo script espande la <em> variabile username </em> al momento dell'installazione, invece che in fase di esecuzione, che causa l'uso di una singola posizione di archiviazione delle impostazioni per tutti gli utenti.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell</p></td>
<td align="left"><p>Quando si installa l'agente UE-V da un prompt di Windows PowerShell o uno script di Windows PowerShell, usare il <em> formato variabile% nomeutente% </em> .</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuzione elettronica del software, ad esempio distribuzione della distribuzione del software di Configuration Manager</p></td>
<td align="left"><p>Quando si installa l'agente UE-V tramite Configuration Manager, usare il <em> formato di variabile ^% nomeutente ^% </em> .</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**Nota**  
L'installazione dell'agente UE-V richiede i diritti di amministratore e il computer richiede un riavvio prima che l'agente UE-V possa essere eseguito.



### <a href="" id="params"></a>Parametri della riga di comando per la distribuzione di agenti UE-V

I parametri della riga di comando dell'agente UE-V sono i seguenti.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parametro della riga di comando</strong></th>
<th align="left"><strong>Definizione</strong></th>
<th align="left"><strong>Note</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help o/h o/?</p></td>
<td align="left"><p>Visualizza la finestra di dialogo utilizzo AgentSetup.exe.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica il percorso UNC (Universal Naming Convention) che definisce la posizione in cui sono archiviate le impostazioni.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>È necessario specificare un SettingsStoragePath in UE-V 2,1 e in UE-V 2,1 SP1. Puoi impostare la stringa AdHomePath per specificare che viene usato il percorso Home dell'utente&#39;s Active Directory. Ad esempio: <code>SettingsStoragePath = \share\path|AdHomePath</code>.</p>
<p>In UE-V 2,0 è possibile abbandonare SettingsStoragePath blank per usare invece il percorso Home di Active Directory.</p>
</div>
<div>

</div>
<p>vengono accettate le variabili di ambiente% nomeutente% o% nomecomputer%. Gli script possono richiedere variabili di escape.</p>
<p><strong>Impostazione predefinita </strong> : &lt; None&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>Ottiene il valore SettingsStoragePath dal registro di sistema durante l'installazione.</p></td>
<td align="left"><p>Al prompt dei comandi digitare l'esempio seguente per imporre a UE-V di usare il percorso Home di Active Directory invece di un UNC specifico.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.</p></td>
<td align="left"><p>Obbligatorio solo per i modelli di posizione delle impostazioni personalizzate</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : vero</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Specifica il metodo di sincronizzazione da usare.</p></td>
<td align="left"><p>SyncProvider | Nessuno</p>
<p><strong>Impostazione predefinita </strong> : SyncProvider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Specifica il numero di millisecondi che il computer attende prima del timeout quando recupera le impostazioni utente dalla posizione di archiviazione delle impostazioni.</p></td>
<td align="left"><p><strong>Impostazione predefinita </strong> : 2000 millisecondi</p>
<p>(attendere fino a 2 secondi)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Specifica se la sincronizzazione UE-V è abilitata o disabilitata.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : vero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Specifica una dimensione del file del pacchetto di impostazioni in byte quando l'agente UE-V segnala che i file superano la soglia.</p></td>
<td align="left"><p>&lt;dimensioni&gt;</p>
<p><strong>Default </strong> : None (nessuna soglia di avviso)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Specifica l'impostazione per la partecipazione al programma Analisi utilizzo software. Se impostato su <strong> true </strong> , le informazioni sul programma di installazione vengono caricate nel sito Microsoft Customer Experience Improvement Program. Se impostato su <strong> false </strong> , non vengono caricate informazioni.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : false</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoRestart</p></td>
<td align="left"><p>Supporta il differimento del riavvio del computer dopo l'installazione dell'agente UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>Consente di impostare una cartella di installazione diversa per l'agente UE-V o per il generatore di UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>Consente alla configurazione di accettare l'opzione da includere nel programma Microsoft Update.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>Consente l'installazione di UE-V in modo invisibile all'utente. Questa operazione deve essere impostata su <strong> true </strong> per installare la versione UE-v in modo silenzioso e ignorare il requisito che l'utente accetti le condizioni di licenza UE-v. Se impostato su <strong> false </strong> o Left Empty, l'utente riceverà un messaggio di errore e non verrà installato UE-V.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Questo parametro è obbligatorio per l'installazione di UE-V in modo invisibile all'utente.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NORESTART</p></td>
<td align="left"><p>Impedisce un riavvio obbligatorio dopo l'installazione dell'agente UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Aggiornare l'agente UE-V

Gli aggiornamenti per il software dell'agente UE-V vengono forniti tramite Microsoft Update. Puoi distribuire gli aggiornamenti di agente UE-V tramite sistemi di infrastruttura ESD (Enterprise Software Distribution).

Durante l'aggiornamento di un agente UE-V, è possibile aggiornare il gruppo predefinito dei modelli di posizione delle impostazioni per le applicazioni Microsoft comuni e le impostazioni di Windows.

### Aggiornare l'agente UE-V 2. x

L'agente UE-V 2. x introduce molte nuove funzionalità e modifica la modalità e il momento in cui l'agente carica il contenuto nella condivisione di archiviazione delle impostazioni. Il processo di aggiornamento automatizza queste modifiche. Per aggiornare l'agente UE-V, eseguire il pacchetto di installazione dell'agente UE-V (AgentSetup.exe, AgentSetupx86.msi o AgentSetupx64.msi) nei computer degli utenti.

**Nota**  
Quando si esegue l'aggiornamento dell'agente UE-V, è necessario usare lo stesso tipo di programma di installazione (file exe o pacchetto MSI) che ha installato il precedente agente UE-V. Ad esempio, usa la AgentSetup.exe UE-V 2 per aggiornare gli agenti UE-V 1,0 installati tramite AgentSetup.exe.



Le configurazioni seguenti vengono mantenute quando viene eseguito il programma di installazione dell'agente:

-   Percorso di archiviazione delle impostazioni

-   Impostazioni del Registro di sistema

-   Attività pianificate (le impostazioni di intervallo vengono reimpostate sui valori predefiniti)

**Nota**  
Un computer con i modelli di posizione delle impostazioni di UE-V 2. x registrati negli errori di registrazione dell'agente UE-V 1,0 nel registro eventi di Windows.



È possibile usare Microsoft System Center 2012 Configuration Manager o un altro strumento di distribuzione del software aziendale per automatizzare e distribuire l'aggiornamento dell'agente UE-V.

**Raccomandazioni:** È consigliabile aggiornare tutti gli agenti UE-V 1,0 in un ambiente di elaborazione, ma non è necessario. I modelli di posizione delle impostazioni di UE-V 2. x possono interagire con un agente UE-V 1,0 perché condividono solo le impostazioni dal percorso di archiviazione delle impostazioni. È tuttavia consigliabile trasferire le distribuzioni a una versione di un singolo agente per semplificare la gestione e supportare UE-V.

### Ripristinare l'agente UE-V dopo un aggiornamento non riuscito

Dopo aver tentato una delle operazioni seguenti, potrebbe verificarsi un errore:

-   Eseguire l'aggiornamento da UE-V 1,0 a UE-V 2

-   Eseguire l'aggiornamento a una versione più recente di Windows, ad esempio da Windows 7 a Windows 8 o da Windows 8 a Windows 8,1.

-   Disinstallare l'agente dopo l'aggiornamento dell'agente UE-V

Per risolvere eventuali problemi, provare a ripristinare l'agente UE-V immettendo questo comando al prompt dei comandi nel computer in cui è installato l'agente.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

Puoi quindi riprovare il processo di disinstallazione o l'aggiornamento installando la versione più recente dell'agente UE-V.






## Argomenti correlati


[Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









