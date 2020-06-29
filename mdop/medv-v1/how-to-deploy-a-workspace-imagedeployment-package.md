---
title: Come distribuire un'immagine dell'area di lavoro
description: Come distribuire un'immagine dell'area di lavoro
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827015"
---
# <span data-ttu-id="feffc-103">Come distribuire un'immagine dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="feffc-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="feffc-104">Quando si usa un pacchetto di distribuzione, è possibile distribuire una nuova immagine sui computer client in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="feffc-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="feffc-105">Download Web</span><span class="sxs-lookup"><span data-stu-id="feffc-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="feffc-106">Pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="feffc-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="feffc-107">Distribuzione dell'immagine all'interno del pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="feffc-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="feffc-108">Come distribuire un'immagine dell'area di lavoro tramite il Web</span><span class="sxs-lookup"><span data-stu-id="feffc-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="feffc-109">Per distribuire un'immagine dell'area di lavoro tramite il Web</span><span class="sxs-lookup"><span data-stu-id="feffc-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="feffc-110">Caricare l'immagine MED-V nel server.</span><span class="sxs-lookup"><span data-stu-id="feffc-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="feffc-111">Per informazioni sul caricamento dell'immagine, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="feffc-112">Creare un pacchetto di distribuzione e includere il percorso del server nella posizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="feffc-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="feffc-113">Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="feffc-114">Distribuire il pacchetto agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="feffc-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="feffc-115">Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="feffc-116">Il client MED-V viene installato e avviato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="feffc-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="feffc-117">Durante l'avvio iniziale, il client Scarica l'immagine dall'indirizzo del server specificato nell'installazione del client.</span><span class="sxs-lookup"><span data-stu-id="feffc-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="feffc-118">Come distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="feffc-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="feffc-119">Per distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="feffc-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="feffc-120">Creare una cartella di immagini pre-stage e spingere l'immagine nella cartella.</span><span class="sxs-lookup"><span data-stu-id="feffc-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="feffc-121">Per informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="feffc-122">Creare un pacchetto di distribuzione e includere il percorso della cartella di pre-stage dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="feffc-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="feffc-123">Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="feffc-124">Distribuire il pacchetto agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="feffc-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="feffc-125">Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="feffc-126">Il client MED-V viene installato e avviato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="feffc-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="feffc-127">Durante l'avvio iniziale, il client recupera l'immagine dalla cartella pre-Stage specificata nell'installazione del client.</span><span class="sxs-lookup"><span data-stu-id="feffc-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="feffc-128">Come distribuire un'immagine dell'area di lavoro usando un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="feffc-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="feffc-129">Per distribuire un'immagine dell'area di lavoro usando un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="feffc-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="feffc-130">Creare un pacchetto di distribuzione e includere l'immagine nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="feffc-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="feffc-131">Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="feffc-132">Distribuire il pacchetto agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="feffc-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="feffc-133">Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="feffc-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="feffc-134">L'immagine viene importata nell'host come parte dell'installazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="feffc-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="feffc-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="feffc-135">Related topics</span></span>


[<span data-ttu-id="feffc-136">Come configurare il server di distribuzione Web di immagini</span><span class="sxs-lookup"><span data-stu-id="feffc-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="feffc-137">Come configurare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="feffc-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





