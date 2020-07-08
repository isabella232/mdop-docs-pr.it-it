---
title: Come eseguire l'aggiornamento di un pacchetto applicazione virtuale (App-V 4.6)
description: Come eseguire l'aggiornamento di un pacchetto applicazione virtuale (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816456"
---
# Come eseguire l'aggiornamento di un pacchetto applicazione virtuale (App-V 4.6)


Usare la procedura seguente per aggiornare un'applicazione virtuale esistente tramite Application Virtualization (App-V) Sequencer. Puoi anche usare la console dell'App-V Sequencer per apportare modifiche a un'applicazione virtuale esistente senza eseguire un aggiornamento, ma non puoi apportare modifiche al file System dell'applicazione virtuale usando questo metodo perché l'App-V Sequencer non decodifica effettivamente il file SFT associato. Per altre informazioni sulla modifica di un pacchetto esistente, vedere [come modificare un pacchetto di applicazione virtuale (App-V 4,6)](how-to-modify-a-virtual-application-package--app-v-46-.md).

**Per aggiornare un'applicazione virtuale esistente**

1.  Per avviare la console App-v sequencer, nel computer in cui è in uso App-v sequencer selezionare **Avvia**  /  **programmi**  /  **Microsoft**Application Virtualization  /  **sequencer**.

2.  Per aprire il pacchetto di applicazione virtuale esistente e avviare la **sequenziazione guidata**, selezionare **Aggiorna un pacchetto**. Individuare il pacchetto da aggiornare e fare clic su **Apri**. Nella finestra di dialogo **Sfoglia per la cartella** specificare la posizione in cui verrà inserita la versione aggiornata del pacchetto. Questa posizione specificata deve trovarsi nell'unità specificata come unità di virtualizzazione dell'applicazione, che in genere è l'unità Q:\\. Per creare una nuova cartella, selezionare **Crea nuova cartella**.

    **Avviso**  Devi specificare la cartella radice dell'applicazione virtuale esistente. Non creare manualmente una sottocartella o l'aggiornamento avrà esito negativo.

     

3.  Nella pagina **informazioni pacchetto** specificare il nome del **pacchetto** che verrà assegnato al pacchetto aggiornato. Il nome del pacchetto è necessario per la generazione del file di Windows Installer associato. È anche necessario aggiungere un commento facoltativo che verrà assegnato al pacchetto e che fornisca informazioni dettagliate sull'applicazione virtuale, ad esempio un numero di versione. Per visualizzare la pagina **Opzioni avanzate** , selezionare **Mostra opzioni di monitoraggio avanzato** e fare clic su **Avanti**; in caso contrario, procedere con il passaggio 5.

4.  Nella pagina **Opzioni avanzate** per consentire a Microsoft Update di aggiornare l'applicazione durante la sequenziazione, selezionare **Consenti l'esecuzione di Microsoft Update durante il monitoraggio**. Se si seleziona questa opzione, gli aggiornamenti di Microsoft possono essere installati durante la fase di monitoraggio e sarà necessario accettare gli aggiornamenti associati per l'installazione. Per rimappare i file dll (Dynamic-Link Library) supportati in modo che usino uno spazio di RAM contiguo, selezionare **rebase dll**. Se si seleziona questa opzione, è possibile risparmiare memoria e migliorare le prestazioni. Fai clic su **Avanti**.

5.  Nella pagina di **installazione di monitor** , quando si è pronti per aggiornare l'applicazione, fare clic su **Avvia monitoraggio**.

    Quando sono stati applicati gli aggiornamenti per l'applicazione, fare clic su **Interrompi monitoraggio**. Fai clic su **Avanti**.

6.  Nella pagina **Configura applicazioni** , se necessario, configura i tasti di scelta rapida e le associazioni di tipi di file che verranno associati all'applicazione virtuale. Per aggiungere una nuova associazione o collegamento di tipo file, fare clic su **Aggiungi**e quindi nella finestra di dialogo **Aggiungi applicazione** specificare il nuovo elemento. Per rimuovere un collegamento o un tipo di file di associazione esistente, fare clic su **Rimuovi**. Per modificare un elemento esistente, selezionare l'elemento che si vuole modificare e quindi fare clic su **modifica**. Specificare le configurazioni nella finestra di dialogo **Modifica applicazione** . Fare clic su **Save**. Fai clic su **Avanti**.

7.  Nella pagina **Avvia applicazioni** , per avviare l'applicazione per verificare che il pacchetto sia stato installato correttamente ed è ottimizzato per lo streaming, selezionare il pacchetto e fare clic su **Avvia**. Questo passaggio è utile per configurare l'esecuzione iniziale dell'applicazione nei computer di destinazione e per accettare eventuali contratti di licenza associati prima che il pacchetto venga reso disponibile ai client App-V. Se sono associate più applicazioni a questo pacchetto, è possibile selezionare **Avvia tutto** per aprire tutte le applicazioni. Per sequenziare il pacchetto, fare clic su **Avanti**.

8.  Per chiudere la procedura guidata di sequenziazione, fare clic su **fine**. Per salvare il pacchetto aggiornato, nella console sequencer selezionare **File**  /  **Salva**file.

    Se si prevede di distribuire il pacchetto aggiornato usando un file di Windows Installer (con estensione msi), è necessario crearne uno nuovo come segue: nella console sequencer selezionare **strumenti**  /  **Crea MSI**. Il nuovo file di Windows Installer verrà creato e salvato nella directory in cui è stato salvato il pacchetto dell'applicazione virtuale aggiornata.

## Argomenti correlati


[Come sequenziare una nuova applicazione (App-V 4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





