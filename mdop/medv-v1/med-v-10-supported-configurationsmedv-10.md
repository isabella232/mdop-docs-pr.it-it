---
title: Configurazioni supportate di MED-V 1.0
description: Configurazioni supportate di MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804354"
---
# <span data-ttu-id="d6833-103">Configurazioni supportate di MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d6833-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="d6833-104">Questo argomento specifica i requisiti necessari per installare ed eseguire Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 nell'ambiente in uso.</span><span class="sxs-lookup"><span data-stu-id="d6833-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="d6833-105">Requisiti di sistema client di MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="d6833-106">Requisiti del sistema operativo client MED-V</span><span class="sxs-lookup"><span data-stu-id="d6833-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="d6833-107">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="d6833-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6833-108">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d6833-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d6833-109">Edizione</span><span class="sxs-lookup"><span data-stu-id="d6833-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="d6833-110">Service Pack</span><span class="sxs-lookup"><span data-stu-id="d6833-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d6833-111">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="d6833-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6833-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6833-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-113">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="d6833-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-114">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="d6833-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-115">x86</span><span class="sxs-lookup"><span data-stu-id="d6833-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6833-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6833-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-117">Business, Enterprise o Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="d6833-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-118">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="d6833-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-119">x86</span><span class="sxs-lookup"><span data-stu-id="d6833-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d6833-120">Nota</span><span class="sxs-lookup"><span data-stu-id="d6833-120">Note</span></span>**  
<span data-ttu-id="d6833-121">Il client MED-V non viene eseguito in modalità x64 nativa.</span><span class="sxs-lookup"><span data-stu-id="d6833-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="d6833-122">Invece, MED-V viene eseguito in Windows in modalità Windows 64 bit (WOW64) in computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d6833-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="d6833-123">Configurazione client di MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="d6833-124">Versione di .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d6833-124">.NET Framework Version</span></span>**

<span data-ttu-id="d6833-125">Le versioni seguenti di Microsoft .NET Framework sono supportate per l'installazione del client MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="d6833-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="d6833-126">.NET Framework 2,0 o .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="d6833-127">.NET Framework 3,0 o .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="d6833-128">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="d6833-129">Motore di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="d6833-129">Virtualization Engine</span></span>**

<span data-ttu-id="d6833-130">Microsoft Virtual PC 2007 SP1 con l'hotfix descritto nell'articolo della Microsoft Knowledge base 974918 è supportato per l'installazione del client di MED-V 1,0 nelle configurazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6833-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="d6833-131">File del disco rigido virtuale statico (VHD)</span><span class="sxs-lookup"><span data-stu-id="d6833-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="d6833-132">Più file VHD che si trovano all'interno della stessa directory</span><span class="sxs-lookup"><span data-stu-id="d6833-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="d6833-133">File VHD dinamico</span><span class="sxs-lookup"><span data-stu-id="d6833-133">Dynamic VHD file</span></span>

**<span data-ttu-id="d6833-134">Browser Internet</span><span class="sxs-lookup"><span data-stu-id="d6833-134">Internet Browser</span></span>**

<span data-ttu-id="d6833-135">Windows Internet Explorer 7 e Windows Internet Explorer 8 sono supportati per l'installazione del client MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="d6833-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="d6833-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="d6833-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="d6833-137">Il client MED-V non è supportato in un ambiente server Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d6833-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="d6833-138">Requisiti di sistema per l'area di lavoro MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="d6833-139">Requisiti del sistema operativo per l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="d6833-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="d6833-140">Nella tabella seguente sono elencati i sistemi operativi supportati per le aree di lavoro MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="d6833-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6833-141">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d6833-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d6833-142">Edizione</span><span class="sxs-lookup"><span data-stu-id="d6833-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="d6833-143">Service Pack</span><span class="sxs-lookup"><span data-stu-id="d6833-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d6833-144">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="d6833-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6833-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6833-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-146">Professional</span><span class="sxs-lookup"><span data-stu-id="d6833-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-147">SP4</span><span class="sxs-lookup"><span data-stu-id="d6833-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-148">X86</span><span class="sxs-lookup"><span data-stu-id="d6833-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6833-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6833-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-150">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="d6833-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-151">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="d6833-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d6833-152">Nota</span><span class="sxs-lookup"><span data-stu-id="d6833-152">Note</span></span></strong><br/><p><span data-ttu-id="d6833-153">È consigliabile usare SP3 per verificare che l'area di lavoro MED-V sia compatibile con le versioni future di MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6833-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="d6833-154">x86</span><span class="sxs-lookup"><span data-stu-id="d6833-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="d6833-155">Configurazione dell'area di lavoro MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="d6833-156">Versione di .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d6833-156">.NET Framework Version</span></span>**

<span data-ttu-id="d6833-157">MED-V richiede una delle versioni supportate seguenti dell'installazione di Microsoft .NET Framework per l'area di lavoro di MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="d6833-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="d6833-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="d6833-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="d6833-160">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="d6833-161">Nota</span><span class="sxs-lookup"><span data-stu-id="d6833-161">Note</span></span>**  
<span data-ttu-id="d6833-162">È consigliabile .NET Framework 3,5 SP1 per garantire che l'area di lavoro MED-V sia compatibile con le versioni future di MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6833-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="d6833-163">Browser Internet</span><span class="sxs-lookup"><span data-stu-id="d6833-163">Internet Browser</span></span>**

<span data-ttu-id="d6833-164">Windows Internet Explorer 6 SP2 e Windows Internet Explorer 7 sono supportati per l'installazione dell'area di lavoro MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="d6833-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="d6833-165">Immagini dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="d6833-165">MED-V Workspace Images</span></span>

<span data-ttu-id="d6833-166">Le immagini dell'area di lavoro MED-V devono essere create usando Virtual PC 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="d6833-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="d6833-167">Requisiti di sistema server MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="d6833-168">Requisiti del sistema operativo server MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="d6833-169">Nella tabella seguente sono elencati i sistemi operativi supportati per le installazioni del server MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="d6833-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6833-170">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d6833-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="d6833-171">Edizione</span><span class="sxs-lookup"><span data-stu-id="d6833-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="d6833-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="d6833-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d6833-173">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="d6833-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6833-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6833-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-175">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="d6833-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d6833-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-177">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="d6833-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="d6833-178">Configurazione del server MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="d6833-179">Versione di .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d6833-179">.NET Framework Version</span></span>**

<span data-ttu-id="d6833-180">MED-V richiede una delle versioni supportate seguenti dell'installazione di Microsoft .NET Framework per l'area di lavoro di MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="d6833-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="d6833-181">.NET Framework 2,0 o .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="d6833-182">.NET Framework 3,0 o .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="d6833-183">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d6833-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="d6833-184">Versione di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="d6833-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="d6833-185">Le versioni seguenti di Microsoft SQL Server sono supportate per MED-V 1,0 quando SQL Server viene installato localmente o in remoto dal server MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="d6833-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6833-186">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="d6833-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="d6833-187">Edizione</span><span class="sxs-lookup"><span data-stu-id="d6833-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="d6833-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="d6833-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="d6833-189">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="d6833-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6833-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="d6833-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-191">Express, standard o Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="d6833-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-192">SP2</span><span class="sxs-lookup"><span data-stu-id="d6833-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-193">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="d6833-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6833-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6833-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-195">Express, standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="d6833-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-196">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d6833-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6833-197">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="d6833-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="d6833-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="d6833-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="d6833-199">Il server MED-V è supportato in un ambiente server Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d6833-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="d6833-200">Informazioni sulla globalizzazione di MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="d6833-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="d6833-201">Anche se MED-V non viene rilasciato in lingue diverse dall'inglese, sono supportate le seguenti versioni della lingua del sistema operativo Windows per il client, l'area di lavoro e le installazioni del server MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="d6833-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="d6833-202">Inglese</span><span class="sxs-lookup"><span data-stu-id="d6833-202">English</span></span>

-   <span data-ttu-id="d6833-203">Francese</span><span class="sxs-lookup"><span data-stu-id="d6833-203">French</span></span>

-   <span data-ttu-id="d6833-204">Tedesco</span><span class="sxs-lookup"><span data-stu-id="d6833-204">German</span></span>

-   <span data-ttu-id="d6833-205">Italiano</span><span class="sxs-lookup"><span data-stu-id="d6833-205">Italian</span></span>

-   <span data-ttu-id="d6833-206">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="d6833-206">Spanish</span></span>

-   <span data-ttu-id="d6833-207">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="d6833-207">Portuguese (Brazil)</span></span>









