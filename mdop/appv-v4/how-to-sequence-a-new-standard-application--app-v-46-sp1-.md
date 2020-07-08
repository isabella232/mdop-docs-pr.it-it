---
title: Come sequenziare una nuova applicazione standard (App-V 4.6 SP1)
description: Come sequenziare una nuova applicazione standard (App-V 4.6 SP1)
author: dansimp
ms.assetid: c4a2eb33-def8-4535-b93a-3d2de21ce29f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47c93b4880d0095c87a98292fda743acc1659e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816665"
---
# Come sequenziare una nuova applicazione standard (App-V 4.6 SP1)


Usare la procedura seguente per creare un nuovo pacchetto di applicazione virtuale standard usando l'Application Virtualization (App-V) Sequencer. Questa procedura si applica alla maggior parte delle applicazioni sequenziate. Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md). È necessario eseguire sequencer (**SFTSequencer.exe**) usando un account che disponga dei privilegi di amministratore a causa delle modifiche apportate dal sequencer al sistema locale. Queste modifiche possono includere la scrittura di file nella directory **C:\\Programmi files** , le modifiche del registro di sistema, l'avvio e l'arresto dei servizi, l'aggiornamento dei descrittori di sicurezza per i file e la modifica delle autorizzazioni.

**Importante**  
Durante la sequenziazione, se il computer che ha eseguito il sequencer è in uso in Windows Vista o Windows 7 e viene avviato un riavvio all'esterno dell'ambiente virtuale, ad esempio, **Start**  /  **Shut Down**, è necessario fare clic su **Annulla** quando viene richiesto di chiudere il programma impedendo l'arresto di Windows Vista o Windows. Se si fa clic su **forza chiusa**, la creazione del pacchetto non riesce. Quando si fa clic su **Annulla**, il sequencer registra correttamente il riavvio durante la sequenziazione dell'applicazione.



**Nota**  
L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.



**Per sequenziare una nuova applicazione standard**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per avviare la **procedura guidata Crea nuovo pacchetto**, fai clic su **Crea un nuovo pacchetto di applicazione virtuale**. Per creare il pacchetto, selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o il pacchetto per contenere dati non necessari. Ti consigliamo vivamente di risolvere tutti i potenziali problemi prima di continuare. Dopo aver risolto i conflitti, per aggiornare le informazioni visualizzate, fare clic su **Aggiorna**. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  
    Se è necessario disabilitare il software per la ricerca di virus, analizzare il computer che esegue il sequencer per assicurarsi che non vengano aggiunti file indesiderati o malevoli al pacchetto.



4.  Nella pagina **tipo di applicazione** fare clic sulla casella di controllo **applicazione standard (impostazione predefinita)** e quindi fare clic su **Avanti**.

    Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella di controllo **Esegui un'installazione personalizzata** e quindi fare clic su **Avanti**.

6.  Nella pagina **nome pacchetto** specificare un nome che verrà associato al pacchetto. Il nome aiuta a identificare lo scopo e la versione dell'applicazione aggiunti al pacchetto. Il nome del pacchetto viene visualizzato anche in App-V Management Console. Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso di virtualizzazione dell'applicazione in cui l'applicazione verrà installata nei computer di destinazione. Per modificare questa posizione, selezionare **modifica (avanzate)**.

    **Importante**  
    La modifica del percorso di virtualizzazione dell'applicazione è un'attività di configurazione avanzata. Dovresti comprendere appieno le implicazioni della modifica del percorso. Per la maggior parte delle applicazioni, è consigliabile il percorso predefinito.



~~~
Click **Next**.
~~~

7. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, installare l'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Eseguire l'installazione usando il processo di installazione dell'applicazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** per individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**. Fai clic su **Avanti**.

8. Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazione virtuale.

9. Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto. Questo passaggio consente di completare tutte le attività di licenza o configurazione associate necessarie per eseguire l'applicazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi che si desidera eseguire e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Per l'esecuzione di tutti i programmi, possono essere necessarie diversi minuti. Fai clic su **Avanti**.

10. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

11. Nella pagina **Personalizza** , se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 15 di questa procedura. Se si vuole personalizzare qualsiasi elemento dell'elenco seguente, selezionare **Personalizza**.

    -   Modificare le associazioni di tipi di file e le icone associate a un'applicazione.

    -   Preparare il pacchetto virtuale per lo streaming. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.

    -   Specifica i sistemi operativi che possono eseguire questo pacchetto.

    Fai clic su **Avanti**.

12. Nella pagina **modifica tasti** di scelta rapida è possibile configurare le associazioni di tipi di file (FTA) e i percorsi di collegamento che verranno associati alle varie applicazioni nel pacchetto. Per creare un nuovo FTA, nel riquadro sinistro selezionare ed espandere l'applicazione che si vuole personalizzare e quindi fare clic su **Aggiungi**. Nella finestra di dialogo **Aggiungi associazione tipo di file** fornisci le informazioni necessarie per il nuovo FTA. Per rivedere le informazioni di collegamento associate a un'applicazione, in applicazione selezionare **scelte rapide**e quindi nel riquadro **posizione** è possibile modificare le informazioni sul file dell'icona. Per modificare un FTA esistente, fare clic su **modifica**. Per rimuovere un FTA, selezionare la FTA e quindi fare clic su **Rimuovi**. Fai clic su **Avanti**.

13. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

   **Nota**  
   Se si vuole interrompere il caricamento di un'applicazione durante questo passaggio, nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi**e selezionare una delle caselle di controllo, **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**, a seconda di cosa si vuole.



14. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare **Consenti il pacchetto per l'esecuzione in qualsiasi sistema operativo**. Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare **Consenti questo pacchetto per l'esecuzione solo nei sistemi operativi seguenti** e specificare i sistemi operativi che possono eseguire questo pacchetto. Fai clic su **Avanti**.

   **Importante**  
   I sistemi operativi specificati durante questo passaggio riflettono i sistemi operativi nei computer di destinazione abilitati per l'esecuzione del pacchetto. Devi verificare che i sistemi operativi specificati siano supportati dall'applicazione che stai sequenziando.



15. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**. Selezionando questa opzione si apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

   Per salvare immediatamente il pacchetto, selezionare l'opzione **Salva il pacchetto in questo momento**. Aggiungere **Commenti** facoltativi che verranno associati al pacchetto. I commenti sono utili per identificare la versione e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia** e specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Se le dimensioni del pacchetto superano i 4 GB (non compressi) e si prevede di eseguire lo streaming del pacchetto in computer di destinazione, è necessario selezionare **Comprimi pacchetto**. Fai clic su **Crea**.

16. Nella pagina **completamento** , dopo aver esaminato le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** , fare clic su **Chiudi**. Le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** sono disponibili anche nella directory specificata nel passaggio 15 di questa procedura, in un file denominato **Report.xml**.

    Il pacchetto è ora disponibile nel sequencer. Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**. Per altre informazioni sulla modifica di un pacchetto, vedere [come modificare un pacchetto di applicazione virtuale esistente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

    **Importante**  
    Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









