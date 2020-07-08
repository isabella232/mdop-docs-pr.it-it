---
title: Come sequenziare una nuova applicazione middleware (App-V 4.6 SP1)
description: Come sequenziare una nuova applicazione middleware (App-V 4.6 SP1)
author: dansimp
ms.assetid: 304045c2-5e5e-4c91-b59e-a91fdf2500fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b26559b8f5c451d01fefe899e96a83dd388b8140
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816675"
---
# Come sequenziare una nuova applicazione middleware (App-V 4.6 SP1)


Usare la procedura seguente per creare un nuovo pacchetto di applicazioni virtuali middleware usando l'Application Virtualization (App-V) Sequencer. Un'applicazione middleware è un software che connette moduli software o applicazioni. Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

Usa questo tipo di pacchetto usando la composizione Dynamic Suite in App-V. La composizione della famiglia di prodotti dinamici consente di definire un pacchetto di applicazione virtuale come dipendente da un altro pacchetto di applicazione virtuale. La dipendenza consente all'applicazione di interagire con il middleware o il plug-in nell'ambiente virtuale, dove in genere questa interazione viene impedita. Ciò è utile perché un pacchetto di applicazione secondario può essere usato con diverse altre applicazioni primarie, che consente a ogni applicazione principale di fare riferimento allo stesso pacchetto secondario. Per altre informazioni su come usare la composizione della famiglia di prodotti dinamici, vedere [come usare la composizione di suite dinamiche](https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) nella raccolta tecnica Microsoft ( https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) .

**Importante**  
Durante la sequenziazione, se il computer che gestisce l'App-V Sequencer è in uso in Windows Vista o Windows 7 e viene avviato un riavvio all'esterno dell'ambiente virtuale, ad esempio, **Start**  /  **Shut Down**, è necessario fare clic su **Annulla** quando viene richiesto di chiudere il programma impedendo l'arresto di Windows. Se si fa clic su **forza chiusa**, la creazione del pacchetto non riesce. Quando si fa clic su **Annulla**, l'App-V Sequencer registra correttamente il riavvio durante la sequenziazione dell'applicazione.



**Per sequenziare una nuova applicazione middleware**

1.  Per avviare App-v sequencer, nel computer in cui è in uso App-v Sequencer fare clic su **Avvia**  /  **tutti i programmi**Microsoft Application Virtualization  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per avviare la **procedura guidata Crea nuovo pacchetto**, fai clic su **Crea un nuovo pacchetto di applicazione virtuale**. Per creare il pacchetto, selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o il pacchetto per contenere dati non necessari. Ti consigliamo vivamente di risolvere tutti i potenziali problemi prima di continuare. Dopo aver risolto i conflitti, per aggiornare le informazioni visualizzate, fare clic su **Aggiorna**. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  
    Se è necessario disabilitare il software per la ricerca di virus, è necessario analizzare il computer che esegue l'App-V Sequencer per assicurarsi che non sia possibile aggiungere file indesiderati o malintenzionati al pacchetto.



4.  Nella pagina **tipo di applicazione** selezionare **middleware**e quindi fare clic su **Avanti**.

    Per altre informazioni sui tipi di applicazioni che è possibile sequenziare, vedere [come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

6.  Nella pagina **nome pacchetto** specificare un nome che verrà associato al pacchetto. Il nome aiuta ad identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto. Il nome del pacchetto viene visualizzato anche in App-V Management Console. Nel percorso di **installazione** viene visualizzato il percorso di virtualizzazione dell'applicazione in cui verrà installata l'applicazione. Per modificare questa posizione, selezionare **modifica (avanzate)**.

    **Importante**  
    La modifica del percorso di virtualizzazione dell'applicazione è un'attività di configurazione avanzata. Dovresti comprendere appieno le implicazioni della modifica del percorso. Per la maggior parte delle applicazioni, è consigliabile il percorso predefinito.



~~~
Click **Next**.
~~~

7. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione middleware sono pronti, installare l'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Eseguire l'installazione usando il processo di installazione dell'applicazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**per individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare la casella di controllo **ho terminato l'installazione** e quindi fare clic su **Avanti**.

8. Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazione virtuale.

9. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

10. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** . Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire il pacchetto. Fai clic su **Avanti**.

11. Nella pagina **Crea pacchetto** , per modificare il pacchetto senza salvarlo, selezionare la casella di controllo **continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** . Selezionando questa opzione si apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

   Per salvare immediatamente il pacchetto, selezionare la casella di controllo **Salva il pacchetto ora** . Aggiungere commenti facoltativi nella casella **Commenti** che verranno associati al pacchetto. I commenti sono utili per identificare la versione e altre informazioni sul pacchetto. Verrà visualizzata anche la **posizione di salvataggio** predefinita. Per cambiare il percorso predefinito, fare clic su **Sfoglia**e quindi specificare la nuova posizione. Viene visualizzata la dimensione del pacchetto non compresso. Se le dimensioni del pacchetto superano i 4 GB (non compressi) e si prevede di eseguire lo streaming del pacchetto in computer di destinazione, è necessario selezionare **Comprimi pacchetto**. Fai clic su **Crea**.

12. Nella pagina **completamento** , dopo aver esaminato le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** , fare clic su **Chiudi**. Le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** sono disponibili anche nella directory specificata nel passaggio 11 di questa procedura, in un file denominato **Report.xml**.

   Il pacchetto è ora disponibile nel sequencer. Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**. Per altre informazioni sulla modifica di un pacchetto, vedere [come modificare un pacchetto di applicazione virtuale esistente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

   **Importante**  
   Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









