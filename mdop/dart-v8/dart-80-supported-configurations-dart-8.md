---
title: Configurazioni supportate di DaRT 8.0
description: Configurazioni supportate di DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823926"
---
# <span data-ttu-id="bf03e-103">Configurazioni supportate di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="bf03e-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="bf03e-104">Questo argomento specifica il software prerequisito e i requisiti di configurazione supportati necessari per installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="bf03e-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="bf03e-105">Vengono specificati sia i requisiti del sistema operativo che i requisiti di sistema necessari per eseguire il comando DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="bf03e-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="bf03e-106">Per informazioni sui prerequisiti che è necessario prendere in considerazione per creare l'immagine di ripristino delle freccette, vedere [pianificazione per creare l'immagine di ripristino di dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="bf03e-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="bf03e-107">Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.</span><span class="sxs-lookup"><span data-stu-id="bf03e-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="bf03e-108">Puoi installare DaRT in uno dei due modi.</span><span class="sxs-lookup"><span data-stu-id="bf03e-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="bf03e-109">È possibile installare tutte le funzionalità in un computer dell'amministratore IT, in cui verranno eseguite tutte le attività associate al dardo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bf03e-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="bf03e-110">In alternativa, è possibile installare, nel computer amministratore, solo la funzionalità DaRT che crea l'immagine di ripristino e quindi installare la funzionalità usata per eseguire il comando DaRT (ovvero il Visualizzatore di connessioni remote DaRT) in un computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="bf03e-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="bf03e-111">Software prerequisiti di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="bf03e-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="bf03e-112">Verificare che siano soddisfatti i prerequisiti seguenti prima di installare dardo.</span><span class="sxs-lookup"><span data-stu-id="bf03e-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="bf03e-113">Prerequisiti computer amministratore</span><span class="sxs-lookup"><span data-stu-id="bf03e-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="bf03e-114">La tabella seguente elenca i prerequisiti di installazione per il computer dell'amministratore durante l'installazione di DaRT 8,0 e di tutti gli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="bf03e-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf03e-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="bf03e-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="bf03e-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="bf03e-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf03e-117">Windows Assessment and Development Kit (ADK)</span><span class="sxs-lookup"><span data-stu-id="bf03e-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-118">Obbligatorio per la creazione guidata immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="bf03e-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="bf03e-119">Contiene gli strumenti di distribuzione, che vengono usati per personalizzare, distribuire e servire immagini di Windows e contiene l'ambiente di preinstallazione di Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="bf03e-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="bf03e-120">ADK non è obbligatorio se si sta installando solo il Visualizzatore di connessioni remote e/o l'analizzatore di crash.</span><span class="sxs-lookup"><span data-stu-id="bf03e-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf03e-121">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="bf03e-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-122">Richiesto dalla creazione guidata immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="bf03e-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf03e-123">Windows Development Kit o Software Development Kit (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="bf03e-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-124">Analizzatore crash richiede gli strumenti di debug di Windows 8 da Windows Driver Kit per analizzare i file di dump della memoria.</span><span class="sxs-lookup"><span data-stu-id="bf03e-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf03e-125">Immagine ISO di Windows 8 64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-126">Dardo richiede l'ambiente Windows Recovery Environment (Windows RE) da Windows 8 Media.</span><span class="sxs-lookup"><span data-stu-id="bf03e-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="bf03e-127">Scaricare la versione a 32 bit o a 64 bit di Windows 8, a seconda del tipo di immagine di recupero DaRT che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="bf03e-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="bf03e-128">Se si supportano entrambi i tipi di sistema nell'ambiente, scaricare entrambe le versioni di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf03e-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="bf03e-129">Prerequisiti del computer help desk</span><span class="sxs-lookup"><span data-stu-id="bf03e-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="bf03e-130">La tabella seguente elenca i prerequisiti di installazione per il computer dell'help desk quando si esegue il Visualizzatore di connessioni remote di DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="bf03e-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf03e-131">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="bf03e-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="bf03e-132">Dettagli</span><span class="sxs-lookup"><span data-stu-id="bf03e-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf03e-133">Visualizzatore connessione remota di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="bf03e-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-134">Deve essere installato in un sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf03e-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf03e-135">NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="bf03e-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-136">Richiesto dalla creazione guidata immagine di ripristino di freccette</span><span class="sxs-lookup"><span data-stu-id="bf03e-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf03e-137">Strumenti di debug per Windows</span><span class="sxs-lookup"><span data-stu-id="bf03e-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf03e-138">Obbligatorio solo se si sta installando lo strumento Analizzatore crash</span><span class="sxs-lookup"><span data-stu-id="bf03e-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="bf03e-139">Prerequisiti per i computer degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="bf03e-139">End-user computer prerequisites</span></span>

<span data-ttu-id="bf03e-140">Non esiste alcun software prerequisito che deve essere installato nei computer degli utenti finali, ad eccezione del sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf03e-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="bf03e-141">Requisiti del sistema operativo DaRT</span><span class="sxs-lookup"><span data-stu-id="bf03e-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="bf03e-142">Requisiti di sistema del computer amministratore</span><span class="sxs-lookup"><span data-stu-id="bf03e-142">Administrator computer system requirements</span></span>

<span data-ttu-id="bf03e-143">La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer dell'amministratore DaRT.</span><span class="sxs-lookup"><span data-stu-id="bf03e-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="bf03e-144">**Nota**  Assicurarsi di allocare spazio sufficiente per gli eventuali strumenti aggiuntivi che si desidera installare nel computer dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="bf03e-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="bf03e-145">**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="bf03e-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="bf03e-146">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="bf03e-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="bf03e-147">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bf03e-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf03e-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="bf03e-149">Edizione</span><span class="sxs-lookup"><span data-stu-id="bf03e-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="bf03e-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="bf03e-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="bf03e-151">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="bf03e-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="bf03e-152">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="bf03e-153">Requisito RAM per l'uso di freccette</span><span class="sxs-lookup"><span data-stu-id="bf03e-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="bf03e-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-155">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-156">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-157">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-158">2 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-159">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf03e-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="bf03e-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-161">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-162">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-163">32 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-164">1 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-165">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf03e-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-167">Standard, Enterprise, Data Center</span><span class="sxs-lookup"><span data-stu-id="bf03e-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-168">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-169">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-170">512 MB</span><span class="sxs-lookup"><span data-stu-id="bf03e-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-171">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="bf03e-172">Requisiti di sistema del computer help desk DaRT</span><span class="sxs-lookup"><span data-stu-id="bf03e-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="bf03e-173">Se si consente a un help desk di risolvere in modo remoto i computer, è necessario che il Visualizzatore di connessione remota sia installato nel computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="bf03e-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="bf03e-174">È possibile installare facoltativamente lo strumento Analizzatore crash nel computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="bf03e-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="bf03e-175">DaRT 8,0 consente a un lavoratore dell'help desk di connettersi a un computer DaRT 8,0 usando il Visualizzatore di connessione remota Dart 7,0 o DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="bf03e-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="bf03e-176">Il Visualizzatore di connessioni remote di DaRT 7,0 richiede un sistema operativo Windows 7, mentre il Visualizzatore di connessione remota DaRT 8,0 richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf03e-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="bf03e-177">Il Visualizzatore di connessione remota DaRT 8,0 e tutti gli altri strumenti DaRT 8,0 possono essere installati solo in un computer che utilizza Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf03e-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="bf03e-178">La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer help desk DaRT.</span><span class="sxs-lookup"><span data-stu-id="bf03e-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf03e-179">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="bf03e-180">Edizione</span><span class="sxs-lookup"><span data-stu-id="bf03e-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="bf03e-181">Service Pack</span><span class="sxs-lookup"><span data-stu-id="bf03e-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="bf03e-182">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="bf03e-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="bf03e-183">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="bf03e-184">Requisiti di RAM per l'uso di freccette</span><span class="sxs-lookup"><span data-stu-id="bf03e-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="bf03e-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-186">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-187">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-188">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-189">2 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-190">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf03e-191">Windows8 (solo con il Visualizzatore di connessione remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="bf03e-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-192">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-193">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-194">32 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-195">1 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-196">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-197">Windows 7 (solo con il Visualizzatore di connessione remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="bf03e-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-198">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="bf03e-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-200">64 bit o 32 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-201">1 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-202">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf03e-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf03e-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-204">Standard, Enterprise, Data Center</span><span class="sxs-lookup"><span data-stu-id="bf03e-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-205">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-206">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-207">51</span><span class="sxs-lookup"><span data-stu-id="bf03e-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-208">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bf03e-209">DaRT offre anche i requisiti hardware minimi seguenti per il computer dell'utente finale:</span><span class="sxs-lookup"><span data-stu-id="bf03e-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="bf03e-210">Un'unità CD o DVD o una porta USB, necessaria solo se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="bf03e-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="bf03e-211">Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bf03e-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="bf03e-212">Requisiti di sistema di computer per gli utenti finali di DaRT</span><span class="sxs-lookup"><span data-stu-id="bf03e-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="bf03e-213">La finestra del set di strumenti di diagnostica e ripristino in DaRT richiede che il computer dell'utente finale usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DaRT:</span><span class="sxs-lookup"><span data-stu-id="bf03e-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf03e-214">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="bf03e-215">Edizione</span><span class="sxs-lookup"><span data-stu-id="bf03e-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="bf03e-216">Service Pack</span><span class="sxs-lookup"><span data-stu-id="bf03e-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="bf03e-217">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="bf03e-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="bf03e-218">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bf03e-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="bf03e-219">Requisiti di RAM</span><span class="sxs-lookup"><span data-stu-id="bf03e-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="bf03e-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-221">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-222">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-223">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-224">2 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-225">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf03e-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="bf03e-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-227">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="bf03e-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-228">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-229">32 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-230">1 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-231">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf03e-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf03e-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-233">Standard, Enterprise, Data Center</span><span class="sxs-lookup"><span data-stu-id="bf03e-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-234">N/D</span><span class="sxs-lookup"><span data-stu-id="bf03e-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-235">64 bit</span><span class="sxs-lookup"><span data-stu-id="bf03e-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-236">512 MB</span><span class="sxs-lookup"><span data-stu-id="bf03e-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf03e-237">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="bf03e-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bf03e-238">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf03e-238">Related topics</span></span>


[<span data-ttu-id="bf03e-239">Pianificazione della distribuzione di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="bf03e-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





