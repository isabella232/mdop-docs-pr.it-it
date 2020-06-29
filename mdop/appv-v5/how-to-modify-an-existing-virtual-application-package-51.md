---
title: Come modificare un pacchetto applicazione virtuale esistente
description: Come modificare un pacchetto applicazione virtuale esistente
author: dansimp
ms.assetid: 6cdeec00-e4fe-4210-b4c7-6ca1ac643ddd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 95963610c8b725412f6d516ee22b1c2f4e186df6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805296"
---
# Come modificare un pacchetto applicazione virtuale esistente


Questo argomento illustra come:

-   [Aggiornare un'applicazione in un pacchetto di applicazione virtuale esistente](#bkmk-update-app-in-pkg)

-   [Modificare le proprietà associate a un pacchetto di applicazione virtuale esistente](#bkmk-chg-props-in-pkg)

-   [Aggiungere una nuova applicazione a un pacchetto di applicazione virtuale esistente](#bkmk-add-app-to-pkg)

**Prima di aggiornare un pacchetto:**

-   Verificare di aver installato Microsoft Application Virtualization (App-V) Sequencer, che è necessario per la modifica di un pacchetto di applicazione virtuale. Per installare l'App-V Sequencer, vedere [come installare il sequencer](how-to-install-the-sequencer-51beta-gb18030.md).

-   Salvare il file con estensione appv in un percorso sicuro e considerare sempre attendibile l'origine prima di provare ad aprire il pacchetto per la modifica.

-   La sezione Gestione autorità viene erroneamente rimossa dal file di configurazione della distribuzione quando si aggiorna un pacchetto. Prima di avviare l'aggiornamento, copiare la sezione autorità di gestione dal file di configurazione della distribuzione esistente e quindi incollare la sezione copiata nel nuovo file di configurazione al termine della conversione.

-   Se si fa clic su **modifica un pacchetto di applicazione virtuale esistente** nel sequencer per modificare un pacchetto, ma non apportare modifiche e chiudere il pacchetto, il comportamento di flusso del pacchetto viene modificato. Il blocco di funzionalità principale viene rimosso dal file StreamMap.xml e tutti i file elencati nel blocco di funzionalità di pubblicazione vengono rimossi. Gli utenti che ricevono il pacchetto modificato usano il pacchetto come se fosse un errore di flusso, indipendentemente dal modo in cui è stato configurato il pacchetto originale.

<a href="" id="bkmk-update-app-in-pkg"></a>**Aggiornare un'applicazione in un pacchetto di applicazione virtuale esistente**

1.  Nel computer che esegue il Sequencer fare clic su **tutti i programmi**, scegliere **virtualizzazione applicazioni Microsoft**e quindi fare clic su **Microsoft Application Virtualization Sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente** &gt; **Next**.

3.  Nella pagina **Seleziona attività** fare clic su **Aggiorna applicazione nel pacchetto esistente** &gt; **successivo**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale che contiene l'applicazione da aggiornare e quindi fare clic su **Avanti**.

5.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'aggiornamento dell'applicazione o impedire che l'applicazione aggiornata contenga dati non necessari. Risolvere tutti i potenziali problemi prima di continuare. Dopo aver eseguito le correzioni e aver risolto tutti i potenziali problemi, fare clic su **Aggiorna** &gt; **Avanti**.

    **Importante**  Se è necessario disabilitare il software antivirus, analizzare prima di tutto il computer in cui viene eseguito il sequencer per assicurarsi che non vengano aggiunti file non desiderati o malevoli al pacchetto.

6.  Nella pagina **selezionare il programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione di aggiornamento per l'applicazione. Se l'aggiornamento non ha un file di programma di installazione associato e se si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

7.  Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione dell'aggiornamento dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**e quindi individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**. Fai clic su **Avanti**.

    **Nota**  Il sequencer monitora tutte le modifiche e le installazioni che si verificano nel computer che esegue il sequencer. Sono incluse tutte le modifiche e le installazioni eseguite all'esterno della procedura guidata di sequenziazione.

8.  Nella pagina del **report di installazione** è possibile esaminare le informazioni sull'applicazione virtuale aggiornata. In **altre informazioni**, fare doppio clic sull'evento per ottenere informazioni più dettagliate. Per continuare, fare clic su **Avanti**.

9.  Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per l'esecuzione di tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

    **Nota**  È possibile interrompere il caricamento di un'applicazione durante questo passaggio. Nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi**e quindi selezionare **Interrompi tutte le applicazioni** o **Interrompi solo l'applicazione**.   

10. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare la casella di controllo per **continuare a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti**. Quando si seleziona questa opzione, il pacchetto si apre nella console App-V Sequencer, in cui è possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

    Per salvare immediatamente il pacchetto, selezionare l'opzione **Salva il pacchetto in questo momento**. Aggiungere **Commenti** facoltativi da associare al pacchetto. I commenti sono utili per identificare la versione dell'applicazione e per specificare altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Fai clic su **Crea**.

11. Nella pagina **completamento** fare clic su **Chiudi** per chiudere la procedura guidata. Il pacchetto è ora disponibile nel sequencer.

<a href="" id="bkmk-chg-props-in-pkg"></a>**Modificare le proprietà associate a un pacchetto di applicazione virtuale esistente**

1.  Nel computer che esegue il Sequencer fare clic su **tutti i programmi**, scegliere **virtualizzazione applicazioni Microsoft**e quindi fare clic su **Microsoft Application Virtualization Sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente** &gt; **Next**.

3.  Nella pagina **Seleziona attività** fare clic su **modifica pacchetto** &gt; **successivo**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale che contiene le proprietà dell'applicazione da modificare e quindi fare clic su **modifica**.

5.  Nella console App-V Sequencer eseguire una delle attività seguenti in base alle esigenze:

    -   Importare ed esportare il file manifesto.

    -   Abilitare o disabilitare gli oggetti helper del browser.

    -   Importare o esportare un file VFS.

    -   Importare una directory nel file system virtuale.

    -   Importare ed esportare le chiavi del registro di sistema virtuali.

    -   Visualizzare le proprietà del pacchetto.

    -   Visualizzare i file di pacchetto associati.

    -   Modificare le impostazioni del registro di sistema.

    -   Rivedere le impostazioni aggiuntive del pacchetto (ad eccezione delle proprietà del file di sistema operativo).

    -   Impostare lo stato della chiave del registro di sistema virtualizzato (override o merge).

    -   Impostare lo stato della cartella virtualizzata.

    -   Aggiungere o modificare collegamenti e associazioni di tipi di file.

        **Nota**  Per modificare le associazioni o i tipi di file, è prima di tutto necessario aprire il pacchetto per l'aggiornamento per aggiungere una nuova applicazione e quindi passare alla pagina di modifica finale.

6.  Al termine della modifica delle proprietà del pacchetto, **File** fare clic su &gt; **Salva** file per salvare il pacchetto.

<a href="" id="bkmk-add-app-to-pkg"></a>**Aggiungere una nuova applicazione a un pacchetto di applicazione virtuale esistente**

1.  Nel computer che esegue il Sequencer fare clic su **tutti i programmi**, scegliere **virtualizzazione applicazioni Microsoft**e quindi fare clic su **Microsoft Application Virtualization Sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente** &gt; **Next**.

3.  Nella pagina **Seleziona attività** fare clic su **Aggiungi nuova applicazione** &gt; **Avanti**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale a cui si vuole aggiungere l'applicazione e quindi fare clic su **Avanti**.

5.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o impedire che il pacchetto modificato contenga dati non necessari. Risolvere tutti i potenziali problemi prima di continuare. Dopo aver eseguito le correzioni e aver risolto tutti i potenziali problemi, fare clic su **Aggiorna** &gt; **Avanti**.

    **Importante**  Se è necessario disabilitare il software antivirus, analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.

6.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

7.  Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, installare l'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**e individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare l' **installazione** &gt; **successiva**. Nella finestra **di dialogo Sfoglia per la cartella** specificare la directory principale in cui verrà installata l'applicazione. Assicurarsi che si tratta di una nuova posizione in modo da non sovrascrivere la versione esistente del pacchetto di applicazione virtuale.

    **Nota**  Il sequencer monitora tutte le modifiche e le installazioni che si verificano nel computer che esegue il sequencer. Sono incluse tutte le modifiche e le installazioni eseguite all'esterno della procedura guidata di sequenziazione.

8.  Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto. Questo passaggio completa tutte le attività di licenza o configurazione associate necessarie per eseguire l'applicazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi che si desidera eseguire e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Per l'esecuzione di tutti i programmi, possono essere necessarie diversi minuti. Fai clic su **Avanti**.

9.  Nella pagina del **report di installazione** è possibile esaminare le informazioni sull'applicazione virtuale aggiornata. In **altre informazioni**, fare doppio clic sull'evento per ottenere informazioni più dettagliate e quindi fare clic su **Avanti** per aprire la pagina **Personalizza** .

10. Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 13 della procedura. Se si vuole eseguire la personalizzazione descritta di seguito, fare clic su **Personalizza**.

    Se si sta personalizzando, preparare il pacchetto virtuale per lo streaming e quindi fare clic su **Avanti**. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.

11. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

    **Nota**  È possibile interrompere il caricamento di un'applicazione durante questo passaggio. Nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e quindi selezionare **Interrompi tutte le applicazioni** o **Interrompi solo l'applicazione**.

12. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare la casella di controllo **continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** . Selezionando questa opzione si apre il pacchetto nella console App-V Sequencer, in cui è possibile modificare il pacchetto prima di salvarlo. Fai clic su **Avanti**.

    Per salvare immediatamente il pacchetto, selezionare l'opzione **Salva il pacchetto in questo momento**. Aggiungere **Commenti** facoltativi da associare al pacchetto. I commenti sono utili per fornire versioni delle applicazioni e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Fai clic su **Crea**.

13. Nella pagina **Completamento** fai clic su **Chiudi**. Il pacchetto è ora disponibile nel sequencer.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





