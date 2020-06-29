---
title: Come configurare un pacchetto di distribuzione
description: Come configurare un pacchetto di distribuzione
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825946"
---
# <span data-ttu-id="82899-103">Come configurare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="82899-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="82899-104">La procedura guidata per la creazione di pacchetti illustra come creare una cartella nel computer locale e trasferire tutti i file di installazione necessari alla singola cartella.</span><span class="sxs-lookup"><span data-stu-id="82899-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="82899-105">Il contenuto della cartella può quindi essere spostato in più unità multimediali rimovibili per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="82899-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="82899-106">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-106">Note</span></span>**  
<span data-ttu-id="82899-107">Un singolo pacchetto non può contenere file di installazione per sistemi x86 e x64.</span><span class="sxs-lookup"><span data-stu-id="82899-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="82899-108">Come creare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="82899-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="82899-109">Per creare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="82899-109">To create a deployment package</span></span>**

1. <span data-ttu-id="82899-110">Verificare nel modulo **Immagini** che è stata creata almeno un'immagine imballata locale.</span><span class="sxs-lookup"><span data-stu-id="82899-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="82899-111">Nel menu **strumenti** selezionare **creazione guidata pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="82899-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="82899-112">Nella pagina di benvenuto della **creazione guidata pacchetti** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="82899-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="82899-113">Nella pagina **immagine area di lavoro** selezionare la casella di controllo **Includi immagine nel pacchetto** per includere un'immagine nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="82899-114">Il campo **immagine** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82899-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="82899-115">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-115">Note</span></span>**  
   <span data-ttu-id="82899-116">Un'immagine non è obbligatoria in un pacchetto MED-V. il pacchetto può essere creato senza un'immagine.</span><span class="sxs-lookup"><span data-stu-id="82899-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="82899-117">In questo caso, l'immagine deve essere caricata nel server in modo che possa essere successivamente scaricata tramite la rete nel client oppure inserita in una cartella di pre-stage.</span><span class="sxs-lookup"><span data-stu-id="82899-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="82899-118">Fare clic sull'elenco **Immagini** per visualizzare tutte le immagini disponibili.</span><span class="sxs-lookup"><span data-stu-id="82899-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="82899-119">Selezionare l'immagine da copiare nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="82899-120">Fare clic su **Aggiorna** per aggiornare l'elenco delle immagini disponibili.</span><span class="sxs-lookup"><span data-stu-id="82899-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="82899-121">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="82899-121">Click **Next**.</span></span>

7. <span data-ttu-id="82899-122">Nella pagina **impostazioni di installazione di Med-v** selezionare il file di installazione di Med-v eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82899-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="82899-123">Nel campo **file di installazione di MED-V** Digitare il percorso completo della directory in cui si trova il file di installazione.</span><span class="sxs-lookup"><span data-stu-id="82899-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="82899-124">Fare clic su **...** per passare alla directory in cui si trova il file di installazione.</span><span class="sxs-lookup"><span data-stu-id="82899-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="82899-125">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-125">Note</span></span>**  
   <span data-ttu-id="82899-126">Questo campo è obbligatorio e la procedura guidata non continuerà senza un nome di file valido.</span><span class="sxs-lookup"><span data-stu-id="82899-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="82899-127">Nel campo **Indirizzo server** Digitare il nome del server o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="82899-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="82899-128">Nel campo **porta server** Digitare la porta del server.</span><span class="sxs-lookup"><span data-stu-id="82899-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="82899-129">Selezionare la casella di controllo **server accessibile tramite HTTPS** per richiedere una connessione HTTPS per la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="82899-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="82899-130">Effettua una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="82899-130">Do one of the following:</span></span>

    -   <span data-ttu-id="82899-131">Fare clic su **impostazioni di installazione predefinite**, quindi fare clic su **Avanti** per continuare e uscire dalle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="82899-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="82899-132">Fare clic su **impostazioni di installazione personalizzate**, quindi fare clic su **Avanti** per personalizzare le impostazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="82899-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="82899-133">Nella pagina **impostazioni personalizzate per l'installazione di Med-v** Digitare nel campo **cartella di installazione** il percorso della cartella in cui verranno installati i file MED-v nel computer host.</span><span class="sxs-lookup"><span data-stu-id="82899-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="82899-134">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-134">Note</span></span>**  
            <span data-ttu-id="82899-135">È consigliabile usare le variabili nel percorso anziché nelle costanti, che possono variare da computer a computer.</span><span class="sxs-lookup"><span data-stu-id="82899-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="82899-136">Ad esempio, USA *%ProgramFiles%\\MED-V* invece di *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="82899-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="82899-137">Nella pagina **installazioni aggiuntive** selezionare la casella di controllo **Includi l'installazione del software di virtualizzazione** per includere l'installazione di Virtual PC nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="82899-138">Il campo **file di installazione** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82899-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="82899-139">Digitare il percorso completo del file di installazione del software di virtualizzazione oppure fare clic su **...** per passare alla directory.</span><span class="sxs-lookup"><span data-stu-id="82899-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="82899-140">Selezionare la casella di controllo **Includi installazione di Virtual PC QFE** per includere l'installazione di Virtual PC Update nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="82899-141">Il campo **file di installazione** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82899-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="82899-142">Digitare il percorso completo del file di installazione di Virtual PC Update oppure fare clic su **...** per passare alla directory.</span><span class="sxs-lookup"><span data-stu-id="82899-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="82899-143">Selezionare la casella di controllo **Includi l'installazione di Microsoft .NET framework 2,0** per includere l'installazione di Microsoft .net Framework 2,0 nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="82899-144">Il campo **file di installazione** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82899-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="82899-145">Digitare il percorso completo del file di installazione di Microsoft .NET Framework 2,0 oppure fare clic su **...** per passare alla directory.</span><span class="sxs-lookup"><span data-stu-id="82899-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="82899-146">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="82899-146">Click **Next**.</span></span>

16. <span data-ttu-id="82899-147">Nella pagina **finalizza** selezionare la posizione in cui deve essere salvato il pacchetto eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82899-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="82899-148">Nel campo **destinazione pacchetto** Digitare il percorso completo della directory in cui deve essere salvato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="82899-149">Fare clic su **...** per passare alla directory in cui devono essere salvati i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="82899-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="82899-150">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-150">Note</span></span>**  
    <span data-ttu-id="82899-151">La creazione del pacchetto può richiedere più spazio rispetto alle dimensioni effettive del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="82899-152">È quindi consigliabile creare il pacchetto sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="82899-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="82899-153">Dopo aver creato il pacchetto, è possibile copiarlo nel dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="82899-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="82899-154">Nel campo **nome pacchetto** immettere un nome per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="82899-155">Fare clic su **fine** per creare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82899-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="82899-156">Il pacchetto viene creato.</span><span class="sxs-lookup"><span data-stu-id="82899-156">The package is created.</span></span> <span data-ttu-id="82899-157">Potrebbero essere necessarie diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="82899-157">This might take several minutes.</span></span>

    <span data-ttu-id="82899-158">Dopo aver creato il pacchetto, viene visualizzato un messaggio che informa che è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="82899-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="82899-159">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-159">Note</span></span>**  
<span data-ttu-id="82899-160">Se sono stati salvati tutti i file localmente e non direttamente nel supporto rimovibile, assicurarsi di copiare solo il contenuto della cartella e non la cartella stessa nel supporto rimovibile.</span><span class="sxs-lookup"><span data-stu-id="82899-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="82899-161">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-161">Note</span></span>**  
<span data-ttu-id="82899-162">Il supporto rimovibile deve essere abbastanza grande in modo che il contenuto del pacchetto consumi un massimo di tre quarti della memoria del supporto rimovibile.</span><span class="sxs-lookup"><span data-stu-id="82899-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="82899-163">Nota</span><span class="sxs-lookup"><span data-stu-id="82899-163">Note</span></span>**  
<span data-ttu-id="82899-164">Quando si crea il pacchetto, le dimensioni effettive del pacchetto potrebbero essere necessarie fino al completamento della compilazione.</span><span class="sxs-lookup"><span data-stu-id="82899-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="82899-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82899-165">Related topics</span></span>


[<span data-ttu-id="82899-166">Creazione di un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="82899-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









