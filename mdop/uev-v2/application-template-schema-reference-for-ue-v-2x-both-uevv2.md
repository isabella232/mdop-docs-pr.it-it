---
title: Riferimento allo schema modello applicazione per UE-V 2. x
description: Riferimento allo schema modello applicazione per UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827406"
---
# <span data-ttu-id="91375-103">Riferimento allo schema modello applicazione per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="91375-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="91375-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usano i modelli di posizione delle impostazioni XML per definire le impostazioni dell'applicazione desktop e le impostazioni di Windows acquisite e applicate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="91375-105">UE-V include un set di modelli di posizione predefiniti per le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="91375-106">È anche possibile creare modelli di posizione delle impostazioni personalizzate con il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="91375-107">Un utente avanzato può personalizzare il file XML per un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="91375-108">Questo argomento descrive in dettaglio la struttura XML dei modelli di posizione delle impostazioni UE-V 2,1 (SP1) e 2,0 e fornisce indicazioni per la modifica di questi file.</span><span class="sxs-lookup"><span data-stu-id="91375-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="91375-109">Informazioni di riferimento sullo schema del modello di applicazione UE-V 2,1 e 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="91375-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="91375-110">Questa sezione descrive in dettaglio la struttura XML del modello di posizione delle impostazioni dell'UE-V 2,1 e 2,1 SP1 e fornisce indicazioni per la modifica di questo file.</span><span class="sxs-lookup"><span data-stu-id="91375-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="91375-111">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="91375-111">In This Section</span></span>

-   [<span data-ttu-id="91375-112">Attributo di codifica e dichiarazione XML</span><span class="sxs-lookup"><span data-stu-id="91375-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="91375-113">Spazio dei nomi e elemento radice</span><span class="sxs-lookup"><span data-stu-id="91375-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="91375-114">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="91375-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="91375-115">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="91375-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="91375-116">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="91375-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="91375-117">Elemento version</span><span class="sxs-lookup"><span data-stu-id="91375-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="91375-118">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="91375-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="91375-119">Processi ed elementi process</span><span class="sxs-lookup"><span data-stu-id="91375-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="91375-120">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="91375-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="91375-121">Elemento comune</span><span class="sxs-lookup"><span data-stu-id="91375-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="91375-122">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="91375-123">Appendice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="91375-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="91375-124">Attributo di codifica e dichiarazione XML</span><span class="sxs-lookup"><span data-stu-id="91375-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="91375-125">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-125">Mandatory: True</span></span>**

**<span data-ttu-id="91375-126">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-126">Type: String</span></span>**

<span data-ttu-id="91375-127">La dichiarazione XML deve specificare l'attributo XML version 1,0 ( &lt; ? XML version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="91375-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="91375-128">I modelli di posizione delle impostazioni creati dal generatore UE-V vengono salvati nella codifica UTF-8, anche se la codifica non è specificata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="91375-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="91375-129">È consigliabile includere l'attributo encoding = "UTF-8" in questo elemento come procedura consigliata.</span><span class="sxs-lookup"><span data-stu-id="91375-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="91375-130">Tutti i modelli inclusi nel prodotto specificano anche questo tag (Vedi i documenti in%ProgramFiles%\\Microsoft User Experience Virtualization\\Templates per riferimento).</span><span class="sxs-lookup"><span data-stu-id="91375-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="91375-131">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="91375-132">Spazio dei nomi e elemento radice</span><span class="sxs-lookup"><span data-stu-id="91375-132">Namespace and Root Element</span></span>

**<span data-ttu-id="91375-133">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-133">Mandatory: True</span></span>**

**<span data-ttu-id="91375-134">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-134">Type: String</span></span>**

<span data-ttu-id="91375-135">UE-V usa lo https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate spazio dei nomi per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="91375-136">SettingsLocationTemplate è l'elemento radice e contiene tutti gli altri elementi.</span><span class="sxs-lookup"><span data-stu-id="91375-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="91375-137">Fare riferimento a SettingsLocationTemplate in tutti i modelli usando questo tag:</span><span class="sxs-lookup"><span data-stu-id="91375-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="91375-138">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="91375-138">Data types</span></span>

<span data-ttu-id="91375-139">Questi sono i tipi di dati per lo schema del modello di applicazione UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="91375-140">**GUID** GUID descrive un'espressione regolare dell'identificatore univoco globale standard nel formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="91375-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="91375-141">Viene usato nell'elemento Filesetting\\Root\\KnownFolder per verificare la formattazione delle cartelle note.</span><span class="sxs-lookup"><span data-stu-id="91375-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="91375-142">**FilenameString** FilenameString si riferisce al nome del file di un processo da monitorare.</span><span class="sxs-lookup"><span data-stu-id="91375-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="91375-143">I relativi valori sono limitati dall'espressione Regex \ [^ \ &lt; &gt; \ \ \ \ \ /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i caratteri del colon.</span><span class="sxs-lookup"><span data-stu-id="91375-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="91375-144">**IdString** IDString fa riferimento al valore ID di elementi Application, SettingsLocationTemplate e elementi comuni (usati per descrivere i gruppi di applicazioni che condividono le impostazioni comuni).</span><span class="sxs-lookup"><span data-stu-id="91375-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="91375-145">È limitato dalla stessa Regex di FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \ &lt; &gt; \ \ \ \ \ \ \ \ \ \ /:\]+).</span><span class="sxs-lookup"><span data-stu-id="91375-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="91375-146">**TemplateVersion** TemplateVersion è un valore intero usato per descrivere la revisione del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="91375-147">Il valore può essere compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="91375-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="91375-148">**Empty** Empty fa riferimento a un valore null.</span><span class="sxs-lookup"><span data-stu-id="91375-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="91375-149">Viene usato in Process\\ShellProcess per indicare che non esiste un processo da monitorare.</span><span class="sxs-lookup"><span data-stu-id="91375-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="91375-150">Questo valore non deve essere usato nei modelli di applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="91375-151">**Autore** Il tipo di dati Author è un tipo complesso che identifica l'autore di un modello.</span><span class="sxs-lookup"><span data-stu-id="91375-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="91375-152">Contiene due elementi figlio: **nome** e **posta elettronica**.</span><span class="sxs-lookup"><span data-stu-id="91375-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="91375-153">All'interno del tipo di dati Author, l'elemento Name è obbligatorio mentre l'elemento di posta elettronica è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91375-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="91375-154">Questo tipo è descritto in modo più dettagliato sotto l'elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="91375-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="91375-155">**Intervallo** Range definisce una classe integer costituita da due elementi figlio: **Minimum** e **Maximum**.</span><span class="sxs-lookup"><span data-stu-id="91375-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="91375-156">Questo tipo di dati viene implementato nel tipo di dati ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="91375-157">Se specificato, è necessario includere i valori minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="91375-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="91375-158">**ProcessVersion** ProcessVersion definisce un tipo con quattro elementi figlio: **Major**, **minor**, **Build**e **patch**.</span><span class="sxs-lookup"><span data-stu-id="91375-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="91375-159">Questo tipo di dati viene usato dall'elemento Process per popolare i relativi valori ProductVersion e fileversion.</span><span class="sxs-lookup"><span data-stu-id="91375-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="91375-160">I dati per questo tipo sono un valore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="91375-160">The data for this type is a Range value.</span></span> <span data-ttu-id="91375-161">L'elemento figlio principale è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="91375-162">**Architettura** L'architettura enumera due valori possibili: **Win32** e **Win64**.</span><span class="sxs-lookup"><span data-stu-id="91375-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="91375-163">Questi valori vengono usati per specificare l'architettura di processo.</span><span class="sxs-lookup"><span data-stu-id="91375-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="91375-164">**Processo** Il tipo di dati processo è un contenitore usato per descrivere i processi da monitorare da UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="91375-165">Contiene sei elementi figlio: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="91375-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="91375-166">Questa tabella descrive in dettaglio i rispettivi tipi di dati di ogni elemento:</span><span class="sxs-lookup"><span data-stu-id="91375-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91375-167">Elemento</span><span class="sxs-lookup"><span data-stu-id="91375-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-168">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="91375-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-169">Mandatory</span><span class="sxs-lookup"><span data-stu-id="91375-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-170">Nome file</span><span class="sxs-lookup"><span data-stu-id="91375-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-171">FilenameString</span><span class="sxs-lookup"><span data-stu-id="91375-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-172">True</span><span class="sxs-lookup"><span data-stu-id="91375-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-173">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-174">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-175">False</span><span class="sxs-lookup"><span data-stu-id="91375-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="91375-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-177">String</span><span class="sxs-lookup"><span data-stu-id="91375-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-178">False</span><span class="sxs-lookup"><span data-stu-id="91375-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="91375-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-180">String</span><span class="sxs-lookup"><span data-stu-id="91375-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-181">False</span><span class="sxs-lookup"><span data-stu-id="91375-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="91375-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="91375-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-184">False</span><span class="sxs-lookup"><span data-stu-id="91375-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="91375-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="91375-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-187">False</span><span class="sxs-lookup"><span data-stu-id="91375-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="91375-188">**Processi** Il tipo di dati processes rappresenta un contenitore per una raccolta di uno o più elementi Process.</span><span class="sxs-lookup"><span data-stu-id="91375-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="91375-189">Nel tipo di sequenza processi sono supportati due elementi figlio: **Process** e **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="91375-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="91375-190">Process è un elemento di tipo Process e ShellProcess è di tipo dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="91375-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="91375-191">Nella sequenza devono essere identificati almeno un elemento.</span><span class="sxs-lookup"><span data-stu-id="91375-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="91375-192">**Percorso** Path viene usato da RegistrySetting e filesetting per fare riferimento ai percorsi del registro di sistema e dei file.</span><span class="sxs-lookup"><span data-stu-id="91375-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="91375-193">Questo elemento supporta due attributi facoltativi: **ricorsive** e **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="91375-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="91375-194">Entrambi i valori sono impostati su default = "false".</span><span class="sxs-lookup"><span data-stu-id="91375-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="91375-195">Ricorsive indica che il percorso e tutte le sottocartelle sono incluse per le impostazioni dei file o che tutte le chiavi del registro di sistema figlio sono incluse per le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91375-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="91375-196">In entrambi i casi, tutti gli elementi a livello corrente sono inclusi nei dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="91375-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="91375-197">Per un oggetto fileSettings, tutti i file all'interno della cartella specificata sono inclusi nei dati acquisiti da UE-V, ma le cartelle non sono incluse.</span><span class="sxs-lookup"><span data-stu-id="91375-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="91375-198">Per i percorsi del registro di sistema, vengono acquisiti tutti i valori nel percorso corrente, ma le chiavi del registro di sistema figlio non vengono acquisite.</span><span class="sxs-lookup"><span data-stu-id="91375-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="91375-199">In entrambi i casi, è necessario prestare attenzione per evitare l'acquisizione di set di dati di grandi dimensioni o un numero elevato di elementi.</span><span class="sxs-lookup"><span data-stu-id="91375-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="91375-200">L'attributo DeleteIfNotFound rimuove l'impostazione dai dati del percorso di archiviazione delle impostazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91375-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="91375-201">Questo potrebbe essere utile nei casi in cui la rimozione di queste impostazioni dal pacchetto salverà una grande quantità di spazio su disco nel file server del percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="91375-202">**FileMask** FileMask specifica solo determinati tipi di file per la cartella definita da path.</span><span class="sxs-lookup"><span data-stu-id="91375-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="91375-203">Ad esempio, Path può essere `C:\users\username\files` e FileMask può `*.txt` includere solo file di testo.</span><span class="sxs-lookup"><span data-stu-id="91375-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="91375-204">**RegistrySetting** RegistrySetting rappresenta un contenitore per le chiavi del registro di sistema e i valori e il comportamento desiderato associato da parte dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="91375-205">In questo tipo sono definiti quattro elementi figlio: **path**, **Name**, **Exclude**e una sequenza di valori **path** e **Name**.</span><span class="sxs-lookup"><span data-stu-id="91375-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="91375-206">**Impostazione Filesetting** Filesetting contiene i parametri associati ai percorsi di file e file.</span><span class="sxs-lookup"><span data-stu-id="91375-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="91375-207">Vengono definiti quattro elementi figlio: **root**, **path**, **FileMask**ed **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="91375-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="91375-208">Root è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="91375-209">**Impostazioni** Settings è un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-210">Contiene le istanze delle impostazioni del registro di sistema, file, SystemParameter e CustomAction descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="91375-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="91375-211">Inoltre, può contenere anche gli elementi figlio seguenti con i comportamenti descritti:</span><span class="sxs-lookup"><span data-stu-id="91375-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91375-212">Elemento</span><span class="sxs-lookup"><span data-stu-id="91375-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-214">Asincrona</span><span class="sxs-lookup"><span data-stu-id="91375-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-215">I pacchetti di impostazioni asincrone vengono applicati senza bloccare l'avvio dell'applicazione in modo che l'avvio dell'applicazione proceda mentre le impostazioni sono ancora applicate.</span><span class="sxs-lookup"><span data-stu-id="91375-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="91375-216">Questa operazione è utile per le impostazioni che possono essere applicate in modo asincrono, ad esempio quelle <code>get/set</code> tramite un'API, come SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="91375-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="91375-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-218">Per impostazione predefinita, UE-V Salva solo le impostazioni per un'applicazione quando viene chiusa l'ultima istanza di un'applicazione che usa il modello.</span><span class="sxs-lookup"><span data-stu-id="91375-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="91375-219">Quando questo elemento è impostato su "false", UE-V Esporta le impostazioni anche se sono in uso altre istanze di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="91375-220">Modelli adatti: quelli che includono una sezione elemento comune, forniti con UE-V, usano questo contrassegno per consentire alle impostazioni condivise di esportare sempre in prossimità dell'applicazione, impedendo l'esportazione di impostazioni specifiche dell'applicazione finché non viene chiusa l'ultima istanza.</span><span class="sxs-lookup"><span data-stu-id="91375-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="91375-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-222">(introdotta in 2,1)</span><span class="sxs-lookup"><span data-stu-id="91375-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="91375-223">Questo parametro impone l'applicazione di un pacchetto di impostazioni importato anche se non ci sono differenze tra il pacchetto e lo stato corrente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="91375-224">Questo parametro deve essere usato solo in casi particolari perché può rallentare l'importazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="91375-225">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="91375-225">Name Element</span></span>

**<span data-ttu-id="91375-226">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-226">Mandatory: True</span></span>**

**<span data-ttu-id="91375-227">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-227">Type: String</span></span>**

<span data-ttu-id="91375-228">Nome specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-229">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-230">In generale, evita di fare riferimento alle informazioni sulla versione, perché questo può essere obiettato dall'elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="91375-231">Ad esempio, specificare `<Name>My Application</Name>` invece di `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="91375-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="91375-232">**Nota**  UE-V non fa riferimento a DTD esterni, quindi non è possibile usare le entità denominate in un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="91375-233">Ad esempio, non usare per &reg; fare riferimento al segno di firma del marchio registrato®.</span><span class="sxs-lookup"><span data-stu-id="91375-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="91375-234">USA invece i riferimenti numerati canonici per includere questi tipi di caratteri speciali, ad esempio & \ #174 per il carattere®.</span><span class="sxs-lookup"><span data-stu-id="91375-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="91375-235">Questa regola si applica a tutti i valori stringa in questo documento.</span><span class="sxs-lookup"><span data-stu-id="91375-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="91375-236">Vedere <http://www.w3.org/TR/xhtml1/dtds.html> per un elenco completo delle entità di caratteri.</span><span class="sxs-lookup"><span data-stu-id="91375-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="91375-237">I documenti con codifica UTF-8 possono includere direttamente i caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="91375-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="91375-238">Il salvataggio dei modelli tramite il generatore UE-V converte automaticamente le entità di caratteri nelle rappresentazioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="91375-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="91375-239">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="91375-239">ID Element</span></span>

**<span data-ttu-id="91375-240">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-240">Mandatory: True</span></span>**

**<span data-ttu-id="91375-241">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-241">Type: String</span></span>**

<span data-ttu-id="91375-242">ID popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-243">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione, ad esempio, Vedi l'output dei cmdlet di PowerShell Get-UevTemplate e Get-UevTemplateProgram.</span><span class="sxs-lookup"><span data-stu-id="91375-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="91375-244">Per convenzione, questo tag non deve contenere spazi, che semplificano lo scripting.</span><span class="sxs-lookup"><span data-stu-id="91375-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="91375-245">I numeri di versione delle applicazioni devono essere specificati in questo elemento per consentire una facile identificazione del modello, ad esempio `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="91375-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="91375-246">Elemento version</span><span class="sxs-lookup"><span data-stu-id="91375-246">Version Element</span></span>

**<span data-ttu-id="91375-247">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-247">Mandatory: True</span></span>**

**<span data-ttu-id="91375-248">Digitare: integer</span><span class="sxs-lookup"><span data-stu-id="91375-248">Type: Integer</span></span>**

**<span data-ttu-id="91375-249">Valore minimo: 0</span><span class="sxs-lookup"><span data-stu-id="91375-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="91375-250">Valore massimo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="91375-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="91375-251">La versione identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-252">Il generatore UE-V incrementa automaticamente questo numero per uno ogni volta che il modello viene salvato.</span><span class="sxs-lookup"><span data-stu-id="91375-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="91375-253">Si noti che questo campo deve essere un numero intero Integer; i valori frazionari, ad esempio `<Version>2.5</Version>` non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="91375-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="91375-254">**Suggerimento:** È possibile salvare le note sulle modifiche della versione usando i tag di commento XML `<!-- -->` , ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="91375-255">**Importante**  Questo valore viene interrogato per determinare se una nuova versione di un modello deve essere applicata a un modello esistente in queste istanze:</span><span class="sxs-lookup"><span data-stu-id="91375-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="91375-256">Quando viene eseguita l'attività di aggiornamento automatico del modello programmato</span><span class="sxs-lookup"><span data-stu-id="91375-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="91375-257">Quando viene eseguito il cmdlet di PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="91375-258">Quando viene chiamato il metodo di aggiornamento microsoft\\uev: SettingsLocationTemplate tramite WMI</span><span class="sxs-lookup"><span data-stu-id="91375-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="91375-259">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="91375-259">Author Element</span></span>

**<span data-ttu-id="91375-260">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-260">Mandatory: False</span></span>**

**<span data-ttu-id="91375-261">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-261">Type: String</span></span>**

<span data-ttu-id="91375-262">Autore identifica il creatore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="91375-263">Sono supportati due elementi figlio facoltativi: **nome** e **posta elettronica**.</span><span class="sxs-lookup"><span data-stu-id="91375-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="91375-264">Entrambi gli attributi sono facoltativi, ma, se l'elemento figlio del messaggio di posta elettronica viene specificato, deve essere accompagnato dall'elemento Name.</span><span class="sxs-lookup"><span data-stu-id="91375-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="91375-265">Autore fa riferimento al nome completo del contatto per il modello di posizione delle impostazioni e la posta elettronica deve fare riferimento a un indirizzo di posta elettronica per l'autore.</span><span class="sxs-lookup"><span data-stu-id="91375-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="91375-266">È consigliabile includere queste informazioni nei modelli pubblicati pubblicamente, ad esempio nella [raccolta modelli di UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="91375-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="91375-267">Processi ed elementi process</span><span class="sxs-lookup"><span data-stu-id="91375-267">Processes and Process Element</span></span>

**<span data-ttu-id="91375-268">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-268">Mandatory: True</span></span>**

**<span data-ttu-id="91375-269">Digitare: elemento</span><span class="sxs-lookup"><span data-stu-id="91375-269">Type: Element</span></span>**

<span data-ttu-id="91375-270">I processi contengono almeno un `<Process>` elemento, che a sua volta contiene gli elementi figlio seguenti: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="91375-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="91375-271">L'elemento figlio filename è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="91375-272">Un elemento completamente popolato contiene tag simili a questo esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="91375-273">Nome file</span><span class="sxs-lookup"><span data-stu-id="91375-273">Filename</span></span>

**<span data-ttu-id="91375-274">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-274">Mandatory: True</span></span>**

**<span data-ttu-id="91375-275">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-275">Type: String</span></span>**

<span data-ttu-id="91375-276">Filename si riferisce al nome effettivo del file eseguibile visualizzato nel file System.</span><span class="sxs-lookup"><span data-stu-id="91375-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="91375-277">Questo elemento specifica il criterio principale usato da UE-V per valutare se un modello si applica o meno a un processo.</span><span class="sxs-lookup"><span data-stu-id="91375-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="91375-278">Questo elemento deve essere specificato nel codice XML del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="91375-279">I nomi file validi non devono corrispondere all'espressione regolare \ [^ \ \ \ \ \ \ \ &lt; &gt; /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i due punti (il \ \?</span><span class="sxs-lookup"><span data-stu-id="91375-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="91375-280">\* | &lt; &gt; /o: caratteri.).</span><span class="sxs-lookup"><span data-stu-id="91375-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="91375-281">**Suggerimento:** Per testare una stringa con questa regex, usare una finestra di comando di PowerShell e sostituire il nome dell'eseguibile per **nomefile**:</span><span class="sxs-lookup"><span data-stu-id="91375-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="91375-282">Il valore **true** indica che la stringa contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="91375-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="91375-283">Ecco alcuni esempi di valori illegali:</span><span class="sxs-lookup"><span data-stu-id="91375-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="91375-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="91375-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="91375-285">Program \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="91375-285">Program\*.exe</span></span>

-   <span data-ttu-id="91375-286">ram.exe Pro?</span><span class="sxs-lookup"><span data-stu-id="91375-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="91375-287">Programma &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="91375-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="91375-288">**Nota**  Il generatore UE-V codifica i caratteri maggiore di e minore di e &gt; &lt; rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="91375-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="91375-289">In rari casi, il valore FileName non include necessariamente l'estensione exe, ma deve essere specificato come parte del valore.</span><span class="sxs-lookup"><span data-stu-id="91375-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="91375-290">Ad esempio, `<Filename>MyApplictication.exe</Filename>` deve essere specificato al posto di `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="91375-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="91375-291">Il secondo esempio non applica il modello al processo se il nome effettivo del file eseguibile è "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="91375-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="91375-292">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-292">Architecture</span></span>

**<span data-ttu-id="91375-293">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-293">Mandatory: False</span></span>**

**<span data-ttu-id="91375-294">Digitare: Architecture (String)</span><span class="sxs-lookup"><span data-stu-id="91375-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="91375-295">L'architettura si riferisce all'architettura del processore per cui è stato compilato l'eseguibile di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91375-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="91375-296">I valori validi sono Win32 per le applicazioni a 32 bit o Win64 per le applicazioni a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="91375-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="91375-297">Se presente, questo tag limita l'applicabilità del modello di posizione delle impostazioni a una particolare architettura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="91375-298">Per un esempio, confronta l'esperienza utente di%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e MicrosoftOffice2010Win64.xml file inclusi in UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="91375-299">Questa operazione è utile quando i percorsi relativi cambiano tra versioni diverse di un file eseguibile o se le impostazioni sono state aggiunte o rimosse quando si spostano da un'architettura del processore a un'altra.</span><span class="sxs-lookup"><span data-stu-id="91375-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="91375-300">Se questo elemento è assente, il modello di posizione delle impostazioni ignora l'architettura del processo e si applica ai processi di 32 e 64 bit se il nome file e gli altri attributi si applicano.</span><span class="sxs-lookup"><span data-stu-id="91375-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="91375-301">**Nota**  UE-V non supporta i processori ARM in questa versione.</span><span class="sxs-lookup"><span data-stu-id="91375-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="91375-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="91375-302">ProductName</span></span>

**<span data-ttu-id="91375-303">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-303">Mandatory: False</span></span>**

**<span data-ttu-id="91375-304">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-304">Type: String</span></span>**

<span data-ttu-id="91375-305">ProductName è un elemento facoltativo usato per identificare un prodotto per scopi amministrativi o per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="91375-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="91375-306">ProductName è diverso dal nome del file, in quanto il relativo valore non contiene restrizioni per le espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="91375-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="91375-307">In questo modo è possibile comprendere più facilmente le descrizioni di un processo in cui il nome eseguibile potrebbe non essere ovvio.</span><span class="sxs-lookup"><span data-stu-id="91375-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="91375-308">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="91375-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="91375-309">FileDescription</span></span>

**<span data-ttu-id="91375-310">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-310">Mandatory: False</span></span>**

**<span data-ttu-id="91375-311">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-311">Type: String</span></span>**

<span data-ttu-id="91375-312">FileDescription è un tag facoltativo che consente di avere una descrizione amministrativa del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91375-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="91375-313">Si tratta di un campo di testo gratuito e può essere utile per distinguere più eseguibili in un pacchetto software in cui è necessario identificare la funzione dell'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91375-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="91375-314">Ad esempio, in un'applicazione appropriata può essere utile specificare i promemoria relativi alla funzione di due eseguibili (MyApplication.exe e MyApplicationHelper.exe), come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="91375-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="91375-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="91375-315">ProductVersion</span></span>

**<span data-ttu-id="91375-316">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-316">Mandatory: False</span></span>**

**<span data-ttu-id="91375-317">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-317">Type: String</span></span>**

<span data-ttu-id="91375-318">ProductVersion si riferisce alle versioni di prodotto principali e secondarie di un file, oltre a una build e a un livello di patch.</span><span class="sxs-lookup"><span data-stu-id="91375-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="91375-319">ProductVersion è un elemento facoltativo, ma se specificato deve contenere almeno l'elemento figlio principale.</span><span class="sxs-lookup"><span data-stu-id="91375-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="91375-320">Il valore deve esprimere un intervallo nella forma Minimum = "X" Maximum = "Y" dove X e Y sono numeri interi.</span><span class="sxs-lookup"><span data-stu-id="91375-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="91375-321">I valori minimo e massimo possono essere identici.</span><span class="sxs-lookup"><span data-stu-id="91375-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="91375-322">Gli elementi della versione del prodotto e del file possono essere lasciati non specificati.</span><span class="sxs-lookup"><span data-stu-id="91375-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="91375-323">In questo modo il modello si applica a "versione agnostica", ovvero il modello verrà applicato a tutte le versioni del file eseguibile specificato.</span><span class="sxs-lookup"><span data-stu-id="91375-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="91375-324">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="91375-324">Example 1:</span></span>**

<span data-ttu-id="91375-325">Versione del prodotto: 1,0 specificato nel generatore di UE-V produce il codice XML seguente:</span><span class="sxs-lookup"><span data-stu-id="91375-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="91375-326">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="91375-326">Example 2:</span></span>**

<span data-ttu-id="91375-327">Versione file: 5.0.2.1000 specificato nel generatore UE-V produce il codice XML seguente:</span><span class="sxs-lookup"><span data-stu-id="91375-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="91375-328">Esempio errato 1-intervallo incompleto:</span><span class="sxs-lookup"><span data-stu-id="91375-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="91375-329">È presente solo l'attributo Minimum.</span><span class="sxs-lookup"><span data-stu-id="91375-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="91375-330">Anche il valore massimo deve essere incluso in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="91375-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="91375-331">Esempio errato 2-secondario specificato senza elemento principale:</span><span class="sxs-lookup"><span data-stu-id="91375-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="91375-332">Solo l'elemento secondario è presente.</span><span class="sxs-lookup"><span data-stu-id="91375-332">Only the Minor element is present.</span></span> <span data-ttu-id="91375-333">Anche Major deve essere incluso.</span><span class="sxs-lookup"><span data-stu-id="91375-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="91375-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="91375-334">FileVersion</span></span>

**<span data-ttu-id="91375-335">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-335">Mandatory: False</span></span>**

**<span data-ttu-id="91375-336">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-336">Type: String</span></span>**

<span data-ttu-id="91375-337">FileVersion differenzia la versione finale di un'applicazione pubblicata e i dettagli di compilazione interni di un eseguibile del componente.</span><span class="sxs-lookup"><span data-stu-id="91375-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="91375-338">Per la maggior parte delle applicazioni commerciali, questi numeri sono identici.</span><span class="sxs-lookup"><span data-stu-id="91375-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="91375-339">Dove variano, la versione del prodotto di un file indica l'identificazione di una versione generica di un file, mentre la versione del file indica una build specifica di un file, come nel caso di un hotfix o di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="91375-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="91375-340">Questo identifica in modo univoco i file senza interrompere la logica di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="91375-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="91375-341">Per determinare la versione del prodotto e la versione del file di un determinato eseguibile, fare clic con il pulsante destro del mouse sul file in Esplora risorse, scegliere Proprietà e quindi fare clic sulla scheda Dettagli.</span><span class="sxs-lookup"><span data-stu-id="91375-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="91375-342">L'inclusione di un elemento FileVersion per un'applicazione consente di definire una logica di rilevamento più granulare, ma non è necessaria per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="91375-343">Le impostazioni dell'elemento ProductVersion sono controllate per prime e quindi viene selezionata la versione Fileversion.</span><span class="sxs-lookup"><span data-stu-id="91375-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="91375-344">Verrà applicata l'impostazione più restrittiva.</span><span class="sxs-lookup"><span data-stu-id="91375-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="91375-345">Gli elementi figlio e le regole di sintassi per fileversion sono identici a quelli di ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="91375-346">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="91375-346">Application Element</span></span>

<span data-ttu-id="91375-347">Application è un contenitore per le impostazioni che si applicano a una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="91375-348">Si tratta di una raccolta dei campi/tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91375-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91375-349">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-350">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-351">Name</span><span class="sxs-lookup"><span data-stu-id="91375-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-352">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-353">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-354">Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-355">ID</span><span class="sxs-lookup"><span data-stu-id="91375-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-356">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-357">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-358">Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-359">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-360">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-362">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-364">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-365">Versione</span><span class="sxs-lookup"><span data-stu-id="91375-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-366">Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-367">Per altre informazioni, vedere la <a href="#version21" data-raw-source="[Version](#version21)"> versione </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="91375-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-369">Controlla se il modello è abilitato in combinazione con un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91375-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="91375-370">Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="91375-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-372">Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365.</span><span class="sxs-lookup"><span data-stu-id="91375-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="91375-373">Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-374">FixedProfile (introdotta in 2,1)</span><span class="sxs-lookup"><span data-stu-id="91375-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-375">Specifica che questo modello può essere associato solo al profilo specificato in questo elemento e non può essere modificato tramite WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91375-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-376">Processi</span><span class="sxs-lookup"><span data-stu-id="91375-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-377">Un contenitore per una raccolta di uno o più elementi Process.</span><span class="sxs-lookup"><span data-stu-id="91375-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="91375-378">Per altre informazioni, vedere <a href="#processes21" data-raw-source="[Processes](#processes21)"> processi </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-379">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="91375-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-380">Un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-381">Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="91375-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="91375-382">Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data21" data-raw-source="[Data types](#data21)"> tipi di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="91375-383">Elemento comune</span><span class="sxs-lookup"><span data-stu-id="91375-383">Common Element</span></span>

<span data-ttu-id="91375-384">Common è simile a un elemento Application, ma è sempre associato a due o più elementi Application.</span><span class="sxs-lookup"><span data-stu-id="91375-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="91375-385">La sezione comune rappresenta il set di impostazioni condivise tra le istanze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="91375-386">Si tratta di una raccolta dei campi/tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91375-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91375-387">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-388">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-389">Name</span><span class="sxs-lookup"><span data-stu-id="91375-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-390">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-391">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-392">Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-393">ID</span><span class="sxs-lookup"><span data-stu-id="91375-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-394">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-395">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-396">Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-397">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-398">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-400">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-402">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-403">Versione</span><span class="sxs-lookup"><span data-stu-id="91375-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-404">Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-405">Per altre informazioni, vedere la <a href="#version21" data-raw-source="[Version](#version21)"> versione </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="91375-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-407">Controlla se il modello è abilitato in combinazione con un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91375-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="91375-408">Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="91375-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-410">Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365.</span><span class="sxs-lookup"><span data-stu-id="91375-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="91375-411">Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-412">FixedProfile (introdotta in 2,1)</span><span class="sxs-lookup"><span data-stu-id="91375-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-413">Specifica che questo modello può essere associato solo al profilo specificato in questo elemento e non può essere modificato tramite WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91375-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-414">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="91375-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-415">Un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-416">Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="91375-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="91375-417">Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data21" data-raw-source="[Data types](#data21)"> tipi di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="91375-418">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="91375-419">Questo elemento definisce le impostazioni per una singola applicazione o una famiglia di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91375-420">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="91375-421">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-422">Name</span><span class="sxs-lookup"><span data-stu-id="91375-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-423">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-424">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-425">Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-426">ID</span><span class="sxs-lookup"><span data-stu-id="91375-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-427">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-428">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-429">Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-430">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-431">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-433">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-435">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="91375-436">Appendice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="91375-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="91375-437">Ecco il file SettingsLocationTemplate. xsd che Mostra gli elementi, gli elementi figlio, gli attributi e i parametri:</span><span class="sxs-lookup"><span data-stu-id="91375-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="91375-438">Informazioni di riferimento sullo schema del modello di applicazione UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="91375-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="91375-439">Questa sezione descrive in dettaglio la struttura XML del modello di posizione delle impostazioni di 2,0 UE-V e fornisce indicazioni per la modifica di questo file.</span><span class="sxs-lookup"><span data-stu-id="91375-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="91375-440">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="91375-440">In This Section</span></span>

-   [<span data-ttu-id="91375-441">Attributo di codifica e dichiarazione XML</span><span class="sxs-lookup"><span data-stu-id="91375-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="91375-442">Spazio dei nomi e elemento radice</span><span class="sxs-lookup"><span data-stu-id="91375-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="91375-443">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="91375-443">Data types</span></span>](#data)

-   [<span data-ttu-id="91375-444">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="91375-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="91375-445">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="91375-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="91375-446">Elemento version</span><span class="sxs-lookup"><span data-stu-id="91375-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="91375-447">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="91375-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="91375-448">Processi ed elementi process</span><span class="sxs-lookup"><span data-stu-id="91375-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="91375-449">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="91375-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="91375-450">Elemento comune</span><span class="sxs-lookup"><span data-stu-id="91375-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="91375-451">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="91375-452">Appendice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="91375-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="91375-453">Attributo di codifica e dichiarazione XML</span><span class="sxs-lookup"><span data-stu-id="91375-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="91375-454">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-454">Mandatory: True</span></span>**

**<span data-ttu-id="91375-455">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-455">Type: String</span></span>**

<span data-ttu-id="91375-456">La dichiarazione XML deve specificare l'attributo XML version 1,0 ( &lt; ? XML version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="91375-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="91375-457">I modelli di posizione delle impostazioni creati dal generatore UE-V vengono salvati nella codifica UTF-8, anche se la codifica non è specificata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="91375-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="91375-458">È consigliabile includere l'attributo encoding = "UTF-8" in questo elemento come procedura consigliata.</span><span class="sxs-lookup"><span data-stu-id="91375-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="91375-459">Tutti i modelli inclusi nel prodotto specificano anche questo tag (Vedi i documenti in%ProgramFiles%\\Microsoft User Experience Virtualization\\Templates per riferimento).</span><span class="sxs-lookup"><span data-stu-id="91375-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="91375-460">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="91375-461">Spazio dei nomi e elemento radice</span><span class="sxs-lookup"><span data-stu-id="91375-461">Namespace and Root Element</span></span>

**<span data-ttu-id="91375-462">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-462">Mandatory: True</span></span>**

**<span data-ttu-id="91375-463">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-463">Type: String</span></span>**

<span data-ttu-id="91375-464">UE-V usa lo https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate spazio dei nomi per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="91375-465">SettingsLocationTemplate è l'elemento radice e contiene tutti gli altri elementi.</span><span class="sxs-lookup"><span data-stu-id="91375-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="91375-466">Fare riferimento a SettingsLocationTemplate in tutti i modelli usando questo tag:</span><span class="sxs-lookup"><span data-stu-id="91375-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="91375-467">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="91375-467">Data types</span></span>

<span data-ttu-id="91375-468">Questi sono i tipi di dati per lo schema del modello di applicazione UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="91375-469">**GUID** GUID descrive un'espressione regolare dell'identificatore univoco globale standard nel formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="91375-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="91375-470">Viene usato nell'elemento Filesetting\\Root\\KnownFolder per verificare la formattazione delle cartelle note.</span><span class="sxs-lookup"><span data-stu-id="91375-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="91375-471">**FilenameString** FilenameString si riferisce al nome del file di un processo da monitorare.</span><span class="sxs-lookup"><span data-stu-id="91375-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="91375-472">I relativi valori sono limitati dall'espressione Regex \ [^ \ &lt; &gt; \ \ \ \ \ /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i caratteri del colon.</span><span class="sxs-lookup"><span data-stu-id="91375-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="91375-473">**IdString** IDString fa riferimento al valore ID di elementi Application, SettingsLocationTemplate e elementi comuni (usati per descrivere i gruppi di applicazioni che condividono le impostazioni comuni).</span><span class="sxs-lookup"><span data-stu-id="91375-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="91375-474">È limitato dalla stessa Regex di FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \ &lt; &gt; \ \ \ \ \ \ \ \ \ \ /:\]+).</span><span class="sxs-lookup"><span data-stu-id="91375-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="91375-475">**TemplateVersion** TemplateVersion è un valore intero usato per descrivere la revisione del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="91375-476">Il valore può essere compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="91375-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="91375-477">**Empty** Empty fa riferimento a un valore null.</span><span class="sxs-lookup"><span data-stu-id="91375-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="91375-478">Viene usato in Process\\ShellProcess per indicare che non esiste un processo da monitorare.</span><span class="sxs-lookup"><span data-stu-id="91375-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="91375-479">Questo valore non deve essere usato nei modelli di applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="91375-480">**Autore** Il tipo di dati Author è un tipo complesso che identifica l'autore di un modello.</span><span class="sxs-lookup"><span data-stu-id="91375-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="91375-481">Contiene due elementi figlio: **nome** e **posta elettronica**.</span><span class="sxs-lookup"><span data-stu-id="91375-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="91375-482">All'interno del tipo di dati Author, l'elemento Name è obbligatorio mentre l'elemento di posta elettronica è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91375-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="91375-483">Questo tipo è descritto in modo più dettagliato sotto l'elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="91375-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="91375-484">**Intervallo** Range definisce una classe integer costituita da due elementi figlio: **Minimum** e **Maximum**.</span><span class="sxs-lookup"><span data-stu-id="91375-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="91375-485">Questo tipo di dati viene implementato nel tipo di dati ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="91375-486">Se specificato, è necessario includere i valori minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="91375-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="91375-487">**ProcessVersion** ProcessVersion definisce un tipo con quattro elementi figlio: **Major**, **minor**, **Build**e **patch**.</span><span class="sxs-lookup"><span data-stu-id="91375-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="91375-488">Questo tipo di dati viene usato dall'elemento Process per popolare i relativi valori ProductVersion e fileversion.</span><span class="sxs-lookup"><span data-stu-id="91375-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="91375-489">I dati per questo tipo sono un valore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="91375-489">The data for this type is a Range value.</span></span> <span data-ttu-id="91375-490">L'elemento figlio principale è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="91375-491">**Architettura** L'architettura enumera due valori possibili: **Win32** e **Win64**.</span><span class="sxs-lookup"><span data-stu-id="91375-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="91375-492">Questi valori vengono usati per specificare l'architettura di processo.</span><span class="sxs-lookup"><span data-stu-id="91375-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="91375-493">**Processo** Il tipo di dati processo è un contenitore usato per descrivere i processi da monitorare da UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="91375-494">Contiene sei elementi figlio: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="91375-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="91375-495">Questa tabella descrive in dettaglio i rispettivi tipi di dati di ogni elemento:</span><span class="sxs-lookup"><span data-stu-id="91375-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91375-496">Elemento</span><span class="sxs-lookup"><span data-stu-id="91375-496">Element</span></span></th>
<th align="left"><span data-ttu-id="91375-497">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="91375-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="91375-498">Mandatory</span><span class="sxs-lookup"><span data-stu-id="91375-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-499">Nome file</span><span class="sxs-lookup"><span data-stu-id="91375-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-500">FilenameString</span><span class="sxs-lookup"><span data-stu-id="91375-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-501">True</span><span class="sxs-lookup"><span data-stu-id="91375-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-502">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-503">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-504">False</span><span class="sxs-lookup"><span data-stu-id="91375-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="91375-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-506">String</span><span class="sxs-lookup"><span data-stu-id="91375-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-507">False</span><span class="sxs-lookup"><span data-stu-id="91375-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="91375-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-509">String</span><span class="sxs-lookup"><span data-stu-id="91375-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-510">False</span><span class="sxs-lookup"><span data-stu-id="91375-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="91375-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="91375-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-513">False</span><span class="sxs-lookup"><span data-stu-id="91375-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="91375-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="91375-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-516">False</span><span class="sxs-lookup"><span data-stu-id="91375-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="91375-517">**Processi** Il tipo di dati processes rappresenta un contenitore per una raccolta di uno o più elementi Process.</span><span class="sxs-lookup"><span data-stu-id="91375-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="91375-518">Nel tipo di sequenza processi sono supportati due elementi figlio: **Process** e **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="91375-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="91375-519">Process è un elemento di tipo Process e ShellProcess è di tipo dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="91375-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="91375-520">Nella sequenza devono essere identificati almeno un elemento.</span><span class="sxs-lookup"><span data-stu-id="91375-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="91375-521">**Percorso** Path viene usato da RegistrySetting e filesetting per fare riferimento ai percorsi del registro di sistema e dei file.</span><span class="sxs-lookup"><span data-stu-id="91375-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="91375-522">Questo elemento supporta due attributi facoltativi: **ricorsive** e **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="91375-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="91375-523">Entrambi i valori sono impostati su default = "false".</span><span class="sxs-lookup"><span data-stu-id="91375-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="91375-524">Ricorsive indica che il percorso e tutte le sottocartelle sono incluse per le impostazioni dei file o che tutte le chiavi del registro di sistema figlio sono incluse per le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91375-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="91375-525">In entrambi i casi, tutti gli elementi a livello corrente sono inclusi nei dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="91375-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="91375-526">Per un oggetto fileSettings, tutti i file all'interno della cartella specificata sono inclusi nei dati acquisiti da UE-V, ma le cartelle non sono incluse.</span><span class="sxs-lookup"><span data-stu-id="91375-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="91375-527">Per i percorsi del registro di sistema, vengono acquisiti tutti i valori nel percorso corrente, ma le chiavi del registro di sistema figlio non vengono acquisite.</span><span class="sxs-lookup"><span data-stu-id="91375-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="91375-528">In entrambi i casi, è necessario prestare attenzione per evitare l'acquisizione di set di dati di grandi dimensioni o un numero elevato di elementi.</span><span class="sxs-lookup"><span data-stu-id="91375-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="91375-529">L'attributo DeleteIfNotFound rimuove l'impostazione dai dati del percorso di archiviazione delle impostazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91375-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="91375-530">Questo potrebbe essere utile nei casi in cui la rimozione di queste impostazioni dal pacchetto salverà una grande quantità di spazio su disco nel file server del percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="91375-531">**FileMask** FileMask specifica solo determinati tipi di file per la cartella definita da path.</span><span class="sxs-lookup"><span data-stu-id="91375-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="91375-532">Ad esempio, Path può essere `C:\users\username\files` e FileMask può `*.txt` includere solo file di testo.</span><span class="sxs-lookup"><span data-stu-id="91375-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="91375-533">**RegistrySetting** RegistrySetting rappresenta un contenitore per le chiavi del registro di sistema e i valori e il comportamento desiderato associato da parte dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="91375-534">In questo tipo sono definiti quattro elementi figlio: **path**, **Name**, **Exclude**e una sequenza di valori **path** e **Name**.</span><span class="sxs-lookup"><span data-stu-id="91375-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="91375-535">**Impostazione Filesetting** Filesetting contiene i parametri associati ai percorsi di file e file.</span><span class="sxs-lookup"><span data-stu-id="91375-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="91375-536">Vengono definiti quattro elementi figlio: **root**, **path**, **FileMask**ed **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="91375-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="91375-537">Root è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="91375-538">**Impostazioni** Settings è un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-539">Contiene le istanze delle impostazioni del registro di sistema, file, SystemParameter e CustomAction descritte in precedenza.</span><span class="sxs-lookup"><span data-stu-id="91375-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="91375-540">Inoltre, può contenere anche gli elementi figlio seguenti con i comportamenti descritti:</span><span class="sxs-lookup"><span data-stu-id="91375-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91375-541">Elemento</span><span class="sxs-lookup"><span data-stu-id="91375-541">Element</span></span></th>
<th align="left"><span data-ttu-id="91375-542">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-543">Asincrona</span><span class="sxs-lookup"><span data-stu-id="91375-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-544">I pacchetti di impostazioni asincrone vengono applicati senza bloccare l'avvio dell'applicazione in modo che l'avvio dell'applicazione proceda mentre le impostazioni sono ancora applicate.</span><span class="sxs-lookup"><span data-stu-id="91375-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="91375-545">Questa operazione è utile per le impostazioni che possono essere applicate in modo asincrono, ad esempio quelle <code>get/set</code> tramite un'API, come SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="91375-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="91375-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-547">Per impostazione predefinita, UE-V Salva solo le impostazioni per un'applicazione quando viene chiusa l'ultima istanza di un'applicazione che usa il modello.</span><span class="sxs-lookup"><span data-stu-id="91375-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="91375-548">Quando questo elemento è impostato su "false", UE-V Esporta le impostazioni anche se sono in uso altre istanze di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="91375-549">Modelli adatti: quelli che includono una sezione elemento comune, forniti con UE-V, usano questo contrassegno per consentire alle impostazioni condivise di esportare sempre in prossimità dell'applicazione, impedendo l'esportazione di impostazioni specifiche dell'applicazione finché non viene chiusa l'ultima istanza.</span><span class="sxs-lookup"><span data-stu-id="91375-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="91375-550">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="91375-550">Name Element</span></span>

**<span data-ttu-id="91375-551">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-551">Mandatory: True</span></span>**

**<span data-ttu-id="91375-552">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-552">Type: String</span></span>**

<span data-ttu-id="91375-553">Nome specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-554">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-555">In generale, evita di fare riferimento alle informazioni sulla versione, perché questo può essere obiettato dall'elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="91375-556">Ad esempio, specificare `<Name>My Application</Name>` invece di `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="91375-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="91375-557">**Nota**  UE-V non fa riferimento a DTD esterni, quindi non è possibile usare le entità denominate in un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="91375-558">Ad esempio, non usare per &reg; fare riferimento al segno di firma del marchio registrato®.</span><span class="sxs-lookup"><span data-stu-id="91375-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="91375-559">USA invece i riferimenti numerati canonici per includere questi tipi di caratteri speciali, ad esempio & \ #174 per il carattere®.</span><span class="sxs-lookup"><span data-stu-id="91375-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="91375-560">Questa regola si applica a tutti i valori stringa in questo documento.</span><span class="sxs-lookup"><span data-stu-id="91375-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="91375-561">Vedere <http://www.w3.org/TR/xhtml1/dtds.html> per un elenco completo delle entità di caratteri.</span><span class="sxs-lookup"><span data-stu-id="91375-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="91375-562">I documenti con codifica UTF-8 possono includere direttamente i caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="91375-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="91375-563">Il salvataggio dei modelli tramite il generatore UE-V converte automaticamente le entità di caratteri nelle rappresentazioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="91375-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="91375-564">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="91375-564">ID Element</span></span>

**<span data-ttu-id="91375-565">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-565">Mandatory: True</span></span>**

**<span data-ttu-id="91375-566">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-566">Type: String</span></span>**

<span data-ttu-id="91375-567">ID popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-568">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione, ad esempio, Vedi l'output dei cmdlet di PowerShell Get-UevTemplate e Get-UevTemplateProgram.</span><span class="sxs-lookup"><span data-stu-id="91375-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="91375-569">Per convenzione, questo tag non deve contenere spazi, che semplificano lo scripting.</span><span class="sxs-lookup"><span data-stu-id="91375-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="91375-570">I numeri di versione delle applicazioni devono essere specificati in questo elemento per consentire una facile identificazione del modello, ad esempio `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="91375-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="91375-571">Elemento version</span><span class="sxs-lookup"><span data-stu-id="91375-571">Version Element</span></span>

**<span data-ttu-id="91375-572">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-572">Mandatory: True</span></span>**

**<span data-ttu-id="91375-573">Digitare: integer</span><span class="sxs-lookup"><span data-stu-id="91375-573">Type: Integer</span></span>**

**<span data-ttu-id="91375-574">Valore minimo: 0</span><span class="sxs-lookup"><span data-stu-id="91375-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="91375-575">Valore massimo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="91375-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="91375-576">La versione identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-577">Il generatore UE-V incrementa automaticamente questo numero per uno ogni volta che il modello viene salvato.</span><span class="sxs-lookup"><span data-stu-id="91375-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="91375-578">Si noti che questo campo deve essere un numero intero Integer; i valori frazionari, ad esempio `<Version>2.5</Version>` non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="91375-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="91375-579">**Suggerimento:** È possibile salvare le note sulle modifiche della versione usando i tag di commento XML `<!-- -->` , ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="91375-580">**Importante**  Questo valore viene interrogato per determinare se una nuova versione di un modello deve essere applicata a un modello esistente in queste istanze:</span><span class="sxs-lookup"><span data-stu-id="91375-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="91375-581">Quando viene eseguita l'attività di aggiornamento automatico del modello programmato</span><span class="sxs-lookup"><span data-stu-id="91375-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="91375-582">Quando viene eseguito il cmdlet di PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="91375-583">Quando viene chiamato il metodo di aggiornamento microsoft\\uev: SettingsLocationTemplate tramite WMI</span><span class="sxs-lookup"><span data-stu-id="91375-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="91375-584">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="91375-584">Author Element</span></span>

**<span data-ttu-id="91375-585">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-585">Mandatory: False</span></span>**

**<span data-ttu-id="91375-586">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-586">Type: String</span></span>**

<span data-ttu-id="91375-587">Autore identifica il creatore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="91375-588">Sono supportati due elementi figlio facoltativi: **nome** e **posta elettronica**.</span><span class="sxs-lookup"><span data-stu-id="91375-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="91375-589">Entrambi gli attributi sono facoltativi, ma, se l'elemento figlio del messaggio di posta elettronica viene specificato, deve essere accompagnato dall'elemento Name.</span><span class="sxs-lookup"><span data-stu-id="91375-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="91375-590">Autore fa riferimento al nome completo del contatto per il modello di posizione delle impostazioni e la posta elettronica deve fare riferimento a un indirizzo di posta elettronica per l'autore.</span><span class="sxs-lookup"><span data-stu-id="91375-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="91375-591">È consigliabile includere queste informazioni nei modelli pubblicati pubblicamente, ad esempio nella [raccolta modelli di UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="91375-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="91375-592">Processi ed elementi process</span><span class="sxs-lookup"><span data-stu-id="91375-592">Processes and Process Element</span></span>

**<span data-ttu-id="91375-593">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-593">Mandatory: True</span></span>**

**<span data-ttu-id="91375-594">Digitare: elemento</span><span class="sxs-lookup"><span data-stu-id="91375-594">Type: Element</span></span>**

<span data-ttu-id="91375-595">I processi contengono almeno un `<Process>` elemento, che a sua volta contiene gli elementi figlio seguenti: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**.</span><span class="sxs-lookup"><span data-stu-id="91375-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="91375-596">L'elemento figlio filename è obbligatorio e gli altri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="91375-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="91375-597">Un elemento completamente popolato contiene tag simili a questo esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="91375-598">Nome file</span><span class="sxs-lookup"><span data-stu-id="91375-598">Filename</span></span>

**<span data-ttu-id="91375-599">Obbligatorio: vero</span><span class="sxs-lookup"><span data-stu-id="91375-599">Mandatory: True</span></span>**

**<span data-ttu-id="91375-600">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-600">Type: String</span></span>**

<span data-ttu-id="91375-601">Filename si riferisce al nome effettivo del file eseguibile visualizzato nel file System.</span><span class="sxs-lookup"><span data-stu-id="91375-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="91375-602">Questo elemento specifica il criterio principale usato da UE-V per valutare se un modello si applica o meno a un processo.</span><span class="sxs-lookup"><span data-stu-id="91375-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="91375-603">Questo elemento deve essere specificato nel codice XML del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="91375-604">I nomi file validi non devono corrispondere all'espressione regolare \ [^ \ \ \ \ \ \ \ &lt; &gt; /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i due punti (il \ \?</span><span class="sxs-lookup"><span data-stu-id="91375-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="91375-605">\* | &lt; &gt; /o: caratteri.).</span><span class="sxs-lookup"><span data-stu-id="91375-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="91375-606">**Suggerimento:** Per testare una stringa con questa regex, usare una finestra di comando di PowerShell e sostituire il nome dell'eseguibile per **nomefile**:</span><span class="sxs-lookup"><span data-stu-id="91375-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="91375-607">Il valore **true** indica che la stringa contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="91375-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="91375-608">Ecco alcuni esempi di valori illegali:</span><span class="sxs-lookup"><span data-stu-id="91375-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="91375-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="91375-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="91375-610">Program \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="91375-610">Program\*.exe</span></span>

-   <span data-ttu-id="91375-611">ram.exe Pro?</span><span class="sxs-lookup"><span data-stu-id="91375-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="91375-612">Programma &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="91375-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="91375-613">**Nota**  Il generatore UE-V codifica i caratteri maggiore di e minore di e &gt; &lt; rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="91375-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="91375-614">In rari casi, il valore FileName non include necessariamente l'estensione exe, ma deve essere specificato come parte del valore.</span><span class="sxs-lookup"><span data-stu-id="91375-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="91375-615">Ad esempio, `<Filename>MyApplictication.exe</Filename>` deve essere specificato al posto di `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="91375-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="91375-616">Il secondo esempio non applica il modello al processo se il nome effettivo del file eseguibile è "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="91375-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="91375-617">Architettura</span><span class="sxs-lookup"><span data-stu-id="91375-617">Architecture</span></span>

**<span data-ttu-id="91375-618">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-618">Mandatory: False</span></span>**

**<span data-ttu-id="91375-619">Digitare: Architecture (String)</span><span class="sxs-lookup"><span data-stu-id="91375-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="91375-620">L'architettura si riferisce all'architettura del processore per cui è stato compilato l'eseguibile di destinazione.</span><span class="sxs-lookup"><span data-stu-id="91375-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="91375-621">I valori validi sono Win32 per le applicazioni a 32 bit o Win64 per le applicazioni a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="91375-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="91375-622">Se presente, questo tag limita l'applicabilità del modello di posizione delle impostazioni a una particolare architettura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="91375-623">Per un esempio, confronta l'esperienza utente di%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e MicrosoftOffice2010Win64.xml file inclusi in UE-V.</span><span class="sxs-lookup"><span data-stu-id="91375-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="91375-624">Questa operazione è utile quando i percorsi relativi cambiano tra versioni diverse di un file eseguibile o se le impostazioni sono state aggiunte o rimosse quando si spostano da un'architettura del processore a un'altra.</span><span class="sxs-lookup"><span data-stu-id="91375-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="91375-625">Se questo elemento è assente, il modello di posizione delle impostazioni ignora l'architettura del processo e si applica ai processi di 32 e 64 bit se il nome file e gli altri attributi si applicano.</span><span class="sxs-lookup"><span data-stu-id="91375-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="91375-626">**Nota**  UE-V non supporta i processori ARM in questa versione.</span><span class="sxs-lookup"><span data-stu-id="91375-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="91375-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="91375-627">ProductName</span></span>

**<span data-ttu-id="91375-628">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-628">Mandatory: False</span></span>**

**<span data-ttu-id="91375-629">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-629">Type: String</span></span>**

<span data-ttu-id="91375-630">ProductName è un elemento facoltativo usato per identificare un prodotto per scopi amministrativi o per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="91375-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="91375-631">ProductName è diverso dal nome del file, in quanto il relativo valore non contiene restrizioni per le espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="91375-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="91375-632">In questo modo è possibile comprendere più facilmente le descrizioni di un processo in cui il nome eseguibile potrebbe non essere ovvio.</span><span class="sxs-lookup"><span data-stu-id="91375-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="91375-633">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="91375-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="91375-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="91375-634">FileDescription</span></span>

**<span data-ttu-id="91375-635">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-635">Mandatory: False</span></span>**

**<span data-ttu-id="91375-636">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-636">Type: String</span></span>**

<span data-ttu-id="91375-637">FileDescription è un tag facoltativo che consente di avere una descrizione amministrativa del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91375-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="91375-638">Si tratta di un campo di testo gratuito e può essere utile per distinguere più eseguibili in un pacchetto software in cui è necessario identificare la funzione dell'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91375-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="91375-639">Ad esempio, in un'applicazione appropriata può essere utile specificare i promemoria relativi alla funzione di due eseguibili (MyApplication.exe e MyApplicationHelper.exe), come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="91375-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="91375-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="91375-640">ProductVersion</span></span>

**<span data-ttu-id="91375-641">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-641">Mandatory: False</span></span>**

**<span data-ttu-id="91375-642">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-642">Type: String</span></span>**

<span data-ttu-id="91375-643">ProductVersion si riferisce alle versioni di prodotto principali e secondarie di un file, oltre a una build e a un livello di patch.</span><span class="sxs-lookup"><span data-stu-id="91375-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="91375-644">ProductVersion è un elemento facoltativo, ma se specificato deve contenere almeno l'elemento figlio principale.</span><span class="sxs-lookup"><span data-stu-id="91375-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="91375-645">Il valore deve esprimere un intervallo nella forma Minimum = "X" Maximum = "Y" dove X e Y sono numeri interi.</span><span class="sxs-lookup"><span data-stu-id="91375-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="91375-646">I valori minimo e massimo possono essere identici.</span><span class="sxs-lookup"><span data-stu-id="91375-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="91375-647">Gli elementi della versione del prodotto e del file possono essere lasciati non specificati.</span><span class="sxs-lookup"><span data-stu-id="91375-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="91375-648">In questo modo il modello si applica a "versione agnostica", ovvero il modello verrà applicato a tutte le versioni del file eseguibile specificato.</span><span class="sxs-lookup"><span data-stu-id="91375-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="91375-649">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="91375-649">Example 1:</span></span>**

<span data-ttu-id="91375-650">Versione del prodotto: 1,0 specificato nel generatore di UE-V produce il codice XML seguente:</span><span class="sxs-lookup"><span data-stu-id="91375-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="91375-651">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="91375-651">Example 2:</span></span>**

<span data-ttu-id="91375-652">Versione file: 5.0.2.1000 specificato nel generatore UE-V produce il codice XML seguente:</span><span class="sxs-lookup"><span data-stu-id="91375-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="91375-653">Esempio errato 1-intervallo incompleto:</span><span class="sxs-lookup"><span data-stu-id="91375-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="91375-654">È presente solo l'attributo Minimum.</span><span class="sxs-lookup"><span data-stu-id="91375-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="91375-655">Anche il valore massimo deve essere incluso in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="91375-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="91375-656">Esempio errato 2-secondario specificato senza elemento principale:</span><span class="sxs-lookup"><span data-stu-id="91375-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="91375-657">Solo l'elemento secondario è presente.</span><span class="sxs-lookup"><span data-stu-id="91375-657">Only the Minor element is present.</span></span> <span data-ttu-id="91375-658">Anche Major deve essere incluso.</span><span class="sxs-lookup"><span data-stu-id="91375-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="91375-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="91375-659">FileVersion</span></span>

**<span data-ttu-id="91375-660">Obbligatorio: falso</span><span class="sxs-lookup"><span data-stu-id="91375-660">Mandatory: False</span></span>**

**<span data-ttu-id="91375-661">Digitare: stringa</span><span class="sxs-lookup"><span data-stu-id="91375-661">Type: String</span></span>**

<span data-ttu-id="91375-662">FileVersion differenzia la versione finale di un'applicazione pubblicata e i dettagli di compilazione interni di un eseguibile del componente.</span><span class="sxs-lookup"><span data-stu-id="91375-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="91375-663">Per la maggior parte delle applicazioni commerciali, questi numeri sono identici.</span><span class="sxs-lookup"><span data-stu-id="91375-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="91375-664">Dove variano, la versione del prodotto di un file indica l'identificazione di una versione generica di un file, mentre la versione del file indica una build specifica di un file, come nel caso di un hotfix o di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="91375-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="91375-665">Questo identifica in modo univoco i file senza interrompere la logica di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="91375-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="91375-666">Per determinare la versione del prodotto e la versione del file di un determinato eseguibile, fare clic con il pulsante destro del mouse sul file in Esplora risorse, scegliere Proprietà e quindi fare clic sulla scheda Dettagli.</span><span class="sxs-lookup"><span data-stu-id="91375-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="91375-667">L'inclusione di un elemento FileVersion per un'applicazione consente di definire una logica di rilevamento più granulare, ma non è necessaria per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="91375-668">Le impostazioni dell'elemento ProductVersion sono controllate per prime e quindi viene selezionata la versione Fileversion.</span><span class="sxs-lookup"><span data-stu-id="91375-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="91375-669">Verrà applicata l'impostazione più restrittiva.</span><span class="sxs-lookup"><span data-stu-id="91375-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="91375-670">Gli elementi figlio e le regole di sintassi per fileversion sono identici a quelli di ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="91375-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="91375-671">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="91375-671">Application Element</span></span>

<span data-ttu-id="91375-672">Application è un contenitore per le impostazioni che si applicano a una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="91375-673">Si tratta di una raccolta dei campi/tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91375-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91375-674">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="91375-675">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-676">Name</span><span class="sxs-lookup"><span data-stu-id="91375-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-677">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-678">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-679">Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-680">ID</span><span class="sxs-lookup"><span data-stu-id="91375-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-681">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-682">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-683">Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-684">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-685">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-687">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-689">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-690">Versione</span><span class="sxs-lookup"><span data-stu-id="91375-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-691">Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-692">Per altre informazioni, vedere la <a href="#version" data-raw-source="[Version](#version)"> versione </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="91375-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-694">Controlla se il modello è abilitato in combinazione con un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91375-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="91375-695">Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="91375-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-697">Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365.</span><span class="sxs-lookup"><span data-stu-id="91375-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="91375-698">Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-699">Processi</span><span class="sxs-lookup"><span data-stu-id="91375-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-700">Un contenitore per una raccolta di uno o più elementi Process.</span><span class="sxs-lookup"><span data-stu-id="91375-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="91375-701">Per altre informazioni, vedere <a href="#processes" data-raw-source="[Processes](#processes)"> processi </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-702">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="91375-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-703">Un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-704">Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="91375-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="91375-705">Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data" data-raw-source="[Data types](#data)"> tipi di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="91375-706">Elemento comune</span><span class="sxs-lookup"><span data-stu-id="91375-706">Common Element</span></span>

<span data-ttu-id="91375-707">Common è simile a un elemento Application, ma è sempre associato a due o più elementi Application.</span><span class="sxs-lookup"><span data-stu-id="91375-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="91375-708">La sezione comune rappresenta il set di impostazioni condivise tra le istanze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91375-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="91375-709">Si tratta di una raccolta dei campi/tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91375-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91375-710">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="91375-711">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-712">Name</span><span class="sxs-lookup"><span data-stu-id="91375-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-713">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-714">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-715">Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-716">ID</span><span class="sxs-lookup"><span data-stu-id="91375-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-717">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-718">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-719">Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-720">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-721">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-723">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-725">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-726">Versione</span><span class="sxs-lookup"><span data-stu-id="91375-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-727">Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="91375-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="91375-728">Per altre informazioni, vedere la <a href="#version" data-raw-source="[Version](#version)"> versione </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="91375-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-730">Controlla se il modello è abilitato in combinazione con un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91375-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="91375-731">Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="91375-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-733">Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365.</span><span class="sxs-lookup"><span data-stu-id="91375-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="91375-734">Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91375-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-735">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="91375-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-736">Un contenitore per tutte le impostazioni che si applicano a un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="91375-737">Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="91375-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="91375-738">Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data" data-raw-source="[Data types](#data)"> tipi di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="91375-739">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="91375-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="91375-740">Questo elemento definisce le impostazioni per una singola applicazione o una famiglia di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91375-741">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="91375-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="91375-742">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-743">Name</span><span class="sxs-lookup"><span data-stu-id="91375-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-744">Specifica un nome univoco per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="91375-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="91375-745">Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug.</span><span class="sxs-lookup"><span data-stu-id="91375-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="91375-746">Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-747">ID</span><span class="sxs-lookup"><span data-stu-id="91375-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-748">Popola un identificatore univoco per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="91375-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="91375-749">Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91375-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="91375-750">Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="91375-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-751">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91375-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-752">Descrizione facoltativa del modello.</span><span class="sxs-lookup"><span data-stu-id="91375-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="91375-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="91375-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-754">Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</span><span class="sxs-lookup"><span data-stu-id="91375-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="91375-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="91375-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="91375-756">Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</span><span class="sxs-lookup"><span data-stu-id="91375-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="91375-757">Appendice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="91375-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="91375-758">Ecco il file SettingsLocationTemplate. xsd che Mostra gli elementi, gli elementi figlio, gli attributi e i parametri:</span><span class="sxs-lookup"><span data-stu-id="91375-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="91375-759">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91375-759">Related topics</span></span>


[<span data-ttu-id="91375-760">Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="91375-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="91375-761">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="91375-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





