---
title: Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)
description: Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817636"
---
# <span data-ttu-id="118b2-103">Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="118b2-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="118b2-104">Puoi usare gli acceleratori pacchetto di App-V per generare automaticamente un nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="118b2-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="118b2-105">Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="118b2-106">Per altre informazioni sugli acceleratori di pacchetto, vedere [informazioni sugli acceleratori di pacchetti App-v (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="118b2-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="118b2-107">La creazione di acceleratori pacchetto App-V è un'attività avanzata.</span><span class="sxs-lookup"><span data-stu-id="118b2-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="118b2-108">Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="118b2-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="118b2-109">È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="118b2-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="118b2-110">In alcune situazioni, per creare l'Acceleratore pacchetto, potrebbe essere necessario installare l'applicazione localmente nel computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="118b2-111">Prima di tutto, prova a creare l'Acceleratore pacchetto usando il supporto di installazione e se sono presenti diversi file mancanti, installa l'applicazione localmente nel computer che esegue il sequencer e quindi crea l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="118b2-112">Importante</span><span class="sxs-lookup"><span data-stu-id="118b2-112">Important</span></span>**  
<span data-ttu-id="118b2-113">Prima di iniziare la procedura seguente, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="118b2-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="118b2-114">Copiare il pacchetto di applicazione virtuale che deve essere usato per creare l'Acceleratore pacchetto in locale nel computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="118b2-115">Copiare tutti i file di installazione necessari associati al pacchetto di applicazione virtuale nel computer in cui è in uso Sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="118b2-116">Importante</span><span class="sxs-lookup"><span data-stu-id="118b2-116">Important</span></span>**  
<span data-ttu-id="118b2-117">Dichiarazione di non responsabilità: Microsoft Application Virtualization Sequencer non offre alcun diritto di licenza per l'applicazione software in uso per creare un Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="118b2-118">È necessario rispettare tutte le condizioni di licenza per l'utente finale per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="118b2-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="118b2-119">È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="118b2-120">Per creare un Acceleratore pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="118b2-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="118b2-121">Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.</span><span class="sxs-lookup"><span data-stu-id="118b2-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="118b2-122">Per avviare l'app-v **creare l'acceleratore guidata pacchetto** , in App-v Sequencer fare clic su **strumenti**  /  **Crea pacchetto acceleratore**.</span><span class="sxs-lookup"><span data-stu-id="118b2-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="118b2-123">Nella pagina **Seleziona pacchetto** , per specificare un pacchetto di applicazione virtuale esistente da usare per creare l'Acceleratore pacchetto, fare clic su **Sfoglia**e individuare il pacchetto di applicazione virtuale esistente (file con estensione SPRJ).</span><span class="sxs-lookup"><span data-stu-id="118b2-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="118b2-124">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="118b2-124">Tip</span></span>**  
    <span data-ttu-id="118b2-125">Copiare i file associati al pacchetto di applicazione virtuale che si prevede di usare localmente per il computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="118b2-126">Nella pagina **file di installazione** per specificare la cartella che contiene i file di installazione usati per creare il pacchetto di applicazione virtuale originale, fare clic su **Sfoglia**e quindi selezionare la directory contenente i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="118b2-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="118b2-127">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="118b2-127">Tip</span></span>**  
   <span data-ttu-id="118b2-128">Copiare la cartella che contiene i file di installazione necessari nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="118b2-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="118b2-129">Nella pagina **raccolta informazioni** esaminare i file che non sono stati trovati nella posizione specificata nella pagina file di **installazione** della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="118b2-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="118b2-130">Se i file visualizzati non sono obbligatori, selezionare **Rimuovi questi file**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="118b2-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="118b2-131">Se i file sono necessari, fare clic su **precedente** e copiare i file necessari nella directory specificata nella pagina **file di installazione** .</span><span class="sxs-lookup"><span data-stu-id="118b2-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="118b2-132">Nota</span><span class="sxs-lookup"><span data-stu-id="118b2-132">Note</span></span>**  
   <span data-ttu-id="118b2-133">Per passare alla pagina successiva della procedura guidata, è necessario rimuovere i file non necessari oppure fare clic su **precedente** e individuare i file necessari.</span><span class="sxs-lookup"><span data-stu-id="118b2-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="118b2-134">Nella pagina **Seleziona file** esaminare attentamente i file rilevati e deselezionare qualsiasi file che deve essere rimosso dall'acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="118b2-135">Selezionare solo i file necessari per l'esecuzione corretta dell'applicazione e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="118b2-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="118b2-136">Nella pagina **Verifica applicazioni verificare** che tutti i file di installazione necessari per compilare il pacchetto vengano visualizzati.</span><span class="sxs-lookup"><span data-stu-id="118b2-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="118b2-137">Quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto, tutti i file di installazione visualizzati nel riquadro **applicazioni** sono necessari per creare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="118b2-138">Se necessario, per aggiungere altri file di installazione, fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="118b2-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="118b2-139">Per rimuovere i file di installazione non necessari, selezionarlo e quindi fare clic su **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="118b2-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="118b2-140">Per modificare le proprietà associate a un programma di installazione, fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="118b2-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="118b2-141">I file di installazione specificati in questo passaggio saranno necessari quando viene usato l'Acceleratore pacchetto per creare un nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="118b2-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="118b2-142">Dopo aver confermato le informazioni visualizzate, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="118b2-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="118b2-143">Nella pagina **Seleziona linee guida** per specificare un file che contiene informazioni sul modo in cui l'acceleratore del pacchetto fa clic su **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="118b2-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="118b2-144">Ad esempio, questo file può contenere informazioni sul modo in cui il computer che eseguono il Sequencer deve essere configurato, informazioni sui prerequisiti dell'applicazione per i computer di destinazione e note generali.</span><span class="sxs-lookup"><span data-stu-id="118b2-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="118b2-145">Devi specificare tutte le informazioni necessarie per applicare correttamente l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="118b2-146">Il file selezionato deve essere in formato RTF (Rich Text) o file di testo (txt).</span><span class="sxs-lookup"><span data-stu-id="118b2-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="118b2-147">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="118b2-147">Click **Next**.</span></span>

9. <span data-ttu-id="118b2-148">Nella pagina **Crea Acceleratore pacchetto** , per specificare dove salvare l'Acceleratore pacchetto, fare clic su **Sfoglia** e selezionare la directory.</span><span class="sxs-lookup"><span data-stu-id="118b2-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="118b2-149">Nella pagina **completamento** , per chiudere la procedura guidata **Crea accelerazione pacchetto** , fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="118b2-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="118b2-150">Importante</span><span class="sxs-lookup"><span data-stu-id="118b2-150">Important</span></span>**  
   <span data-ttu-id="118b2-151">Per assicurarti che l'acceleratore del pacchetto sia il più sicuro possibile e che il Publisher possa essere verificato quando viene applicato l'Acceleratore pacchetto, devi sempre firmare digitalmente l'acceleratore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="118b2-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="118b2-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="118b2-152">Related topics</span></span>


<span data-ttu-id="118b2-153">Configurazione dell'Application Virtualization Sequencer (App-V 4,6 SP1) [come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (app-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="118b2-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









