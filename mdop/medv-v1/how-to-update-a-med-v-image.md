---
title: Come aggiornare un'immagine MED-V
description: Come aggiornare un'immagine MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804270"
---
# <span data-ttu-id="3f78d-103">Come aggiornare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="3f78d-104">Come aggiornare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="3f78d-105">Un'immagine MED-V esistente può essere aggiornata, creando così una nuova versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="3f78d-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="3f78d-106">La nuova versione può quindi essere distribuita nei computer client, sostituendo l'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="3f78d-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="3f78d-107">**Nota**  Quando una nuova versione viene distribuita nel client, sovrascrive l'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="3f78d-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="3f78d-108">Quando si aggiorna un'immagine, assicurarsi che non sia necessario salvare dati nel client.</span><span class="sxs-lookup"><span data-stu-id="3f78d-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="3f78d-109">Per aggiornare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="3f78d-110">Aprire l'immagine esistente in Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="3f78d-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="3f78d-111">Apportare le modifiche necessarie all'immagine, aggiornando l'immagine, ad esempio l'installazione di un nuovo software.</span><span class="sxs-lookup"><span data-stu-id="3f78d-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="3f78d-112">Chiudere Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="3f78d-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="3f78d-113">Testare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3f78d-113">Test the image.</span></span>

5.  <span data-ttu-id="3f78d-114">Dopo aver testato l'immagine, imballarla nel repository locale usando lo stesso nome dell'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="3f78d-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="3f78d-115">**Nota**  Se il nome dell'immagine è diverso rispetto alla versione esistente, verrà creata una nuova immagine invece di una nuova versione dell'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="3f78d-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="3f78d-116">Caricare la nuova versione nel server o distribuirla tramite un pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3f78d-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="3f78d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f78d-117">Related topics</span></span>


[<span data-ttu-id="3f78d-118">Creazione di un'immagine Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="3f78d-119">Come creare e testare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="3f78d-120">Come comprimere un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="3f78d-121">Come caricare un'immagine MED-V nel server</span><span class="sxs-lookup"><span data-stu-id="3f78d-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="3f78d-122">Aggiornamento di un'immagine dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="3f78d-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





