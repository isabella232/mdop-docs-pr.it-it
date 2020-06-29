---
title: Come sequenziare una nuova applicazione con App-V 5.1
description: Come sequenziare una nuova applicazione con App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805187"
---
# <span data-ttu-id="40325-103">Come sequenziare una nuova applicazione con App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="40325-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="40325-104">Per eseguire una revisione o una procedura prima di iniziare la sequenziazione</span><span class="sxs-lookup"><span data-stu-id="40325-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="40325-105">Determinare il tipo di pacchetto di applicazione virtualizzato che si vuole creare:</span><span class="sxs-lookup"><span data-stu-id="40325-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="40325-106">Tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="40325-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="40325-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40325-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="40325-108">Standard</span><span class="sxs-lookup"><span data-stu-id="40325-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="40325-109">Crea un pacchetto che contiene un'applicazione o una famiglia di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="40325-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="40325-110">Questa è l'opzione preferita per la maggior parte dei tipi di applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="40325-111">Componente aggiuntivo o plug-in</span><span class="sxs-lookup"><span data-stu-id="40325-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="40325-112">Crea un pacchetto che estende la funzionalità di un'applicazione standard, ad esempio un plug-in per Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="40325-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="40325-113">È inoltre possibile usare i plug-in per le applicazioni installate nativamente o per un altro pacchetto collegato tramite i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="40325-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="40325-114">Middleware</span><span class="sxs-lookup"><span data-stu-id="40325-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="40325-115">Crea un pacchetto richiesto da un'applicazione standard, ad esempio Java.</span><span class="sxs-lookup"><span data-stu-id="40325-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="40325-116">I pacchetti middleware vengono usati per il collegamento ad altri pacchetti usando i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="40325-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="40325-117">Copiare tutti i file di installazione necessari nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="40325-118">Creare un'immagine di backup dell'ambiente virtuale prima di sequenziare un'applicazione e quindi ripristinare l'immagine ogni volta che si termina la sequenziazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="40325-119">Esaminare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="40325-119">Review the following items:</span></span>

    -   <span data-ttu-id="40325-120">Se un programma di installazione dell'applicazione cambia l'accesso alla sicurezza a un file o a una directory esistente o nuova, le modifiche non vengono acquisite nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="40325-121">Se i percorsi brevi sono stati disabilitati per il volume di destinazione del pacchetto virtualizzato, è necessario anche sequenziare il pacchetto su un volume creato ed è ancora disabilitato il Short-Path.</span><span class="sxs-lookup"><span data-stu-id="40325-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="40325-122">Non può essere il volume di sistema.</span><span class="sxs-lookup"><span data-stu-id="40325-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="40325-123">Il sequencer App-V 5. x non può sequenziare le applicazioni con nomi di file corrispondenti "CO_ &lt; x &gt; " dove x è un numero qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="40325-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="40325-124">Verrà generato l'errore 0x8007139F.</span><span class="sxs-lookup"><span data-stu-id="40325-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="40325-125">Per sequenziare una nuova applicazione standard</span><span class="sxs-lookup"><span data-stu-id="40325-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="40325-126">Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="40325-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="40325-127">Nel Sequencer fare clic su **Crea un nuovo pacchetto di applicazione virtuale**.</span><span class="sxs-lookup"><span data-stu-id="40325-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="40325-128">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="40325-129">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="40325-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="40325-130">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="40325-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="40325-131">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="40325-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="40325-132">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="40325-133">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="40325-134">Nella pagina **tipo di applicazione** fare clic sulla casella di controllo **applicazione standard (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="40325-135">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="40325-136">Se il programma di installazione dell'applicazione specificato modifica l'accesso alla sicurezza a un file o una directory, esistente o nuova, le modifiche associate non verranno acquisite nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="40325-137">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="40325-138">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="40325-139">Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="40325-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="40325-140">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-140">Click **Next**.</span></span>

7. <span data-ttu-id="40325-141">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="40325-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-142">È consigliabile installare le applicazioni sempre in un percorso sicuro e assicurarsi che nessun altro utente abbia effettuato l'accesso al computer che esegue il sequencer durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="40325-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="40325-143">Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="40325-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="40325-144">Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="40325-145">Questo passaggio consente di completare tutte le attività necessarie per la licenza o la configurazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40325-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="40325-146">Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**.</span><span class="sxs-lookup"><span data-stu-id="40325-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="40325-147">Per eseguire programmi specifici, selezionare il programma o i programmi e quindi fare clic su **Esegui selezionato**.</span><span class="sxs-lookup"><span data-stu-id="40325-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="40325-148">Completare le attività di configurazione necessarie e quindi chiudere le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="40325-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="40325-149">Potrebbe essere necessario attendere diversi minuti per l'esecuzione di tutti i programmi.</span><span class="sxs-lookup"><span data-stu-id="40325-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="40325-150">Per eseguire le attività di primo utilizzo per qualsiasi applicazione che non è disponibile nell'elenco, aprire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="40325-151">Le informazioni associate verranno acquisite durante questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="40325-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="40325-152">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtualizzato appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="40325-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="40325-153">In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="40325-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="40325-154">Per continuare, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="40325-155">Viene visualizzata la pagina **Personalizza** .</span><span class="sxs-lookup"><span data-stu-id="40325-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="40325-156">Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 14 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="40325-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="40325-157">Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.</span><span class="sxs-lookup"><span data-stu-id="40325-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="40325-158">Preparare il pacchetto virtuale per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="40325-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="40325-159">Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40325-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="40325-160">Specifica i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="40325-161">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-161">Click **Next**.</span></span>

12. <span data-ttu-id="40325-162">Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40325-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="40325-163">Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="40325-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="40325-164">Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="40325-165">Se non si aprono applicazioni durante questo passaggio, il metodo di flusso predefinito è il recapito dello streaming su richiesta.</span><span class="sxs-lookup"><span data-stu-id="40325-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="40325-166">Questo significa che le applicazioni verranno scaricate bit per bit finché non sarà possibile aprirle e quindi, a seconda del modo in cui il caricamento in background è configurato, verrà caricato il resto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="40325-167">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="40325-168">Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare **Consenti questo pacchetto per l'esecuzione in qualsiasi sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="40325-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="40325-169">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare **Consenti questo pacchetto per l'esecuzione solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="40325-170">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-171">Verificare che i sistemi operativi specificati in questo articolo siano supportati dall'applicazione che si sta sequenziando.</span><span class="sxs-lookup"><span data-stu-id="40325-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="40325-172">Viene visualizzata la pagina **Crea pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="40325-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="40325-173">Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="40325-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="40325-174">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="40325-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="40325-175">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-175">Click **Next**.</span></span>

   <span data-ttu-id="40325-176">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto ora** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="40325-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="40325-177">Aggiungere **Commenti** facoltativi da associare al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="40325-178">I commenti sono utili per identificare la versione del programma e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-179">Il sistema non supporta i caratteri non stampabili nei **Commenti** e nelle **descrizioni**.</span><span class="sxs-lookup"><span data-stu-id="40325-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="40325-180">Viene visualizzata la pagina **completamento** .</span><span class="sxs-lookup"><span data-stu-id="40325-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="40325-181">Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="40325-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="40325-182">Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory in cui è stato creato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="40325-183">Il pacchetto è ora disponibile nel sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-184">Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="40325-185">Per sequenziare un'applicazione per il componente aggiuntivo o il plug-in</span><span class="sxs-lookup"><span data-stu-id="40325-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="40325-186">Prima di eseguire la procedura seguente, installare l'applicazione padre localmente nel computer in cui è in esecuzione Sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="40325-187">Oppure, se l'applicazione padre è virtualizzata, è possibile eseguire la procedura descritta nel flusso di lavoro del componente aggiuntivo o del plug-in per decomprimere l'applicazione padre nel computer.</span><span class="sxs-lookup"><span data-stu-id="40325-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="40325-188">Ad esempio, se si esegue la sequenziazione di un plug-in per Microsoft Excel, installare Microsoft Excel localmente nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="40325-189">Installare inoltre l'applicazione padre nella stessa directory in cui è installata l'applicazione nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40325-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="40325-190">Se il plug-in o il componente aggiuntivo verrà usato con un pacchetto di applicazione virtuale esistente, installare l'applicazione nella stessa unità di applicazione virtuale usata quando è stato creato il pacchetto dell'applicazione virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="40325-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="40325-191">\*<strong><em>Nel Sequencer fare clic su \* </em> creare un nuovo pacchetto di applicazione virtuale </strong> .</span><span class="sxs-lookup"><span data-stu-id="40325-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="40325-192">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="40325-193">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o potrebbero causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="40325-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="40325-194">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="40325-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="40325-195">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="40325-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="40325-196">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-197">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="40325-198">Nella pagina **tipo di applicazione** selezionare **componente aggiuntivo o plug-in**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="40325-199">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per il componente aggiuntivo o il plug-in.</span><span class="sxs-lookup"><span data-stu-id="40325-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="40325-200">Se il componente aggiuntivo o il plug-in non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="40325-201">Nella pagina **Install Primary** verificare che l'applicazione principale sia installata nel computer in cui è in esecuzione Sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="40325-202">In alternativa, è possibile espandere un pacchetto esistente salvato localmente nel computer in cui viene eseguito il sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="40325-203">A tale scopo, fare clic su **Espandi pacchetto**e quindi selezionare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="40325-204">Dopo aver espanso o installato il programma padre, selezionare **ho installato il programma padre principale**.</span><span class="sxs-lookup"><span data-stu-id="40325-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="40325-205">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-205">Click **Next**.</span></span>

7. <span data-ttu-id="40325-206">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="40325-207">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="40325-208">Il nome del pacchetto verrà visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="40325-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="40325-209">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-209">Click **Next**.</span></span>

8. <span data-ttu-id="40325-210">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione del plug-in o dell'applicazione del componente aggiuntivo in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="40325-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="40325-211">Usa il processo di installazione dell'applicazione per eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="40325-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="40325-212">Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** e individuare ed eseguire i file di installazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="40325-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="40325-213">Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="40325-214">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="40325-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="40325-215">Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento.</span><span class="sxs-lookup"><span data-stu-id="40325-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="40325-216">Dopo aver esaminato le informazioni, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="40325-217">Viene visualizzata la pagina **Personalizza** .</span><span class="sxs-lookup"><span data-stu-id="40325-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="40325-218">Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 12 della procedura.</span><span class="sxs-lookup"><span data-stu-id="40325-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="40325-219">Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.</span><span class="sxs-lookup"><span data-stu-id="40325-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="40325-220">Ottimizzare la modalità di esecuzione del pacchetto in una rete lenta o inaffidabile.</span><span class="sxs-lookup"><span data-stu-id="40325-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="40325-221">Specifica i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="40325-222">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-222">Click **Next**.</span></span>

11. <span data-ttu-id="40325-223">Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40325-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="40325-224">Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione in reti a latenza elevata.</span><span class="sxs-lookup"><span data-stu-id="40325-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="40325-225">Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="40325-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="40325-226">Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="40325-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="40325-227">È anche possibile configurare il pacchetto da richiedere per il download completo prima dell'apertura selezionando la casella di controllo **forza applicazioni da scaricare** .</span><span class="sxs-lookup"><span data-stu-id="40325-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="40325-228">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="40325-229">Se necessario, è possibile interrompere il caricamento di un'applicazione durante questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="40325-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="40325-230">Nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e selezionare una delle caselle di controllo: **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**.</span><span class="sxs-lookup"><span data-stu-id="40325-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="40325-231">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="40325-232">Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="40325-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="40325-233">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e quindi selezionare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="40325-234">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-234">Click **Next**.</span></span>

13. <span data-ttu-id="40325-235">Viene visualizzata la pagina **Crea pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="40325-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="40325-236">Per modificare il pacchetto senza salvarlo, selezionare **la casella di controllo continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** .</span><span class="sxs-lookup"><span data-stu-id="40325-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="40325-237">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="40325-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="40325-238">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-238">Click **Next**.</span></span>

    <span data-ttu-id="40325-239">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="40325-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="40325-240">Facoltativamente, aggiungere una **Descrizione** che verrà associata al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="40325-241">Le descrizioni sono utili per identificare la versione e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="40325-242">Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="40325-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="40325-243">Per sequenziare un'applicazione middleware</span><span class="sxs-lookup"><span data-stu-id="40325-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="40325-244">Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="40325-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="40325-245">\*<strong><em>Nel Sequencer fare clic su \* </em> creare un nuovo pacchetto di applicazione virtuale </strong> .</span><span class="sxs-lookup"><span data-stu-id="40325-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="40325-246">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="40325-247">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="40325-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="40325-248">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="40325-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="40325-249">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="40325-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="40325-250">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-251">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer di App-V 5,0, in modo da assicurarti che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="40325-252">Nella pagina **tipo di applicazione** selezionare **middleware**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="40325-253">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40325-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="40325-254">Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="40325-255">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="40325-256">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="40325-257">Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="40325-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="40325-258">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-258">Click **Next**.</span></span>

7. <span data-ttu-id="40325-259">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione middleware sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="40325-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="40325-260">Usa il processo di installazione dell'applicazione per eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="40325-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="40325-261">Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**per individuare ed eseguire i file di installazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="40325-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="40325-262">Dopo aver completato l'installazione, selezionare la casella di controllo **ho terminato l'installazione** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="40325-263">Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="40325-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="40325-264">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="40325-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="40325-265">In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="40325-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="40325-266">Per continuare, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="40325-267">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="40325-268">Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="40325-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="40325-269">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="40325-270">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-270">Click **Next**.</span></span>

11. <span data-ttu-id="40325-271">Nella pagina **Crea pacchetto** viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="40325-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="40325-272">Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="40325-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="40325-273">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="40325-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="40325-274">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="40325-274">Click **Next**.</span></span>

    <span data-ttu-id="40325-275">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="40325-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="40325-276">Facoltativamente, aggiungere una **Descrizione** da associare al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="40325-277">Le descrizioni sono utili per identificare la versione del programma e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="40325-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="40325-278">Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="40325-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="40325-279">Viene visualizzata la pagina **completamento** .</span><span class="sxs-lookup"><span data-stu-id="40325-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="40325-280">Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="40325-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="40325-281">Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory specificata nel passaggio 11 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="40325-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="40325-282">Il pacchetto è ora disponibile nel sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="40325-283">Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**.</span><span class="sxs-lookup"><span data-stu-id="40325-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="40325-284">Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.</span><span class="sxs-lookup"><span data-stu-id="40325-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="40325-285">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40325-285">Related topics</span></span>


[<span data-ttu-id="40325-286">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="40325-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









