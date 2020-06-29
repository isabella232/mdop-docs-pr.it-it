---
title: Come installare manualmente l'agente host MED-V
description: Come installare manualmente l'agente host MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804570"
---
# <span data-ttu-id="6c776-103">Come installare manualmente l'agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="6c776-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="6c776-104">Esistono due componenti distinti ma correlati alla soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0: l'agente host MED-V e l'agente guest.</span><span class="sxs-lookup"><span data-stu-id="6c776-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="6c776-105">L'agente host risiede nel computer host (un computer dell'utente che sta usando Windows 7) e fornisce un canale per comunicare con il guest MED-V (la macchina virtuale MED-V in uso nel computer host).</span><span class="sxs-lookup"><span data-stu-id="6c776-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="6c776-106">Offre anche alcune funzionalità correlate a MED-V, ad esempio la pubblicazione di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6c776-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="6c776-107">In genere, si distribuisce e si installa l'agente host MED-V usando il metodo preferito della società per il provisioning del software.</span><span class="sxs-lookup"><span data-stu-id="6c776-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="6c776-108">Tuttavia, prima di distribuire MED-V nell'organizzazione, potrebbe essere preferibile installare l'agente host localmente per i test.</span><span class="sxs-lookup"><span data-stu-id="6c776-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="6c776-109">Questa sezione fornisce istruzioni dettagliate per l'installazione manuale dell'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="6c776-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="6c776-110">**Nota**  L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="6c776-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="6c776-111">**Importante**  Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="6c776-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="6c776-112">Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6c776-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="6c776-113">Per installare l'agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="6c776-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="6c776-114">Individuare i file di installazione di MED-V ricevuti come parte del download del software.</span><span class="sxs-lookup"><span data-stu-id="6c776-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="6c776-115">Fare doppio clic sul file di installazione MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="6c776-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="6c776-116">Verrà visualizzata la **Configurazione guidata agente host di Microsoft Enterprise Desktop Virtualization (MED-V)** .</span><span class="sxs-lookup"><span data-stu-id="6c776-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="6c776-117">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="6c776-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="6c776-118">Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6c776-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="6c776-119">Selezionare la cartella di destinazione per l'installazione dell'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="6c776-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="6c776-120">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6c776-120">Click **Next**.</span></span>

5.  <span data-ttu-id="6c776-121">Per avviare l'installazione dell'agente host, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="6c776-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="6c776-122">Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="6c776-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="6c776-123">Per verificare che l'installazione dell'agente host sia stata eseguita correttamente, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="6c776-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="6c776-124">**Nota**  Finché non viene installata un'area di lavoro MED-V, l'agente host MED-V può essere avviato ed eseguito, ma non offre alcuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6c776-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="6c776-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c776-125">Related topics</span></span>


[<span data-ttu-id="6c776-126">Come distribuire i componenti MED-V con un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="6c776-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="6c776-127">Come installare Packager nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="6c776-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="6c776-128">Come disinstallare i componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="6c776-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





