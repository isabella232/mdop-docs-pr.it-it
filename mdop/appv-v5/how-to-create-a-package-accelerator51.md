---
title: Come creare un acceleratore pacchetto
description: Come creare un acceleratore pacchetto
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805596"
---
# Come creare un acceleratore pacchetto


Gli acceleratori del pacchetto App-V 5,1 generano automaticamente nuovi pacchetti di applicazioni virtuali.

**Nota**  
Puoi usare PowerShell per creare un Acceleratore pacchetto. Per altre informazioni [, vedere come creare un Acceleratore pacchetto usando PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).



Per creare un Acceleratore pacchetto, usare la procedura seguente.

**Importante**  
Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente. È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto App-V 5,1.



**Importante**  
Prima di iniziare la procedura seguente, è necessario eseguire le operazioni seguenti:

-   Copiare il pacchetto di applicazione virtuale che verrà usato per creare l'Acceleratore pacchetto in locale nel computer che gestisce il sequencer.

-   Copiare tutti i file di installazione necessari associati al pacchetto di applicazione virtuale nel computer in cui è in uso Sequencer.



**Per creare un Acceleratore pacchetto**

1.  **Importante**  
    L'App-V 5,1 sequencer non concede diritti di licenza per l'applicazione software in uso per creare l'Acceleratore pacchetto. È necessario rispettare tutte le condizioni di licenza per l'utente finale per l'applicazione in uso. È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando l'App-V 5,1 Sequencer.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Per avviare l'app-v 5,1 **creazione guidata pacchetto acceleratore** , nella console di sequencer App-v 5,1 fare clic su **strumenti**  /  **Crea Acceleratore**.

3. Nella pagina **Seleziona pacchetto** , per specificare un pacchetto di applicazione virtuale esistente da usare per creare l'Acceleratore pacchetto, fare clic su **Sfoglia**e individuare il pacchetto di applicazione virtuale esistente (file con estensione appv).

   **Suggerimento**  
   Copiare i file associati al pacchetto di applicazione virtuale che si prevede di usare localmente per il computer in cui è in uso il sequencer.



~~~
Click **Next**.
~~~

4. Nella pagina **file di installazione** per specificare la cartella che contiene i file di installazione usati per creare il pacchetto di applicazione virtuale originale, fare clic su **Sfoglia**e quindi selezionare la directory contenente i file di installazione.

   **Suggerimento**  
   Copiare la cartella che contiene i file di installazione necessari nel computer in cui è in corso il sequencer.



5. Se l'applicazione è già installata nel computer in cui è in uso il sequencer, per specificare il file di installazione, selezionare **file installati nel sistema locale**. Per usare questa opzione, l'applicazione deve essere già installata nel percorso di installazione predefinito.

6. Nella pagina **raccolta informazioni** esaminare i file che non sono stati trovati nella posizione specificata nella pagina file di **installazione** della procedura guidata. Se i file visualizzati non sono obbligatori, selezionare **Rimuovi questi file**e quindi fare clic su **Avanti**. Se i file sono necessari, fare clic su **precedente** e copiare i file necessari nella directory specificata nella pagina **file di installazione** .

   **Nota**  
   Per passare alla pagina successiva della procedura guidata, è necessario rimuovere i file non necessari oppure fare clic su **precedente** e individuare i file necessari.



7. Nella pagina **Seleziona file** esaminare attentamente i file rilevati e deselezionare qualsiasi file che deve essere rimosso dall'acceleratore pacchetto. Selezionare solo i file necessari per l'esecuzione corretta dell'applicazione e quindi fare clic su **Avanti**.

8. Nella pagina **Verifica applicazioni verificare** che tutti i file di installazione necessari per compilare il pacchetto vengano visualizzati. Quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto, tutti i file di installazione visualizzati nel riquadro **applicazioni** sono necessari per creare il pacchetto.

   Se necessario, per aggiungere altri file di installazione, fare clic su **Aggiungi**. Per rimuovere i file di installazione non necessari, selezionarlo e quindi fare clic su **Elimina**. Per modificare le proprietà associate a un programma di installazione, fare clic su **modifica**. I file di installazione specificati in questo passaggio saranno necessari quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto di applicazione virtuale. Dopo aver confermato le informazioni visualizzate, fare clic su **Avanti**.

9. Nella pagina **Seleziona linee guida** per specificare un file che contiene informazioni sul modo in cui l'acceleratore del pacchetto fa clic su **Sfoglia**. Ad esempio, questo file può contenere informazioni sul modo in cui il computer che eseguono il Sequencer deve essere configurato, informazioni sui prerequisiti dell'applicazione per i computer di destinazione e note generali. Devi specificare tutte le informazioni necessarie per applicare correttamente l'Acceleratore pacchetto. Il file selezionato deve essere in formato RTF (Rich Text) o file di testo (txt). Fai clic su **Avanti**.

10. Nella pagina **Crea Acceleratore pacchetto** , per specificare dove salvare l'Acceleratore pacchetto, fare clic su **Sfoglia** e selezionare la directory.

11. Nella pagina **completamento** , per chiudere la procedura guidata **Crea accelerazione pacchetto** , fare clic su **Chiudi**.

   **Importante**  
   Per assicurarti che l'acceleratore del pacchetto sia il più sicuro possibile e che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto, devi sempre firmare digitalmente l'acceleratore del pacchetto.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

[Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









