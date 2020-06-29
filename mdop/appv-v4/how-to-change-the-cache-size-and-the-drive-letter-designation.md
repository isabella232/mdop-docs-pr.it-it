---
title: Come modificare le dimensioni della cache e definire la lettera di unità
description: Come modificare le dimensioni della cache e definire la lettera di unità
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818036"
---
# <span data-ttu-id="31b67-103">Come modificare le dimensioni della cache e definire la lettera di unità</span><span class="sxs-lookup"><span data-stu-id="31b67-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="31b67-104">È possibile modificare le dimensioni della cache e la designazione delle lettere di unità direttamente dal nodo **Application Virtualization** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="31b67-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="31b67-105">Nota</span><span class="sxs-lookup"><span data-stu-id="31b67-105">Note</span></span>**  
<span data-ttu-id="31b67-106">Dopo aver impostato la dimensione della cache, non può essere ridotta.</span><span class="sxs-lookup"><span data-stu-id="31b67-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="31b67-107">Per modificare le dimensioni della cache</span><span class="sxs-lookup"><span data-stu-id="31b67-107">To change the cache size</span></span>**

1.  <span data-ttu-id="31b67-108">Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="31b67-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="31b67-109">Selezionare la scheda **file System** nella finestra di dialogo **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="31b67-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="31b67-110">Nella sezione **impostazioni di configurazione della cache client** fare clic su uno dei pulsanti di opzione seguenti per scegliere come gestire lo spazio della cache:</span><span class="sxs-lookup"><span data-stu-id="31b67-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="31b67-111">Importante</span><span class="sxs-lookup"><span data-stu-id="31b67-111">Important</span></span>**  
    <span data-ttu-id="31b67-112">Se si seleziona l'impostazione **USA soglia spazio libero su disco** , il valore immesso imposterà le dimensioni della cache sulla dimensione totale del disco meno il numero di soglia dello spazio libero su disco immesso.</span><span class="sxs-lookup"><span data-stu-id="31b67-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="31b67-113">Se si vuole quindi ripristinare l'uso dell'impostazione **Usa la dimensione massima della cache** , è necessario specificare un numero più grande rispetto alle dimensioni della cache esistenti.</span><span class="sxs-lookup"><span data-stu-id="31b67-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="31b67-114">In caso contrario, verrà visualizzato l'errore "la nuova dimensione deve essere superiore alla dimensione della cache esistente".</span><span class="sxs-lookup"><span data-stu-id="31b67-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="31b67-115">Fare clic su **OK** o su **applica** per modificare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="31b67-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="31b67-116">Per modificare la denominazione della lettera dell'unità</span><span class="sxs-lookup"><span data-stu-id="31b67-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="31b67-117">Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="31b67-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="31b67-118">Nella scheda **file System** nella finestra di dialogo **Proprietà** , nel campo **unità da usare** , selezionare la lettera di unità desiderata nell'elenco a discesa delle lettere di unità disponibili.</span><span class="sxs-lookup"><span data-stu-id="31b67-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="31b67-119">Questa impostazione diventa effettiva quando il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="31b67-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="31b67-120">Fare clic su **OK** o su **applica** per modificare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="31b67-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="31b67-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31b67-121">Related topics</span></span>


[<span data-ttu-id="31b67-122">Come configurare il client in Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="31b67-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









