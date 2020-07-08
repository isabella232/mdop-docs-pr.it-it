---
title: Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB
description: Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823666"
---
# Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB


Dopo aver completato l' **installazione guidata immagine di ripristino di freccette**, è possibile usare lo strumento su <https://go.microsoft.com/fwlink/?LinkId=218888> per copiare il file di immagine ISO in un'unità flash USB.

È anche possibile copiare manualmente il file di immagine ISO in un'unità flash USB seguendo i passaggi descritti in questa sezione.

**Per salvare l'immagine di ripristino delle freccette in un'unità flash USB**

1.  Formattare l'unità flash USB.

    1.  In un sistema operativo valido o una sessione WindowsPE in uso, inserire l'unità flash USB.

    2.  Al prompt dei comandi con autorizzazioni di amministratore digitare **DiskPart** e quindi digitare **elenco disco**.

        Nella finestra del prompt dei comandi viene visualizzato il numero di disco dell'unità flash USB, ad esempio il **disco 1**.

    3.  Immettere i comandi seguenti uno alla volta al prompt dei comandi.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **Nota**  L'esempio di codice precedente presuppone che disk1 sia l'unità flash USB. Se necessario, sostituire il disco 1 con il numero di disco.

         

2.  Usando il metodo preferito della società per il montaggio di un'immagine, montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** della **procedura guidata**per l'immagine di ripristino delle freccette. Per questo è necessario disporre di un metodo disponibile per montare un file di immagine.

3.  Aprire il file di immagine ISO montato e copiare tutto il contenuto nell'unità flash USB formattata.

    **Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il contenuto nell'unità flash USB. In questo modo è possibile ignorare la necessità di montare l'immagine.

     

## Argomenti correlati


[Distribuzione dell'immagine di ripristino di DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





