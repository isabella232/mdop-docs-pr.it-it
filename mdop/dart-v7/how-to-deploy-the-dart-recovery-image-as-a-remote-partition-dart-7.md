---
title: Come distribuire l'immagine di ripristino di DaRT come partizione remota
description: Come distribuire l'immagine di ripristino di DaRT come partizione remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823566"
---
# Come distribuire l'immagine di ripristino di DaRT come partizione remota


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.

**Per distribuire il dardo come partizione remota**

1.  Estrarre il file Boot. wim dal file di immagine ISO DaRT.

    1.  Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.

    2.  Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.

        **Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources. In questo modo è possibile ignorare la necessità di montare l'immagine.

         

2.  Distribuire il file Boot. wim in un server WDS a cui è possibile accedere dai computer degli utenti finali dell'organizzazione.

3.  Configurare il server WDS per usare il file Boot. wim per DaRT seguendo le procedure di distribuzione di WDS standard.

Per altre informazioni su come distribuire il dardo come partizione remota, vedere quanto segue:

-   [Procedura dettagliata: distribuire un'immagine tramite PXE](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [Guida introduttiva di servizi di distribuzione Windows](https://go.microsoft.com/fwlink/?LinkId=212106)

## Argomenti correlati


[Distribuzione dell'immagine di ripristino di DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





