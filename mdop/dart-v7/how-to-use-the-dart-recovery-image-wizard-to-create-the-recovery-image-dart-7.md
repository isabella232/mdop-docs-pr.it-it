---
title: Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino
description: Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822925"
---
# <span data-ttu-id="e457d-103">Come usare la procedura guidata immagine di ripristino di DaRT per creare l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="e457d-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="e457d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include la **procedura guidata** per l'immagine di ripristino delle freccette usata in Windows per creare un'immagine dell'organizzazione internazionale per la standardizzazione (ISO) avviabile.</span><span class="sxs-lookup"><span data-stu-id="e457d-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="e457d-105">Un'immagine ISO è un file che rappresenta il contenuto non elaborato di un CD.</span><span class="sxs-lookup"><span data-stu-id="e457d-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="e457d-106">La **procedura guidata immagine di ripristino di freccette** richiede le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e457d-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="e457d-107">**Immagine di avvio**˚ ˚ è necessario specificare il percorso di un file di origine di Windows 7 DVD o Windows 7 necessario per creare l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="e457d-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="e457d-108">**Strumento di selezione**˚ ˚ è possibile selezionare gli strumenti da includere nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="e457d-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="e457d-109">**Connessioni remote**˚ ˚ è possibile specificare se si vuole che l'immagine di ripristino delle freccette includa la possibilità di stabilire una connessione remota tra l'helpdesk e il computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e457d-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="e457d-110">**Strumenti di debug per Windows**˚ ˚ viene richiesto di specificare la posizione degli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="e457d-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="e457d-111">**Definizioni per il sistema autonomo Sweeper**˚ ˚ è possibile decidere se scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino o scaricare le definizioni in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="e457d-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="e457d-112">**Driver**˚ ˚ viene chiesto se si vuole aggiungere driver all'immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="e457d-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="e457d-113">**File aggiuntivi**˚ ˚ è possibile aggiungere file all'immagine ISO che potrebbero essere utili per la diagnosi dei problemi.</span><span class="sxs-lookup"><span data-stu-id="e457d-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="e457d-114">**Posizione dell'immagine ISO**˚ ˚ viene chiesto di specificare dove deve essere posizionata l'immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="e457d-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="e457d-115">**Unità CD/DVD**˚ ˚ viene chiesto di specificare se usare l'unità CD o DVD per masterizzare il CD o il DVD.</span><span class="sxs-lookup"><span data-stu-id="e457d-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="e457d-116">**Nota**  Le dimensioni dell'immagine ISO possono variare a seconda degli strumenti selezionati nella **creazione guidata immagine di ripristino di Dart**.</span><span class="sxs-lookup"><span data-stu-id="e457d-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="e457d-117">Per creare l'immagine di ripristino usando la creazione guidata immagine di ripristino di freccette</span><span class="sxs-lookup"><span data-stu-id="e457d-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="e457d-118">Seguire queste istruzioni per usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="e457d-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="e457d-119">Per selezionare gli strumenti da includere nell'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="e457d-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="e457d-120">La **procedura guidata immagine recupero dardo** presenta una finestra di dialogo di **selezione dello strumento** .</span><span class="sxs-lookup"><span data-stu-id="e457d-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="e457d-121">È possibile selezionare o rimuovere strumenti dall'elenco di strumenti da includere nell'immagine di ripristino delle freccette evidenziando uno strumento e quindi facendo clic sui pulsanti **Abilita** o **Disabilita** .</span><span class="sxs-lookup"><span data-stu-id="e457d-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="e457d-122">Dopo aver selezionato tutti gli strumenti che si desidera includere nell'immagine di ripristino, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="e457d-123">Per aggiungere l'opzione per consentire la connettività remota</span><span class="sxs-lookup"><span data-stu-id="e457d-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="e457d-124">È possibile selezionare la casella di controllo **Consenti connessioni remote** per specificare l'opzione nella finestra del **set di strumenti di diagnostica e ripristino** per stabilire una connessione remota tra l'agente helpdesk e un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e457d-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="e457d-125">Dopo che un agente dell'helpdesk stabilisce una connessione remota, può eseguire gli strumenti DaRT nel computer dell'utente finale da una posizione remota.</span><span class="sxs-lookup"><span data-stu-id="e457d-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="e457d-126">È possibile selezionare la casella di controllo **specifica il numero di porta** per immettere un numero di porta specifico che verrà usato per stabilire una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e457d-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="e457d-127">È possibile specificare un numero di porta compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e457d-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="e457d-128">È consigliabile che il numero di porta sia 1024 o superiore per ridurre al minimo la possibilità di un conflitto.</span><span class="sxs-lookup"><span data-stu-id="e457d-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="e457d-129">È anche possibile creare un messaggio personalizzato che verrà ricevuto da un utente finale quando stabilisce una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e457d-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="e457d-130">Il messaggio può contenere un massimo di 2048 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e457d-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="e457d-131">Per altre informazioni su come eseguire in remoto gli strumenti DaRT, Vedi [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="e457d-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="e457d-132">Per aggiungere gli strumenti di debug per Windows all'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="e457d-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="e457d-133">Nella finestra di dialogo **analizzatore crash** della **creazione guidata immagine di ripristino di freccette**viene richiesto di specificare la posizione degli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="e457d-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="e457d-134">Se non si dispone di una copia degli strumenti, è possibile scaricarli da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e457d-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="e457d-135">Il collegamento seguente alla pagina di download è disponibile nella procedura guidata: [scaricare e installare gli strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="e457d-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="e457d-136">È possibile specificare la posizione degli strumenti di debug nel computer in cui è in uso la **creazione guidata immagine di ripristino di freccette**oppure si può decidere di usare gli strumenti disponibili nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e457d-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="e457d-137">Se si decide di usare una copia in un altro computer, è necessario assicurarsi che gli strumenti siano installati in ogni computer in cui si sta effettuando la diagnosi di un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="e457d-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="e457d-138">**Nota**  Se si include l' **analizzatore crash** nell'immagine ISO, è consigliabile includere anche gli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="e457d-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="e457d-139">Seguire questa procedura per aggiungere gli strumenti di debug per Windows:</span><span class="sxs-lookup"><span data-stu-id="e457d-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="e457d-140">Opzionale Fare clic sul collegamento ipertestuale per scaricare gli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="e457d-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="e457d-141">Selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e457d-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="e457d-142">**Usare gli strumenti di debug per Windows nella posizione seguente**.</span><span class="sxs-lookup"><span data-stu-id="e457d-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="e457d-143">Se si seleziona questa opzione, è possibile passare alla posizione degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e457d-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="e457d-144">**Individuare gli strumenti di debug per Windows nel sistema che si sta ripristinando**.</span><span class="sxs-lookup"><span data-stu-id="e457d-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="e457d-145">Se si seleziona questa opzione, l' **analizzatore crash** non funzionerà se gli strumenti di debug per Windows non vengono trovati nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="e457d-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="e457d-146">Al termine, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="e457d-147">Per aggiungere definizioni per la spazzatrice di sistema autonoma all'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="e457d-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="e457d-148">Le definizioni sono un repository di malware noti e di altri software potenzialmente indesiderati.</span><span class="sxs-lookup"><span data-stu-id="e457d-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="e457d-149">Poiché il malware viene continuamente sviluppato, la **spazzatrice di sistema autonoma** si basa sulle definizioni correnti per determinare se il software che sta provando a installare, eseguire o modificare le impostazioni in un computer è un software potenzialmente indesiderato o malevolo.</span><span class="sxs-lookup"><span data-stu-id="e457d-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="e457d-150">Per includere le definizioni più recenti nell'immagine di ripristino delle freccette (scelta consigliata), fare clic su **Sì, scaricare le definizioni più recenti.**</span><span class="sxs-lookup"><span data-stu-id="e457d-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="e457d-151">L'aggiornamento della definizione viene avviato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e457d-151">The definition update starts automatically.</span></span> <span data-ttu-id="e457d-152">Per completare il processo, è necessario essere connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="e457d-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="e457d-153">Per ignorare l'aggiornamento della definizione, fare clic su **No, scaricare manualmente le definizioni in un secondo momento**.</span><span class="sxs-lookup"><span data-stu-id="e457d-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="e457d-154">Le definizioni non verranno incluse nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="e457d-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="e457d-155">Se si decide di non includere le definizioni più recenti nell'immagine di ripristino o se le definizioni incluse nell'immagine di ripristino non sono più aggiornate quando si è pronti per **l'uso,** è possibile ottenere le definizioni più recenti prima di iniziare un'analisi seguendo le istruzioni fornite nella **spazzatrice di sistema autonomo**.</span><span class="sxs-lookup"><span data-stu-id="e457d-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="e457d-156">**Importante**  Non è possibile eseguire la digitalizzazione se non sono presenti definizioni.</span><span class="sxs-lookup"><span data-stu-id="e457d-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="e457d-157">Al termine, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="e457d-158">Per aggiungere driver all'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="e457d-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="e457d-159">**Attenzione**  Per impostazione predefinita, quando si aggiunge un driver all'immagine di ripristino DaRT, tutti i file e le sottocartelle presenti in tale cartella vengono aggiunti all'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e457d-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="e457d-160">Per altre informazioni, vedere [risoluzione dei problemi relativi a DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="e457d-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="e457d-161">È consigliabile includere altri driver nell'immagine di ripristino per DaRT7 che potrebbe essere necessario quando si ripristina un computer.</span><span class="sxs-lookup"><span data-stu-id="e457d-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="e457d-162">In genere possono includere controller di archiviazione o di rete non inclusi in Windows DVD.</span><span class="sxs-lookup"><span data-stu-id="e457d-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="e457d-163">**Importante**  Quando si selezionano i driver da includere, tenere presente che la connettività wireless (ad esempio Bluetooth o 802.11 a/b/g/n) non è supportata in DaRT.</span><span class="sxs-lookup"><span data-stu-id="e457d-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="e457d-164">Per aggiungere un driver di archiviazione o controller di rete all'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="e457d-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="e457d-165">Nella finestra di dialogo **driver aggiuntivi** della **creazione guidata immagine di ripristino di freccette**fare clic su **Aggiungi dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="e457d-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="e457d-166">Passare al file da aggiungere per il driver e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="e457d-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="e457d-167">**Nota**  Il file del **driver** viene fornito dal produttore del controller di archiviazione o di rete.</span><span class="sxs-lookup"><span data-stu-id="e457d-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="e457d-168">Ripetere i passaggi 1 e 2 per ogni driver che si desidera includere.</span><span class="sxs-lookup"><span data-stu-id="e457d-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="e457d-169">Al termine, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="e457d-170">Per aggiungere file all'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="e457d-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="e457d-171">Seguire questa procedura per aggiungere file all'immagine di ripristino, in modo da poterli usare per diagnosticare i problemi del computer.</span><span class="sxs-lookup"><span data-stu-id="e457d-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="e457d-172">Nella finestra di dialogo **file aggiuntivi** della **creazione guidata immagine di ripristino di freccette**fare clic su **Mostra file**.</span><span class="sxs-lookup"><span data-stu-id="e457d-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="e457d-173">Verrà aperta una finestra di Esplora risorse che visualizza la cartella che contiene i file condivisi.</span><span class="sxs-lookup"><span data-stu-id="e457d-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="e457d-174">Creare una sottocartella nella cartella elencata nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e457d-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="e457d-175">Copiare i file desiderati nella nuova sottocartella.</span><span class="sxs-lookup"><span data-stu-id="e457d-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="e457d-176">Al termine, fare clic su **Avanti.**</span><span class="sxs-lookup"><span data-stu-id="e457d-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="e457d-177">Per selezionare una posizione per l'ISO che contiene l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="e457d-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="e457d-178">Seguire questa procedura per specificare la posizione in cui viene creata l'immagine ISO:</span><span class="sxs-lookup"><span data-stu-id="e457d-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="e457d-179">Nella finestra di dialogo **Crea immagine di avvio** della **creazione guidata immagine di ripristino di freccette**fare clic su **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="e457d-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="e457d-180">Passare alla posizione preferita nella finestra **Salva con nome** e quindi fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="e457d-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="e457d-181">Al termine, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="e457d-182">Le dimensioni dell'immagine ISO variano a seconda degli strumenti selezionati e dei file che si aggiungono nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e457d-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="e457d-183">La procedura guidata richiede che l'immagine ISO abbia un'estensione di file **ISO,** perché la maggior parte dei programmi che masterizzano un CD o un DVD richiedono tale estensione.</span><span class="sxs-lookup"><span data-stu-id="e457d-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="e457d-184">Se non specifichi una posizione diversa, l'immagine ISO viene creata sul desktop con il nome **DaRT70. ISO**.</span><span class="sxs-lookup"><span data-stu-id="e457d-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="e457d-185">Per masterizzare l'immagine di ripristino su un CD o un DVD</span><span class="sxs-lookup"><span data-stu-id="e457d-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="e457d-186">Se la **procedura guidata** per l'immagine di ripristino di freccette rileva un'unità CD-RW compatibile nel computer, offre di masterizzare l'immagine ISO su un disco.</span><span class="sxs-lookup"><span data-stu-id="e457d-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="e457d-187">Se si vuole masterizzare un CD o un DVD e la procedura guidata non riconosce l'unità, è necessario usare un altro programma, ad esempio il programma incluso nell'unità.</span><span class="sxs-lookup"><span data-stu-id="e457d-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="e457d-188">È possibile usare un duplicatore, un servizio di duplicazione o un software di masterizzazione CD o DVD per apportare altre copie.</span><span class="sxs-lookup"><span data-stu-id="e457d-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="e457d-189">Nella finestra di dialogo **Masterizza in un CD/DVD registrabile** della **procedura guidata immagine di ripristino di freccette**Selezionare **brucia l'immagine per l'unità CD/DVD registrabile seguente**.</span><span class="sxs-lookup"><span data-stu-id="e457d-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="e457d-190">Selezionare l'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="e457d-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="e457d-191">**Nota**  Se un'unità non viene riconosciuta e si installa una nuova unità, è possibile fare clic su **Aggiorna elenco unità** per forzare la procedura guidata ad aggiornare l'elenco delle unità disponibili.</span><span class="sxs-lookup"><span data-stu-id="e457d-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="e457d-192">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e457d-192">Click **Next**.</span></span>

## <span data-ttu-id="e457d-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e457d-193">Related topics</span></span>


[<span data-ttu-id="e457d-194">Creazione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="e457d-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





