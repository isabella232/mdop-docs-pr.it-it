---
title: Distribuzione dell'immagine di ripristino di DaRT 7.0
description: Distribuzione dell'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804390"
---
# Distribuzione dell'immagine di ripristino di DaRT 7.0


Dopo aver creato il file ISO (International Organization for Standardizzation) che contiene l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7, è possibile distribuire l'immagine di ripristino delle freccette in tutta l'organizzazione in modo che sia disponibile per gli utenti finali e gli agenti dell'helpdesk. Esistono quattro metodi supportati che è possibile usare per distribuire l'immagine di ripristino delle freccette.

-   Masterizzare il file di immagine ISO su un CD o un DVD

-   Salvare il contenuto del file di immagine ISO in un'unità flash USB

-   Estrarre il file Boot. wim dall'immagine ISO e distribuirlo come partizione remota disponibile per i computer degli utenti finali

-   Estrarre il file Boot. wim dall'immagine ISO e distribuirlo nella partizione di ripristino di una nuova installazione di Windows 7

**Importante**  La **Configurazione guidata immagine di ripristino DaRT** offre solo l'opzione per masterizzare un CD o un DVD. Tutti gli altri metodi per il salvataggio e la distribuzione dell'immagine di ripristino richiedono passaggi aggiuntivi che coinvolgono strumenti non inclusi in DaRT. In questa sezione sono disponibili alcune linee guida e collegamenti per questi altri metodi.

 

## Distribuire l'immagine di ripristino delle freccette usando un'unità flash USB


Dopo aver completato l'installazione guidata immagine di ripristino di freccette, è possibile usare lo strumento su <https://go.microsoft.com/fwlink/?LinkId=218888> per copiare il file di immagine ISO in un'unità flash USB.

[Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## Distribuire l'immagine di ripristino delle freccette come parte di una partizione di ripristino


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 7.

[Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## Distribuire l'immagine di ripristino delle freccette come partizione remota


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.

[Come distribuire l'immagine di ripristino di DaRT come partizione remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## Altre risorse per la gestione della distribuzione dell'immagine di ripristino delle freccette


-   [Distribuzione di DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





