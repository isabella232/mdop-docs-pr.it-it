---
title: Come comprimere un'immagine MED-V
description: Come comprimere un'immagine MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824676"
---
# <span data-ttu-id="fab53-103">Come comprimere un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="fab53-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="fab53-104">Un'immagine MED-V deve essere imballata prima che possa essere aggiunta a un pacchetto di distribuzione o caricata nel server.</span><span class="sxs-lookup"><span data-stu-id="fab53-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="fab53-105">Per creare un'immagine di MED-V imballata</span><span class="sxs-lookup"><span data-stu-id="fab53-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="fab53-106">Fare clic sul pulsante Gestione **Immagini** .</span><span class="sxs-lookup"><span data-stu-id="fab53-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="fab53-107">Nel modulo **Immagini** , nel riquadro **Immagini imballate locali** , fare clic su **nuovo**.</span><span class="sxs-lookup"><span data-stu-id="fab53-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="fab53-108">Nella finestra di dialogo **creazione immagine imballata** selezionare l'immagine della macchina virtuale eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fab53-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="fab53-109">Nel campo **file di immagine di base** Digitare il percorso completo della directory in cui si trova l'immagine PC virtuale Microsoft predisposta per MED-V.</span><span class="sxs-lookup"><span data-stu-id="fab53-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="fab53-110">Fare clic su **Sfoglia** per passare alla directory in cui si trova l'immagine del PC virtuale Microsoft predisposta per MED-V.</span><span class="sxs-lookup"><span data-stu-id="fab53-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="fab53-111">Specificare il nome della nuova immagine eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fab53-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="fab53-112">Nel campo **nome immagine** Digitare il nome desiderato.</span><span class="sxs-lookup"><span data-stu-id="fab53-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="fab53-113">Nota</span><span class="sxs-lookup"><span data-stu-id="fab53-113">Note</span></span>**  
        <span data-ttu-id="fab53-114">I caratteri seguenti non possono essere inclusi nel nome dell'immagine: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="fab53-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="fab53-115">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="fab53-115">Click **OK**.</span></span>

   <span data-ttu-id="fab53-116">Nel computer host viene creata una nuova immagine imballata di MED-V con le proprietà definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fab53-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="fab53-117">Nota</span><span class="sxs-lookup"><span data-stu-id="fab53-117">Note</span></span>**  
<span data-ttu-id="fab53-118">Nelle immagini imballate **locali** e nelle **Immagini imballate nei** riquadri del server, la versione più recente di ogni immagine viene visualizzata come nodo padre.</span><span class="sxs-lookup"><span data-stu-id="fab53-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="fab53-119">Fare clic sul nodo padre per visualizzare tutte le altre versioni esistenti dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="fab53-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="fab53-120">Proprietà delle immagini imballate locali</span><span class="sxs-lookup"><span data-stu-id="fab53-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fab53-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fab53-121">Property</span></span></th>
<th align="left"><span data-ttu-id="fab53-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fab53-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fab53-123">Nome immagine</span><span class="sxs-lookup"><span data-stu-id="fab53-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="fab53-124">Nome dell'immagine imballata come è stato definito quando l'amministratore ha creato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="fab53-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fab53-125">Versione</span><span class="sxs-lookup"><span data-stu-id="fab53-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="fab53-126">La versione dell'immagine visualizzata.</span><span class="sxs-lookup"><span data-stu-id="fab53-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fab53-127">Nota</span><span class="sxs-lookup"><span data-stu-id="fab53-127">Note</span></span></strong><br/><p><span data-ttu-id="fab53-128">Tutte le versioni precedenti vengono mantenute, a meno che non vengano eliminate.</span><span class="sxs-lookup"><span data-stu-id="fab53-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fab53-129">Dimensioni file (compressi)</span><span class="sxs-lookup"><span data-stu-id="fab53-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fab53-130">Dimensione compressa fisica dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="fab53-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fab53-131">Dimensioni immagine (non compresso)</span><span class="sxs-lookup"><span data-stu-id="fab53-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fab53-132">Dimensioni non compresse fisiche dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="fab53-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fab53-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fab53-133">Related topics</span></span>


[<span data-ttu-id="fab53-134">Come installare il client MED-V e MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="fab53-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="fab53-135">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="fab53-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="fab53-136">Creazione di un'immagine Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="fab53-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









