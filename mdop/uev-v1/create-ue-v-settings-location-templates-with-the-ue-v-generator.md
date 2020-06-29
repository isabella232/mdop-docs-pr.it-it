---
title: Creare modelli percorsi impostazioni UE-V con Generatore UE-V
description: Creare modelli percorsi impostazioni UE-V con Generatore UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826645"
---
# <span data-ttu-id="477eb-103">Creare modelli percorsi impostazioni UE-V con Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="477eb-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="477eb-104">Microsoft User Experience Virtualization (UE-V) USA i *modelli di posizione delle impostazioni* per aggirare le impostazioni delle applicazioni tra i computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="477eb-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="477eb-105">Alcuni modelli di posizione standard delle impostazioni sono inclusi nella virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="477eb-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="477eb-106">È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate con il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="477eb-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="477eb-107">Il generatore di UE-V monitora un'applicazione per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="477eb-108">L'applicazione che viene monitorata deve essere un'applicazione tradizionale.</span><span class="sxs-lookup"><span data-stu-id="477eb-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="477eb-109">Il generatore UE-V non può creare un modello di posizione delle impostazioni dai tipi di applicazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="477eb-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="477eb-110">Applicazioni virtualizzate</span><span class="sxs-lookup"><span data-stu-id="477eb-110">Virtualized applications</span></span>

-   <span data-ttu-id="477eb-111">Applicazione offerta tramite Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="477eb-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="477eb-112">Applicazioni Java</span><span class="sxs-lookup"><span data-stu-id="477eb-112">Java applications</span></span>

-   <span data-ttu-id="477eb-113">Applicazioni di Windows 8</span><span class="sxs-lookup"><span data-stu-id="477eb-113">Windows 8 applications</span></span>

<span data-ttu-id="477eb-114">**Nota**  I modelli UE-V non possono essere creati da applicazioni virtualizzate o da applicazioni di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="477eb-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="477eb-115">Tuttavia, le impostazioni sincronizzate con i modelli possono essere applicate a tali applicazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="477eb-116">Per creare modelli che supportano le applicazioni VDI (Virtual Desktop Infrastructure) e Servizi terminal, aprire una versione di Windows Installer (con estensione msi) dell'applicazione con il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="477eb-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="477eb-117">Percorsi esclusi</span><span class="sxs-lookup"><span data-stu-id="477eb-117">Excluded Locations</span></span>**

<span data-ttu-id="477eb-118">Il processo di individuazione esclude le posizioni che in genere archiviano i file software dell'applicazione che non si spostano correttamente tra i computer degli utenti o gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="477eb-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="477eb-119">Gli elementi seguenti sono esclusi:</span><span class="sxs-lookup"><span data-stu-id="477eb-119">The following are excluded:</span></span>

-   <span data-ttu-id="477eb-120">HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori</span><span class="sxs-lookup"><span data-stu-id="477eb-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="477eb-121">HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows</span><span class="sxs-lookup"><span data-stu-id="477eb-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="477eb-122">Tutte le chiavi del registro di sistema situate nell'HKEY \ _LOCAL \ _MACHINE hive</span><span class="sxs-lookup"><span data-stu-id="477eb-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="477eb-123">File che si trovano nelle directory dei file di programma</span><span class="sxs-lookup"><span data-stu-id="477eb-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="477eb-124">File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="477eb-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="477eb-125">File di sistema operativo Windows che si trovano in% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="477eb-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="477eb-126">Se le chiavi del registro di sistema e i file archiviati in questi percorsi esclusi sono necessari per il roaming delle impostazioni dell'applicazione, gli amministratori possono aggiungere manualmente le posizioni al modello di posizione delle impostazioni durante il processo di creazione del modello.</span><span class="sxs-lookup"><span data-stu-id="477eb-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="477eb-127">Creare modelli UE-V</span><span class="sxs-lookup"><span data-stu-id="477eb-127">Create UE-V templates</span></span>


<span data-ttu-id="477eb-128">Usare il generatore UE-V per creare modelli di posizione delle impostazioni per le applicazioni line-of-business o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="477eb-129">Dopo la creazione del modello per un'applicazione, è possibile distribuire il modello ai computer in modo che gli utenti possano aggirare le impostazioni per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="477eb-130">Per creare un modello di posizione delle impostazioni di UE-V con il generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="477eb-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="477eb-131">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="477eb-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="477eb-132">Fare clic su **Crea modello posizione impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="477eb-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="477eb-133">Specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-133">Specify the application.</span></span> <span data-ttu-id="477eb-134">Individuare il percorso del file dell'applicazione (con estensione exe) o il collegamento all'applicazione (con estensione lnk) per cui si vuole creare un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="477eb-135">Specificare gli argomenti della riga di comando, se presenti, e la directory di lavoro, se presenti.</span><span class="sxs-lookup"><span data-stu-id="477eb-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="477eb-136">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="477eb-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="477eb-137">**Nota**  Prima che l'applicazione venga avviata, il sistema Visualizza un prompt per il **controllo dell'account utente**.</span><span class="sxs-lookup"><span data-stu-id="477eb-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="477eb-138">È necessaria l'autorizzazione per monitorare il registro di sistema e i percorsi dei file usati dall'applicazione per archiviare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="477eb-139">Dopo l'avvio dell'applicazione, chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-139">After the application starts, close the application.</span></span> <span data-ttu-id="477eb-140">Il generatore UE-V registra le posizioni in cui vengono archiviate le impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="477eb-141">Al termine del processo, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="477eb-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="477eb-142">Esaminare e selezionare le caselle di controllo accanto alle posizioni appropriate per le impostazioni del registro di sistema e alle posizioni dei file di impostazioni per spostarsi nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="477eb-143">L'elenco include le due categorie seguenti per i percorsi delle impostazioni:</span><span class="sxs-lookup"><span data-stu-id="477eb-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="477eb-144">**Standard**: impostazioni dell'applicazione archiviate nel registro di sistema in HKEY \ _CURRENT \ _USER i tasti o nelle cartelle file in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="477eb-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="477eb-145">Il generatore UE-V include queste impostazioni per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="477eb-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="477eb-146">Non **standard**: impostazioni dell'applicazione archiviate all'esterno dei percorsi specificati nelle procedure consigliate per l'archiviazione dei dati delle impostazioni (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="477eb-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="477eb-147">Questi includono file e cartelle in **utenti** \ \ \ [nome utente \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="477eb-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="477eb-148">Esaminare queste posizioni per determinare se includerle nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="477eb-149">Selezionare le caselle di controllo percorsi per includerle.</span><span class="sxs-lookup"><span data-stu-id="477eb-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="477eb-150">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="477eb-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="477eb-151">Rivedere e modificare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="477eb-152">Modificare le proprietà seguenti nella scheda **Proprietà** :</span><span class="sxs-lookup"><span data-stu-id="477eb-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="477eb-153">**Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà dei file di programma.</span><span class="sxs-lookup"><span data-stu-id="477eb-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="477eb-154">**Nome programma**: nome del programma ricavato dalle proprietà del file di programma.</span><span class="sxs-lookup"><span data-stu-id="477eb-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="477eb-155">Questo nome contiene in genere l'estensione exe.</span><span class="sxs-lookup"><span data-stu-id="477eb-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="477eb-156">**Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="477eb-157">Questa proprietà, insieme alla versione del file, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="477eb-158">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="477eb-158">This property accepts a major version number.</span></span> <span data-ttu-id="477eb-159">Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del prodotto.</span><span class="sxs-lookup"><span data-stu-id="477eb-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="477eb-160">**Versione file**: il numero di versione del file the.exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="477eb-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="477eb-161">Questa proprietà, insieme alla versione del prodotto, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="477eb-162">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="477eb-162">This property accepts a major version number.</span></span> <span data-ttu-id="477eb-163">Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del programma.</span><span class="sxs-lookup"><span data-stu-id="477eb-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="477eb-164">**Nome autore modello** (facoltativo): nome dell'autore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="477eb-165">**Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="477eb-166">La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="477eb-167">Modificare i percorsi del registro di sistema tramite il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="477eb-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="477eb-168">Le attività includono l'aggiunta di nuove chiavi, la modifica del nome o dell'ambito delle chiavi esistenti, l'eliminazione di chiavi e l'esplorazione del registro di sistema in cui si trovano i tasti.</span><span class="sxs-lookup"><span data-stu-id="477eb-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="477eb-169">Usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="477eb-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="477eb-170">Usare **tutte le impostazioni e le sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.</span><span class="sxs-lookup"><span data-stu-id="477eb-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="477eb-171">Nella scheda **file** sono elencati il percorso del file e la maschera di file dei percorsi di file inclusi nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="477eb-172">Modificare i percorsi dei file usando il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="477eb-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="477eb-173">Le attività per i percorsi dei file includono l'aggiunta di nuovi file o posizioni delle cartelle, la modifica dell'ambito di file o cartelle esistenti, l'eliminazione di file o cartelle e l'apertura della posizione selezionata in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="477eb-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="477eb-174">Lascia vuota la maschera di file per includere tutti i file nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="477eb-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="477eb-175">Fare clic su **Crea** e salvare il modello posizione impostazioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="477eb-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="477eb-176">Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="477eb-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="477eb-177">Uscire dall'applicazione Generator UE-V.</span><span class="sxs-lookup"><span data-stu-id="477eb-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="477eb-178">Dopo aver creato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello.</span><span class="sxs-lookup"><span data-stu-id="477eb-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="477eb-179">Distribuire il modello in un ambiente lab prima di inserirlo nella produzione aziendale.</span><span class="sxs-lookup"><span data-stu-id="477eb-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="477eb-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="477eb-180">Related topics</span></span>


[<span data-ttu-id="477eb-181">Uso di modelli UE-V personalizzati e di Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="477eb-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="477eb-182">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="477eb-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





