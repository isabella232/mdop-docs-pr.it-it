---
title: Installazione di applicazioni in un'immagine di Windows Virtual PC
description: Installazione di applicazioni in un'immagine di Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826835"
---
# <span data-ttu-id="891e2-103">Installazione di applicazioni in un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="891e2-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="891e2-104">Dopo aver creato un'immagine di Windows Virtual PC per l'uso con Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è possibile installare altri componenti utili quando si esegue MED-V, ad esempio un sistema ESD (Electronic Software Distribution) e un software antivirus.</span><span class="sxs-lookup"><span data-stu-id="891e2-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="891e2-105">La sezione seguente contiene informazioni utili per installare il software nell'immagine MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="891e2-106">**Attenzione**  Per semplificare la gestione dell'area di lavoro MED-V dopo la distribuzione, è consigliabile limitare il numero di componenti da installare nell'immagine MED-V per i componenti necessari o utili quando si usa MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="891e2-107">Ad esempio, anche se non è necessario eseguire MED-V, è possibile installare un sistema ESD da usare in seguito per l'installazione di applicazioni in un'area di lavoro MED-V e un software antivirus per la sicurezza sull'immagine.</span><span class="sxs-lookup"><span data-stu-id="891e2-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="891e2-108">Installazione del software in un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="891e2-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="891e2-109">Se non è attualmente in uso, aprire la macchina virtuale MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="891e2-110">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC** e quindi fare clic su **Virtual PC Windows**.</span><span class="sxs-lookup"><span data-stu-id="891e2-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="891e2-111">Fare doppio clic sulla macchina virtuale MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="891e2-112">Nel sistema operativo della macchina virtuale individuare i file di installazione per il software che si vuole installare.</span><span class="sxs-lookup"><span data-stu-id="891e2-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="891e2-113">Seguire le istruzioni di installazione fornite dal fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="891e2-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="891e2-114">**Nota**  Dopo aver completato l'installazione, potrebbe essere necessario chiudere e quindi riavviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="891e2-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="891e2-115">Ripetere questi passaggi per qualsiasi software o applicazione che si vuole installare nell'immagine MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="891e2-116">È consigliabile limitare il numero di applicazioni preinstallate nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="891e2-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="891e2-117">Il processo consigliato per l'installazione di applicazioni e altri software nell'immagine consiste nel preinstallare ora un sistema ESD e usarlo in seguito per distribuire il software all'immagine.</span><span class="sxs-lookup"><span data-stu-id="891e2-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="891e2-118">In alternativa, puoi anche usare criteri di gruppo o App-V per aggiungere o rimuovere applicazioni in un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="891e2-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="891e2-119">Per altre informazioni, vedere [gestione delle applicazioni distribuite nelle aree di lavoro MED-V](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="891e2-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="891e2-120">Per altre informazioni su come installare il software in un'immagine virtuale, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="891e2-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="891e2-121">[Pubblicare e usare le applicazioni virtuali](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="891e2-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="891e2-122">[Guida di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="891e2-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="891e2-123">Dopo aver installato tutto il software desiderato nell'immagine MED-V, l'immagine è pronta per essere inclusa nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="891e2-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="891e2-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="891e2-124">Related topics</span></span>


[<span data-ttu-id="891e2-125">Configurazione di un'immagine di Windows Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="891e2-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="891e2-126">Creare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="891e2-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





