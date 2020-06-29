---
title: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
description: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823556"
---
# Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 7.

**Per distribuire il dardo nella partizione di ripristino di un'immagine di Windows 7**

1.  Creare una partizione di destinazione nell'immagine di Windows 7 uguale o maggiore della dimensione del file di immagine ISO creato tramite la **creazione guidata immagine di ripristino di Dart**.

    Le dimensioni minime necessarie per una partizione DaRT sono approssimativamente 300MB. Tuttavia, ti consigliamo di 450MB per la funzionalità di connessione remota in DaRT.

2.  Estrarre il file Boot. wim dal file di immagine ISO DaRT.

    1.  Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.

    2.  Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.

        **Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources. In questo modo è possibile ignorare la necessità di montare l'immagine.

         

3.  Usa il file Boot. wim per creare una partizione di ripristino avviabile usando il metodo standard della società per la creazione di un'immagine ripristino personalizzata di Windows.

    Per altre informazioni su come creare o personalizzare una partizione di ripristino, vedere [personalizzazione dell'esperienza Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Sostituisci la partizione di destinazione nell'immagine di Windows 7 con la partizione di ripristino.

Dopo che l'immagine di Windows 7 è pronta, distribuire l'immagine ai computer dell'organizzazione usando il processo di distribuzione delle immagini standard della società. Per altre informazioni su come creare un'immagine di Windows 7, vedere [creazione di un'immagine standard di Windows 7: Guida dettagliata](https://go.microsoft.com/fwlink/?LinkId=212103).

Per altre informazioni su come distribuire una soluzione di ripristino per reinstallare l'immagine Factory in caso di errore di sistema, vedere [distribuire un'immagine di ripristino del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Argomenti correlati


[Distribuzione dell'immagine di ripristino di DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





