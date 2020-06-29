---
title: Come creare un acceleratore pacchetto
description: Come creare un acceleratore pacchetto
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805607"
---
# <span data-ttu-id="21209-103">Come creare un acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="21209-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="21209-104">Gli acceleratori del pacchetto App-V 5,0 generano automaticamente nuovi pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="21209-104">App-V 5.0 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="21209-105">Nota</span><span class="sxs-lookup"><span data-stu-id="21209-105">Note</span></span>**  
<span data-ttu-id="21209-106">Puoi usare PowerShell per creare un Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="21209-107">Per altre informazioni [, vedere come creare un Acceleratore pacchetto usando PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="21209-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span></span>



<span data-ttu-id="21209-108">Per creare un Acceleratore pacchetto, usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="21209-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="21209-109">Importante</span><span class="sxs-lookup"><span data-stu-id="21209-109">Important</span></span>**  
<span data-ttu-id="21209-110">Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21209-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="21209-111">È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="21209-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>



**<span data-ttu-id="21209-112">Importante</span><span class="sxs-lookup"><span data-stu-id="21209-112">Important</span></span>**  
<span data-ttu-id="21209-113">Prima di iniziare la procedura seguente, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="21209-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="21209-114">Copiare il pacchetto di applicazione virtuale che verrà usato per creare l'Acceleratore pacchetto in locale nel computer che gestisce il sequencer.</span><span class="sxs-lookup"><span data-stu-id="21209-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="21209-115">Copiare tutti i file di installazione necessari associati al pacchetto di applicazione virtuale nel computer in cui è in uso Sequencer.</span><span class="sxs-lookup"><span data-stu-id="21209-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="21209-116">Per creare un Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="21209-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="21209-117">Importante</span><span class="sxs-lookup"><span data-stu-id="21209-117">Important</span></span>**  
    <span data-ttu-id="21209-118">L'App-V 5,0 sequencer non concede diritti di licenza per l'applicazione software in uso per creare l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-118">The App-V 5.0 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="21209-119">È necessario rispettare tutte le condizioni di licenza per l'utente finale per l'applicazione in uso.</span><span class="sxs-lookup"><span data-stu-id="21209-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="21209-120">È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando l'App-V 5,0 sequencer.</span><span class="sxs-lookup"><span data-stu-id="21209-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.0 Sequencer.</span></span>



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="21209-121">Per avviare l'app-v 5,0 **creazione guidata pacchetto acceleratore** , nella console di sequencer App-v 5,0 fare clic su **strumenti**  /  **Crea Acceleratore**.</span><span class="sxs-lookup"><span data-stu-id="21209-121">To start the App-V 5.0 **Create Package Accelerator** wizard, in the App-V 5.0 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="21209-122">Nella pagina **Seleziona pacchetto** , per specificare un pacchetto di applicazione virtuale esistente da usare per creare l'Acceleratore pacchetto, fare clic su **Sfoglia**e individuare il pacchetto di applicazione virtuale esistente (file con estensione appv).</span><span class="sxs-lookup"><span data-stu-id="21209-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="21209-123">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="21209-123">Tip</span></span>**  
   <span data-ttu-id="21209-124">Copiare i file associati al pacchetto di applicazione virtuale che si prevede di usare localmente per il computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="21209-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="21209-125">Nella pagina **file di installazione** per specificare la cartella che contiene i file di installazione usati per creare il pacchetto di applicazione virtuale originale, fare clic su **Sfoglia**e quindi selezionare la directory contenente i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="21209-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="21209-126">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="21209-126">Tip</span></span>**  
   <span data-ttu-id="21209-127">Copiare la cartella che contiene i file di installazione necessari nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="21209-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="21209-128">Se l'applicazione è già installata nel computer in cui è in uso il sequencer, per specificare il file di installazione, selezionare **file installati nel sistema locale**.</span><span class="sxs-lookup"><span data-stu-id="21209-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="21209-129">Per usare questa opzione, l'applicazione deve essere già installata nel percorso di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="21209-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="21209-130">Nella pagina **raccolta informazioni** esaminare i file che non sono stati trovati nella posizione specificata nella pagina file di **installazione** della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="21209-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="21209-131">Se i file visualizzati non sono obbligatori, selezionare **Rimuovi questi file**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="21209-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="21209-132">Se i file sono necessari, fare clic su **precedente** e copiare i file necessari nella directory specificata nella pagina **file di installazione** .</span><span class="sxs-lookup"><span data-stu-id="21209-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="21209-133">Nota</span><span class="sxs-lookup"><span data-stu-id="21209-133">Note</span></span>**  
   <span data-ttu-id="21209-134">Per passare alla pagina successiva della procedura guidata, è necessario rimuovere i file non necessari oppure fare clic su **precedente** e individuare i file necessari.</span><span class="sxs-lookup"><span data-stu-id="21209-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="21209-135">Nella pagina **Seleziona file** esaminare attentamente i file rilevati e deselezionare qualsiasi file che deve essere rimosso dall'acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="21209-136">Selezionare solo i file necessari per l'esecuzione corretta dell'applicazione e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="21209-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="21209-137">Nella pagina **Verifica applicazioni verificare** che tutti i file di installazione necessari per compilare il pacchetto vengano visualizzati.</span><span class="sxs-lookup"><span data-stu-id="21209-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="21209-138">Quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto, tutti i file di installazione visualizzati nel riquadro **applicazioni** sono necessari per creare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="21209-139">Se necessario, per aggiungere altri file di installazione, fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="21209-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="21209-140">Per rimuovere i file di installazione non necessari, selezionarlo e quindi fare clic su **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="21209-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="21209-141">Per modificare le proprietà associate a un programma di installazione, fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="21209-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="21209-142">I file di installazione specificati in questo passaggio saranno necessari quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="21209-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="21209-143">Dopo aver confermato le informazioni visualizzate, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="21209-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="21209-144">Nella pagina **Seleziona linee guida** per specificare un file che contiene informazioni sul modo in cui l'acceleratore del pacchetto fa clic su **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="21209-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="21209-145">Ad esempio, questo file può contenere informazioni sul modo in cui il computer che eseguono il Sequencer deve essere configurato, informazioni sui prerequisiti dell'applicazione per i computer di destinazione e note generali.</span><span class="sxs-lookup"><span data-stu-id="21209-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="21209-146">Devi specificare tutte le informazioni necessarie per applicare correttamente l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="21209-147">Il file selezionato deve essere in formato RTF (Rich Text) o file di testo (txt).</span><span class="sxs-lookup"><span data-stu-id="21209-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="21209-148">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="21209-148">Click **Next**.</span></span>

10. <span data-ttu-id="21209-149">Nella pagina **Crea Acceleratore pacchetto** , per specificare dove salvare l'Acceleratore pacchetto, fare clic su **Sfoglia** e selezionare la directory.</span><span class="sxs-lookup"><span data-stu-id="21209-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="21209-150">Nella pagina **completamento** , per chiudere la procedura guidata **Crea accelerazione pacchetto** , fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="21209-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="21209-151">Importante</span><span class="sxs-lookup"><span data-stu-id="21209-151">Important</span></span>**  
   <span data-ttu-id="21209-152">Per assicurarti che l'acceleratore del pacchetto sia il più sicuro possibile e che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto, devi sempre firmare digitalmente l'acceleratore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="21209-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="21209-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21209-153">Related topics</span></span>


[<span data-ttu-id="21209-154">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="21209-154">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="21209-155">Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V</span><span class="sxs-lookup"><span data-stu-id="21209-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)









