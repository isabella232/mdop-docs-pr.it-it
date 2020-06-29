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
# <span data-ttu-id="a0ec4-103">Come creare un'immagine di ripristino con una durata limitata</span><span class="sxs-lookup"><span data-stu-id="a0ec4-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="a0ec4-104">È possibile creare un'immagine di ripristino delle freccette che può essere usata solo per un determinato numero di giorni dopo la generazione.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="a0ec4-105">A tale scopo, è necessario eseguire la **creazione guidata immagine di ripristino di freccette** al prompt dei comandi e specificare il numero di giorni.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="a0ec4-106">Per creare un'immagine di ripristino con un limite di tempo</span><span class="sxs-lookup"><span data-stu-id="a0ec4-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="a0ec4-107">Aprire un prompt dei comandi con le credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="a0ec4-108">Cambiare la directory nella posizione del programma ERDC.exe.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="a0ec4-109">Usando la sintassi seguente, Esegui la **creazione guidata immagine di ripristino di freccette**.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="a0ec4-110">*NumberOfDays* è un valore integer positivo che rappresenta il numero di giorni in cui l'immagine di ripristino DaRT sarà utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="a0ec4-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="a0ec4-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0ec4-111">Related topics</span></span>


[<span data-ttu-id="a0ec4-112">Creazione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a0ec4-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





