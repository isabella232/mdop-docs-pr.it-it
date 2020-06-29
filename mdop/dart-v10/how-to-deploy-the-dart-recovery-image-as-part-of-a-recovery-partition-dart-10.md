---
title: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
description: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
author: dansimp
ms.assetid: 0d2192c1-4058-49fb-b0b6-baf4699ac7f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: bc5f295d35dff1e4fc2a84c47188be40153b85c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804701"
---
# <span data-ttu-id="84962-103">Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="84962-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="84962-104">Dopo aver eseguito la creazione guidata immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10 e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84962-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span> <span data-ttu-id="84962-105">È consigliabile una partizione, perché i problemi di danneggiamento che impediscono l'avvio del sistema operativo Windows impediscono anche l'avvio dell'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84962-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="84962-106">Una partizione separata elimina inoltre la necessità di specificare due volte la chiave di ripristino di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="84962-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="84962-107">È consigliabile nascondere la partizione per evitare che gli utenti memorizzino i file.</span><span class="sxs-lookup"><span data-stu-id="84962-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="84962-108">Per distribuire il dardo nella partizione di ripristino di un'immagine di Windows 10</span><span class="sxs-lookup"><span data-stu-id="84962-108">To deploy DaRT in the recovery partition of a Windows 10 image</span></span>**

1.  <span data-ttu-id="84962-109">Creare una partizione di destinazione nell'immagine di Windows 10 uguale o maggiore della dimensione del file di immagine ISO creato tramite la **creazione guidata immagine di ripristino di Dart 10**.</span><span class="sxs-lookup"><span data-stu-id="84962-109">Create a target partition in your Windows 10 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 10 Recovery Image wizard**.</span></span>

    <span data-ttu-id="84962-110">La dimensione minima richiesta per una partizione DaRT è 500MB per adattare la funzionalità di connessione remota in DaRT.</span><span class="sxs-lookup"><span data-stu-id="84962-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="84962-111">Estrarre il file Boot. wim dal file di immagine ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="84962-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="84962-112">Usando il metodo preferito della società, montare il file di immagine ISO creato nella pagina **Crea immagine di avvio** .</span><span class="sxs-lookup"><span data-stu-id="84962-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="84962-113">Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.</span><span class="sxs-lookup"><span data-stu-id="84962-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="84962-114">**Nota**  Se si è masterizzato un CD, un DVD o un USB dell'immagine di ripristino, è possibile aprire i file nel supporto rimovibile e copiare il file Boot. wim dalla cartella \\sources.</span><span class="sxs-lookup"><span data-stu-id="84962-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="84962-115">Se si copia il file Boot. wim, non è necessario montare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="84962-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="84962-116">Usa il file Boot. wim per creare una partizione di ripristino avviabile usando il metodo standard della società per la creazione di un'immagine ripristino personalizzata di Windows.</span><span class="sxs-lookup"><span data-stu-id="84962-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="84962-117">Per altre informazioni su come creare o personalizzare una partizione di ripristino, vedere [personalizzazione dell'esperienza Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="84962-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="84962-118">Sostituisci la partizione di destinazione nell'immagine di Windows 10 con la partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="84962-118">Replace the target partition in your Windows 10 image with the recovery partition.</span></span>

    <span data-ttu-id="84962-119">Per altre informazioni su come distribuire una soluzione di ripristino per reinstallare l'immagine Factory in caso di errore di sistema, vedere [distribuire un'immagine di ripristino del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="84962-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="84962-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84962-120">Related topics</span></span>


[<span data-ttu-id="84962-121">Creazione dell'immagine di ripristino di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="84962-121">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

[<span data-ttu-id="84962-122">Distribuzione dell'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="84962-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

[<span data-ttu-id="84962-123">Pianificazione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="84962-123">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

 

 





