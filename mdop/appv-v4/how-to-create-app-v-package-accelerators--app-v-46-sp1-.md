---
title: Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)
description: Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817636"
---
# Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)


Puoi usare gli acceleratori pacchetto di App-V per generare automaticamente un nuovo pacchetto di applicazione virtuale. Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto. Per altre informazioni sugli acceleratori di pacchetto, vedere [informazioni sugli acceleratori di pacchetti App-v (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md). La creazione di acceleratori pacchetto App-V è un'attività avanzata. Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente. È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto App-V.

In alcune situazioni, per creare l'Acceleratore pacchetto, potrebbe essere necessario installare l'applicazione localmente nel computer in cui è in uso il sequencer. Prima di tutto, prova a creare l'Acceleratore pacchetto usando il supporto di installazione e se sono presenti diversi file mancanti, installa l'applicazione localmente nel computer che esegue il sequencer e quindi crea l'Acceleratore pacchetto.

**Importante**  
Prima di iniziare la procedura seguente, è necessario eseguire le operazioni seguenti:

-   Copiare il pacchetto di applicazione virtuale che deve essere usato per creare l'Acceleratore pacchetto in locale nel computer in cui è in uso il sequencer.

-   Copiare tutti i file di installazione necessari associati al pacchetto di applicazione virtuale nel computer in cui è in uso Sequencer.



**Importante**  
Dichiarazione di non responsabilità: Microsoft Application Virtualization Sequencer non offre alcun diritto di licenza per l'applicazione software in uso per creare un Acceleratore pacchetto. È necessario rispettare tutte le condizioni di licenza per l'utente finale per tale applicazione. È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando Application Virtualization Sequencer.



**Per creare un Acceleratore pacchetto App-V**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per avviare l'app-v **creare l'acceleratore guidata pacchetto** , in App-v Sequencer fare clic su **strumenti**  /  **Crea pacchetto acceleratore**.

3.  Nella pagina **Seleziona pacchetto** , per specificare un pacchetto di applicazione virtuale esistente da usare per creare l'Acceleratore pacchetto, fare clic su **Sfoglia**e individuare il pacchetto di applicazione virtuale esistente (file con estensione SPRJ).

    **Suggerimento**  
    Copiare i file associati al pacchetto di applicazione virtuale che si prevede di usare localmente per il computer in cui è in uso il sequencer.



~~~
Click **Next**.
~~~

4. Nella pagina **file di installazione** per specificare la cartella che contiene i file di installazione usati per creare il pacchetto di applicazione virtuale originale, fare clic su **Sfoglia**e quindi selezionare la directory contenente i file di installazione.

   **Suggerimento**  
   Copiare la cartella che contiene i file di installazione necessari nel computer in cui è in corso il sequencer.



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. Nella pagina **raccolta informazioni** esaminare i file che non sono stati trovati nella posizione specificata nella pagina file di **installazione** della procedura guidata. Se i file visualizzati non sono obbligatori, selezionare **Rimuovi questi file**e quindi fare clic su **Avanti**. Se i file sono necessari, fare clic su **precedente** e copiare i file necessari nella directory specificata nella pagina **file di installazione** .

   **Nota**  
   Per passare alla pagina successiva della procedura guidata, è necessario rimuovere i file non necessari oppure fare clic su **precedente** e individuare i file necessari.



6. Nella pagina **Seleziona file** esaminare attentamente i file rilevati e deselezionare qualsiasi file che deve essere rimosso dall'acceleratore pacchetto. Selezionare solo i file necessari per l'esecuzione corretta dell'applicazione e quindi fare clic su **Avanti**.

7. Nella pagina **Verifica applicazioni verificare** che tutti i file di installazione necessari per compilare il pacchetto vengano visualizzati. Quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto, tutti i file di installazione visualizzati nel riquadro **applicazioni** sono necessari per creare il pacchetto.

   Se necessario, per aggiungere altri file di installazione, fare clic su **Aggiungi**. Per rimuovere i file di installazione non necessari, selezionarlo e quindi fare clic su **Elimina**. Per modificare le proprietà associate a un programma di installazione, fare clic su **modifica**. I file di installazione specificati in questo passaggio saranno necessari quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto di applicazione virtuale. Dopo aver confermato le informazioni visualizzate, fare clic su **Avanti**.

8. Nella pagina **Seleziona linee guida** per specificare un file che contiene informazioni sul modo in cui l'acceleratore del pacchetto fa clic su **Sfoglia**. Ad esempio, questo file può contenere informazioni sul modo in cui il computer che eseguono il Sequencer deve essere configurato, informazioni sui prerequisiti dell'applicazione per i computer di destinazione e note generali. Devi specificare tutte le informazioni necessarie per applicare correttamente l'Acceleratore pacchetto. Il file selezionato deve essere in formato RTF (Rich Text) o file di testo (txt). Fai clic su **Avanti**.

9. Nella pagina **Crea Acceleratore pacchetto** , per specificare dove salvare l'Acceleratore pacchetto, fare clic su **Sfoglia** e selezionare la directory.

10. Nella pagina **completamento** , per chiudere la procedura guidata **Crea accelerazione pacchetto** , fare clic su **Chiudi**.

   **Importante**  
   Per assicurarti che l'acceleratore del pacchetto sia il più sicuro possibile e che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto, devi sempre firmare digitalmente l'acceleratore del pacchetto.



## Argomenti correlati


Configurazione dell'Application Virtualization Sequencer (App-V 4,6 SP1) [come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (app-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)









