---
title: Come sequenziare un nuovo componente aggiuntivo o applicazione plug-in (App-V 4.6 SP1)
description: Come sequenziare un nuovo componente aggiuntivo o applicazione plug-in (App-V 4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816706"
---
# Come sequenziare un nuovo componente aggiuntivo o applicazione plug-in (App-V 4.6 SP1)


Usare la procedura seguente per creare un nuovo pacchetto di applicazione virtuale o plug-in aggiuntivo tramite Application Virtualization (App-V) Sequencer. Un'applicazione per il componente aggiuntivo o plug-in è un'applicazione che estende la funzionalità di un'applicazione, ad esempio un plug-in per Microsoft Excel. Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

**Importante**  
Prima di eseguire la procedura seguente, installare l'applicazione padre localmente nel computer in cui è in esecuzione Sequencer. Ad esempio, se si esegue la sequenziazione di un plug-in per Microsoft Excel, installare Microsoft Excel localmente nel computer in cui è in corso il sequencer. Installare inoltre l'applicazione padre nella stessa directory in cui è installata l'applicazione nei computer di destinazione. Se il plug-in o il componente aggiuntivo verrà usato con un pacchetto di applicazione virtuale esistente, installare l'applicazione nella stessa unità di applicazione virtuale usata quando è stato creato il pacchetto dell'applicazione virtuale padre.



Puoi anche usare un pacchetto di applicazione virtuale esistente come applicazione padre. Per usare un pacchetto di applicazione virtuale esistente, eseguire la procedura seguente prima di sequenziare il nuovo componente aggiuntivo o plug-in.

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per espandere un pacchetto esistente nel computer in cui è in uso il sequencer, fare clic su **strumenti**  /  **Espandi pacchetto nel sistema locale**.

3.  Individuare e selezionare il pacchetto (file con**estensione SPRJ** ) che si desidera espandere e quindi fare clic su **Apri**. Continuare con la procedura seguente.

**Per sequenziare una nuova applicazione per il componente aggiuntivo o il plug-in**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per avviare la **procedura guidata Crea nuovo pacchetto**, fai clic su **Crea un nuovo pacchetto di applicazione virtuale**. Per creare il pacchetto, selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o il pacchetto per contenere dati non necessari. Ti consigliamo vivamente di risolvere tutti i potenziali problemi prima di continuare. Dopo aver risolto i conflitti, per aggiornare le informazioni visualizzate, fare clic su **Aggiorna**. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  
    Se è necessario disabilitare il software per la ricerca di virus, analizzare il computer che esegue il sequencer per assicurarsi che non vengano aggiunti file indesiderati o malevoli al pacchetto.



4.  Nella pagina **tipo di applicazione** selezionare **componente aggiuntivo o plug-in**e quindi fare clic su **Avanti**.

    Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per il componente aggiuntivo o il plug-in. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

6.  Nella pagina **Select Primary** fare clic su **Sfoglia** e specificare l'applicazione padre.

    **Importante**  
    Se l'applicazione padre che il componente aggiuntivo o il plug-in che si sta installando sta per supportare non è stata installata localmente, arrestarsi qui e installare l'applicazione nel computer che esegue il sequencer. Ad esempio, il file di programma **Excel.exe** deve essere installato localmente per un plug-in di Microsoft Excel.



~~~
Click **Next**.
~~~

7. Nella pagina **nome pacchetto** specificare un nome che verrà associato al pacchetto. Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto. Il nome del pacchetto verrà visualizzato anche in App-V Management Console. Nel percorso di **installazione** viene visualizzato il percorso di virtualizzazione dell'applicazione in cui verrà installata l'applicazione. Per modificare questa posizione, selezionare **modifica (avanzate)**.

   **Importante**  
   La modifica del percorso di virtualizzazione dell'applicazione è un'attività di configurazione avanzata. Dovresti comprendere appieno le implicazioni della modifica del percorso. Per la maggior parte delle applicazioni, è consigliabile il percorso predefinito.



~~~
Click **Next**.
~~~

8. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, installa il plug-in o l'applicazione del componente aggiuntivo in modo che il Sequencer possa monitorare il processo di installazione. Eseguire l'installazione usando il processo di installazione dell'applicazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** e individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**e quindi fare clic su **Avanti**.

9. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

10. Nella pagina **Personalizza** , se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 14 di questa procedura. Se si vuole personalizzare qualsiasi elemento dell'elenco seguente, selezionare **Personalizza**.

    -   Modificare le associazioni di tipi di file associate a un'applicazione.

    -   Preparare il pacchetto virtuale per lo streaming. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.

    -   Specifica i sistemi operativi che possono eseguire questo pacchetto.

    Fai clic su **Avanti**.

11. Nella pagina **Modifica collegamenti** è possibile configurare facoltativamente le associazioni di tipi di file (FTA) che verranno associate alle varie applicazioni nel pacchetto. Per creare un nuovo FTA, nel riquadro sinistro selezionare ed espandere l'applicazione che si vuole personalizzare e quindi fare clic su **Aggiungi**. Nella finestra di dialogo **Aggiungi associazione tipo di file** fornisci le informazioni necessarie per il nuovo FTA. In applicazione selezionare **scelte rapide** per rivedere le informazioni di collegamento associate a un'applicazione. Nel riquadro **posizione** è possibile esaminare le informazioni sul file dell'icona. Per modificare un FTA esistente, fare clic su **modifica**. Per rimuovere un FTA, selezionare la FTA e quindi fare clic su **Rimuovi**. Fai clic su **Avanti**.

12. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

   **Nota**  
   Se si vuole interrompere il caricamento di un'applicazione durante questo passaggio, nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e selezionare una delle caselle di controllo, **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**.



13. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** . Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e quindi selezionare i sistemi operativi che possono eseguire il pacchetto. Fai clic su **Avanti**.

14. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare la casella di controllo **continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** . Selezionando questa opzione si apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

   Per salvare immediatamente il pacchetto, selezionare l'opzione **Salva il pacchetto in questo momento**. Facoltativamente, selezionare **Commenti** per aggiungere commenti che verranno associati al pacchetto. I commenti sono utili per identificare la versione e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Se le dimensioni del pacchetto superano i 4 GB (non compressi) e si prevede di eseguire lo streaming del pacchetto in computer di destinazione, è necessario selezionare **Comprimi pacchetto**. Fai clic su **Crea**.

15. Nella pagina **completamento** , dopo aver esaminato le informazioni visualizzate nel riquadro **report pacchetto di applicazione virtuale riuscito** , fare clic su **Chiudi**. Le informazioni visualizzate nel riquadro **report pacchetto di applicazione virtuale riuscito** sono disponibili anche nella directory specificata nel passaggio 14 di questa procedura, in un file denominato **Reports.xml**.

   Il pacchetto è ora disponibile nel sequencer. Fare clic su **modifica \ [nome pacchetto \]** per modificare le proprietà del pacchetto. Per altre informazioni sulla modifica di un pacchetto, vedere [come modificare un pacchetto di applicazione virtuale esistente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

   **Importante**  
   Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









