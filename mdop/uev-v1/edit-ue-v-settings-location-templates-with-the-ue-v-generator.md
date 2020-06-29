---
title: Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V
description: Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827115"
---
# <span data-ttu-id="1d2ff-103">Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="1d2ff-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="1d2ff-104">Usare il generatore Microsoft User Experience Virtualization (UE-V) per modificare i modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="1d2ff-105">Quando le impostazioni modificate vengono aggiunte ai modelli tramite il generatore UE-V, le informazioni sulla versione all'interno del modello vengono aggiornate automaticamente per verificare che i modelli esistenti distribuiti nell'organizzazione vengano aggiornati correttamente.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="1d2ff-106">Come modificare un modello di posizione delle impostazioni di UE-V con il generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="1d2ff-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="1d2ff-107">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="1d2ff-108">Fare clic su **modifica modello posizione impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="1d2ff-109">Nell'elenco dei modelli usati di recente selezionare il modello da modificare.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="1d2ff-110">In alternativa, **passare** al file del modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="1d2ff-111">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="1d2ff-112">Esaminare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="1d2ff-113">Modifica in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-113">Edit as needed.</span></span>

    -   <span data-ttu-id="1d2ff-114">La scheda **Proprietà** consente di visualizzare e modificare le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d2ff-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="1d2ff-115">**Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà del file di programma.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="1d2ff-116">**Nome programma**: nome del programma ricavato dalle proprietà del file di programma.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="1d2ff-117">Questo nome contiene in genere l'estensione exe.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="1d2ff-118">**Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="1d2ff-119">Questa proprietà, insieme alla **versione del file**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="1d2ff-120">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-120">This property accepts a major version number.</span></span> <span data-ttu-id="1d2ff-121">Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="1d2ff-122">**Versione file**: il numero di versione del file the.exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="1d2ff-123">Questa proprietà, insieme alla **versione del prodotto**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="1d2ff-124">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-124">This property accepts a major version number.</span></span> <span data-ttu-id="1d2ff-125">Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del programma.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="1d2ff-126">**Nome autore modello** (facoltativo): nome dell'autore del modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="1d2ff-127">**Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="1d2ff-128">La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="1d2ff-129">Per modificare i percorsi del registro di sistema, è possibile usare il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="1d2ff-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="1d2ff-130">Le attività includono l'aggiunta di nuove chiavi, la modifica del nome o dell'ambito delle chiavi esistenti, l'eliminazione di chiavi e l'esplorazione del registro di sistema in cui si trovano le chiavi.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="1d2ff-131">Quando si definisce l'ambito per il registro di sistema, è possibile usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="1d2ff-132">Usare **tutte le impostazioni** e le **sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="1d2ff-133">Nella scheda **file** sono elencati il percorso del file e la maschera di file dei percorsi di file inclusi nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="1d2ff-134">Per modificare i percorsi dei file, è possibile usare il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="1d2ff-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="1d2ff-135">Le attività per i percorsi dei file includono l'aggiunta di nuovi file o posizioni delle cartelle, la modifica dell'ambito di file o cartelle esistenti, l'eliminazione di file o cartelle e l'apertura della posizione selezionata in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="1d2ff-136">Per includere tutti i file nella cartella specificata, lascia vuota la maschera di file.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="1d2ff-137">Fare clic su **Salva** per salvare le modifiche apportate al modello posizione impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="1d2ff-138">Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="1d2ff-139">Uscire dall'applicazione Generator UE-V.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="1d2ff-140">Dopo aver modificato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="1d2ff-141">Distribuire il modello di posizione delle impostazioni modificate in un ambiente lab prima di inserirlo nella produzione aziendale.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="1d2ff-142">Come modificare manualmente un modello di posizione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="1d2ff-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="1d2ff-143">Creare una copia locale del modello di posizione delle impostazioni (file con estensione XML).</span><span class="sxs-lookup"><span data-stu-id="1d2ff-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="1d2ff-144">I modelli di posizione delle impostazioni di UE-V sono file XML che identificano le posizioni in cui i valori delle impostazioni dell'archivio applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="1d2ff-145">Aprire il file del modello di posizione delle impostazioni con un editor XML.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="1d2ff-146">Modificare il file del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-146">Edit the settings location template file.</span></span> <span data-ttu-id="1d2ff-147">Tutte le modifiche devono essere conformi al file di schema UE-V definito in SettingsLocationTempate. xsd.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="1d2ff-148">Per impostazione predefinita, viene individuata una copia del file XSD. `\ProgramData\Microsoft\UEV\Templates`</span><span class="sxs-lookup"><span data-stu-id="1d2ff-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="1d2ff-149">Salvare il file del modello di posizione delle impostazioni e chiudere l'editor XML.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="1d2ff-150">Convalidare il file del modello della posizione delle impostazioni modificate con il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="1d2ff-151">Per altre informazioni sulla convalida con il generatore UE-V, vedere [convalidare i modelli di posizione delle impostazioni di UE-v con generatore di UE-v](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="1d2ff-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="1d2ff-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d2ff-152">Related topics</span></span>


[<span data-ttu-id="1d2ff-153">Uso di modelli UE-V personalizzati e di Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="1d2ff-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="1d2ff-154">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1d2ff-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





