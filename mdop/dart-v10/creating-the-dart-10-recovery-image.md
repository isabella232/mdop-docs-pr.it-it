---
title: Creazione dell'immagine di ripristino di DaRT 10
description: Creazione dell'immagine di ripristino di DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804804"
---
# <span data-ttu-id="dbb3c-103">Creazione dell'immagine di ripristino di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="dbb3c-103">Creating the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="dbb3c-104">Dopo l'installazione di Microsoft Diagnostics and Recovery Toolset (DaRT) 10, puoi creare un'immagine di ripristino di DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you create a DaRT 10 recovery image.</span></span> <span data-ttu-id="dbb3c-105">L'immagine di ripristino avvia Windows RE, da cui è possibile avviare gli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="dbb3c-106">Puoi generare file ISO (International Organization for Standardizzation) e immagini WIM (Windows Imaging Format).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="dbb3c-107">Inoltre, puoi usare PowerShell per generare script che usano le impostazioni selezionate nella procedura guidata immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbb3c-108">Puoi usare lo script in un secondo momento per ricostruire le immagini di ripristino usando le stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="dbb3c-109">L'immagine di ripristino offre un'ampia varietà di strumenti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="dbb3c-110">Per una descrizione degli strumenti, vedere [Panoramica degli strumenti in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-110">For a description of the tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

<span data-ttu-id="dbb3c-111">Dopo aver avviato il computer in DaRT, puoi eseguire i diversi strumenti DaRT per provare a diagnosticare e ripristinare il computer.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="dbb3c-112">Questa sezione illustra il processo di creazione dell'immagine di ripristino delle freccette e consente di selezionare gli strumenti e le funzionalità che si desidera includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="dbb3c-113">Puoi creare l'immagine di ripristino delle freccette usando uno dei due metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="dbb3c-114">Usa la configurazione guidata immagine di ripristino di freccette, che viene eseguita in un ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="dbb3c-115">Modificare uno script di PowerShell di esempio con i valori desiderati.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="dbb3c-116">Per altre informazioni, vedere [come usare uno script di PowerShell per creare l'immagine di ripristino](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="dbb3c-117">È possibile scrivere l'ISO in un CD o un DVD registrabile, salvarlo in un'unità flash USB oppure salvarlo in un formato che può essere usato per l'avvio in freccette da una partizione remota o da una partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="dbb3c-118">Dopo aver creato l'immagine ISO, è possibile masterizzarla su un CD o un DVD vuoto (se il computer ha un'unità CD o DVD).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="dbb3c-119">Se il computer in uso non ha un'unità per questo scopo, è possibile usare la maggior parte dei programmi generici usati per masterizzare CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="dbb3c-120">Selezionare l'architettura dell'immagine e specificare il percorso</span><span class="sxs-lookup"><span data-stu-id="dbb3c-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="dbb3c-121">Nella pagina Windows 10 Media selezionare se creare un'immagine di ripristino DaRT a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-121">On the Windows 10 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="dbb3c-122">Usa la versione di Windows a 32 bit per creare immagini di ripristino delle freccette a 32 bit e Windows a 64 bit per creare immagini di ripristino delle freccette a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="dbb3c-123">È possibile usare un singolo computer per creare immagini di ripristino per entrambi i tipi di architettura, ma non è possibile creare un'immagine che funzioni sia in architetture a 32 bit che a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="dbb3c-124">Indichi anche il percorso del supporto di installazione di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-124">You also indicate the path of the Windows 10 installation media.</span></span> <span data-ttu-id="dbb3c-125">Scegli l'architettura che corrisponde a quella dell'immagine di ripristino che stai creando.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="dbb3c-126">Per selezionare l'architettura dell'immagine e specificare il percorso</span><span class="sxs-lookup"><span data-stu-id="dbb3c-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="dbb3c-127">Nella pagina **Windows 10 media** selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-127">On the **Windows 10 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="dbb3c-128">Se si sta creando un'immagine di ripristino per i computer a 64 bit, selezionare **Crea immagine di dardo x64 (64 bit)**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="dbb3c-129">Se si sta creando un'immagine di ripristino per i computer a 32 bit, selezionare **Crea immagine di dardo x86 (32 bit)**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="dbb3c-130">Nella casella **specifica il percorso radice della finestra di dialogo per l'installazione di Windows 10 &lt; 64 &gt; bit o 32 bit** digitare il percorso dei file di installazione di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-130">In the **Specify the root path of the Windows 10 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 10 installation files.</span></span> <span data-ttu-id="dbb3c-131">Usare un percorso che corrisponda all'architettura dell'immagine di ripristino che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="dbb3c-132">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-132">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-133">Selezionare gli strumenti da includere nell'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="dbb3c-134">Nella pagina strumenti è possibile selezionare numerosi strumenti da includere nell'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="dbb3c-135">Questi strumenti saranno disponibili per gli utenti finali quando si avviano nell'immagine del dardo.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="dbb3c-136">Tuttavia, se si Abilita la connettività remota quando si crea l'immagine del dardo, tutti gli strumenti saranno disponibili quando un lavoratore dell'help desk si connette al computer dell'utente finale, indipendentemente dagli strumenti scelti per includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="dbb3c-137">Per limitare l'accesso degli utenti finali a questi strumenti, mantenendo comunque l'accesso completo agli strumenti tramite il Visualizzatore connessione remota, non selezionare questi strumenti nella pagina strumenti.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="dbb3c-138">Gli utenti finali potranno usare solo la connessione remota e saranno in grado di vedere, ma non di accedere, tutti gli strumenti che Escludi dall'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="dbb3c-139">Per selezionare gli strumenti da includere nell'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="dbb3c-140">Nella pagina **strumenti** selezionare la casella di controllo accanto a ogni strumento che si vuole includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="dbb3c-141">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-141">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-142">Scegliere se consentire la connettività remota tramite un help desk</span><span class="sxs-lookup"><span data-stu-id="dbb3c-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="dbb3c-143">Nella pagina connessione remota è possibile scegliere di consentire a un lavoratore dell'help desk di connettersi in remoto ed eseguire gli strumenti DaRT nel computer di un utente finale.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="dbb3c-144">L'opzione connettività remota viene quindi visualizzata come opzione disponibile nella finestra del set di strumenti di diagnostica e ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="dbb3c-145">Dopo che i dipendenti dell'help desk stabiliscono una connessione remota, possono eseguire gli strumenti DaRT nel computer dell'utente finale da una posizione remota.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="dbb3c-146">Per scegliere se consentire la connettività remota dagli operatori del supporto tecnico</span><span class="sxs-lookup"><span data-stu-id="dbb3c-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="dbb3c-147">Nella pagina **connessione remota** selezionare la casella di controllo **Consenti connessioni remote** per consentire connessioni remote o deselezionare la casella di controllo per impedire connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="dbb3c-148">Se la casella di controllo **Consenti connessioni remote** è stata deselezionata, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="dbb3c-149">In caso contrario, passare al passaggio successivo per continuare a configurare la connettività remota.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="dbb3c-150">Seleziona una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-150">Select one of the following:</span></span>

    -   <span data-ttu-id="dbb3c-151">Fare in modo che Windows scelga un numero di porta aperto.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="dbb3c-152">Specificare il numero di porta.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-152">Specify the port number.</span></span> <span data-ttu-id="dbb3c-153">Se si seleziona questa opzione, immettere un numero di porta compreso tra 1 e 65535 nel campo sotto l'opzione.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="dbb3c-154">Questo numero di porta verrà usato per stabilire una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="dbb3c-155">È consigliabile che il numero di porta sia 1024 o superiore per ridurre al minimo la possibilità di un conflitto.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="dbb3c-156">(Facoltativo) nella finestra del messaggio di **benvenuto della connessione remota** creare un messaggio personalizzato che gli utenti finali ricevono quando stabiliscono una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="dbb3c-157">Il messaggio può contenere un massimo di 2048 caratteri.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="dbb3c-158">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-158">Click **Next**.</span></span>

    <span data-ttu-id="dbb3c-159">Per altre informazioni sull'uso remoto degli strumenti DaRT, Vedi [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

## <span data-ttu-id="dbb3c-160">Aggiungere driver all'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="dbb3c-161">Nella scheda driver della pagina Opzioni avanzate è possibile aggiungere altri driver di dispositivo che potrebbero essere necessari per la riparazione di un computer.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="dbb3c-162">In genere possono includere controller di archiviazione o di rete non forniti da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-162">These may typically include storage or network controllers that Windows 10 does not provide.</span></span> <span data-ttu-id="dbb3c-163">I driver vengono installati quando viene creata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="dbb3c-164">**Importante**  Quando si selezionano i driver da includere, tenere presente che la connettività wireless (ad esempio Bluetooth o 802.11 a/b/g/n) non è supportata in DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="dbb3c-165">Per aggiungere driver all'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="dbb3c-166">Nella pagina **Opzioni avanzate** fare clic sulla scheda **driver** .</span><span class="sxs-lookup"><span data-stu-id="dbb3c-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="dbb3c-167">Fai clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-167">Click **Add**.</span></span>

3.  <span data-ttu-id="dbb3c-168">Passare al file da aggiungere per il driver e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="dbb3c-169">**Nota**  Il file del driver viene fornito dal produttore del controller di archiviazione o di rete.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="dbb3c-170">Ripetere i passaggi 2 e 3 per ogni driver che si desidera includere.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="dbb3c-171">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-171">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-172">Aggiungere pacchetti facoltativi di WinPE all'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="dbb3c-173">Nella scheda WinPE della pagina Opzioni avanzate puoi aggiungere pacchetti facoltativi di WinPE all'immagine DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="dbb3c-174">Questi pacchetti fanno parte di Windows ADK, un prerequisito per l'installazione della procedura guidata per l'immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbb3c-175">Gli strumenti che è possibile selezionare sono tutti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="dbb3c-176">Tutti i pacchetti necessari vengono aggiunti automaticamente, in base agli strumenti selezionati nella pagina strumenti.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="dbb3c-177">È anche possibile specificare le dimensioni dello spazio di Scratch.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="dbb3c-178">Scratch Space è la quantità di spazio su disco RAM che viene accantonata per l'esecuzione di DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="dbb3c-179">Lo spazio di Scratch è utile nel caso in cui il disco rigido dell'utente finale non sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="dbb3c-180">Se si stanno usando altri strumenti e driver, è consigliabile aumentare lo spazio di Scratch.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="dbb3c-181">Per aggiungere pacchetti facoltativi di WinPE all'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="dbb3c-182">Nella pagina **Opzioni avanzate** fare clic sulla scheda **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="dbb3c-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="dbb3c-183">Selezionare la casella di controllo accanto a ogni pacchetto che si vuole includere nell'immagine oppure fare clic sulla casella di controllo **nome** per selezionare tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="dbb3c-184">Nel campo **spazio di Scratch** selezionare la quantità di spazio su disco RAM da allocare per l'uso di freccette nel caso in cui il disco rigido dell'utente finale non sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="dbb3c-185">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-185">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-186">Aggiungere gli strumenti di debug per Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="dbb3c-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="dbb3c-187">Se si include lo strumento Analizzatore crash nell'immagine ISO, è necessario includere anche gli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="dbb3c-188">Nella scheda Analizzatore arresto anomalo della pagina Opzioni avanzate Immetti il percorso degli strumenti di debug di Windows 10, che analizza Crash Analyzer USA per analizzare i file di dump della memoria.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 10 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="dbb3c-189">È possibile usare gli strumenti presenti nel computer in cui è in uso la creazione guidata immagine di ripristino di freccette oppure usare gli strumenti presenti nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="dbb3c-190">Se si decide di usare gli strumenti nel computer dell'utente finale, tenere presente che tutti i computer diagnosticati devono disporre degli strumenti di debug installati.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="dbb3c-191">Se è stato installato Microsoft Windows Software Development Kit (SDK) o Microsoft Windows Development Kit (WDK), gli strumenti di debug di Windows 10 vengono aggiunti all'immagine di ripristino per impostazione predefinita e il percorso degli strumenti di debug viene compilato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 10 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="dbb3c-192">È possibile modificare il percorso degli strumenti di debug di Windows 10 se i file si trovano in un punto diverso da quello indicato dal percorso predefinito del file.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-192">You can change the path of the Windows 10 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="dbb3c-193">Un collegamento nella procedura guidata consente di scaricare e installare gli strumenti di debug per Windows, se non sono già installati.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="dbb3c-194">Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="dbb3c-195">Installare gli strumenti di debug nella posizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="dbb3c-196">**Nota**  La procedura guidata DaRT controlla gli strumenti nella `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="dbb3c-197">Se il valore del registro di sistema non è presente, la procedura guidata verrà eseguita in una delle posizioni seguenti, a seconda dell'architettura di sistemi:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**<span data-ttu-id="dbb3c-198">Per aggiungere gli strumenti di debug per Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="dbb3c-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="dbb3c-199">Nella pagina **Opzioni avanzate** fare clic sulla scheda **analizzatore crash** .</span><span class="sxs-lookup"><span data-stu-id="dbb3c-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="dbb3c-200">Opzionale Fare clic su **Scarica gli strumenti di debug** per scaricare gli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="dbb3c-201">Selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="dbb3c-202">**Includere gli strumenti di debug di Windows 10 &lt; 64 bit o &gt; 32**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-202">**Include the Windows 10 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="dbb3c-203">Se si seleziona questa opzione, individuare e selezionare la posizione degli strumenti se il percorso non è già visualizzato.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="dbb3c-204">**Usare gli strumenti di debug del sistema di cui si sta**eseguendo il debugger.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="dbb3c-205">Se si seleziona questa opzione, l'analizzatore crash non funzionerà se gli strumenti di debug per Windows non vengono trovati nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="dbb3c-206">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-206">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-207">Selezionare i tipi di file di immagine di ripristino da creare</span><span class="sxs-lookup"><span data-stu-id="dbb3c-207">Select the types of recovery image files to create</span></span>


<span data-ttu-id="dbb3c-208">Nella pagina Crea immagine Scegli una cartella di output per l'immagine di ripristino, immetti un nome di immagine e seleziona i tipi di file di immagine di recupero DaRT da creare.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-208">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="dbb3c-209">Durante il processo di creazione di immagini di ripristino, i file di origine di Windows vengono spacchettati, i file di freccette vengono copiati e l'immagine viene quindi "reimballata" nei formati di file selezionati in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-209">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="dbb3c-210">I tipi di file immagine disponibili sono:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-210">The available image file types are:</span></span>

-   <span data-ttu-id="dbb3c-211">**File Windows Imaging (wim)** : consente di distribuire il dardo in un ambiente PXE (Preboot Execution Environment) o in una partizione locale.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-211">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="dbb3c-212">**ISO (International Standards Organization)** : usato per la distribuzione su CD o DVD oppure per l'uso in macchine virtuali (VM).</span><span class="sxs-lookup"><span data-stu-id="dbb3c-212">**International Standards Organization (ISO)** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="dbb3c-213">La procedura guidata richiede che l'immagine ISO abbia un'estensione di file ISO, perché la maggior parte dei programmi che masterizzano un CD o un DVD richiedono tale estensione.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-213">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="dbb3c-214">Se non specifichi una posizione diversa, l'immagine ISO viene creata sul desktop con il nome DaRT10. ISO.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-214">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT10.ISO.</span></span>

-   <span data-ttu-id="dbb3c-215">**Script di PowerShell** : crea un'immagine di ripristino DaRT con comandi che contengono essenzialmente le stesse opzioni che puoi selezionare usando la creazione guidata immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-215">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="dbb3c-216">Lo script consente inoltre di aggiungere o modificare i file nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-216">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="dbb3c-217">Se si seleziona la casella di controllo modifica immagine in questa pagina, è possibile personalizzare l'immagine di ripristino durante il processo di creazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-217">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="dbb3c-218">Ad esempio, è possibile modificare il file "winpeshl.ini" per creare un ordine di avvio personalizzato o per aggiungere strumenti di terze parti.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-218">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="dbb3c-219">Per selezionare i tipi di file di immagine di ripristino da creare</span><span class="sxs-lookup"><span data-stu-id="dbb3c-219">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="dbb3c-220">Nella pagina **Crea immagine** fare clic su **Sfoglia** per scegliere la cartella di output per il file di immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-220">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="dbb3c-221">**Nota**  Le dimensioni dell'immagine variano a seconda degli strumenti selezionati e dei file che si aggiungono nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-221">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="dbb3c-222">Nella casella **nome immagine** immettere un nome per l'immagine di ripristino DaRT o accettare il nome predefinito, ovvero DaRT10.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-222">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT10.</span></span>

    <span data-ttu-id="dbb3c-223">La procedura guidata crea una sottocartella nel percorso di output con questo nome.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-223">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="dbb3c-224">Selezionare i tipi di file di immagine che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-224">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="dbb3c-225">Scegliere una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbb3c-225">Choose one of the following:</span></span>

    -   <span data-ttu-id="dbb3c-226">Per modificare i file nell'immagine di ripristino prima di creare i file di immagine, selezionare la casella di controllo **modifica immagine** e quindi fare clic su **prepara**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-226">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="dbb3c-227">Per creare l'immagine di ripristino senza modificare i file, fare clic su **Crea**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-227">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="dbb3c-228">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-228">Click **Next**.</span></span>

## <span data-ttu-id="dbb3c-229">Modificare i file di immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-229">Edit the recovery image files</span></span>


<span data-ttu-id="dbb3c-230">È possibile modificare l'immagine di ripristino solo se è stata selezionata la casella di controllo modifica immagine nella pagina Crea immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-230">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="dbb3c-231">Dopo aver preparato l'immagine di ripristino per la modifica, è possibile aggiungere e modificare i file di immagine di ripristino prima di creare il supporto di avvio.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-231">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="dbb3c-232">Ad esempio, puoi creare un ordine personalizzato per l'avvio, aggiungere vari strumenti di terze parti e così via.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-232">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="dbb3c-233">Per modificare i file di immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-233">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="dbb3c-234">Nella pagina **modifica immagine** fare clic su **Apri** in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-234">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="dbb3c-235">Creare una sottocartella nella cartella elencata nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-235">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="dbb3c-236">Copiare i file desiderati nella nuova sottocartella oppure rimuovere i file che non si desidera.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-236">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="dbb3c-237">Fare clic su **Crea** per iniziare a creare l'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-237">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="dbb3c-238">Generare i file di immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-238">Generate the recovery image files</span></span>


<span data-ttu-id="dbb3c-239">Nella pagina genera file viene generata l'immagine di ripristino DaRT per i tipi di file selezionati nella pagina Crea immagine.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-239">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="dbb3c-240">Per generare i file di immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="dbb3c-240">To generate the recovery image files</span></span>**

-   <span data-ttu-id="dbb3c-241">Nella pagina **genera file** fare clic su **Avanti** per generare i file di immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-241">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="dbb3c-242">Copiare l'immagine di ripristino in un CD, un DVD o un USB</span><span class="sxs-lookup"><span data-stu-id="dbb3c-242">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="dbb3c-243">Nella pagina Crea supporto avviabile è possibile copiare facoltativamente il file di immagine in un CD, un DVD o un'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-243">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="dbb3c-244">È anche possibile creare altri elementi multimediali avviabili da questa pagina riavviando la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-244">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="dbb3c-245">**Nota**  Il programma PXE (Preboot Execution Environment) e la distribuzione di immagini locali non sono supportati in modo nativo da questo strumento, poiché richiedono strumenti aziendali aggiuntivi, ad esempio System Center Configuration Manager Server e Microsoft Development Toolkit.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-245">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="dbb3c-246">Per copiare l'immagine di ripristino in un CD, un DVD o un USB</span><span class="sxs-lookup"><span data-stu-id="dbb3c-246">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="dbb3c-247">Nella pagina **Crea supporto avviabile** selezionare il file ISO che si vuole copiare.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-247">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="dbb3c-248">Inserire un CD, un DVD o un USB e quindi selezionare l'unità.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-248">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="dbb3c-249">**Nota**  Se un'unità non viene riconosciuta e si installa una nuova unità, è possibile fare clic su **Aggiorna** per forzare la procedura guidata ad aggiornare l'elenco delle unità disponibili.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-249">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="dbb3c-250">Fare clic sul pulsante **Crea supporto avviabile** .</span><span class="sxs-lookup"><span data-stu-id="dbb3c-250">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="dbb3c-251">Per creare un'altra immagine di ripristino, fare clic su Riavvia oppure su **Chiudi** se è stata completata la creazione di tutto il contenuto multimediale desiderato.</span><span class="sxs-lookup"><span data-stu-id="dbb3c-251">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="dbb3c-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbb3c-252">Related topics</span></span>


[<span data-ttu-id="dbb3c-253">Panoramica degli strumenti di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="dbb3c-253">Overview of the Tools in DaRT 10</span></span>](overview-of-the-tools-in-dart-10.md)

[<span data-ttu-id="dbb3c-254">Distribuzione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="dbb3c-254">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





