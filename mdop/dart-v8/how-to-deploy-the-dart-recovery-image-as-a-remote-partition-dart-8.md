---
title: Come distribuire l'immagine di ripristino di DaRT come partizione remota
description: Come distribuire l'immagine di ripristino di DaRT come partizione remota
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821266"
---
# Come distribuire l'immagine di ripristino di DaRT come partizione remota


Dopo aver eseguito la creazione guidata immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.

**Per distribuire il dardo 8,0 come partizione remota**

1.  Estrarre il file Boot. wim dal file di immagine ISO DaRT.

    1.  Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.

    2.  Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.

        **Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources. In questo modo è possibile ignorare la necessità di montare l'immagine.

         

2.  Distribuire il file Boot. wim in un server WDS a cui è possibile accedere dai computer degli utenti finali dell'organizzazione.

3.  Configurare il server WDS per usare il file Boot. wim per DaRT seguendo le procedure di distribuzione di WDS standard.

Per altre informazioni su come distribuire il dardo come partizione remota, vedere [procedura dettagliata: distribuire un'immagine usando la](https://go.microsoft.com/fwlink/?LinkId=212108) [Guida introduttiva di servizi di distribuzione](https://go.microsoft.com/fwlink/?LinkId=212106)di PXE e Windows.

## Argomenti correlati


[Creazione dell'immagine di ripristino di DaRT 8.0](creating-the-dart-80-recovery-image-dart-8.md)

[Distribuzione dell'immagine di ripristino di DaRT](deploying-the-dart-recovery-image-dart-8.md)

[Pianificazione di DaRT 8.0](planning-for-dart-80-dart-8.md)

 

 





