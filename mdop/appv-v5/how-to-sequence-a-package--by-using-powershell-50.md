---
title: Come sequenziare un pacchetto usando PowerShell
description: Come sequenziare un pacchetto usando PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805175"
---
# <span data-ttu-id="312f4-103">Come sequenziare un pacchetto usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="312f4-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="312f4-104">Usare la procedura seguente per creare un nuovo pacchetto App-V 5,0 con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="312f4-104">Use the following procedure to create a new App-V 5.0 package using PowerShell.</span></span>

<span data-ttu-id="312f4-105">**Nota**  Prima di usare questa procedura, è necessario copiare i file del programma di installazione associati nel computer in cui è in corso il sequencer e leggere e comprendere la sezione sequencer della [pianificazione per l'App-V 5,0 sequencer e la distribuzione del client](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="312f4-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="312f4-106">Per creare una nuova applicazione virtuale tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="312f4-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="312f4-107">Installare l'App-V 5,0 sequencer.</span><span class="sxs-lookup"><span data-stu-id="312f4-107">Install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="312f4-108">Per altre informazioni sull'installazione del sequencer [, vedere come installare il sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="312f4-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="312f4-109">Per aprire una console di PowerShell, fare clic su **Start** e digitare **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="312f4-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="312f4-110">Fare clic con il pulsante destro del mouse su **Windows PowerShell** e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="312f4-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="312f4-111">Usando la console di PowerShell, digitare quanto segue: **Import-Module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="312f4-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="312f4-112">Per creare un pacchetto, usa il cmdlet **New-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="312f4-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="312f4-113">Per creare un pacchetto sono necessari i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="312f4-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="312f4-114">**Nome** : specifica il nome del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="312f4-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="312f4-115">**PrimaryVirtualApplicationDirectory** -specifica il percorso della directory che verrà usata per installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="312f4-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="312f4-116">Questo percorso deve esistere.</span><span class="sxs-lookup"><span data-stu-id="312f4-116">This path must exist.</span></span>

    -   <span data-ttu-id="312f4-117">**Installer** : specifica il percorso del programma di installazione dell'applicazione associato.</span><span class="sxs-lookup"><span data-stu-id="312f4-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="312f4-118">**Path** : specifica la directory di output per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="312f4-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="312f4-119">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="312f4-119">For example:</span></span>

    **<span data-ttu-id="312f4-120">New-AppvSequencerPackage-nome &lt; del pacchetto-percorso di PrimaryVirtualApplicationDirectory del percorso del &gt; &lt; pacchetto radice &gt; -programma &lt; di installazione per l'eseguibile del programma di installazione &gt; - &lt; directory OutputPath del percorso di output&gt;</span><span class="sxs-lookup"><span data-stu-id="312f4-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="312f4-121">Attendere che il sequencer crei il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="312f4-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="312f4-122">La creazione di un pacchetto tramite PowerShell può richiedere tempo.</span><span class="sxs-lookup"><span data-stu-id="312f4-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="312f4-123">Se il pacchetto non è stato creato correttamente, verrà restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="312f4-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="312f4-124">L'elenco seguente mostra i parametri facoltativi aggiuntivi che possono essere usati con il cmdlet **New-AppvSequencerPackage** :</span><span class="sxs-lookup"><span data-stu-id="312f4-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="312f4-125">AcceleratorFilePath: specifica il percorso del file Accelerator. cab per generare un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="312f4-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="312f4-126">InstalledFilesPath-specifica il percorso in cui vengono salvati i file locali installati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="312f4-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="312f4-127">InstallMediaPath-specifica il percorso in cui si trova il supporto di installazione</span><span class="sxs-lookup"><span data-stu-id="312f4-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="312f4-128">TemplateFilePath: specifica il percorso di un file modello se si vuole personalizzare il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="312f4-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="312f4-129">FullLoad-specifica che il pacchetto deve essere completamente scaricato nel computer in cui è in uso l'App-V 5,0 prima che possa essere aperto.</span><span class="sxs-lookup"><span data-stu-id="312f4-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.0 before it can be opened.</span></span>

    <span data-ttu-id="312f4-130">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="312f4-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="312f4-131">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="312f4-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="312f4-132">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="312f4-132">Got an App-V issue?</span></span>** <span data-ttu-id="312f4-133">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="312f4-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="312f4-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="312f4-134">Related topics</span></span>


[<span data-ttu-id="312f4-135">Amministrazione di App-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="312f4-135">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





