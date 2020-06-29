---
title: Come sequenziare una nuova applicazione
description: Come sequenziare una nuova applicazione
author: dansimp
ms.assetid: e01e98cd-2378-478f-9739-f72c465bf79a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aab769256116e2635edbc4bcf55d212e3a2152f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816666"
---
# Come sequenziare una nuova applicazione


L'Application Virtualization (App-V) Sequencer crea applicazioni che possono essere eseguite in un ambiente virtuale. App-V Sequencer monitora il processo di installazione e configurazione per un'applicazione e registra le informazioni necessarie per l'esecuzione dell'applicazione in un ambiente virtuale. Puoi anche usare l'App-V Sequencer per configurare i file e le configurazioni applicabili a tutti gli utenti e i file e le configurazioni che gli utenti possono personalizzare. Quando si sequenzia un'applicazione, è necessario salvare il pacchetto in un'unità locale del computer in cui si esegue la sequenziazione.

Un'applicazione sequenziata non interagisce con il sistema operativo perché ogni applicazione viene eseguita in un ambiente virtuale ed è isolata da altre applicazioni che potrebbero essere installate o in esecuzione nel computer di destinazione. Questo isolamento riduce drasticamente i conflitti delle applicazioni e diminuisce la quantità necessaria di test pre-distribuzione dell'applicazione.

Dopo aver correttamente sequenziato l'applicazione, è disponibile nella console App-V Sequencer. L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.

**Per sequenziare una nuova applicazione**

1.  Devi creare l'unità di virtualizzazione dell'applicazione per sequenziare una nuova applicazione virtuale. Per creare l'unità di virtualizzazione dell'applicazione, eseguire il mapping dell'unità Q:\\ a una posizione che può essere usata per salvare i file durante la sequenziazione di un'applicazione. È quindi necessario creare singole directory per ogni applicazione che si prevede di sequenziare nell'unità Q:\\. È possibile creare le cartelle di destinazione dell'applicazione virtuale prima di sequenziare un'applicazione oppure crearla nel passaggio 5 di questa procedura.

2.  Per avviare la console App-v sequencer, nel computer in cui è in uso l'app-v sequencer selezionare **Avvia**  /  **programmi**  /  **Microsoft**Application Virtualization  /  **sequencer**. Per avviare la **sequenziazione guidata**, selezionare **file**  /  **nuovo pacchetto**.

3.  Nella pagina **informazioni pacchetto** specificare il nome del **pacchetto** che verrà assegnato all'applicazione virtuale. Il nome del pacchetto è necessario per la generazione del file di Windows Installer associato. Dovresti anche aggiungere un commento facoltativo che verrà assegnato al pacchetto e che fornisce informazioni dettagliate sull'applicazione virtuale. Per visualizzare la pagina **Opzioni avanzate** , selezionare **Mostra opzioni di monitoraggio avanzate**. Fai clic su **Avanti**.

    **Nota**  
    Per visualizzare la pagina **Opzioni avanzate** , è necessario selezionare **Mostra opzioni di monitoraggio avanzate**. Se non è necessaria la pagina **Opzioni avanzate** , passare al passaggio 4.



4.  Nella pagina **Opzioni avanzate** per specificare le dimensioni del **blocco** per l'applicazione virtuale, selezionare le dimensioni desiderate. La dimensione del blocco determina il modo in cui verrà suddiviso il file **. SFT** per lo streaming del pacchetto in rete per i computer di destinazione. Per consentire a Microsoft Update di aggiornare l'applicazione man mano che viene sequenziata; Selezionare **Consenti l'esecuzione di Microsoft Update durante il monitoraggio**. Se si seleziona questa opzione, gli aggiornamenti di Microsoft possono essere installati durante la fase di monitoraggio e sarà necessario accettare gli aggiornamenti associati per l'installazione. Per rimappare i file dll (Dynamic Link Library) supportati in modo che usino uno spazio di RAM contiguo, selezionare **rebase dll**. Se si seleziona questa opzione, è possibile risparmiare memoria e migliorare le prestazioni. Molte applicazioni non supportano questa opzione, ma è utile in ambienti con RAM limitata, ad esempio in scenari Terminal Server. Fai clic su **Avanti**.

5.  Nella pagina di **installazione di monitor** , per monitorare l'installazione di un'applicazione, fare clic su **Avvia monitoraggio**. Dopo aver fatto clic su **Avvia monitoraggio**, specificare la directory nell'unità Q:\\ in cui verrà installata l'applicazione. Per installare l'applicazione in una cartella che non è stata creata, fare clic su **Crea nuova cartella**. È necessario installare ogni applicazione sequenziata in una directory separata.

    **Importante**  
    Il nome della cartella specificato non deve contenere più di 8 caratteri.



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring** and then click **Next**.
~~~

6. Nella pagina file **aggiuntivi da associare a Virtual File System (VFS)** , per specificare altri file da aggiungere al file system virtuale (VFS), fare clic su **Aggiungi**. Passare al file che si vuole aggiungere e fare clic su **Apri**. Per cancellare i file esistenti aggiunti, fare clic su **Reimposta** e quindi su **Avanti**.

7. Nella pagina **Configura applicazioni** configurare i tasti di scelta rapida e le associazioni di tipi di file che verranno associati all'applicazione virtuale. Selezionare l'elemento che si vuole aggiornare e quindi fare clic su **modifica posizioni**. Specificare le configurazioni nella finestra di dialogo **posizioni di scelta rapida** . Fare clic su **OK** e quindi su **Avanti**.

8. Nella pagina **Avvia applicazioni** , per avviare l'applicazione per verificare che il pacchetto sia ottimizzato per lo streaming, selezionare il pacchetto e fare clic su **Avvia**. Questo passaggio è utile per configurare l'esecuzione iniziale dell'applicazione nei computer di destinazione e per accettare eventuali contratti di licenza associati prima che il pacchetto venga reso disponibile ai client. Se sono presenti più applicazioni associate al pacchetto, è possibile selezionare **Avvia tutto** per aprire tutte le applicazioni. Per sequenziare il pacchetto, fare clic su **Avanti**.

9. Nella pagina **Sequence Package** , per chiudere la procedura guidata, fare clic su **fine**.

10. Dopo aver creato il pacchetto, per salvare il pacchetto, nella console App-V Sequencer selezionare **File**  /  **Salva** file e specificare il nome e il percorso in cui verrà salvato il pacchetto.

## Argomenti correlati


[Attività per Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









