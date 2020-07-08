---
title: Distribuzione dell'immagine di ripristino di DaRT
description: Distribuzione dell'immagine di ripristino di DaRT
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824115"
---
# Distribuzione dell'immagine di ripristino di DaRT


Dopo aver creato il file ISO (International Organization for Standardizzation) che contiene l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, è possibile distribuire l'immagine di ripristino di DaRT 8,0 in tutta l'organizzazione in modo che sia disponibile per gli utenti finali e gli addetti al supporto tecnico. Esistono quattro metodi supportati che è possibile usare per distribuire l'immagine di ripristino delle freccette. Per esaminare i vantaggi e gli svantaggi di ogni metodo, vedere [pianificazione della procedura per salvare e distribuire l'immagine di ripristino di DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

Masterizzare il file di immagine ISO in un CD o un DVD usando la creazione guidata immagine di ripristino di freccette

Salvare il contenuto del file di immagine ISO in un'unità flash USB tramite la creazione guidata immagine di ripristino di freccette

Estrarre il file Boot. wim dall'immagine ISO e distribuirlo come partizione remota disponibile per i computer degli utenti finali

Estrarre il file Boot. wim dall'immagine ISO e distribuirlo nella partizione di ripristino di una nuova installazione di Windows 8

**Importante**  La **creazione guidata immagine di ripristino DaRT** offre la possibilità di masterizzare l'immagine in un CD, un DVD o un'unità flash USB, ma gli altri metodi di salvataggio e distribuzione dell'immagine di ripristino richiedono ulteriori passaggi che coinvolgono strumenti non inclusi in DART. In questa sezione sono disponibili alcune linee guida e collegamenti per questi altri metodi.

 

## Distribuire l'immagine di ripristino delle freccette come parte di una partizione di ripristino


Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 8.

[Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## Distribuire l'immagine di ripristino delle freccette come partizione remota


È possibile ospitare l'immagine di ripristino in un server di avvio di rete centrale, ad esempio servizi di distribuzione Windows, e consentire agli utenti o al personale di supporto di trasmettere l'immagine a computer su richiesta.

[Come distribuire l'immagine di ripristino di DaRT come partizione remota](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## Altre risorse per la distribuzione dell'immagine di ripristino DaRT


[Distribuzione di DaRT 8.0](deploying-dart-80-dart-8.md)

 

 





