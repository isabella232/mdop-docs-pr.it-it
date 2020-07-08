---
title: Come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (App-V 4,6 SP1)
description: Come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821385"
---
# Come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (App-V 4,6 SP1)


Puoi usare gli acceleratori pacchetto di App-V per generare automaticamente un nuovo pacchetto di applicazione virtuale. Per altre informazioni sugli acceleratori di pacchetto, vedere [informazioni sugli acceleratori di pacchetti App-v (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

**Importante**  
Dichiarazione di non responsabilità: Application Virtualization Sequencer non offre alcun diritto di licenza per l'applicazione software in uso per creare un Acceleratore pacchetto. È necessario rispettare tutte le condizioni di licenza per l'utente finale per tale applicazione. È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando Application Virtualization Sequencer.



**Nota**  
Prima di iniziare questa procedura, copiare l'Acceleratore pacchetto richiesto localmente nel computer che ha eseguito App-V Sequencer. Dovresti anche copiare tutti i file di installazione necessari per il pacchetto in una directory locale nel computer in cui è in uso Sequencer. Questa è la directory che è necessario specificare nel passaggio 5 di questa procedura.



Usare la procedura seguente per creare un pacchetto di applicazione virtuale usando un Acceleratore pacchetto.

**Per creare un pacchetto di applicazione virtuale usando un Acceleratore pacchetto App-V**

1. Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2. Per avviare la **procedura guidata Crea nuovo pacchetto**, fai clic su **Crea un nuovo pacchetto di applicazione virtuale**. Per creare il pacchetto, selezionare la casella di controllo **Crea pacchetto usando un Acceleratore pacchetto** e quindi fare clic su **Avanti**.

3. Nella pagina **Seleziona Acceleratore pacchetto** per specificare l'Acceleratore pacchetto che verrà usato per creare il nuovo pacchetto di applicazione virtuale, fare clic su **Sfoglia** per individuare l'acceleratore di pacchetto che si vuole usare. Fai clic su **Avanti**.

   **Importante**  
   Se l'autore dell'Accelerator pacchetto non può essere verificato e non contiene una firma digitale valida, nella finestra di dialogo **avviso di sicurezza** è necessario verificare che sia attendibile l'origine dell'acceleratore del pacchetto prima di fare clic su **Esegui**.



4. Nella pagina **linee guida** esaminare le informazioni sulle indicazioni per la pubblicazione visualizzate nel riquadro delle informazioni. Le informazioni visualizzate sono state aggiunte quando l'Acceleratore pacchetto è stato creato e contiene informazioni sulla creazione e la pubblicazione del pacchetto. Per esportare le informazioni di orientamento in un file di testo (txt), fare clic su **Esporta** e specificare il percorso in cui salvare il file e quindi fare clic su **Avanti**.

5. Nella pagina **selezionare i file di installazione** per creare una cartella locale contenente tutti i file di installazione necessari per il pacchetto, fare clic su **Crea nuova cartella** e specificare la posizione in cui salvare la cartella. Devi anche specificare un nome che deve essere assegnato alla cartella. È quindi necessario copiare tutti i file di installazione necessari nella posizione specificata. Se la cartella che contiene i file di installazione esiste già nel computer in cui è in corso il sequencer, fare clic su **Sfoglia** per selezionare la cartella.

   In alternativa, se i file di installazione sono già stati copiati in una directory di questo computer, fare clic su **Crea nuova cartella**, passare alla cartella contenente i file di installazione e quindi fare clic su **Avanti**.

   **Nota**  
   Puoi specificare i tipi di file di installazione supportati seguenti:

   -   File di Windows Installer (con**estensione msi**

   -   file CAB

   -   File compressi con estensione zip

   -   File di applicazione effettivi

   I tipi di file seguenti non sono supportati: file **msp** e <strong> exe </strong> . Se si specifica un file **exe,** è necessario estrarre manualmente i file di installazione.



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. Nella pagina **nome pacchetto** specificare un nome che verrà associato al pacchetto. Il nome specificato identifica il pacchetto in App-V Management Console. Fai clic su **Avanti**.

7. Nella pagina **Crea pacchetto** , fornisci i commenti che verranno associati al pacchetto. I commenti devono contenere informazioni di identificazione sul pacchetto da creare. Per confermare la posizione in cui è stato creato il pacchetto, esaminare le informazioni visualizzate in **Salva posizione**. Per comprimere il pacchetto, seleziona **Comprimi pacchetto**. Selezionare la casella di controllo **Comprimi pacchetto** se il pacchetto verrà trasmesso attraverso la rete o quando la dimensione del pacchetto supera 4 GB.

   Per creare il pacchetto, fare clic su **Crea**. Dopo aver creato il pacchetto, fare clic su **Avanti**.

8. Nella pagina **Configura software** per consentire al sequencer di configurare le applicazioni contenute nel pacchetto, selezionare **Configura software**. Questo passaggio è utile per configurare le attività associate che devono essere completate per eseguire l'applicazione nei computer di destinazione, ad esempio la configurazione di eventuali contratti di licenza associati.

   Se si seleziona **Configura software**, gli elementi seguenti vengono configurati dal sequencer come parte di questo passaggio:

   -   **Caricare il pacchetto**. Il sequencer carica i file associati al pacchetto. Per decodificare il pacchetto può essere necessario un massimo di alcuni secondi fino a un'ora.

   -   **Eseguire ogni programma**. Facoltativamente, eseguire i programmi contenuti nel pacchetto. Questo passaggio è utile per completare le attività di configurazione o di licenza associate necessarie per eseguire l'applicazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi che si desidera eseguire e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Per l'esecuzione di tutti i programmi, possono essere necessarie diversi minuti. Fai clic su **Avanti**.

   -   **Salva pacchetto**. Il sequencer Salva il pacchetto.

   -   **Blocco di funzionalità principale**. Il sequencer ottimizza il pacchetto per lo streaming ricostruendo il blocco di funzionalità principale.

   Se non si desidera configurare le applicazioni, fare clic su **Ignora questo passaggio**e passare al passaggio 9 della procedura e quindi fare clic su **Avanti**.

9. Nella pagina **completamento** , dopo aver esaminato le informazioni visualizzate nel riquadro **report pacchetto applicazione virtuale** , fare clic su **Chiudi**.

   Il pacchetto è ora disponibile nel sequencer. Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**. Per altre informazioni sulla modifica di un pacchetto, vedere [come modificare un pacchetto di applicazione virtuale esistente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

## Argomenti correlati


[Configurazione di Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









