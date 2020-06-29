---
title: Come distribuire DaRT 10
description: Come distribuire DaRT 10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804702"
---
# <span data-ttu-id="56d6e-103">Come distribuire DaRT 10</span><span class="sxs-lookup"><span data-stu-id="56d6e-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="56d6e-104">Le istruzioni seguenti spiegano come distribuire Microsoft Diagnostics and Recovery Toolset (DaRT) 10 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="56d6e-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="56d6e-105">Per ottenere il software DaRT, Vedi [come ottenere MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="56d6e-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="56d6e-106">Si presuppone che si stiano installando tutte le funzionalità in un computer amministratore.</span><span class="sxs-lookup"><span data-stu-id="56d6e-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="56d6e-107">Se devi distribuire o disinstallare DaRT 10 su più computer, usando un sistema di distribuzione elettronica del software, ad esempio, potrebbe essere più semplice usare le opzioni di installazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="56d6e-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="56d6e-108">In questa sezione vengono fornite le descrizioni ed esempi delle opzioni della riga di comando disponibili.</span><span class="sxs-lookup"><span data-stu-id="56d6e-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="56d6e-109">**Importante**  Prima di installare DaRT, Vedi [configurazioni supportate da Dart 10](dart-10-supported-configurations.md) per assicurarti di avere installato tutti i prerequisiti software e che il computer soddisfi i requisiti minimi di sistema.</span><span class="sxs-lookup"><span data-stu-id="56d6e-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="56d6e-110">Il computer su cui si installa dardo deve eseguire Windows 10.</span><span class="sxs-lookup"><span data-stu-id="56d6e-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="56d6e-111">È possibile installare DaRT usando una delle due diverse configurazioni:</span><span class="sxs-lookup"><span data-stu-id="56d6e-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="56d6e-112">Installare DaRT e tutti gli strumenti DaRT nel computer dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="56d6e-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="56d6e-113">Installare nel computer di amministrazione solo gli strumenti necessari per creare l'immagine di ripristino delle freccette e quindi installare il **Visualizzatore connessione remota** e, facoltativamente, **Crash Analyzer** in un computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="56d6e-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="56d6e-114">Il file di installazione di DaRT è disponibile nelle versioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="56d6e-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="56d6e-115">Installare la versione che corrisponde all'architettura del computer in cui è in esecuzione la creazione guidata immagine di ripristino di freccette, non l'architettura del computer dell'immagine di ripristino che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="56d6e-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="56d6e-116">È possibile usare una versione del file di installazione di DaRT per creare un'immagine di ripristino per i computer a 32 bit o a 64 bit, ma non è possibile creare un'immagine di ripristino per i computer a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="56d6e-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="56d6e-117">Per installare freccette e tutti gli strumenti DaRT in un computer amministratore</span><span class="sxs-lookup"><span data-stu-id="56d6e-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="56d6e-118">Scaricare la versione a 32 bit o a bit 64 del file del programma di installazione di DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="56d6e-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="56d6e-119">Scegliere l'architettura che corrisponde al computer in cui si sta installando DaRT ed eseguire la procedura guidata di ripristino delle immagini.</span><span class="sxs-lookup"><span data-stu-id="56d6e-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="56d6e-120">Nella cartella in cui è stato scaricato il dardo 10 eseguire il file di installazione di **MSDaRT.msi** che corrisponde ai requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="56d6e-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="56d6e-121">Nella pagina **Introduzione alla configurazione guidata di Microsoft DaRT 10** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="56d6e-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="56d6e-122">Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="56d6e-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="56d6e-123">Nella pagina **Microsoft Update** selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="56d6e-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="56d6e-124">Nella pagina **selezionare la cartella di installazione** selezionare una cartella oppure fare clic su **Avanti** per installare il dardo nel percorso di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="56d6e-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="56d6e-125">Nella pagina **Opzioni di configurazione** selezionare le funzionalità DART che si vuole installare oppure fare clic su **Avanti** per installare Dart con tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="56d6e-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="56d6e-126">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="56d6e-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="56d6e-127">Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="56d6e-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="56d6e-128">Per installare DaRT e tutti gli strumenti DaRT in un computer amministratore usando un prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="56d6e-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="56d6e-129">Quando si installa o si disinstalla il dardo, è possibile eseguire i file di installazione al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="56d6e-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="56d6e-130">Questa sezione descrive alcuni esempi di opzioni diverse che è possibile specificare quando si installa o si disinstalla il dardo al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="56d6e-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="56d6e-131">L'esempio seguente mostra come installare tutte le funzionalità dardo.</span><span class="sxs-lookup"><span data-stu-id="56d6e-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="56d6e-132">L'esempio seguente mostra come installare solo la creazione guidata immagine di ripristino di freccette.</span><span class="sxs-lookup"><span data-stu-id="56d6e-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="56d6e-133">L'esempio seguente mostra come installare solo l'analizzatore crash e il Visualizzatore di connessioni remote DaRT.</span><span class="sxs-lookup"><span data-stu-id="56d6e-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="56d6e-134">L'esempio seguente crea un log di configurazione per Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56d6e-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="56d6e-135">Questa operazione è utile per il debug.</span><span class="sxs-lookup"><span data-stu-id="56d6e-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="56d6e-136">**Nota**  Puoi aggiungere/qn o/qb per eseguire un'installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="56d6e-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="56d6e-137">Per convalidare l'installazione di DaRT</span><span class="sxs-lookup"><span data-stu-id="56d6e-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="56d6e-138">Fare clic sul pulsante **Start**e selezionare **strumenti di diagnostica e ripristino**.</span><span class="sxs-lookup"><span data-stu-id="56d6e-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="56d6e-139">Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="56d6e-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="56d6e-140">Verificare che tutti gli strumenti DaRT selezionati per l'installazione siano stati correttamente installati.</span><span class="sxs-lookup"><span data-stu-id="56d6e-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="56d6e-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56d6e-141">Related topics</span></span>


[<span data-ttu-id="56d6e-142">Distribuzione di DaRT 10 nei computer di amministrazione</span><span class="sxs-lookup"><span data-stu-id="56d6e-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





