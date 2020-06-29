---
title: Copia dei modelli dei Criteri di gruppo di MBAM 2.5
description: Copia dei modelli dei Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825225"
---
# <span data-ttu-id="bcb16-103">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bcb16-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="bcb16-104">Prima di distribuire l'installazione di MBAM client, è necessario scaricare i modelli di criteri di gruppo di MBAM, che contengono le impostazioni dei criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bcb16-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="bcb16-105">Dopo aver scaricato i modelli, è possibile impostare le impostazioni di criteri di gruppo per l'implementazione in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="bcb16-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="bcb16-106">Scaricare e distribuire i modelli di criteri di gruppo di MDOP</span><span class="sxs-lookup"><span data-stu-id="bcb16-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="bcb16-107">I modelli di criteri di gruppo di MDOP sono disponibili per il download in un file compresso autoestraente, raggruppato per tecnologia e versione.</span><span class="sxs-lookup"><span data-stu-id="bcb16-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="bcb16-108">Come scaricare e distribuire i modelli di criteri di gruppo di MDOP</span><span class="sxs-lookup"><span data-stu-id="bcb16-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="bcb16-109">Scaricare i modelli di criteri di gruppo di MDOP dai [modelli amministrativi di criteri di gruppo di Microsoft Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=55531).</span><span class="sxs-lookup"><span data-stu-id="bcb16-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="bcb16-110">Eseguire il file scaricato per estrarre le cartelle del modello.</span><span class="sxs-lookup"><span data-stu-id="bcb16-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="bcb16-111">Warning</span><span class="sxs-lookup"><span data-stu-id="bcb16-111">Warning</span></span>**  
   <span data-ttu-id="bcb16-112">Non estrarre i modelli direttamente nella directory di distribuzione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bcb16-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="bcb16-113">In questo file vengono raggruppate più tecnologie e versioni.</span><span class="sxs-lookup"><span data-stu-id="bcb16-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="bcb16-114">Nella cartella estratta individuare il file Technology-Version. admx.</span><span class="sxs-lookup"><span data-stu-id="bcb16-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="bcb16-115">Alcune tecnologie MDOP hanno più set di oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bcb16-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="bcb16-116">Ad esempio, MBAM include le impostazioni di gestione di MBAM e le impostazioni utente di mbam.</span><span class="sxs-lookup"><span data-stu-id="bcb16-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="bcb16-117">Individuare il file con estensione adml appropriato per lingua-impostazioni cultura (ovvero, *en* per l'inglese-Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="bcb16-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="bcb16-118">Copiare i file con estensione ADMX e ADML in una cartella di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="bcb16-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="bcb16-119">A seconda della posizione in cui vengono archiviati i modelli, è possibile configurare le impostazioni dei criteri di gruppo dal dispositivo locale o da qualsiasi computer del dominio.</span><span class="sxs-lookup"><span data-stu-id="bcb16-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="bcb16-120">File locali.</span><span class="sxs-lookup"><span data-stu-id="bcb16-120">Local files.</span></span>** <span data-ttu-id="bcb16-121">Per configurare le impostazioni dei criteri di gruppo dal dispositivo locale, copiare i file dei modelli nei percorsi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bcb16-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="bcb16-122">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="bcb16-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="bcb16-123">Percorso del file</span><span class="sxs-lookup"><span data-stu-id="bcb16-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bcb16-124">Modello di criteri di gruppo (con estensione ADMX)</span><span class="sxs-lookup"><span data-stu-id="bcb16-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="bcb16-125">&lt;&gt;PolicyDefinitions forte</span><span class="sxs-lookup"><span data-stu-id="bcb16-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bcb16-126">File di lingua dei criteri di gruppo (con estensione adml)</span><span class="sxs-lookup"><span data-stu-id="bcb16-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="bcb16-127">&lt;&gt;PolicyDefinitions forte</span><span class="sxs-lookup"><span data-stu-id="bcb16-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="bcb16-128">Modificare le impostazioni dei criteri di gruppo usando la console Gestione criteri di gruppo o Advanced Group Policy Management per configurare le impostazioni dei criteri di gruppo per la tecnologia MDOP.</span><span class="sxs-lookup"><span data-stu-id="bcb16-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="bcb16-129">Per altre informazioni, vedere [modificare le impostazioni dei criteri di gruppo di MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb16-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="bcb16-130">Per le descrizioni delle impostazioni dei criteri di gruppo, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcb16-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="bcb16-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bcb16-131">Related topics</span></span>


[<span data-ttu-id="bcb16-132">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bcb16-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="bcb16-133">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="bcb16-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bcb16-134">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="bcb16-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="bcb16-135">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bcb16-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






