---
title: Distribuzione dell'immagine di ripristino di DaRT
description: Distribuzione dell'immagine di ripristino di DaRT
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804737"
---
# Distribuzione dell'immagine di ripristino di DaRT


Dopo aver creato il file ISO (International Organization for Standardizzation) che contiene l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10, è possibile distribuire l'immagine di ripristino di DaRT 10 in tutta l'organizzazione in modo che sia disponibile per gli utenti finali e gli addetti al supporto tecnico. Esistono quattro metodi supportati che è possibile usare per distribuire l'immagine di ripristino delle freccette. Per esaminare i vantaggi e gli svantaggi di ogni metodo, vedere [pianificazione della procedura per salvare e distribuire l'immagine di ripristino di Dart 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).

Masterizzare il file di immagine ISO in un CD o un DVD usando la creazione guidata immagine di ripristino di freccette

Salvare il contenuto del file di immagine ISO in un'unità flash USB tramite la creazione guidata immagine di ripristino di freccette

Estrarre il file Boot. wim dall'immagine ISO e distribuirlo come partizione remota disponibile per i computer degli utenti finali

Estrarre il file Boot. wim dall'immagine ISO e distribuirlo nella partizione di ripristino di una nuova installazione di Windows 10

**Importante**  La **creazione guidata immagine di ripristino DaRT** offre la possibilità di masterizzare l'immagine in un CD, un DVD o un'unità flash USB, ma gli altri metodi di salvataggio e distribuzione dell'immagine di ripristino richiedono ulteriori passaggi che coinvolgono strumenti non inclusi in DART. In questa sezione sono disponibili alcune linee guida e collegamenti per questi altri metodi.

 

## Distribuire l'immagine di ripristino delle freccette come parte di una partizione di ripristino


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 10.

[Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## Distribuire l'immagine di ripristino delle freccette come partizione remota


È possibile ospitare l'immagine di ripristino in un server di avvio di rete centrale, ad esempio servizi di distribuzione Windows, e consentire agli utenti o al personale di supporto di trasmettere l'immagine a computer su richiesta.

[Come distribuire l'immagine di ripristino di DaRT come partizione remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## Altre risorse per la distribuzione dell'immagine di ripristino DaRT


[Distribuzione di DaRT 10](deploying-dart-10.md)

 

 





