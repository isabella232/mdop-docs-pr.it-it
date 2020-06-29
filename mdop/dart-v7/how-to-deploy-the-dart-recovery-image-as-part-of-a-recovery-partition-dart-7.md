---
title: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
description: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823556"
---
# <span data-ttu-id="97d9d-103">Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="97d9d-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="97d9d-104">Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97d9d-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="97d9d-105">Per distribuire il dardo nella partizione di ripristino di un'immagine di Windows 7</span><span class="sxs-lookup"><span data-stu-id="97d9d-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="97d9d-106">Creare una partizione di destinazione nell'immagine di Windows 7 uguale o maggiore della dimensione del file di immagine ISO creato tramite la **creazione guidata immagine di ripristino di Dart**.</span><span class="sxs-lookup"><span data-stu-id="97d9d-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="97d9d-107">Le dimensioni minime necessarie per una partizione DaRT sono approssimativamente 300MB.</span><span class="sxs-lookup"><span data-stu-id="97d9d-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="97d9d-108">Tuttavia, ti consigliamo di 450MB per la funzionalità di connessione remota in DaRT.</span><span class="sxs-lookup"><span data-stu-id="97d9d-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="97d9d-109">Estrarre il file Boot. wim dal file di immagine ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="97d9d-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="97d9d-110">Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="97d9d-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="97d9d-111">Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.</span><span class="sxs-lookup"><span data-stu-id="97d9d-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="97d9d-112">**Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources.</span><span class="sxs-lookup"><span data-stu-id="97d9d-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="97d9d-113">In questo modo è possibile ignorare la necessità di montare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="97d9d-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="97d9d-114">Usa il file Boot. wim per creare una partizione di ripristino avviabile usando il metodo standard della società per la creazione di un'immagine ripristino personalizzata di Windows.</span><span class="sxs-lookup"><span data-stu-id="97d9d-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="97d9d-115">Per altre informazioni su come creare o personalizzare una partizione di ripristino, vedere [personalizzazione dell'esperienza Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="97d9d-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="97d9d-116">Sostituisci la partizione di destinazione nell'immagine di Windows 7 con la partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="97d9d-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="97d9d-117">Dopo che l'immagine di Windows 7 è pronta, distribuire l'immagine ai computer dell'organizzazione usando il processo di distribuzione delle immagini standard della società.</span><span class="sxs-lookup"><span data-stu-id="97d9d-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="97d9d-118">Per altre informazioni su come creare un'immagine di Windows 7, vedere [creazione di un'immagine standard di Windows 7: Guida dettagliata](https://go.microsoft.com/fwlink/?LinkId=212103).</span><span class="sxs-lookup"><span data-stu-id="97d9d-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="97d9d-119">Per altre informazioni su come distribuire una soluzione di ripristino per reinstallare l'immagine Factory in caso di errore di sistema, vedere [distribuire un'immagine di ripristino del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="97d9d-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="97d9d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97d9d-120">Related topics</span></span>


[<span data-ttu-id="97d9d-121">Distribuzione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="97d9d-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





