---
title: Come distribuire DaRT 8.0
description: Come distribuire DaRT 8.0
author: dansimp
ms.assetid: ab772e7a-c02f-4847-acdf-8bd362769a77
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e7d64297f7687ebc0a23add3aa749ee4719beee4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824296"
---
# Come distribuire DaRT 8.0


Le istruzioni seguenti spiegano come distribuire Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 nell'ambiente. Per ottenere il software DaRT, Vedi [come ottenere MDOP](https://go.microsoft.com/fwlink/?LinkId=322049). Si presuppone che si stiano installando tutte le funzionalità in un computer amministratore. Se è necessario distribuire o disinstallare il dardo 8,0 in più computer, usando un sistema di distribuzione elettronica del software, ad esempio, potrebbe essere più semplice usare le opzioni di installazione della riga di comando. In questa sezione vengono fornite le descrizioni ed esempi delle opzioni della riga di comando disponibili.

**Importante**  Prima di installare dardo, vedere [configurazioni supportate di dart 8,0](dart-80-supported-configurations-dart-8.md) per assicurarsi di avere installato tutti i prerequisiti software e che il computer soddisfi i requisiti minimi di sistema. Il computer su cui si installa DaRT deve eseguire Windows 8 o Windows Server 2012.

 

È possibile installare DaRT usando una delle due diverse configurazioni:

-   Installare DaRT e tutti gli strumenti DaRT nel computer dell'amministratore.

-   Installare nel computer di amministrazione solo gli strumenti necessari per creare l'immagine di ripristino delle freccette e quindi installare il **Visualizzatore connessione remota** e, facoltativamente, **Crash Analyzer** in un computer dell'help desk.

Il file di installazione di DaRT è disponibile nelle versioni a 32 bit e 64 bit. Installare la versione che corrisponde all'architettura del computer in cui è in esecuzione la creazione guidata immagine di ripristino di freccette, non l'architettura del computer dell'immagine di ripristino che si sta creando.

È possibile usare una versione del file di installazione di DaRT per creare un'immagine di ripristino per i computer a 32 bit o a 64 bit, ma non è possibile creare un'immagine di ripristino per i computer a 32 bit e a 64 bit.

**Per installare freccette e tutti gli strumenti DaRT in un computer amministratore**

1.  Scaricare la versione a 32 bit o a bit 64 del file di installazione di DaRT 8,0. Scegliere l'architettura che corrisponde al computer in cui si sta installando DaRT ed eseguire la procedura guidata di ripristino delle immagini.

2.  Nella cartella in cui è stato scaricato dardo 8,0 eseguire il file di installazione **MSDaRT80.msi** che corrisponde ai requisiti di sistema.

3.  Nella pagina **Introduzione alla configurazione guidata di Microsoft DaRT 8,0** fare clic su **Avanti**.

4.  Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.

5.  Nella pagina **Microsoft Update** selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti**e quindi fare clic su **Avanti**.

6.  Nella pagina **selezionare la cartella di installazione** selezionare una cartella oppure fare clic su **Avanti** per installare il dardo nel percorso di installazione predefinito.

7.  Nella pagina **Opzioni di configurazione** selezionare le funzionalità DART che si vuole installare oppure fare clic su **Avanti** per installare Dart con tutte le funzionalità.

8.  Per avviare l'installazione, fare clic su **Installa**.

9.  Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.

## Per installare DaRT e tutti gli strumenti DaRT in un computer amministratore usando un prompt dei comandi


Quando si installa o si disinstalla il dardo, è possibile eseguire i file di installazione al prompt dei comandi. Questa sezione descrive alcuni esempi di opzioni diverse che è possibile specificare quando si installa o si disinstalla il dardo al prompt dei comandi.

L'esempio seguente mostra come installare tutte le funzionalità dardo.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

L'esempio seguente mostra come installare solo la creazione guidata immagine di ripristino di freccette.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

L'esempio seguente mostra come installare solo l'analizzatore crash e il Visualizzatore di connessioni remote DaRT.

``` syntax
msiexec /i MSDaRT80.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

L'esempio seguente crea un log di configurazione per Windows Installer. Questa operazione è utile per il debug.

``` syntax
msiexec.exe /i MSDaRT80.msi /l*v log.txt 
```

**Nota**  Puoi aggiungere/qn o/qb per eseguire un'installazione invisibile all'utente.

 

**Per convalidare l'installazione di DaRT**

1.  Fare clic sul pulsante **Start**e selezionare **strumenti di diagnostica e ripristino**.

    Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** .

2.  Verificare che tutti gli strumenti DaRT selezionati per l'installazione siano stati correttamente installati.

## Argomenti correlati


[Distribuzione di DaRT 8.0 nei computer di amministrazione](deploying-dart-80-to-administrator-computers-dart-8.md)

 

 





