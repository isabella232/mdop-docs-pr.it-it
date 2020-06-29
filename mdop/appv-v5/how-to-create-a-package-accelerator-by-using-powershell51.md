---
title: Come creare un acceleratore pacchetto con PowerShell
description: Come creare un acceleratore pacchetto con PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805608"
---
# <span data-ttu-id="9278c-103">Come creare un acceleratore pacchetto con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9278c-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="9278c-104">Gli acceleratori del pacchetto App-V 5,1 sequenziano automaticamente le applicazioni grandi e complesse.</span><span class="sxs-lookup"><span data-stu-id="9278c-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="9278c-105">Inoltre, quando applichi un Acceleratore pacchetto App-V 5,1, non sempre devi installare manualmente un'applicazione per creare il pacchetto virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="9278c-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="9278c-106">Per creare un Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="9278c-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="9278c-107">Installare l'App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9278c-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="9278c-108">Per altre informazioni sull'installazione del sequencer [, vedere come installare il sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="9278c-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="9278c-109">Per aprire una console di PowerShell, fare clic su **Start** e digitare **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="9278c-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="9278c-110">Fare clic con il pulsante destro del mouse su **Windows PowerShell** e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="9278c-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="9278c-111">Usa il cmdlet **New-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="9278c-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="9278c-112">Per creare un Acceleratore pacchetto, assicurati di avere il pacchetto. AppV per creare un acceleratore, il supporto di installazione o i file di installazione e, facoltativamente, un file Leggimi per i consumatori dell'acceleratore da usare.</span><span class="sxs-lookup"><span data-stu-id="9278c-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="9278c-113">I parametri seguenti sono necessari per usare il cmdlet Acceleratore pacchetto:</span><span class="sxs-lookup"><span data-stu-id="9278c-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="9278c-114">**InstalledFilesPath** -specifica il percorso di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9278c-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="9278c-115">**Installer** : specifica il percorso del supporto del programma di installazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9278c-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="9278c-116">**InputPackagePath** : specifica il percorso del pacchetto. AppV</span><span class="sxs-lookup"><span data-stu-id="9278c-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="9278c-117">**Path** : specifica la directory di output per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9278c-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="9278c-118">L'esempio seguente mostra come creare un Acceleratore pacchetto con un pacchetto appv e il supporto di installazione:</span><span class="sxs-lookup"><span data-stu-id="9278c-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="9278c-119">New-AppvPackageAccelerator-InputPackagePath &lt; path to the. AppV file &gt; -percorso del programma di installazione &lt; per la directory del percorso eseguibile &gt; del programma di installazione &lt; del percorso di output&gt;</span><span class="sxs-lookup"><span data-stu-id="9278c-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="9278c-120">I parametri facoltativi aggiuntivi che possono essere usati con il cmdlet **New-AppvPackageAccelerator** vengono visualizzati nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="9278c-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="9278c-121">**AcceleratorDescriptionFile** -specifica il percorso delle istruzioni per l'Acceleratore pacchetto creato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9278c-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="9278c-122">Le istruzioni per l'acceleratore del pacchetto sono file di descrizione **txt** o **RTF** che verranno impacchettati con il pacchetto creato con l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9278c-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="9278c-123">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="9278c-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9278c-124">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9278c-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9278c-125">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="9278c-125">Got an App-V issue?</span></span>** <span data-ttu-id="9278c-126">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9278c-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9278c-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9278c-127">Related topics</span></span>


[<span data-ttu-id="9278c-128">Amministrazione di App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9278c-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





