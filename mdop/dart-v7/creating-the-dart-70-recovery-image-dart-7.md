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
# <span data-ttu-id="70a26-103">Creazione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="70a26-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="70a26-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include la **procedura guidata** per l'immagine di ripristino delle freccette usata in Windows per creare un'immagine dell'organizzazione internazionale per la standardizzazione (ISO) avviabile.</span><span class="sxs-lookup"><span data-stu-id="70a26-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="70a26-105">Un'immagine ISO è un file che rappresenta il contenuto non elaborato di un CD.</span><span class="sxs-lookup"><span data-stu-id="70a26-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="70a26-106">Usare la creazione guidata immagine di ripristino di freccette per creare l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="70a26-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="70a26-107">L'immagine ISO creata dalla creazione guidata immagine di ripristino di freccette contiene l'icona di ripristino delle freccette che consente di avviare un problema di computer, anche se non è possibile che venga avviata.</span><span class="sxs-lookup"><span data-stu-id="70a26-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="70a26-108">Dopo aver avviato il computer in DaRT, puoi eseguire i diversi strumenti DaRT per provare a diagnosticare e ripristinare il computer.</span><span class="sxs-lookup"><span data-stu-id="70a26-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="70a26-109">È possibile scrivere l'ISO in un CD o un DVD registrabile, salvarlo in un'unità flash USB oppure salvarlo in un formato che può essere usato per l'avvio in freccette da una partizione remota o da una partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="70a26-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="70a26-110">Per altre informazioni, vedere [distribuzione dell'immagine di ripristino di DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="70a26-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="70a26-111">**Nota**  Se il computer include un'unità CD-RW, la procedura guidata offre di masterizzare l'immagine ISO in un CD o DVD vuoto.</span><span class="sxs-lookup"><span data-stu-id="70a26-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="70a26-112">Se il computer in uso non include un'unità supportata dalla procedura guidata, è possibile masterizzare l'immagine ISO su un CD o un DVD usando la maggior parte dei programmi che possono masterizzare un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="70a26-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="70a26-113">Per creare un CD o un DVD avviabile dall'immagine ISO, è necessario disporre di:</span><span class="sxs-lookup"><span data-stu-id="70a26-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="70a26-114">Un'unità CD-RW.</span><span class="sxs-lookup"><span data-stu-id="70a26-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="70a26-115">Un CD o un DVD registrabile (in un formato supportato dall'unità registrabile).</span><span class="sxs-lookup"><span data-stu-id="70a26-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="70a26-116">Software che supporta l'unità registrabile e supporta la masterizzazione di un'immagine ISO direttamente su CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="70a26-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="70a26-117">**Importante**  Testare il CD o il DVD creato in tutti i diversi tipi di computer che si desidera supportare perché alcuni computer non possono iniziare da qualsiasi tipo di elemento multimediale registrabile.</span><span class="sxs-lookup"><span data-stu-id="70a26-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="70a26-118">Per salvare l'immagine ISO in un'unità flash USB, è necessario disporre di:</span><span class="sxs-lookup"><span data-stu-id="70a26-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="70a26-119">Un'unità flash USB formattata correttamente.</span><span class="sxs-lookup"><span data-stu-id="70a26-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="70a26-120">Un programma che è possibile usare per montare l'immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="70a26-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="70a26-121">Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="70a26-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="70a26-122">Creare un'immagine di ripristino a tempo limitato</span><span class="sxs-lookup"><span data-stu-id="70a26-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="70a26-123">È possibile creare un'immagine di ripristino delle freccette che può essere usata solo per un determinato numero di giorni dopo la generazione.</span><span class="sxs-lookup"><span data-stu-id="70a26-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="70a26-124">A tale scopo, è necessario eseguire la **creazione guidata immagine di ripristino di freccette** al prompt dei comandi e specificare il numero di giorni.</span><span class="sxs-lookup"><span data-stu-id="70a26-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="70a26-125">Come creare un'immagine di ripristino con una durata limitata</span><span class="sxs-lookup"><span data-stu-id="70a26-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="70a26-126">Altre risorse per creare l'immagine di ripristino di DaRT7</span><span class="sxs-lookup"><span data-stu-id="70a26-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="70a26-127">Distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="70a26-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





