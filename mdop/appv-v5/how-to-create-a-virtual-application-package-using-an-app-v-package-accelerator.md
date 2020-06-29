---
title: Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V
description: Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V
author: dansimp
ms.assetid: 715e7526-e100-419c-8fc1-75cbfe433835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 547cb93f334e025243937a97a1f904410fe2d504
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805601"
---
# Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V


**Importante**  
L'App-V 5,0 sequencer non concede diritti di licenza per l'applicazione software che usi per creare l'Acceleratore pacchetto. È necessario rispettare tutte le condizioni di licenza per l'utente finale per l'applicazione in uso. È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto con l'App-V 5,0 sequencer.



Usare la procedura seguente per creare un pacchetto di applicazione virtuale con l'acceleratore del pacchetto App-V 5,0.

**Nota**  
Prima di iniziare questa procedura, copiare l'Acceleratore pacchetto richiesto localmente nel computer in cui è in esecuzione l'App-V 5,0 sequencer. È consigliabile copiare anche tutti i file di installazione necessari per il pacchetto in una directory locale nel computer in cui è in esecuzione il sequencer. Questa è la directory che è necessario specificare nel passaggio 5 di questa procedura.



**Per creare un pacchetto di applicazione virtuale con un Acceleratore pacchetto App-V 5,0**

1.  Per avviare l'app-v sequencer, nel computer in cui è in esecuzione l'app-v 5,0 Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Per avviare la **procedura guidata Crea nuovo pacchetto**, fai clic su **Crea un nuovo pacchetto di applicazione virtuale**. Per creare il pacchetto, selezionare la casella di controllo **Crea pacchetto usando un Acceleratore pacchetto** e quindi fare clic su **Avanti**.

3.  Per specificare l'Acceleratore pacchetto che verrà usato per creare il nuovo pacchetto di applicazione virtuale, fare clic su **Sfoglia** nella pagina **Seleziona Acceleratore pacchetto** . Fai clic su **Avanti**.

    **Importante**  
    Se l'autore dell'Accelerator pacchetto non può essere verificato e non contiene una firma digitale valida, prima di fare clic su **Esegui**, è necessario verificare che l'origine dell'acceleratore pacchetto sia attendibile. Confermare l'opzione desiderata nella finestra di dialogo **avviso di sicurezza** .



4.  Nella pagina **linee guida** esaminare le informazioni di guida per la pubblicazione visualizzate nel riquadro informazioni. Queste informazioni sono state aggiunte quando l'Acceleratore pacchetto è stato creato e contiene indicazioni su come creare e pubblicare il pacchetto. Per esportare le informazioni di orientamento in un file di testo (txt), fare clic su **Esporta** e specificare il percorso in cui salvare il file e quindi fare clic su **Avanti**.

5.  Nella pagina **selezionare i file di installazione** fare clic su Crea **nuova cartella** per creare una cartella locale contenente tutti i file di installazione necessari per il pacchetto e specificare la posizione in cui salvare la cartella. Devi anche specificare un nome che deve essere assegnato alla cartella. È quindi necessario copiare tutti i file di installazione necessari nella posizione specificata. Se nel computer che esegue il sequencer esiste già la cartella che contiene i file di installazione, fare clic su **Sfoglia** per selezionare la cartella.

    In alternativa, se i file di installazione sono già stati copiati in una directory di questo computer, fare clic su **Crea nuova cartella**, passare alla cartella contenente i file di installazione e quindi fare clic su **Avanti**.

    **Nota**  
    Puoi specificare i tipi di file di installazione supportati seguenti:

    -   File di Windows Installer (con**estensione msi**)

    -   File cabinet (CAB)

    -   File compressi con estensione zip

    -   File di applicazione effettivi

    I tipi di file seguenti non sono supportati: file **msp** e **exe** . Se si specifica un file **exe** , è necessario estrarre manualmente i file di installazione.



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. Nella pagina **nome pacchetto** specificare un nome che verrà associato al pacchetto. Il nome specificato identifica il pacchetto in App-V Management Console. Fai clic su **Avanti**.

7. Nella pagina **Crea pacchetto** , fornisci i commenti che verranno associati al pacchetto. I commenti devono contenere informazioni di identificazione sul pacchetto da creare. Per confermare la posizione in cui è stato creato il pacchetto, esaminare le informazioni visualizzate in **Salva posizione**. Per comprimere il pacchetto, seleziona **Comprimi pacchetto**. Selezionare la casella di controllo **Comprimi pacchetto** se il pacchetto verrà trasmesso attraverso la rete o quando la dimensione del pacchetto supera 4 GB.

   Per creare il pacchetto, fare clic su **Crea**. Dopo aver creato il pacchetto, fare clic su **Avanti**.

8. Nella pagina **Configura software** per consentire al sequencer di configurare le applicazioni contenute nel pacchetto, selezionare **Configura software**. In questo passaggio è possibile configurare le attività associate che devono essere completate per eseguire l'applicazione nei computer di destinazione. Ad esempio, puoi configurare qualsiasi contratto di licenza associato.

   Se si seleziona **Configura software**, gli elementi seguenti possono essere configurati usando il sequencer come parte di questo passaggio:

   -   **Caricare il pacchetto**. Il sequencer carica i file associati al pacchetto. Per decodificare il pacchetto può essere necessario qualche secondo a un'ora.

   -   **Eseguire ogni programma**. Facoltativamente, eseguire i programmi contenuti nel pacchetto. Questo passaggio è utile per completare le attività di configurazione o di licenza associate necessarie per eseguire l'applicazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire tutti i programmi contemporaneamente, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi che si desidera eseguire e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Per l'esecuzione di tutti i programmi, possono essere necessarie diversi minuti. Fai clic su **Avanti**.

   -   **Salva pacchetto**. Il sequencer Salva il pacchetto.

   -   **Blocco di funzionalità principale**. Il sequencer ottimizza il pacchetto per lo streaming ricostruendo il blocco di funzionalità principale.

   Se non si desidera configurare le applicazioni, fare clic su **Ignora questo passaggio**e passare al passaggio 9 della procedura e quindi fare clic su **Avanti**.

9. Nella pagina **completamento** , dopo aver esaminato le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** , fare clic su **Chiudi**.

   Il pacchetto è ora disponibile nel sequencer. Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**. Per altre informazioni su come modificare un pacchetto, vedere [come modificare un pacchetto di applicazione virtuale esistente](how-to-modify-an-existing-virtual-application-package-beta.md).

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)









