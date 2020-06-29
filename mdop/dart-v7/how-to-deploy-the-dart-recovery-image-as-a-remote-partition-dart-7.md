---
title: Come distribuire l'immagine di ripristino di DaRT come partizione remota
description: Come distribuire l'immagine di ripristino di DaRT come partizione remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823566"
---
# <span data-ttu-id="8717e-103">Come distribuire l'immagine di ripristino di DaRT come partizione remota</span><span class="sxs-lookup"><span data-stu-id="8717e-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="8717e-104">Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="8717e-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="8717e-105">Per distribuire il dardo come partizione remota</span><span class="sxs-lookup"><span data-stu-id="8717e-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="8717e-106">Estrarre il file Boot. wim dal file di immagine ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="8717e-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="8717e-107">Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8717e-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="8717e-108">Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.</span><span class="sxs-lookup"><span data-stu-id="8717e-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="8717e-109">**Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources.</span><span class="sxs-lookup"><span data-stu-id="8717e-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="8717e-110">In questo modo è possibile ignorare la necessità di montare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8717e-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="8717e-111">Distribuire il file Boot. wim in un server WDS a cui è possibile accedere dai computer degli utenti finali dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8717e-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="8717e-112">Configurare il server WDS per usare il file Boot. wim per DaRT seguendo le procedure di distribuzione di WDS standard.</span><span class="sxs-lookup"><span data-stu-id="8717e-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="8717e-113">Per altre informazioni su come distribuire il dardo come partizione remota, vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="8717e-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="8717e-114">Procedura dettagliata: distribuire un'immagine tramite PXE</span><span class="sxs-lookup"><span data-stu-id="8717e-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="8717e-115">Guida introduttiva di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="8717e-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="8717e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8717e-116">Related topics</span></span>


[<span data-ttu-id="8717e-117">Distribuzione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8717e-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





