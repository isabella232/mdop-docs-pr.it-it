---
title: Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino
description: Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822925"
---
# Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include la **procedura guidata** per l'immagine di ripristino delle freccette usata in Windows per creare un'immagine dell'organizzazione internazionale per la standardizzazione (ISO) avviabile. Un'immagine ISO è un file che rappresenta il contenuto non elaborato di un CD.

La **procedura guidata immagine di ripristino di freccette** richiede le informazioni seguenti:

-   **Immagine di avvio**˚ ˚ è necessario specificare il percorso di un file di origine di Windows 7 DVD o Windows 7 necessario per creare l'immagine di ripristino delle freccette.

-   **Strumento di selezione**˚ ˚ è possibile selezionare gli strumenti da includere nell'immagine di ripristino delle freccette.

-   **Connessioni remote**˚ ˚ è possibile specificare se si vuole che l'immagine di ripristino delle freccette includa la possibilità di stabilire una connessione remota tra l'helpdesk e il computer dell'utente finale.

-   **Strumenti di debug per Windows**˚ ˚ viene richiesto di specificare la posizione degli strumenti di debug per Windows.

-   **Definizioni per il sistema autonomo Sweeper**˚ ˚ è possibile decidere se scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino o scaricare le definizioni in un secondo momento.

-   **Driver**˚ ˚ viene chiesto se si vuole aggiungere driver all'immagine ISO.

-   **File aggiuntivi**˚ ˚ è possibile aggiungere file all'immagine ISO che potrebbero essere utili per la diagnosi dei problemi.

-   **Posizione dell'immagine ISO**˚ ˚ viene chiesto di specificare dove deve essere posizionata l'immagine ISO.

-   **Unità CD/DVD**˚ ˚ viene chiesto di specificare se usare l'unità CD o DVD per masterizzare il CD o il DVD.

**Nota**  Le dimensioni dell'immagine ISO possono variare a seconda degli strumenti selezionati nella **creazione guidata immagine di ripristino di Dart**.

 

## Per creare l'immagine di ripristino usando la creazione guidata immagine di ripristino di freccette


Seguire queste istruzioni per usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino delle freccette.

### Per selezionare gli strumenti da includere nell'immagine di ripristino delle freccette

La **procedura guidata immagine recupero dardo** presenta una finestra di dialogo di **selezione dello strumento** . È possibile selezionare o rimuovere strumenti dall'elenco di strumenti da includere nell'immagine di ripristino delle freccette evidenziando uno strumento e quindi facendo clic sui pulsanti **Abilita** o **Disabilita** .

Dopo aver selezionato tutti gli strumenti che si desidera includere nell'immagine di ripristino, fare clic su **Avanti**.

### Per aggiungere l'opzione per consentire la connettività remota

È possibile selezionare la casella di controllo **Consenti connessioni remote** per specificare l'opzione nella finestra del **set di strumenti di diagnostica e ripristino** per stabilire una connessione remota tra l'agente helpdesk e un computer dell'utente finale. Dopo che un agente dell'helpdesk stabilisce una connessione remota, può eseguire gli strumenti DaRT nel computer dell'utente finale da una posizione remota.

È possibile selezionare la casella di controllo **specifica il numero di porta** per immettere un numero di porta specifico che verrà usato per stabilire una connessione remota. È possibile specificare un numero di porta compreso tra 1 e 65535. È consigliabile che il numero di porta sia 1024 o superiore per ridurre al minimo la possibilità di un conflitto.

È anche possibile creare un messaggio personalizzato che verrà ricevuto da un utente finale quando stabilisce una connessione remota. Il messaggio può contenere un massimo di 2048 caratteri.

Per altre informazioni su come eseguire in remoto gli strumenti DaRT, Vedi [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

### Per aggiungere gli strumenti di debug per Windows all'immagine di ripristino DaRT

Nella finestra di dialogo **analizzatore crash** della **creazione guidata immagine di ripristino di freccette**viene richiesto di specificare la posizione degli strumenti di debug per Windows. Se non si dispone di una copia degli strumenti, è possibile scaricarli da Microsoft. Il collegamento seguente alla pagina di download è disponibile nella procedura guidata: [scaricare e installare gli strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

È possibile specificare la posizione degli strumenti di debug nel computer in cui è in uso la **creazione guidata immagine di ripristino di freccette**oppure si può decidere di usare gli strumenti disponibili nel computer di destinazione. Se si decide di usare una copia in un altro computer, è necessario assicurarsi che gli strumenti siano installati in ogni computer in cui si sta effettuando la diagnosi di un arresto anomalo.

**Nota**  Se si include l' **analizzatore crash** nell'immagine ISO, è consigliabile includere anche gli strumenti di debug per Windows.

 

Seguire questa procedura per aggiungere gli strumenti di debug per Windows:

1.  Opzionale Fare clic sul collegamento ipertestuale per scaricare gli strumenti di debug per Windows.

2.  Selezionare una delle opzioni seguenti:

    -   **Usare gli strumenti di debug per Windows nella posizione seguente**. Se si seleziona questa opzione, è possibile passare alla posizione degli strumenti.

    -   **Individuare gli strumenti di debug per Windows nel sistema che si sta ripristinando**. Se si seleziona questa opzione, l' **analizzatore crash** non funzionerà se gli strumenti di debug per Windows non vengono trovati nel computer problema.

3.  Al termine, fare clic su **Avanti**.

### Per aggiungere definizioni per la spazzatrice di sistema autonoma all'immagine di ripristino DaRT

Le definizioni sono un repository di malware noti e di altri software potenzialmente indesiderati. Poiché il malware viene continuamente sviluppato, la **spazzatrice di sistema autonoma** si basa sulle definizioni correnti per determinare se il software che sta provando a installare, eseguire o modificare le impostazioni in un computer è un software potenzialmente indesiderato o malevolo.

Per includere le definizioni più recenti nell'immagine di ripristino delle freccette (scelta consigliata), fare clic su **Sì, scaricare le definizioni più recenti.** L'aggiornamento della definizione viene avviato automaticamente. Per completare il processo, è necessario essere connessi a Internet.

Per ignorare l'aggiornamento della definizione, fare clic su **No, scaricare manualmente le definizioni in un secondo momento**. Le definizioni non verranno incluse nell'immagine di ripristino delle freccette.

Se si decide di non includere le definizioni più recenti nell'immagine di ripristino o se le definizioni incluse nell'immagine di ripristino non sono più aggiornate quando si è pronti per **l'uso,** è possibile ottenere le definizioni più recenti prima di iniziare un'analisi seguendo le istruzioni fornite nella **spazzatrice di sistema autonomo**.

**Importante**  Non è possibile eseguire la digitalizzazione se non sono presenti definizioni.

 

Al termine, fare clic su **Avanti**.

### Per aggiungere driver all'immagine di ripristino delle freccette

**Attenzione**  Per impostazione predefinita, quando si aggiunge un driver all'immagine di ripristino DaRT, tutti i file e le sottocartelle presenti in tale cartella vengono aggiunti all'immagine di ripristino. Per altre informazioni, vedere [risoluzione dei problemi relativi a DaRT 7,0](troubleshooting-dart-70-new-ia.md).

 

È consigliabile includere altri driver nell'immagine di ripristino per DaRT7 che potrebbe essere necessario quando si ripristina un computer. In genere possono includere controller di archiviazione o di rete non inclusi in Windows DVD.

**Importante**  Quando si selezionano i driver da includere, tenere presente che la connettività wireless (ad esempio Bluetooth o 802.11 a/b/g/n) non è supportata in DaRT.

 

**Per aggiungere un driver di archiviazione o controller di rete all'immagine di ripristino**

1.  Nella finestra di dialogo **driver aggiuntivi** della **creazione guidata immagine di ripristino di freccette**fare clic su **Aggiungi dispositivo**.

2.  Passare al file da aggiungere per il driver e quindi fare clic su **Apri**.

    **Nota**  Il file del **driver** viene fornito dal produttore del controller di archiviazione o di rete.

     

3.  Ripetere i passaggi 1 e 2 per ogni driver che si desidera includere.

4.  Al termine, fare clic su **Avanti**.

### Per aggiungere file all'immagine di ripristino delle freccette

Seguire questa procedura per aggiungere file all'immagine di ripristino, in modo da poterli usare per diagnosticare i problemi del computer.

1.  Nella finestra di dialogo **file aggiuntivi** della **creazione guidata immagine di ripristino di freccette**fare clic su **Mostra file**. Verrà aperta una finestra di Esplora risorse che visualizza la cartella che contiene i file condivisi.

2.  Creare una sottocartella nella cartella elencata nella finestra di dialogo.

3.  Copiare i file desiderati nella nuova sottocartella.

4.  Al termine, fare clic su **Avanti.**

### Per selezionare una posizione per l'ISO che contiene l'immagine di ripristino DaRT

Seguire questa procedura per specificare la posizione in cui viene creata l'immagine ISO:

1.  Nella finestra di dialogo **Crea immagine di avvio** della **creazione guidata immagine di ripristino di freccette**fare clic su **Sfoglia**.

2.  Passare alla posizione preferita nella finestra **Salva con nome** e quindi fare clic su **Salva**.

3.  Al termine, fare clic su **Avanti**.

Le dimensioni dell'immagine ISO variano a seconda degli strumenti selezionati e dei file che si aggiungono nella procedura guidata.

La procedura guidata richiede che l'immagine ISO abbia un'estensione di file **ISO,** perché la maggior parte dei programmi che masterizzano un CD o un DVD richiedono tale estensione. Se non specifichi una posizione diversa, l'immagine ISO viene creata sul desktop con il nome **DaRT70. ISO**.

### Per masterizzare l'immagine di ripristino su un CD o un DVD

Se la **procedura guidata** per l'immagine di ripristino di freccette rileva un'unità CD-RW compatibile nel computer, offre di masterizzare l'immagine ISO su un disco. Se si vuole masterizzare un CD o un DVD e la procedura guidata non riconosce l'unità, è necessario usare un altro programma, ad esempio il programma incluso nell'unità. È possibile usare un duplicatore, un servizio di duplicazione o un software di masterizzazione CD o DVD per apportare altre copie.

1.  Nella finestra di dialogo **Masterizza in un CD/DVD registrabile** della **procedura guidata immagine di ripristino di freccette**Selezionare **brucia l'immagine per l'unità CD/DVD registrabile seguente**.

2.  Selezionare l'unità CD o DVD.

    **Nota**  Se un'unità non viene riconosciuta e si installa una nuova unità, è possibile fare clic su **Aggiorna elenco unità** per forzare la procedura guidata ad aggiornare l'elenco delle unità disponibili.

     

3.  Fai clic su **Avanti**.

## Argomenti correlati


[Creazione dell'immagine di ripristino di DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





