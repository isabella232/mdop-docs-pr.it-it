---
title: Configurazioni supportate di DaRT 10
description: Configurazioni supportate di DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804750"
---
# <span data-ttu-id="9e280-103">Configurazioni supportate di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="9e280-104">Questo argomento specifica il software prerequisito e i requisiti di configurazione supportati necessari per installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 10 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="9e280-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="9e280-105">Sono specificati sia i requisiti del sistema operativo che i requisiti di sistema necessari per eseguire il dardo 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="9e280-106">Per informazioni sui prerequisiti che è necessario prendere in considerazione per creare l'immagine di ripristino delle freccette, vedere [pianificazione per creare l'immagine di ripristino di Dart 10](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="9e280-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="9e280-107">Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.</span><span class="sxs-lookup"><span data-stu-id="9e280-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="9e280-108">Puoi installare DaRT in uno dei due modi.</span><span class="sxs-lookup"><span data-stu-id="9e280-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="9e280-109">È possibile installare tutte le funzionalità in un computer dell'amministratore IT, in cui verranno eseguite tutte le attività associate al dardo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e280-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="9e280-110">In alternativa, è possibile installare, nel computer amministratore, solo la funzionalità DaRT che crea l'immagine di ripristino e quindi installare la funzionalità usata per eseguire il comando DaRT (ovvero il Visualizzatore di connessioni remote DaRT) in un computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="9e280-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="9e280-111">Software prerequisiti di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="9e280-112">Verificare che siano soddisfatti i prerequisiti seguenti prima di installare dardo.</span><span class="sxs-lookup"><span data-stu-id="9e280-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="9e280-113">Prerequisiti computer amministratore</span><span class="sxs-lookup"><span data-stu-id="9e280-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="9e280-114">La tabella seguente elenca i prerequisiti di installazione per il computer dell'amministratore durante l'installazione di DaRT 10 e tutti gli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="9e280-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e280-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9e280-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="9e280-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="9e280-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e280-117">Windows Assessment and Development Kit (ADK)</span><span class="sxs-lookup"><span data-stu-id="9e280-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e280-118">Obbligatorio per la creazione guidata immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="9e280-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="9e280-119">Contiene gli strumenti di distribuzione, che vengono usati per personalizzare, distribuire e servire immagini di Windows e contiene l'ambiente di preinstallazione di Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="9e280-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="9e280-120">ADK non è obbligatorio se si sta installando solo il Visualizzatore di connessioni remote e/o l'analizzatore di crash.</span><span class="sxs-lookup"><span data-stu-id="9e280-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9e280-121">Windows Development Kit o Software Development Kit (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="9e280-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e280-122">Analizzatore crash richiede gli strumenti di debug di Windows 10 da Windows Driver Kit per analizzare i file di dump della memoria.</span><span class="sxs-lookup"><span data-stu-id="9e280-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e280-123">Immagine ISO di Windows 10 64 bit o 32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e280-124">Dardo richiede l'ambiente Windows Recovery Environment (Windows RE) da Windows 10 Media.</span><span class="sxs-lookup"><span data-stu-id="9e280-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="9e280-125">Scaricare la versione a 32 bit o a 64 bit di Windows 10, a seconda del tipo di immagine di recupero delle freccette che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="9e280-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="9e280-126">Se si supportano entrambi i tipi di sistema nell'ambiente, scaricare entrambe le versioni di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9e280-127">Prerequisiti del computer help desk</span><span class="sxs-lookup"><span data-stu-id="9e280-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="9e280-128">La tabella seguente elenca i prerequisiti di installazione per il computer dell'help desk quando si esegue il Visualizzatore di connessioni remote di DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e280-129">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9e280-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="9e280-130">Dettagli</span><span class="sxs-lookup"><span data-stu-id="9e280-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e280-131">Visualizzatore di connessioni remote di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e280-132">Deve essere installato in un sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9e280-133">Strumenti di debug per Windows</span><span class="sxs-lookup"><span data-stu-id="9e280-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e280-134">Obbligatorio solo se si sta installando lo strumento Analizzatore crash</span><span class="sxs-lookup"><span data-stu-id="9e280-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9e280-135">Prerequisiti per i computer degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="9e280-135">End-user computer prerequisites</span></span>

<span data-ttu-id="9e280-136">Non esiste alcun software prerequisito che deve essere installato nei computer degli utenti finali, ad eccezione del sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="9e280-137">Requisiti del sistema operativo DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="9e280-138">Requisiti di sistema del computer amministratore</span><span class="sxs-lookup"><span data-stu-id="9e280-138">Administrator computer system requirements</span></span>

<span data-ttu-id="9e280-139">La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer dell'amministratore di DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="9e280-140">**Nota**  Assicurarsi di allocare spazio sufficiente per gli eventuali strumenti aggiuntivi che si desidera installare nel computer dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="9e280-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="9e280-141">**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="9e280-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="9e280-142">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="9e280-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="9e280-143">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e280-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="9e280-144">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="9e280-145">Edizione</span><span class="sxs-lookup"><span data-stu-id="9e280-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e280-146">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e280-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="9e280-147">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="9e280-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="9e280-148">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="9e280-149">Requisito RAM per l'uso di freccette</span><span class="sxs-lookup"><span data-stu-id="9e280-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e280-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-151">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-152">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-153">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-154">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-155">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e280-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e280-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-157">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-158">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-159">32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-160">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-161">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="9e280-162">Requisiti di sistema del computer help desk DaRT</span><span class="sxs-lookup"><span data-stu-id="9e280-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="9e280-163">Se si consente a un help desk di risolvere in modo remoto i computer, è necessario che il Visualizzatore di connessione remota sia installato nel computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="9e280-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="9e280-164">È possibile installare facoltativamente lo strumento Analizzatore crash nel computer dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="9e280-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="9e280-165">DaRT 10 consente a un lavoratore dell'help desk di connettersi a un computer con freccette 10 usando il Visualizzatore di connessione remota Dart 7,0, DaRT 8,0, DaRt 8,1 o il visore remoto di DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="9e280-166">Il dardo 7,0, il dardo 8,0 e il dardo 8,1, i visualizzatori di connessione remota richiedono rispettivamente i sistemi operativi Windows 7, Windows 8 o Windows 8,1, mentre il Visualizzatore di connessioni remote DaRT 10 richiede Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="9e280-167">Il Visualizzatore di connessione remota DaRT 10 e tutti gli altri strumenti DaRT 10 possono essere installati solo in un computer con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9e280-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="9e280-168">La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer help desk DaRT.</span><span class="sxs-lookup"><span data-stu-id="9e280-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="9e280-169">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="9e280-170">Edizione</span><span class="sxs-lookup"><span data-stu-id="9e280-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e280-171">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e280-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="9e280-172">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="9e280-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="9e280-173">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="9e280-174">Requisiti di RAM per l'uso di freccette</span><span class="sxs-lookup"><span data-stu-id="9e280-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e280-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-176">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-177">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-178">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-179">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e280-181">Windows10 (solo con il Visualizzatore di connessione remota 10,0)</span><span class="sxs-lookup"><span data-stu-id="9e280-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-182">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-183">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-184">32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-185">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-186">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="9e280-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-188">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-189">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-190">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-191">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-192">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e280-193">Windows8 (solo con il Visualizzatore di connessione remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="9e280-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-194">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-195">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-196">32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-197">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-198">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-199">Windows 7 (solo con il Visualizzatore di connessione remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="9e280-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-200">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="9e280-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-202">64 bit o 32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-203">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-204">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e280-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e280-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-206">Standard, Enterprise, Data Center</span><span class="sxs-lookup"><span data-stu-id="9e280-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-207">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-208">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-209">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-210">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-211">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e280-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-212">Standard, Enterprise, Data Center</span><span class="sxs-lookup"><span data-stu-id="9e280-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-213">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-214">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-215">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-216">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9e280-217">DaRT offre anche i requisiti hardware minimi seguenti per il computer dell'utente finale:</span><span class="sxs-lookup"><span data-stu-id="9e280-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="9e280-218">Un'unità CD o DVD o una porta USB, necessaria solo se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="9e280-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="9e280-219">Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9e280-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="9e280-220">Requisiti di sistema di computer per gli utenti finali DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="9e280-221">La finestra del set di strumenti di diagnostica e ripristino in DaRT 10 richiede che il computer dell'utente finale usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DaRT:</span><span class="sxs-lookup"><span data-stu-id="9e280-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="9e280-222">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="9e280-223">Edizione</span><span class="sxs-lookup"><span data-stu-id="9e280-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e280-224">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e280-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="9e280-225">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="9e280-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="9e280-226">Requisiti del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e280-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="9e280-227">Requisiti di RAM</span><span class="sxs-lookup"><span data-stu-id="9e280-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e280-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e280-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-229">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-230">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-231">64 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-233">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e280-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e280-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-235">Tutte le edizioni</span><span class="sxs-lookup"><span data-stu-id="9e280-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-236">N/D</span><span class="sxs-lookup"><span data-stu-id="9e280-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-237">32 bit</span><span class="sxs-lookup"><span data-stu-id="9e280-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-238">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e280-239">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="9e280-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9e280-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e280-240">Related topics</span></span>


[<span data-ttu-id="9e280-241">Pianificazione della distribuzione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="9e280-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





