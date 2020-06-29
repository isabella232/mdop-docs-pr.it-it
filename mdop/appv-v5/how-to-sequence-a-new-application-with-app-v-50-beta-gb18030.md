---
title: Come sequenziare una nuova applicazione con App-V 5.0
description: Come sequenziare una nuova applicazione con App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805188"
---
# <span data-ttu-id="59879-103">Come sequenziare una nuova applicazione con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="59879-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="59879-104">Per eseguire una revisione o una procedura prima di iniziare la sequenziazione</span><span class="sxs-lookup"><span data-stu-id="59879-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="59879-105">Determinare il tipo di pacchetto di applicazione virtualizzato che si vuole creare:</span><span class="sxs-lookup"><span data-stu-id="59879-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="59879-106">Tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="59879-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="59879-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59879-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="59879-108">Standard</span><span class="sxs-lookup"><span data-stu-id="59879-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="59879-109">Crea un pacchetto che contiene un'applicazione o una famiglia di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="59879-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="59879-110">Questa è l'opzione preferita per la maggior parte dei tipi di applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="59879-111">Componente aggiuntivo o plug-in</span><span class="sxs-lookup"><span data-stu-id="59879-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="59879-112">Crea un pacchetto che estende la funzionalità di un'applicazione standard, ad esempio un plug-in per Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="59879-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="59879-113">È inoltre possibile usare i plug-in per le applicazioni installate nativamente o per un altro pacchetto collegato tramite i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="59879-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="59879-114">Middleware</span><span class="sxs-lookup"><span data-stu-id="59879-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="59879-115">Crea un pacchetto richiesto da un'applicazione standard, ad esempio Java.</span><span class="sxs-lookup"><span data-stu-id="59879-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="59879-116">I pacchetti middleware vengono usati per il collegamento ad altri pacchetti usando i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="59879-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="59879-117">Copiare tutti i file di installazione necessari nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="59879-118">Creare un'immagine di backup dell'ambiente virtuale prima di sequenziare un'applicazione e quindi ripristinare l'immagine ogni volta che si termina la sequenziazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="59879-119">Esaminare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="59879-119">Review the following items:</span></span>

    -   <span data-ttu-id="59879-120">Se un programma di installazione dell'applicazione cambia l'accesso alla sicurezza a un file o a una directory esistente o nuova, le modifiche non vengono acquisite nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="59879-121">Se i percorsi brevi sono stati disabilitati per il volume di destinazione del pacchetto virtualizzato, è necessario anche sequenziare il pacchetto su un volume creato ed è ancora disabilitato il Short-Path.</span><span class="sxs-lookup"><span data-stu-id="59879-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="59879-122">Non può essere il volume di sistema.</span><span class="sxs-lookup"><span data-stu-id="59879-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="59879-123">A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla.</span><span class="sxs-lookup"><span data-stu-id="59879-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="59879-124">Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="59879-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="59879-125">Per sequenziare una nuova applicazione standard</span><span class="sxs-lookup"><span data-stu-id="59879-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="59879-126">Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="59879-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="59879-127">Nel Sequencer fare clic su **Crea un nuovo pacchetto di applicazione virtuale**.</span><span class="sxs-lookup"><span data-stu-id="59879-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="59879-128">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="59879-129">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="59879-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="59879-130">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="59879-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="59879-131">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="59879-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="59879-132">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="59879-133">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-133">Important</span></span>**  
    <span data-ttu-id="59879-134">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="59879-135">Nella pagina **tipo di applicazione** fare clic sulla casella di controllo **applicazione standard (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="59879-136">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="59879-137">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-137">Note</span></span>**  
    <span data-ttu-id="59879-138">Se il programma di installazione dell'applicazione specificato modifica l'accesso alla sicurezza a un file o una directory, esistente o nuova, le modifiche associate non verranno acquisite nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="59879-139">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="59879-140">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="59879-141">Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="59879-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="59879-142">Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="59879-143">Per specificare questa posizione, selezionare **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="59879-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="59879-144">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-144">Note</span></span>**  
   <span data-ttu-id="59879-145">A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla.</span><span class="sxs-lookup"><span data-stu-id="59879-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="59879-146">Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="59879-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="59879-147">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="59879-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="59879-148">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-148">Important</span></span>**  
   <span data-ttu-id="59879-149">È consigliabile installare le applicazioni sempre in un percorso sicuro e assicurarsi che nessun altro utente abbia effettuato l'accesso al computer che esegue il sequencer durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="59879-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="59879-150">Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="59879-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="59879-151">Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="59879-152">Questo passaggio consente di completare tutte le attività necessarie per la licenza o la configurazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="59879-153">Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**.</span><span class="sxs-lookup"><span data-stu-id="59879-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="59879-154">Per eseguire programmi specifici, selezionare il programma o i programmi e quindi fare clic su **Esegui selezionato**.</span><span class="sxs-lookup"><span data-stu-id="59879-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="59879-155">Completare le attività di configurazione necessarie e quindi chiudere le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="59879-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="59879-156">Potrebbe essere necessario attendere diversi minuti per l'esecuzione di tutti i programmi.</span><span class="sxs-lookup"><span data-stu-id="59879-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="59879-157">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-157">Note</span></span>**  
   <span data-ttu-id="59879-158">Per eseguire le attività di primo utilizzo per qualsiasi applicazione che non è disponibile nell'elenco, aprire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="59879-159">Le informazioni associate verranno acquisite durante questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="59879-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="59879-160">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtualizzato appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="59879-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="59879-161">In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="59879-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="59879-162">Per continuare, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="59879-163">Viene visualizzata la pagina **Personalizza** .</span><span class="sxs-lookup"><span data-stu-id="59879-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="59879-164">Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 14 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="59879-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="59879-165">Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.</span><span class="sxs-lookup"><span data-stu-id="59879-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="59879-166">Preparare il pacchetto virtuale per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="59879-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="59879-167">Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="59879-168">Specifica i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="59879-169">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-169">Click **Next**.</span></span>

12. <span data-ttu-id="59879-170">Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="59879-171">Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="59879-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="59879-172">Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="59879-173">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-173">Note</span></span>**  
   <span data-ttu-id="59879-174">Se non si aprono applicazioni durante questo passaggio, il metodo di flusso predefinito è il recapito dello streaming su richiesta.</span><span class="sxs-lookup"><span data-stu-id="59879-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="59879-175">Questo significa che le applicazioni verranno scaricate bit per bit finché non sarà possibile aprirle e quindi, a seconda del modo in cui il caricamento in background è configurato, verrà caricato il resto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="59879-176">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="59879-177">Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare **Consenti questo pacchetto per l'esecuzione in qualsiasi sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="59879-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="59879-178">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare **Consenti questo pacchetto per l'esecuzione solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="59879-179">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-179">Click **Next**.</span></span>

   **<span data-ttu-id="59879-180">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-180">Important</span></span>**  
   <span data-ttu-id="59879-181">Verificare che i sistemi operativi specificati in questo articolo siano supportati dall'applicazione che si sta sequenziando.</span><span class="sxs-lookup"><span data-stu-id="59879-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="59879-182">Viene visualizzata la pagina **Crea pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="59879-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="59879-183">Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="59879-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="59879-184">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="59879-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="59879-185">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-185">Click **Next**.</span></span>

   <span data-ttu-id="59879-186">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto ora** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="59879-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="59879-187">Aggiungere **Commenti** facoltativi da associare al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="59879-188">I commenti sono utili per identificare la versione del programma e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="59879-189">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-189">Important</span></span>**  
   <span data-ttu-id="59879-190">Il sistema non supporta i caratteri non stampabili nei **Commenti** e nelle **descrizioni**.</span><span class="sxs-lookup"><span data-stu-id="59879-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="59879-191">Viene visualizzata la pagina **completamento** .</span><span class="sxs-lookup"><span data-stu-id="59879-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="59879-192">Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="59879-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="59879-193">Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory in cui è stato creato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="59879-194">Il pacchetto è ora disponibile nel sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="59879-195">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-195">Important</span></span>**  
   <span data-ttu-id="59879-196">Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="59879-197">Per sequenziare un'applicazione per il componente aggiuntivo o il plug-in</span><span class="sxs-lookup"><span data-stu-id="59879-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="59879-198">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-198">Note</span></span>**  
    <span data-ttu-id="59879-199">Prima di eseguire la procedura seguente, installare l'applicazione padre localmente nel computer in cui è in esecuzione Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="59879-200">Oppure, se l'applicazione padre è virtualizzata, è possibile eseguire la procedura descritta nel flusso di lavoro del componente aggiuntivo o del plug-in per decomprimere l'applicazione padre nel computer.</span><span class="sxs-lookup"><span data-stu-id="59879-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="59879-201">Ad esempio, se si esegue la sequenziazione di un plug-in per Microsoft Excel, installare Microsoft Excel localmente nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="59879-202">Installare inoltre l'applicazione padre nella stessa directory in cui è installata l'applicazione nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="59879-203">Se il plug-in o il componente aggiuntivo verrà usato con un pacchetto di applicazione virtuale esistente, installare l'applicazione nella stessa unità di applicazione virtuale usata quando è stato creato il pacchetto dell'applicazione virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="59879-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="59879-204">\*<strong><em>Nel Sequencer fare clic su \* </em> creare un nuovo pacchetto di applicazione virtuale </strong> .</span><span class="sxs-lookup"><span data-stu-id="59879-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="59879-205">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="59879-206">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o potrebbero causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="59879-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="59879-207">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="59879-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="59879-208">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="59879-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="59879-209">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="59879-210">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-210">Important</span></span>**  
   <span data-ttu-id="59879-211">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="59879-212">Nella pagina **tipo di applicazione** selezionare **componente aggiuntivo o plug-in**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="59879-213">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per il componente aggiuntivo o il plug-in.</span><span class="sxs-lookup"><span data-stu-id="59879-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="59879-214">Se il componente aggiuntivo o il plug-in non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="59879-215">Nella pagina **Install Primary** verificare che l'applicazione principale sia installata nel computer in cui è in esecuzione Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="59879-216">In alternativa, è possibile espandere un pacchetto esistente salvato localmente nel computer in cui viene eseguito il sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="59879-217">A tale scopo, fare clic su **Espandi pacchetto**e quindi selezionare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="59879-218">Dopo aver espanso o installato il programma padre, selezionare **ho installato il programma padre principale**.</span><span class="sxs-lookup"><span data-stu-id="59879-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="59879-219">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-219">Click **Next**.</span></span>

7. <span data-ttu-id="59879-220">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="59879-221">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="59879-222">Il nome del pacchetto verrà visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="59879-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="59879-223">Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="59879-224">Per specificare questa posizione, digitare il percorso oppure fare clic su **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="59879-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="59879-225">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-225">Note</span></span>**  
   <span data-ttu-id="59879-226">A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla.</span><span class="sxs-lookup"><span data-stu-id="59879-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="59879-227">Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="59879-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="59879-228">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione del plug-in o dell'applicazione del componente aggiuntivo in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="59879-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="59879-229">Usa il processo di installazione dell'applicazione per eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59879-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="59879-230">Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** e individuare ed eseguire i file di installazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="59879-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="59879-231">Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="59879-232">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="59879-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="59879-233">Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento.</span><span class="sxs-lookup"><span data-stu-id="59879-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="59879-234">Dopo aver esaminato le informazioni, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="59879-235">Viene visualizzata la pagina **Personalizza** .</span><span class="sxs-lookup"><span data-stu-id="59879-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="59879-236">Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 12 della procedura.</span><span class="sxs-lookup"><span data-stu-id="59879-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="59879-237">Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.</span><span class="sxs-lookup"><span data-stu-id="59879-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="59879-238">Ottimizzare la modalità di esecuzione del pacchetto in una rete lenta o inaffidabile.</span><span class="sxs-lookup"><span data-stu-id="59879-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="59879-239">Specifica i sistemi operativi che possono eseguire questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="59879-240">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-240">Click **Next**.</span></span>

11. <span data-ttu-id="59879-241">Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59879-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="59879-242">Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione in reti a latenza elevata.</span><span class="sxs-lookup"><span data-stu-id="59879-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="59879-243">Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti.</span><span class="sxs-lookup"><span data-stu-id="59879-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="59879-244">Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="59879-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="59879-245">È anche possibile configurare il pacchetto da richiedere per il download completo prima dell'apertura selezionando la casella di controllo **forza applicazioni da scaricare** .</span><span class="sxs-lookup"><span data-stu-id="59879-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="59879-246">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-246">Click **Next**.</span></span>

   **<span data-ttu-id="59879-247">Nota</span><span class="sxs-lookup"><span data-stu-id="59879-247">Note</span></span>**  
   <span data-ttu-id="59879-248">Se necessario, è possibile interrompere il caricamento di un'applicazione durante questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="59879-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="59879-249">Nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e selezionare una delle caselle di controllo: **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**.</span><span class="sxs-lookup"><span data-stu-id="59879-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="59879-250">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="59879-251">Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="59879-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="59879-252">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e quindi selezionare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="59879-253">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-253">Click **Next**.</span></span>

13. <span data-ttu-id="59879-254">Viene visualizzata la pagina **Crea pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="59879-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="59879-255">Per modificare il pacchetto senza salvarlo, selezionare **la casella di controllo continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** .</span><span class="sxs-lookup"><span data-stu-id="59879-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="59879-256">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="59879-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="59879-257">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-257">Click **Next**.</span></span>

   <span data-ttu-id="59879-258">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="59879-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="59879-259">Facoltativamente, aggiungere una **Descrizione** che verrà associata al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="59879-260">Le descrizioni sono utili per identificare la versione e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="59879-261">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-261">Important</span></span>**  
   <span data-ttu-id="59879-262">Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="59879-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="59879-263">Per sequenziare un'applicazione middleware</span><span class="sxs-lookup"><span data-stu-id="59879-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="59879-264">Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="59879-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="59879-265">\*<strong><em>Nel Sequencer fare clic su \* </em> creare un nuovo pacchetto di applicazione virtuale </strong> .</span><span class="sxs-lookup"><span data-stu-id="59879-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="59879-266">Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="59879-267">Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari.</span><span class="sxs-lookup"><span data-stu-id="59879-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="59879-268">Devi risolvere tutti i potenziali problemi prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="59879-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="59879-269">Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="59879-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="59879-270">Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="59879-271">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-271">Important</span></span>**  
   <span data-ttu-id="59879-272">Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer di App-V 5,0, in modo da assicurarti che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="59879-273">Nella pagina **tipo di applicazione** selezionare **middleware**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="59879-274">Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="59879-275">Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="59879-276">Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="59879-277">Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="59879-278">Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="59879-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="59879-279">Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59879-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="59879-280">Per specificare questa posizione, digitare il percorso o fare clic su **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="59879-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="59879-281">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-281">Click **Next**.</span></span>

7. <span data-ttu-id="59879-282">Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione middleware sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="59879-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="59879-283">Usa il processo di installazione dell'applicazione per eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59879-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="59879-284">Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**per individuare ed eseguire i file di installazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="59879-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="59879-285">Dopo aver completato l'installazione, selezionare la casella di controllo **ho terminato l'installazione** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="59879-286">Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="59879-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="59879-287">Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato.</span><span class="sxs-lookup"><span data-stu-id="59879-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="59879-288">In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="59879-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="59879-289">Per continuare, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="59879-290">Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="59879-291">Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="59879-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="59879-292">Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="59879-293">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-293">Click **Next**.</span></span>

11. <span data-ttu-id="59879-294">Nella pagina **Crea pacchetto** viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="59879-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="59879-295">Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="59879-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="59879-296">Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato.</span><span class="sxs-lookup"><span data-stu-id="59879-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="59879-297">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="59879-297">Click **Next**.</span></span>

    <span data-ttu-id="59879-298">Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="59879-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="59879-299">Facoltativamente, aggiungere una **Descrizione** da associare al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="59879-300">Le descrizioni sono utili per identificare la versione del programma e altre informazioni sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="59879-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="59879-301">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-301">Important</span></span>**  
    <span data-ttu-id="59879-302">Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.</span><span class="sxs-lookup"><span data-stu-id="59879-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="59879-303">Viene visualizzata la pagina **completamento** .</span><span class="sxs-lookup"><span data-stu-id="59879-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="59879-304">Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="59879-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="59879-305">Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory specificata nel passaggio 11 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="59879-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="59879-306">Il pacchetto è ora disponibile nel sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="59879-307">Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**.</span><span class="sxs-lookup"><span data-stu-id="59879-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="59879-308">Importante</span><span class="sxs-lookup"><span data-stu-id="59879-308">Important</span></span>**  
   <span data-ttu-id="59879-309">Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59879-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="59879-310">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59879-310">Related topics</span></span>


[<span data-ttu-id="59879-311">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="59879-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









