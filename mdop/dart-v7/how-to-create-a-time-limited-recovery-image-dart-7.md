---
title: Come creare un'immagine di ripristino con una durata limitata
description: Come creare un'immagine di ripristino con una durata limitata
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804372"
---
# Come creare un'immagine di ripristino con una durata limitata


È possibile creare un'immagine di ripristino delle freccette che può essere usata solo per un determinato numero di giorni dopo la generazione. A tale scopo, è necessario eseguire la **creazione guidata immagine di ripristino di freccette** al prompt dei comandi e specificare il numero di giorni.

**Per creare un'immagine di ripristino con un limite di tempo**

1.  Aprire un prompt dei comandi con le credenziali di amministratore.

2.  Cambiare la directory nella posizione del programma ERDC.exe.

3.  Usando la sintassi seguente, Esegui la **creazione guidata immagine di ripristino di freccette**. *NumberOfDays* è un valore integer positivo che rappresenta il numero di giorni in cui l'immagine di ripristino DaRT sarà utilizzabile.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## Argomenti correlati


[Creazione dell'immagine di ripristino di DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





