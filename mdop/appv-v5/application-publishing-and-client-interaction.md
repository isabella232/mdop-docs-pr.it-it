---
title: Pubblicazione delle applicazioni e interazione dei client
description: Pubblicazione delle applicazioni e interazione dei client
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805950"
---
# Pubblicazione delle applicazioni e interazione dei client


Questo articolo fornisce informazioni tecniche sulle comuni operazioni client App-V e la loro integrazione con il sistema operativo locale.

-   [File di pacchetto App-V creati dal sequencer](#bkmk-appv-pkg-files-list)

-   [Cosa contiene il file appv?](#bkmk-appv-file-contents)

-   [Percorsi di archiviazione dei dati client App-V](#bkmk-files-data-storage)

-   [Registro del pacchetto](#bkmk-pkg-registry)

-   [Comportamento dell'archivio pacchetti App-V](#bkmk-pkg-store-behavior)

-   [Registro di sistema e dati mobili](#bkmk-roaming-reg-data)

-   [Gestione del ciclo di vita dell'applicazione client App-V](#bkmk-clt-app-lifecycle)

-   [Integrazione dei pacchetti App-V](#bkmk-integr-appv-pkgs)

-   [Elaborazione della configurazione dinamica](#bkmk-dynamic-config)

-   [Assembly affiancati](#bkmk-sidebyside-assemblies)

-   [Registrazione client](#bkmk-client-logging)

Per altre informazioni di riferimento, vedere [pagina di download delle risorse della documentazione di Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-pkg-files-list"></a>File di pacchetto App-V creati dal sequencer


Sequencer crea pacchetti App-V e produce un'applicazione virtualizzata. Il processo di sequenziazione crea i file seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>. AppV</p></td>
<td align="left"><ul>
<li><p>Il file del pacchetto principale, che contiene le informazioni relative agli asset e allo stato acquisiti dal processo di sequenziazione.</p></li>
<li><p>Architettura del file di pacchetto, informazioni sulla pubblicazione e registro di sistema in una maschera in formato token che può essere riapplicata a un computer e a un utente specifico al momento del recapito.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. MSI</p></td>
<td align="left"><p>Wrapper di distribuzione eseguibile che puoi usare per distribuire file con estensione appv manualmente o usando una piattaforma di distribuzione di terze parti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>File usato per personalizzare i parametri di pubblicazione predefiniti per tutte le applicazioni in un pacchetto distribuito globalmente a tutti gli utenti in un computer in cui è in uso il client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>File usato per personalizzare i parametri di pubblicazione per tutte le applicazioni in un pacchetto distribuito a un utente specifico in un computer in cui è in uso il client App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Riepilogo dei messaggi risultante dal processo di sequenziazione, inclusi i driver omessi, i file e le posizioni del registro di sistema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>. TAXI</p></td>
<td align="left"><p><em>Facoltativo: </em> file di accelerazione pacchetto usato per ricostruire automaticamente un pacchetto di applicazione virtuale sequenziato in precedenza.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Facoltativo: </em> file di modello sequencer usato per mantenere le impostazioni di Sequencer comunemente riutilizzate.</p></td>
</tr>
</tbody>
</table>

 

Per informazioni sulla sequenziazione, vedere [Guida alla sequenziazione di Application Virtualization 5,0](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-file-contents"></a>Cosa contiene il file appv?


Il file appv è un contenitore che archivia i file XML e non XML insieme in una singola entità. Questo file è compilato dal formato AppX, che si basa sullo standard Open Packaging Conventions (OPC).

Per visualizzare il contenuto del file appv, creare una copia del pacchetto e quindi rinominare il file copiato in un'estensione ZIP.

Il file appv contiene la cartella e i file seguenti, che vengono usati durante la creazione e la pubblicazione di un'applicazione virtuale:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Root</p></td>
<td align="left"><p>Cartella di file</p></td>
<td align="left"><p>Directory che contiene il file System per l'applicazione virtualizzata acquisita durante la sequenziazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. XML</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Elenco dei tipi di contenuto principali nel file appv (ad esempio DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Layout del file appv, che usa gli elementi file, Block e BlockMap che consentono la posizione e la convalida dei file nel pacchetto App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Metadati per il pacchetto che contiene le informazioni necessarie per l'aggiunta, la pubblicazione e l'avvio del pacchetto. Include i punti di estensione (associazioni di tipi di file e tasti di scelta rapida) e i nomi e i GUID associati al pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Elenco dei file acquisiti durante la sequenziazione, inclusi gli attributi (ad esempio, directory, file, directory opache, directory vuote e nomi lunghi e brevi).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Informazioni sul computer di sequenziazione (versione del sistema operativo, versione di Internet Explorer, versione di .NET Framework) ed elaborazione (aggiornamento, versione del pacchetto).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry. dat</p></td>
<td align="left"><p>File DAT</p></td>
<td align="left"><p>Chiavi del registro di sistema e valori acquisiti durante il processo di sequenziazione per il pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>File XML</p></td>
<td align="left"><p>Elenco di file per il blocco delle caratteristiche primarie e di pubblicazione. Il blocco di funzionalità di pubblicazione contiene i file ICO e le parti necessarie di file (EXE e DLL) per la pubblicazione del pacchetto. Quando è presente, il blocco di funzionalità principale include i file che sono stati ottimizzati per lo streaming durante il processo di sequenziazione.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>Percorsi di archiviazione dei dati client App-V


Il client App-V esegue le attività per garantire che le applicazioni virtuali vengano eseguite correttamente e funzioni come le applicazioni installate localmente. Il processo di apertura ed esecuzione delle applicazioni virtuali richiede il mapping dal file system virtuale e dal registro di sistema per garantire che l'applicazione abbia i componenti necessari di un'applicazione tradizionale prevista dagli utenti. Questa sezione descrive gli asset necessari per eseguire applicazioni virtuali ed elenca la posizione in cui App-V archivia gli asset.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Percorso</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Archivio pacchetti</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Percorso predefinito per i file di pacchetto di sola lettura</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catalogo computer</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contiene documenti di configurazione per computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catalogo utenti</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contiene documenti di configurazione per utente</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup di scelta rapida</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Archivia i punti di integrazione precedenti che consentono di ripristinare il pacchetto Unpublish</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Copia su scrittura (mucca) roaming</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Posizione di roaming scrivibile per la modifica del pacchetto</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copia in scrittura (mucca) local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Posizione di non roaming scrivibile per la modifica del pacchetto</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registro di sistema del computer</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene informazioni sullo stato del pacchetto, tra cui ORSAE per computer o pacchetti pubblicati globalmente (hive macchina)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registro utenti</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene informazioni sullo stato del pacchetto utente, tra cui ORSAE</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classi del registro di sistema degli utenti</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contiene informazioni aggiuntive sullo stato del pacchetto utente</p></td>
</tr>
</tbody>
</table>

 

I dettagli aggiuntivi per la tabella sono disponibili nella sezione seguente e in tutto il documento.

### Archivio pacchetti

Il client App-V gestisce gli asset delle applicazioni montati nell'archivio pacchetti. Questo percorso di archiviazione predefinito è `%ProgramData%\App-V` , ma è possibile configurarlo durante o dopo la configurazione usando il `Set-AppVClientConfiguration` comando di PowerShell, che modifica il registro di sistema locale ( `PackageInstallationRoot` valore sotto la `HKLM\Software\Microsoft\AppV\Client\Streaming` chiave). L'archivio pacchetti deve trovarsi in un percorso locale nel sistema operativo client. I singoli pacchetti vengono archiviati nell'archivio pacchetti in sottodirectory denominati per il GUID del pacchetto e il GUID della versione.

Esempio di percorso di un'applicazione specifica:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Per modificare la posizione predefinita dell'archivio pacchetti durante l'installazione, vedere [come distribuire il client App-V](how-to-deploy-the-app-v-client-gb18030.md).

### Archivio contenuto condiviso

Se il client App-V è configurato in modalità archivio contenuto condiviso, non vengono scritti dati su disco quando si verifica un errore di flusso, il che significa che i pacchetti richiedono spazio minimo su disco locale (dati di pubblicazione). L'uso di meno spazio su disco è molto utile in ambienti VDI, in cui l'archiviazione locale può essere limitata e lo streaming delle applicazioni da un percorso di rete ad alte prestazioni, ad esempio un SAN, è preferibile. Per altre informazioni sulla modalità di archiviazione del contenuto condivisa, vedere <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Nota**  Il computer e l'archivio pacchetti devono essere posizionati in un'unità locale, anche quando si usano configurazioni di archivio contenuto condiviso per il client App-V.

 

### Cataloghi di pacchetti

Il client App-V gestisce i due percorsi basati su file seguenti:

-   **Cataloghi (utente e computer).**

-   **Posizioni del registro di sistema** -dipende dalla modalità di destinazione del pacchetto per la pubblicazione. È disponibile un catalogo (archivio dati) per il computer e un catalogo per ogni singolo utente. Il catalogo computer archivia le informazioni globali applicabili a tutti gli utenti o a qualsiasi utente e il catalogo dell'utente archivia le informazioni applicabili a un utente specifico. Il catalogo è una raccolta di configurazioni dinamiche e file manifesto; sono disponibili dati discreti sia per file che per il registro di sistema per versione del pacchetto. 

### Catalogo computer

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Archivia i documenti del pacchetto disponibili per gli utenti nel computer, quando i pacchetti vengono aggiunti e pubblicati. Tuttavia, se un pacchetto è "globale" in fase di pubblicazione, le integrazioni sono disponibili per tutti gli utenti.</p>
<p>Se un pacchetto non è globale, le integrazioni vengono pubblicate solo per utenti specifici, ma esistono ancora risorse globali modificate e visibili a chiunque nel computer client (ad esempio, la directory del pacchetto si trova in un percorso del disco condiviso).</p>
<p>Se un pacchetto è disponibile per un utente nel computer (globale o non globale), il manifesto viene archiviato nel catalogo computer. Quando un pacchetto viene pubblicato globalmente, esiste un file di configurazione dinamica archiviato nel catalogo computer; di conseguenza, la determinazione del fatto che un pacchetto sia globale viene definita in base alla presenza di un file di criteri (file UserDeploymentConfiguration) nel catalogo computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione di archiviazione predefinita</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Questa posizione non è uguale alla posizione dell'archivio pacchetti. L'archivio pacchetti è la copia dorata o incontaminata dei file di pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>File nel catalogo computer</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (pacchetto pubblicato globalmente)</p></li>
<li><p>UserDeploymentConfiguration.xml (pacchetto pubblicato globalmente)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione del catalogo computer aggiuntivo, usata quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p>La posizione seguente è in aggiunta al percorso specifico del pacchetto menzionato sopra:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>File aggiuntivi nel catalogo computer quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (gruppo di connessioni pubblicato globalmente)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Catalogo utenti

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Creato durante il processo di pubblicazione. Contiene le informazioni usate per la pubblicazione del pacchetto e usate anche all'avvio per verificare che un pacchetto venga provisionato a un utente specifico. Creato in un percorso di roaming e include informazioni di pubblicazione specifiche per l'utente.</p>
<p>Quando un pacchetto viene pubblicato per un utente, il file di criteri viene archiviato nel catalogo utenti. Contemporaneamente, nel catalogo utente viene archiviata anche una copia del manifesto. Quando viene rimosso un diritto del pacchetto per un utente, i file di pacchetto rilevanti vengono rimossi dal catalogo utenti. Guardando il catalogo degli utenti, un amministratore può visualizzare la presenza di un file di configurazione dinamica, che indica che il pacchetto è autorizzato per l'utente.</p>
<p>Per gli utenti mobili, il catalogo utente deve essere in una posizione comune o in roaming per mantenere il comportamento legacy di App-V di destinazione degli utenti per impostazione predefinita. I diritti e i criteri sono collegati a un utente, non a un computer, in modo che debbano eseguire il roaming con l'utente dopo il provisioning.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione di archiviazione predefinita</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>File nel catalogo utenti</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml o UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Posizione del catalogo utenti aggiuntiva, usata quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p>La posizione seguente è in aggiunta al percorso specifico del pacchetto menzionato sopra:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>File aggiuntivo nel catalogo computer quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### Backup di scelta rapida

Durante il processo di pubblicazione, il client App-V consente di eseguire il backup di tutti i tasti di scelta rapida e i punti di integrazione di `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` questo supporto per consentire il ripristino di questi punti di integrazione con le versioni precedenti quando il pacchetto non è pubblicato.

### Copiare i file in scrittura

L'archivio pacchetti contiene una copia incontaminata dei file di pacchetto che sono stati trasmessi dal server di pubblicazione. Durante il normale funzionamento di un'applicazione App-V, l'utente o il servizio può richiedere modifiche ai file. Queste modifiche non vengono apportate nell'archivio pacchetti per mantenere la possibilità di ripristinare l'applicazione, che rimuove queste modifiche. Queste posizioni, denominate copia in scrittura (mucca), supportano le posizioni di roaming e non in roaming. La posizione in cui sono archiviate le modifiche dipende dal punto in cui l'applicazione è stata programmata per scrivere le modifiche in un'esperienza nativa.

### Roaming mucca

La posizione di roaming mucca descritta sopra memorizza le modifiche apportate ai file e alle directory che sono destinati al percorso tipico% AppData% o alla posizione di \\Users\\{username}\\AppData\\Roaming. Queste directory e file vengono quindi spostati in roaming in base alle impostazioni del sistema operativo.

### MUCCA locale

La posizione locale della mucca è simile alla posizione di roaming, ma le directory e i file non sono in roaming con altri computer, anche se è stato configurato il supporto per il roaming. La posizione locale COW descritta sopra memorizza le modifiche applicabili alle finestre tipiche e non la posizione% AppData%. Le directory elencate variano, ma ci saranno due posizioni per tutti i percorsi di Windows tipici, ad esempio AppData comuni e AppData comuni. La **S** indica la posizione con restrizioni quando il servizio virtuale richiede la modifica come utente elevato diverso dagli utenti connessi. La posizione non**S** archivia le modifiche basate sull'utente.

## <a href="" id="bkmk-pkg-registry"></a>Registro del pacchetto


Prima che un'applicazione possa accedere ai dati del registro di sistema del pacchetto, il client App-V deve rendere disponibili i dati del registro di sistema per le applicazioni. Il client App-V usa il registro di sistema reale come archivio di backup per tutti i dati del registro di sistema.

Quando viene aggiunto un nuovo pacchetto al client App-V, una copia del registro di sistema. Viene creato il file DAT dal pacchetto `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . Il nome del file è il GUID della versione con. Estensione DAT. Il motivo per cui viene eseguita questa copia consiste nel garantire che il file hive effettivo nel pacchetto non sia mai in uso, impedendo così la rimozione del pacchetto in un secondo momento.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry. dat dall'archivio pacchetti</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</strong></p></td>
</tr>
</tbody>
</table>

 

Quando la prima applicazione del pacchetto viene avviata nel client, il client fasi o copia il contenuto del file hive, ricreando i dati del registro di sistema in una posizione alternativa `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . I dati del registro di sistema a fasi includono due tipi distinti di dati del computer e dati utente. I dati del computer vengono condivisi in tutti gli utenti del computer. I dati degli utenti vengono inscenati per ogni utente in una posizione userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . I dati del computer vengono rimossi in definitiva al momento della rimozione del pacchetto e i dati dell'utente vengono rimossi in un'operazione di annullamento della pubblicazione da parte dell'utente.

### Staging del registro di sistema del pacchetto e organizzazione del registro di sistema Connection Group

Quando i gruppi di connessioni sono presenti, il processo precedente di staging del registro di sistema è vero, ma invece di avere un file hive da elaborare, ce ne sono più di uno. I file vengono elaborati nell'ordine in cui vengono visualizzati nel codice XML del gruppo di connessioni, con il primo autore che vince i conflitti.

Il registro di sistema a fasi viene mantenuto allo stesso modo del caso del singolo pacchetto. I dati del registro di sistema degli utenti a fasi rimangono per il gruppo di connessioni finché non vengono disabilitati; i dati del registro di sistema a fasi vengono rimossi nella rimozione dei gruppi di connessioni.

### Registro di sistema virtuale

Lo scopo del registro di sistema virtuale (ORSAE) consiste nel creare una singola visualizzazione unita del registro di sistema e del registro di sistema nativo delle applicazioni. Offre anche funzionalità di mucca (copy-on-Write), ovvero tutte le modifiche apportate al registro di sistema dal contesto di un processo virtuale vengono effettuate in una posizione di mucca separata. Questo significa che ORSAE deve combinare fino a tre posizioni separate del registro di sistema in una singola visualizzazione in base alle posizioni compilate nel registro di sistema COW- &gt; package- &gt; native. Quando viene eseguita una richiesta per i dati del registro di sistema verranno individuati in ordine fino a quando non vengono trovati i dati che richiedevano. Significato se c'è un valore archiviato in una posizione di mucca non procederà ad altre posizioni, tuttavia, se non ci sono dati nella posizione della mucca procederà al pacchetto e quindi alla posizione nativa finché non trova i dati appropriati.

### Posizioni del registro di sistema

Esistono due posizioni del registro dei pacchetti e due posizioni del gruppo di connessioni in cui il client App-V archivia le informazioni del registro di sistema, a seconda che il pacchetto venga pubblicato singolarmente o come parte di un gruppo di connessioni. Esistono tre posizioni di mucca per i pacchetti e tre per i gruppi di connessioni, che vengono creati e gestiti da ORSAE. Le impostazioni per i pacchetti e i gruppi di connessioni non sono condivise:

**ORSAE pacchetto singolo:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Percorso</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>MUCCA</strong></p></td>
<td align="left"><ul>
<li><p>Registry\Client\Packages\PkgGUID\REGISTRY computer (solo il processo di elevazione può scrivere)</p></li>
<li><p>Registry\Client\Packages\PkgGUID\REGISTRY utente (utente che si sposta in un altro elemento scritto in HKCU eccetto Software\Classes</p></li>
<li><p>Classes\Client\Packages\PkgGUID\REGISTRY del registro di sistema degli utenti (HKCU\Software\Classes scrive e HKLM per processi non elevati)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacchetto</strong></p></td>
<td align="left"><ul>
<li><p>Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine del computer</p></li>
<li><p>Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry del registro di sistema degli utenti</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Percorso del registro di sistema delle applicazioni native</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Gruppo di connessioni ORSAE:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Percorso</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>MUCCA</strong></p></td>
<td align="left"><ul>
<li><p>Registry\Client\PackageGroups\GrpGUID\REGISTRY computer (solo il processo di elevazione può scrivere)</p></li>
<li><p>Registry\Client\PackageGroups\GrpGUID\REGISTRY utente (qualsiasi elemento scritto in HKCU eccetto Software\Classes</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\REGISTRY del registro di sistema degli utenti</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacchetto</strong></p></td>
<td align="left"><ul>
<li><p>Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY del computer</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY del registro di sistema degli utenti</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Percorso del registro di sistema delle applicazioni native</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Esistono due posizioni della mucca per HKLM; processi sopraelevati e non elevati. I processi elevati scrivono sempre le modifiche HKLM alla mucca sicura in HKLM. I processi non elevati scrivono sempre le modifiche HKLM alla mucca non sicura in HKCU\\Software\\Classes. Quando un'applicazione legge le modifiche da HKLM, i processi elevati leggeranno le modifiche apportate dalla mucca sicura in HKLM. Letture non elevate da entrambi, che favoriscono prima le modifiche apportate alla mucca non sicura.

### Tasti pass-through

I tasti pass-through consentono a un amministratore di configurare determinati tasti in modo che possano essere letti solo dal registro di sistema nativo, ignorando le posizioni del pacchetto e della mucca. I percorsi di passaggio sono globali per il computer (non specifici del pacchetto) e possono essere configurati aggiungendo il percorso alla chiave, che deve essere considerato come pass-through per il valore **reg \ _MULTI \ _SZ** denominato **PassThroughPaths** della chiave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Qualsiasi chiave visualizzata in questo valore multistringa (e i relativi elementi figlio) verrà considerata come pass-through.

Le posizioni seguenti sono configurate come posizioni passate per impostazione predefinita:

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY \ _CURRENT \ _USER impostazioni \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies

Lo scopo delle chiavi pass-through consiste nel garantire che un'applicazione virtuale non scriva i dati del registro di sistema ORSAE necessari per le applicazioni non virtuali per l'operazione o l'integrazione riuscita. La chiave policy garantisce che le impostazioni basate su criteri di gruppo impostate dall'amministratore vengano usate e non per le impostazioni del pacchetto. La chiave AppModel è necessaria per l'integrazione con le applicazioni basate sull'interfaccia utente moderna di Windows. È consigliabile che le amministrazioni non modifichino i tasti pass-through predefiniti, ma in alcuni casi, in base al comportamento delle applicazioni, potrebbe essere necessario aggiungere ulteriori chiavi pass-through.

## <a href="" id="bkmk-pkg-store-behavior"></a>Comportamento dell'archivio pacchetti App-V


App-V 5 gestisce l'archivio dei pacchetti, ovvero la posizione in cui sono archiviati i file di asset espansi dal file AppV. Per impostazione predefinita, questa posizione è archiviata in%ProgramData%\\App-V ed è limitata in termini di funzionalità di archiviazione solo per spazio su disco gratuito. L'archivio pacchetti è organizzato dai GUID per il pacchetto e la versione come indicato nella sezione precedente.

### Aggiungere pacchetti

I pacchetti App-V vengono assegnati al computer con il client App-V. Il client App-V offre la gestione temporanea su richiesta. Durante la pubblicazione o un manuale Add-AppVClientPackage, la struttura dei dati viene compilata nell'archivio pacchetti (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). I file di pacchetto identificati nel blocco di pubblicazione definiti nella StreamMap.xml vengono aggiunti al sistema e le cartelle di primo livello e i file figlio sono in fase di esecuzione per garantire l'esistenza di asset applicazione corretti all'avvio.

### Installazione di pacchetti

I pacchetti possono essere caricati in modo esplicito usando PowerShell `Mount-AppVClientPackage` o usando l' **interfaccia utente del client App-V** per scaricare un pacchetto. Questa operazione carica completamente l'intero pacchetto nell'archivio pacchetti.

### Pacchetti di flusso

Il client App-V può essere configurato per modificare il comportamento predefinito del flusso. Tutti i criteri di flusso sono archiviati nella chiave del registro di sistema seguente: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . I criteri vengono impostati tramite il cmdlet di PowerShell `Set-AppvClientConfiguration` . I criteri seguenti si applicano allo streaming:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Criterio</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>In Windows 8 consente lo streaming su reti 3G e cellulari</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Specifica l'impostazione di caricamento in background:</p>
<p><strong>0 </strong> - disabilitato</p>
<p><strong>1 </strong> -solo pacchetti usati in precedenza</p>
<p><strong>2 </strong> -tutti i pacchetti</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>Cartella radice per l'archivio di pacchetti nel computer locale</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>L'override radice in cui devono essere trasmessi i pacchetti da</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Consente l'uso dell'archivio contenuto condiviso per gli scenari VDI</p></td>
</tr>
</tbody>
</table>

 

 

Queste impostazioni influiscono sul comportamento degli asset del pacchetto di App-V in streaming al client. Per impostazione predefinita, App-V Scarica solo gli asset necessari dopo il download dei blocchi di funzionalità primari e di pubblicazione iniziali. Esistono tre comportamenti specifici per lo streaming di pacchetti che devono essere spiegati:

-   Flusso di sfondo

-   Flusso ottimizzato

-   Errori di flusso

### Flusso di sfondo

Il cmdlet `Get-AppvClientConfiguration` di PowerShell può essere usato per determinare la modalità corrente per il flusso dello sfondo con l'impostazione AutoLoad e modificata con il cmdlet Set-AppvClientConfiguration o dal registro di sistema (chiave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming). Lo streaming in background è un'impostazione predefinita in cui l'impostazione autoload è impostata per il download dei pacchetti usati in precedenza. Il comportamento basato sull'impostazione predefinita (valore = 1) Scarica i blocchi di dati App-V in background dopo l'avvio dell'applicazione. Questa impostazione può essere disabilitata tutti insieme (valore = 0) o abilitata per tutti i pacchetti (valore = 2), indipendentemente dal fatto che siano stati avviati.

### Flusso ottimizzato

I pacchetti App-V possono essere configurati con un blocco di funzionalità principale durante la sequenziazione. Questa impostazione consente all'ingegnere di sequenziazione di monitorare i file di avvio per un'applicazione o applicazioni specifiche e di contrassegnare i blocchi di dati nel pacchetto App-V per lo streaming al primo avvio di qualsiasi applicazione nel pacchetto.

### Errori di flusso

Dopo il flusso iniziale di tutti i dati di pubblicazione e il blocco di funzionalità principale, le richieste di file aggiuntivi eseguono errori di flusso. Questi blocchi di dati vengono scaricati nell'archivio pacchetti in base alle esigenze. In questo modo, un utente deve scaricare solo una piccola parte del pacchetto, in genere sufficiente per avviare il pacchetto ed eseguire attività normali. Tutti gli altri blocchi vengono scaricati quando un utente avvia un'operazione che richiede dati non attualmente presenti nell'archivio pacchetti.

Per altre informazioni su App-V pacchetto in streaming, visita: <https://go.microsoft.com/fwlink/?LinkId=392770> .

La sequenziazione per l'ottimizzazione del flusso è disponibile all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### Aggiornamenti del pacchetto

I pacchetti App-V richiedono l'aggiornamento per tutto il ciclo di vita dell'applicazione. Gli aggiornamenti del pacchetto App-V sono simili all'operazione di pubblicazione del pacchetto, poiché ogni versione verrà creata nella propria posizione di PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . L'operazione di aggiornamento è ottimizzata creando collegamenti rigidi a file identici e in streaming da altre versioni dello stesso pacchetto.

### Rimozione del pacchetto

Il comportamento del client App-V quando i pacchetti vengono rimossi dipende dal metodo usato per la rimozione. Usando un'infrastruttura completa di App-V per annullare la pubblicazione dell'applicazione, i file di catalogo degli utenti (Catalogo macchine per le applicazioni pubblicate a livello globale) vengono rimossi, ma conservano la posizione e le posizioni della mucca nello Store del pacchetto. Quando `Remove-AppVClientPackge` si usa il cmdlet di PowerShell per rimuovere un pacchetto di App-V, la posizione dell'archivio pacchetti viene pulita. Tenere presente che l'annullamento della pubblicazione di un pacchetto App-V dal server di gestione non esegue un'operazione di rimozione. Nessuna delle due operazioni rimuoverà i file del pacchetto di archiviazione del pacchetto.

## <a href="" id="bkmk-roaming-reg-data"></a>Registro di sistema e dati mobili


App-V 5 è in grado di creare un'esperienza quasi nativa durante il roaming, a seconda di come viene scritta l'applicazione usata. Per impostazione predefinita, App-V fa roaming AppData archiviato nel percorso di roaming, in base alla configurazione del roaming del sistema operativo. In altre posizioni per l'archiviazione dei dati basati su file non è possibile eseguire il roaming da computer a computer, poiché si trovano in posizioni non in roaming.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>Requisiti di roaming e archiviazione dei dati del catalogo degli utenti

App-V archivia i dati, che rappresentano lo stato del catalogo dell'utente, sotto forma di:

-   File in%appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Impostazioni del registro di sistema in `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Insieme, questi file e le impostazioni del registro di sistema rappresentano il catalogo dell'utente, quindi entrambi devono essere in roaming oppure non devono essere spostati in roaming per un utente specifico. App-V non supporta il roaming% AppData%, ma non il roaming del profilo dell'utente (registro di sistema) o viceversa.

**Nota**  Il cmdlet **Repair-AppvClientPackage** non ripristina lo stato di pubblicazione dei pacchetti, dove lo stato dell'App-V dell'utente in `HKEY_CURRENT_USER` è mancante o non corrisponde ai dati in% AppData%.

 

### Dati basati sul Registro di sistema

Il roaming del registro di sistema di App-V rientra in due scenari, come illustrato nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applicazioni eseguite come utenti standard</p></td>
<td align="left"><p>Quando un utente standard avvia un'applicazione App-V, sia HKLM che HKCU per le applicazioni App-V vengono archiviati nell'hive HKCU nel computer. Questo si presenta come due percorsi distinti:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ SOFTWARE</p></li>
</ul>
<p>Le posizioni sono abilitate per il roaming in base alle impostazioni del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicazioni eseguite con l'elevazione</p></td>
<td align="left"><p>Quando un'applicazione viene avviata con l'elevazione:</p>
<ul>
<li><p>I dati HKLM sono archiviati nell'hive HKLM nel computer locale</p></li>
<li><p>I dati HKCU vengono archiviati nel percorso del registro di sistema dell'utente</p></li>
</ul>
<p>In questo scenario, queste impostazioni non vengono spostate in roaming con le normali configurazioni di roaming del sistema operativo e le chiavi e i valori dei registri risultanti sono archiviati nella posizione seguente:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### App-V e reindirizzamento delle cartelle

App-V 5.0 SP2 supporta il reindirizzamento delle cartelle della cartella AppData Roaming (% AppData%). Quando l'ambiente virtuale viene avviato, lo stato di AppData Roaming dalla directory AppData Roaming dell'utente viene copiato nella cache locale. Viceversa, quando l'ambiente virtuale viene arrestato, la cache locale associata al AppData Roaming di un utente specifico viene trasferita nella posizione effettiva della directory AppData Roaming di tale utente.

Un pacchetto tipico include diverse posizioni mappate nell'archivio di backup dell'utente per le impostazioni sia in AppData\\Local che in AppData\\Roaming. Questi percorsi sono la copia nei percorsi di scrittura archiviati per ogni utente nel profilo dell'utente e usati per archiviare le modifiche apportate alle directory del pacchetto VFS e per proteggere il pacchetto VFS predefinito.

La tabella seguente mostra le posizioni locali e di roaming, quando il reindirizzamento delle cartelle non è stato implementato.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Directory VFS nel pacchetto</th>
<th align="left">Percorso mappato dell'archivio di backup</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; forte &gt; roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

La tabella seguente mostra le posizioni locali e di roaming, quando il reindirizzamento delle cartelle è stato implementato per% AppData% e la posizione è stata reindirizzata (in genere in un percorso di rete).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Directory VFS nel pacchetto</th>
<th align="left">Percorso mappato dell'archivio di backup</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Il driver di App-V client VFS corrente non può scrivere nei percorsi di rete, in modo che il client App-V rilevi la presenza del reindirizzamento delle cartelle e copi i dati nell'unità locale durante la pubblicazione e quando l'ambiente virtuale viene avviato. Dopo che l'utente ha chiuso l'applicazione App-V e il client App-V chiude l'ambiente virtuale, l'archiviazione locale di VFS AppData viene copiata di nuovo nella rete, consentendo il roaming ad altri computer, in cui il processo verrà ripetuto. La procedura dettagliata dei processi è:

1.  Durante l'avvio della pubblicazione o dell'ambiente virtuale, il client App-V rileva la posizione della directory AppData.

2.  Se il percorso AppData Roaming è locale o viene mappato il percorso di AppData\\Roaming, non succede nulla.

3.  Se il percorso AppData Roaming non è locale, la directory VFS AppData viene mappata alla directory AppData locale.

Questo processo risolve il problema di un% AppData% non locale che non è supportato dal driver di App-V client VFS. I dati archiviati in questa nuova posizione non vengono tuttavia spostati in roaming con il reindirizzamento delle cartelle. Tutte le modifiche durante l'utilizzo dell'applicazione si verificano nella posizione AppData locale e devono essere copiate nella posizione reindirizzata. I passaggi dettagliati di questo processo sono i seguenti:

1.  L'applicazione App-V viene chiusa, che arresta l'ambiente virtuale.

2.  La cache locale della posizione AppData in roaming viene compressa e archiviata in un file ZIP.

3.  Un timestamp alla fine del processo di creazione di pacchetti ZIP viene usato per assegnare un nome al file.

4.  Il timestamp viene registrato nel registro di sistema: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime come ultimo timestamp noto di AppData.

5.  Il processo di reindirizzamento delle cartelle viene chiamato per valutare e avviare il file ZIP caricato nella directory AppData Roaming.

Il timestamp viene usato per determinare lo scenario "ultimo autore WINS" se esiste un conflitto e viene usato per ottimizzare il download dei dati quando viene pubblicata l'applicazione App-V o viene avviato l'ambiente virtuale. Il reindirizzamento delle cartelle rende disponibili i dati da qualsiasi altro client coperto dai criteri di supporto e avvia il processo di archiviazione dei dati di AppData\\Roaming nella posizione AppData locale del client. I processi dettagliati sono:

1.  L'utente avvia l'ambiente virtuale avviando un'applicazione.

2.  L'ambiente virtuale dell'applicazione controlla l'ora più recente del file ZIP con timbro, se presente.

3.  Il registro di sistema viene controllato per l'ultimo timestamp caricato noto, se presente.

4.  Il file ZIP più recente viene scaricato a meno che il timestamp dell'ultimo caricamento noto locale sia maggiore o uguale al timestamp del file ZIP.

5.  Se l'ultimo timestamp di caricamento noto locale è precedente rispetto a quello del file ZIP più recente nella posizione AppData in roaming, il file ZIP viene estratto nella directory Temp locale nel profilo dell'utente.

6.  Dopo che il file ZIP viene estratto correttamente, la cache locale della directory AppData Roaming viene rinominata e i nuovi dati vengono spostati in posizione.

7.  La directory rinominata viene eliminata e l'applicazione si apre con i dati comuni di roaming salvati più di recente.

Questa operazione completa il roaming corretto delle impostazioni dell'applicazione presenti nei percorsi di AppData\\Roaming. L'unica altra condizione che deve essere affrontata è un'operazione di ripristino del pacchetto. I dettagli del processo sono:

1.  Durante il ripristino, rilevare se il percorso della directory AppData Roaming dell'utente non è locale.

2.  Mappare le destinazioni del percorso AppData non locali per il roaming vengono ricreate le posizioni di roaming e AppData locali previste.

3.  Eliminare il timestamp archiviato nel registro di sistema, se presente.

Questo processo ricrea sia le posizioni locali che quelle di rete per AppData e rimuove il record del registro di sistema del timestamp.

## <a href="" id="bkmk-clt-app-lifecycle"></a>Gestione del ciclo di vita dell'applicazione client App-V


In un'infrastruttura completa di App-V, dopo la sequenziazione delle applicazioni, queste vengono gestite e pubblicate in utenti o computer tramite i server di gestione e pubblicazione di App-V. Questa sezione descrive in dettaglio le operazioni che si verificano durante le operazioni comuni di ciclo di vita delle applicazioni App-V (aggiungere, pubblicare, avviare, aggiornare e rimuovere) e le posizioni di file e del registro di sistema modificate e modificate dal punto di vista del client App-V. Le operazioni client App-V vengono eseguite come una serie di comandi di PowerShell avviati nel computer che esegue il client App-V.

Questo documento si incentra sulle soluzioni per l'infrastruttura completa di App-V. Per informazioni specifiche sull'integrazione di App-V con Configuration Manager 2012, visitare il sito: <https://go.microsoft.com/fwlink/?LinkId=392773> .

Le attività del ciclo di vita dell'applicazione App-V vengono attivate all'accesso dell'utente (impostazione predefinita), all'avvio del computer o alle operazioni temporizzate in background. Le impostazioni per le operazioni client App-V, inclusi i server di pubblicazione, gli intervalli di aggiornamento, l'abilitazione dello script del pacchetto e altre, vengono configurate durante l'installazione del client o post-installazione con i comandi di PowerShell. Vedere la sezione come distribuire il client in TechNet all'indirizzo: [come distribuire il client App-V](how-to-deploy-the-app-v-client-gb18030.md) o utilizzare PowerShell:

```powershell
get-command *appv*
```

### Aggiornamento pubblicazione

Il processo di aggiornamento della pubblicazione è costituito da diverse operazioni più piccole eseguite nel client App-V. Poiché App-V è una tecnologia di virtualizzazione delle applicazioni e non una tecnologia di pianificazione delle attività, l'utilità di pianificazione di Windows viene utilizzata per abilitare il processo all'accesso dell'utente, all'avvio del computer e a intervalli pianificati. La configurazione del client durante l'installazione di cui sopra è il metodo preferito durante la distribuzione del client a un numero elevato di computer con le impostazioni corrette. Queste impostazioni client possono essere configurate con i cmdlet di PowerShell seguenti:

-   **Add-AppVPublishingServer:** Configura il client con un server di pubblicazione App-V che fornisce pacchetti App-V.

-   **Set-AppVPublishingServer:** Modifica le impostazioni correnti per il server di pubblicazione App-V.

-   **Set-AppVClientConfiguration:** Modifica le impostazioni correnti per il client App-V.

-   **Sincronizzazione-AppVPublishingServer:** Avvia manualmente un processo di aggiornamento della pubblicazione App-V. Questa operazione viene utilizzata anche nelle attività pianificate create durante la configurazione del server di pubblicazione.

Lo stato principale delle sezioni seguenti consiste nel dettaglio delle operazioni che si verificano durante le diverse fasi di un aggiornamento della pubblicazione App-V. Gli argomenti includono:

-   Aggiunta di un pacchetto App-V

-   Pubblicazione di un pacchetto App-V

### Aggiunta di un pacchetto App-V

L'aggiunta di un pacchetto App-V al client è il primo passaggio del processo di aggiornamento della pubblicazione. Il risultato finale è uguale al `Add-AppVClientPackage` cmdlet in PowerShell, eccetto durante il processo di aggiunta dell'aggiornamento della pubblicazione, il server di pubblicazione configurato viene contattato e passa un elenco di applicazioni di alto livello al client per ottenere informazioni più dettagliate e non una singola operazione di aggiunta di un pacchetto. Il processo continua configurando il client per le aggiunte o gli aggiornamenti del gruppo di connessioni o pacchetti, quindi accede al file AppV. Il contenuto del file appv viene quindi espanso e inserito nel sistema operativo locale nelle posizioni appropriate. Di seguito è riportato un flusso di lavoro dettagliato del processo, presupponendo che il pacchetto sia configurato per il flusso di errore.

**Come aggiungere un pacchetto App-V**

1.  Avvio manuale tramite l'avvio di PowerShell o sequenza di attività del processo di aggiornamento della pubblicazione.

    1.  Il client App-V effettua una connessione HTTP e richiede un elenco di applicazioni in base alla destinazione. Il processo di aggiornamento della pubblicazione supporta i computer o gli utenti di destinazione.

    2.  Il server di pubblicazione App-V usa l'identità della destinazione, dell'utente o del computer iniziale e interroga il database per un elenco di applicazioni intitolate. L'elenco delle applicazioni viene fornito come risposta XML, che il client usa per inviare ulteriori richieste al server per ottenere altre informazioni su una base per pacchetto.

2.  L'agente di pubblicazione nel client App-V esegue tutte le azioni sotto serializzate.

    Valutare eventuali gruppi di connessioni non pubblicati o disabilitati, poiché gli aggiornamenti della versione del pacchetto che fanno parte del gruppo di connessioni non possono essere elaborati.

3.  Configurare i pacchetti identificando le operazioni di aggiunta o aggiornamento.

    1.  Il client App-V usa l'API AppX da Windows e accede al file appv dal server di pubblicazione.

    2.  Il file del pacchetto viene aperto e i AppXManifest.xml e StreamMap.xml vengono scaricati nell'archivio pacchetti.

    3.  Completamente i dati del blocco di pubblicazione in streaming definiti nella StreamMap.xml. Archivia i dati del blocco di pubblicazione nel pacchetto Store\\PkgGUID\\VerGUID\\Root.

        -   Icone: destinazioni dei punti di estensione.

        -   Intestazioni eseguibili portatili (intestazioni PE): destinazioni di punti di estensione che contengono le informazioni di base sulle esigenze di immagine su disco, accessibili direttamente o tramite tipi di file.

        -   Script: scaricare la directory scripts per l'uso durante il processo di pubblicazione.

    4.  Popolare l'archivio pacchetti:

        1.  Creare file sparsi su disco che rappresentano il pacchetto estratto per qualsiasi directory elencata.

        2.  Organizzare file e directory di primo livello in root.

        3.  Tutti gli altri file vengono creati quando la directory è elencata come sparsa su disco e trasmessa su richiesta.

    5.  Creare le voci del catalogo del computer. Creare la Manifest.xml e DeploymentConfiguration.xml dai file del pacchetto (se non è stato creato alcun file di DeploymentConfiguration.xml nel pacchetto).

    6.  Creare la posizione dell'archivio pacchetti nel registro di sistema HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Creare il file Registry. dat dall'archivio pacchetti in%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat

    8.  Registrare il pacchetto con il driver della modalità kernel App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Richiamare gli script dal file AppxManifest.xml o DeploymentConfig.xml per aggiungere un intervallo di pacchetti.

4.  Configurare i gruppi di connessioni aggiungendo e abilitando o disabilitando.

5.  Rimuovere gli oggetti non pubblicati nella destinazione (utente o computer).

    **Nota**  In questo modo non verrà eseguita l'eliminazione di un pacchetto, ma si rimuovono i punti di integrazione per il target specifico (utente o computer) e si rimuovono i file di catalogo degli utenti (file catalogo computer per la pubblicazione globale).

     

6.  Richiamare il supporto del caricamento in background in base alla configurazione client.

7.  I pacchetti che hanno già informazioni sulla pubblicazione per il computer o l'utente vengono immediatamente ripristinati.

    **Nota**  Questa condizione si verifica come prodotto della rimozione senza l'annullamento della pubblicazione con l'aggiunta di sfondo del pacchetto.

     

Viene completato un pacchetto App-V che aggiunge il processo di aggiornamento della pubblicazione. Il passaggio successivo consiste nel pubblicare il pacchetto nella destinazione specifica (computer o utente).

![pacchetto Aggiungi file e dati del registro di sistema](images/packageaddfileandregistrydata.png)

### Pubblicazione di un pacchetto App-V

Durante l'operazione di aggiornamento della pubblicazione, l'operazione di pubblicazione specifica (Publish-AppVClientPackage) aggiunge voci al catalogo utenti, associa l'autorizzazione all'utente, identifica l'archivio locale e termina completando i passaggi di integrazione. Di seguito sono illustrati i passaggi dettagliati.

**Come pubblicare e pacchetto App-V**

1.  Le voci del pacchetto vengono aggiunte al catalogo utenti

    1.  Pacchetti mirati dall'utente: le UserDeploymentConfiguration.xml e le UserManifest.xml vengono posizionate nel computer del catalogo utenti

    2.  Pacchetti di destinazione del computer (globali): la UserDeploymentConfiguration.xml viene inserita nel catalogo del computer

2.  Registrare il pacchetto con il driver in modalità kernel per l'utente su HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Eseguire attività di integrazione.

    1.  Creare punti di estensione.

    2.  Archiviare le informazioni di backup nel registro di sistema e nel profilo di roaming dell'utente (backup dei collegamenti).

        **Nota**  Questo consente di ripristinare i punti di estensione se il pacchetto non è pubblicato.

         

    3.  Eseguire script mirati per l'intervallo di pubblicazione.

La pubblicazione di un pacchetto App-V che fa parte di un gruppo di connessioni è molto simile al processo precedente. Per i gruppi di connessioni, il percorso in cui sono archiviate le informazioni specifiche del catalogo include PackageGroups come elemento figlio della directory del catalogo. Per informazioni dettagliate, vedere il catalogo computer e gli utenti.

![pacchetto Aggiungi file e dati del registro di sistema-globale](images/packageaddfileandregistrydata-global.png)

### Avvio di un'applicazione

Dopo il processo di aggiornamento della pubblicazione, l'utente avvia e successivamente riavvia un'applicazione App-V. Il processo è molto semplice e ottimizzato per l'avvio rapido con un minimo di traffico di rete. Il client App-V controlla il percorso del catalogo utente per i file creati durante la pubblicazione. Dopo aver stabilito i diritti per l'avvio del pacchetto, il client App-V crea un ambiente virtuale, inizia a trasmettere i dati necessari e applica i file di configurazione del manifesto e della distribuzione appropriati durante la creazione di ambiente virtuale. Con l'ambiente virtuale creato e configurato per il pacchetto e l'applicazione specifici, viene avviata l'applicazione.

**Come avviare le applicazioni App-V**

1.  L'utente avvia l'applicazione facendo clic su un collegamento o una chiamata di tipo file.

2.  Il client App-V Verifica l'esistenza nel catalogo utente per i file seguenti

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Se i file sono presenti, l'applicazione ha diritto a tale utente specifico e l'applicazione avvierà il processo per l'avvio. A questo punto non esiste un traffico di rete.

4.  Il client App-V Verifica quindi che il percorso del pacchetto registrato per il servizio client App-V si trovi nel registro di sistema.

5.  Dopo aver trovato il percorso dell'archivio pacchetti, viene creato l'ambiente virtuale. Se si tratta del primo avvio, il blocco di funzionalità principale verrà scaricato se presente.

6.  Dopo il download, il servizio client App-V usa i file di configurazione del manifesto e della distribuzione per configurare l'ambiente virtuale e tutti i sottosistemi App-V caricati.

7.  L'applicazione viene avviata. Per tutti i file mancanti nell'archivio dei pacchetti (file sparsi), l'App-V scaricherà i file in base alle esigenze.

    ![pacchetto Aggiungi file e dati del registro di sistema-Stream](images/packageaddfileandregistrydata-stream.png)

### Aggiornamento di un pacchetto App-V

Il processo di aggiornamento del pacchetto App-V 5 si differenzia dalle versioni precedenti di App-V. App-V supporta più versioni dello stesso pacchetto in un computer avente diritto a utenti diversi. Le versioni del pacchetto possono essere aggiunte in qualsiasi momento, in quanto l'archivio dei pacchetti e i cataloghi vengono aggiornati con le nuove risorse. L'unico processo specifico per l'aggiunta delle nuove risorse della versione è l'ottimizzazione dello spazio di archiviazione. Durante un aggiornamento, solo i nuovi file vengono aggiunti alla nuova posizione dell'archivio versioni e i collegamenti rigidi vengono creati per i file non modificati. In questo modo si riduce l'archiviazione complessiva solo presentando il file in una posizione del disco e quindi proiettando in tutte le cartelle con una voce di posizione del file sul disco. I dettagli specifici dell'aggiornamento di un pacchetto App-V sono i seguenti:

**Come aggiornare un pacchetto di App-V**

1.  Il client App-V esegue un aggiornamento della pubblicazione e individua una versione più recente di un pacchetto App-V.

2.  Le voci del pacchetto vengono aggiunte al catalogo appropriato per la nuova versione

    1.  Pacchetti mirati dall'utente: le UserDeploymentConfiguration.xml e le UserManifest.xml vengono posizionate nel computer nel catalogo utenti in appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Pacchetti di destinazione del computer (globali): la UserDeploymentConfiguration.xml viene inserita nel catalogo computer in%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Registrare il pacchetto con il driver in modalità kernel per l'utente su HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Eseguire attività di integrazione.

    -   Integrare i punti estensioni (EP) dai file di configurazione manifesto e dinamico.

    1.  I dati EP basati su file sono archiviati nella cartella AppData che utilizza punti di giunzione dall'archivio pacchetti.

    2.  La versione 1 EPs esiste già quando una nuova versione diventa disponibile.

    3.  I punti di estensione vengono passati alla posizione della versione 2 in cataloghi di computer o utenti per eventuali punti di estensione più recenti o aggiornati.

5.  Eseguire script mirati per l'intervallo di pubblicazione.

6.  Installare gli assembly affiancati in base alle esigenze.

### Aggiornamento di un pacchetto App-V in uso

A **partire da App-V 5 SP2**: se si tenta di aggiornare un pacchetto in uso da parte di un utente finale, l'attività di aggiornamento viene inserita in uno stato in sospeso. L'aggiornamento verrà eseguito in un secondo momento, in base alle regole seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di attività</th>
<th align="left">Regola applicabile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</p></td>
</tr>
</tbody>
</table>

 

Quando un'attività viene inserita in uno stato in sospeso, il client App-V genera anche una chiave del registro di sistema per l'attività in sospeso, come indicato di seguito:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività basata su utenti o globale</th>
<th align="left">Dove viene generata la chiave del registro di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basate sull'utente</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basate su base globale</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Le operazioni seguenti devono essere completate prima che gli utenti possano usare la versione più recente del pacchetto:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiungere il pacchetto al computer</p></td>
<td align="left"><p>Questa attività è specifica del computer ed è possibile eseguirla in qualsiasi momento completando i passaggi della sezione Aggiungi pacchetto precedente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pubblicare il pacchetto</p></td>
<td align="left"><p>Vedere la sezione pubblicazione del pacchetto sopra per i passaggi. Questo processo richiede l'aggiornamento dei punti di estensione nel sistema. Gli utenti finali non possono usare l'applicazione quando si completa questa attività.</p></td>
</tr>
</tbody>
</table>

 

Usare gli scenari di esempio seguenti come guida per l'aggiornamento dei pacchetti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Requisiti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Il pacchetto App-V non è in uso quando si tenta di eseguire l'aggiornamento</p></td>
<td align="left"><p>Nessuno dei componenti seguenti del pacchetto può essere in uso: applicazione virtuale, server COM o estensioni della shell.</p>
<p>L'amministratore pubblica una versione più recente del pacchetto e l'aggiornamento funziona la volta successiva che viene avviato un componente o un'applicazione all'interno del pacchetto. La nuova versione del pacchetto è in streaming ed è in esecuzione. Questo scenario non è stato modificato in App-V 5 SP2 dalle versioni precedenti di App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Il pacchetto App-V è in uso quando l'amministratore pubblica una versione più recente del pacchetto</p></td>
<td align="left"><p>L'operazione di aggiornamento è impostata su in sospeso dal client App-V, il che significa che viene accodato e eseguito in seguito quando il pacchetto non è in uso.</p>
<p>Se l'applicazione pacchetto è in uso, l'utente arresta l'applicazione virtuale, dopo la quale può essere eseguito l'aggiornamento.</p>
<p>Se il pacchetto include estensioni della shell (Office 2013), che vengono caricate in modo permanente da Esplora risorse, l'utente non può essere connesso. Gli utenti devono disconnettersi e accedere di nuovo per avviare l'aggiornamento del pacchetto App-V.</p></td>
</tr>
</tbody>
</table>

 

### Pubblicazione globale degli utenti vs

I pacchetti App-V possono essere pubblicati in uno dei due modi seguenti: Utente che dà diritto a un pacchetto di App-V a un utente o un gruppo di utenti specifico e globale che dà diritto al pacchetto App-V a tutto il computer per tutti gli utenti del computer. Una volta che un aggiornamento del pacchetto è stato sospeso e il pacchetto App-V non è in uso, prendere in considerazione i due tipi di pubblicazione:

-   **Pubblicazione globale**: l'applicazione viene pubblicata in un computer; tutti gli utenti del computer possono usarlo. L'aggiornamento avverrà quando viene avviato il servizio client App-V, che significa effettivamente riavviare il computer.

-   **Utente pubblicato**: l'applicazione viene pubblicata in un utente. Se nel computer sono presenti più utenti, è possibile che l'applicazione venga pubblicata in un sottoinsieme degli utenti. L'aggiornamento avverrà quando l'utente accede o quando viene pubblicato di nuovo (periodicamente, ConfigMgr aggiornamento dei criteri e valutazione o una pubblicazione/aggiornamento periodico di App-V o in modo esplicito tramite i comandi di PowerShell).

### Rimozione di un pacchetto App-V

La rimozione delle applicazioni App-V in un'infrastruttura completa è un'operazione di annullamento della pubblicazione e non esegue una rimozione del pacchetto. Il processo è uguale al processo di pubblicazione precedente, ma invece di aggiungere il processo di rimozione Annulla le modifiche apportate per i pacchetti di App-V.

### Ripristino di un pacchetto App-V

L'operazione di ripristino è molto semplice, ma può interessare molte posizioni nel computer. Vengono rimosse le posizioni di copia in scrittura (mucca) in precedenza e i punti di estensione vengono disintegrati e quindi reintegrati. Esaminare le posizioni di posizionamento dei dati della mucca rivedendo il punto in cui sono registrate nel registro di sistema. Questa operazione viene eseguita automaticamente e non esiste un controllo amministrativo diverso dall'avvio di un'operazione di ripristino dalla console client App-V o tramite PowerShell (Repair-AppVClientPackage).

## <a href="" id="bkmk-integr-appv-pkgs"></a>Integrazione dei pacchetti App-V


L'architettura client e pacchetto App-V offre un'integrazione specifica con il sistema operativo locale durante l'aggiunta e la pubblicazione di pacchetti. Tre file definiscono i punti di integrazione o di estensione per un pacchetto di App-V:

-   AppXManifest.xml: archiviato all'interno del pacchetto con le copie di fallback archiviate nell'archivio pacchetti e nel profilo utente. Contiene le opzioni create durante il processo di sequenziazione.

-   DeploymentConfig.xml: fornisce informazioni sulla configurazione dei punti di estensione di integrazione basati su computer e utenti.

-   UserConfig.xml: un sottoinsieme della Deploymentconfig.xml che fornisce solo configurazioni basate sull'utente e solo i punti di estensione basati sull'utente.

### Regole di integrazione

Quando le applicazioni App-V vengono pubblicate in un computer con il client App-V, alcune azioni specifiche avvengono come descritto nell'elenco seguente:

-   Pubblicazione globale: i tasti di scelta rapida sono archiviati nella posizione tutti i profili degli utenti e altri punti di estensione sono archiviati nel registro di sistema dell'hive HKLM.

-   Pubblicazione degli utenti: i tasti di scelta rapida sono archiviati nel profilo dell'account utente corrente e altri punti di estensione vengono archiviati nel registro di sistema nell'hive HKCU.

-   Backup e ripristino: i dati e il registro di sistema esistenti delle applicazioni native (ad esempio le registrazioni FTA) vengono copiati durante la pubblicazione.

    1.  I pacchetti App-V vengono assegnati alla proprietà in base all'ultimo pacchetto integrato in cui la proprietà viene passata alla più recente applicazione App-V pubblicata.

    2.  I trasferimenti di proprietà da un pacchetto di App-V a un altro quando il pacchetto dell'App-V proprietario è inedito. In questo modo non verrà avviato un ripristino dei dati o del registro di sistema.

    3.  Ripristinare i dati di cui è stato eseguito il backup quando l'ultimo pacchetto non viene pubblicato o rimosso in base al punto di estensione.

### Punti di estensione

I file di pubblicazione App-V (manifesto e configurazione dinamica) offrono diversi punti di estensione che consentono all'applicazione di integrarsi con il sistema operativo locale. Questi punti di estensione eseguono le tipiche attività di installazione delle applicazioni, ad esempio l'immissione di collegamenti, la creazione di associazioni di tipi di file e la registrazione dei componenti. Poiché si tratta di applicazioni virtualizzate che non sono installate allo stesso modo di un'applicazione tradizionale, esistono alcune differenze. Di seguito è riportato un elenco di punti di estensione descritti in questa sezione:

-   Scorciatoie

-   Associazioni di tipi di file

-   Estensioni della shell

-   COM

-   Client software

-   Funzionalità delle applicazioni

-   Gestore protocollo URL

-   AppPath

-   Applicazione virtuale

### Scorciatoie

La scorciatoia è uno degli elementi di base per l'integrazione con il sistema operativo ed è l'interfaccia per l'avvio diretto degli utenti di un'applicazione App-V. Durante la pubblicazione e l'annullamento della pubblicazione delle applicazioni App-V.

Dal manifesto del pacchetto e dai file XML di configurazione dinamica, il percorso di un eseguibile specifico dell'applicazione può essere trovato in una sezione simile alla seguente:

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

Come accennato in precedenza, i tasti di scelta rapida dell'App-V vengono posizionati per impostazione predefinita nel profilo dell'utente in base all'operazione di aggiornamento. Le scelte rapide da tastiera di aggiornamento globale sono memorizzate nel profilo di tutti gli utenti e l'aggiornamento dell'utente viene archiviato nello specifico utente. L'eseguibile effettivo viene archiviato nell'archivio pacchetti. La posizione del file ICO è una posizione in formato token nel pacchetto App-V.

### Associazioni di tipi di file

Il client App-V gestisce le associazioni dei tipi di file del sistema operativo locale durante la pubblicazione, che consente agli utenti di usare le chiamate di tipo file o di aprire un file con estensione docx specificatamente registrata per avviare un'applicazione App-V. Le associazioni di tipi di file sono presenti nei file di configurazione manifesto e dinamico come rappresentato nell'esempio seguente:

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**Nota**  In questo esempio:

-   `<Name>.xdp</Name>` è l'estensione

-   `<Name>AcroExch.XDPDoc</Name>` è il valore ProgId (che punta al ProgId adiacente)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` è la riga di comando, che punta al file eseguibile dell'applicazione

 

### Estensioni della shell

Le estensioni della shell vengono inserite automaticamente nel pacchetto durante il processo di sequenziazione. Quando il pacchetto viene pubblicato globalmente, l'estensione della Shell offre agli utenti le stesse funzionalità di se l'applicazione è stata installata localmente. L'applicazione non richiede alcuna installazione o configurazione aggiuntiva nel client per abilitare la funzionalità di estensione della shell.

**Requisiti per l'uso delle estensioni della shell:**

-   I pacchetti che contengono estensioni della shell incorporata devono essere pubblicati globalmente.

-   Il "bit" dell'applicazione, il sequencer e il client App-V devono corrispondere o le estensioni della shell non funzionano. Ad esempio:

    -   La versione dell'applicazione è 64 bit.

    -   Il sequencer viene eseguito in un computer a 64 bit.

    -   Il pacchetto viene recapitato a un computer client App-V a 64 bit.

La tabella seguente mostra le estensioni della shell supportate.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gestore</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestore del menu di scelta rapida</p></td>
<td align="left"><p>Aggiunge voci di menu al menu di scelta rapida. Viene chiamata prima che venga visualizzato il menu di scelta rapida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore di trascinamento della selezione</p></td>
<td align="left"><p>Controlla l'azione quando fai clic con il pulsante destro del mouse su trascinamento della selezione e modifica il menu di scelta rapida visualizzato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Trascinare il gestore di destinazione</p></td>
<td align="left"><p>Controlla l'azione dopo il trascinamento e l'eliminazione di un oggetto dati su una destinazione di rilascio, ad esempio un file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore oggetti dati</p></td>
<td align="left"><p>Controlla l'azione dopo la copia di un file negli Appunti o il trascinamento della selezione su una destinazione di rilascio. Può includere altri formati di Appunti nella destinazione di rilascio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore della finestra delle proprietà</p></td>
<td align="left"><p>Sostituisce o aggiunge pagine alla finestra di dialogo delle proprietà di un oggetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore infotip</p></td>
<td align="left"><p>Consente di recuperare le informazioni di flag e infotip per un elemento e di visualizzarle all'interno di una descrizione comando popup al passaggio del mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore di colonne</p></td>
<td align="left"><p>Consente la creazione e la visualizzazione di colonne personalizzate nella visualizzazione dettagli di Esplora risorse <em> </em> . Può essere usato per estendere l'ordinamento e il raggruppamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore di anteprime</p></td>
<td align="left"><p>Consente di visualizzare un'anteprima di un file nel riquadro di anteprima di Windows Explorer.</p></td>
</tr>
</tbody>
</table>

 

### COM

Il client App-V supporta le applicazioni di pubblicazione con il supporto per l'integrazione e la virtualizzazione COM. L'integrazione COM consente al client App-V di registrare oggetti COM nel sistema operativo locale e la virtualizzazione degli oggetti. Per gli scopi di questo documento, l'integrazione di oggetti COM richiede dettagli aggiuntivi.

App-V supporta la registrazione di oggetti COM dal pacchetto nel sistema operativo locale con due tipi di processo: out-of-process e in-process. La registrazione di oggetti COM viene eseguita con una o una combinazione di più modalità di operazione per un pacchetto App-V specifico che include disattivato, isolato e integrato. La modalità integrata è configurata per il tipo out-of-process o in-process. La configurazione delle modalità e dei tipi COM viene eseguita con i file di configurazione dinamici (deploymentconfig.xml o userconfig.xml).

I dettagli sull'integrazione di App-V sono disponibili all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### Client software e funzionalità delle applicazioni

App-V supporta i client software specifici e i punti di estensione delle funzionalità applicative che consentono di registrare le applicazioni virtualizzate con il client software del sistema operativo. Questo consente agli utenti di selezionare programmi predefiniti per operazioni come la posta elettronica, la messaggistica istantanea e il lettore multimediale. Questa operazione viene eseguita nel pannello di controllo con le impostazioni predefinite per l'accesso ai programmi e i computer e configurata durante la sequenziazione nei file di configurazione manifesto o dinamico. Le funzionalità dell'applicazione sono supportate solo quando le applicazioni App-V vengono pubblicate globalmente.

Esempio di registrazione client software di un client di posta elettronica basato su App-V.

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**Nota**  In questo esempio:

-   `<ClientConfiguration EmailEnabled="true" />` è l'impostazione complessiva dei client software per integrare i client di posta elettronica

-   `<EMail MakeDefault="true">` è il contrassegno per impostare un determinato client di posta elettronica come client di posta elettronica predefinito

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` è la registrazione della DLL MAPI

 

### Gestore protocollo URL

Le applicazioni non sempre espressamente denominate applicazioni virtualizzate che usano la chiamata del tipo di file. Ad esempio, in un'applicazione che supporta l'incorporamento di un collegamento mailto: all'interno di un documento o di una pagina Web, l'utente fa clic su un collegamento mailto: e prevede di ottenere il client di posta elettronica registrato. App-V supporta i gestori di protocolli URL che possono essere registrati per ogni singolo pacchetto con il sistema operativo locale. Durante la sequenziazione, i gestori di protocolli URL vengono aggiunti automaticamente al pacchetto.

Per le situazioni in cui sono presenti più applicazioni in grado di registrare il gestore del protocollo URL specifico, è possibile usare i file di configurazione dinamica per modificare il comportamento ed eliminare o disabilitare questa caratteristica per un'applicazione che non deve essere l'applicazione principale avviata.

### AppPath

Il punto di estensione AppPath supporta la chiamata delle applicazioni App-V direttamente dal sistema operativo. Questa operazione viene in genere eseguita dalla schermata Esegui o Start, a seconda del sistema operativo, che consente agli amministratori di consentire l'accesso alle applicazioni App-V da comandi o script del sistema operativo senza chiamare il percorso specifico dell'eseguibile. Evita quindi di modificare la variabile di ambiente PATH di sistema in tutti i sistemi, come avviene durante la pubblicazione.

Il punto di estensione AppPath è configurato nel manifesto o nei file di configurazione dinamica e viene archiviato nel registro di sistema nel computer locale durante la pubblicazione per l'utente. Per altre informazioni su AppPath Review: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### Applicazione virtuale

Questo sottosistema fornisce un elenco di applicazioni acquisite durante la sequenziazione che in genere sono usate da altri componenti di App-V. L'integrazione di punti di estensione appartenenti a una particolare applicazione può essere disabilitata con i file di configurazione dinamici. Ad esempio, se un pacchetto contiene due applicazioni, è possibile disabilitare tutti i punti di estensione appartenenti a un'applicazione, in modo da consentire solo l'integrazione dei punti di estensione di un'altra applicazione.

### Regole del punto di estensione

I punti di estensione descritti sopra sono integrati nel sistema operativo in base al modo in cui i pacchetti sono stati pubblicati. I punti di estensione per la pubblicazione globale sono ubicati in posizioni macchina pubbliche, in cui i punti di estensione della pubblicazione degli utenti vengono posizionati in Ad esempio, un collegamento creato sul desktop e pubblicato globalmente comporterà i dati del file per il collegamento (%Public%\\Desktop) e i dati del registro di sistema (HKLM\\Software\\Classes). Lo stesso collegamento avrebbe i dati dei file (%UserProfile%\\Desktop) e i dati del registro di sistema (HKCU\\Software\\Classes).

I punti di estensione non sono tutti pubblicati nello stesso modo, in cui alcuni punti di estensione richiedono la pubblicazione globale e altri richiedono la sequenziazione nel sistema operativo specifico e nell'architettura in cui vengono recapitati. Di seguito è riportata una tabella che descrive queste due regole chiave.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estensione virtuale</th>
<th align="left">Richiede la sequenziazione del sistema operativo di destinazione</th>
<th align="left">Richiede la pubblicazione globale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Collegamento</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Associazione tipo di file</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocolli URL</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modalità COM</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Client software</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Funzionalità delle applicazioni</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore del menu di scelta rapida</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore di trascinamento della selezione</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore oggetti dati</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore della finestra delle proprietà</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore infotip</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore di colonne</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Estensioni della shell</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Oggetto helper del browser</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Oggetto X attivo</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a>Elaborazione della configurazione dinamica


La distribuzione di pacchetti App-V in un computer o un utente è molto semplice. Tuttavia, dato che le organizzazioni distribuiscono applicazioni AppV tra le linee aziendali e i confini geografici e politici, la possibilità di sequenziare un'applicazione una sola volta con un set di impostazioni diventa impossibile. App-V è stato progettato per questo scenario, poiché acquisisce impostazioni e configurazioni specifiche durante la sequenziazione nel file manifesto, ma supporta anche la modifica con i file di configurazione dinamica.

La configurazione dinamica di App-V consente di specificare un criterio per un pacchetto a livello di computer o a livello di utente. I file di configurazione dinamica consentono agli ingegneri di sequenziazione di modificare la configurazione di un pacchetto, la post-sequenziazione, per soddisfare le esigenze dei singoli gruppi di utenti o computer. In alcuni casi potrebbe essere necessario apportare modifiche all'applicazione per offrire funzionalità appropriate nell'ambiente App-V. Ad esempio, potrebbe essere necessario apportare modifiche ai file \ _ \ * config.xml per consentire l'esecuzione di determinate azioni in un determinato periodo di tempo, come la disabilitazione di un'estensione mailto per impedire che un'applicazione virtualizzata sovrascriva tale estensione da un'altra applicazione.

I pacchetti App-V contengono il file manifesto all'interno del file del pacchetto appv, che rappresenta le operazioni di sequenziazione ed è il criterio di scelta, a meno che non vengano assegnati file di configurazione dinamici a un pacchetto specifico. Post-sequenziazione, i file di configurazione dinamici possono essere modificati per consentire la pubblicazione di un'applicazione in desktop o utenti diversi con punti di estensione diversi. I due file di configurazione dinamici sono i file di configurazione della distribuzione dinamica (DDC) e della configurazione degli utenti dinamici (DUC). Questa sezione si basa sulla combinazione dei file di configurazione manifesto e dinamico.

### Esempio per i file di configurazione dinamica

L'esempio seguente mostra la combinazione del manifesto, della configurazione della distribuzione e dei file di configurazione degli utenti dopo la pubblicazione e durante il normale funzionamento. Questi esempi sono esempi abbreviati di ognuno dei file. Lo scopo è mostrare la combinazione dei file solo e non essere una descrizione completa delle categorie specifiche disponibili in ognuno dei file. Per altre informazioni, vedere la guida alla sequenziazione di App-V 5 all'indirizzo: <https://go.microsoft.com/fwlink/?LinkID=269810>

**Manifesto**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**Configurazione della distribuzione**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**Configurazione utente**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a>Assembly affiancati


App-V supporta la creazione automatica di assembly side-by-Side (SxS) durante la sequenziazione e la distribuzione nel client durante la pubblicazione di applicazioni virtuali. App-V 5 SP2 supporta l'acquisizione di assembly SxS durante la sequenziazione per gli assembly non presenti nel computer di sequenziazione. Per gli assembly costituiti da Visual C++ (versione 8 e successive) e/o da Runtime di MSXML, il sequencer rileverà e catturerà automaticamente queste dipendenze anche se non sono state installate durante il monitoraggio. La caratteristica assiemi affiancati rimuove le limitazioni delle versioni precedenti di App-V, in cui l'App-V Sequencer non ha acquisito gli assembly già presenti nella workstation di sequenziazione e ha privatizzato gli assembly che limitavano la versione di un bit per ogni pacchetto. Questo comportamento ha provocato le applicazioni App-V distribuite ai client che mancano degli assembly SxS necessari, causando errori di avvio dell'applicazione. In questo modo il processo di creazione del pacchetto è stato costretto a documentare e quindi assicurarsi che tutti gli assembly necessari per i pacchetti fossero installati localmente nel sistema operativo client dell'utente per garantire il supporto per le applicazioni virtuali. In base al numero di assembly e alla mancanza di documentazione dell'applicazione per le dipendenze richieste, questa attività è stata una sfida di gestione e implementazione.

Il supporto per l'assembly affiancato in App-V include le caratteristiche seguenti.

-   Acquisisce automaticamente l'assembly SxS durante la sequenziazione, indipendentemente dal fatto che l'assembly sia già stato installato nella workstation di sequenziazione.

-   Il client App-V installa automaticamente gli assembly SxS obbligatori nel computer client in fase di pubblicazione quando non sono presenti.

-   Il sequencer riporta la dipendenza di runtime VC nel meccanismo di creazione di report Sequencer.

-   Il Sequencer consente di non creare il pacchetto degli assembly già installati nel sequencer, sostenendo gli scenari in cui gli assembly sono stati installati in precedenza nei computer di destinazione.

### Pubblicazione automatica di assembly SxS

Durante la pubblicazione di un pacchetto App-V con gli assembly SxS, il client App-V verificherà la presenza dell'assembly nel computer. Se l'assembly non esiste, il client distribuirà l'assembly nel computer. I pacchetti che fanno parte dei gruppi di connessioni si basano sulle installazioni affiancate di assembly che fanno parte dei pacchetti di base, poiché il gruppo di connessioni non contiene informazioni sull'installazione di assembly.

**Nota**  L'annullamento della pubblicazione o della rimozione di un pacchetto con un assembly non rimuove gli assembly per il pacchetto.

 

## <a href="" id="bkmk-client-logging"></a>Registrazione client


Il client App-V registra le informazioni nel log eventi di Windows in formato ETW standard. Gli eventi specifici di App-V si trovano nel Visualizzatore eventi, in applicazioni e servizi Logs\\Microsoft\\AppV\\Client.

**Nota**  In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati nella posizione seguente:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Per un elenco dei registri spostati, vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

Sono state registrate tre categorie di eventi specifiche descritte di seguito.

**Amministratore**: registra gli eventi per le configurazioni applicate al client App-V e contiene gli avvisi e gli errori principali.

**Operativo**: registra l'esecuzione generale dell'app-v e l'uso dei singoli componenti creando un log di controllo delle operazioni di App-v che sono state completate nel client App-v.

**Applicazione virtuale**: registra i lanci delle applicazioni virtuali e l'uso dei sottosistemi di virtualizzazione.






 

 





