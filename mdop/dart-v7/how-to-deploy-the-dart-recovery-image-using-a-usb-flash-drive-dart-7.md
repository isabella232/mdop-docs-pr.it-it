---
title: Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB
description: Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823666"
---
# <span data-ttu-id="70ca8-103">Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="70ca8-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="70ca8-104">Dopo aver completato l' **installazione guidata immagine di ripristino di freccette**, è possibile usare lo strumento su <https://go.microsoft.com/fwlink/?LinkId=218888> per copiare il file di immagine ISO in un'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="70ca8-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="70ca8-105">È anche possibile copiare manualmente il file di immagine ISO in un'unità flash USB seguendo i passaggi descritti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="70ca8-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="70ca8-106">Per salvare l'immagine di ripristino delle freccette in un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="70ca8-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="70ca8-107">Formattare l'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="70ca8-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="70ca8-108">In un sistema operativo valido o una sessione WindowsPE in uso, inserire l'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="70ca8-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="70ca8-109">Al prompt dei comandi con autorizzazioni di amministratore digitare **DiskPart** e quindi digitare **elenco disco**.</span><span class="sxs-lookup"><span data-stu-id="70ca8-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="70ca8-110">Nella finestra del prompt dei comandi viene visualizzato il numero di disco dell'unità flash USB, ad esempio il **disco 1**.</span><span class="sxs-lookup"><span data-stu-id="70ca8-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="70ca8-111">Immettere i comandi seguenti uno alla volta al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="70ca8-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="70ca8-112">**Nota**  L'esempio di codice precedente presuppone che disk1 sia l'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="70ca8-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="70ca8-113">Se necessario, sostituire il disco 1 con il numero di disco.</span><span class="sxs-lookup"><span data-stu-id="70ca8-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="70ca8-114">Usando il metodo preferito della società per il montaggio di un'immagine, montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** della **procedura guidata**per l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="70ca8-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="70ca8-115">Per questo è necessario disporre di un metodo disponibile per montare un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="70ca8-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="70ca8-116">Aprire il file di immagine ISO montato e copiare tutto il contenuto nell'unità flash USB formattata.</span><span class="sxs-lookup"><span data-stu-id="70ca8-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="70ca8-117">**Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il contenuto nell'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="70ca8-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="70ca8-118">In questo modo è possibile ignorare la necessità di montare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="70ca8-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="70ca8-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70ca8-119">Related topics</span></span>


[<span data-ttu-id="70ca8-120">Distribuzione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="70ca8-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





