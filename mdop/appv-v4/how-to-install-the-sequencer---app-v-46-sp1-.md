---
title: Come installare il sequencer (App-V 4,6 SP1)
description: Come installare il sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817275"
---
# <span data-ttu-id="8cd29-103">Come installare il sequencer (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8cd29-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="8cd29-104">Microsoft Application Virtualization (App-V) Sequencer monitora e registra il processo di installazione e configurazione per le applicazioni in modo che l'applicazione possa essere eseguita come applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cd29-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="8cd29-105">È necessario installare l'App-V Sequencer in un computer in cui è installato solo il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8cd29-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="8cd29-106">In alternativa, puoi installare il sequencer in un computer in uso in un ambiente virtuale, ad esempio un computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cd29-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="8cd29-107">Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che è possibile riutilizzare con una configurazione aggiuntiva minima.</span><span class="sxs-lookup"><span data-stu-id="8cd29-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="8cd29-108">È necessario avere credenziali amministrative nel computer in uso per sequenziare l'applicazione e il computer non deve eseguire alcuna versione di client App-V.</span><span class="sxs-lookup"><span data-stu-id="8cd29-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="8cd29-109">La creazione di un'applicazione virtuale tramite App-V Sequencer richiede più operazioni, quindi è importante installare il sequencer in un computer che soddisfi o superi i [requisiti hardware e software di Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8cd29-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="8cd29-110">Nota</span><span class="sxs-lookup"><span data-stu-id="8cd29-110">Note</span></span>**  
<span data-ttu-id="8cd29-111">L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8cd29-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="8cd29-112">Per installare Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8cd29-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="8cd29-113">Copiare i file di installazione di Microsoft Application Virtualization Sequencer nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="8cd29-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="8cd29-114">Per avviare l'installazione guidata di Microsoft Application Virtualization Sequencer, fare doppio clic su **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="8cd29-115">Se il **pacchetto ridistribuibile Microsoft Visual C++ SP1 (x86)** non viene rilevato prima dell'installazione, fare clic su **Installa** per installare il prerequisito necessario.</span><span class="sxs-lookup"><span data-stu-id="8cd29-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="8cd29-116">Per continuare l'installazione, nella pagina **iniziale** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="8cd29-117">Per accettare le condizioni del contratto di licenza nella pagina **contratto** di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="8cd29-118">Nella pagina **cartella di destinazione** , per accettare la cartella di installazione predefinita, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="8cd29-119">Per specificare una cartella di destinazione diversa, fare clic su **Cambia** e specificare la cartella di installazione che verrà usata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8cd29-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="8cd29-120">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-120">Click **Next**.</span></span>

6.  <span data-ttu-id="8cd29-121">Nella pagina **Virtual Drive** , per configurare l'unità di **Q:\\** predefinita per la virtualizzazione dell'applicazione (impostazione predefinita) come unità in cui verranno eseguite tutte le applicazioni sequenziate, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="8cd29-122">Se si vuole specificare una lettera di unità diversa, usare l'elenco e selezionare la lettera dell'unità che si vuole usare selezionando la lettera di unità appropriata e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="8cd29-123">Importante</span><span class="sxs-lookup"><span data-stu-id="8cd29-123">Important</span></span>**  
    <span data-ttu-id="8cd29-124">La lettera dell'unità di virtualizzazione dell'applicazione specificata con questo passaggio è la lettera dell'unità in cui verranno eseguite le applicazioni virtuali nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cd29-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="8cd29-125">La lettera dell'unità specificata deve essere disponibile e non attualmente in uso nei computer che eseguono il client App-V.</span><span class="sxs-lookup"><span data-stu-id="8cd29-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="8cd29-126">Se l'unità specificata è già in uso, l'applicazione virtuale non riesce nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cd29-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="8cd29-127">Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="8cd29-128">Nella pagina **completamento guidata InstallShield** , per chiudere l'installazione guidata e aprire App-V Sequencer, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="8cd29-129">Per chiudere l'installazione guidata senza aprire il sequencer, deselezionare **Avvia il programma**e quindi fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="8cd29-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="8cd29-130">Nota</span><span class="sxs-lookup"><span data-stu-id="8cd29-130">Note</span></span>**  
    <span data-ttu-id="8cd29-131">Se l'App-V Sequencer è stato installato in un computer che gestisce un ambiente virtuale, ad esempio una macchina virtuale, ora è necessario eseguire uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="8cd29-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="8cd29-132">Dopo aver sequenziato un'applicazione, è possibile tornare a questa immagine, in modo da poter sequenziare l'applicazione successiva.</span><span class="sxs-lookup"><span data-stu-id="8cd29-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="8cd29-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cd29-133">Related topics</span></span>


[<span data-ttu-id="8cd29-134">Configurazione di Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8cd29-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









