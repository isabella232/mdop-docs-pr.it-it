---
title: Creazione dell'immagine di ripristino di DaRT 10
description: Creazione dell'immagine di ripristino di DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804804"
---
# Creazione dell'immagine di ripristino di DaRT 10


Dopo l'installazione di Microsoft Diagnostics and Recovery Toolset (DaRT) 10, puoi creare un'immagine di ripristino di DaRT 10. L'immagine di ripristino avvia Windows RE, da cui è possibile avviare gli strumenti DaRT. Puoi generare file ISO (International Organization for Standardizzation) e immagini WIM (Windows Imaging Format). Inoltre, puoi usare PowerShell per generare script che usano le impostazioni selezionate nella procedura guidata immagine di ripristino di DaRT. Puoi usare lo script in un secondo momento per ricostruire le immagini di ripristino usando le stesse impostazioni. L'immagine di ripristino offre un'ampia varietà di strumenti di ripristino. Per una descrizione degli strumenti, vedere [Panoramica degli strumenti in DART 10](overview-of-the-tools-in-dart-10.md).

Dopo aver avviato il computer in DaRT, puoi eseguire i diversi strumenti DaRT per provare a diagnosticare e ripristinare il computer. Questa sezione illustra il processo di creazione dell'immagine di ripristino delle freccette e consente di selezionare gli strumenti e le funzionalità che si desidera includere nell'immagine.

Puoi creare l'immagine di ripristino delle freccette usando uno dei due metodi seguenti:

-   Usa la configurazione guidata immagine di ripristino di freccette, che viene eseguita in un ambiente Windows.

-   Modificare uno script di PowerShell di esempio con i valori desiderati. Per altre informazioni, vedere [come usare uno script di PowerShell per creare l'immagine di ripristino](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).

È possibile scrivere l'ISO in un CD o un DVD registrabile, salvarlo in un'unità flash USB oppure salvarlo in un formato che può essere usato per l'avvio in freccette da una partizione remota o da una partizione di ripristino.

Dopo aver creato l'immagine ISO, è possibile masterizzarla su un CD o un DVD vuoto (se il computer ha un'unità CD o DVD). Se il computer in uso non ha un'unità per questo scopo, è possibile usare la maggior parte dei programmi generici usati per masterizzare CD o DVD.

## Selezionare l'architettura dell'immagine e specificare il percorso


Nella pagina Windows 10 Media selezionare se creare un'immagine di ripristino DaRT a 32 bit o a 64 bit. Usa la versione di Windows a 32 bit per creare immagini di ripristino delle freccette a 32 bit e Windows a 64 bit per creare immagini di ripristino delle freccette a 64 bit. È possibile usare un singolo computer per creare immagini di ripristino per entrambi i tipi di architettura, ma non è possibile creare un'immagine che funzioni sia in architetture a 32 bit che a 64 bit. Indichi anche il percorso del supporto di installazione di Windows 10. Scegli l'architettura che corrisponde a quella dell'immagine di ripristino che stai creando.

**Per selezionare l'architettura dell'immagine e specificare il percorso**

1.  Nella pagina **Windows 10 media** selezionare una delle opzioni seguenti:

    -   Se si sta creando un'immagine di ripristino per i computer a 64 bit, selezionare **Crea immagine di dardo x64 (64 bit)**.

    -   Se si sta creando un'immagine di ripristino per i computer a 32 bit, selezionare **Crea immagine di dardo x86 (32 bit)**.

2.  Nella casella **specifica il percorso radice della finestra di dialogo per l'installazione di Windows 10 &lt; 64 &gt; bit o 32 bit** digitare il percorso dei file di installazione di Windows 10. Usare un percorso che corrisponda all'architettura dell'immagine di ripristino che si sta creando.

3.  Fai clic su **Avanti**.

## Selezionare gli strumenti da includere nell'immagine di ripristino


Nella pagina strumenti è possibile selezionare numerosi strumenti da includere nell'immagine di ripristino. Questi strumenti saranno disponibili per gli utenti finali quando si avviano nell'immagine del dardo. Tuttavia, se si Abilita la connettività remota quando si crea l'immagine del dardo, tutti gli strumenti saranno disponibili quando un lavoratore dell'help desk si connette al computer dell'utente finale, indipendentemente dagli strumenti scelti per includere nell'immagine.

Per limitare l'accesso degli utenti finali a questi strumenti, mantenendo comunque l'accesso completo agli strumenti tramite il Visualizzatore connessione remota, non selezionare questi strumenti nella pagina strumenti. Gli utenti finali potranno usare solo la connessione remota e saranno in grado di vedere, ma non di accedere, tutti gli strumenti che Escludi dall'immagine di ripristino.

**Per selezionare gli strumenti da includere nell'immagine di ripristino**

1.  Nella pagina **strumenti** selezionare la casella di controllo accanto a ogni strumento che si vuole includere nell'immagine.

2.  Fai clic su **Avanti**.

## Scegliere se consentire la connettività remota tramite un help desk


Nella pagina connessione remota è possibile scegliere di consentire a un lavoratore dell'help desk di connettersi in remoto ed eseguire gli strumenti DaRT nel computer di un utente finale. L'opzione connettività remota viene quindi visualizzata come opzione disponibile nella finestra del set di strumenti di diagnostica e ripristino. Dopo che i dipendenti dell'help desk stabiliscono una connessione remota, possono eseguire gli strumenti DaRT nel computer dell'utente finale da una posizione remota.

**Per scegliere se consentire la connettività remota dagli operatori del supporto tecnico**

1.  Nella pagina **connessione remota** selezionare la casella di controllo **Consenti connessioni remote** per consentire connessioni remote o deselezionare la casella di controllo per impedire connessioni remote.

2.  Se la casella di controllo **Consenti connessioni remote** è stata deselezionata, fare clic su **Avanti**. In caso contrario, passare al passaggio successivo per continuare a configurare la connettività remota.

3.  Seleziona una delle opzioni seguenti:

    -   Fare in modo che Windows scelga un numero di porta aperto.

    -   Specificare il numero di porta. Se si seleziona questa opzione, immettere un numero di porta compreso tra 1 e 65535 nel campo sotto l'opzione. Questo numero di porta verrà usato per stabilire una connessione remota. È consigliabile che il numero di porta sia 1024 o superiore per ridurre al minimo la possibilità di un conflitto.

4.  (Facoltativo) nella finestra del messaggio di **benvenuto della connessione remota** creare un messaggio personalizzato che gli utenti finali ricevono quando stabiliscono una connessione remota. Il messaggio può contenere un massimo di 2048 caratteri.

5.  Fai clic su **Avanti**.

    Per altre informazioni sull'uso remoto degli strumenti DaRT, Vedi [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).

## Aggiungere driver all'immagine di ripristino


Nella scheda driver della pagina Opzioni avanzate è possibile aggiungere altri driver di dispositivo che potrebbero essere necessari per la riparazione di un computer. In genere possono includere controller di archiviazione o di rete non forniti da Windows 10. I driver vengono installati quando viene creata l'immagine.

**Importante**  Quando si selezionano i driver da includere, tenere presente che la connettività wireless (ad esempio Bluetooth o 802.11 a/b/g/n) non è supportata in DaRT.

 

**Per aggiungere driver all'immagine di ripristino**

1.  Nella pagina **Opzioni avanzate** fare clic sulla scheda **driver** .

2.  Fai clic su **Aggiungi**.

3.  Passare al file da aggiungere per il driver e quindi fare clic su **Apri**.

    **Nota**  Il file del driver viene fornito dal produttore del controller di archiviazione o di rete.

     

4.  Ripetere i passaggi 2 e 3 per ogni driver che si desidera includere.

5.  Fai clic su **Avanti**.

## Aggiungere pacchetti facoltativi di WinPE all'immagine di ripristino


Nella scheda WinPE della pagina Opzioni avanzate puoi aggiungere pacchetti facoltativi di WinPE all'immagine DaRT. Questi pacchetti fanno parte di Windows ADK, un prerequisito per l'installazione della procedura guidata per l'immagine di ripristino di DaRT. Gli strumenti che è possibile selezionare sono tutti facoltativi. Tutti i pacchetti necessari vengono aggiunti automaticamente, in base agli strumenti selezionati nella pagina strumenti.

È anche possibile specificare le dimensioni dello spazio di Scratch. Scratch Space è la quantità di spazio su disco RAM che viene accantonata per l'esecuzione di DaRT. Lo spazio di Scratch è utile nel caso in cui il disco rigido dell'utente finale non sia disponibile. Se si stanno usando altri strumenti e driver, è consigliabile aumentare lo spazio di Scratch.

**Per aggiungere pacchetti facoltativi di WinPE all'immagine di ripristino**

1.  Nella pagina **Opzioni avanzate** fare clic sulla scheda **WinPE** .

2.  Selezionare la casella di controllo accanto a ogni pacchetto che si vuole includere nell'immagine oppure fare clic sulla casella di controllo **nome** per selezionare tutti i pacchetti.

3.  Nel campo **spazio di Scratch** selezionare la quantità di spazio su disco RAM da allocare per l'uso di freccette nel caso in cui il disco rigido dell'utente finale non sia disponibile.

4.  Fai clic su **Avanti**.

## Aggiungere gli strumenti di debug per Crash Analyzer


Se si include lo strumento Analizzatore crash nell'immagine ISO, è necessario includere anche gli strumenti di debug per Windows. Nella scheda Analizzatore arresto anomalo della pagina Opzioni avanzate Immetti il percorso degli strumenti di debug di Windows 10, che analizza Crash Analyzer USA per analizzare i file di dump della memoria. È possibile usare gli strumenti presenti nel computer in cui è in uso la creazione guidata immagine di ripristino di freccette oppure usare gli strumenti presenti nel computer dell'utente finale. Se si decide di usare gli strumenti nel computer dell'utente finale, tenere presente che tutti i computer diagnosticati devono disporre degli strumenti di debug installati.

Se è stato installato Microsoft Windows Software Development Kit (SDK) o Microsoft Windows Development Kit (WDK), gli strumenti di debug di Windows 10 vengono aggiunti all'immagine di ripristino per impostazione predefinita e il percorso degli strumenti di debug viene compilato automaticamente. È possibile modificare il percorso degli strumenti di debug di Windows 10 se i file si trovano in un punto diverso da quello indicato dal percorso predefinito del file. Un collegamento nella procedura guidata consente di scaricare e installare gli strumenti di debug per Windows, se non sono già installati.

Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=266248). Installare gli strumenti di debug nella posizione predefinita.

**Nota**  La procedura guidata DaRT controlla gli strumenti nella `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` chiave del registro di sistema. Se il valore del registro di sistema non è presente, la procedura guidata verrà eseguita in una delle posizioni seguenti, a seconda dell'architettura di sistemi:

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**Per aggiungere gli strumenti di debug per Crash Analyzer**

1.  Nella pagina **Opzioni avanzate** fare clic sulla scheda **analizzatore crash** .

2.  Opzionale Fare clic su **Scarica gli strumenti di debug** per scaricare gli strumenti di debug per Windows.

3.  Selezionare una delle opzioni seguenti:

    -   **Includere gli strumenti di debug di Windows 10 &lt; 64 bit o &gt; 32**. Se si seleziona questa opzione, individuare e selezionare la posizione degli strumenti se il percorso non è già visualizzato.

    -   **Usare gli strumenti di debug del sistema di cui si sta**eseguendo il debugger. Se si seleziona questa opzione, l'analizzatore crash non funzionerà se gli strumenti di debug per Windows non vengono trovati nel computer problema.

4.  Fai clic su **Avanti**.

## Selezionare i tipi di file di immagine di ripristino da creare


Nella pagina Crea immagine Scegli una cartella di output per l'immagine di ripristino, immetti un nome di immagine e seleziona i tipi di file di immagine di recupero DaRT da creare. Durante il processo di creazione di immagini di ripristino, i file di origine di Windows vengono spacchettati, i file di freccette vengono copiati e l'immagine viene quindi "reimballata" nei formati di file selezionati in questa pagina.

I tipi di file immagine disponibili sono:

-   **File Windows Imaging (wim)** : consente di distribuire il dardo in un ambiente PXE (Preboot Execution Environment) o in una partizione locale.

-   **ISO (International Standards Organization)** : usato per la distribuzione su CD o DVD oppure per l'uso in macchine virtuali (VM). La procedura guidata richiede che l'immagine ISO abbia un'estensione di file ISO, perché la maggior parte dei programmi che masterizzano un CD o un DVD richiedono tale estensione. Se non specifichi una posizione diversa, l'immagine ISO viene creata sul desktop con il nome DaRT10. ISO.

-   **Script di PowerShell** : crea un'immagine di ripristino DaRT con comandi che contengono essenzialmente le stesse opzioni che puoi selezionare usando la creazione guidata immagine di ripristino DaRT. Lo script consente inoltre di aggiungere o modificare i file nell'immagine di ripristino delle freccette.

Se si seleziona la casella di controllo modifica immagine in questa pagina, è possibile personalizzare l'immagine di ripristino durante il processo di creazione delle immagini. Ad esempio, è possibile modificare il file "winpeshl.ini" per creare un ordine di avvio personalizzato o per aggiungere strumenti di terze parti.

**Per selezionare i tipi di file di immagine di ripristino da creare**

1.  Nella pagina **Crea immagine** fare clic su **Sfoglia** per scegliere la cartella di output per il file di immagine.

    **Nota**  Le dimensioni dell'immagine variano a seconda degli strumenti selezionati e dei file che si aggiungono nella procedura guidata.

     

2.  Nella casella **nome immagine** immettere un nome per l'immagine di ripristino DaRT o accettare il nome predefinito, ovvero DaRT10.

    La procedura guidata crea una sottocartella nel percorso di output con questo nome.

3.  Selezionare i tipi di file di immagine che si desidera creare.

4.  Scegliere una delle opzioni seguenti:

    -   Per modificare i file nell'immagine di ripristino prima di creare i file di immagine, selezionare la casella di controllo **modifica immagine** e quindi fare clic su **prepara**.

    -   Per creare l'immagine di ripristino senza modificare i file, fare clic su **Crea**.

5.  

    Fai clic su **Avanti**.

## Modificare i file di immagine di ripristino


È possibile modificare l'immagine di ripristino solo se è stata selezionata la casella di controllo modifica immagine nella pagina Crea immagine. Dopo aver preparato l'immagine di ripristino per la modifica, è possibile aggiungere e modificare i file di immagine di ripristino prima di creare il supporto di avvio. Ad esempio, puoi creare un ordine personalizzato per l'avvio, aggiungere vari strumenti di terze parti e così via.

**Per modificare i file di immagine di ripristino**

1.  Nella pagina **modifica immagine** fare clic su **Apri** in Esplora risorse.

2.  Creare una sottocartella nella cartella elencata nella finestra di dialogo.

3.  Copiare i file desiderati nella nuova sottocartella oppure rimuovere i file che non si desidera.

4.  Fare clic su **Crea** per iniziare a creare l'immagine di ripristino.

## Generare i file di immagine di ripristino


Nella pagina genera file viene generata l'immagine di ripristino DaRT per i tipi di file selezionati nella pagina Crea immagine.

**Per generare i file di immagine di ripristino**

-   Nella pagina **genera file** fare clic su **Avanti** per generare i file di immagine di ripristino.

## Copiare l'immagine di ripristino in un CD, un DVD o un USB


Nella pagina Crea supporto avviabile è possibile copiare facoltativamente il file di immagine in un CD, un DVD o un'unità flash USB. È anche possibile creare altri elementi multimediali avviabili da questa pagina riavviando la procedura guidata.

**Nota**  Il programma PXE (Preboot Execution Environment) e la distribuzione di immagini locali non sono supportati in modo nativo da questo strumento, poiché richiedono strumenti aziendali aggiuntivi, ad esempio System Center Configuration Manager Server e Microsoft Development Toolkit.

 

**Per copiare l'immagine di ripristino in un CD, un DVD o un USB**

1.  Nella pagina **Crea supporto avviabile** selezionare il file ISO che si vuole copiare.

2.  Inserire un CD, un DVD o un USB e quindi selezionare l'unità.

    **Nota**  Se un'unità non viene riconosciuta e si installa una nuova unità, è possibile fare clic su **Aggiorna** per forzare la procedura guidata ad aggiornare l'elenco delle unità disponibili.

     

3.  Fare clic sul pulsante **Crea supporto avviabile** .

4.  Per creare un'altra immagine di ripristino, fare clic su Riavvia oppure su **Chiudi** se è stata completata la creazione di tutto il contenuto multimediale desiderato.

## Argomenti correlati


[Panoramica degli strumenti di DaRT 10](overview-of-the-tools-in-dart-10.md)

[Distribuzione di DaRT 10](deploying-dart-10.md)

 

 





