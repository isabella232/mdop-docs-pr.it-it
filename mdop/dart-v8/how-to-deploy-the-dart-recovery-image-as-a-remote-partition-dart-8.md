---
title: Come distribuire l'immagine di ripristino di DaRT come partizione remota
description: Come distribuire l'immagine di ripristino di DaRT come partizione remota
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821266"
---
# <span data-ttu-id="3da16-103">Come distribuire l'immagine di ripristino di DaRT come partizione remota</span><span class="sxs-lookup"><span data-stu-id="3da16-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="3da16-104">Dopo aver eseguito la creazione guidata immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="3da16-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="3da16-105">Per distribuire il dardo 8,0 come partizione remota</span><span class="sxs-lookup"><span data-stu-id="3da16-105">To deploy DaRT 8.0 as a remote partition</span></span>**

1.  <span data-ttu-id="3da16-106">Estrarre il file Boot. wim dal file di immagine ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="3da16-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="3da16-107">Montare il file di immagine ISO creato nella finestra di dialogo **Crea immagine di avvio** usando il metodo preferito della società per il montaggio di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="3da16-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="3da16-108">Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.</span><span class="sxs-lookup"><span data-stu-id="3da16-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="3da16-109">**Nota**  Se si è masterizzato un CD o un DVD dell'immagine di ripristino, è possibile aprire i file nel CD o nel DVD e copiare il file Boot. wim dalla cartella \\sources.</span><span class="sxs-lookup"><span data-stu-id="3da16-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="3da16-110">In questo modo è possibile ignorare la necessità di montare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3da16-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="3da16-111">Distribuire il file Boot. wim in un server WDS a cui è possibile accedere dai computer degli utenti finali dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="3da16-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="3da16-112">Configurare il server WDS per usare il file Boot. wim per DaRT seguendo le procedure di distribuzione di WDS standard.</span><span class="sxs-lookup"><span data-stu-id="3da16-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="3da16-113">Per altre informazioni su come distribuire il dardo come partizione remota, vedere [procedura dettagliata: distribuire un'immagine usando la](https://go.microsoft.com/fwlink/?LinkId=212108) [Guida introduttiva di servizi di distribuzione](https://go.microsoft.com/fwlink/?LinkId=212106)di PXE e Windows.</span><span class="sxs-lookup"><span data-stu-id="3da16-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="3da16-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3da16-114">Related topics</span></span>


[<span data-ttu-id="3da16-115">Creazione dell'immagine di ripristino di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3da16-115">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="3da16-116">Distribuzione dell'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="3da16-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="3da16-117">Pianificazione di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3da16-117">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 




