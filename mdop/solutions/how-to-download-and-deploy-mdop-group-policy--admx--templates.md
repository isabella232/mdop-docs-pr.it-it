---
title: Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)
description: Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826916"
---
# <span data-ttu-id="47cc1-103">Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)</span><span class="sxs-lookup"><span data-stu-id="47cc1-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="47cc1-104">Puoi gestire le impostazioni delle caratteristiche di alcune tecnologie MDOP (Microsoft Desktop Optimization Pack), ad esempio App-V, UE-V o MBAM, usando i modelli di criteri di gruppo, i file con estensione ADMX e adml.</span><span class="sxs-lookup"><span data-stu-id="47cc1-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="47cc1-105">I modelli di criteri di gruppo di MDOP sono disponibili per il download in un file compresso autoestraente, raggruppato per tecnologia e versione.</span><span class="sxs-lookup"><span data-stu-id="47cc1-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="47cc1-106">Modelli di criteri di gruppo di MDOP</span><span class="sxs-lookup"><span data-stu-id="47cc1-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="47cc1-107">Come scaricare e distribuire i modelli di criteri di gruppo di MDOP</span><span class="sxs-lookup"><span data-stu-id="47cc1-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="47cc1-108">Scaricare i [modelli di criteri di gruppo](https://www.microsoft.com/download/details.aspx?id=55531) più recenti di MDOP</span><span class="sxs-lookup"><span data-stu-id="47cc1-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="47cc1-109">Espandere il file CAB scaricato eseguendo</span><span class="sxs-lookup"><span data-stu-id="47cc1-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="47cc1-110">Warning</span><span class="sxs-lookup"><span data-stu-id="47cc1-110">Warning</span></span>**  
   <span data-ttu-id="47cc1-111">Non estrarre i modelli direttamente nella directory di distribuzione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="47cc1-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="47cc1-112">In questo file vengono raggruppate più tecnologie e versioni.</span><span class="sxs-lookup"><span data-stu-id="47cc1-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="47cc1-113">Nella cartella estratta individuare il file Technology-Version. admx.</span><span class="sxs-lookup"><span data-stu-id="47cc1-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="47cc1-114">Alcune tecnologie MDOP hanno più set di oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="47cc1-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="47cc1-115">Ad esempio, MBAM include le impostazioni di gestione di MBAM e le impostazioni utente di mbam.</span><span class="sxs-lookup"><span data-stu-id="47cc1-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="47cc1-116">Individuare il file con estensione adml appropriato per lingua-impostazioni cultura (ovvero *en-US* per l'inglese-Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="47cc1-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="47cc1-117">Copiare i file con estensione ADMX e ADML in una cartella di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="47cc1-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="47cc1-118">A seconda della posizione in cui vengono archiviati i modelli, è possibile configurare le impostazioni dei criteri di gruppo dal dispositivo locale o da qualsiasi computer del dominio.</span><span class="sxs-lookup"><span data-stu-id="47cc1-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="47cc1-119">**File locali:** Per configurare le impostazioni dei criteri di gruppo dal dispositivo locale, copiare i file dei modelli nei percorsi seguenti:</span><span class="sxs-lookup"><span data-stu-id="47cc1-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="47cc1-120">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="47cc1-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="47cc1-121">Percorso del file</span><span class="sxs-lookup"><span data-stu-id="47cc1-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="47cc1-122">Modello di criteri di gruppo (con estensione ADMX)</span><span class="sxs-lookup"><span data-stu-id="47cc1-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="47cc1-123">&lt;&gt;PolicyDefinitions forte</span><span class="sxs-lookup"><span data-stu-id="47cc1-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="47cc1-124">File di lingua dei criteri di gruppo (con estensione adml)</span><span class="sxs-lookup"><span data-stu-id="47cc1-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="47cc1-125">&lt;&gt;PolicyDefinitions forte</span><span class="sxs-lookup"><span data-stu-id="47cc1-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="47cc1-126">**Archivio centrale di dominio:** Per abilitare la configurazione delle impostazioni dei criteri di gruppo da un amministratore di criteri di gruppo da qualsiasi computer del dominio, copiare i file nelle posizioni seguenti del controller di dominio:</span><span class="sxs-lookup"><span data-stu-id="47cc1-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="47cc1-127">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="47cc1-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="47cc1-128">Percorso del file</span><span class="sxs-lookup"><span data-stu-id="47cc1-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="47cc1-129">Modello di criteri di gruppo (con estensione ADMX)</span><span class="sxs-lookup"><span data-stu-id="47cc1-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="47cc1-130">&lt;&gt;sysvol\domain\policies\PolicyDefinitions forte</span><span class="sxs-lookup"><span data-stu-id="47cc1-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="47cc1-131">File di lingua dei criteri di gruppo (con estensione adml)</span><span class="sxs-lookup"><span data-stu-id="47cc1-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="47cc1-132">&lt;Strong &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="47cc1-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="47cc1-133">Ad esempio, il file specifico della lingua ADML in inglese USA verrà archiviato in%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span><span class="sxs-lookup"><span data-stu-id="47cc1-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="47cc1-134">Modificare le impostazioni dei criteri di gruppo usando la console Gestione criteri di gruppo o Advanced Group Policy Management per configurare le impostazioni dei criteri di gruppo per la tecnologia MDOP.</span><span class="sxs-lookup"><span data-stu-id="47cc1-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="47cc1-135">Criteri di gruppo di MDOP per tecnologia</span><span class="sxs-lookup"><span data-stu-id="47cc1-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="47cc1-136">Per altre informazioni sui criteri di gruppo di MDOP supportati, vedere la documentazione specifica relativa alla tecnologia.</span><span class="sxs-lookup"><span data-stu-id="47cc1-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47cc1-137">Tecnologia MDOP</span><span class="sxs-lookup"><span data-stu-id="47cc1-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="47cc1-138">Bundle di versioni</span><span class="sxs-lookup"><span data-stu-id="47cc1-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="47cc1-139">Note</span><span class="sxs-lookup"><span data-stu-id="47cc1-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="47cc1-140">Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="47cc1-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47cc1-141">App-V 5,0 e App-V 5,0 Service Pack</span><span class="sxs-lookup"><span data-stu-id="47cc1-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="47cc1-142">Come modificare la configurazione del client App-V 5.0 usando il modello ADMX e Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="47cc1-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="47cc1-143">User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="47cc1-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47cc1-144">UE-V 2,0 e UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="47cc1-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="47cc1-145">Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="47cc1-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="47cc1-146">UE-V 1,0 incluso 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="47cc1-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="47cc1-147">Configurazione di UE-V con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="47cc1-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="47cc1-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span><span class="sxs-lookup"><span data-stu-id="47cc1-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47cc1-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="47cc1-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="47cc1-150">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="47cc1-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="47cc1-151">MBAM 2,0 incluso 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="47cc1-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="47cc1-152">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47cc1-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="47cc1-153">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="47cc1-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="47cc1-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="47cc1-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="47cc1-155">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="47cc1-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





