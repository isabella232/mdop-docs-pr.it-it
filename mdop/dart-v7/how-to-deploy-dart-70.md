---
title: Come distribuire DaRT 7.0
description: Come distribuire DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804684"
---
# Come distribuire DaRT 7.0


Questo argomento fornisce istruzioni per distribuire Microsoft Diagnostics and Recovery Toolset (DaRT) 7 nell'ambiente. La prima procedura in questo argomento presuppone che si stiano installando tutte le funzionalità in un computer amministratore. Quando è necessario distribuire o disinstallare il dardo in più computer usando un sistema di distribuzione elettronica del software, ad esempio, potrebbe essere più semplice usare le opzioni di installazione della riga di comando. Queste opzioni sono definite nella seconda procedura descritta in questo argomento che fornisce l'utilizzo di esempio per le opzioni della riga di comando disponibili.

**Importante**  Prima di installare DaRT, assicurati che il computer soddisfi i requisiti minimi di sistema elencati nelle [configurazioni supportate di dart 7,0](dart-70-supported-configurations-dart-7.md).

 

**Per installare il dardo in un computer amministratore**

1.  Individuare i file di installazione di DaRT ricevuti come parte del download del software.

2.  Fare doppio clic sul file di installazione di DaRT che corrisponde ai requisiti di sistema, ovvero 32 bit o 64 bit. Il file di installazione di DaRT è denominato **MSDaRT70.msi**.

3.  Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.

4.  Selezionare la cartella di destinazione per l'installazione di DaRT, selezionare se il dardo deve essere installato per tutti gli utenti o solo per l'utente corrente e quindi fare clic su **Avanti**.

5.  Selezionare se l'installazione deve essere **tipica**, **personalizzata**o **completa**e quindi fare clic su **Avanti**.

    -   **Tipico** installa gli strumenti usati più di frequente. Questo metodo è consigliato per la maggior parte degli utenti.

    -   **Personalizzato** consente di selezionare gli strumenti installati e dove verranno installati. Questo è consigliato per gli utenti avanzati, soprattutto se stai installando diversi strumenti DaRT in diversi computer dell'helpdesk.

    -   **Completa** installa tutti gli strumenti DART e richiede la maggior parte dello spazio su disco.

    Dopo aver selezionato il metodo di installazione, fare clic su **Avanti**.

6.  Per avviare l'installazione, fare clic su **Installa**.

7.  Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.

**Per installare il dardo al prompt dei comandi**

1.  L'esempio seguente mostra come installare tutte le funzionalità dardo.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  L'esempio seguente mostra come installare solo la **creazione guidata immagine di ripristino di freccette**.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  L'esempio seguente mostra come installare solo l'analizzatore crash e il Visualizzatore di connessioni remote DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  L'esempio seguente crea un log di configurazione per Windows Installer. Questa operazione è utile per il debug.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**Nota**  Puoi aggiungere/qn o/qb alle opzioni del prompt dei comandi per l'installazione di DaRT per eseguire un'installazione invisibile all'utente.

 

## Argomenti correlati


[Distribuzione di DaRT 7.0 nei computer di amministrazione](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





