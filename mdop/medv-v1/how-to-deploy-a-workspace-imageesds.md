---
title: Come distribuire un'immagine dell'area di lavoro
description: Come distribuire un'immagine dell'area di lavoro
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827005"
---
# <span data-ttu-id="9fa9f-103">Come distribuire un'immagine dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9fa9f-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="9fa9f-104">Quando si usa un sistema di distribuzione del software aziendale, è possibile distribuire una nuova immagine sui computer client in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9fa9f-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="9fa9f-105">Download Web</span><span class="sxs-lookup"><span data-stu-id="9fa9f-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="9fa9f-106">Pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="9fa9f-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="9fa9f-107">Come distribuire un'immagine dell'area di lavoro tramite il Web</span><span class="sxs-lookup"><span data-stu-id="9fa9f-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="9fa9f-108">Per distribuire un'immagine dell'area di lavoro tramite il Web</span><span class="sxs-lookup"><span data-stu-id="9fa9f-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="9fa9f-109">Caricare l'immagine MED-V nel server.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="9fa9f-110">Per informazioni sul caricamento dell'immagine, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9f-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="9fa9f-111">Usando il sistema di distribuzione del software aziendale, installare il pacchetto client. msi di MED-V nei computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="9fa9f-112">Per informazioni sull'installazione del pacchetto client. msi di MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9f-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="9fa9f-113">Il client MED-V viene installato e avviato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="9fa9f-114">Durante l'avvio iniziale, il client Scarica l'immagine dall'indirizzo del server specificato nell'installazione del client.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="9fa9f-115">Come distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="9fa9f-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="9fa9f-116">Per distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="9fa9f-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="9fa9f-117">Creare una cartella di immagini pre-stage e spingere l'immagine nella cartella.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="9fa9f-118">Per informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9f-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="9fa9f-119">Usando il sistema di distribuzione del software aziendale, installare il pacchetto client. msi di MED-V nei computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="9fa9f-120">Per informazioni sull'installazione del pacchetto client. msi di MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9f-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="9fa9f-121">Il client MED-V viene installato e avviato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="9fa9f-122">Durante l'avvio iniziale, il client recupera l'immagine dalla cartella pre-Stage specificata nell'installazione del client.</span><span class="sxs-lookup"><span data-stu-id="9fa9f-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="9fa9f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fa9f-123">Related topics</span></span>


[<span data-ttu-id="9fa9f-124">Come configurare il server di distribuzione Web di immagini</span><span class="sxs-lookup"><span data-stu-id="9fa9f-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





