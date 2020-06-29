---
title: Come creare e testare un'immagine MED-V
description: Come creare e testare un'immagine MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827045"
---
# <span data-ttu-id="b9f1a-103">Come creare e testare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="b9f1a-104">L'amministratore di MED-V crea un'immagine MED-V in modo che possa essere caricata, associata a un'area di lavoro MED-V e quindi distribuita al client sul Web, aggiunta a un pacchetto MED-V o scaricata nel client usando un sistema di terze parti.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="b9f1a-105">È consigliabile creare prima di tutto un'immagine di test e testarla nel client MED-V prima di distribuirla.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="b9f1a-106">Quando si crea un'immagine MED-V, viene eseguito l'esecuzione delle fasi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9f1a-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="b9f1a-107">**Immagine di test locale**: un'immagine di base che può essere testata localmente.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="b9f1a-108">**Immagine imballata locale**: dopo aver testato l'immagine, l'immagine viene imballata come esisteva prima del test.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="b9f1a-109">Nessuna modifica apportata durante il test è inclusa nell'immagine compressa.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="b9f1a-110">**Immagine imballata sul server**: l'immagine compressa viene caricata nel server.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="b9f1a-111">Come creare un'immagine di test MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="b9f1a-112">Per creare una nuova immagine di test MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="b9f1a-113">Fare clic sul pulsante Gestione **Immagini** .</span><span class="sxs-lookup"><span data-stu-id="b9f1a-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="b9f1a-114">Viene visualizzato il modulo **Immagini** .</span><span class="sxs-lookup"><span data-stu-id="b9f1a-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="b9f1a-115">Il modulo **Immagini** è costituito dai riquadri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9f1a-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="b9f1a-116">**Immagini di test locali**: immagini decomprimete locali.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="b9f1a-117">**Immagini imballate locali**: tutte le immagini imballate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="b9f1a-118">**Immagini imballate sul server**: tutte le immagini imballate e caricate nel server.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="b9f1a-119">Nelle immagini imballate **locali** e nelle **Immagini imballate nei** riquadri del server, la versione più recente di ogni immagine viene visualizzata come nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="b9f1a-120">Fare clic sul nodo padre per visualizzare tutte le altre versioni esistenti dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="b9f1a-121">Nel riquadro **Immagini di test locali** fare clic su **nuovo**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="b9f1a-122">Nella finestra di dialogo **creazione immagine di test** selezionare l'immagine della macchina virtuale che si vuole configurare come immagine di test MED-V eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9f1a-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="b9f1a-123">Nel campo file di **immagine di base** Digitare il percorso completo della directory in cui si trova l'immagine PC virtuale Microsoft predisposta per MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="b9f1a-124">Fare clic su **Sfoglia** per passare alla directory in cui si trova l'immagine del PC virtuale Microsoft predisposta per MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="b9f1a-125">Nel campo **nome immagine** Digitare o selezionare il nome desiderato.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="b9f1a-126">**Nota**  I caratteri seguenti non possono essere inclusi nel nome dell'immagine: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="b9f1a-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="b9f1a-127">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-127">Click **OK**.</span></span>

    <span data-ttu-id="b9f1a-128">Nel computer host viene creata una nuova immagine di test MED-V con le proprietà definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="b9f1a-129">Per altre informazioni sulla configurazione dell'immagine dell'area di lavoro MED-V, vedere [configurazione dei criteri di area di lavoro MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="b9f1a-130">Proprietà delle immagini di test locali</span><span class="sxs-lookup"><span data-stu-id="b9f1a-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9f1a-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9f1a-131">Property</span></span></th>
<th align="left"><span data-ttu-id="b9f1a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9f1a-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9f1a-133">Nome immagine</span><span class="sxs-lookup"><span data-stu-id="b9f1a-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9f1a-134">Nome dell'immagine di test come è stato definito quando l'amministratore ha creato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9f1a-135">Percorso immagine</span><span class="sxs-lookup"><span data-stu-id="b9f1a-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9f1a-136">Percorso locale dell'immagine di test.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9f1a-137">Creato</span><span class="sxs-lookup"><span data-stu-id="b9f1a-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9f1a-138">Data in cui è stata creata l'immagine di test.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b9f1a-139">Come testare un'immagine MED-V dal client MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="b9f1a-140">Dopo aver creato un'immagine di test MED-V, usare la procedura seguente per testare localmente l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="b9f1a-141">Per testare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="b9f1a-142">Fare clic sul pulsante Gestione **criteri** .</span><span class="sxs-lookup"><span data-stu-id="b9f1a-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="b9f1a-143">Nel modulo **criteri** assegnare l'immagine di test med-v a un'area di lavoro MED-v eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9f1a-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="b9f1a-144">Fare clic sulla scheda **macchina virtuale** .</span><span class="sxs-lookup"><span data-stu-id="b9f1a-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="b9f1a-145">Nel campo **immagine assegnata** selezionare l'immagine di test MED-V creata.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="b9f1a-146">Se l'immagine di test non è presente nell'elenco, fare clic su **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="b9f1a-147">Sulla barra degli strumenti fare clic su **Salva modifiche**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="b9f1a-148">Configurare le altre impostazioni dell'area di lavoro MED-V da testare.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="b9f1a-149">Per altre informazioni, vedere [configurazione dei criteri di area di lavoro MED-V](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="b9f1a-150">Avviare client MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="b9f1a-151">Nella casella **conferma test di verifica in corso** fare clic su **Usa immagine di test**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="b9f1a-152">Testare l'immagine di test dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="b9f1a-153">Per informazioni su come avviare ed eseguire client MED-V, vedere [operazioni client Med-v](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="b9f1a-154">**Nota**  Durante il test di un'immagine, non aprire VPC e apportare modifiche all'immagine.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="b9f1a-155">**Nota**  Quando si esegue il test di un'immagine, nessuna modifica viene salvata nell'immagine tra le sessioni. al contrario, vengono salvati in un file temporaneo separato.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="b9f1a-156">In questo modo, quando l'immagine viene imballata ed eseguita nell'ambiente di produzione, è l'immagine originale e pulita.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="b9f1a-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9f1a-157">Related topics</span></span>


[<span data-ttu-id="b9f1a-158">Creazione di un'immagine Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="b9f1a-159">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="b9f1a-160">Configurazione dei criteri dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="b9f1a-161">Operazioni del client MED-V</span><span class="sxs-lookup"><span data-stu-id="b9f1a-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





