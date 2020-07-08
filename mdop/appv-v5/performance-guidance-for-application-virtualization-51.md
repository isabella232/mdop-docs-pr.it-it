---
title: Linee guida sulle prestazioni di Application Virtualization 5.1
description: Linee guida sulle prestazioni di Application Virtualization 5.1
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805038"
---
# Linee guida sulle prestazioni di Application Virtualization 5.1


Scopri come configurare App-V 5,1 per ottenere prestazioni ottimali, ottimizzare i pacchetti di app virtuali e migliorare l'esperienza utente con RDS e VDI.

L'implementazione di più metodi può aiutare a migliorare l'esperienza dell'utente finale. Tuttavia, l'ambiente potrebbe non supportare tutti i metodi.

Prima di leggere il documento, leggere e comprendere le informazioni seguenti.

-   [Guida dell'amministratore di Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Pubblicazione di applicazioni App-V 5 SP2 e interazione client](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Guida alla sequenziazione di Microsoft Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=269953)

**Nota**  
Alcuni termini usati in questo documento possono avere significati diversi a seconda dell'origine esterna e del contesto. Per altre informazioni sui termini usati in questo documento seguiti da un asterisco **\\** *, vedere la sezione [terminologia dell'applicazione per la virtualizzazione delle prestazioni](#bkmk-terms1) di questo documento.



Infine, questo documento ti fornirà le informazioni per configurare il computer che gestisce il client App-V 5,1 e l'ambiente per ottenere prestazioni ottimali. Ottimizza i pacchetti di applicazioni virtuali per le prestazioni usando il sequencer e per capire come usare la virtualizzazione dell'esperienza utente (UE-V) o altre tecnologie di gestione dell'ambiente utente per ottenere un'esperienza utente ottimale con App-V 5,1 sia in Servizi Desktop remoto che in infrastrutture desktop virtuali non permanenti (VDI).

Per determinare quali informazioni sono rilevanti per l'ambiente, è necessario rivedere la breve panoramica di ogni sezione e l'elenco di controllo dell'applicabilità.

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> App-V 5,1 in stato \ * distribuzioni non persistenti


In questa sezione vengono fornite informazioni su un approccio che consente di garantire che un utente possa accedere a tutte le applicazioni virtuali in pochi secondi dopo l'accesso. Questa operazione viene eseguita per affrontare in modo univoco l'aggiornamento della pubblicazione di App V 5,1 spesso a lunga durata. Man mano che si scoprirà la base dell'approccio, l'aggiornamento della pubblicazione più veloce è uno che non deve effettivamente eseguire alcuna operazione. È necessario rispettare una serie di condizioni e seguire i passaggi per ottenere un'esperienza utente ottimale.

Per altre informazioni, usare le informazioni nella sezione seguente:

[Scenari di utilizzo](#bkmk-us) : durante la revisione dei due scenari, tieni presente che questi sono gli estremi di approccio. In base ai requisiti di utilizzo, è possibile scegliere di applicare questi passaggi a un sottoinsieme di utenti e/o pacchetti di applicazioni virtuali.

-   Ottimizzato per le prestazioni: per offrire un'esperienza ottimale, è possibile prevedere che l'immagine di base includa parte del pacchetto di applicazione virtuale App-V. Questo e altri requisiti vengono discussi.

-   Ottimizzato per lo spazio di archiviazione: se si è interessati all'impatto dello spazio di archiviazione, seguire questo scenario consentirà di risolvere i problemi.

[Preparazione dell'ambiente](#bkmk-pe)

-   Procedura per preparare l'immagine di base: in un ambiente VDI o RDSH non persistente, è necessario completare solo pochi passaggi nell'immagine di base per abilitare questo approccio.

-   USA UE-V 2,1 come soluzione di gestione dei profili utente (UPM) per l'approccio App-V-la pietra angolare di questo approccio è la capacità di una soluzione UEM di rendere persistente il contenuto di pochi percorsi di registro e file. Queste posizioni costituiscono le integrazioni degli utenti \ *. Assicurarsi di esaminare i requisiti specifici per la soluzione UPM.

[Esperienza utente walk-through](#bkmk-uewt)

-   Walk-through: si tratta di una procedura dettagliata per le operazioni di App-V e UE-V e per le aspettative che gli utenti devono avere.

-   Risultato: descrive i risultati previsti.

[Impatto sul ciclo di vita del pacchetto](#bkmk-plc)

[Migliorare l'esperienza VDI attraverso ottimizzazione delle prestazioni/ottimizzazione](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>Elenco di controllo applicabilità

Ambiente di distribuzione

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>VDI o RDSH non persistente.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Virtualizzazione dell'esperienza utente (UE-V), altre soluzioni UPM o disk del profilo utente (UPD).</p></td>
</tr>
</tbody>
</table>



Configurazione prevista

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>User Experience Virtualization (UE-V) con il modello di stato utente App-V abilitato o con il software UPM (User Profile Management). Il software UPM non UE-V deve essere in grado di attivare l'accesso o l'inizio e la disconnessione dell'applicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>App-V Shared Content Store (SCS) è configurato o può essere configurato.</p></td>
</tr>
</tbody>
</table>



Amministrazione IT

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L'amministratore potrebbe dover aggiornare regolarmente l'immagine di base di VM per garantire prestazioni ottimali o l'amministratore potrebbe dover gestire più immagini per gruppi di utenti diversi.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>Scenario di utilizzo

Mentre esaminiamo i due scenari, tieni presente che questi approcci si avvicinano agli estremi. In base ai requisiti di utilizzo, è possibile scegliere di applicare questi passaggi a un sottoinsieme di utenti, pacchetti di applicazioni virtuali o entrambi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ottimizzato per le prestazioni</th>
<th align="left">Ottimizzato per lo spazio di archiviazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Per offrire un'esperienza utente ottimale, questo approccio sfrutta le funzionalità di una soluzione UPM e richiede ulteriore preparazione delle immagini e può incorrere in un sovraccarico di gestione delle immagini aggiuntivo.</p>
<p>Di seguito vengono illustrati molti miglioramenti delle prestazioni nelle distribuzioni non permanenti con stato. Per altre informazioni, vedere la <strong> procedura di sequenziazione per ottimizzare i pacchetti per la pubblicazione delle prestazioni </strong> e il riferimento alla <strong> Guida alla sequenziazione di App-V </strong> nella <strong> sezione vedere anche di questo documento </strong> .</p></td>
<td align="left"><p>Le aspettative generali dello scenario precedente si applicano ancora qui. Tuttavia, tieni presente che le immagini VM sono in genere archiviate in matrici molto costose; è stata apportata una lieve modifica all'approccio. Non preconfigurare pacchetti di applicazioni virtuali mirati dall'utente nell'immagine di base.</p>
<p>L'impatto di questa alterazione è dettagliato nella sezione relativa all'esperienza utente di questo documento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>Preparazione dell'ambiente

Nella tabella seguente vengono illustrati i passaggi necessari per preparare l'immagine di base e l'UE-V o un'altra soluzione UPM per l'approccio.

**Preparare l'immagine di base**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ottimizzato per le prestazioni</th>
<th align="left">Ottimizzato per lo spazio di archiviazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Installare la versione client App-V 5,1 del client.</p></li>
<li><p>Installare UE-V e scaricare il modello di impostazioni app-V dalla raccolta modelli UE-V, vedere i passaggi seguenti.</p></li>
<li><p>Configurare la modalità SCS (Shared Content Store). Per altre informazioni <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> , vedere come installare il client App-V 5,1 per la modalità di archiviazione del contenuto condiviso </a> .</p></li>
<li><p>Configurare Mantieni le integrazioni degli utenti nel DWORD del registro di accesso.</p></li>
<li><p>Preconfigurare tutti i pacchetti con destinazione globale e utente, ad esempio <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Preconfigurare tutti i gruppi di connessioni mirati dall'utente e globale, ad esempio <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Pre-pubblicare tutti i pacchetti di destinazione globale.</p>
<p></p>
<p>Alternativamente</p>
<ul>
<li><p>Eseguire una pubblicazione/aggiornamento globale.</p></li>
<li><p>Eseguire una pubblicazione/aggiornamento degli utenti.</p></li>
<li><p>Annullare la pubblicazione di tutti i pacchetti mirati dall'utente.</p></li>
<li><p>Eliminare le voci VFS (User-Virtual File System) seguenti.</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Installare la versione client App-V 5,1 del client.</p></li>
<li><p>Installare UE-V e scaricare il modello di impostazioni app-V dalla raccolta modelli UE-V, vedere i passaggi seguenti.</p></li>
<li><p>Configurare la modalità SCS (Shared Content Store). Per altre informazioni <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> , vedere come installare il client App-V 5,1 per la modalità di archiviazione del contenuto condiviso </a> .</p></li>
<li><p>Configurare Mantieni le integrazioni degli utenti nel DWORD del registro di accesso.</p></li>
<li><p>Preconfigura tutti i pacchetti di destinazione globale, ad esempio <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Preconfigurare tutti i gruppi di connessioni con destinazione globale, ad esempio <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Pre-pubblicare tutti i pacchetti di destinazione globale.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**Configurazioni** -per le configurazioni client App-V critiche e per un po' più di contesto e procedure, esaminare le informazioni seguenti:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Impostazione di configurazione</th>
<th align="left">Che cosa fa questo?</th>
<th align="left">Come si usa?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Modalità SCS (Shared Content Store)</p>
<ul>
<li><p>Configurabile in PowerShell tramite <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> oppure</p></li>
<li><p>Durante l'installazione del client App-V.</p></li>
</ul></td>
<td align="left"><p>Quando si esegua l'archiviazione del contenuto condiviso, solo i dati vengono mantenuti nel disco rigido; altri asset delle applicazioni virtuali vengono mantenuti in memoria (RAM).</p>
<p>In questo modo è possibile risparmiare spazio di archiviazione locale e ridurre a icona I/O del disco al secondo (IOPS).</p></td>
<td align="left"><p>Questa operazione è consigliata quando sono disponibili connessioni a bassa latenza tra l'endpoint client App-V e il server del contenuto SCS, SAN.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p>Configurare il registro di sistema in <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> software </strong>  \  <strong> Microsoft </strong>  \  <strong> appv </strong>  \  <strong> client </strong>  \  <strong> Integration </strong> .</p></li>
<li><p>Creare il valore DWORD <strong> PreserveUserIntegrationsOnLogin </strong> con un valore pari a <strong> 1 </strong> .</p></li>
<li><p>Riavviare il servizio client App-V o riavviare il computer in cui è in uso il client App-V.</p></li>
</ul></td>
<td align="left"><p>Se non è già stato configurato ( <strong> Add-AppvClientPackage </strong> ) un pacchetto specifico e questa impostazione non è configurata, il client App-V disintegrerà * le integrazioni permanenti degli utenti e quindi reintegrerà *.</p>
<p>Per ogni pacchetto che soddisfa le condizioni precedenti, il lavoro verrà eseguito due volte durante la pubblicazione/aggiornamento.</p></td>
<td align="left"><p>Se non si prevede di pre-configurare ogni pacchetto utente disponibile nell'immagine di base, usare questa impostazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p>Configurare il registro di sistema in <strong> HKEY_LOCAL_MACHINE </strong> &lt; &gt; software </strong>  \  <strong> Microsoft </strong>  \  <strong> appv Strong </strong> &lt; &gt; client </strong>  \  <strong> Publishing </strong> .</p></li>
<li><p>Crea il valore DWORD <strong> MaxConcurrentPublishingrefresh </strong> con il numero massimo desiderato di aggiornamenti per la pubblicazione simultanea.</p></li>
<li><p>Il servizio client App-V e il computer non devono essere riavviati.</p></li>
</ul></td>
<td align="left"><p>Questa impostazione determina il numero di utenti che possono eseguire una sincronizzazione/aggiornamento della pubblicazione simultaneamente. L'impostazione predefinita non è limite.</p></td>
<td align="left"><p>Se si limita il numero di aggiornamenti simultanei della pubblicazione, viene impedito un uso eccessivo della CPU che potrebbe influire sulle prestazioni del computer. Questo limite è consigliato in un ambiente RDS, in cui più utenti possono accedere allo stesso computer contemporaneamente ed eseguire una sincronizzazione di aggiornamento della pubblicazione.</p>
<p>Se viene raggiunta la soglia di aggiornamento della pubblicazione simultanea, il tempo necessario per pubblicare le nuove applicazioni e renderle disponibili per gli utenti finali dopo l'accesso potrebbe richiedere un periodo di tempo indeterminato.</p></td>
</tr>
</tbody>
</table>



### Configurare la soluzione UE-V per l'approccio App-V

Ti consigliamo di usare Microsoft User Experience Virtualization (UE-V) per acquisire e centralizzare le impostazioni delle applicazioni e le impostazioni del sistema operativo Windows per un utente specifico. Queste impostazioni vengono quindi applicate ai diversi computer a cui si accede dall'utente, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure). UE-V è ottimizzato per gli scenari RDS e VDI.

Per altre informazioni, vedere [Introduzione alla virtualizzazione dell'esperienza utente 2,0](https://technet.microsoft.com/library/dn458926.aspx)

In sostanza, tutto ciò che è necessario è installare il client UE-V e scaricare il modello di impostazioni di App-V di Microsoft authored seguente dalla [raccolta di modelli Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33). Registrare il modello. Per altre informazioni sui modelli UE-V, vedere [la risorsa specifica UE-v per l'acquisizione e la registrazione del modello](https://technet.microsoft.com/library/dn458926.aspx).

**Nota**  
Senza eseguire un ulteriore passaggio di configurazione, Microsoft User Environment Virtualization (UE-V) non sarà in grado di sincronizzare i tasti di scelta rapida del menu Start (file lnk) nel computer di destinazione. Il tipo di file lnk è escluso per impostazione predefinita.

UE-V supporta solo la rimozione del tipo di file lnk dall'elenco di esclusione negli scenari RDS e VDI, in cui ogni dispositivo dell'utente avrà lo stesso set di applicazioni installato nella stessa posizione e ogni file lnk è valido per tutti i dispositivi degli utenti. Ad esempio, UE-V non supporta attualmente i due scenari seguenti, perché il risultato netto sarà che il collegamento sarà valido in uno ma non in tutti i dispositivi.

-   Se un utente ha un'applicazione installata in un dispositivo con i file lnk abilitati e la stessa applicazione nativa installata in un altro dispositivo a una radice di installazione diversa con i file lnk abilitati.

-   Se un utente ha un'applicazione installata in un dispositivo ma non in un altro con i file lnk abilitati.



**Importante**  
Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema. Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows. Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat). Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti. Cambiare il registro di sistema a proprio rischio.



Con l'editor del registro di sistema Microsoft (regedit.exe), passare a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** e Remove **. lnk** dai tipi di file esclusi.

**Configurare un'altra soluzione UPM (User Profile Management) per l'approccio App-V**

L'aspettativa in un ambiente con stato è che una soluzione UPM è implementata e può supportare la persistenza dei dati degli utenti tra le sessioni e tra gli account di accesso.

I requisiti per la soluzione UPM sono i seguenti.

Per abilitare un'esperienza di accesso ottimizzata, ad esempio l'approccio App-V 5,1 per l'utente, la soluzione deve essere in grado di:

-   Rendere persistenti le integrazioni seguenti degli utenti nell'ambito del profilo utente/persona.

-   Attivazione di una sincronizzazione del profilo utente per l'accesso (o l'avvio dell'applicazione), che può garantire che tutte le integrazioni degli utenti vengano applicate prima dell'inizio della pubblicazione/aggiornamento o,

-   Allegare e scollegare un disco di profilo utente (UPD) o una tecnologia simile che contiene le integrazioni degli utenti.

    **Nota**  
    App-V è supportata quando si usa UPD solo quando l'intero profilo è archiviato nel disco del profilo utente.

    I pacchetti App-V non sono supportati quando si usa UPD con le cartelle selezionate archiviate nel disco del profilo utente. Il driver copia in scrittura non gestisce le cartelle selezionate di UPD.



-   Acquisizione delle modifiche apportate alle posizioni, che costituiscono le integrazioni degli utenti, prima della disconnessione della sessione.

Con App-V 5,1 quando si aggiunge un server di pubblicazione (**Add-AppvPublishingServer**) è possibile configurare la sincronizzazione, ad esempio aggiorna durante l'accesso e/o dopo un intervallo di aggiornamento specificato. In entrambi i casi viene creata un'attività pianificata.

Nelle versioni precedenti di App-V 5,1 sono state configurate entrambe le attività pianificate usando un VBScript che avviava l'utente e l'aggiornamento globale. Con il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 l'aggiornamento dell'utente in accesso è stato avviato da **SyncAppvPublishingServer.exe**. Questa modifica è stata introdotta per dare alle soluzioni UPM un processo di trigger. Questo processo ritarda la pubblicazione di/Refresh per consentire alla soluzione UPM di applicare le integrazioni degli utenti. Verrà chiusa una volta completata la pubblicazione/aggiornamento.

**Integrazioni degli utenti**

Registro di sistema-HKEY \ _CURRENT \ _USER

-   Path-Software\\Classes

    Exclude: impostazioni locali, ActivatableClasses, AppX \ *

-   Path-Software\\Microsoft\\AppV

-   Path-percorsi Software\\Microsoft\\Windows\\CurrentVersion\\App

**Percorsi di file**

-   Radice-"variabile di ambiente" APPDATA

    Path-Microsoft\\AppV\\Client\\Catalog

-   Radice-"variabile di ambiente" APPDATA

    Path-Microsoft\\AppV\\Client\\Integration

-   Radice-"variabile di ambiente" APPDATA

    Path-Microsoft\\Windows\\Start Menu\\Programs

-   (Per rendere persistenti tutti i collegamenti desktop, virtuali e non virtuali)

    Radice-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ *. lnk

**Virtualizzazione di Microsoft User Experience (UE-V)**

Inoltre, ti consigliamo di usare Microsoft User Experience Virtualization (UE-V) per acquisire e centralizzare le impostazioni delle applicazioni e le impostazioni del sistema operativo Windows per un utente specifico. Queste impostazioni vengono quindi applicate ai diversi computer a cui si accede dall'utente, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure).

Per altre informazioni, vedere [Introduzione a User Experience Virtualization 1,0](https://technet.microsoft.com/library/jj680015.aspx) e [modelli di posizione di condivisione delle impostazioni con la raccolta di modelli UE-V](https://technet.microsoft.com/library/jj679972.aspx).

### <a href="" id="bkmk-uewt"></a>Esperienza utente walk-through

Di seguito è riportata una procedura dettagliata delle operazioni di App-V e UPM e le aspettative che gli utenti dovrebbero aspettarsi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ottimizzato per le prestazioni</th>
<th align="left">Ottimizzato per lo spazio di archiviazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dopo aver implementato questo approccio nell'ambiente VDI/RDSH, al primo accesso</p>
<ul>
<li><p>Operazione Viene avviata la pubblicazione/aggiornamento degli utenti. Presupposto Se è la prima volta che un utente ha pubblicato applicazioni virtuali (ad esempio non persistenti), la durata consueta di una pubblicazione/aggiornamento sarà la solita.</p></li>
<li><p>Operazione Dopo la pubblicazione/aggiornamento, la soluzione UPM acquisisce le integrazioni degli utenti. Presupposto A seconda di come è configurata la soluzione UPM, questa operazione può essere eseguita durante il processo di disconnessione. Questo comporterà lo stesso overhead/simile a quello di persistenza dello stato utente.</p></li>
</ul>
<p>Sugli accessi successivi:</p>
<ul>
<li><p>Operazione La soluzione UPM applica le integrazioni degli utenti al sistema prima della pubblicazione/aggiornamento.</p>
<p>Presupposto Sul desktop saranno presenti tasti di scelta rapida, oppure nel menu Start, che funzionano immediatamente. Quando il completamento della pubblicazione/aggiornamento (ad esempio, i diritti del pacchetto cambiano), alcuni potrebbero andarsene.</p></li>
<li><p>Operazione La pubblicazione/aggiornamento elaborerà le operazioni di annullamento della pubblicazione e pubblicazione per le modifiche apportate ai pacchetti utente. Presupposto Se non sono presenti modifiche al diritto, publishing1 verrà completato in pochi secondi. In caso contrario, la pubblicazione/aggiornamento aumenterà in relazione al numero e alla complessità * delle applicazioni virtuali</p></li>
<li><p>Operazione La soluzione UPM acquisirà di nuovo le integrazioni degli utenti alla disconnessione. Presupposto Uguale a precedente.</p></li>
</ul>
<p>¹ l'operazione di pubblicazione ( <strong> Publish-AppVClientPackage </strong> ) aggiunge voci al catalogo dell'utente, associa il diritto all'utente, identifica l'archivio locale e termina completando i passaggi di integrazione.</p></td>
<td align="left"><p>Dopo aver implementato questo approccio nell'ambiente VDI/RDSH, al primo accesso</p>
<ul>
<li><p>Operazione Viene avviata la pubblicazione/aggiornamento degli utenti. Presupposto</p>
<ul>
<li><p>Se è la prima volta che un utente ha pubblicato applicazioni virtuali (ad esempio, non persistenti), la durata normale di una pubblicazione/aggiornamento sarà la consueta.</p></li>
<li><p>I primi e gli accessi successivi saranno interessati dalla preconfigurazione dei pacchetti (Aggiungi/Aggiorna).</p>
<p></p></li>
</ul></li>
<li><p>Operazione Dopo la pubblicazione/aggiornamento, la soluzione UPM acquisisce le integrazioni degli utenti. Presupposto A seconda di come è configurata la soluzione UPM, questa operazione può essere eseguita durante il processo di disconnessione. Questo comporterà lo stesso overhead/simile a quello di persistenza dello stato utente</p></li>
</ul>
<p>Sugli accessi successivi:</p>
<ul>
<li><p>Operazione La soluzione UPM applica le integrazioni degli utenti al sistema prima della pubblicazione/aggiornamento.</p></li>
<li><p>Operazione L'aggiunta/aggiornamento deve preconfigurare tutte le applicazioni di destinazione dell'utente. Presupposto</p>
<ul>
<li><p>In questo modo è possibile aumentare significativamente la disponibilità dell'applicazione (nell'ordine di 10 secondi).</p></li>
<li><p>In questo modo si aumenta il tempo di aggiornamento della pubblicazione relativo al numero e alla complessità * delle applicazioni virtuali.</p>
<p></p></li>
</ul></li>
<li><p>Operazione La pubblicazione/aggiornamento elaborerà le operazioni di annullamento della pubblicazione e pubblicazione per le modifiche apportate ai diritti del pacchetto utente.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Risultato</th>
<th align="left">Risultato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Dato che le integrazioni degli utenti sono completamente conservate, ad esempio, l'integrazione per la pubblicazione/aggiornamento verrà completata. Tutte le applicazioni virtuali saranno disponibili entro pochi secondi dall'accesso.</p></li>
<li><p>La pubblicazione/aggiornamento elaborerà le modifiche apportate agli utenti aventi diritto alle applicazioni virtuali che hanno un impatto sull'esperienza.</p></li>
</ul></td>
<td align="left"><p>Poiché il componente aggiuntivo/aggiornamento deve riconfigurare tutte le applicazioni virtuali nella VM, il tempo di aggiornamento della pubblicazione su ogni account di accesso verrà esteso.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>Impatto sul ciclo di vita del pacchetto

L'aggiornamento di un pacchetto è un aspetto cruciale del ciclo di vita del pacchetto. Per garantire agli utenti l'accesso ai pacchetti di applicazioni virtuali (pubblicati) o declassati (non pubblicati) appropriati, è consigliabile aggiornare l'immagine di base in modo che corrispondano alle modifiche apportate. Per capire perché rivedere la sezione seguente:

App-V 5,0 SP2 ha introdotto il concetto di stati in sospeso. In passato,

-   Se un amministratore ha modificato i diritti o ha creato una nuova versione di un pacchetto (aggiornato) e durante una pubblicazione/aggiornamento il pacchetto è stato usato, l'operazione di annullamento della pubblicazione o di pubblicazione, rispettivamente, non riesce.

-   A questo punto, se un pacchetto è in uso, l'operazione verrà sospesa. Le operazioni di annullamento della pubblicazione e pubblicazione in sospeso verranno elaborate nel riavvio del servizio o se viene emesso un altro comando pubblica o non pubblica. In quest'ultimo caso, se l'applicazione virtuale è in uso in caso contrario, l'applicazione virtuale resterà in uno stato in sospeso. Per i pacchetti pubblicati a livello globale, è spesso necessario riavviare o riavviare il servizio.

In un ambiente non persistente è improbabile che le operazioni in sospeso vengano elaborate. Le operazioni in sospeso, ad esempio le attività vengono acquisite in **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **appv**  \\  **client**  \\  **PendingTasks**. Anche se questa posizione viene mantenuta dalla soluzione UPM, se non viene applicata all'ambiente prima di eseguire l'accesso, non verrà elaborata.

### <a href="" id="bkmk-evdi"></a>Migliorare l'esperienza VDI attraverso l'ottimizzazione delle prestazioni

La sezione seguente contiene elenchi con informazioni su documentazione e download Microsoft che potrebbero risultare utili per ottimizzare l'ambiente per le prestazioni.

**Blog e script di NGEN .NET (altamente consigliato)**

Informazioni sulla tecnologia NGEN

-   [Come velocizzare l'ottimizzazione NGEN](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [Script](https://aka.ms/DrainNGenQueue)

**Ruoli di Windows Server e server**

Linee guida per l'ottimizzazione delle prestazioni del server

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**Ruoli del server**

-   [Host di virtualizzazione Desktop remoto](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [Host sessione Desktop remoto](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [Pertinenza di IIS: gestione di App-V, pubblicazione, servizi Web per la creazione di report](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [Pertinenza del file server (SMB): se usato per l'archiviazione e il recapito del contenuto di App-V in modalità SCS](https://technet.microsoft.com/library/jj134210.aspx)

**Istruzioni per l'ottimizzazione delle prestazioni del client Windows (sistema operativo guest)**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [Script di ottimizzazione: (fornito dal supporto Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [Script di ottimizzazione: (fornito dal supporto Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## Sequenziazione dei passaggi per ottimizzare i pacchetti per le prestazioni di pubblicazione


Diverse funzionalità App-V facilitano nuovi scenari o abilitano nuovi scenari di distribuzione dei clienti. Queste caratteristiche seguenti possono influire sulle prestazioni delle operazioni di pubblicazione e avvio.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Considerazione</th>
<th align="left">Vantaggi</th>
<th align="left">Sui compromessi nella</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nessun blocco di funzionalità 1 (FB1, noto anche come FB principale)</p></td>
<td align="left"><p>Nessun FB1 indica che l'applicazione verrà avviata immediatamente e il flusso di errore (applicazione richiede file, DLL e deve essere abbattuti in rete) durante il lancio. Se sono presenti limitazioni di rete, FB1 sarà:</p>
<ul>
<li><p>Ridurre il numero di errori di flusso e larghezza di banda della rete usati quando si avvia un'applicazione per la prima volta.</p></li>
<li><p>Posticipa il lancio fino a quando l'intero FB1 non è stato trasmesso.</p></li>
</ul></td>
<td align="left"><p>Il flusso di errore riduce il tempo di avvio.</p></td>
<td align="left"><p>I pacchetti di applicazioni virtuali con FB1 configurati dovranno essere risequenziati.</p></td>
</tr>
</tbody>
</table>



### Rimozione di FB1

La rimozione di FB1 non richiede il programma di installazione dell'applicazione originale. Dopo aver completato i passaggi seguenti, è consigliabile ripristinare il computer in cui è in esecuzione il sequencer in uno snapshot pulito.

**Interfaccia utente di Sequencer** : crea un nuovo pacchetto di applicazione virtuale.

1.  Completare i passaggi di sequenziazione fino a Personalizza- &gt; streaming.

2.  Durante il passaggio di flusso, non selezionare **ottimizza il pacchetto per la distribuzione su rete lenta o non affidabile**.

3.  Se lo si desidera, passa al **sistema operativo di destinazione**.

**Modificare un pacchetto di applicazione virtuale esistente**

1.  Completare i passaggi di sequenziazione fino allo streaming.

2.  Non selezionare **ottimizza il pacchetto per la distribuzione in una rete lenta o inaffidabile**.

3.  Passa a **Crea pacchetto**.

**PowerShell** -aggiornare un pacchetto di applicazione virtuale esistente.

1.  Aprire una sessione di PowerShell con privilegi elevati.

2.  Import-Module **appvsequencer**.

3.  **Update-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.appv"-programma di installazione

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **Nota**  
    Questo cmdlet richiede un file eseguibile (con estensione exe) o batch (. bat). Devi specificare un file eseguibile o batch vuoto (Nothing).



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Considerazioni</th>
<th align="left">Vantaggi</th>
<th align="left">Sui compromessi nella</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nessuna installazione di SXS in pubblicazione (pre-installare gli assembly SxS)</p></td>
<td align="left"><p>I pacchetti di applicazioni virtuali non devono essere risequenziati. Gli assembly SxS possono rimanere nel pacchetto dell'applicazione virtuale.</p></td>
<td align="left"><p>Le dipendenze dell'assembly SxS non verranno installate in fase di pubblicazione.</p></td>
<td align="left"><p>Le dipendenze dell'assembly SxS devono essere preinstallate.</p></td>
</tr>
</tbody>
</table>



### Creazione di un nuovo pacchetto di applicazione virtuale nel sequencer

Se durante il monitoraggio del sequencer viene installato un assembly SxS, ad esempio un runtime VC + +, come parte dell'installazione di un'applicazione, l'assembly SxS verrà rilevato e incluso automaticamente nel pacchetto. L'amministratore riceverà una notifica e avrà l'opzione di escludere l'assembly SxS.

**Lato client**:

Quando si pubblica un pacchetto di applicazione virtuale, il client App-V rileverà se è già installata una dipendenza di SxS necessaria. Se la dipendenza non è disponibile nel computer ed è inclusa nel pacchetto, un Windows Installer tradizionale (.** MSI**) verrà avviata l'installazione dell'assembly SxS. Come descritto in precedenza, è sufficiente installare la dipendenza dal computer in cui viene eseguito il client per verificare che l'installazione di Windows Installer (con estensione msi) non si verifichi.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Considerazioni</th>
<th align="left">Vantaggi</th>
<th align="left">Sui compromessi nella</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usare i file di configurazione dinamica in modo selettivo</p></td>
<td align="left"><p>Il client App-V 5,1 deve analizzare ed elaborare questi file di configurazione dinamica.</p>
<p>Essere consapevoli delle dimensioni e della complessità (esecuzione di script, inclusioni/esclusioni di ORSAE) del file.</p>
<p>I numerosi pacchetti di applicazioni virtuali possono avere già file di configurazioni dinamiche specifici dell'utente o del computer.</p></td>
<td align="left"><p>Gli orari di pubblicazione migliorano se questi file vengono usati in modo selettivo o non.</p></td>
<td align="left"><p>I pacchetti di applicazioni virtuali devono essere riconfigurati singolarmente o tramite la console di gestione di App-V Server per rimuovere i file di configurazione dinamica associati.</p></td>
</tr>
</tbody>
</table>



### Disabilitazione di una configurazione dinamica tramite PowerShell

-   Per i pacchetti già pubblicati, è possibile usare `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` senza

    Parametro **-DynamicDeploymentConfiguration**

-   Allo stesso modo, quando si aggiungono nuovi pacchetti in uso `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , non usare la

    **-Parametro DynamicDeploymentConfiguration** .

Per la documentazione su come applicare una configurazione dinamica, vedere:

-   [Come applicare il file di configurazione utente con PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [Come applicare il file di configurazione della distribuzione con PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Considerazioni</th>
<th align="left">Vantaggi</th>
<th align="left">Sui compromessi nella</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Account per l'esecuzione di script sincroni durante il ciclo di vita del pacchetto.</p></td>
<td align="left"><p>Se la garanzia di script è incorporata nel pacchetto, Add (PowerShell) potrebbe essere significativamente più lento.</p>
<p>L'esecuzione di script durante l'avvio dell'applicazione virtuale (StartVirtualEnvironment, StartProcess quale nome) e/o Add + Publish avrà un impatto sulle prestazioni percepite durante una o più delle operazioni del ciclo di vita.</p></td>
<td align="left"><p>L'uso di script asincroni (non bloccanti) assicura che le operazioni di ciclo di vita vengano completate in modo efficiente.</p></td>
<td align="left"><p>Questo passaggio richiede la conoscenza della gestione di tutti i pacchetti di applicazioni virtuali con garanzie di script incorporato, che hanno associato file di configurazioni dinamiche e che fanno riferimento ed eseguono script in modo sincrono.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Rimuovere i tipi di carattere virtuali estranei dal pacchetto.</p></td>
<td align="left"><p>La maggior parte delle applicazioni esaminate dal team di prodotti App-V conteneva un numero limitato di tipi di carattere, in genere meno di 20.</p></td>
<td align="left"><p>I tipi di carattere virtuali incidono sulle prestazioni di aggiornamento.</p></td>
<td align="left"><p>I tipi di carattere desiderati devono essere abilitati/installati in modo nativo. Per istruzioni, vedere installare o disinstallare tipi di carattere.</p></td>
</tr>
</tbody>
</table>



### Determinazione dei tipi di carattere virtuali presenti nel pacchetto

-   Creare una copia del pacchetto.

-   Rinomina pacchetto \ _copy. AppV in Package\_copy.zip

-   Aprire AppxManifest.xml e individuare le operazioni seguenti:

    &lt;appv: Extension Category = "AppV. fonts"&gt;

    &lt;appv: tipi di carattere&gt;

    &lt;appv: font path = "\ [{fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /appv: tipo di carattere&gt;

    **Nota**  
    Se sono presenti tipi di carattere contrassegnati come **DelayLoad**, il primo avvio non verrà influenzato.



~~~
&lt;/appv:Fonts&gt;
~~~

### Esclusione di tipi di carattere virtuali dal pacchetto

Usare il file di configurazione dinamica più adatto per l'ambito utente, ovvero la configurazione della distribuzione per tutti gli utenti del computer, la configurazione utente per utente o utenti specifici.

-   Disabilitare i tipi di carattere con la configurazione di distribuzione o utente.

Tipi di carattere

--&gt;

&lt;Tipi di carattere abilitati = "falso"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> Terminologia di guida alle prestazioni di App-V 5,1


I termini seguenti vengono usati per descrivere concetti e azioni correlati all'ottimizzazione delle prestazioni di App-V 5,1.

-   **Complessità** : si riferisce a una o più caratteristiche del pacchetto che potrebbero avere un impatto sulle prestazioni durante la configurazione preliminare (**Add-AppvClientPackage**) o Integration (**Publish-AppvClientPackage**). Alcune caratteristiche dell'esempio sono: dimensione del manifesto, numero di tipi di carattere virtuali, numero di file.

-   **De-integrare** : rimuove le integrazioni degli utenti

-   **Reintegrarsi** : applica le integrazioni degli utenti.

-   **Non persistente, in pool** : crea un computer che gestisce un ambiente virtuale ogni volta che effettua l'accesso.

-   **Persistente, personale,** un computer che gestisce un ambiente virtuale che rimane invariato per ogni account di accesso.

-   Con **stato** -per questo documento, implica che le integrazioni degli utenti vengano rese persistenti tra le sessioni e che una tecnologia di gestione dell'ambiente utente venga usata in combinazione con RDSH non persistente o VDI.

-   **Apolide** : rappresenta uno scenario in cui nessun stato utente viene mantenuto tra le sessioni.

-   **Trigger** -(o trigger di azione nativa). UPM usa questi tipi di trigger per avviare operazioni di monitoraggio o sincronizzazione.

-   **User Experience** -nel contesto dell'App-V 5,1, l'esperienza utente, quantitativamente, è la somma delle parti seguenti:

    -   Dal punto in cui gli utenti avviano un log-in quando sono in grado di manipolare il desktop.

    -   Dal punto in cui il desktop può essere interagito con il punto di inizio di un aggiornamento della pubblicazione (in termini di PowerShell, sincronizzazione) quando si usa l'infrastruttura di server completo di App-V 5,1. In istanze autonome, è il momento in cui vengono avviati i comandi di PowerShell **Add-AppVClientPackage** e **Publish-AppVClientPackage** .

    -   Dall'inizio al completamento dell'aggiornamento della pubblicazione. In istanze autonome questa è la prima dell'ultima applicazione virtuale pubblicata.

    -   Dal punto in cui è disponibile l'applicazione virtuale per l'avvio da un collegamento. In alternativa, è il punto in cui è registrata l'associazione del tipo di file e verrà avviata un'applicazione virtuale specificata.

-   **Gestione dei profili utente** : approccio controllato e strutturato per la gestione dei componenti utente associati all'ambiente. Ad esempio, i profili utente, la gestione delle preferenze e dei criteri, il controllo delle applicazioni e la distribuzione delle applicazioni. Puoi usare le soluzioni di scripting o di terze parti per configurare l'ambiente in base alle esigenze.






## Argomenti correlati


[Guida dell'amministratore di Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)









