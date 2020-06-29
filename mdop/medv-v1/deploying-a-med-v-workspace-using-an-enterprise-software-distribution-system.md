---
title: Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale
description: Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823626"
---
# <span data-ttu-id="2c214-103">Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale</span><span class="sxs-lookup"><span data-stu-id="2c214-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="2c214-104">Il client MED-V può essere distribuito usando un sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2c214-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="2c214-105">**Nota**  Se MED-V viene installato con Microsoft System Center Configuration Manager, quando si crea un pacchetto per MED-V, impostare la modalità di esecuzione su diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="2c214-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="2c214-106">Prima di distribuire MED-V usando un sistema di distribuzione del software aziendale, verificare di aver creato un'immagine MED-V pronta per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2c214-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="2c214-107">Per altre informazioni sulla creazione di un'immagine MED-V, vedere [creazione di un'immagine MED-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="2c214-108">Dopo aver preparato l'immagine MED-V, prendere in considerazione il metodo migliore per distribuire l'immagine nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="2c214-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="2c214-109">L'immagine può essere distribuita in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c214-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="2c214-110">Caricato sul Web e distribuito tramite download Web, utilizzando facoltativamente la tecnologia di trasferimento trim.</span><span class="sxs-lookup"><span data-stu-id="2c214-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="2c214-111">Distribuiti usando la pre-staging delle immagini.</span><span class="sxs-lookup"><span data-stu-id="2c214-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="2c214-112">Distribuzione dell'immagine tramite il Web</span><span class="sxs-lookup"><span data-stu-id="2c214-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="2c214-113">Se si distribuisce l'immagine tramite il Web, caricare l'immagine MED-V in un server di distribuzione Web delle immagini.</span><span class="sxs-lookup"><span data-stu-id="2c214-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="2c214-114">Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="2c214-115">Per informazioni sul caricamento di un'immagine nel server, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="2c214-116">Distribuzione dell'immagine tramite pre-staging</span><span class="sxs-lookup"><span data-stu-id="2c214-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="2c214-117">Se si sta distribuendo l'immagine tramite pre-staging delle immagini, configurare la cartella pre-stage e premere l'immagine MED-V nella cartella.</span><span class="sxs-lookup"><span data-stu-id="2c214-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="2c214-118">Per altre informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="2c214-119">**Nota**  Se si usa la pre-staging delle immagini, è importante configurare la cartella di pre-stage dell'immagine prima di spingere il pacchetto client. msi.</span><span class="sxs-lookup"><span data-stu-id="2c214-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="2c214-120">Il percorso della cartella deve essere incluso nel pacchetto client. msi.</span><span class="sxs-lookup"><span data-stu-id="2c214-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="2c214-121">Infine, premi il pacchetto client. MSI usando il centro di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="2c214-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="2c214-122">È quindi possibile installare MED-V e distribuire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2c214-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="2c214-123">Per altre informazioni sull'installazione di client MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="2c214-124">Per altre informazioni sulla distribuzione dell'immagine, vedere [come distribuire un'immagine dell'area di lavoro](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="2c214-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





