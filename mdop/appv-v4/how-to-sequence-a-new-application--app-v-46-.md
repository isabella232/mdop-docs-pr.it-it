---
title: Come sequenziare una nuova applicazione (App-V 4.6)
description: Come sequenziare una nuova applicazione (App-V 4.6)
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816696"
---
# Come sequenziare una nuova applicazione (App-V 4.6)


Usare la procedura seguente per creare una nuova applicazione virtuale usando l'Application Virtualization (App-V) Sequencer. Puoi anche usare l'App-V Sequencer per configurare i file e le configurazioni applicabili a tutti gli utenti e i file e le configurazioni che gli utenti possono personalizzare. Dopo aver correttamente sequenziato l'applicazione, è disponibile nell'App-V Sequencer.

**Importante**  
Durante la sequenziazione, se il computer che sta eseguendo il sequencer sta eseguendo Windows Vista o Windows 7 e viene avviato un riavvio all'esterno dell'ambiente virtuale, ad esempio, facendo clic su **Start**  /  **Shut Down**, è necessario fare clic su **Annulla** quando viene richiesto di chiudere il programma impedendo l'arresto di Windows. Se si fa clic su **forza chiusa**, la creazione del pacchetto non riesce e il computer viene riavviato. Quando si fa clic su **Annulla**, il sequencer registra correttamente il riavvio durante la sequenziazione dell'applicazione.



**Per sequenziare una nuova applicazione**

1.  Per creare l'unità App-V, configura l'unità Q come posizione che può essere usata per salvare i file durante la sequenziazione di un'applicazione. È quindi necessario creare singole directory per ogni applicazione che si prevede di sequenziare nell'unità Q. È possibile creare le cartelle di destinazione dell'applicazione virtuale prima di sequenziare un'applicazione oppure crearle nel passaggio 5 della procedura.

    **Nota**  
    L'unità App-V specificata deve essere accessibile nei computer di destinazione. Se l'unità Q non è accessibile, è possibile scegliere una lettera di unità diversa.



2.  Per avviare la console App-v sequencer, nel computer in cui è in uso l'app-v sequencer selezionare **Avvia**  /  **programmi**  /  **Microsoft**Application Virtualization  /  **sequencer**. Per avviare la sequenziazione guidata, fare clic su **Crea un pacchetto**.

3.  Nella pagina **informazioni pacchetto** specificare il nome del **pacchetto** che verrà assegnato all'applicazione virtuale. Il nome del pacchetto è necessario per la generazione del file di Windows Installer associato. Dovresti anche aggiungere un commento facoltativo che verrà assegnato al pacchetto e che fornisce informazioni dettagliate sull'applicazione virtuale. Per visualizzare la pagina **Opzioni avanzate** , selezionare **Mostra opzioni di monitoraggio avanzato**e quindi fare clic su **Avanti**. in caso contrario, procedere con il passaggio 5.

4.  Nella pagina **Opzioni avanzate** per consentire a Microsoft Update di aggiornare l'applicazione durante la sequenziazione, selezionare **Consenti l'esecuzione di Microsoft Update durante il monitoraggio**. Se si seleziona questa opzione, è possibile installare Microsoft Updates durante la fase di monitoraggio e accettare gli aggiornamenti associati per l'installazione. Per rimappare i file dll (Dynamic Link Library) supportati in modo che usino uno spazio di RAM contiguo, selezionare **rebase dll**. Se si seleziona questa opzione, è possibile risparmiare memoria e migliorare le prestazioni. Molte applicazioni non supportano questa opzione, ma è utile in ambienti con RAM limitata, ad esempio in scenari Terminal Server. Fai clic su **Avanti**.

5.  Nella pagina di **installazione di monitor** , quando si è pronti per installare l'applicazione, fare clic su **Avvia monitoraggio**e quindi nella finestra di dialogo **Cerca nella cartella** specificare la directory nell'unità Q in cui verrà installata l'applicazione. Se non è stata configurata l'unità Q e si è usata una lettera di unità diversa per l'unità di virtualizzazione dell'applicazione, selezionare la lettera dell'unità specificata nel passaggio 1 di questa procedura. Per installare l'applicazione in una cartella che non è stata creata nell'unità di virtualizzazione dell'applicazione, fare clic su **Crea nuova cartella**. Dopo aver specificato la cartella, attendere che il Sequencer configuri il computer per la sequenziazione.

    **Importante**  
    È necessario installare ogni applicazione sequenziata in una directory separata nell'unità dell'applicazione virtuale e il nome della cartella associata non deve contenere più di otto caratteri.



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. Nella pagina **Configura applicazioni** , se necessario, configura i tasti di scelta rapida e le associazioni di tipi di file che verranno associati all'applicazione virtuale. Per aggiungere una nuova associazione o collegamento di tipo file, fare clic su **Aggiungi**e quindi nella finestra di dialogo **Aggiungi applicazione** specificare il nuovo elemento. Per rimuovere un collegamento o un tipo di file di associazione esistente, fare clic su **Rimuovi**. Per modificare un elemento esistente, selezionare l'elemento che si vuole modificare e quindi fare clic su **modifica**. Specificare le configurazioni nella finestra di dialogo **Modifica applicazione** . Fare clic su **Salva**e quindi su **Avanti**.

7. Nella pagina **Avvia applicazioni** , per avviare l'applicazione per verificare che il pacchetto sia stato installato correttamente ed è ottimizzato per lo streaming, selezionare il pacchetto e quindi fare clic su **Avvia**. Questo passaggio è utile per configurare il modo in cui l'applicazione viene eseguita inizialmente su computer di destinazione e per accettare eventuali contratti di licenza associati prima che il pacchetto diventi disponibile per i client App-V. Se sono associate più applicazioni a questo pacchetto, è possibile selezionare **Avvia tutto** per aprire tutte le applicazioni. Per sequenziare il pacchetto, fare clic su **Avanti**.

8. Dopo aver creato il pacchetto, nella console App-V Sequencer selezionare **File**  /  **Salva** file e specificare il nome e il percorso dell'unità virtuale in cui verrà salvato il pacchetto.

   È possibile creare facoltativamente un file di Windows Installer (con**estensione msi**) associato per installare il pacchetto dell'applicazione virtuale nei computer di destinazione. Per creare un file di Windows Installer, aprire il pacchetto nel sequencer e selezionare **strumenti**  /  **Crea MSI**. Il file di Windows Installer verrà creato e salvato nella directory in cui è salvato il pacchetto dell'applicazione virtuale.

   **Importante**  
   Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



## Argomenti correlati


[Come eseguire l'aggiornamento di un pacchetto applicazione virtuale (App-V 4.6)](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









