---
title: Distribuzione dell'immagine di ripristino di DaRT
description: Distribuzione dell'immagine di ripristino di DaRT
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804737"
---
# <span data-ttu-id="400b6-103">Distribuzione dell'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="400b6-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="400b6-104">Dopo aver creato il file ISO (International Organization for Standardizzation) che contiene l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10, è possibile distribuire l'immagine di ripristino di DaRT 10 in tutta l'organizzazione in modo che sia disponibile per gli utenti finali e gli addetti al supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="400b6-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can deploy the DaRT 10 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="400b6-105">Esistono quattro metodi supportati che è possibile usare per distribuire l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="400b6-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="400b6-106">Per esaminare i vantaggi e gli svantaggi di ogni metodo, vedere [pianificazione della procedura per salvare e distribuire l'immagine di ripristino di Dart 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="400b6-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="400b6-107">Masterizzare il file di immagine ISO in un CD o un DVD usando la creazione guidata immagine di ripristino di freccette</span><span class="sxs-lookup"><span data-stu-id="400b6-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="400b6-108">Salvare il contenuto del file di immagine ISO in un'unità flash USB tramite la creazione guidata immagine di ripristino di freccette</span><span class="sxs-lookup"><span data-stu-id="400b6-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="400b6-109">Estrarre il file Boot. wim dall'immagine ISO e distribuirlo come partizione remota disponibile per i computer degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="400b6-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="400b6-110">Estrarre il file Boot. wim dall'immagine ISO e distribuirlo nella partizione di ripristino di una nuova installazione di Windows 10</span><span class="sxs-lookup"><span data-stu-id="400b6-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 10 installation</span></span>

<span data-ttu-id="400b6-111">**Importante**  La **creazione guidata immagine di ripristino DaRT** offre la possibilità di masterizzare l'immagine in un CD, un DVD o un'unità flash USB, ma gli altri metodi di salvataggio e distribuzione dell'immagine di ripristino richiedono ulteriori passaggi che coinvolgono strumenti non inclusi in DART.</span><span class="sxs-lookup"><span data-stu-id="400b6-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="400b6-112">In questa sezione sono disponibili alcune linee guida e collegamenti per questi altri metodi.</span><span class="sxs-lookup"><span data-stu-id="400b6-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="400b6-113">Distribuire l'immagine di ripristino delle freccette come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="400b6-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="400b6-114">Dopo aver completato l'installazione guidata immagine di ripristino di freccette e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="400b6-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span>

[<span data-ttu-id="400b6-115">Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="400b6-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## <span data-ttu-id="400b6-116">Distribuire l'immagine di ripristino delle freccette come partizione remota</span><span class="sxs-lookup"><span data-stu-id="400b6-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="400b6-117">È possibile ospitare l'immagine di ripristino in un server di avvio di rete centrale, ad esempio servizi di distribuzione Windows, e consentire agli utenti o al personale di supporto di trasmettere l'immagine a computer su richiesta.</span><span class="sxs-lookup"><span data-stu-id="400b6-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="400b6-118">Come distribuire l'immagine di ripristino di DaRT come partizione remota</span><span class="sxs-lookup"><span data-stu-id="400b6-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## <span data-ttu-id="400b6-119">Altre risorse per la distribuzione dell'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="400b6-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="400b6-120">Distribuzione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="400b6-120">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 




