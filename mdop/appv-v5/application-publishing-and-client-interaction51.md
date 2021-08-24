---
title: Pubblicazione delle applicazioni e interazione dei client
description: Pubblicazione delle applicazioni e interazione dei client
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b94ef87043d428ac92fe1656b3afeb8a8b743808
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910821"
---
# <a name="application-publishing-and-client-interaction"></a>Pubblicazione delle applicazioni e interazione dei client


Questo articolo fornisce informazioni tecniche sulle operazioni comuni del client App-V e sulla relativa integrazione con il sistema operativo locale.

-   [File del pacchetto App-V creati da Sequencer](#bkmk-appv-pkg-files-list)

-   [Cosa c'è nel file appv?](#bkmk-appv-file-contents)

-   [Posizioni di archiviazione dei dati del client App-V](#bkmk-files-data-storage)

-   [Registro di sistema del pacchetto](#bkmk-pkg-registry)

-   [Comportamento dell'archivio pacchetti app-V](#bkmk-pkg-store-behavior)

-   [Roaming del Registro di sistema e dei dati](#bkmk-roaming-reg-data)

-   [Gestione del ciclo di vita delle applicazioni client App-V](#bkmk-clt-app-lifecycle)

-   [Integrazione di pacchetti App-V](#bkmk-integr-appv-pkgs)

-   [Elaborazione della configurazione dinamica](#bkmk-dynamic-config)

-   [Assembly affiancati](#bkmk-sidebyside-assemblies)

-   [Registrazione client](#bkmk-client-logging)

Per ulteriori informazioni di riferimento, vedere Pagina di download delle risorse della documentazione di [Microsoft Application Virtualization (App-V).](https://www.microsoft.com/download/details.aspx?id=27760)

## <a name="app-v-package-files-created-by-the-sequencer"></a><a href="" id="bkmk-appv-pkg-files-list"></a>File del pacchetto App-V creati da Sequencer


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
<td align="left"><p>.appv</p></td>
<td align="left"><ul>
<li><p>Il file del pacchetto principale, che contiene gli asset acquisiti e le informazioni sullo stato del processo di sequenziazione.</p></li>
<li><p>Architettura del file del pacchetto, informazioni di pubblicazione e Registro di sistema in un formato token che può essere riapplicato a un computer e a un utente specifico al momento della consegna.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>.MSI</p></td>
<td align="left"><p>Wrapper di distribuzione eseguibile che puoi usare per distribuire i file appv manualmente o usando una piattaforma di distribuzione di terze parti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>File utilizzato per personalizzare i parametri di pubblicazione predefiniti per tutte le applicazioni di un pacchetto distribuito a livello globale a tutti gli utenti in un computer che esegue il client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>File utilizzato per personalizzare i parametri di pubblicazione per tutte le applicazioni di un pacchetto distribuito a un utente specifico in un computer che esegue il client App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Riepilogo dei messaggi risultanti dal processo di sequenziazione, inclusi driver, file e percorsi del Registro di sistema omessi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>Facoltativo: </em> file acceleratore del pacchetto usato per ricreare automaticamente un pacchetto di applicazione virtuale sequenziato in precedenza.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Facoltativo: </em> file modello sequencer usato per conservare le impostazioni di Sequencer comunemente riutilizzate.</p></td>
</tr>
</tbody>
</table>

 

Per informazioni sulla sequenziazione, vedere [Application Virtualization Sequencing Guide.](https://go.microsoft.com/fwlink/?LinkID=269810)

## <a name="whats-in-the-appv-file"></a><a href="" id="bkmk-appv-file-contents"></a>Cosa c'è nel file appv?


Il file appv è un contenitore che archivia file XML e non XML insieme in una singola entità. Questo file è basato sul formato AppX, basato sullo standard OPC (Open Packaging Conventions).

Per visualizzare il contenuto del file appv, crea una copia del pacchetto e quindi rinomina il file copiato con un'estensione ZIP.

Il file appv contiene la cartella e i file seguenti, utilizzati per la creazione e la pubblicazione di un'applicazione virtuale:

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
<td align="left"><p>Directory contenente il file system per l'applicazione virtualizzata acquisita durante la sequenziazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types].xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Elenco dei tipi di contenuto di base nel file appv (ad esempio DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Layout del file appv, che usa gli elementi File, Block e BlockMap che consentono la posizione e la convalida dei file nel pacchetto App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Metadati per il pacchetto che contiene le informazioni necessarie per l'aggiunta, la pubblicazione e l'avvio del pacchetto. Include i punti di estensione (associazioni di tipi di file e collegamenti) e i nomi e i GUID associati al pacchetto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Elenco dei file acquisiti durante la sequenziazione, inclusi gli attributi (ad esempio, directory, file, directory opache, directory vuote e nomi lunghi e brevi).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Informazioni sul computer di sequenziazione (versione del sistema operativo, versione di Internet Explorer, versione .Net Framework) e processo (aggiornamento, versione del pacchetto).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry.dat</p></td>
<td align="left"><p>DAT File</p></td>
<td align="left"><p>Chiavi del Registro di sistema e valori acquisiti durante il processo di sequenziazione per il pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>XML File</p></td>
<td align="left"><p>Elenco di file per il blocco di funzionalità principale e di pubblicazione. Il blocco di funzionalità di pubblicazione contiene i file ICO e le parti di file necessarie (EXE e DLL) per la pubblicazione del pacchetto. Se presente, il blocco di funzionalità principale include i file ottimizzati per lo streaming durante il processo di sequenziazione.</p></td>
</tr>
</tbody>
</table>

 

## <a name="app-v-client-data-storage-locations"></a><a href="" id="bkmk-files-data-storage"></a>Posizioni di archiviazione dei dati del client App-V


Il client App-V esegue attività per garantire che le applicazioni virtuali funzionino correttamente e funzionino come le applicazioni installate localmente. Il processo di apertura ed esecuzione di applicazioni virtuali richiede il mapping dal file system virtuale e dal Registro di sistema per garantire che l'applicazione abbia i componenti necessari di un'applicazione tradizionale prevista dagli utenti. In questa sezione vengono descritti gli asset necessari per eseguire applicazioni virtuali ed è elencato il percorso in cui App-V archivia gli asset.

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
<td align="left"><p>Backup dei collegamenti</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Archivia i punti di integrazione precedenti che abilitano il ripristino durante l'annullamento della pubblicazione del pacchetto</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Copia in scrittura (COW) Roaming</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Percorso roaming scrivibile per la modifica del pacchetto</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copia in scrittura (COW) Locale</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Percorso non mobile scrivibile per la modifica del pacchetto</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registro di sistema del computer</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene informazioni sullo stato del pacchetto, tra cui VReg per il computer o i pacchetti pubblicati globalmente (hive del computer)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registro di sistema utente</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contiene informazioni sullo stato del pacchetto utente, tra cui VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classi del Registro di sistema utente</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contiene informazioni aggiuntive sullo stato del pacchetto utente</p></td>
</tr>
</tbody>
</table>

 

Ulteriori dettagli per la tabella sono disponibili nella sezione seguente e in tutto il documento.

### <a name="package-store"></a>Archivio pacchetti

Il client App-V gestisce gli asset delle applicazioni montati nell'archivio pacchetti. Questo percorso di archiviazione predefinito è , ma è possibile configurarlo durante o dopo l'installazione utilizzando il comando PowerShell, che modifica il Registro di sistema locale ( valore sotto `%ProgramData%\App-V` `Set-AppVClientConfiguration` la `PackageInstallationRoot` `HKLM\Software\Microsoft\AppV\Client\Streaming` chiave). L'archivio dei pacchetti deve trovarsi in un percorso locale nel sistema operativo client. I singoli pacchetti vengono archiviati nell'archivio pacchetti in sottodirectory denominate per il GUID del pacchetto e il GUID della versione.

Esempio di percorso di un'applicazione specifica:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Per modificare il percorso predefinito dell'archivio pacchetti durante l'installazione, vedi [Come distribuire il client App-V.](how-to-deploy-the-app-v-client-51gb18030.md)

### <a name="shared-content-store"></a>Archivio contenuto condiviso

Se il client App-V è configurato in modalità Archivio contenuto condiviso, non vengono scritti dati su disco quando si verifica un errore di flusso, il che significa che i pacchetti richiedono uno spazio su disco locale minimo (dati di pubblicazione). L'uso di una quantità minore di spazio su disco è molto utile negli ambienti VDI, in cui l'archiviazione locale può essere limitata e lo streaming delle applicazioni da un percorso di rete ad alte prestazioni (ad esempio una san) è preferibile. Per ulteriori informazioni sulla modalità archivio contenuto condiviso, vedere <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Nota**  
Il computer e l'archivio pacchetti devono trovarsi in un'unità locale, anche quando si usano le configurazioni dell'archivio contenuto condiviso per il client App-V.

 

### <a name="package-catalogs"></a>Cataloghi di pacchetti

Il client App-V gestisce i due percorsi basati su file seguenti:

-   **Cataloghi (utente e computer).**

-   **Percorsi del Registro** di sistema: dipende dalla destinazione del pacchetto per la pubblicazione. Esiste un catalogo (archivio dati) per il computer e un catalogo per ogni singolo utente. Nel Catalogo computer vengono archiviate le informazioni globali applicabili a tutti gli utenti o a qualsiasi utente e nel Catalogo utenti vengono archiviate le informazioni applicabili a un utente specifico. Il catalogo è una raccolta di configurazioni dinamiche e file manifesto. sono disponibili dati discreti per file e Registro di sistema per ogni versione del pacchetto. 

### <a name="machine-catalog"></a>Catalogo computer

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Archivia i documenti dei pacchetti disponibili per gli utenti nel computer, quando i pacchetti vengono aggiunti e pubblicati. Tuttavia, se un pacchetto è "globale" al momento della pubblicazione, le integrazioni sono disponibili per tutti gli utenti.</p>
<p>Se un pacchetto non è globale, le integrazioni vengono pubblicate solo per utenti specifici, ma esistono ancora risorse globali che vengono modificate e visibili a chiunque nel computer client (ad esempio, la directory del pacchetto si trova in un percorso su disco condiviso).</p>
<p>Se un pacchetto è disponibile per un utente nel computer (globale o non globale), il manifesto viene archiviato nel Catalogo computer. Quando un pacchetto viene pubblicato a livello globale, esiste un file di configurazione dinamica, archiviato nel Catalogo computer. Di conseguenza, la determinazione del fatto che un pacchetto sia globale viene definita in base al fatto che sia presente un file di criteri (file UserDeploymentConfiguration) nel Catalogo computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso di archiviazione predefinito</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Questa posizione non corrisponde alla posizione dell'archivio pacchetti. L'archivio pacchetti è la copia dorata o intatta dei file del pacchetto.</p></td>
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
<td align="left"><p>Percorso del catalogo computer aggiuntivo, utilizzato quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p>Il percorso seguente è in aggiunta al percorso del pacchetto specifico menzionato in precedenza:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>File aggiuntivi nel catalogo computer quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (gruppo di connessione pubblicato a livello globale)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="user-catalog"></a>Catalogo utenti

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Creato durante il processo di pubblicazione. Contiene informazioni utilizzate per la pubblicazione del pacchetto e utilizzate anche all'avvio per garantire che il provisioning di un pacchetto sia eseguito a un utente specifico. Creato in una posizione di roaming e include informazioni di pubblicazione specifiche dell'utente.</p>
<p>Quando un pacchetto viene pubblicato per un utente, il file dei criteri viene archiviato nel Catalogo utenti. Contemporaneamente, una copia del manifesto viene archiviata anche nel Catalogo utenti. Quando un diritto di pacchetto viene rimosso per un utente, i file del pacchetto pertinenti vengono rimossi dal Catalogo utenti. Esaminando il catalogo utenti, un amministratore può visualizzare la presenza di un file di configurazione dinamica, che indica che il pacchetto è autorizzato per tale utente.</p>
<p>Per gli utenti mobili, il Catalogo utenti deve essere in un percorso condiviso o in roaming per mantenere il comportamento legacy di App-V di destinazione degli utenti per impostazione predefinita. I diritti e i criteri sono associati a un utente e non a un computer, quindi devono eseguire il roaming con l'utente dopo il provisioning.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso di archiviazione predefinito</p></td>
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
<td align="left"><p>Percorso del catalogo utenti aggiuntivo, utilizzato quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p>Il percorso seguente è in aggiunta al percorso del pacchetto specifico menzionato in precedenza:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>File aggiuntivo nel catalogo del computer quando il pacchetto fa parte di un gruppo di connessioni</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <a name="shortcut-backups"></a>Backup dei collegamenti

Durante il processo di pubblicazione, il client App-V esegue il backup di tutti i collegamenti e i punti di integrazione a Questo backup consente il ripristino di questi punti di integrazione alle versioni precedenti quando il pacchetto viene `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` annullato.

### <a name="copy-on-write-files"></a>Copia nei file di scrittura

L'archivio pacchetti contiene una copia intatta dei file del pacchetto trasmessi dal server di pubblicazione. Durante il normale funzionamento di un'applicazione App-V, l'utente o il servizio potrebbe richiedere modifiche ai file. Queste modifiche non vengono apportate nell'archivio pacchetti per mantenere la possibilità di ripristinare l'applicazione, rimuovendo tali modifiche. Queste posizioni, denominate Copy on Write (COW), supportano sia le posizioni mobili che quelle non mobili. Il percorso in cui vengono archiviate le modifiche dipende dalla posizione in cui l'applicazione è stata programmata per scrivere le modifiche in un'esperienza nativa.

### <a name="cow-roaming"></a>ROAMING DI MUCCA

Il percorso DI ROAMING descritto in precedenza archivia le modifiche apportate a file e directory destinati al percorso %AppData% tipico o \\Users\\{username}\\AppData\\Roaming. Tali directory e file vengono quindi esere esere in roaming in base alle impostazioni del sistema operativo.

### <a name="cow-local"></a>LOCALE DI MUCCA

Il percorso locale di COW è simile al percorso di roaming, ma le directory e i file non vengono evasi in altri computer, anche se è stato configurato il supporto per il roaming. La posizione LOCALE DI COW descritta in precedenza archivia le modifiche applicabili alle finestre tipiche e non alla posizione %AppData%. Le directory elencate variano, ma ci saranno due posizioni per tutte le posizioni Windows tipiche (ad esempio, AppData comuni e AppData comuni). S **indica** la posizione con restrizioni quando il servizio virtuale richiede la modifica come utente con privilegi elevati diverso dagli utenti connessi. La posizione non**S** archivia le modifiche basate sull'utente.

## <a name="package-registry"></a><a href="" id="bkmk-pkg-registry"></a>Registro di sistema del pacchetto


Prima che un'applicazione possa accedere ai dati del Registro di sistema del pacchetto, il client App-V deve rendere disponibili per le applicazioni i dati del Registro di sistema del pacchetto. Il client App-V usa il Registro di sistema reale come archivio di supporto per tutti i dati del Registro di sistema.

Quando viene aggiunto un nuovo pacchetto al client App-V, viene creata una copia del Registro di sistema. Il file DAT del pacchetto viene creato in `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . Il nome del file è il GUID della versione con . Estensione DAT. Il motivo per cui questa copia viene effettuata è garantire che il file hive effettivo nel pacchetto non sia mai in uso, impedendo così la rimozione del pacchetto in un secondo momento.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry.dat dall'archivio pacchetti</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</strong></p></td>
</tr>
</tbody>
</table>

 

Quando la prima applicazione del pacchetto viene avviata nel client, il client esegue o copia il contenuto dal file hive, rielizzando i dati del Registro di sistema del pacchetto in un percorso `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` alternativo. I dati del Registro di sistema a fasi hanno due tipi distinti di dati del computer e dati utente. I dati del computer vengono condivisi tra tutti gli utenti del computer. I dati utente vengono a fasi per ogni utente in una posizione specifica `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` dell'utente. I dati del computer vengono infine rimossi al momento della rimozione del pacchetto e i dati utente vengono rimossi in un'operazione di annullamento della pubblicazione da parte dell'utente.

### <a name="package-registry-staging-vs-connection-group-registry-staging"></a>Gestione temporanea del Registro di sistema del pacchetto e gestione temporanea del Registro di sistema del gruppo di connessione

Quando i gruppi di connessione sono presenti, il processo precedente di gestione temporanea del Registro di sistema ha valore true, ma invece di avere un file hive da elaborare, ne esistono più di uno. I file vengono elaborati nell'ordine in cui vengono visualizzati nel file XML del gruppo di connessione, con il primo writer che vince eventuali conflitti.

Il Registro di sistema a fasi persiste come nel caso di un singolo pacchetto. I dati del Registro di sistema degli utenti a fasi rimangono per il gruppo di connessione fino a quando non vengono disabilitati. I dati del Registro di sistema del computer a fasi vengono rimossi durante la rimozione del gruppo di connessioni.

### <a name="virtual-registry"></a>Registro di sistema virtuale

Lo scopo del Registro di sistema virtuale (VREG) è fornire una singola visualizzazione unita del Registro di sistema del pacchetto e del Registro di sistema nativo alle applicazioni. Fornisce inoltre la funzionalità di copia in scrittura (COW), ovvero qualsiasi modifica apportata al Registro di sistema dal contesto di un processo virtuale viene apportata a un percorso DISA separato. Ciò significa che VREG deve combinare fino a tre posizioni separate del Registro di sistema in una singola visualizzazione in base alle posizioni popolate nel Registro di sistema COW - &gt; pacchetto - &gt; nativo. Quando viene effettuata una richiesta per i dati del Registro di sistema, verrà individuata nell'ordine fino a quando non trova i dati che richiedeva. Ciò significa che se è presente un valore archiviato in una posizione DISA, non procederà ad altre posizioni, tuttavia, se non vi sono dati nella posizione DI COW, procederà al pacchetto e quindi alla posizione nativa fino a quando non troverà i dati appropriati.

### <a name="registry-locations"></a>Posizioni del Registro di sistema

Esistono due percorsi del Registro di sistema del pacchetto e due percorsi dei gruppi di connessione in cui il client App-V archivia le informazioni del Registro di sistema, a seconda che il pacchetto sia pubblicato singolarmente o come parte di un gruppo di connessione. Esistono tre percorsi DISA per i pacchetti e tre per i gruppi di connessione, creati e gestiti da VREG. Impostazioni pacchetti e gruppi di connessione non sono condivisi:

**VReg pacchetto singolo:**

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
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY (Solo il processo elevate può scrivere)</p></li>
<li><p>User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</p></li>
<li><p>User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacchetto</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Classi del Registro di sistema utente\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Percorso del Registro di sistema dell'applicazione nativa</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Gruppo di connessione VReg:**

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
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (solo il processo elevate può scrivere)</p></li>
<li><p>User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Qualsiasi elemento scritto in HKCU tranne Software\Classes</p></li>
<li><p>Classi del Registro di sistema utente\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacchetto</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Classi del Registro di sistema utente\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Percorso del Registro di sistema dell'applicazione nativa</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Esistono due posizioni DISA per HKLM; processi elevati e non elevati. I processi con privilegi elevati scrivono sempre le modifiche HKLM nell'applicazione sicura DISA in HKLM. I processi non con privilegi elevati scrivono sempre le modifiche HKLM nell'oggetto NON SICURO DI COW in HKCU\\Software\\Classes. Quando un'applicazione legge le modifiche da HKLM, i processi con privilegi elevati leggeranno le modifiche dalla protezione di COW in HKLM. Le operazioni di lettura con privilegi non elevati vengono effettuate da entrambi, favorendo innanzitutto le modifiche apportate all'elemento NON sicuro.

### <a name="pass-through-keys"></a>Chiavi pass-through

Le chiavi pass-through consentono a un amministratore di configurare determinate chiavi in modo che possano essere lette solo dal Registro di sistema nativo, ignorando i percorsi Package e COW. I percorsi pass-through sono globali per il computer (non specifici del pacchetto) e possono essere configurati aggiungendo il percorso alla chiave, che deve essere considerato come pass-through per il valore **REG\_MULTI\_SZ** denominato **PassThroughPaths** della chiave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Qualsiasi chiave visualizzata sotto questo valore multi-stringa (e i relativi figli) verrà considerata pass-through.

Per impostazione predefinita, le posizioni seguenti sono configurate come posizioni pass-through:

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Impostazioni\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Impostazioni\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Impostazioni

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Policies

Lo scopo delle chiavi pass-through è garantire che un'applicazione virtuale non scrivo i dati del Registro di sistema nel VReg necessario per le applicazioni non virtuali per il corretto funzionamento o l'integrazione. La chiave Criteri garantisce che le impostazioni basate su Criteri di gruppo impostate dall'amministratore siano utilizzate e non in base alle impostazioni del pacchetto. La chiave AppModel è necessaria per l'integrazione con Windows moderne applicazioni basate sull'interfaccia utente. È consigliabile che gli amministratori non modificano le chiavi pass-through predefinite, ma in alcuni casi, in base al comportamento dell'applicazione potrebbe essere necessario aggiungere altre chiavi pass-through.

## <a name="app-v-package-store-behavior"></a><a href="" id="bkmk-pkg-store-behavior"></a>Comportamento dell'archivio pacchetti app-V


App-V 5 gestisce l'archivio pacchetti, ovvero il percorso in cui vengono archiviati i file di asset espansi dal file appv. Per impostazione predefinita, questa posizione è archiviata in %ProgramData%\\App-V ed è limitata in termini di funzionalità di archiviazione solo dallo spazio libero su disco. L'archivio pacchetti è organizzato in base ai GUID per il pacchetto e la versione, come indicato nella sezione precedente.

### <a name="add-packages"></a>Aggiungere pacchetti

I pacchetti App-V vengono a fasi dopo l'aggiunta al computer con il client App-V. Il client App-V fornisce la gestione temporanea su richiesta. Durante la pubblicazione o un oggetto Add-AppVClientPackage manuale, la struttura dei dati viene compilata nell'archivio pacchetti (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). I file di pacchetto identificati nel blocco di pubblicazione definito nel StreamMap.xml vengono aggiunti al sistema e le cartelle di primo livello e i file figlio vengono a fasi per garantire che all'avvio siano presenti asset dell'applicazione adeguati.

### <a name="mounting-packages"></a>Pacchetti di montaggio

I pacchetti possono essere caricati in modo esplicito tramite PowerShell o tramite l'interfaccia utente del `Mount-AppVClientPackage` **client App-V** per scaricare un pacchetto. Questa operazione carica completamente l'intero pacchetto nell'archivio pacchetti.

### <a name="streaming-packages"></a>Pacchetti di streaming

Il client App-V può essere configurato per modificare il comportamento predefinito dello streaming. Tutti i criteri di streaming vengono archiviati nella chiave del Registro di sistema seguente: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . I criteri vengono impostati utilizzando il cmdlet PowerShell `Set-AppvClientConfiguration` . I criteri seguenti si applicano allo streaming:

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
<td align="left"><p>In Windows 8 e versioni successive, consente lo streaming su 3G e reti cellulari</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Specifica l'impostazione Caricamento in background:</p>
<p><strong>0 </strong> - Disabilitato</p>
<p><strong>1 </strong> - Solo pacchetti usati in precedenza</p>
<p><strong>2 </strong> - Tutti i pacchetti</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>La cartella radice per l'archivio pacchetti nel computer locale</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>Override radice da cui devono essere trasmessi i pacchetti</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Abilita l'utilizzo dell'archivio contenuto condiviso per scenari VDI</p></td>
</tr>
</tbody>
</table>

 

 

Queste impostazioni influiscono sul comportamento dello streaming degli asset del pacchetto App-V nel client. Per impostazione predefinita, App-V scarica solo gli asset necessari dopo il download della pubblicazione iniziale e dei blocchi di funzionalità principali. Esistono tre comportamenti specifici per i pacchetti di streaming che devono essere spiegati:

-   Background Streaming

-   Streaming ottimizzato

-   Errori di flusso

### <a name="background-streaming"></a>Streaming in background

Il cmdlet PowerShell può essere utilizzato per determinare la modalità corrente per il flusso in background con l'impostazione AutoLoad e modificato con il cmdlet Set-AppvClientConfiguration o dal Registro di sistema `Get-AppvClientConfiguration` (chiave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming). Lo streaming in background è un'impostazione predefinita in cui l'impostazione Di caricamento automatico è impostata per scaricare i pacchetti usati in precedenza. Il comportamento basato sull'impostazione predefinita (valore=1) scarica i blocchi di dati di App-V in background dopo l'avvio dell'applicazione. Questa impostazione può essere disabilitata tutti insieme (valore=0) o abilitata per tutti i pacchetti (valore=2), indipendentemente dal fatto che siano stati avviati.

### <a name="optimized-streaming"></a>Streaming ottimizzato

I pacchetti App-V possono essere configurati con un blocco di funzionalità principale durante la sequenziazione. Questa impostazione consente al tecnico della sequenziazione di monitorare i file di avvio per un'applicazione o applicazioni specifiche e contrassegnare i blocchi di dati nel pacchetto App-V per lo streaming al primo avvio di qualsiasi applicazione nel pacchetto.

### <a name="stream-faults"></a>Errori di flusso

Dopo il flusso iniziale di tutti i dati di pubblicazione e il blocco di funzionalità principale, le richieste di file aggiuntivi eseguono errori di flusso. Questi blocchi di dati vengono scaricati nell'archivio pacchetti in base alle esigenze. In questo modo un utente può scaricare solo una piccola parte del pacchetto, in genere sufficiente per avviare il pacchetto ed eseguire attività normali. Tutti gli altri blocchi vengono scaricati quando un utente avvia un'operazione che richiede dati non presenti nell'archivio pacchetti.

Per altre informazioni sullo streaming del pacchetto App-V, visita: <https://go.microsoft.com/fwlink/?LinkId=392770> .

La sequenziazione per l'ottimizzazione dello streaming è disponibile all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### <a name="package-upgrades"></a>Aggiornamenti dei pacchetti

I pacchetti App-V richiedono l'aggiornamento durante tutto il ciclo di vita dell'applicazione. Gli aggiornamenti del pacchetto App-V sono simili all'operazione di pubblicazione del pacchetto, in quanto ogni versione verrà creata nel proprio percorso PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . L'operazione di aggiornamento viene ottimizzata creando collegamenti rigidi a file identici e trasmessi da altre versioni dello stesso pacchetto.

### <a name="package-removal"></a>Rimozione del pacchetto

Il comportamento del client App-V quando i pacchetti vengono rimossi dipende dal metodo utilizzato per la rimozione. Se si utilizza un'infrastruttura completa di App-V per annullare la pubblicazione dell'applicazione, i file di catalogo utente (catalogo computer per le applicazioni pubblicate globalmente) vengono rimossi, ma vengono mantenuti il percorso dell'archivio pacchetti e i percorsi DISA. Quando il cmdlet PowerShell `Remove-AppVClientPackge` viene utilizzato per rimuovere un pacchetto App-V, il percorso dell'archivio pacchetti viene pulito. Tenere presente che l'annullamento della pubblicazione di un pacchetto App-V dal server di gestione non esegue un'operazione di rimozione. Nessuna delle due operazioni rimuoverà i file del pacchetto dell'archivio pacchetti.

## <a name="roaming-registry-and-data"></a><a href="" id="bkmk-roaming-reg-data"></a>Roaming del Registro di sistema e dei dati


App-V 5 è in grado di offrire un'esperienza quasi nativa durante il roaming, a seconda di come viene scritta l'applicazione in uso. Per impostazione predefinita, App-V evade AppData archiviati nella posizione di roaming, in base alla configurazione roaming del sistema operativo. Altri percorsi per l'archiviazione dei dati basati su file non esere in roaming da un computer all'altro, poiché si tratta di percorsi che non vengono evasi.

### <a name="roaming-requirements-and-user-catalog-data-storage"></a><a href="" id="bkmk-clt-inter-roam-reqs"></a>Requisiti di roaming e archiviazione dei dati del catalogo utenti

App-V archivia i dati, che rappresentano lo stato del catalogo dell'utente, sotto forma di:

-   File in %appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Impostazioni del Registro di sistema in `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Insieme, questi file e le impostazioni del Registro di sistema rappresentano il catalogo dell'utente, quindi entrambi devono essere di roaming o nessuno dei due deve essere in roaming per un determinato utente. App-V non supporta il roaming di %AppData%, ma non il roaming del profilo dell'utente (Registro di sistema) o viceversa.

**Nota**  
Il cmdlet **Repair-AppvClientPackage** non ripristina lo stato di pubblicazione dei pacchetti, in cui lo stato App-V dell'utente in cui si trova è mancante o non corrisponde ai dati `HKEY_CURRENT_USER` in %appdata%.

 

### <a name="registry-based-data"></a>Dati basati sul Registro di sistema

Il roaming del Registro di sistema di App-V è suddiviso in due scenari, come illustrato nella tabella seguente.

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
<td align="left"><p>Quando un utente standard avvia un'applicazione App-V, HKLM e HKCU per le applicazioni App-V vengono archiviati nell'hive HKCU nel computer. Si presenta come due percorsi distinti:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</p></li>
</ul>
<p>Le posizioni sono abilitate per il roaming in base alle impostazioni del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicazioni eseguite con elevazione</p></td>
<td align="left"><p>Quando un'applicazione viene avviata con l'elevazione:</p>
<ul>
<li><p>I dati HKLM vengono archiviati nell'hive HKLM nel computer locale</p></li>
<li><p>I dati HKCU vengono archiviati nel percorso del Registro di sistema dell'utente</p></li>
</ul>
<p>In questo scenario, queste impostazioni non vengono visualizzate con le normali configurazioni mobili del sistema operativo e le chiavi e i valori del Registro di sistema risultanti vengono archiviati nel percorso seguente:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="app-v-and-folder-redirection"></a>Reindirizzamento di app-V e cartelle

App-V 5.1 supporta il reindirizzamento delle cartelle della cartella AppData mobile (%AppData%). Quando viene avviato l'ambiente virtuale, lo stato AppData roaming dalla directory AppData mobile dell'utente viene copiato nella cache locale. Al contrario, quando l'ambiente virtuale viene arrestato, la cache locale associata a AppData mobile di un utente specifico viene trasferita alla posizione effettiva della directory AppData mobile di tale utente.

Un pacchetto tipico ha diverse posizioni mappate nell'archivio di supporto dell'utente per le impostazioni sia in AppData\\Local che in AppData\\Roaming. Questi percorsi sono i percorsi copia in scrittura archiviati per utente nel profilo dell'utente e che vengono utilizzati per archiviare le modifiche apportate alle directory VFS del pacchetto e per proteggere il pacchetto VFS predefinito.

La tabella seguente mostra i percorsi locali e mobili, quando non è stato implementato il reindirizzamento delle cartelle.

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
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

La tabella seguente mostra i percorsi locali e mobili, quando il reindirizzamento delle cartelle è stato implementato per %AppData% e il percorso è stato reindirizzato (in genere a un percorso di rete).

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
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Il driver VFS del client App-V corrente non può scrivere nei percorsi di rete, quindi il client App-V rileva la presenza del reindirizzamento delle cartelle e copia i dati nell'unità locale durante la pubblicazione e l'avvio dell'ambiente virtuale. Dopo che l'utente chiude l'applicazione App-V e il client App-V chiude l'ambiente virtuale, l'archiviazione locale di VFS AppData viene copiata di nuovo nella rete, consentendo il roaming in altri computer, in cui il processo verrà ripetuto. I passaggi dettagliati dei processi sono:

1.  Durante la pubblicazione o l'avvio dell'ambiente virtuale, il client App-V rileva il percorso della directory AppData.

2.  Se il percorso AppData roaming è locale o ino AppData\\Roaming è mappato, non accade nulla.

3.  Se il percorso AppData mobile non è locale, la directory AppData VFS viene mappata alla directory AppData locale.

Questo processo risolve il problema di un %AppData% non locale non supportato dal driver VFS client App-V. Tuttavia, i dati archiviati in questa nuova posizione non vengono evasi con il reindirizzamento delle cartelle. Tutte le modifiche apportate durante l'esecuzione dell'applicazione vengono apportate al percorso AppData locale e devono essere copiate nel percorso reindirizzato. I passaggi dettagliati di questo processo sono:

1.  L'applicazione App-V viene arrestata, che arresta l'ambiente virtuale.

2.  La cache locale del percorso AppData mobile viene compressa e archiviata in un file ZIP.

3.  Un timestamp alla fine del processo di creazione del pacchetto ZIP viene usato per assegnare un nome al file.

4.  Il timestamp viene registrato nel Registro di sistema: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime come ultimo timestamp AppData noto.

5.  Il processo di reindirizzamento delle cartelle viene chiamato per valutare e avviare il file ZIP caricato nella directory AppData mobile.

Il timestamp viene usato per determinare uno scenario "last writer wins" in caso di conflitto e viene usato per ottimizzare il download dei dati quando viene pubblicata l'applicazione App-V o viene avviato l'ambiente virtuale. Il reindirizzamento delle cartelle rende disponibili i dati di qualsiasi altro client coperto dal criterio di supporto e avvia il processo di archiviazione dei dati AppData\\Roaming nel percorso AppData locale nel client. I processi dettagliati sono:

1.  L'utente avvia l'ambiente virtuale avviando un'applicazione.

2.  L'ambiente virtuale dell'applicazione verifica la presenza del file ZIP con timestamp più recente, se presente.

3.  Nel Registro di sistema viene verificata la data e l'ora dell'ultimo caricamento noto, se presente.

4.  Il file ZIP più recente viene scaricato a meno che il timestamp dell'ultimo caricamento noto locale non sia maggiore o uguale al timestamp del file ZIP.

5.  Se il timestamp dell'ultimo caricamento noto locale è precedente a quello del file ZIP più recente nel percorso AppData mobile, il file ZIP viene estratto nella directory temporanea locale nel profilo dell'utente.

6.  Dopo aver estratto correttamente il file ZIP, la cache locale della directory AppData mobile viene rinominata e i nuovi dati vengono spostati sul posto.

7.  La directory rinominata viene eliminata e l'applicazione viene aperta con i dati AppData mobili salvati più di recente.

In questo modo viene completato il roaming corretto delle impostazioni dell'applicazione presenti in AppData\\Roaming locations. L'unica altra condizione che deve essere affrontata è un'operazione di ripristino del pacchetto. I dettagli del processo sono:

1.  Durante il ripristino, rileva se il percorso della directory AppData mobile dell'utente non è locale.

2.  Mappare le destinazioni del percorso AppData roaming non locale vengono ricreate le posizioni appData locali e roaming previste.

3.  Eliminare il timestamp archiviato nel Registro di sistema, se presente.

Questo processo creerà nuovamente i percorsi locali e di rete per AppData e rimuoverà il record del Registro di sistema del timestamp.

## <a name="app-v-client-application-lifecycle-management"></a><a href="" id="bkmk-clt-app-lifecycle"></a>Gestione del ciclo di vita delle applicazioni client App-V


In un'infrastruttura completa di App-V, dopo la sequenza delle applicazioni vengono gestite e pubblicate per utenti o computer tramite i server di gestione e pubblicazione di App-V. In questa sezione vengono fornite informazioni dettagliate sulle operazioni che si verificano durante le operazioni comuni relative al ciclo di vita dell'applicazione App-V (aggiunta, pubblicazione, avvio, aggiornamento e rimozione) e i percorsi dei file e del Registro di sistema modificati dal punto di vista del client App-V. Le operazioni del client App-V vengono eseguite come una serie di comandi di PowerShell avviati nel computer che esegue il client App-V.

Questo documento si concentra sulle soluzioni di infrastruttura completa app-V. Per informazioni specifiche sull'integrazione di App-V con Configuration Manager 2012, visitare: <https://go.microsoft.com/fwlink/?LinkId=392773> .

Le attività del ciclo di vita dell'applicazione App-V vengono attivate all'accesso dell'utente (impostazione predefinita), all'avvio del computer o come operazioni a tempo in background. Le impostazioni per le operazioni del client App-V, inclusi i server di pubblicazione, gli intervalli di aggiornamento, l'abilitazione dello script del pacchetto e altri, vengono configurate durante l'installazione del client o dopo l'installazione con i comandi di PowerShell. Vedere la sezione How to Deploy the Client in TechNet all'indirizzo: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md) or utilize the PowerShell:

```powershell
get-command *appv*
```

### <a name="publishing-refresh"></a>Aggiornamento della pubblicazione

Il processo di aggiornamento della pubblicazione è costituito da diverse operazioni più piccole eseguite nel client App-V. Poiché App-V è una tecnologia di virtualizzazione delle applicazioni e non una tecnologia di pianificazione delle attività, l'Utilità di pianificazione di Windows viene utilizzata per abilitare il processo all'accesso dell'utente, all'avvio del computer e a intervalli pianificati. La configurazione del client durante l'installazione sopra elencata è il metodo preferito quando si distribuisce il client a un gruppo di computer di grandi dimensioni con le impostazioni corrette. Queste impostazioni client possono essere configurate con i cmdlet di PowerShell seguenti:

-   **Add-AppVPublishingServer:** Configura il client con un server di pubblicazione App-V che fornisce pacchetti App-V.

-   **Set-AppVPublishingServer:** Modifica le impostazioni correnti per il server di pubblicazione App-V.

-   **Set-AppVClientConfiguration:** Modifica le impostazioni correnti per il client App-V.

-   **Sync-AppVPublishingServer:** Avvia manualmente un processo di aggiornamento della pubblicazione app-V. Viene inoltre utilizzato nelle attività pianificate create durante la configurazione del server di pubblicazione.

L'obiettivo delle sezioni seguenti è quello di illustrare in dettaglio le operazioni che si verificano durante le diverse fasi di un aggiornamento della pubblicazione di App-V. Gli argomenti includono:

-   Aggiunta di un pacchetto App-V

-   Pubblicazione di un pacchetto App-V

### <a name="adding-an-app-v-package"></a>Aggiunta di un pacchetto App-V

L'aggiunta di un pacchetto App-V al client è il primo passaggio del processo di aggiornamento della pubblicazione. Il risultato finale è lo stesso del cmdlet in PowerShell, tranne che durante il processo di aggiunta dell'aggiornamento della pubblicazione, il server di pubblicazione configurato viene contattato e passa un elenco di applicazioni di alto livello al client per estrarre informazioni più dettagliate e non un'operazione di aggiunta di un singolo `Add-AppVClientPackage` pacchetto. Il processo continua configurando il client per le aggiunte o gli aggiornamenti del pacchetto o del gruppo di connessione, quindi accede al file appv. Successivamente, il contenuto del file appv viene espanso e posizionato nel sistema operativo locale nelle posizioni appropriate. Di seguito è riportato un flusso di lavoro dettagliato del processo, presupponendo che il pacchetto sia configurato per il flusso di errore.

**Come aggiungere un pacchetto App-V**

1.  Avvio manuale tramite PowerShell o avvio della sequenza di attività del processo di aggiornamento della pubblicazione.

    1.  Il client App-V effettua una connessione HTTP e richiede un elenco di applicazioni in base alla destinazione. Il processo di aggiornamento della pubblicazione supporta i computer o gli utenti di destinazione.

    2.  Il server di pubblicazione App-V utilizza l'identità della destinazione di avvio, dell'utente o del computer ed esegue una query nel database per un elenco delle applicazioni autorizzate. L'elenco delle applicazioni viene fornito come risposta XML, che il client utilizza per inviare ulteriori richieste al server per ulteriori informazioni in base al pacchetto.

2.  L'agente di pubblicazione nel client App-V esegue tutte le azioni seguenti serializzate.

    Valutare eventuali gruppi di connessioni non pubblicati o disabilitati, poiché gli aggiornamenti della versione del pacchetto che fanno parte del gruppo di connessione non possono essere elaborati.

3.  Configurare i pacchetti identificando le operazioni Add o Update.

    1.  Il client App-V utilizza l'API AppX da Windows e accede al file appv dal server di pubblicazione.

    2.  Il file del pacchetto viene aperto e le AppXManifest.xml e StreamMap.xml vengono scaricate nell'archivio pacchetti.

    3.  Trasmettere completamente i dati dei blocchi di pubblicazione definiti nel StreamMap.xml. Archivia i dati dei blocchi di pubblicazione nell'archivio pacchetti\\PkgGUID\\VerGUID\\Root.

        -   Icone: destinazioni dei punti di estensione.

        -   Intestazioni pe (Portable Executable Headers): destinazioni dei punti di estensione che contengono le informazioni di base sulla necessità di un'immagine su disco, accessibili direttamente o tramite tipi di file.

        -   Script: consente di scaricare la directory degli script da utilizzare durante tutto il processo di pubblicazione.

    4.  Popolare l'archivio pacchetti:

        1.  Creare file di tipo sparse su disco che rappresentano il pacchetto estratto per tutte le directory elencate.

        2.  Stage top level files and directories under root.

        3.  Tutti gli altri file vengono creati quando la directory viene elencata come sparse sul disco e trasmessa su richiesta.

    5.  Creare le voci del catalogo computer. Crea le Manifest.xml e DeploymentConfiguration.xml dai file del pacchetto (se non viene creato DeploymentConfiguration.xml file nel pacchetto un segnaposto).

    6.  Creare il percorso dell'archivio pacchetti nel Registro di sistema HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Creare il file Registry.dat dall'archivio pacchetti a %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat

    8.  Registrare il pacchetto con il driver in modalità kernel di App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Richiama script dal file AppxManifest.xml o DeploymentConfig.xml per la tempistica di aggiunta del pacchetto.

4.  Configurare i gruppi di connessioni aggiungendo e abilitando o disabilitando.

5.  Rimuovere gli oggetti non pubblicati nella destinazione (utente o computer).

    **Nota**  
    In questo modo non verrà eseguita l'eliminazione di un pacchetto, bensì verranno eliminati i punti di integrazione per la destinazione specifica (utente o computer) e verranno eliminati i file di catalogo degli utenti (file di catalogo dei computer per la pubblicazione globale).

     

6.  Richiamare il montaggio del carico in background in base alla configurazione del client.

7.  I pacchetti che dispongono già di informazioni di pubblicazione per il computer o l'utente vengono ripristinati immediatamente.

    **Nota**  
    Questa condizione si verifica come prodotto della rimozione senza annullare la pubblicazione con l'aggiunta in background del pacchetto.

     

In questo modo viene completata l'aggiunta di un pacchetto App-V del processo di aggiornamento della pubblicazione. Il passaggio successivo consiste nella pubblicazione del pacchetto nella destinazione specifica (computer o utente).

![pacchetto aggiungere file e dati del Registro di sistema.](images/packageaddfileandregistrydata.png)

### <a name="publishing-an-app-v-package"></a>Pubblicazione di un pacchetto App-V

Durante l'operazione di aggiornamento della pubblicazione, l'operazione di pubblicazione specifica (Publish-AppVClientPackage) aggiunge voci al catalogo utente, mappa il diritto all'utente, identifica l'archivio locale e termina completando i passaggi di integrazione. Di seguito sono riportati i passaggi dettagliati.

**Come pubblicare e pacchetto App-V**

1.  Le voci del pacchetto vengono aggiunte al catalogo utenti

    1.  Pacchetti destinati all'utente: UserDeploymentConfiguration.xml e UserManifest.xml vengono posizionati nel computer nel Catalogo utenti

    2.  Pacchetti di destinazione del computer (globali): la UserDeploymentConfiguration.xml viene inserita nel Catalogo computer

2.  Registrare il pacchetto con il driver in modalità kernel per l'utente in HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Eseguire attività di integrazione.

    1.  Creare punti di estensione.

    2.  Archiviare le informazioni di backup nel Registro di sistema e nel profilo mobile dell'utente (backup dei collegamenti).

        **Nota**  
        In questo modo vengono abilitati i punti di estensione di ripristino se il pacchetto non viene pubblicato.

         

    3.  Eseguire script destinati alla tempistica di pubblicazione.

La pubblicazione di un pacchetto App-V che fa parte di un gruppo di connessione è molto simile al processo precedente. Per i gruppi di connessioni, il percorso in cui sono archiviate le informazioni specifiche del catalogo include PackageGroups come figlio della directory del catalogo. Per informazioni dettagliate, esaminare le informazioni del catalogo del computer e degli utenti sopra riportate.

![package add file and registry data - global.](images/packageaddfileandregistrydata-global.png)

### <a name="application-launch"></a>Avvio dell'applicazione

Dopo il processo di aggiornamento della pubblicazione, l'utente avvia e successivamente avvia nuovamente un'applicazione App-V. Il processo è molto semplice e ottimizzato per l'avvio rapido con un minimo di traffico di rete. Il client App-V controlla il percorso del catalogo utente per i file creati durante la pubblicazione. Dopo aver stabilito i diritti per avviare il pacchetto, il client App-V crea un ambiente virtuale, avvia il flusso dei dati necessari e applica i file di configurazione di distribuzione e manifesto appropriati durante la creazione dell'ambiente virtuale. Con l'ambiente virtuale creato e configurato per il pacchetto e l'applicazione specifici, viene avviata l'applicazione.

**Come avviare applicazioni App-V**

1.  L'utente avvia l'applicazione facendo clic su un collegamento o una chiamata al tipo di file.

2.  Il client App-V verifica l'esistenza nel Catalogo utenti per i file seguenti

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Se i file sono presenti, l'applicazione ha diritto all'utente specifico e l'applicazione avvierà il processo per l'avvio. Non c'è traffico di rete a questo punto.

4.  Successivamente, il client App-V verifica che il percorso del pacchetto registrato per il servizio client App-V sia presente nel Registro di sistema.

5.  Dopo aver trovato il percorso dell'archivio pacchetti, viene creato l'ambiente virtuale. Se si tratta del primo avvio, il blocco di funzionalità principale viene scaricato, se presente.

6.  Dopo il download, il servizio client App-V utilizza il manifesto e i file di configurazione della distribuzione per configurare l'ambiente virtuale e vengono caricati tutti i sottosistemi App-V.

7.  L'applicazione viene avviata. Per gli eventuali file mancanti nell'archivio dei pacchetti (file sparse), App-V inserirà i file in base alle esigenze.

    ![package add file and registry data - stream.](images/packageaddfileandregistrydata-stream.png)

### <a name="upgrading-an-app-v-package"></a>Aggiornamento di un pacchetto App-V

Il processo di aggiornamento del pacchetto App-V 5 è diverso dalle versioni precedenti di App-V. App-V supporta più versioni dello stesso pacchetto in un computer autorizzato a utenti diversi. Le versioni dei pacchetti possono essere aggiunte in qualsiasi momento quando l'archivio pacchetti e i cataloghi vengono aggiornati con le nuove risorse. L'unico processo specifico per l'aggiunta di nuove risorse di versione è l'ottimizzazione dell'archiviazione. Durante un aggiornamento, solo i nuovi file vengono aggiunti al nuovo percorso dell'archivio delle versioni e vengono creati collegamenti rigidi per i file non modificati. In questo modo si riduce l'archiviazione complessiva presentando il file solo in un percorso su disco e quindi proiettando il file in tutte le cartelle con una voce relativa al percorso del file sul disco. I dettagli specifici dell'aggiornamento di un pacchetto App-V sono i seguenti:

**Come aggiornare un pacchetto App-V**

1.  Il client App-V esegue un aggiornamento della pubblicazione e individua una versione più recente di un pacchetto App-V.

2.  Le voci del pacchetto vengono aggiunte al catalogo appropriato per la nuova versione

    1.  Pacchetti di destinazione dell'utente: il UserDeploymentConfiguration.xml e il UserManifest.xml vengono posizionati nel computer nel catalogo utenti in appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Pacchetti di destinazione del computer (globali): il UserDeploymentConfiguration.xml viene inserito nel catalogo del computer in %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Registrare il pacchetto con il driver in modalità kernel per l'utente in HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Eseguire attività di integrazione.

    -   Integrare i punti di estensione (EP) dai file manifesto e di configurazione dinamica.

    1.  I dati EP basati su file vengono archiviati nella cartella AppData utilizzando i punti di giunzione dall'archivio pacchetti.

    2.  I EP versione 1 esistono già quando una nuova versione diventa disponibile.

    3.  I punti di estensione vengono commutati al percorso versione 2 nei cataloghi di computer o utenti per qualsiasi punto di estensione più recente o aggiornato.

5.  Eseguire script destinati alla tempistica di pubblicazione.

6.  Installare assembly affiancati in base alle esigenze.

### <a name="upgrading-an-in-use-app-v-package"></a>Aggiornamento di un pacchetto App-V in uso

**A partire da App-V 5 SP2:** se si tenta di aggiornare un pacchetto in uso da un utente finale, l'attività di aggiornamento viene posizionata in uno stato in sospeso. L'aggiornamento verrà eseguito in un secondo momento, in base alle regole seguenti:

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
<td align="left"><p>Attività basata sull'utente, ad esempio la pubblicazione di un pacchetto a un utente</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita dopo la disconnettersi e quindi l'accesso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basata su livello globale, ad esempio l'abilitazione di un gruppo di connessione a livello globale</p></td>
<td align="left"><p>L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</p></td>
</tr>
</tbody>
</table>

 

Quando un'attività viene inserita in uno stato in sospeso, il client App-V genera anche una chiave del Registro di sistema per l'attività in sospeso, come indicato di seguito:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività basata sull'utente o a livello globale</th>
<th align="left">Dove viene generata la chiave del Registro di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività basate sull'utente</p></td>
<td align="left"><p>KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Attività basate su livello globale</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Prima che gli utenti possano utilizzare la versione più recente del pacchetto, è necessario completare le operazioni seguenti:

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
<td align="left"><p>Questa attività è specifica del computer ed è possibile eseguirla in qualsiasi momento completando i passaggi descritti nella sezione Aggiunta pacchetto precedente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pubblicare il pacchetto</p></td>
<td align="left"><p>Per la procedura, vedi la sezione Pubblicazione pacchetti sopra riportata. Questo processo richiede l'aggiornamento dei punti di estensione nel sistema. Gli utenti finali non possono utilizzare l'applicazione al termine di questa attività.</p></td>
</tr>
</tbody>
</table>

 

Usa gli scenari di esempio seguenti come guida per l'aggiornamento dei pacchetti.

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
<p>L'amministratore pubblica una versione più recente del pacchetto e l'aggiornamento funziona al successivo avvio di un componente o di un'applicazione all'interno del pacchetto. La nuova versione del pacchetto viene trasmessa ed eseguita. Nulla è cambiato in questo scenario in App-V 5 SP2 rispetto alle versioni precedenti di App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Il pacchetto App-V è in uso quando l'amministratore pubblica una versione più recente del pacchetto</p></td>
<td align="left"><p>L'operazione di aggiornamento viene impostata su pending dal client App-V, il che significa che viene accodata ed eseguita in un secondo momento quando il pacchetto non è in uso.</p>
<p>Se l'applicazione del pacchetto è in uso, l'utente arresta l'applicazione virtuale, dopo di che può verificarsi l'aggiornamento.</p>
<p>Se il pacchetto ha estensioni della shell (Office 2013), che vengono caricate in modo permanente da Windows Explorer, l'utente non può essere connesso. Gli utenti devono disconnettersi e accedere di nuovo per avviare l'aggiornamento del pacchetto App-V.</p></td>
</tr>
</tbody>
</table>

 

### <a name="global-vs-user-publishing"></a>Pubblicazione globale e utente

I pacchetti App-V possono essere pubblicati in uno dei due modi seguenti. Utente che autorizza un pacchetto App-V a uno specifico utente o gruppo di utenti e Global che autorizza il pacchetto App-V all'intero computer per tutti gli utenti del computer. Una volta che un aggiornamento del pacchetto è stato pendeto e il pacchetto App-V non è in uso, considerare i due tipi di pubblicazione:

-   **Globally published**: l'applicazione viene pubblicata in un computer; tutti gli utenti del computer possono usarlo. L'aggiornamento verrà eseguito all'avvio del servizio client App-V, ovvero un riavvio del computer.

-   **Utente pubblicato**: l'applicazione viene pubblicata per un utente. Se nel computer sono presenti più utenti, l'applicazione può essere pubblicata in un sottoinsieme degli utenti. L'aggiornamento verrà eseguito quando l'utente esegue l'accesso o quando viene pubblicato di nuovo (periodicamente, aggiornamento e valutazione dei criteri di ConfigMgr o pubblicazione/aggiornamento periodico di App-V o in modo esplicito tramite comandi di PowerShell).

### <a name="removing-an-app-v-package"></a>Rimozione di un pacchetto App-V

La rimozione di applicazioni App-V in un'infrastruttura completa è un'operazione di annullamento della pubblicazione e non esegue la rimozione di un pacchetto. Il processo è lo stesso del processo di pubblicazione precedente, ma invece di aggiungere il processo di rimozione inverte le modifiche apportate per i pacchetti App-V.

### <a name="repairing-an-app-v-package"></a>Ripristino di un pacchetto App-V

L'operazione di ripristino è molto semplice, ma può influire su molte posizioni nel computer. Le posizioni di Copia in scrittura (COW) menzionate in precedenza vengono rimosse e i punti di estensione vengono de-integrati e quindi ri-integrati. Esaminare le posizioni di posizionamento dei dati DI COW esaminando dove sono registrati nel Registro di sistema. Questa operazione viene eseguita automaticamente e non esiste alcun controllo amministrativo diverso dall'avvio di un'operazione di ripristino dalla console client app-V o tramite PowerShell (Repair-AppVClientPackage).

## <a name="integration-of-app-v-packages"></a><a href="" id="bkmk-integr-appv-pkgs"></a>Integrazione di pacchetti App-V


L'architettura del pacchetto e del client App-V fornisce un'integrazione specifica con il sistema operativo locale durante l'aggiunta e la pubblicazione dei pacchetti. Tre file definiscono i punti di integrazione o di estensione per un pacchetto App-V:

-   AppXManifest.xml: archiviato all'interno del pacchetto con copie di fallback archiviate nell'archivio pacchetti e nel profilo utente. Contiene le opzioni create durante il processo di sequenziazione.

-   DeploymentConfig.xml: fornisce informazioni di configurazione dei punti di estensione di integrazione basati su computer e utenti.

-   UserConfig.xml: un sottoinsieme del Deploymentconfig.xml che fornisce solo configurazioni basate sull'utente e punta solo ai punti di estensione basati sull'utente.

### <a name="rules-of-integration"></a>Regole di integrazione

Quando le applicazioni App-V vengono pubblicate in un computer con il client App-V, alcune azioni specifiche vengono eseguite come descritto nell'elenco seguente:

-   Pubblicazione globale: i collegamenti vengono archiviati nel percorso del profilo Tutti gli utenti e altri punti di estensione vengono archiviati nel Registro di sistema nell'hive HKLM.

-   Pubblicazione utente: i collegamenti vengono archiviati nel profilo dell'account utente corrente e altri punti di estensione vengono archiviati nel Registro di sistema nell'hive HKCU.

-   Backup e ripristino: durante la pubblicazione viene eseguito il backup dei dati delle applicazioni native esistenti e del Registro di sistema (ad esempio, le registrazioni FTA).

    1.  Ai pacchetti App-V viene data la proprietà in base all'ultimo pacchetto integrato in cui la proprietà viene passata all'applicazione App-V pubblicata più recente.

    2.  La proprietà trasferisce da un pacchetto App-V a un altro quando il pacchetto App-V proprietario non viene pubblicato. In questo modo non verrà avviato un ripristino dei dati o del Registro di sistema.

    3.  Ripristinare i dati di cui è stato eseguito il backup quando l'ultimo pacchetto viene annullato o rimosso in base al punto di estensione.

### <a name="extension-points"></a>Punti di estensione

I file di pubblicazione app-V (manifesto e configurazione dinamica) forniscono diversi punti di estensione che consentono all'applicazione di integrarsi con il sistema operativo locale. Questi punti di estensione eseguono attività tipiche di installazione delle applicazioni, ad esempio l'inserimento di collegamenti, la creazione di associazioni di tipi di file e la registrazione di componenti. Poiché si tratta di applicazioni virtualizzate che non vengono installate nello stesso modo di un'applicazione tradizionale, esistono alcune differenze. Di seguito è riportato un elenco dei punti di estensione trattati in questa sezione:

-   Collegamenti

-   Associazioni di tipi di file

-   Estensioni shell

-   COM

-   Client software

-   Funzionalità dell'applicazione

-   Gestore protocollo URL

-   AppPath

-   Applicazione virtuale

### <a name="shortcuts"></a>Collegamenti

Il taglio breve è uno degli elementi di base dell'integrazione con il sistema operativo ed è l'interfaccia per l'avvio diretto da parte dell'utente di un'applicazione App-V. Durante la pubblicazione e l'annullamento della pubblicazione delle applicazioni App-V.

Dal manifesto del pacchetto e dai file XML di configurazione dinamica, il percorso di un file eseguibile dell'applicazione specifico è disponibile in una sezione simile alla seguente:

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

Come accennato in precedenza, i collegamenti di App-V vengono inseriti per impostazione predefinita nel profilo dell'utente in base all'operazione di aggiornamento. L'aggiornamento globale inserisce i collegamenti nel profilo Tutti gli utenti e l'aggiornamento utente li archivia nel profilo dell'utente specifico. L'eseguibile effettivo viene archiviato nell'archivio pacchetti. Il percorso del file ICO è un percorso in token nel pacchetto App-V.

### <a name="file-type-associations"></a>Associazioni di tipi di file

Il client App-V gestisce le associazioni dei tipi di file del sistema operativo locale durante la pubblicazione, che consente agli utenti di utilizzare le chiamate al tipo di file o di aprire un file con un'estensione registrata in modo specifico (.docx) per avviare un'applicazione App-V. Le associazioni dei tipi di file sono presenti nel manifesto e nei file di configurazione dinamici, come illustrato nell'esempio seguente:

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

**Nota**  
In questo esempio:

-   `<Name>.xdp</Name>` è l'estensione

-   `<Name>AcroExch.XDPDoc</Name>` è il valore ProgId (che punta all'oggetto ProgId adiacente)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` è la riga di comando, che punta al file eseguibile dell'applicazione

 

### <a name="shell-extensions"></a>Estensioni della shell

Le estensioni della shell vengono incorporate automaticamente nel pacchetto durante il processo di sequenziazione. Quando il pacchetto viene pubblicato a livello globale, l'estensione della shell offre agli utenti la stessa funzionalità di se l'applicazione è stata installata localmente. L'applicazione non richiede alcuna configurazione o configurazione aggiuntiva nel client per abilitare la funzionalità di estensione della shell.

**Requisiti per l'utilizzo delle estensioni della shell:**

-   I pacchetti che contengono estensioni della shell incorporate devono essere pubblicati a livello globale.

-   Il "bitness" del client app, Sequencer e App-V deve corrispondere o le estensioni della shell non funzioneranno. Ad esempio:

    -   La versione dell'applicazione è a 64 bit.

    -   Sequencer è in esecuzione in un computer a 64 bit.

    -   Il pacchetto viene recapitato a un computer client App-V a 64 bit.

Nella tabella seguente vengono visualizzate le estensioni della shell supportate.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Handler</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestore menu di scelta rapida</p></td>
<td align="left"><p>Aggiunge voci di menu al menu di scelta rapida. Viene chiamato prima della visualizzazione del menu di scelta rapida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore del trascinamento della selezione</p></td>
<td align="left"><p>Controlla l'azione quando si fa clic con il pulsante destro del mouse sul trascinamento della selezione e modifica il menu di scelta rapida visualizzato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore destinazione di rilascio</p></td>
<td align="left"><p>Controlla l'azione dopo che un oggetto dati è stato trascinato e rilasciato su una destinazione di rilascio, ad esempio un file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore dell'oggetto dati</p></td>
<td align="left"><p>Controlla l'azione dopo la copia di un file negli Appunti o il trascinamento della selezione su una destinazione di rilascio. Può fornire ulteriori formati degli Appunti alla destinazione di rilascio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore della finestra delle proprietà</p></td>
<td align="left"><p>Sostituisce o aggiunge pagine alla finestra di dialogo della finestra delle proprietà di un oggetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore infotip</p></td>
<td align="left"><p>Consente il recupero di flag e informazioni di suggerimento per un elemento e la visualizzazione all'interno di una descrizione comando popup al passaggio del mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore colonne</p></td>
<td align="left"><p>Consente la creazione e la visualizzazione di colonne personalizzate Windows visualizzazione <em> Dettagli di Esplora </em> risorse. Può essere utilizzato per estendere l'ordinamento e il raggruppamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore di anteprima</p></td>
<td align="left"><p>Consente di visualizzare un'anteprima di un file nel riquadro di anteprima Windows Explorer.</p></td>
</tr>
</tbody>
</table>

 

### <a name="com"></a>COM

Il client App-V supporta la pubblicazione di applicazioni con supporto per l'integrazione COM e la virtualizzazione. L'integrazione COM consente al client App-V di registrare gli oggetti COM nel sistema operativo locale e nella virtualizzazione degli oggetti. Ai fini di questo documento, l'integrazione degli oggetti COM richiede ulteriori dettagli.

App-V supporta la registrazione di oggetti COM dal pacchetto al sistema operativo locale con due tipi di processo: Out-of-process e in-process. La registrazione di oggetti COM viene eseguita con una o una combinazione di più modalità operative per un pacchetto App-V specifico che include off, Isolated e Integrated. La modalità integrata è configurata per il tipo out-of-process o in-process. La configurazione delle modalità e dei tipi COM viene eseguita con i file di configurazione dinamici (deploymentconfig.xml o userconfig.xml).

I dettagli sull'integrazione di App-V sono disponibili all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### <a name="software-clients-and-application-capabilities"></a>Client software e funzionalità delle applicazioni

App-V supporta specifici client software e punti di estensione delle funzionalità dell'applicazione che consentono la registrazione delle applicazioni virtualizzate con il client software del sistema operativo. In questo modo gli utenti possono selezionare programmi predefiniti per operazioni quali posta elettronica, messaggistica istantanea e lettore multimediale. Questa operazione viene eseguita nel pannello di controllo con l'opzione Imposta accesso ai programmi e impostazioni predefinite computer e configurata durante la sequenziazione nel manifesto o nei file di configurazione dinamici. Le funzionalità delle applicazioni sono supportate solo quando le applicazioni App-V vengono pubblicate a livello globale.

Esempio di registrazione client software di un client di posta basato su App-V.

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

**Nota**  
In questo esempio:

-   `<ClientConfiguration EmailEnabled="true" />` è l'impostazione complessiva dei client software per integrare i client di posta elettronica

-   `<EMail MakeDefault="true">` è il flag per impostare un client di posta elettronica specifico come client di posta elettronica predefinito

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` è la registrazione della dll MAPI

 

### <a name="url-protocol-handler"></a>Gestore protocollo URL

Le applicazioni non sempre vengono chiamate in modo specifico applicazioni virtualizzate che utilizzano la chiamata al tipo di file. Ad esempio, in un'applicazione che supporta l'incorporamento di un collegamento mailto: all'interno di un documento o di una pagina Web, l'utente fa clic su un collegamento mailto: e si aspetta di ottenere il client di posta registrato. App-V supporta gestori di protocollo URL che possono essere registrati in base al pacchetto con il sistema operativo locale. Durante la sequenziazione, i gestori di protocollo URL vengono aggiunti automaticamente al pacchetto.

Per le situazioni in cui sono presenti più applicazioni in grado di registrare il gestore del protocollo URL specifico, è possibile utilizzare i file di configurazione dinamici per modificare il comportamento e disattivare o disabilitare questa funzionalità per un'applicazione che non dovrebbe essere l'applicazione principale avviata.

### <a name="apppath"></a>AppPath

Il punto di estensione AppPath supporta la chiamata di applicazioni App-V direttamente dal sistema operativo. Questa operazione viene in genere eseguita dalla schermata Run o Start, a seconda del sistema operativo, che consente agli amministratori di fornire l'accesso alle applicazioni App-V da comandi o script del sistema operativo senza chiamare il percorso specifico dell'eseguibile. Evita pertanto di modificare la variabile di ambiente del percorso di sistema in tutti i sistemi, come viene eseguita durante la pubblicazione.

Il punto di estensione AppPath è configurato nel manifesto o nei file di configurazione dinamici e viene archiviato nel Registro di sistema nel computer locale durante la pubblicazione per l'utente. Per ulteriori informazioni su AppPath, vedere: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### <a name="virtual-application"></a>Applicazione virtuale

Questo sottosistema fornisce un elenco delle applicazioni acquisite durante la sequenziazione, che in genere viene utilizzata da altri componenti di App-V. L'integrazione dei punti di estensione appartenenti a una determinata applicazione può essere disabilitata utilizzando file di configurazione dinamici. Ad esempio, se un pacchetto contiene due applicazioni, è possibile disabilitare tutti i punti di estensione appartenenti a un'applicazione, per consentire solo l'integrazione dei punti di estensione di un'altra applicazione.

### <a name="extension-point-rules"></a>Regole del punto di estensione

I punti di estensione descritti in precedenza sono integrati nel sistema operativo in base alla modalità di pubblicazione dei pacchetti. La pubblicazione globale inserisce i punti di estensione nei percorsi dei computer pubblici, in cui la pubblicazione degli utenti colloca i punti di estensione nelle posizioni degli utenti. Ad esempio, un collegamento creato sul desktop e pubblicato globalmente comporta i dati del file per il collegamento (%Public%\\Desktop) e i dati del Registro di sistema (HKLM\\Software\\Classes). Lo stesso collegamento contiene i dati del file (%UserProfile%\\Desktop) e i dati del Registro di sistema (HKCU\\Software\\Classes).

I punti di estensione non vengono pubblicati nello stesso modo, in cui alcuni punti di estensione richiedono la pubblicazione globale e altri richiedono la sequenziazione nel sistema operativo e nell'architettura specifici in cui vengono recapitati. Di seguito è riportata una tabella che descrive queste due regole chiave.

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
<td align="left"><p>Associazione dei tipi di file</p></td>
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
<td align="left"><p>Software Client</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Funzionalità dell'applicazione</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore menu di scelta rapida</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore trascinamento della selezione</p></td>
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
<td align="left"><p>Gestore colonne</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Estensioni shell</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Oggetto Browser Helper</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Oggetto Active X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a name="dynamic-configuration-processing"></a><a href="" id="bkmk-dynamic-config"></a>Elaborazione della configurazione dinamica


La distribuzione di pacchetti App-V in un computer o in un utente è molto semplice. Tuttavia, poiché le organizzazioni distribuiscono applicazioni AppV tra linee di business e confini geografici e politici, la possibilità di sequenziare un'applicazione una sola volta con un set di impostazioni diventa impossibile. App-V è stato progettato per questo scenario, poiché acquisisce impostazioni e configurazioni specifiche durante la sequenziazione nel file Manifesto, ma supporta anche la modifica con i file di configurazione dinamica.

La configurazione dinamica di App-V consente di specificare un criterio per un pacchetto a livello di computer o di utente. I file di configurazione dinamica consentono ai tecnici di sequenziazione di modificare la configurazione di un pacchetto, dopo la sequenziazione, per soddisfare le esigenze di singoli gruppi di utenti o computer. In alcuni casi potrebbe essere necessario apportare modifiche all'applicazione per fornire funzionalità appropriate all'interno dell'ambiente App-V. Ad esempio, potrebbe essere necessario apportare modifiche ai file \_\*config.xml per consentire l'esecuzione di determinate azioni in un determinato momento durante l'esecuzione dell'applicazione, ad esempio disabilitando un'estensione mailto per impedire a un'applicazione virtualizzata di sovrascrivere tale estensione da un'altra applicazione.

I pacchetti App-V contengono il file Manifesto all'interno del file del pacchetto appv, che è rappresentativo delle operazioni di sequenziazione ed è il criterio di scelta, a meno che i file di configurazione dinamica non siano assegnati a un pacchetto specifico. Dopo la sequenziazione, i file di configurazione dinamica possono essere modificati per consentire la pubblicazione di un'applicazione in desktop o utenti diversi con punti di estensione diversi. I due file di configurazione dinamica sono i file DDC (Dynamic Deployment Configuration) e DUC (Dynamic User Configuration). Questa sezione è incentrata sulla combinazione del manifesto e dei file di configurazione dinamici.

### <a name="example-for-dynamic-configuration-files"></a>Esempio di file di configurazione dinamica

L'esempio seguente mostra la combinazione dei file Manifesto, Configurazione distribuzione e Configurazione utente dopo la pubblicazione e durante il normale funzionamento. Questi esempi sono esempi abbreviati di ognuno dei file. Lo scopo è mostrare solo la combinazione dei file e non essere una descrizione completa delle categorie specifiche disponibili in ognuno dei file. Per altre informazioni, consulta la Guida alla sequenziazione di App-V 5 all'indirizzo: <https://go.microsoft.com/fwlink/?LinkID=269810>

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

**Configurazione distribuzione**

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

## <a name="side-by-side-assemblies"></a><a href="" id="bkmk-sidebyside-assemblies"></a>Assembly affiancati


App-V supporta la creazione automatica di pacchetti di assembly side-by-side (SxS) durante la sequenziazione e la distribuzione nel client durante la pubblicazione di applicazioni virtuali. App-V 5 SP2 supporta l'acquisizione di assembly SxS durante la sequenziazione di assembly non presenti nel computer di sequenziazione. Per gli assembly costituiti da Visual C++ (versione 8 e successive) e/o dalla fase di esecuzione di MSXML, Sequencer rileva e acquisisce automaticamente queste dipendenze anche se non sono state installate durante il monitoraggio. La funzionalità Assembly affiancati rimuove le limitazioni delle versioni precedenti di App-V, in cui App-V Sequencer non acquisisce gli assembly già presenti nella workstation di sequenziazione e privatizza gli assembly che si limitano a una versione di bit per pacchetto. Questo comportamento ha provocato la distribuzione di applicazioni App-V ai client senza gli assembly SxS necessari, causando errori di avvio dell'applicazione. Questo ha forzato il processo di creazione di pacchetti a documentare e quindi verificare che tutti gli assembly necessari per i pacchetti siano stati installati localmente nel sistema operativo client dell'utente per garantire il supporto per le applicazioni virtuali. In base al numero di assembly e alla mancanza di documentazione dell'applicazione per le dipendenze necessarie, questa attività è stata una sfida sia per la gestione che per l'implementazione.

Il supporto degli assembly affiancati in App-V include le funzionalità seguenti.

-   Acquisizioni automatiche dell'assembly SxS durante la sequenziazione, indipendentemente dal fatto che l'assembly sia già installato nella workstation di sequenziazione.

-   Il client App-V installa automaticamente gli assembly SxS necessari nel computer client al momento della pubblicazione quando non sono presenti.

-   Sequencer segnala la dipendenza di run-time di VC nel meccanismo di creazione di report di Sequencer.

-   Sequencer consente di scegliere di non creare un pacchetto degli assembly già installati nel Sequencer, supportando gli scenari in cui gli assembly sono stati installati in precedenza nei computer di destinazione.

### <a name="automatic-publishing-of-sxs-assemblies"></a>Pubblicazione automatica di assembly SxS

Durante la pubblicazione di un pacchetto App-V con assembly SxS, il client App-V verifica la presenza dell'assembly nel computer. Se l'assembly non esiste, il client distribuirà l'assembly nel computer. I pacchetti che fanno parte dei gruppi di connessione si basano sulle installazioni di assembly side-by-side che fanno parte dei pacchetti di base, poiché il gruppo di connessione non contiene informazioni sull'installazione di assembly.

**Nota**  
L'annullamento della pubblicazione o la rimozione di un pacchetto con un assembly non rimuove gli assembly per tale pacchetto.

 

## <a name="client-logging"></a><a href="" id="bkmk-client-logging"></a>Registrazione client


Il client App-V registra le informazioni nel Windows eventi in formato ETW standard. Gli eventi app-V specifici sono disponibili nel Visualizzatore eventi, in Registri applicazioni e servizi\\Microsoft\\AppV\\Client.

**Nota**  
In App-V 5.0 SP3 alcuni log sono stati consolidati e spostati nel percorso seguente:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Per un elenco dei log spostati, vedere [Informazioni su App-V 5.0 SP3.](about-app-v-50-sp3.md#bkmk-event-logs-moved)

 

Di seguito sono descritte tre categorie specifiche di eventi.

**Amministratore:** registra gli eventi per le configurazioni applicate al client App-V e contiene gli avvisi e gli errori principali.

**Operativo**: registra l'esecuzione generale di App-V e l'utilizzo di singoli componenti creando un log di controllo delle operazioni di App-V completate nel client App-V.

**Applicazione virtuale:** registra l'avvio e l'uso di sottosistemi di virtualizzazione.






 

 





