---
title: Configurazioni supportate di App-V 5.1
description: Configurazioni supportate di App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805943"
---
# <span data-ttu-id="afde1-103">Configurazioni supportate di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="afde1-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="afde1-104">Si applica a: Windows 10, versione 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (aggiornamento della sicurezza esteso)</span><span class="sxs-lookup"><span data-stu-id="afde1-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="afde1-105">Questo argomento specifica i requisiti per installare ed eseguire Microsoft Application Virtualization (App-V) 5,1 nell'ambiente in uso.</span><span class="sxs-lookup"><span data-stu-id="afde1-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="afde1-106">Requisiti di sistema di App-V Server</span><span class="sxs-lookup"><span data-stu-id="afde1-106">App-V Server system requirements</span></span>

<span data-ttu-id="afde1-107">Questa sezione elenca i requisiti hardware e del sistema operativo per tutti i componenti di App-V Server.</span><span class="sxs-lookup"><span data-stu-id="afde1-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="afde1-108">Scenari server App-V 5,1 non supportati</span><span class="sxs-lookup"><span data-stu-id="afde1-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="afde1-109">Il server App-V 5,1 non supporta gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="afde1-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="afde1-110">Distribuzione in un computer che esegue Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="afde1-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="afde1-111">Distribuzione in un computer in cui è in esecuzione una versione precedente di componenti server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="afde1-112">È possibile installare l'App-V 5,1 affiancata al solo server App-V 4.5 Lightweight streaming server (garanzia).</span><span class="sxs-lookup"><span data-stu-id="afde1-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="afde1-113">La distribuzione di App-V affiancata al server HWS (Application Virtualization Management Service) App-V 4,5 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="afde1-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="afde1-114">Distribuzione in un computer che esegue Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="afde1-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="afde1-115">Distribuzione a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="afde1-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="afde1-116">Percorsi brevi.</span><span class="sxs-lookup"><span data-stu-id="afde1-116">Short paths.</span></span> <span data-ttu-id="afde1-117">Se si prevede di usare un breve percorso, è necessario creare un nuovo volume.</span><span class="sxs-lookup"><span data-stu-id="afde1-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="afde1-118">Requisiti del sistema operativo del server di gestione</span><span class="sxs-lookup"><span data-stu-id="afde1-118">Management server operating system requirements</span></span>

<span data-ttu-id="afde1-119">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di gestione App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="afde1-120">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="afde1-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="afde1-121">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="afde1-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="afde1-122">Per altre informazioni, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft</span><span class="sxs-lookup"><span data-stu-id="afde1-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="afde1-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-123">Operating System</span></span>                 | <span data-ttu-id="afde1-124">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-124">Service Pack</span></span> | <span data-ttu-id="afde1-125">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="afde1-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="afde1-127">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-127">64-bit</span></span>       |
| <span data-ttu-id="afde1-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="afde1-129">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-129">64-bit</span></span>       |
| <span data-ttu-id="afde1-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="afde1-131">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-131">64-bit</span></span>       |
| <span data-ttu-id="afde1-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="afde1-133">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-133">64-bit</span></span>       |
| <span data-ttu-id="afde1-134">[Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="afde1-135">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-135">SP1</span></span>     |        <span data-ttu-id="afde1-136">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-136">64-bit</span></span>       |
 

<span data-ttu-id="afde1-137">**Importante**  La distribuzione del ruolo del server di gestione in un computer con funzionalità RDS (Remote Desktop Sharing) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="afde1-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="afde1-138">Requisiti hardware del server di gestione</span><span class="sxs-lookup"><span data-stu-id="afde1-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="afde1-139">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="afde1-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="afde1-140">RAM — 1 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="afde1-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="afde1-141">Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto</span><span class="sxs-lookup"><span data-stu-id="afde1-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="afde1-142">Requisiti per il database del server di gestione</span><span class="sxs-lookup"><span data-stu-id="afde1-142">Management server database requirements</span></span>

<span data-ttu-id="afde1-143">Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione di database di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="afde1-144">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="afde1-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="afde1-145">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="afde1-146">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="afde1-148">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="afde1-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="afde1-150">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-151">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-152">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-153">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="afde1-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-155">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-156">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-158">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-159">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-161">SP3</span><span class="sxs-lookup"><span data-stu-id="afde1-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-162">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afde1-163">Per altre informazioni sui file di configurazione degli utenti con SQL Server 2016 o versione successiva, vedere l' [articolo del supporto](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="afde1-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="afde1-164">Requisiti del sistema operativo di Publishing Server</span><span class="sxs-lookup"><span data-stu-id="afde1-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="afde1-165">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di pubblicazione App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="afde1-166">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-166">Operating System</span></span>                 | <span data-ttu-id="afde1-167">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-167">Service Pack</span></span> | <span data-ttu-id="afde1-168">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="afde1-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="afde1-170">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-170">64-bit</span></span>       |
| <span data-ttu-id="afde1-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="afde1-172">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-172">64-bit</span></span>       |
| <span data-ttu-id="afde1-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="afde1-174">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-174">64-bit</span></span>       |
| <span data-ttu-id="afde1-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="afde1-176">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-176">64-bit</span></span>       |
| <span data-ttu-id="afde1-177">[Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="afde1-178">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-178">SP1</span></span>     |        <span data-ttu-id="afde1-179">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="afde1-180">Requisiti hardware del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="afde1-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="afde1-181">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="afde1-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="afde1-182">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="afde1-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="afde1-183">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="afde1-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="afde1-184">Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto</span><span class="sxs-lookup"><span data-stu-id="afde1-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="afde1-185">Requisiti del sistema operativo per Reporting Server</span><span class="sxs-lookup"><span data-stu-id="afde1-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="afde1-186">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di report App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="afde1-187">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-187">Operating System</span></span>                 | <span data-ttu-id="afde1-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-188">Service Pack</span></span> | <span data-ttu-id="afde1-189">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="afde1-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="afde1-191">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-191">64-bit</span></span>       |
| <span data-ttu-id="afde1-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="afde1-193">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-193">64-bit</span></span>       |
| <span data-ttu-id="afde1-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="afde1-195">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-195">64-bit</span></span>       |
| <span data-ttu-id="afde1-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="afde1-197">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-197">64-bit</span></span>       |
| <span data-ttu-id="afde1-198">[Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="afde1-199">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-199">SP1</span></span>     |        <span data-ttu-id="afde1-200">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="afde1-201">Requisiti hardware del server di Reporting</span><span class="sxs-lookup"><span data-stu-id="afde1-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="afde1-202">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="afde1-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="afde1-203">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="afde1-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="afde1-204">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="afde1-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="afde1-205">Spazio su disco: 200 MB di spazio disponibile su disco rigido</span><span class="sxs-lookup"><span data-stu-id="afde1-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="afde1-206">Requisiti del database del server di report</span><span class="sxs-lookup"><span data-stu-id="afde1-206">Reporting server database requirements</span></span>

<span data-ttu-id="afde1-207">Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione del database di report App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="afde1-208">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="afde1-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="afde1-209">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="afde1-210">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="afde1-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="afde1-212">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-213">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-214">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-215">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="afde1-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-217">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-218">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-220">SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-221">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-223">SP3</span><span class="sxs-lookup"><span data-stu-id="afde1-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-224">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="afde1-225">Requisiti di sistema client App-V</span><span class="sxs-lookup"><span data-stu-id="afde1-225">App-V client system requirements</span></span>

<span data-ttu-id="afde1-226">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="afde1-227">Con il rilascio di Windows 10 Anniversary (aka versione 1607), il client App-V è in-box e blocca l'installazione di qualsiasi versione precedente del client App-V</span><span class="sxs-lookup"><span data-stu-id="afde1-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="afde1-228">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="afde1-229">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="afde1-230">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-231">Microsoft Windows10 (versione precedente a 1607)</span><span class="sxs-lookup"><span data-stu-id="afde1-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="afde1-232">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="afde1-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="afde1-234">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-235">Windows7</span><span class="sxs-lookup"><span data-stu-id="afde1-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-236">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-237">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="afde1-238">Gli scenari di installazione client App-V seguenti non sono supportati, ad eccezione di quanto indicato:</span><span class="sxs-lookup"><span data-stu-id="afde1-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="afde1-239">Computer che eseguono Windows Server</span><span class="sxs-lookup"><span data-stu-id="afde1-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="afde1-240">Computer che eseguono App-V 4.6 SP1 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="afde1-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="afde1-241">Il client Servizi Desktop remoto di App-V 5,1 è supportato solo per i server abilitati per RDS</span><span class="sxs-lookup"><span data-stu-id="afde1-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="afde1-242">Requisiti hardware client App-V</span><span class="sxs-lookup"><span data-stu-id="afde1-242">App-V client hardware requirements</span></span>

<span data-ttu-id="afde1-243">Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="afde1-244">Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="afde1-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="afde1-245">RAM — 1 GB (32 bit) o 2 GB (64 bit)</span><span class="sxs-lookup"><span data-stu-id="afde1-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="afde1-246">Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="afde1-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="afde1-247">Requisiti di sistema client di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="afde1-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="afde1-248">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione client RDS (Remote Desktop Services) di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="afde1-249">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-249">Operating System</span></span>                 | <span data-ttu-id="afde1-250">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-250">Service Pack</span></span> | <span data-ttu-id="afde1-251">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="afde1-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="afde1-253">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-253">64-bit</span></span>       |
| <span data-ttu-id="afde1-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="afde1-255">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-255">64-bit</span></span>       |
| <span data-ttu-id="afde1-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="afde1-257">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-257">64-bit</span></span>       |
| <span data-ttu-id="afde1-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="afde1-259">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-259">64-bit</span></span>       |
| <span data-ttu-id="afde1-260">[Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="afde1-261">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-261">SP1</span></span>     |        <span data-ttu-id="afde1-262">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-262">64-bit</span></span>       |

### <span data-ttu-id="afde1-263">Requisiti hardware client di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="afde1-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="afde1-264">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="afde1-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="afde1-265">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="afde1-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="afde1-266">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="afde1-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="afde1-267">Spazio su disco: 200 MB di spazio disponibile su disco rigido</span><span class="sxs-lookup"><span data-stu-id="afde1-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="afde1-268">Requisiti di sistema sequencer</span><span class="sxs-lookup"><span data-stu-id="afde1-268">Sequencer system requirements</span></span>

<span data-ttu-id="afde1-269">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione di sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="afde1-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="afde1-270">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="afde1-270">Operating System</span></span>                 | <span data-ttu-id="afde1-271">Service Pack</span><span class="sxs-lookup"><span data-stu-id="afde1-271">Service Pack</span></span> | <span data-ttu-id="afde1-272">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="afde1-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="afde1-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="afde1-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="afde1-274">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-274">64-bit</span></span>       |
| <span data-ttu-id="afde1-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afde1-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="afde1-276">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-276">64-bit</span></span>       |
| <span data-ttu-id="afde1-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="afde1-278">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-278">64-bit</span></span>       |
| <span data-ttu-id="afde1-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afde1-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="afde1-280">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-280">64-bit</span></span>       |
| <span data-ttu-id="afde1-281">[Aggiornamento della sicurezza estesa](https://www.microsoft.com/windows-server/extended-security-updates) di Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afde1-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="afde1-282">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-282">SP1</span></span>     |        <span data-ttu-id="afde1-283">64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-283">64-bit</span></span>       |
| <span data-ttu-id="afde1-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="afde1-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="afde1-285">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="afde1-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="afde1-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="afde1-287">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="afde1-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="afde1-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="afde1-289">SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-289">SP1</span></span>     | <span data-ttu-id="afde1-290">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="afde1-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="afde1-291">Requisiti hardware sequencer</span><span class="sxs-lookup"><span data-stu-id="afde1-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="afde1-292">Vedere la documentazione di Windows o Windows Server per i requisiti hardware.</span><span class="sxs-lookup"><span data-stu-id="afde1-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="afde1-293">App-V non aggiunge requisiti hardware aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="afde1-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="afde1-294">Versioni supportate di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="afde1-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="afde1-295">Il client App-V supporta le versioni seguenti di System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="afde1-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="afde1-296">ConfigurationManager di MicrosoftSystemCenter2012</span><span class="sxs-lookup"><span data-stu-id="afde1-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="afde1-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="afde1-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="afde1-298">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="afde1-299">La matrice di versioni di App-V e System Center Configuration Manager seguente mostra tutte le combinazioni supportate ufficialmente da App-V e Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="afde1-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="afde1-300">Sia App-V 4,5 che 4,6 hanno terminato il supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="afde1-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="afde1-301">Versione App-V</span><span class="sxs-lookup"><span data-stu-id="afde1-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="afde1-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="afde1-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="afde1-303">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="afde1-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="afde1-304">System Center Configuration Manager 2012 SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="afde1-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="afde1-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="afde1-306">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="afde1-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="afde1-307">System Center Configuration Manager 2012 SP2</span><span class="sxs-lookup"><span data-stu-id="afde1-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="afde1-308">System Center Configuration Manager versione 1511</span><span class="sxs-lookup"><span data-stu-id="afde1-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="afde1-309">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="afde1-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-310">MSI-solo wrapper</span><span class="sxs-lookup"><span data-stu-id="afde1-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-311">No</span><span class="sxs-lookup"><span data-stu-id="afde1-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="afde1-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="afde1-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-314">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-315">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-316">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="afde1-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="afde1-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-318">MSI-solo wrapper</span><span class="sxs-lookup"><span data-stu-id="afde1-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-319">No</span><span class="sxs-lookup"><span data-stu-id="afde1-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="afde1-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="afde1-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-322">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-323">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="afde1-324">Sì</span><span class="sxs-lookup"><span data-stu-id="afde1-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="afde1-325">Per altre informazioni su come si integra Configuration Manager con App-V, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="afde1-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="afde1-326">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afde1-326">Related topics</span></span>

[<span data-ttu-id="afde1-327">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="afde1-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="afde1-328">Prerequisiti di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="afde1-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
