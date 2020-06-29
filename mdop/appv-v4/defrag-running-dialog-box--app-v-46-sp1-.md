---
title: Finestra di dialogo Deframmentazione in esecuzione (App-V 4.6 SP1)
description: Finestra di dialogo Deframmentazione in esecuzione (App-V 4.6 SP1)
author: dansimp
ms.assetid: 0ceb0897-377e-4754-a7ab-3bc2b5af1452
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ca56723dedb46ba87890ae62d476ca365b201c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821726"
---
# <span data-ttu-id="e0c9b-103">Finestra di dialogo Deframmentazione in esecuzione (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e0c9b-103">Defrag Running Dialog Box (App-V 4.6 SP1)</span></span>


<span data-ttu-id="e0c9b-104">Il servizio di deframmentazione disco è in funzione.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-104">The Disk Defragmenter service is running.</span></span> <span data-ttu-id="e0c9b-105">Il servizio di deframmentazione disco usa le risorse di sistema e può causare degradazioni nelle prestazioni o aumentare il tempo necessario per creare un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-105">The Disk Defragmenter service uses system resources and can cause degradation in performance or increase the time it takes to create virtual application package.</span></span>

<span data-ttu-id="e0c9b-106">Usare la procedura seguente per arrestare l'utilizzo del servizio di deframmentazione disco durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-106">Use the following procedure to stop the Disk Defragmenter service from running during sequencing.</span></span>

1.  <span data-ttu-id="e0c9b-107">Nel computer che gestisce l'App-V Sequencer fare clic su **Start**, fare clic con il pulsante destro del mouse su **computer**e quindi scegliere **Gestisci**.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-107">On the computer running the App-V Sequencer, click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="e0c9b-108">Nella console di **Gestione computer** fare doppio clic su **Servizi e applicazioni**e quindi fare doppio clic su **Servizi** per espandere **Servizi**.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-108">In the **Computer Management** console, double-click **Services and Applications**, and then double-click **Services** to expand **Services**,.</span></span>

3.  <span data-ttu-id="e0c9b-109">Individuarla nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-109">Locate it in the list.</span></span> <span data-ttu-id="e0c9b-110">Fare clic con il pulsante destro del mouse su **deframmentazione disco**, scegliere **altre azioni**, fare clic su **Interrompi** per arrestare il deframmentazione disco e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0c9b-110">Right-click **Disk Defragmenter**, click **More Actions**, click **Stop** to stop Disk Defragmenter, and then click **OK**.</span></span>

## <span data-ttu-id="e0c9b-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0c9b-111">Related topics</span></span>


[<span data-ttu-id="e0c9b-112">Finestre di dialogo (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="e0c9b-112">Dialog Boxes (AppV 4.6 SP1)</span></span>](dialog-boxes--appv-46-sp1-.md)

 

 





