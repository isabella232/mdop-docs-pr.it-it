---
title: Come condividere le cartelle tra l'host e l'area di lavoro MED-V
description: Come condividere le cartelle tra l'host e l'area di lavoro MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825755"
---
# <span data-ttu-id="d1a54-103">Come condividere le cartelle tra l'host e l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="d1a54-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="d1a54-104">È possibile condividere cartelle tra l'host e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1a54-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="d1a54-105">Le cartelle condivise possono essere archiviate in questa procedura:</span><span class="sxs-lookup"><span data-stu-id="d1a54-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="d1a54-106">Un computer esterno della rete</span><span class="sxs-lookup"><span data-stu-id="d1a54-106">An external computer on the network</span></span>

-   <span data-ttu-id="d1a54-107">Il computer host</span><span class="sxs-lookup"><span data-stu-id="d1a54-107">The host computer</span></span>

<span data-ttu-id="d1a54-108">Le procedure seguenti illustrano come condividere cartelle tra l'host e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1a54-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="d1a54-109">Per condividere le cartelle presenti nella rete</span><span class="sxs-lookup"><span data-stu-id="d1a54-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="d1a54-110">Configurare MED-V in modalità desktop completo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="d1a54-111">In gestione MED-V, nella scheda rete, fare clic su **Usa indirizzo IP diverso da host (Bridge)**.</span><span class="sxs-lookup"><span data-stu-id="d1a54-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="d1a54-112">Eseguire le operazioni seguenti nel computer host:</span><span class="sxs-lookup"><span data-stu-id="d1a54-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="d1a54-113">Nel pannello di controllo fare clic su **Visualizza stato e attività della rete**e impostare **individuazione rete** **su**attivato.</span><span class="sxs-lookup"><span data-stu-id="d1a54-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="d1a54-114">Nel menu Start fare clic con il pulsante destro del mouse su **computer**e scegliere **Mappa unità di rete**.</span><span class="sxs-lookup"><span data-stu-id="d1a54-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="d1a54-115">Nella finestra di dialogo **Map Drive di rete** selezionare un'unità nel campo **unità** .</span><span class="sxs-lookup"><span data-stu-id="d1a54-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="d1a54-116">**Nota**  Assicurarsi che la stessa lettera di unità non sia in uso in entrambi i computer.</span><span class="sxs-lookup"><span data-stu-id="d1a54-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="d1a54-117">Fai clic su **Browse**.</span><span class="sxs-lookup"><span data-stu-id="d1a54-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="d1a54-118">Nella finestra di dialogo **Sfoglia per la cartella** individuare l'unità condivisa e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1a54-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="d1a54-119">Fai clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="d1a54-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="d1a54-120">Ripetere il passaggio 3 nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1a54-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="d1a54-121">Posizionare il puntatore sulla stessa unità del computer host.</span><span class="sxs-lookup"><span data-stu-id="d1a54-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="d1a54-122">Per condividere le cartelle presenti nell'host</span><span class="sxs-lookup"><span data-stu-id="d1a54-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="d1a54-123">Configurare la cartella da condividere con le autorizzazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="d1a54-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="d1a54-124">Nell'area di lavoro MED-V passare a **risorse di rete** e individuare la cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="d1a54-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="d1a54-125">Nell'area di lavoro MED-V individuare la cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="d1a54-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="d1a54-126">**Nota**  Assicurarsi che i computer dell'area di lavoro host e MED-V si trovino nello stesso dominio o in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d1a54-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





