---
title: Come caricare un'immagine MED-V nel server
description: Come caricare un'immagine MED-V nel server
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825705"
---
# <span data-ttu-id="541d9-103">Come caricare un'immagine MED-V nel server</span><span class="sxs-lookup"><span data-stu-id="541d9-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="541d9-104">Dopo aver testato un'immagine MED-V, è possibile che venga imballata e quindi caricata nel server.</span><span class="sxs-lookup"><span data-stu-id="541d9-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="541d9-105">Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="541d9-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="541d9-106">Una volta che un'immagine MED-V viene compressa e caricata nel server, può essere distribuita agli utenti usando un centro di distribuzione del software aziendale oppure può essere scaricata dagli utenti che usano un pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="541d9-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="541d9-107">Per informazioni sulla distribuzione tramite un centro distribuzione software aziendale, vedere [distribuzione di un'area di lavoro MED-V tramite un sistema di distribuzione del software aziendale](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="541d9-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="541d9-108">Per informazioni sulla distribuzione tramite un pacchetto, vedere [distribuzione di un'area di lavoro MED-V tramite un pacchetto di distribuzione](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="541d9-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="541d9-109">Nota</span><span class="sxs-lookup"><span data-stu-id="541d9-109">Note</span></span>**  
<span data-ttu-id="541d9-110">Prima di caricare un'immagine, verificare che un proxy Web non sia definito nelle impostazioni del browser e che Windows Update non sia attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="541d9-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="541d9-111">Per caricare un'immagine MED-V nel server</span><span class="sxs-lookup"><span data-stu-id="541d9-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="541d9-112">Nel riquadro **Immagini locali imballati** selezionare l'immagine creata.</span><span class="sxs-lookup"><span data-stu-id="541d9-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="541d9-113">Fare clic su **carica**.</span><span class="sxs-lookup"><span data-stu-id="541d9-113">Click **Upload**.</span></span>

    <span data-ttu-id="541d9-114">L'immagine viene caricata nel server.</span><span class="sxs-lookup"><span data-stu-id="541d9-114">The image is uploaded to the server.</span></span> <span data-ttu-id="541d9-115">Potrebbe essere necessario un periodo di tempo considerevole.</span><span class="sxs-lookup"><span data-stu-id="541d9-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="541d9-116">Le immagini nel server sono definite con le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="541d9-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="541d9-117">Immagini imballate sulle proprietà del server</span><span class="sxs-lookup"><span data-stu-id="541d9-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="541d9-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="541d9-118">Property</span></span></th>
<th align="left"><span data-ttu-id="541d9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="541d9-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="541d9-120">Nome immagine</span><span class="sxs-lookup"><span data-stu-id="541d9-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="541d9-121">Nome dell'immagine imballata come è stato definito quando l'amministratore ha creato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="541d9-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="541d9-122">Versione</span><span class="sxs-lookup"><span data-stu-id="541d9-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="541d9-123">La versione dell'immagine visualizzata.</span><span class="sxs-lookup"><span data-stu-id="541d9-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="541d9-124">Nota</span><span class="sxs-lookup"><span data-stu-id="541d9-124">Note</span></span></strong><br/><p><span data-ttu-id="541d9-125">Tutte le versioni precedenti vengono mantenute, a meno che non vengano eliminate.</span><span class="sxs-lookup"><span data-stu-id="541d9-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="541d9-126">Dimensioni file (compressi)</span><span class="sxs-lookup"><span data-stu-id="541d9-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="541d9-127">Dimensione compressa fisica dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="541d9-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="541d9-128">Dimensioni immagine (non compresso)</span><span class="sxs-lookup"><span data-stu-id="541d9-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="541d9-129">Dimensioni non compresse fisiche dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="541d9-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="541d9-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="541d9-130">Related topics</span></span>


[<span data-ttu-id="541d9-131">Come installare il client MED-V e MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="541d9-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="541d9-132">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="541d9-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="541d9-133">Creazione di un'immagine Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="541d9-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="541d9-134">Come comprimere un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="541d9-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









