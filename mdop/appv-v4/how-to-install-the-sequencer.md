---
title: Come installare Sequencer
description: Come installare Sequencer
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817266"
---
# <span data-ttu-id="e5731-103">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="e5731-103">How to Install the Sequencer</span></span>


<span data-ttu-id="e5731-104">Microsoft Application Virtualization (App-V) Sequencer monitora e registra il processo di installazione e configurazione per le applicazioni in modo che l'applicazione possa essere eseguita come applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5731-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="e5731-105">È necessario installare il sequencer in un computer in cui è installato solo il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5731-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="e5731-106">In alternativa, è possibile installare il sequencer in un computer che gestisce un ambiente virtuale, ad esempio Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="e5731-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="e5731-107">Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che può essere riutilizzato con una configurazione aggiuntiva minima.</span><span class="sxs-lookup"><span data-stu-id="e5731-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="e5731-108">È necessario disporre di diritti amministrativi nel computer in uso per sequenziare l'applicazione e il computer deve essere connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="e5731-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="e5731-109">Il computer non deve eseguire alcuna versione del client Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="e5731-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="e5731-110">La creazione di un'applicazione virtuale tramite il sequencer è molto intensiva delle risorse, quindi è importante installare il sequencer in un computer che soddisfi o superi i requisiti consigliati.</span><span class="sxs-lookup"><span data-stu-id="e5731-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="e5731-111">Per altre informazioni sui requisiti di sistema, vedere [requisiti hardware e software sequencer](sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5731-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="e5731-112">Per installare Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="e5731-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="e5731-113">Copiare i file di installazione di Microsoft Application Virtualization Sequencer nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="e5731-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="e5731-114">Per avviare l'installazione guidata di Microsoft Application Virtualization Sequencer, selezionare **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="e5731-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="e5731-115">Se il **pacchetto ridistribuibile Microsoft Visual C++ SP1 (x86)** non viene rilevato prima dell'installazione, **setup.exe** lo installerà.</span><span class="sxs-lookup"><span data-stu-id="e5731-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="e5731-116">Nella pagina di **benvenuto** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e5731-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="e5731-117">Per accettare le condizioni del contratto di licenza nella pagina **contratto** di licenza, selezionare **Accetto i termini del contratto di licenza**.</span><span class="sxs-lookup"><span data-stu-id="e5731-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="e5731-118">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e5731-118">Click **Next**.</span></span>

5.  <span data-ttu-id="e5731-119">Nella pagina **cartella di destinazione** , per accettare la cartella di installazione predefinita, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e5731-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="e5731-120">Per specificare una cartella di destinazione diversa, fare clic su **Cambia** e specificare la cartella di installazione che verrà usata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e5731-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="e5731-121">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e5731-121">Click **Next**.</span></span>

6.  <span data-ttu-id="e5731-122">Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="e5731-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="e5731-123">Nella pagina **completamento guidata InstallShield** , per chiudere l'installazione guidata e aprire il sequencer, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="e5731-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="e5731-124">Per chiudere l'installazione guidata senza aprire il sequencer, deselezionare **Avvia il programma** e fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="e5731-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="e5731-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5731-125">Related topics</span></span>


[<span data-ttu-id="e5731-126">Configurazione di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="e5731-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





