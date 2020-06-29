---
title: Informazioni su App-V 5.1
description: Informazioni su App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806111"
---
# Informazioni su App-V 5.1


Usare le sezioni seguenti per esaminare le informazioni sulle modifiche significative che si applicano alla virtualizzazione delle applicazioni (App-V) 5,1:

[Prerequisiti software App-V 5,1 e configurazioni supportate](#bkmk-51-prereq-configs)

[Migrazione a App-V 5,1](#bkmk-migrate-to-51)

[Novità dell'App-V 5,1](#bkmk-whatsnew)

[Supporto di App-V per Windows 10](#bkmk-win10support)

[Modifiche alla console di gestione di App-V](#bkmk-mgmtconsole)

[Miglioramenti di Sequencer](#bkmk-seqimprove)

[Miglioramenti al convertitore di pacchetti](#bkmk-pkgconvimprove)

[Supporto per più script in un singolo trigger di evento](#bkmk-supmultscripts)

[Il percorso hardcoded della cartella di installazione viene reindirizzato alla radice del file system virtuale](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>Prerequisiti software App-V 5,1 e configurazioni supportate


Vedere i collegamenti seguenti per i prerequisiti software App-V 5,1 e le configurazioni supportate.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Collegamenti ai prerequisiti e alle configurazioni supportate</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">Prerequisiti di App-V 5.1</a></p></td>
<td align="left"><p>Software prerequisito che è necessario installare prima di avviare l'installazione di App-V 5,1</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Configurazioni supportate di App-V 5.1</a></p></td>
<td align="left"><p>Requisiti hardware e sistemi operativi supportati per i componenti App-V Server, sequencer e client</p></td>
</tr>
</tbody>
</table>



**Supporto per l'uso di Configuration Manager con App-V:** App-V 5,1 supporta System Center 2012 R2 Configuration Manager SP1. Per informazioni su come integrare l'ambiente App-V con Configuration Manager e Configuration Manager, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .

## <a href="" id="bkmk-migrate-to-51"></a>Migrazione a App-V 5,1


Usare le informazioni seguenti per eseguire l'aggiornamento a App-V 5,1 dalle versioni precedenti. Per altre informazioni, vedere [eseguire la migrazione a App-V 5,1 da una versione precedente](migrating-to-app-v-51-from-a-previous-version.md) .

### Prima di iniziare l'aggiornamento

Prima di iniziare l'aggiornamento, esaminare le informazioni seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementi da rivedere prima dell'aggiornamento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componenti da aggiornare in qualsiasi ordine</p></td>
<td align="left"><ol>
<li><p>App-V Server</p></li>
<li><p>Sequencer</p></li>
<li><p>App-V client o client RDS (Remote Desktop Services) App-V</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Prima di App-V 5,0 SP2, l'interfaccia utente di gestione client è stata fornita con l'installazione del client App-V. Per le installazioni di App-V 5,0 SP2 (o versioni successive), puoi usare l'interfaccia utente di gestione client eseguendo il download dall' <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> applicazione di interfaccia utente client Application Virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiornamento da App-V 4. x</p></td>
<td align="left"><p>Devi prima eseguire l'aggiornamento a App-V 5,0. Non è possibile eseguire l'aggiornamento direttamente da App-V 4. x a App-V 5,1. Per altre informazioni, vedi:</p>
<ul>
<li><p>"Differenze tra App-V 4,6 e App-V 5,0" in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> informazioni su App-v 5,0</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Pianificazione per la migrazione da una versione precedente di App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiornamento da App-V 5,0 o versione successiva</p></td>
<td align="left"><p>È possibile eseguire l'aggiornamento a App-V 5,1 direttamente da una delle versioni seguenti:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
<li><p>App-V 5,0 SP3</p></li>
</ul>
<p>Per eseguire l'aggiornamento a App-V 5,1, seguire la procedura descritta nelle sezioni rimanenti di questo argomento.</p>
<p>I pacchetti e i gruppi di connessioni continueranno a funzionare con l'App-V 5,1 al momento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Procedura per aggiornare l'infrastruttura di App-V

Completare i passaggi seguenti per aggiornare ogni componente dell'infrastruttura App-V in App-V 5,1. L'ordine seguente è solo un suggerimento; è possibile aggiornare i componenti in qualsiasi ordine.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Per altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passaggio 1: aggiornare l'App-V Server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se non si usa App-V Server, ignorare questo passaggio e passare al passaggio successivo.</p>
</div>
<div>

</div></td>
<td align="left"><p>Segui questa procedura: </p>
<ol>
<li><p>Eseguire una delle operazioni seguenti, a seconda del metodo usato per aggiornare il database di gestione e/o il database di report:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo di aggiornamento del database</th>
<th align="left">Passaggio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Ignorare questo passaggio e passare al passaggio 2, "Se si esegue l'aggiornamento del server App-V..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Script SQL</p></td>
<td align="left"><p>Seguire i passaggi descritti in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> come distribuire i database di App-V tramite gli script SQL </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>Se si sta aggiornando il pacchetto di hotfix App-v 5,0 SP1 3 o versione successiva, eseguire la procedura descritta nella sezione <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> controllare le chiavi del registro di sistema dopo l'installazione del server App-v 5,0 SP3 </a> .</p></li>
<li><p>Seguire la procedura descritta in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> come distribuire il server App-V 5,1</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Passaggio 2: aggiornare l'App-V Sequencer.</p></td>
<td align="left"><p>Vedere <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> come installare il sequencer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passaggio 3: aggiornare il client App-V o client RDS App-v.</p></td>
<td align="left"><p>Scopri <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> come distribuire il client App-V </a> .</p></td>
</tr>
</tbody>
</table>



### Conversione di pacchetti creati con una versione precedente di App-V

Usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni di App-V precedenti a App-V 5,0. Il convertitore di pacchetti usa PowerShell per convertire i pacchetti e può aiutare a automatizzare il processo se sono presenti molti pacchetti che richiedono la conversione.

**Nota**  
I pacchetti App-V 5,1 sono esattamente gli stessi dei pacchetti App-V 5,0. Non è stato modificato il formato del pacchetto tra le versioni e quindi non è necessario convertire i pacchetti App-V 5,0 in pacchetti App-V 5,1.



## <a href="" id="bkmk-whatsnew"></a>Novità dell'App-V 5,1


Queste sezioni sono per gli utenti che hanno già familiarità con App-V e vogliono sapere cosa è cambiato in App-V 5,1. Se non si ha familiarità con l'App-V, è consigliabile iniziare leggendo [la pianificazione per l'app-v 5,1](planning-for-app-v-51.md).

### <a href="" id="bkmk-win10support"></a>Supporto di App-V per Windows 10

La tabella seguente elenca il supporto di Windows 10 per App-V. Windows 10 non è supportato nelle versioni di App-V precedenti a App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">App-V 5.1</th>
<th align="left">App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client RDS App-V</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequencer App-V</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>Modifiche alla console di gestione di App-V

Questa sezione confronta le funzionalità correnti e precedenti della console di gestione di App-V.

### Silverlight non è più necessario

L'interfaccia utente della console di gestione non richiede più Silverlight. La console di gestione di 5,1 è basata su HTML5 e JavaScript.

### Le notifiche e i messaggi vengono visualizzati singolarmente in una finestra di dialogo

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuovo in App-V 5,1</th>
<th align="left">Prima dell'App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Indicatore numero di messaggi:</strong></p>
<p>Sulla barra del titolo di App-V Management Console viene ora visualizzato un numero accanto a un'icona di contrassegno per indicare il numero di messaggi in attesa di lettura.</p></td>
<td align="left"><p>È possibile visualizzare solo un messaggio o un errore alla volta e non è stato possibile determinare il numero di messaggi.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Aspetto del messaggio:</strong></p>
<ul>
<li><p>I messaggi che richiedono l'input dell'utente vengono visualizzati in una finestra di dialogo separata visualizzata nella parte superiore della pagina corrente che si stava visualizzando e richiedono una risposta prima di poterli respingere.</p></li>
<li><p>I messaggi e gli errori vengono visualizzati in un elenco, con uno sotto l'altro.</p></li>
</ul></td>
<td align="left"><p>È possibile visualizzare solo un messaggio o un errore alla volta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Invio di messaggi:</strong></p>
<p>Usare il <strong> collegamento Ignora tutto </strong> per ignorare tutti i messaggi e gli errori contemporaneamente o eliminarli uno alla volta.</p></td>
<td align="left"><p>È possibile ignorare i messaggi e gli errori solo uno alla volta.</p></td>
</tr>
</tbody>
</table>



### Le pagine della console ora sono URL separati

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuovo in App-V 5,1</th>
<th align="left">Prima dell'App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ogni pagina della console ha un URL diverso, che consente di contrassegnare pagine specifiche per l'accesso rapido in futuro.</p>
<p>Il numero visualizzato in alcuni URL indica il pacchetto specifico. Questi numeri sono univoci.</p></td>
<td align="left"><p>Si accede a tutte le pagine della console tramite lo stesso URL.</p></td>
</tr>
</tbody>
</table>



### Pagina nuovi gruppi di connessioni separati e opzione di menu

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuovo in App-V 5,1</th>
<th align="left">Prima dell'App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>La pagina gruppi di connessioni fa ora parte del menu principale, allo stesso livello della pagina pacchetti.</p></td>
<td align="left"><p>Per aprire la pagina gruppi di connessioni, è possibile spostarsi nella pagina pacchetti.</p></td>
</tr>
</tbody>
</table>



### Le opzioni di menu per i pacchetti sono cambiate

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuovo in App-V 5,1</th>
<th align="left">Prima dell'App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le opzioni seguenti sono ora pulsanti visualizzati nella parte inferiore della pagina pacchetti:</p>
<ul>
<li><p>Aggiungere o aggiornare</p></li>
<li><p>Pubblicazione</p></li>
<li><p>Annullare la pubblicazione</p></li>
<li><p>Delete</p></li>
</ul>
<p>Le opzioni seguenti verranno comunque visualizzate quando si fa clic con il pulsante destro del mouse su un pacchetto per aprire il menu di scelta rapida a discesa:</p>
<ul>
<li><p>Pubblicazione</p></li>
<li><p>Annullare la pubblicazione</p></li>
<li><p>Modificare l'accesso AD</p></li>
<li><p>Modificare la configurazione della distribuzione</p></li>
<li><p>Trasferire la configurazione della distribuzione da...</p></li>
<li><p>Trasferire l'accesso e la configurazione da...</p></li>
<li><p>Delete</p></li>
</ul>
<p>Quando si fa clic su <strong> Elimina </strong> per rimuovere un pacchetto, viene visualizzata una finestra di dialogo che chiede di confermare che si vuole eliminare il pacchetto.</p></td>
<td align="left"><p>L' <strong> opzione Aggiungi o aggiorna </strong> è stata un pulsante nella parte superiore destra della pagina pacchetti.</p>
<p>Le <strong> </strong> Opzioni pubblica, Annulla <strong> pubblica </strong> ed <strong> Elimina </strong> sono disponibili solo se si fa clic con il pulsante destro del mouse su un nome di pacchetto nell'elenco pacchetti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le operazioni del pacchetto seguenti sono ora pulsanti nella pagina dei dettagli del pacchetto per ogni pacchetto:</p>
<ul>
<li><p>Transfer (menu a discesa con le opzioni seguenti):</p>
<ul>
<li><p>Trasferire la configurazione della distribuzione da...</p></li>
<li><p>Trasferire l'accesso e la configurazione da...</p></li>
</ul></li>
<li><p>Modifica (gruppi di connessione e accesso AD)</p></li>
<li><p>Annullare la pubblicazione</p></li>
<li><p>Delete</p></li>
<li><p>Modificare la configurazione predefinita</p></li>
</ul></td>
<td align="left"><p>Queste opzioni del pacchetto sono disponibili solo se si fa clic con il pulsante destro del mouse su un nome di pacchetto nell'elenco pacchetti.</p></td>
</tr>
</tbody>
</table>



### Le icone nel riquadro sinistro hanno nuovi colori e testo

I colori delle icone nel riquadro sinistro sono stati modificati e il testo è stato aggiunto per rendere le icone coerenti con altri prodotti Microsoft.

### La pagina di panoramica è stata rimossa

Nel riquadro sinistro della console di gestione è stata rimossa l'opzione di menu panoramica e la pagina di panoramica associata.

### <a href="" id="bkmk-seqimprove"></a>Miglioramenti di Sequencer

Sono stati apportati i miglioramenti seguenti per l'editor di pacchetti nell'App-V 5,1 Sequencer.

### Importare ed esportare il file manifesto

È possibile importare ed esportare il file AppxManifest.xml. Per esportare il file manifesto, selezionare la scheda **Avanzate** e nella casella manifesto file fare clic su **Esporta...**. È possibile apportare modifiche al file manifesto, ad esempio rimuovere le estensioni della shell o modificare le associazioni di tipi di file.

Dopo avere apportato le modifiche, fare clic su **Importa...** e selezionare il file modificato. Dopo aver eseguito correttamente l'importazione, il file manifesto viene immediatamente aggiornato all'interno dell'editor di pacchetti.

**Attenzione**  
Quando si importa il file, le modifiche vengono convalidate in base allo schema XML. Se il file non è valido, viene visualizzato un messaggio di errore. Tenere presente che è possibile importare un file convalidato in base allo schema XML, ma che potrebbe comunque non funzionare per altri motivi.



### Aggiunta di Windows 10 all'elenco dei sistemi operativi

Nella scheda distribuzione i bit di Windows 10 32 bit e Windows 10-64 sono stati aggiunti all'elenco dei sistemi operativi per cui è possibile sequenziare un pacchetto. Se si seleziona **un sistema operativo**, Windows 10 viene incluso automaticamente tra i sistemi operativi supportati dal pacchetto sequenziato.

### Il percorso corrente viene visualizzato nella parte inferiore dell'editor del registro di sistema virtuale

Nella scheda Registro di sistema virtuale il percorso viene visualizzato nella parte inferiore dell'editor del registro di sistema virtuale, che consente di determinare la chiave attualmente selezionata. In precedenza era necessario scorrere l'albero del registro di sistema per trovare la chiave attualmente selezionata.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>Finestra di dialogo "trova e Sostituisci" combinata e tasti di scelta rapida aggiunti nell'editor del registro di sistema virtuale

Nell'editor del registro di sistema virtuale sono stati aggiunti tasti di scelta rapida per l'opzione trova (CTRL + F) e una finestra di dialogo che combina le attività "trova" e "Sostituisci" per consentire l'individuazione e la sostituzione di valori e dati. Per accedere a questa finestra di dialogo combinata, selezionare una chiave ed eseguire una delle operazioni seguenti:

-   Premere **CTRL + H**

-   Fare clic con il pulsante destro del mouse su un tasto e scegliere **Sostituisci**.

-   Selezionare **Visualizza** il &gt; **Registro di sistema virtuale** &gt; **Sostituisci**.

In precedenza la finestra di dialogo "Sostituisci" non esisteva e bisognava apportare le modifiche manualmente.

### Rinominare le chiavi del registro di sistema e i file di pacchetto

È possibile rinominare i file e le chiavi del registro di sistema virtuali senza problemi con il sequencer. In precedenza, il sequencer ha smesso di funzionare se si è tentato di rinominare una chiave.

### Importare ed esportare le chiavi del registro di sistema virtuali

È possibile importare ed esportare le chiavi del registro di sistema virtuali. Per importare una chiave, fare clic con il pulsante destro del mouse sul nodo in cui importare la chiave, passare alla chiave che si vuole importare e quindi fare clic su **Importa**. Per esportare una chiave, fare clic con il pulsante destro del mouse sulla chiave e scegliere **Esporta**.

### Importare una directory nel file system virtuale

È possibile importare una directory in VFS. Per importare una directory, fare clic sulla scheda **file di pacchetto** e quindi su **Visualizza** &gt; directory di importazione di **virtual file System** &gt; **Import Directory**. Se si tenta di importare una directory che contiene file già presenti in VFS, l'importazione non riesce e viene visualizzato un messaggio esplicativo. Prima di App-V 5,1 non è stato possibile importare directory.

### Importare o esportare un file VFS senza doverlo eliminare e quindi aggiungerlo di nuovo al pacchetto

È possibile importare o esportare file da VFS senza dover eliminare il file e quindi aggiungerlo di nuovo al pacchetto. Ad esempio, è possibile usare questa caratteristica per esportare un log delle modifiche in un'unità locale, modificare il file usando un editor esterno e quindi reimportare il file in VFS.

Per esportare un file, selezionare la scheda **file di pacchetto** , fare clic con il pulsante destro del mouse sul file in VFS, scegliere **Esporta**e scegliere un percorso di esportazione da cui è possibile apportare le modifiche.

Per importare un file, seleziona la scheda **file di pacchetto** e fai clic con il pulsante destro del mouse sul file che hai esportato. Passare al file modificato e quindi fare clic su **Importa**. Il file importato sovrascriverà il file esistente.

Dopo aver importato un file, è necessario salvare il pacchetto **File** facendo clic su &gt; **Salva**file.

### Menu per l'aggiunta di un file di pacchetto è stato spostato

L'opzione di menu per l'aggiunta di un file di pacchetto è stata spostata. Per trovare l'opzione Aggiungi, selezionare la scheda **file di pacchetto** , quindi fare clic su **Visualizza** file di file di &gt; **Virtual System** &gt; **Add**. In precedenza, hai fatto clic con il pulsante destro del mouse su una cartella sotto il nodo VFS e scegli **Aggiungi file**.

### Il nodo del registro di sistema virtuale espande il computer e gli hive utente per impostazione predefinita

Quando si apre il registro di sistema virtuale, gli hive del computer e degli utenti vengono visualizzati sotto il nodo del registro di livello principale. In precedenza era necessario espandere il nodo del registro di sistema per visualizzare gli hive sotto.

### Abilitare o disabilitare gli oggetti helper del browser

È possibile abilitare o disabilitare gli oggetti helper del browser selezionando una nuova casella di controllo, Abilita oggetti helper del browser, nella scheda avanzate dell'interfaccia utente di Sequencer. Se gli oggetti helper del browser:

-   Esiste nel pacchetto e sono abilitati, la casella di controllo è selezionata per impostazione predefinita.

-   Esistono nel pacchetto e sono disabilitati, la casella di controllo è deselezionata per impostazione predefinita.

-   Esiste nel pacchetto, con uno o più abilitato e uno o più disabilitato, la casella di controllo è impostata su indeterminata per impostazione predefinita.

-   Non sono presenti nel pacchetto, la casella di controllo è disabilitata.

### <a href="" id="bkmk-pkgconvimprove"></a>Miglioramenti al convertitore di pacchetti

Ora puoi usare il convertitore di pacchetti per convertire i pacchetti App-V 4,6 che contengono script e le informazioni del registro di sistema e gli script dei file di origine. OSD ora sono inclusi nell'output del convertitore di pacchetti.

Per altre informazioni, inclusi gli esempi, vedere [eseguire la migrazione a App-V 5,1 da una versione precedente](migrating-to-app-v-51-from-a-previous-version.md).

### <a href="" id="bkmk-supmultscripts"></a>Supporto per più script in un singolo trigger di evento

App-V 5,1 supporta l'uso di più script in un singolo trigger di evento per i pacchetti App-V, inclusi i pacchetti che si stanno convertendo da App-V 4,6 a App-V 5,0 o versioni successive. Per abilitare l'uso di più script, App-V 5,1 usa un'applicazione di avvio di script, denominata ScriptRunner.exe, che viene installata come parte dell'installazione del client App-V.

Per altre informazioni, incluso un elenco di trigger di eventi e il contesto in cui è possibile eseguire gli script, vedere la sezione Scripts in [informazioni sulla configurazione dinamica di App-V 5,1](about-app-v-51-dynamic-configuration.md).

### <a href="" id="bkmk-hardcodepath"></a>Il percorso hardcoded della cartella di installazione viene reindirizzato alla radice del file system virtuale

Quando si convertono i pacchetti da App-V 4,6 a 5,1, il pacchetto App-V 5,1 può accedere all'unità hardcoded che era necessario usare per la creazione di pacchetti di 4,6. La lettera dell'unità sarà l'unità selezionata come unità di installazione nel computer di sequenziazione di 4,6. (La lettera di unità predefinita è Q:\\.)

In precedenza, la cartella radice di 4,6 non è stata riconosciuta e non è stato possibile accedervi dai pacchetti App-V 5,0. I pacchetti App-V 5,1 possono accedere ai file codificati in base al percorso completo o possono enumerare i file a livello di codice nella radice dell'installazione di App-V 4,6.

**Dettagli tecnici:** Il convertitore di pacchetti App-V 5,1 salverà la cartella radice dell'installazione di App-V 4,6 e i nomi delle cartelle brevi nel file FilesystemMetadata.xml nell'elemento filesystem. Quando il client App-V 5,1 crea il processo virtuale, eseguirà il mapping delle richieste dalla radice di installazione di App-V 4,6 alla radice del file system virtuale.

## Come ottenere le tecnologie MDOP


App-V fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Argomenti correlati


[Note sulla versione per App-V 5.1](release-notes-for-app-v-51.md)









