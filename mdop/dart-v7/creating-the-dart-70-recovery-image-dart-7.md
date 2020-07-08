---
title: Creazione dell'immagine di ripristino di DaRT 7.0
description: Creazione dell'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823285"
---
# Creazione dell'immagine di ripristino di DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include la **procedura guidata** per l'immagine di ripristino delle freccette usata in Windows per creare un'immagine dell'organizzazione internazionale per la standardizzazione (ISO) avviabile. Un'immagine ISO è un file che rappresenta il contenuto non elaborato di un CD.

## Usare la creazione guidata immagine di ripristino di freccette per creare l'immagine di ripristino


L'immagine ISO creata dalla creazione guidata immagine di ripristino di freccette contiene l'icona di ripristino delle freccette che consente di avviare un problema di computer, anche se non è possibile che venga avviata. Dopo aver avviato il computer in DaRT, puoi eseguire i diversi strumenti DaRT per provare a diagnosticare e ripristinare il computer.

È possibile scrivere l'ISO in un CD o un DVD registrabile, salvarlo in un'unità flash USB oppure salvarlo in un formato che può essere usato per l'avvio in freccette da una partizione remota o da una partizione di ripristino. Per altre informazioni, vedere [distribuzione dell'immagine di ripristino di DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

**Nota**  Se il computer include un'unità CD-RW, la procedura guidata offre di masterizzare l'immagine ISO in un CD o DVD vuoto. Se il computer in uso non include un'unità supportata dalla procedura guidata, è possibile masterizzare l'immagine ISO su un CD o un DVD usando la maggior parte dei programmi che possono masterizzare un CD o un DVD.

 

Per creare un CD o un DVD avviabile dall'immagine ISO, è necessario disporre di:

-   Un'unità CD-RW.

-   Un CD o un DVD registrabile (in un formato supportato dall'unità registrabile).

-   Software che supporta l'unità registrabile e supporta la masterizzazione di un'immagine ISO direttamente su CD o DVD.

    **Importante**  Testare il CD o il DVD creato in tutti i diversi tipi di computer che si desidera supportare perché alcuni computer non possono iniziare da qualsiasi tipo di elemento multimediale registrabile.

     

Per salvare l'immagine ISO in un'unità flash USB, è necessario disporre di:

-   Un'unità flash USB formattata correttamente.

-   Un programma che è possibile usare per montare l'immagine ISO.

[Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## Creare un'immagine di ripristino a tempo limitato


È possibile creare un'immagine di ripristino delle freccette che può essere usata solo per un determinato numero di giorni dopo la generazione. A tale scopo, è necessario eseguire la **creazione guidata immagine di ripristino di freccette** al prompt dei comandi e specificare il numero di giorni.

[Come creare un'immagine di ripristino con una durata limitata](how-to-create-a-time-limited-recovery-image-dart-7.md)

## Altre risorse per creare l'immagine di ripristino di DaRT7


-   [Distribuzione di DaRT 7.0](deploying-dart-70-new-ia.md)

 

 





