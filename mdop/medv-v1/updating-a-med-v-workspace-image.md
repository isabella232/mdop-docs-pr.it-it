---
title: Aggiornamento di un'immagine dell'area di lavoro MED-V
description: Aggiornamento di un'immagine dell'area di lavoro MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825855"
---
# <span data-ttu-id="1af5f-103">Aggiornamento di un'immagine dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="1af5f-104">Un'immagine può essere aggiornata in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1af5f-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="1af5f-105">L'aggiornamento può essere inserito nel sistema operativo guest usando il sistema di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="1af5f-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="1af5f-106">L'aggiornamento può essere caricato nel server di distribuzione Web Image e quindi scaricato dal client e applicato all'immagine MED-V.</span><span class="sxs-lookup"><span data-stu-id="1af5f-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="1af5f-107">L'immagine di base di MED-V può essere aggiornata e ridistribuita.</span><span class="sxs-lookup"><span data-stu-id="1af5f-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="1af5f-108">Come aggiornare un'immagine MED-V usando un sistema di distribuzione del software aziendale</span><span class="sxs-lookup"><span data-stu-id="1af5f-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="1af5f-109">Per aggiornare un'immagine MED-V usando un sistema di distribuzione del software aziendale</span><span class="sxs-lookup"><span data-stu-id="1af5f-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="1af5f-110">Fare riferimento alla documentazione del sistema in uso.</span><span class="sxs-lookup"><span data-stu-id="1af5f-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="1af5f-111">Come aggiornare un'immagine MED-V tramite il download Web</span><span class="sxs-lookup"><span data-stu-id="1af5f-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="1af5f-112">Per aggiornare un'immagine MED-V tramite download Web</span><span class="sxs-lookup"><span data-stu-id="1af5f-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="1af5f-113">In gestione MED-V, nella scheda **macchina virtuale** verificare che le impostazioni seguenti vengano applicate ai criteri dell'area di lavoro MED-v associati all'immagine MED-v da aggiornare:</span><span class="sxs-lookup"><span data-stu-id="1af5f-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="1af5f-114">La casella **di controllo Suggerisci aggiornamento quando è disponibile una nuova versione** è selezionata.</span><span class="sxs-lookup"><span data-stu-id="1af5f-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="1af5f-115">Facoltativamente, i **client devono usare il trasferimento trim durante il download delle immagini per l'area di lavoro** selezionata.</span><span class="sxs-lookup"><span data-stu-id="1af5f-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="1af5f-116">Per altre informazioni, vedere [come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1af5f-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="1af5f-117">Caricare l'aggiornamento delle immagini nel server di distribuzione di immagini Web.</span><span class="sxs-lookup"><span data-stu-id="1af5f-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="1af5f-118">Tutti i client con immagini che devono essere aggiornati scaricano automaticamente l'aggiornamento e lo applicano all'immagine.</span><span class="sxs-lookup"><span data-stu-id="1af5f-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="1af5f-119">Come aggiornare un'immagine di base di MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="1af5f-120">Per aggiornare un'immagine di base di MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="1af5f-121">Aprire l'immagine esistente in Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="1af5f-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="1af5f-122">Apportare le modifiche necessarie all'immagine, aggiornando l'immagine, ad esempio l'installazione di un nuovo software.</span><span class="sxs-lookup"><span data-stu-id="1af5f-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="1af5f-123">Chiudere Virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="1af5f-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="1af5f-124">Testare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="1af5f-124">Test the image.</span></span>

5.  <span data-ttu-id="1af5f-125">Dopo aver testato l'immagine, imballarla nel repository locale usando lo stesso nome dell'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="1af5f-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="1af5f-126">**Nota**  Se il nome dell'immagine è diverso rispetto alla versione esistente, verrà creata una nuova immagine invece di una nuova versione dell'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="1af5f-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="1af5f-127">Caricare la nuova versione nel server, premerla nella cartella di pre-stage dell'immagine o distribuirla tramite un pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1af5f-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="1af5f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1af5f-128">Related topics</span></span>


[<span data-ttu-id="1af5f-129">Creazione di un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="1af5f-130">Come aggiornare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="1af5f-131">Configurazione dei criteri dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1af5f-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="1af5f-132">Come configurare il server di distribuzione Web di immagini</span><span class="sxs-lookup"><span data-stu-id="1af5f-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





