---
title: Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione
description: Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823635"
---
# <span data-ttu-id="80e2a-103">Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="80e2a-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="80e2a-104">L'installazione del pacchetto di distribuzione offre un metodo per installare client MED-V insieme a tutti i prerequisiti necessari e alle impostazioni predefinite dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="80e2a-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="80e2a-105">Quando si usa un pacchetto di distribuzione, il pacchetto viene distribuito tramite una rete condivisa o un supporto rimovibile.</span><span class="sxs-lookup"><span data-stu-id="80e2a-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="80e2a-106">L'immagine può essere inclusa nel pacchetto o può essere distribuita separatamente.</span><span class="sxs-lookup"><span data-stu-id="80e2a-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="80e2a-107">Prima di creare un pacchetto di distribuzione, verificare di aver creato un'immagine MED-V pronta per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="80e2a-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="80e2a-108">Per altre informazioni sulla creazione di un'immagine MED-V, vedere [creazione di un'immagine MED-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="80e2a-109">Dopo aver preparato l'immagine MED-V, prendere in considerazione il metodo migliore per distribuire l'immagine nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="80e2a-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="80e2a-110">L'immagine può essere distribuita in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="80e2a-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="80e2a-111">Caricato sul Web e distribuito tramite download Web, facoltativamente usando la tecnologia di trasferimento trim.</span><span class="sxs-lookup"><span data-stu-id="80e2a-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="80e2a-112">Distribuiti usando la pre-staging delle immagini.</span><span class="sxs-lookup"><span data-stu-id="80e2a-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="80e2a-113">Incluso nel pacchetto di distribuzione e distribuito insieme a tutti gli altri componenti MED-V.</span><span class="sxs-lookup"><span data-stu-id="80e2a-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="80e2a-114">Se l'immagine verrà inclusa nel pacchetto, non saranno necessarie altre configurazioni per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="80e2a-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="80e2a-115">Se l'immagine non verrà inclusa nel pacchetto di distribuzione, eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="80e2a-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="80e2a-116">Se si sta distribuendo l'immagine tramite il Web, caricare l'immagine MED-V nel server di distribuzione Web Image.</span><span class="sxs-lookup"><span data-stu-id="80e2a-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="80e2a-117">Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="80e2a-118">Per informazioni sul caricamento di un'immagine nel server, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="80e2a-119">Se si sta distribuendo l'immagine tramite pre-staging delle immagini, configurare la cartella pre-stage e premere l'immagine MED-V nella cartella.</span><span class="sxs-lookup"><span data-stu-id="80e2a-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="80e2a-120">Per altre informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="80e2a-121">**Nota**  Se si usa la pre-staging delle immagini, è importante configurare la cartella di pre-stage dell'immagine prima di creare il pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="80e2a-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="80e2a-122">Il percorso della cartella deve essere incluso nel pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="80e2a-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="80e2a-123">Infine, crea il pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="80e2a-123">Finally, create the deployment package.</span></span> <span data-ttu-id="80e2a-124">Per altre informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="80e2a-125">Dopo aver completato il pacchetto, distribuirlo per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="80e2a-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="80e2a-126">Una volta distribuito il pacchetto di distribuzione, è possibile installare client MED-V e distribuire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="80e2a-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="80e2a-127">Per altre informazioni sull'installazione di client MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="80e2a-128">Per altre informazioni sulla distribuzione dell'immagine, vedere [come distribuire un'immagine dell'area di lavoro](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="80e2a-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





