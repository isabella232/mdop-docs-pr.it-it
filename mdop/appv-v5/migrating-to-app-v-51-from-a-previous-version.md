---
title: Migrazione ad App-V 5.1 da una versione precedente
description: Migrazione ad App-V 5.1 da una versione precedente
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805062"
---
# <span data-ttu-id="82466-103">Migrazione ad App-V 5.1 da una versione precedente</span><span class="sxs-lookup"><span data-stu-id="82466-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="82466-104">Con Microsoft Application Virtualization (App-V) 5,1, puoi eseguire la migrazione dell'infrastruttura App-V 4,6 o dell'app-v 5,0 esistente nell'infrastruttura più flessibile, integrata e più facile da gestire dell'App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="82466-105">Tuttavia, non è possibile eseguire la migrazione direttamente da App-V 4. x a App-V 5,1, per prima cosa è necessario eseguire la migrazione a App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="82466-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="82466-106">Per altre informazioni sulla migrazione da App-V 4. x a App-V 5,0, vedere [migrazione da una versione precedente](migrating-from-a-previous-version-app-v-50.md)</span><span class="sxs-lookup"><span data-stu-id="82466-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="82466-107">**Nota**  I pacchetti App-V 5,1 sono esattamente gli stessi dei pacchetti App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="82466-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="82466-108">Non è stato modificato il formato del pacchetto tra le versioni e quindi non è necessario convertire i pacchetti App-V 5,0 in pacchetti App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="82466-109">Per altre informazioni sulle differenze tra App-V 4,6 e App-V 5,1, Vedi le **differenze tra la sezione App-v 4,6 e App-v 5,0** di [About app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="82466-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="82466-110">Miglioramenti apportati al convertitore di pacchetti App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82466-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="82466-111">Ora puoi usare il convertitore di pacchetti per convertire i pacchetti App-V 4,6 che contengono script e le informazioni del registro di sistema e gli script dei file di origine. OSD ora sono inclusi nell'output del convertitore di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="82466-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="82466-112">Puoi anche usare il `–OSDsToIncludeInPackage` parametro con il `ConvertFrom-AppvLegacyPackage` cmdlet per specificare quali informazioni sui file OSD vengono convertite e inserite nel nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82466-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82466-113">Nuovo in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82466-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="82466-114">Prima dell'App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82466-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-115">I nuovi file XML vengono creati in corrispondenza dei file OSD associati a un pacchetto; questi file includono le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82466-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="82466-116">variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="82466-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="82466-117">scorciatoie</span><span class="sxs-lookup"><span data-stu-id="82466-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="82466-118">associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="82466-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="82466-119">informazioni sul Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="82466-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="82466-120">script</span><span class="sxs-lookup"><span data-stu-id="82466-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="82466-121">Ora è possibile scegliere di aggiungere informazioni da un sottoinsieme dei file OSD nella directory di origine al pacchetto usando il <code>-OSDsToIncludeInPackage</code> parametro.</span><span class="sxs-lookup"><span data-stu-id="82466-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="82466-122">Le informazioni del registro di sistema e gli script inclusi nei file OSD associati a un pacchetto non sono inclusi nell'output del convertitore di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="82466-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="82466-123">Il convertitore di pacchetti compilerebbe il nuovo pacchetto con le informazioni provenienti da tutti i file OSD nella directory di origine.</span><span class="sxs-lookup"><span data-stu-id="82466-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="82466-124">Istruzione di conversione di esempio</span><span class="sxs-lookup"><span data-stu-id="82466-124">Example conversion statement</span></span>

<span data-ttu-id="82466-125">Per informazioni sul nuovo processo, vedere l'istruzione del convertitore di pacchetti di esempio seguente `ConvertFrom-AppvLegacyPackage` .</span><span class="sxs-lookup"><span data-stu-id="82466-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="82466-126">Se la directory di origine (\\\\OldPkgStore\\ContosoApp) include le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="82466-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="82466-127">ContosoApp. SFT</span><span class="sxs-lookup"><span data-stu-id="82466-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="82466-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="82466-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="82466-129">ContosoApp. sprj</span><span class="sxs-lookup"><span data-stu-id="82466-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="82466-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="82466-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="82466-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-131">X.osd</span></span>

-   <span data-ttu-id="82466-132">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-132">Y.osd</span></span>

-   <span data-ttu-id="82466-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-133">Z.osd</span></span>

**<span data-ttu-id="82466-134">E si esegue questo comando:</span><span class="sxs-lookup"><span data-stu-id="82466-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="82466-135">Il codice seguente viene creato nella directory di destinazione (\\\\NewPkgStore\\ContosoApp):</span><span class="sxs-lookup"><span data-stu-id="82466-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="82466-136">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="82466-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="82466-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="82466-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="82466-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="82466-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="82466-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="82466-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="82466-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-140">X\_Config.xml</span></span>

-   <span data-ttu-id="82466-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="82466-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-142">Z\_Config.xml</span></span>

**<span data-ttu-id="82466-143">Nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="82466-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82466-144">Questi file della directory di origine...</span><span class="sxs-lookup"><span data-stu-id="82466-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="82466-145">... vengono convertiti in questi file di directory di destinazione...</span><span class="sxs-lookup"><span data-stu-id="82466-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="82466-146">... e conterrà questi elementi</span><span class="sxs-lookup"><span data-stu-id="82466-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="82466-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82466-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="82466-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="82466-149">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="82466-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82466-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="82466-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="82466-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="82466-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82466-154">Variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="82466-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="82466-155">Scorciatoie</span><span class="sxs-lookup"><span data-stu-id="82466-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="82466-156">Associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="82466-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="82466-157">Informazioni sul Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="82466-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="82466-158">Script</span><span class="sxs-lookup"><span data-stu-id="82466-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="82466-159">Ogni file OSD viene convertito in un file XML separato corrispondente che contiene gli elementi elencati nel formato di configurazione della distribuzione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="82466-160">Questi elementi possono quindi essere copiati da questi file XML e inseriti nella configurazione di distribuzione o nei file di configurazione dell'utente come desiderato.</span><span class="sxs-lookup"><span data-stu-id="82466-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="82466-161">In questo esempio sono presenti tre file XML, corrispondenti ai tre file OSD nella directory di origine.</span><span class="sxs-lookup"><span data-stu-id="82466-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="82466-162">Ogni file XML contiene le variabili di ambiente, i tasti di scelta rapida, le associazioni dei tipi di file, le informazioni del registro di sistema e gli script nel file OSD corrispondente.</span><span class="sxs-lookup"><span data-stu-id="82466-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="82466-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="82466-164">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="82466-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82466-165">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="82466-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="82466-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="82466-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="82466-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="82466-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="82466-168">Variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="82466-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="82466-169">Scorciatoie</span><span class="sxs-lookup"><span data-stu-id="82466-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="82466-170">Associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="82466-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="82466-171">Le informazioni dei file OSD specificati nel <code>-OSDsToIncludeInPackage</code> parametro vengono convertite e inserite all'interno del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82466-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="82466-172">Il convertitore compila quindi il file di configurazione della distribuzione e il file di configurazione dell'utente con il contenuto del pacchetto, così come fa l'App-V Sequencer durante la sequenziazione di un nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82466-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="82466-173">In questo esempio, le variabili di ambiente, i tasti di scelta rapida e le associazioni di tipi di file inclusi in X. OSD e Y. OSD sono stati convertiti e inseriti nel pacchetto App-V e alcune di queste informazioni sono state incluse anche nei file di configurazione della distribuzione e configurazione utente.</span><span class="sxs-lookup"><span data-stu-id="82466-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="82466-174">X. OSD e Y. OSD sono stati usati perché sono stati inclusi come argomenti per il <code>-OSDsToIncludeInPackage</code> parametro.</span><span class="sxs-lookup"><span data-stu-id="82466-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="82466-175">Nessuna informazione da Z. OSD è stata inclusa nel pacchetto, perché non è stata inclusa come uno di questi argomenti.</span><span class="sxs-lookup"><span data-stu-id="82466-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="82466-176">Conversione di pacchetti creati con una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="82466-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="82466-177">Usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni di App-V precedenti a App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="82466-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="82466-178">Il convertitore di pacchetti usa PowerShell per convertire i pacchetti e può aiutare a automatizzare il processo se sono presenti molti pacchetti che richiedono la conversione.</span><span class="sxs-lookup"><span data-stu-id="82466-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="82466-179">**Importante**  Dopo aver convertito un pacchetto esistente, è consigliabile testare il pacchetto prima di distribuire il pacchetto per verificare che il processo di conversione abbia avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="82466-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="82466-180">Informazioni utili prima di convertire i pacchetti esistenti</span><span class="sxs-lookup"><span data-stu-id="82466-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82466-181">Problema</span><span class="sxs-lookup"><span data-stu-id="82466-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="82466-182">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="82466-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-183">I pacchetti virtuali che usano DSC non sono collegati dopo la conversione.</span><span class="sxs-lookup"><span data-stu-id="82466-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="82466-184">Collegare i pacchetti usando i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="82466-184">Link the packages using connection groups.</span></span> <span data-ttu-id="82466-185">Vedere <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> gestione dei gruppi di connessioni </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82466-186">I conflitti di variabili di ambiente vengono rilevati durante la conversione.</span><span class="sxs-lookup"><span data-stu-id="82466-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="82466-187">Risolvere i conflitti nel <strong> file OSD associato </strong> .</span><span class="sxs-lookup"><span data-stu-id="82466-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-188">I percorsi hardcoded vengono rilevati durante la conversione.</span><span class="sxs-lookup"><span data-stu-id="82466-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="82466-189">I percorsi hardcoded sono difficili da convertire correttamente.</span><span class="sxs-lookup"><span data-stu-id="82466-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="82466-190">Il convertitore di pacchetti rileverà e restituirà pacchetti con file che contengono percorsi hardcoded.</span><span class="sxs-lookup"><span data-stu-id="82466-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="82466-191">Visualizzare il file con il percorso hardcoded e determinare se il pacchetto richiede il file.</span><span class="sxs-lookup"><span data-stu-id="82466-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="82466-192">In questo caso, è consigliabile ripetere la sequenza del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="82466-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="82466-193">Quando si converte un pacchetto, verificare la mancanza di file o tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="82466-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="82466-194">Individuare l'elemento nel pacchetto App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="82466-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="82466-195">Potrebbe anche essere un percorso hardcoded.</span><span class="sxs-lookup"><span data-stu-id="82466-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="82466-196">Convertire il percorso.</span><span class="sxs-lookup"><span data-stu-id="82466-196">Convert the path.</span></span>

<span data-ttu-id="82466-197">**Nota**  È consigliabile usare il sequencer App-V 5,1 per la conversione di applicazioni o applicazioni critiche che devono sfruttare le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="82466-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="82466-198">Vedere [come sequenziare una nuova applicazione con App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="82466-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="82466-199">Se un pacchetto convertito non si apre dopo averlo convertito, è anche consigliabile ripetere la sequenza dell'applicazione usando il sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="82466-200">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="82466-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="82466-201">Migrazione dei client</span><span class="sxs-lookup"><span data-stu-id="82466-201">Migrating Clients</span></span>


<span data-ttu-id="82466-202">Nella tabella seguente viene visualizzato il metodo consigliato per l'aggiornamento dei client.</span><span class="sxs-lookup"><span data-stu-id="82466-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82466-203">Attività</span><span class="sxs-lookup"><span data-stu-id="82466-203">Task</span></span></th>
<th align="left"><span data-ttu-id="82466-204">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="82466-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-205">Aggiornare l'ambiente alla versione più recente di App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="82466-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="82466-206">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82466-207">Installare il client App-V 5,1 con la coesistenza abilitata.</span><span class="sxs-lookup"><span data-stu-id="82466-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="82466-208">Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-209">Sequenziare e distribuire pacchetti App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="82466-210">Se necessario, Annulla la pubblicazione di pacchetti App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="82466-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="82466-211">Come sequenziare una nuova applicazione con App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="82466-212">**Importante**  È necessario eseguire la versione più recente di App-V 4.6 per usare la modalità di coesistenza.</span><span class="sxs-lookup"><span data-stu-id="82466-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="82466-213">Inoltre, quando si sequenzia un pacchetto, è necessario configurare l'impostazione dell'autorità di gestione, che si trova nella **Configurazione utente** nella sezione **Configurazione utente** .</span><span class="sxs-lookup"><span data-stu-id="82466-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="82466-214">Migrazione dell'infrastruttura completa del server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="82466-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="82466-215">Non esiste un metodo diretto per eseguire l'aggiornamento a un'infrastruttura App-V 5,1 completa.</span><span class="sxs-lookup"><span data-stu-id="82466-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="82466-216">Usare le informazioni nella sezione seguente per informazioni sull'aggiornamento del server App-V.</span><span class="sxs-lookup"><span data-stu-id="82466-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="82466-217">Attività</span><span class="sxs-lookup"><span data-stu-id="82466-217">Task</span></span></th>
<th align="left"><span data-ttu-id="82466-218">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="82466-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-219">Aggiornare l'ambiente alla versione più recente di App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="82466-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="82466-220">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82466-221">Distribuire App-V 5,1 versione del client.</span><span class="sxs-lookup"><span data-stu-id="82466-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="82466-222">Come distribuire il client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="82466-223">Installare App-V 5,1 server.</span><span class="sxs-lookup"><span data-stu-id="82466-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="82466-224">Come distribuire il server App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="82466-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="82466-225">Eseguire la migrazione dei pacchetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="82466-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="82466-226">Vedere i <strong> pacchetti di conversione creati con una versione precedente della sezione App-V </strong> di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="82466-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="82466-227">Altre attività di migrazione</span><span class="sxs-lookup"><span data-stu-id="82466-227">Additional Migration tasks</span></span>


<span data-ttu-id="82466-228">È anche possibile eseguire altre attività di migrazione, come la riconfigurazione dei punti finali e l'apertura di un pacchetto creato con una versione precedente in un computer che esegue il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="82466-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="82466-229">I collegamenti seguenti includono ulteriori informazioni sull'esecuzione di queste attività.</span><span class="sxs-lookup"><span data-stu-id="82466-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="82466-230">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="82466-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="82466-231">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="82466-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="82466-232">Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="82466-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="82466-233">Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="82466-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="82466-234">Altre risorse per l'esecuzione di attività di migrazione App-V</span><span class="sxs-lookup"><span data-stu-id="82466-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="82466-235">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="82466-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="82466-236">Procedura di aggiornamento del server di gestione di Microsoft App-V 5,1 semplificata</span><span class="sxs-lookup"><span data-stu-id="82466-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





