---
title: Come installare Application Virtualization Sequencer
description: Come installare Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817306"
---
# <span data-ttu-id="ecec3-103">Come installare Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ecec3-103">How to Install the Application Virtualization Sequencer</span></span>


<span data-ttu-id="ecec3-104">Microsoft Application Virtualization Sequencer monitora e registra il processo di installazione e configurazione per le applicazioni in modo che l'applicazione possa essere eseguita come applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="ecec3-104">The Microsoft Application Virtualization Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="ecec3-105">È necessario installare il sequencer in un computer in cui è installato solo il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ecec3-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="ecec3-106">In alternativa, è possibile installare il sequencer in un computer che gestisce un ambiente virtuale, ad esempio Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="ecec3-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="ecec3-107">Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che può essere riutilizzato con una configurazione aggiuntiva minima.</span><span class="sxs-lookup"><span data-stu-id="ecec3-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="ecec3-108">È necessario disporre di diritti amministrativi nel computer in uso per sequenziare l'applicazione e il computer non deve eseguire alcuna versione del client Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="ecec3-108">You must have administrative rights on the computer you are using to sequence the application and the computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="ecec3-109">La creazione di un'applicazione virtuale tramite il sequencer è molto intensivo delle risorse, quindi è importante installare il sequencer in un computer che soddisfi o superi i requisiti consigliati.</span><span class="sxs-lookup"><span data-stu-id="ecec3-109">Creating a virtual application by using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="ecec3-110">L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ecec3-110">Running the App-V sequencer in Safe Mode is not supported.</span></span> <span data-ttu-id="ecec3-111">Per altre informazioni sui requisiti di sistema, vedere [requisiti di sistema per la virtualizzazione delle applicazioni](application-virtualization-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ecec3-111">For more information about the system requirements, see [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span></span>

<span data-ttu-id="ecec3-112">**Importante**  Dopo aver sequenziato un'applicazione, prima di poter sequenziare correttamente una nuova applicazione è necessario reinstallare il sistema operativo e il sequencer nel computer in uso per sequenziare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ecec3-112">**Important** After you have sequenced an application, before you can properly sequence a new application you must reinstall the operating system and the Sequencer on the computer you are using to sequence applications.</span></span>

 

**<span data-ttu-id="ecec3-113">Per installare Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ecec3-113">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="ecec3-114">Copiare i file di installazione di Microsoft Application Virtualization Sequencer nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="ecec3-114">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="ecec3-115">Per avviare l'installazione guidata di Microsoft Application Virtualization Sequencer, selezionare **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-115">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="ecec3-116">Se il **pacchetto ridistribuibile Microsoft Visual C++ SP1 (x86)** non viene rilevato prima dell'installazione, **setup.exe** lo installerà.</span><span class="sxs-lookup"><span data-stu-id="ecec3-116">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="ecec3-117">Nella pagina di **benvenuto** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-117">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="ecec3-118">Per accettare le condizioni del contratto di licenza nella pagina **contratto** di licenza, selezionare **Accetto i termini del contratto di licenza**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-118">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="ecec3-119">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-119">Click **Next**.</span></span>

5.  <span data-ttu-id="ecec3-120">Nella pagina **cartella di destinazione** , per accettare la cartella di installazione predefinita, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-120">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="ecec3-121">Per specificare una cartella di destinazione diversa, fare clic su **Cambia** e specificare la cartella di installazione che verrà usata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ecec3-121">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="ecec3-122">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-122">Click **Next**.</span></span>

6.  <span data-ttu-id="ecec3-123">Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-123">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="ecec3-124">Nella pagina **completamento guidata InstallShield** , per chiudere l'installazione guidata e aprire il sequencer, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-124">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="ecec3-125">Per chiudere l'installazione guidata senza aprire il sequencer, deselezionare **Avvia il programma** e fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="ecec3-125">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="ecec3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecec3-126">Related topics</span></span>


[<span data-ttu-id="ecec3-127">Come eseguire l'aggiornamento di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ecec3-127">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="ecec3-128">Requisiti per la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ecec3-128">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

 

 





