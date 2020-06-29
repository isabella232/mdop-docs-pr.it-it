---
title: Come modificare un pacchetto applicazione virtuale esistente (App-V 4.6 SP1)
description: Come modificare un pacchetto applicazione virtuale esistente (App-V 4.6 SP1)
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817036"
---
# Come modificare un pacchetto applicazione virtuale esistente (App-V 4.6 SP1)


Usare le procedure seguenti per modificare un pacchetto di applicazione virtuale esistente. È possibile usare queste procedure per:

-   Aggiornare un'applicazione che fa parte di un pacchetto di applicazione virtuale esistente. Per eseguire questa attività, usare la procedura **"per aggiornare un'applicazione in un pacchetto di applicazione esistente"** in questo documento.

-   Modificare le proprietà associate a un pacchetto di applicazione virtuale esistente. Per eseguire questa attività, usare la procedura **"per modificare le proprietà associate a un pacchetto di applicazione virtuale esistente"** in questo documento.

-   Aggiungere una nuova applicazione a un pacchetto di applicazione virtuale esistente. Per eseguire questa attività, usare la procedura **"per aggiungere una nuova applicazione a un pacchetto di applicazione virtuale esistente"** in questo documento.

Per modificare un pacchetto di applicazione virtuale, è necessario che l'App-V Sequencer sia installata. Per altre informazioni sull'installazione di App-V Sequencer, vedere [come installare Sequencer (app-v 4,6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).

**Per aggiornare un'applicazione in un pacchetto di applicazione virtuale esistente**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente**e quindi su **Avanti**.

3.  Nella pagina **Seleziona attività** fare clic su **Aggiorna applicazione nel pacchetto esistente**e quindi fare clic su **Avanti**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale che contiene l'applicazione che si vuole aggiornare e quindi fare clic su **Avanti**.

5.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare un errore dell'applicazione o l'aggiornamento dell'applicazione per contenere dati non necessari. Ti consigliamo vivamente di risolvere tutti i potenziali problemi prima di continuare. Dopo aver risolto i conflitti, per aggiornare le informazioni visualizzate, fare clic su **Aggiorna**. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  Se è necessario disabilitare il software antivirus, analizzare il computer che esegue il sequencer per assicurarsi che non vengano aggiunti file non desiderati o malevoli al pacchetto.

     

6.  Nella pagina **selezionare il programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione di aggiornamento per l'applicazione. Se l'aggiornamento non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

7.  Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, installare l'aggiornamento dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** e individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**. Fai clic su **Avanti**.

    **Nota**  Il sequencer monitora tutte le modifiche e le installazioni nel computer che esegue il sequencer, incluse le modifiche e le installazioni eseguite all'esterno della sequenziazione guidata.

     

8.  Nella pagina del **report di installazione** è possibile esaminare le informazioni sull'applicazione virtuale appena aggiornata. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

9.  Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

    **Nota**  Se si vuole interrompere il caricamento di un'applicazione durante questo passaggio, nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi**e quindi fare clic su una delle opzioni seguenti, **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**, a seconda di cosa si vuole.

     

10. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare la casella di controllo **continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** . Quando si seleziona questa opzione, il pacchetto nella console del sequencer si apre in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

    Per salvare immediatamente il pacchetto, selezionare l'opzione **Salva il pacchetto in questo momento**. Aggiungere **Commenti** facoltativi che verranno associati al pacchetto. I commenti sono utili per identificare la versione e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Se le dimensioni del pacchetto superano i 4 GB (non compressi) e si prevede di eseguire lo streaming del pacchetto in computer di destinazione, è necessario selezionare **Comprimi pacchetto**e quindi fare clic su **Crea**.

11. Nella pagina **completamento** fare clic su **Chiudi** per chiudere la procedura guidata. Il pacchetto è ora disponibile nel sequencer.

**Per modificare le proprietà associate a un pacchetto di applicazione virtuale esistente**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente**e quindi su **Avanti**.

3.  Nella pagina **Seleziona attività** fare clic su **modifica pacchetto**e quindi su **Avanti**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale che contiene le proprietà dell'applicazione che si desidera modificare e quindi fare clic su **modifica**.

5.  Nella console sequencer è possibile eseguire una delle attività seguenti:

    -   Visualizzare le proprietà del pacchetto.

    -   Visualizzare la cronologia delle modifiche del pacchetto.

    -   Visualizzare i file di pacchetto associati.

    -   Modificare le impostazioni del registro di sistema.

    -   Rivedere le impostazioni aggiuntive del pacchetto (ad eccezione delle proprietà del file di sistema operativo).

    -   Creare un Windows Installer (MSI) associato.

    -   Modificare il file OSD.

    -   Comprimere e decomprimere il pacchetto.

    -   Aggiungere associazioni di tipi di file.

    -   Impostare lo stato della chiave del registro di sistema virtualizzato (override o merge).

    -   Impostare lo stato della cartella virtualizzata.

    -   Modificare i mapping di file system virtuali.

6.  Dopo aver completato la modifica delle proprietà del pacchetto, **File**fare clic su  /  **Salva** file per salvare il pacchetto.

**Per aggiungere una nuova applicazione a un pacchetto di applicazione virtuale esistente**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Nell'App-V Sequencer fare clic su **modifica un pacchetto di applicazione virtuale esistente**e quindi su **Avanti**.

3.  Nella pagina **Seleziona attività** fare clic su **Aggiungi nuova applicazione**e quindi su **Avanti**.

4.  Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** per individuare il pacchetto di applicazione virtuale a cui si vuole aggiungere l'applicazione e quindi fare clic su **Avanti**.

5.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto oppure per l'aggiornamento che contenga dati non necessari. Ti consigliamo vivamente di risolvere tutti i potenziali problemi prima di continuare. Dopo aver risolto i conflitti, per aggiornare le informazioni visualizzate, fare clic su **Aggiorna**. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  Se è necessario disabilitare il software per la ricerca di virus, analizzare il computer che esegue il sequencer per assicurarsi che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.

     

6.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

7.  Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, installare l'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**e individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**. Fai clic su **Avanti**. Nella finestra **di dialogo Sfoglia per la cartella** specificare la directory principale in cui verrà installata l'applicazione. Dovrebbe essere una nuova posizione in modo da non sovrascrivere la versione esistente del pacchetto di applicazione virtuale.

    **Nota**  Tutte le modifiche e le installazioni al computer che esegue il sequencer vengono monitorate dal sequencer, incluse le modifiche e le installazioni eseguite all'esterno della sequenziazione guidata.

     

8.  Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto. Questo passaggio consente di completare tutte le attività di licenza o configurazione associate necessarie per eseguire l'applicazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi che si desidera eseguire e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Per l'esecuzione di tutti i programmi, possono essere necessarie diversi minuti. Fai clic su **Avanti**.

9.  Nella pagina del **report di installazione** è possibile esaminare le informazioni sull'applicazione virtuale appena aggiornata. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

10. Nella pagina **Personalizza** , se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 14 di questa procedura. Se si vuole personalizzare qualsiasi elemento dell'elenco seguente, fare clic su **Personalizza**.

    -   Modificare le associazioni di tipi di file associate a un'applicazione.

    -   Preparare il pacchetto virtuale per lo streaming. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.

    Fai clic su **Avanti**.

11. Nella pagina **Modifica collegamenti** è possibile configurare facoltativamente le associazioni di tipi di file (FTA) che verranno associate alle varie applicazioni nel pacchetto. Per creare un nuovo FTA, selezionare ed espandere l'applicazione che si desidera personalizzare nel riquadro sinistro e quindi fare clic su **Aggiungi**. Nella finestra di dialogo **Aggiungi associazione tipo di file** fornisci le informazioni necessarie per il nuovo FTA. Per rivedere le informazioni di collegamento associate a un'applicazione, in applicazione selezionare la casella di controllo **collegamenti** e nel riquadro **posizione** è possibile esaminare le informazioni sul file dell'icona. Per modificare un FTA esistente, fare clic su **modifica**. Per rimuovere un FTA, selezionare la FTA e quindi fare clic su **Rimuovi**. Fai clic su **Avanti**.

12. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

    **Nota**  Se si vuole interrompere il caricamento di un'applicazione durante questo passaggio, nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e selezionare la casella di controllo **Interrompi tutte le applicazioni** o **arresta solo l'applicazione** , a seconda di cosa si vuole.

     

13. Nella pagina **Crea pacchetto** selezionare la casella di controllo **continua a modificare il pacchetto senza salvare con l'editor di pacchetti** , per modificare il pacchetto senza salvarlo. Quando si seleziona questa opzione, il pacchetto nella console del sequencer si apre in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

    Selezionare l'impostazione predefinita **Salva il pacchetto ora**, per salvare il pacchetto immediatamente. Aggiungere **Commenti** facoltativi che verranno associati al pacchetto. I commenti sono utili per identificare la versione e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Se le dimensioni del pacchetto superano i 4 GB (non compressi) e si prevede di eseguire lo streaming del pacchetto in computer di destinazione, è necessario selezionare **Comprimi pacchetto**. Fai clic su **Crea**.

14. Nella pagina **Completamento** fai clic su **Chiudi**. Il pacchetto è ora disponibile nel sequencer.

## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





