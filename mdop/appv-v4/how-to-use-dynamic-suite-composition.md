---
title: Come usare Dynamic Suite Composition
description: Come usare Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816416"
---
# Come usare Dynamic Suite Composition


La composizione delle suite dinamiche nella virtualizzazione delle applicazioni consente di definire un'applicazione dipendente da un'altra applicazione, ad esempio middleware o plug-in. In questo modo l'applicazione può interagire con il middleware o il plug-in nell'ambiente virtuale, dove in genere questa operazione viene impedita. Ciò è utile perché un pacchetto di applicazione secondario può essere usato con diverse altre applicazioni, dette le *applicazioni principali*, che consentono a ogni applicazione principale di fare riferimento allo stesso pacchetto secondario.

Quando si sequenziano applicazioni che dipendono da plug-in come controlli ActiveX o da applicazioni che dipendono da middleware come OLE DB o Java Runtime Environment (JRE), è possibile usare la composizione di una famiglia di prodotti dinamici. Se ogni applicazione che ha usato questi componenti dipendenti richiede la sequenziazione, inclusi i componenti, gli aggiornamenti di questi componenti richiedono la risequenziazione di tutte le applicazioni principali. Se si sequenziano le applicazioni primarie senza i componenti e quindi si sequenzia il middleware o il plug-in come pacchetto secondario, è necessario aggiornare solo il pacchetto secondario.

Un vantaggio di questo approccio è che riduce le dimensioni dei pacchetti principali. Un altro vantaggio è che offre un migliore controllo delle autorizzazioni di accesso per le applicazioni secondarie. Tieni presente che l'applicazione secondaria può essere in streaming in modo normale e che non deve essere completamente memorizzata nella cache per l'esecuzione.

Un pacchetto principale può avere più di un pacchetto secondario. Tuttavia, è supportato un solo livello di dipendenza, quindi non è possibile definire un pacchetto secondario come dipendente da un altro pacchetto secondario. Anche l'applicazione secondaria può essere solo un middleware o un plug-in e non può essere un altro prodotto software completo.

Se si prevede di fare in modo che diverse applicazioni primarie dipendano da un singolo prodotto middleware, verificare di aver testato questa configurazione per determinare l'effetto potenziale sulle prestazioni del sistema prima di distribuirlo.

**Importante**  Le dipendenze del pacchetto possono essere specificate come obbligatorie per un'applicazione principale. Se un pacchetto secondario viene contrassegnato come obbligatorio e non è possibile accedervi per qualche motivo durante il caricamento, il caricamento del pacchetto secondario non riuscirà. Inoltre, l'applicazione principale non riesce quando l'utente tenta di avviarlo.

 

Puoi usare le procedure seguenti per creare un pacchetto secondario, sia per un componente plug-in che middleware, e quindi puoi usare la procedura finale per definire la dipendenza nel file OSD del pacchetto secondario.

**Per creare un pacchetto secondario per un plug-in tramite la composizione della famiglia di prodotti dinamici**

1.  In un computer di sequenziazione configurato con un'immagine pulita, installare Application Virtualization Sequencer e salvare lo stato del computer.

2.  Sequenziare l'applicazione principale e salvare il pacchetto nella cartella contenuto nel server.

3.  Ripristinare il computer di sequenziazione nello stato salvato dal passaggio 1.

4.  Installare e configurare l'applicazione principale localmente nel computer di sequenziazione.

    **Importante**  Devi specificare una nuova radice del pacchetto per il pacchetto secondario.

     

5.  Avviare la fase di monitoraggio del sequencer.

6.  Installare il plug-in nel computer di sequenziazione e configurarlo in base alle esigenze.

7.  Aprire l'applicazione principale e verificare che il plug-in funzioni correttamente.

8.  Nella console sequencer creare un'applicazione fittizia per rappresentare il pacchetto secondario che conterrà il plug-in e selezionare un'icona.

9.  Salvare il pacchetto nella cartella contenuto nel server.

    **Nota**  Per facilitare la gestione dei pacchetti secondari, è consigliabile che il nome del pacchetto includa il termine "pacchetto secondario" per sottolineare che si tratta di un pacchetto che non funzionerà come applicazione autonoma, ad esempio **\ [plug in Name \] pacchetto secondario**.

     

**Per creare un pacchetto secondario per middleware usando la composizione della famiglia di prodotti dinamici**

1.  In un computer di sequenziazione configurato con un'immagine pulita, installare Application Virtualization Sequencer e salvare lo stato del computer.

2.  Installare il middleware localmente nel computer di sequenziazione e configurarlo.

3.  Sequenziare l'applicazione principale e salvare il pacchetto nella cartella contenuto nel server.

4.  Ripristinare il computer di sequenziazione nello stato salvato dal passaggio 1.

5.  Avviare il sequencer per creare un nuovo pacchetto.

6.  Avviare la fase di monitoraggio del sequencer.

7.  Installare l'applicazione middleware nel computer di sequenziazione e configurarla come in un'installazione tipica.

8.  Completare il processo di sequenziazione.

9.  Salvare il pacchetto nella cartella contenuto nel server.

    **Nota**  Per facilitare la gestione dei pacchetti secondari, è consigliabile che il nome del pacchetto includa il termine "pacchetto secondario" per sottolineare che si tratta di un pacchetto che non funzionerà come applicazione autonoma, ad esempio **\ [middleware Name \] pacchetto secondario**.

     

**Per definire la dipendenza nel pacchetto principale**

1. Nel server aprire il file OSD del pacchetto secondario per la modifica. È consigliabile usare un editor XML per apportare modifiche al file OSD, tuttavia, è possibile usare il blocco note in alternativa.

2. Copiare la riga **codebase href** da tale file.

3. Aprire il file OSD del pacchetto principale per la modifica.

4. Inserire il <strong> &lt; tag dipendenze &gt; </strong> dopo la chiusura del tag ** &lt; /ENVLIST &gt; ** alla fine della sezione ** &lt; virtualenv &gt; ** appena prima del tag ** &lt; /virtualenv &gt; ** .

5. Incollare la riga **codebase href** dal pacchetto secondario dopo il tag ** &lt; &gt; dipendenze** appena creato.

6. Se il pacchetto secondario è un pacchetto obbligatorio, il che significa che deve essere avviato prima dell'avvio del pacchetto principale, aggiungere la proprietà **obbligatorio = "true"** all'interno del tag **codebase** . Se non è obbligatorio, la proprietà può essere omessa.

7. Chiudere il tag ** &lt; Dipendenze &gt; ** inserendo i seguenti elementi:

   **&lt;/DEPENDENCIES&gt;**

8. Esaminare le modifiche apportate al file OSD e quindi salvare e chiudere il file. L'esempio seguente mostra il modo in cui deve essere visualizzata la sezione aggiunta. I valori di tag riportati di seguito sono ad esempio solo.

   **&lt;VIRTUALENV&gt;**

        **&lt;ENVLIST&gt;**

   **…**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **&lt;/VIRTUALENV&gt;**

9. Se il pacchetto secondario contiene voci nella sezione ** &lt; ENVLIST &gt; ** del file OSD, è necessario copiare le voci nella stessa sezione del pacchetto principale.

## Argomenti correlati


[Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





