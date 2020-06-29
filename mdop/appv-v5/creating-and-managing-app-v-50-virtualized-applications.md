---
title: Creazione e gestione di applicazioni virtualizzate di App-V 5.0
description: Creazione e gestione di applicazioni virtualizzate di App-V 5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805925"
---
# <span data-ttu-id="edac4-103">Creazione e gestione di applicazioni virtualizzate di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="edac4-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="edac4-104">Dopo aver distribuito correttamente il sequencer di Microsoft Application Virtualization (App-V) 5,0, è possibile usarlo per monitorare e registrare il processo di installazione e configurazione per un'applicazione da eseguire come applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="edac4-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="edac4-105">**Nota**  Per altre informazioni sulla configurazione del sequencer di Microsoft Application Virtualization (App-V) 5,0, la sequenziazione delle procedure consigliate e un esempio di creazione e aggiornamento di un'applicazione virtuale, vedere la [Guida alla sequenziazione di Microsoft Application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 sequenziazione Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="edac4-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="edac4-106">Sequenziazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="edac4-106">Sequencing an application</span></span>


<span data-ttu-id="edac4-107">Puoi usare il sequencer App-V 5,0 per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="edac4-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="edac4-108">Creare pacchetti virtuali che possono essere distribuiti nei computer che eseguono il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="edac4-109">Aggiornare i pacchetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="edac4-109">Upgrade existing packages.</span></span> <span data-ttu-id="edac4-110">Puoi espandere un pacchetto esistente nel computer che esegue il sequencer e quindi aggiornare l'applicazione per creare una versione più recente.</span><span class="sxs-lookup"><span data-stu-id="edac4-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="edac4-111">Modificare le informazioni di configurazione associate a un pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="edac4-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="edac4-112">Ad esempio, è possibile aggiungere un collegamento o modificare un'associazione di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="edac4-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="edac4-113">**Nota**  È necessario creare tasti di scelta rapida e salvarli in un percorso di rete disponibile per consentire il roaming.</span><span class="sxs-lookup"><span data-stu-id="edac4-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="edac4-114">Se un collegamento viene creato e salvato in una posizione privata, il pacchetto deve essere pubblicato localmente nel computer che esegue il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="edac4-115">Convertire i pacchetti virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="edac4-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="edac4-116">Il sequencer usa la directory **% tmp% \ \ Scratch** o **% Temp% \ \ Scratch** e la directory **Temp** per archiviare i file temporanei durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="edac4-117">Nel computer che esegue il sequencer devi configurare queste directory con spazio su disco gratuito equivalente ai requisiti stimati per l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="edac4-118">La configurazione delle directory Temp e della directory Temp in partizioni disco rigido diverse può contribuire a migliorare le prestazioni durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="edac4-119">Quando si usa sequencer per creare una nuova applicazione virtuale, vengono creati i file elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="edac4-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="edac4-120">Questi file includono il pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="edac4-121">file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="edac4-121">.msi file.</span></span> <span data-ttu-id="edac4-122">Questo file di Windows Installer (con estensione msi) viene creato dal sequencer e viene usato per installare il pacchetto virtuale nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="edac4-123">Report.xml file.</span><span class="sxs-lookup"><span data-stu-id="edac4-123">Report.xml file.</span></span> <span data-ttu-id="edac4-124">In questo file, sequencer Salva tutti i problemi, gli avvisi e gli errori individuati durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="edac4-125">Visualizza le informazioni dopo la creazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="edac4-126">Questo report può essere segnalato per la diagnosi e la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="edac4-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="edac4-127">file con estensione AppV.</span><span class="sxs-lookup"><span data-stu-id="edac4-127">.appv file.</span></span> <span data-ttu-id="edac4-128">Questo è il file dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="edac4-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="edac4-129">File di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="edac4-129">Deployment configuration file.</span></span> <span data-ttu-id="edac4-130">Il file di configurazione della distribuzione determina il modo in cui verrà distribuita l'applicazione virtuale per i computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="edac4-131">File di configurazione utente.</span><span class="sxs-lookup"><span data-stu-id="edac4-131">User configuration file.</span></span> <span data-ttu-id="edac4-132">Il file di configurazione dell'utente determina il modo in cui verrà eseguita l'applicazione virtuale nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="edac4-133">**Importante**  È necessario configurare le cartelle% TMP% e% TEMP% che il convertitore di pacchetti usa per essere un percorso e una directory sicuri.</span><span class="sxs-lookup"><span data-stu-id="edac4-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="edac4-134">Un percorso sicuro è accessibile solo da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="edac4-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="edac4-135">Inoltre, quando si sequenzia il pacchetto, è necessario salvare il pacchetto in una posizione sicura oppure assicurarsi che nessun altro utente sia autorizzato a eseguire l'accesso durante il processo di conversione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="edac4-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="edac4-136">La finestra di dialogo **Opzioni** nella console sequencer contiene le schede seguenti:</span><span class="sxs-lookup"><span data-stu-id="edac4-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="edac4-137">**Generale**.</span><span class="sxs-lookup"><span data-stu-id="edac4-137">**General**.</span></span> <span data-ttu-id="edac4-138">Usare questa scheda per consentire l'esecuzione di aggiornamenti Microsoft durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="edac4-139">Selezionare **Accoda versione pacchetto a nomefile** per configurare la sequenza per aggiungere un numero di versione al pacchetto virtualizzato che viene sequenziato.</span><span class="sxs-lookup"><span data-stu-id="edac4-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="edac4-140">Selezionare **Considera sempre attendibile l'origine degli acceleratori di pacchetto** per creare pacchetti virtualizzati usando un Acceleratore pacchetto senza richiedere l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="edac4-141">**Importante**  Gli acceleratori di pacchetti creati con App-V 4.6 non sono supportati da App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="edac4-142">**Analizzare gli elementi**.</span><span class="sxs-lookup"><span data-stu-id="edac4-142">**Parse Items**.</span></span> <span data-ttu-id="edac4-143">Questa scheda Visualizza i percorsi di percorso file associati che verranno analizzati o suddivisi in token nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="edac4-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="edac4-144">I token sono utili per l'aggiunta di file tramite la scheda **file di pacchetto** in **modifica avanzata**.</span><span class="sxs-lookup"><span data-stu-id="edac4-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="edac4-145">**Elementi di esclusione**.</span><span class="sxs-lookup"><span data-stu-id="edac4-145">**Exclusion Items**.</span></span> <span data-ttu-id="edac4-146">Usare questa scheda per specificare quali cartelle e directory non devono essere monitorate durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="edac4-147">Per aggiungere i dati dell'applicazione locale salvati nella cartella dati locali dell'app nel pacchetto, fare clic su **nuovo** e specificare la posizione e il **tipo di mapping**associato.</span><span class="sxs-lookup"><span data-stu-id="edac4-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="edac4-148">Questa opzione è obbligatoria per alcuni pacchetti.</span><span class="sxs-lookup"><span data-stu-id="edac4-148">This option is required for some packages.</span></span>

<span data-ttu-id="edac4-149">App-V 5,0 supporta le applicazioni che includono i servizi Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="edac4-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="edac4-150">Se un'applicazione include un servizio Windows, il servizio verrà incluso nel pacchetto virtuale sequenziato finché viene installato durante il monitoraggio da parte del sequencer.</span><span class="sxs-lookup"><span data-stu-id="edac4-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="edac4-151">Se un'applicazione virtuale crea un servizio Windows quando viene eseguito inizialmente, in seguito, dopo l'installazione, l'applicazione deve essere eseguita durante il monitoraggio del sequencer in modo che il servizio Windows venga aggiunto al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="edac4-152">Sono supportati solo i servizi eseguiti con l'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="edac4-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="edac4-153">I servizi configurati per l'autostart o l'avvio in ritardo vengono avviati prima che la prima applicazione virtuale in un pacchetto venga eseguita all'interno dell'ambiente virtuale del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="edac4-154">I servizi Windows configurati per l'avvio su richiesta da un'applicazione vengono avviati quando l'applicazione virtuale all'interno del pacchetto avvia il servizio tramite chiamata API.</span><span class="sxs-lookup"><span data-stu-id="edac4-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="edac4-155">Come sequenziare una nuova applicazione con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="edac4-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="edac4-156">Supporto delle estensioni della shell App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="edac4-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="edac4-157">App-V 5.0 SP2 supporta le estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="edac4-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="edac4-158">Le estensioni della shell verranno rilevate e incorporate nel pacchetto durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="edac4-159">Le estensioni della shell vengono inserite automaticamente nel pacchetto durante il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="edac4-160">Quando il pacchetto viene pubblicato, l'estensione della Shell offre agli utenti le stesse funzionalità di se l'applicazione è stata installata localmente.</span><span class="sxs-lookup"><span data-stu-id="edac4-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="edac4-161">Requisiti per l'uso delle estensioni della shell:</span><span class="sxs-lookup"><span data-stu-id="edac4-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="edac4-162">I pacchetti che contengono estensioni della shell incorporata devono essere pubblicati globalmente.</span><span class="sxs-lookup"><span data-stu-id="edac4-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="edac4-163">L'applicazione non richiede alcuna installazione o configurazione aggiuntiva nel client per abilitare la funzionalità di estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="edac4-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="edac4-164">Il "bit" dell'applicazione, il sequencer e il client App-V devono corrispondere o le estensioni della shell non funzionano.</span><span class="sxs-lookup"><span data-stu-id="edac4-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="edac4-165">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="edac4-165">For example:</span></span>

    -   <span data-ttu-id="edac4-166">La versione dell'applicazione è 64 bit.</span><span class="sxs-lookup"><span data-stu-id="edac4-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="edac4-167">Il sequencer viene eseguito in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="edac4-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="edac4-168">Il pacchetto viene recapitato a un computer client App-V a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="edac4-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="edac4-169">La tabella seguente elenca le estensioni della shell supportate:</span><span class="sxs-lookup"><span data-stu-id="edac4-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edac4-170">Gestore</span><span class="sxs-lookup"><span data-stu-id="edac4-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="edac4-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edac4-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edac4-172">Gestore del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="edac4-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-173">Aggiunge voci di menu al menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="edac4-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="edac4-174">Viene chiamata prima che venga visualizzato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="edac4-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edac4-175">Gestore di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="edac4-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-176">Controlla l'azione in cui fare clic con il pulsante destro del mouse, trascinare e rilasciare e modificare il menu di scelta rapida visualizzato.</span><span class="sxs-lookup"><span data-stu-id="edac4-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edac4-177">Trascinare il gestore di destinazione</span><span class="sxs-lookup"><span data-stu-id="edac4-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-178">Controlla l'azione dopo il trascinamento di un oggetto dati e l'eliminazione di una destinazione di rilascio, ad esempio un file.</span><span class="sxs-lookup"><span data-stu-id="edac4-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edac4-179">Gestore oggetti dati</span><span class="sxs-lookup"><span data-stu-id="edac4-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-180">Controlla l'azione dopo la copia di un file negli Appunti o trascinato e rilasciata su una destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="edac4-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="edac4-181">Può includere altri formati di Appunti nella destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="edac4-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edac4-182">Gestore della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="edac4-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-183">Sostituisce o aggiunge pagine alla finestra di dialogo delle proprietà di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edac4-184">Gestore infotip</span><span class="sxs-lookup"><span data-stu-id="edac4-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-185">Consente di recuperare le informazioni di flag e infotip per un elemento e di visualizzarle all'interno di una descrizione comando popup al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="edac4-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edac4-186">Gestore di colonne</span><span class="sxs-lookup"><span data-stu-id="edac4-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-187">Consente la creazione e la visualizzazione di colonne personalizzate nella <strong> visualizzazione dettagli di Esplora risorse </strong> .</span><span class="sxs-lookup"><span data-stu-id="edac4-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="edac4-188">Può essere usato per estendere l'ordinamento e il raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="edac4-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edac4-189">Gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="edac4-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="edac4-190">Consente di visualizzare un'anteprima di un file nel riquadro di anteprima di Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="edac4-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="edac4-191">Supporto dell'estensione di file copy on Write (mucca)</span><span class="sxs-lookup"><span data-stu-id="edac4-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="edac4-192">Copia in scrittura (mucca) le estensioni di file consentono a App-V 5,0 di scrivere in modo dinamico in posizioni specifiche contenute nel pacchetto virtuale durante l'uso.</span><span class="sxs-lookup"><span data-stu-id="edac4-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="edac4-193">Nella tabella seguente sono visualizzati i tipi di file che possono esistere in un pacchetto virtuale nella directory VFS, ma non possono essere aggiornati nel computer che gestisce il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="edac4-194">Tutti gli altri file e directory possono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="edac4-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="edac4-195">. acm</span><span class="sxs-lookup"><span data-stu-id="edac4-195">.acm</span></span>

<span data-ttu-id="edac4-196">. asa</span><span class="sxs-lookup"><span data-stu-id="edac4-196">.asa</span></span>

<span data-ttu-id="edac4-197">.asp</span><span class="sxs-lookup"><span data-stu-id="edac4-197">.asp</span></span>

<span data-ttu-id="edac4-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="edac4-198">.aspx</span></span>

<span data-ttu-id="edac4-199">. ax</span><span class="sxs-lookup"><span data-stu-id="edac4-199">.ax</span></span>

<span data-ttu-id="edac4-200">.bat</span><span class="sxs-lookup"><span data-stu-id="edac4-200">.bat</span></span>

<span data-ttu-id="edac4-201">.cer</span><span class="sxs-lookup"><span data-stu-id="edac4-201">.cer</span></span>

<span data-ttu-id="edac4-202">.chm</span><span class="sxs-lookup"><span data-stu-id="edac4-202">.chm</span></span>

<span data-ttu-id="edac4-203">. clb</span><span class="sxs-lookup"><span data-stu-id="edac4-203">.clb</span></span>

<span data-ttu-id="edac4-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="edac4-204">.cmd</span></span>

<span data-ttu-id="edac4-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="edac4-205">.cnt</span></span>

<span data-ttu-id="edac4-206">. cnv</span><span class="sxs-lookup"><span data-stu-id="edac4-206">.cnv</span></span>

<span data-ttu-id="edac4-207">.com</span><span class="sxs-lookup"><span data-stu-id="edac4-207">.com</span></span>

<span data-ttu-id="edac4-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="edac4-208">.cpl</span></span>

<span data-ttu-id="edac4-209">. CPX</span><span class="sxs-lookup"><span data-stu-id="edac4-209">.cpx</span></span>

<span data-ttu-id="edac4-210">.crt</span><span class="sxs-lookup"><span data-stu-id="edac4-210">.crt</span></span>

<span data-ttu-id="edac4-211">.dll</span><span class="sxs-lookup"><span data-stu-id="edac4-211">.dll</span></span>

<span data-ttu-id="edac4-212">.drv</span><span class="sxs-lookup"><span data-stu-id="edac4-212">.drv</span></span>

<span data-ttu-id="edac4-213">.exe</span><span class="sxs-lookup"><span data-stu-id="edac4-213">.exe</span></span>

<span data-ttu-id="edac4-214">.fon</span><span class="sxs-lookup"><span data-stu-id="edac4-214">.fon</span></span>

<span data-ttu-id="edac4-215">.grp</span><span class="sxs-lookup"><span data-stu-id="edac4-215">.grp</span></span>

<span data-ttu-id="edac4-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="edac4-216">.hlp</span></span>

<span data-ttu-id="edac4-217">.hta</span><span class="sxs-lookup"><span data-stu-id="edac4-217">.hta</span></span>

<span data-ttu-id="edac4-218">. IME</span><span class="sxs-lookup"><span data-stu-id="edac4-218">.ime</span></span>

<span data-ttu-id="edac4-219">.inf</span><span class="sxs-lookup"><span data-stu-id="edac4-219">.inf</span></span>

<span data-ttu-id="edac4-220">.ins</span><span class="sxs-lookup"><span data-stu-id="edac4-220">.ins</span></span>

<span data-ttu-id="edac4-221">.isp</span><span class="sxs-lookup"><span data-stu-id="edac4-221">.isp</span></span>

<span data-ttu-id="edac4-222">. its</span><span class="sxs-lookup"><span data-stu-id="edac4-222">.its</span></span>

<span data-ttu-id="edac4-223">.js</span><span class="sxs-lookup"><span data-stu-id="edac4-223">.js</span></span>

<span data-ttu-id="edac4-224">.jse</span><span class="sxs-lookup"><span data-stu-id="edac4-224">.jse</span></span>

<span data-ttu-id="edac4-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="edac4-225">.lnk</span></span>

<span data-ttu-id="edac4-226">.msc</span><span class="sxs-lookup"><span data-stu-id="edac4-226">.msc</span></span>

<span data-ttu-id="edac4-227">.msi</span><span class="sxs-lookup"><span data-stu-id="edac4-227">.msi</span></span>

<span data-ttu-id="edac4-228">.msp</span><span class="sxs-lookup"><span data-stu-id="edac4-228">.msp</span></span>

<span data-ttu-id="edac4-229">.mst</span><span class="sxs-lookup"><span data-stu-id="edac4-229">.mst</span></span>

<span data-ttu-id="edac4-230">. mui</span><span class="sxs-lookup"><span data-stu-id="edac4-230">.mui</span></span>

<span data-ttu-id="edac4-231">. nls</span><span class="sxs-lookup"><span data-stu-id="edac4-231">.nls</span></span>

<span data-ttu-id="edac4-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="edac4-232">.ocx</span></span>

<span data-ttu-id="edac4-233">. PAL</span><span class="sxs-lookup"><span data-stu-id="edac4-233">.pal</span></span>

<span data-ttu-id="edac4-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="edac4-234">.pcd</span></span>

<span data-ttu-id="edac4-235">.pif</span><span class="sxs-lookup"><span data-stu-id="edac4-235">.pif</span></span>

<span data-ttu-id="edac4-236">.reg</span><span class="sxs-lookup"><span data-stu-id="edac4-236">.reg</span></span>

<span data-ttu-id="edac4-237">.scf</span><span class="sxs-lookup"><span data-stu-id="edac4-237">.scf</span></span>

<span data-ttu-id="edac4-238">.scr</span><span class="sxs-lookup"><span data-stu-id="edac4-238">.scr</span></span>

<span data-ttu-id="edac4-239">. SCT</span><span class="sxs-lookup"><span data-stu-id="edac4-239">.sct</span></span>

<span data-ttu-id="edac4-240">.shb</span><span class="sxs-lookup"><span data-stu-id="edac4-240">.shb</span></span>

<span data-ttu-id="edac4-241">.shs</span><span class="sxs-lookup"><span data-stu-id="edac4-241">.shs</span></span>

<span data-ttu-id="edac4-242">.sys</span><span class="sxs-lookup"><span data-stu-id="edac4-242">.sys</span></span>

<span data-ttu-id="edac4-243">. tlb</span><span class="sxs-lookup"><span data-stu-id="edac4-243">.tlb</span></span>

<span data-ttu-id="edac4-244">. tsp</span><span class="sxs-lookup"><span data-stu-id="edac4-244">.tsp</span></span>

<span data-ttu-id="edac4-245">.url</span><span class="sxs-lookup"><span data-stu-id="edac4-245">.url</span></span>

<span data-ttu-id="edac4-246">.vb</span><span class="sxs-lookup"><span data-stu-id="edac4-246">.vb</span></span>

<span data-ttu-id="edac4-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="edac4-247">.vbe</span></span>

<span data-ttu-id="edac4-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="edac4-248">.vbs</span></span>

<span data-ttu-id="edac4-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="edac4-249">.vsmacros</span></span>

<span data-ttu-id="edac4-250">.ws</span><span class="sxs-lookup"><span data-stu-id="edac4-250">.ws</span></span>

<span data-ttu-id="edac4-251">. ESC</span><span class="sxs-lookup"><span data-stu-id="edac4-251">.esc</span></span>

<span data-ttu-id="edac4-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="edac4-252">.wsf</span></span>

<span data-ttu-id="edac4-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="edac4-253">.wsh</span></span>

 

## <span data-ttu-id="edac4-254">Modifica di un pacchetto di applicazione virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="edac4-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="edac4-255">Puoi usare il sequencer per modificare un pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="edac4-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="edac4-256">Il computer in cui si esegue questa operazione deve corrispondere all'architettura di chip del computer usato per creare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="edac4-257">Ad esempio, se hai inizialmente sequenziato un pacchetto usando un computer che usa un sistema operativo a 64 bit, devi modificare il pacchetto usando un computer che usa un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="edac4-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="edac4-258">Come modificare un pacchetto applicazione virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="edac4-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="edac4-259">Creazione di un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="edac4-259">Creating a project template</span></span>


<span data-ttu-id="edac4-260">Un file con estensione appvt è un modello di progetto che può essere usato per salvare le impostazioni comunemente applicate e personalizzate.</span><span class="sxs-lookup"><span data-stu-id="edac4-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="edac4-261">Puoi quindi usare più facilmente queste impostazioni per le sequenziazioni future.</span><span class="sxs-lookup"><span data-stu-id="edac4-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="edac4-262">I modelli di progetto di App-V 5,0 si differenziano dagli acceleratori delle applicazioni App-V 5,0 perché gli acceleratori di applicazioni App-V 5,0 sono specifici dell'applicazione e i modelli di progetto di App-V 5,0 possono essere applicati a più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="edac4-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="edac4-263">Non è inoltre possibile usare un modello di progetto quando si usa un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="edac4-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="edac4-264">Le impostazioni generali seguenti vengono salvate con un modello di progetto App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="edac4-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="edac4-265">Un modello può specificare e archiviare più impostazioni nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="edac4-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="edac4-266">**Opzioni di monitoraggio avanzate**.</span><span class="sxs-lookup"><span data-stu-id="edac4-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="edac4-267">Consente l'esecuzione di Microsoft Update durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="edac4-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="edac4-268">Consente di salvare le impostazioni dell'opzione interazione locale</span><span class="sxs-lookup"><span data-stu-id="edac4-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="edac4-269">**Opzioni generali**.</span><span class="sxs-lookup"><span data-stu-id="edac4-269">**General Options**.</span></span> <span data-ttu-id="edac4-270">Consente l'uso di **Windows Installer**, **accodare la versione del pacchetto al nome del file**.</span><span class="sxs-lookup"><span data-stu-id="edac4-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="edac4-271">Elementi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="edac4-271">Exclusion Items.</span></span>** <span data-ttu-id="edac4-272">Contiene l'elenco dei criteri di esclusione.</span><span class="sxs-lookup"><span data-stu-id="edac4-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="edac4-273">Come creare e usare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="edac4-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="edac4-274">Creazione di un Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="edac4-274">Creating a package accelerator</span></span>


<span data-ttu-id="edac4-275">**Nota**  Gli acceleratori di pacchetti creati con una versione precedente di App-V devono essere ricreati usando App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="edac4-276">Puoi usare gli acceleratori del pacchetto App-V 5,0 per generare automaticamente nuovi pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="edac4-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="edac4-277">Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="edac4-278">In alcune situazioni, per creare l'Acceleratore pacchetto, potrebbe essere necessario installare l'applicazione localmente nel computer che esegue il sequencer.</span><span class="sxs-lookup"><span data-stu-id="edac4-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="edac4-279">In questi casi, devi prima di tutto provare a creare l'Acceleratore pacchetto con il supporto di installazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="edac4-280">Se sono necessari più file mancanti, è necessario installare l'applicazione localmente nel computer in cui viene eseguito il sequencer e quindi creare l'acceleratore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="edac4-281">Dopo aver creato un Acceleratore pacchetto, è possibile riutilizzare e condividere l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edac4-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="edac4-282">La creazione di acceleratori pacchetto App-V 5,0 è un'attività avanzata.</span><span class="sxs-lookup"><span data-stu-id="edac4-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="edac4-283">Gli acceleratori pacchetto possono contenere password e informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="edac4-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="edac4-284">È quindi necessario salvare gli acceleratori pacchetto e il supporto di installazione associato in una posizione sicura e firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="edac4-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="edac4-285">Come creare un acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="edac4-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="edac4-286">Come creare un pacchetto applicazione virtuale con un acceleratore pacchetto di App-V</span><span class="sxs-lookup"><span data-stu-id="edac4-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="edac4-287">Segnalazione errori sequenziatore</span><span class="sxs-lookup"><span data-stu-id="edac4-287">Sequencer error reporting</span></span>


<span data-ttu-id="edac4-288">Il sequencer App-V 5,0 può rilevare i problemi di sequenziazione comuni durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="edac4-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="edac4-289">La pagina del **report di installazione** alla fine della sequenziazione guidata Visualizza i messaggi di diagnostica categorizzati in **errori**, **avvisi**e **informazioni** in base alla gravità del problema.</span><span class="sxs-lookup"><span data-stu-id="edac4-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="edac4-290">Puoi anche trovare altre informazioni sulla sequenziazione degli errori usando il Visualizzatore eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="edac4-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="edac4-291">Altre risorse per l'App-V 5,0 sequencer</span><span class="sxs-lookup"><span data-stu-id="edac4-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="edac4-292">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="edac4-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





