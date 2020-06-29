---
title: Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7
description: Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827285"
---
# <span data-ttu-id="362ac-103">Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7</span><span class="sxs-lookup"><span data-stu-id="362ac-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="362ac-104">Puoi installare tutti i componenti MED-V in un'immagine di Windows 7 distribuita in tutta l'organizzazione come per qualsiasi nuova installazione di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="362ac-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="362ac-105">L'utente finale termina quindi l'installazione dell'area di lavoro MED-V facendo clic su un collegamento al menu **Start** configurato per avviare MED-v.</span><span class="sxs-lookup"><span data-stu-id="362ac-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="362ac-106">La prima volta che viene avviata la configurazione e l'utente finale segue le istruzioni per completare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="362ac-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="362ac-107">La sezione seguente contiene informazioni e istruzioni utili per distribuire l'area di lavoro MED-V in tutta l'organizzazione usando un'immagine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="362ac-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="362ac-108">Per distribuire un'area di lavoro MED-V in un'immagine di Windows 7</span><span class="sxs-lookup"><span data-stu-id="362ac-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="362ac-109">Creare un'immagine standard di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="362ac-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="362ac-110">Per altre informazioni, vedere [creazione di un'immagine standard di Windows 7: Guida dettagliata](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="362ac-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="362ac-111">Nell'immagine di Windows 7 installare Windows Virtual PC e gli aggiornamenti di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="362ac-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="362ac-112">Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="362ac-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="362ac-113">Installare l'agente host MED-V usando il file di installazione MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="362ac-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="362ac-114">Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="362ac-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="362ac-115">**Avviso**  Internet Explorer deve essere chiuso prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="362ac-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="362ac-116">Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="362ac-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="362ac-117">Copiare i file del pacchetto dell'area di lavoro MED-V nell'immagine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="362ac-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="362ac-118">I file del pacchetto area di lavoro MED-V sono il programma di installazione dell'area di lavoro MED-V, il file con estensione MEDV e il file setup.exe creato tramite **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="362ac-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="362ac-119">**Importante**  Il file con estensione MEDV e setup.exe deve trovarsi nella stessa cartella del programma di installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="362ac-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="362ac-120">Installare quindi l'area di lavoro MED-V eseguendo setup.exe.</span><span class="sxs-lookup"><span data-stu-id="362ac-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="362ac-121">Configurare un collegamento nel menu **Start** per aprire l'installazione del pacchetto area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="362ac-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="362ac-122">Creare un collegamento al menu **Start** al file setup.exe che consente all'utente finale di avviare un'installazione di MED-V come richiesto.</span><span class="sxs-lookup"><span data-stu-id="362ac-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="362ac-123">Usando il processo di distribuzione delle immagini standard della società, distribuire l'immagine di Windows 7 ai computer dell'organizzazione che richiedono MED-V.</span><span class="sxs-lookup"><span data-stu-id="362ac-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="362ac-124">Quando l'utente finale deve accedere a un'applicazione pubblicata nell'area di lavoro MED-V, può fare clic sul collegamento al menu **Start** per installare l'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="362ac-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="362ac-125">In questo modo viene avviata automaticamente la prima configurazione e viene completata la configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="362ac-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="362ac-126">Dopo aver completato la configurazione per la prima volta, l'utente finale può accedere alle applicazioni MED-V nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="362ac-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="362ac-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="362ac-127">Related topics</span></span>


[<span data-ttu-id="362ac-128">Panoramica della distribuzione di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="362ac-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="362ac-129">Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="362ac-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





