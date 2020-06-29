---
title: Creazione e gestione di applicazioni virtualizzate di App-V 5.1
description: Creazione e gestione di applicazioni virtualizzate di App-V 5.1
author: dansimp
ms.assetid: 26be4331-88eb-4cfb-9d82-e63d7ee54576
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 207529fb5d5333694d31a82f44f08b35513dd4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805914"
---
# Creazione e gestione di applicazioni virtualizzate di App-V 5.1


Dopo aver distribuito correttamente il sequencer di Microsoft Application Virtualization (App-V) 5,1, è possibile usarlo per monitorare e registrare il processo di installazione e configurazione per un'applicazione da eseguire come applicazione virtualizzata.

**Nota**  Per altre informazioni sulla configurazione dell'App-V 5,1 sequencer, la sequenziazione delle procedure consigliate e un esempio di creazione e aggiornamento di un'applicazione virtuale, vedere la [Guida alla sequenziazione di Microsoft Application Virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V%205.0%20Sequencing%20Guide.docx).

**Nota** Il sequencer App-V 5. x non può sequenziare le applicazioni con nomi di file corrispondenti "CO_ &lt; x &gt; " dove x è un numero qualsiasi. Verrà generato l'errore 0x8007139F.

## Sequenziazione di un'applicazione


Puoi usare il sequencer App-V 5,1 per eseguire le attività seguenti:

-   Creare pacchetti virtuali che possono essere distribuiti nei computer che eseguono il client App-V 5,1.

-   Aggiornare i pacchetti esistenti. Puoi espandere un pacchetto esistente nel computer che esegue il sequencer e quindi aggiornare l'applicazione per creare una versione più recente.

-   Modificare le informazioni di configurazione associate a un pacchetto esistente. Ad esempio, è possibile aggiungere un collegamento o modificare un'associazione di tipi di file.

    **Nota**  È necessario creare tasti di scelta rapida e salvarli in un percorso di rete disponibile per consentire il roaming. Se un collegamento viene creato e salvato in una posizione privata, il pacchetto deve essere pubblicato localmente nel computer che esegue il client App-V 5,1.
 
-   Convertire i pacchetti virtuali esistenti.

Il sequencer usa la directory **% tmp% \ \ Scratch** o **% Temp% \ \ Scratch** e la directory **Temp** per archiviare i file temporanei durante la sequenziazione. Nel computer che esegue il sequencer devi configurare queste directory con spazio su disco gratuito equivalente ai requisiti stimati per l'installazione dell'applicazione. La configurazione delle directory Temp e della directory Temp in partizioni disco rigido diverse può contribuire a migliorare le prestazioni durante la sequenziazione.

Quando si usa sequencer per creare una nuova applicazione virtuale, vengono creati i file elencati di seguito. Questi file includono il pacchetto App-V 5,1.

-   file con estensione msi. Questo file di Windows Installer (con estensione msi) viene creato dal sequencer e viene usato per installare il pacchetto virtuale nei computer di destinazione.

-   Report.xml file. In questo file, sequencer Salva tutti i problemi, gli avvisi e gli errori individuati durante la sequenziazione. Visualizza le informazioni dopo la creazione del pacchetto. Questo report può essere segnalato per la diagnosi e la risoluzione dei problemi.

-   file con estensione AppV. Questo è il file dell'applicazione virtuale.

-   File di configurazione della distribuzione. Il file di configurazione della distribuzione determina il modo in cui verrà distribuita l'applicazione virtuale per i computer di destinazione.

-   File di configurazione utente. Il file di configurazione dell'utente determina il modo in cui verrà eseguita l'applicazione virtuale nei computer di destinazione.

**Importante**  È necessario configurare le cartelle% TMP% e% TEMP% che il convertitore di pacchetti usa per essere un percorso e una directory sicuri. Un percorso sicuro è accessibile solo da un amministratore. Inoltre, quando si sequenzia il pacchetto, è necessario salvare il pacchetto in una posizione sicura oppure assicurarsi che nessun altro utente sia autorizzato a eseguire l'accesso durante il processo di conversione e monitoraggio. 

La finestra di dialogo **Opzioni** nella console sequencer contiene le schede seguenti:

-   **Generale**. Usare questa scheda per consentire l'esecuzione di aggiornamenti Microsoft durante la sequenziazione. Selezionare **Accoda versione pacchetto a nomefile** per configurare la sequenza per aggiungere un numero di versione al pacchetto virtualizzato che viene sequenziato. Selezionare **Considera sempre attendibile l'origine degli acceleratori di pacchetto** per creare pacchetti virtualizzati usando un Acceleratore pacchetto senza richiedere l'autorizzazione.

    **Importante**  Gli acceleratori di pacchetti creati con App-V 4.6 non sono supportati da App-V 5,1.     

-   **Analizzare gli elementi**. Questa scheda Visualizza i percorsi di percorso file associati che verranno analizzati o suddivisi in token nell'ambiente virtuale. I token sono utili per l'aggiunta di file tramite la scheda **file di pacchetto** in **modifica avanzata**.

-   **Elementi di esclusione**. Usare questa scheda per specificare quali cartelle e directory non devono essere monitorate durante la sequenziazione. Per aggiungere i dati dell'applicazione locale salvati nella cartella dati locali dell'app nel pacchetto, fare clic su **nuovo** e specificare la posizione e il **tipo di mapping**associato. Questa opzione è obbligatoria per alcuni pacchetti.

App-V 5,1 supporta le applicazioni che includono i servizi Microsoft Windows. Se un'applicazione include un servizio Windows, il servizio verrà incluso nel pacchetto virtuale sequenziato finché viene installato durante il monitoraggio da parte del sequencer. Se un'applicazione virtuale crea un servizio Windows quando viene eseguito inizialmente, in seguito, dopo l'installazione, l'applicazione deve essere eseguita durante il monitoraggio del sequencer in modo che il servizio Windows venga aggiunto al pacchetto. Sono supportati solo i servizi eseguiti con l'account di sistema locale. I servizi configurati per l'autostart o l'avvio in ritardo vengono avviati prima che la prima applicazione virtuale in un pacchetto venga eseguita all'interno dell'ambiente virtuale del pacchetto. I servizi Windows configurati per l'avvio su richiesta da un'applicazione vengono avviati quando l'applicazione virtuale all'interno del pacchetto avvia il servizio tramite chiamata API.

[Come sequenziare una nuova applicazione con App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)

## <a href="" id="---------app-v-5-1-shell-extension-support"></a> Supporto dell'estensione di Shell per App-V 5.1


App-V 5.1 supporta le estensioni della shell. Le estensioni della shell verranno rilevate e incorporate nel pacchetto durante la sequenziazione.

Le estensioni della shell vengono inserite automaticamente nel pacchetto durante il processo di sequenziazione. Quando il pacchetto viene pubblicato, l'estensione della Shell offre agli utenti le stesse funzionalità di se l'applicazione è stata installata localmente.

**Requisiti per l'uso delle estensioni della shell:**

-   I pacchetti che contengono estensioni della shell incorporata devono essere pubblicati globalmente. L'applicazione non richiede alcuna installazione o configurazione aggiuntiva nel client per abilitare la funzionalità di estensione della shell.

-   Il "bit" dell'applicazione, il sequencer e il client App-V devono corrispondere o le estensioni della shell non funzionano. Ad esempio:

    -   La versione dell'applicazione è 64 bit.

    -   Il sequencer viene eseguito in un computer a 64 bit.

    -   Il pacchetto viene recapitato a un computer client App-V a 64 bit.

La tabella seguente elenca le estensioni della shell supportate:

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
<td align="left"><p>Controlla l'azione in cui fare clic con il pulsante destro del mouse, trascinare e rilasciare e modificare il menu di scelta rapida visualizzato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Trascinare il gestore di destinazione</p></td>
<td align="left"><p>Controlla l'azione dopo il trascinamento di un oggetto dati e l'eliminazione di una destinazione di rilascio, ad esempio un file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore oggetti dati</p></td>
<td align="left"><p>Controlla l'azione dopo la copia di un file negli Appunti o trascinato e rilasciata su una destinazione di rilascio. Può includere altri formati di Appunti nella destinazione di rilascio.</p></td>
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
<td align="left"><p>Consente la creazione e la visualizzazione di colonne personalizzate nella <strong> visualizzazione dettagli di Esplora risorse </strong> . Può essere usato per estendere l'ordinamento e il raggruppamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore di anteprime</p></td>
<td align="left"><p>Consente di visualizzare un'anteprima di un file nel riquadro di anteprima di Windows Explorer.</p></td>
</tr>
</tbody>
</table>

## Supporto dell'estensione di file copy on Write (mucca)

Copia in scrittura (mucca) le estensioni di file consentono a App-V 5,1 di scrivere in modo dinamico in posizioni specifiche contenute nel pacchetto virtuale durante l'uso.

Nella tabella seguente sono visualizzati i tipi di file che possono esistere in un pacchetto virtuale nella directory VFS, ma non possono essere aggiornati nel computer che gestisce il client App-V 5,1. Tutti gli altri file e directory possono essere modificati.

| Tipo di file     |               |               |               |               |               |
|------------   |-------------  |-------------  |------------   |------------   |------------   |
| . acm          | . asa          | .asp          | . aspx         | . ax           | .bat          |
| .cer          | .chm          | . clb          | .cmd          | .cnt          | . cnv          |
| .com          | .cpl          | . CPX          | .crt          | .dll          | .drv          |
| . ESC          | .exe          | .fon          | .grp          | .hlp          | .hta          |
| . IME          | .inf          | .ins          | .isp          | . its          | .js           |
| .jse          | .lnk          | .msc          | .msi          | .msp          | .mst          |
| . mui          | . nls          | .ocx          | . PAL          | .pcd          | .pif          |
| .reg          | .scf          | .scr          | . SCT          | .shb          | .shs          |
| .sys          | . tlb          | . tsp          | .url          | .vb           | .vbe          |
| .vbs          | .vsmacros     | .ws           | .wsf          | .wsh          |               |


## Modifica di un pacchetto di applicazione virtuale esistente


Puoi usare il sequencer per modificare un pacchetto esistente. Il computer in cui si esegue questa operazione deve corrispondere all'architettura di chip del computer usato per creare l'applicazione. Ad esempio, se hai inizialmente sequenziato un pacchetto usando un computer che usa un sistema operativo a 64 bit, devi modificare il pacchetto usando un computer che usa un sistema operativo a 64 bit.

[Come modificare un pacchetto applicazione virtuale esistente](how-to-modify-an-existing-virtual-application-package-51.md)

## Creazione di un modello di progetto


Un file con estensione appvt è un modello di progetto che può essere usato per salvare le impostazioni comunemente applicate e personalizzate. Puoi quindi usare più facilmente queste impostazioni per le sequenziazioni future.

I modelli di progetto di App-V 5,1 si differenziano dagli acceleratori delle applicazioni App-V 5,1 perché gli acceleratori di applicazioni App-V 5,1 sono specifici dell'applicazione e i modelli di progetto di App-V 5,1 possono essere applicati a più applicazioni. Non è inoltre possibile usare un modello di progetto quando si usa un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale. Le impostazioni generali seguenti vengono salvate con un modello di progetto App-V 5,1:

Un modello può specificare e archiviare più impostazioni nel modo seguente:

-   **Opzioni di monitoraggio avanzate**. Consente l'esecuzione di Microsoft Update durante il monitoraggio. Consente di salvare le impostazioni dell'opzione interazione locale

-   **Opzioni generali**. Consente l'uso di **Windows Installer**, **accodare la versione del pacchetto al nome del file**.

-   **Elementi di esclusione.** Contiene l'elenco dei criteri di esclusione.

[Come creare e usare un modello di progetto](how-to-create-and-use-a-project-template51.md)

## Creazione di un Acceleratore pacchetto


**Nota**  Gli acceleratori di pacchetti creati con una versione precedente di App-V devono essere ricreati usando App-V 5,1.

Puoi usare gli acceleratori del pacchetto App-V 5,1 per generare automaticamente nuovi pacchetti di applicazioni virtuali. Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto.

In alcune situazioni, per creare l'Acceleratore pacchetto, potrebbe essere necessario installare l'applicazione localmente nel computer che esegue il sequencer. In questi casi, devi prima di tutto provare a creare l'Acceleratore pacchetto con il supporto di installazione. Se sono necessari più file mancanti, è necessario installare l'applicazione localmente nel computer in cui viene eseguito il sequencer e quindi creare l'acceleratore del pacchetto.

Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto. La creazione di acceleratori pacchetto App-V 5,1 è un'attività avanzata. Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente. È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto App-V 5,1.

[Come creare un acceleratore pacchetto](how-to-create-a-package-accelerator51.md)

[Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)

## Segnalazione errori sequenziatore


Il sequencer App-V 5,1 può rilevare i problemi di sequenziazione comuni durante la sequenziazione. La pagina del **report di installazione** alla fine della sequenziazione guidata Visualizza i messaggi di diagnostica categorizzati in **errori**, **avvisi**e **informazioni** in base alla gravità del problema.

Puoi anche trovare altre informazioni sulla sequenziazione degli errori usando il Visualizzatore eventi di Windows.


## <a href="" id="other-resources-for-the-app-v-5-1-sequencer-"></a>Altre risorse per l'App-V 5,1 sequencer


-   [Operazioni per App-V 5.1](operations-for-app-v-51.md)

