---
title: Distribuzione dell'immagine di ripristino di DaRT 7.0
description: Distribuzione dell'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804390"
---
# <span data-ttu-id="9e61e-103">Distribuzione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9e61e-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="9e61e-104">Dopo aver creato il file ISO (International Organization for Standardizzation) che contiene l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7, è possibile distribuire l'immagine di ripristino delle freccette in tutta l'organizzazione in modo che sia disponibile per gli utenti finali e gli agenti dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="9e61e-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="9e61e-105">Esistono quattro metodi supportati che è possibile usare per distribuire l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="9e61e-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="9e61e-106">Masterizzare il file di immagine ISO su un CD o un DVD</span><span class="sxs-lookup"><span data-stu-id="9e61e-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="9e61e-107">Salvare il contenuto del file di immagine ISO in un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="9e61e-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="9e61e-108">Estrarre il file Boot. wim dall'immagine ISO e distribuirlo come partizione remota disponibile per i computer degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="9e61e-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="9e61e-109">Estrarre il file Boot. wim dall'immagine ISO e distribuirlo nella partizione di ripristino di una nuova installazione di Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e61e-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="9e61e-110">**Importante**  La **Configurazione guidata immagine di ripristino DaRT** offre solo l'opzione per masterizzare un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="9e61e-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="9e61e-111">Tutti gli altri metodi per il salvataggio e la distribuzione dell'immagine di ripristino richiedono passaggi aggiuntivi che coinvolgono strumenti non inclusi in DaRT.</span><span class="sxs-lookup"><span data-stu-id="9e61e-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="9e61e-112">In questa sezione sono disponibili alcune linee guida e collegamenti per questi altri metodi.</span><span class="sxs-lookup"><span data-stu-id="9e61e-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="9e61e-113">Distribuire l'immagine di ripristino delle freccette usando un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="9e61e-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="9e61e-114">Dopo aver completato l'installazione guidata immagine di ripristino di freccette, è possibile usare lo strumento su <https://go.microsoft.com/fwlink/?LinkId=218888> per copiare il file di immagine ISO in un'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="9e61e-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="9e61e-115">Come distribuire l'immagine di ripristino di DaRT usando un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="9e61e-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="9e61e-116">Distribuire l'immagine di ripristino delle freccette come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="9e61e-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="9e61e-117">Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e61e-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="9e61e-118">Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="9e61e-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="9e61e-119">Distribuire l'immagine di ripristino delle freccette come partizione remota</span><span class="sxs-lookup"><span data-stu-id="9e61e-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="9e61e-120">Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="9e61e-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="9e61e-121">Come distribuire l'immagine di ripristino di DaRT come partizione remota</span><span class="sxs-lookup"><span data-stu-id="9e61e-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="9e61e-122">Altre risorse per la gestione della distribuzione dell'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="9e61e-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="9e61e-123">Distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9e61e-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





