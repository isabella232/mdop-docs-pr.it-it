---
title: Configurazioni supportate da App-V 5.0 SP3
description: Configurazioni supportate da App-V 5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805992"
---
# <span data-ttu-id="16568-103">Configurazioni supportate da App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="16568-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="16568-104">Questo argomento specifica i requisiti per installare ed eseguire Microsoft Application Virtualization (App-V) 5,0 SP3 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="16568-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="16568-105">Requisiti di sistema di App-V Server</span><span class="sxs-lookup"><span data-stu-id="16568-105">App-V Server system requirements</span></span>


<span data-ttu-id="16568-106">Questa sezione elenca i requisiti hardware e del sistema operativo per tutti i componenti di App-V Server.</span><span class="sxs-lookup"><span data-stu-id="16568-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="16568-107">Scenari di Server SP3 App-V 5,0 non supportati</span><span class="sxs-lookup"><span data-stu-id="16568-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="16568-108">Il server App-V 5,0 SP3 non supporta gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="16568-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="16568-109">Distribuzione in un computer che esegue Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="16568-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="16568-110">Distribuzione in un computer che esegue una versione precedente dei componenti del server App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="16568-111">È possibile installare l'App-V 5,0 SP3 affiancata solo al server App-V 4.5 Lightweight streaming server (garanzia).</span><span class="sxs-lookup"><span data-stu-id="16568-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="16568-112">La distribuzione di App-V affiancata al server HWS (Application Virtualization Management Service) App-V 4,5 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="16568-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="16568-113">Distribuzione in un computer che esegue Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="16568-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="16568-114">Distribuzione remota del database del server di gestione o del database di report.</span><span class="sxs-lookup"><span data-stu-id="16568-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="16568-115">È necessario eseguire il programma di installazione direttamente nel computer in cui è in esecuzione Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="16568-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="16568-116">Distribuzione a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="16568-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="16568-117">Percorsi brevi.</span><span class="sxs-lookup"><span data-stu-id="16568-117">Short paths.</span></span> <span data-ttu-id="16568-118">Se si prevede di usare un breve percorso, è necessario creare un nuovo volume.</span><span class="sxs-lookup"><span data-stu-id="16568-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="16568-119">Requisiti del sistema operativo del server di gestione</span><span class="sxs-lookup"><span data-stu-id="16568-119">Management server operating system requirements</span></span>

<span data-ttu-id="16568-120">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di gestione di App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="16568-121">**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="16568-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="16568-122">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="16568-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="16568-123">Per altre informazioni, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976) di supporto del ciclo di vita del supporto Microsoft</span><span class="sxs-lookup"><span data-stu-id="16568-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-124">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-125">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="16568-126">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16568-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-128">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-130">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-132">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-133">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16568-134">**Importante**  La distribuzione del ruolo del server di gestione in un computer con funzionalità RDS (Remote Desktop Sharing) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="16568-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="16568-135">Requisiti hardware del server di gestione</span><span class="sxs-lookup"><span data-stu-id="16568-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="16568-136">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="16568-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="16568-137">RAM — 1 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="16568-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="16568-138">Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto</span><span class="sxs-lookup"><span data-stu-id="16568-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="16568-139">Requisiti per il database del server di gestione</span><span class="sxs-lookup"><span data-stu-id="16568-139">Management server database requirements</span></span>

<span data-ttu-id="16568-140">Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione di database di gestione di App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-141">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="16568-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="16568-142">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="16568-143">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="16568-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-145">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-147">SP2</span><span class="sxs-lookup"><span data-stu-id="16568-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-148">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-150">SP3</span><span class="sxs-lookup"><span data-stu-id="16568-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-151">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="16568-152">Requisiti del sistema operativo di Publishing Server</span><span class="sxs-lookup"><span data-stu-id="16568-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="16568-153">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di pubblicazione App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-154">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-155">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="16568-156">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16568-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-158">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-160">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-162">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-163">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="16568-164">Requisiti hardware del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="16568-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="16568-165">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="16568-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="16568-166">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="16568-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="16568-167">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="16568-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="16568-168">Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto</span><span class="sxs-lookup"><span data-stu-id="16568-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="16568-169">Requisiti del sistema operativo per Reporting Server</span><span class="sxs-lookup"><span data-stu-id="16568-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="16568-170">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di report App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-171">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="16568-173">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16568-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-175">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-177">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-179">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-180">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="16568-181">Requisiti hardware del server di Reporting</span><span class="sxs-lookup"><span data-stu-id="16568-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="16568-182">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="16568-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="16568-183">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="16568-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="16568-184">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="16568-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="16568-185">Spazio su disco: 200 MB di spazio disponibile su disco rigido</span><span class="sxs-lookup"><span data-stu-id="16568-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="16568-186">Requisiti del database del server di report</span><span class="sxs-lookup"><span data-stu-id="16568-186">Reporting server database requirements</span></span>

<span data-ttu-id="16568-187">Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione del database di report App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-188">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="16568-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="16568-189">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="16568-190">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="16568-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-192">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-194">SP2</span><span class="sxs-lookup"><span data-stu-id="16568-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-195">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-197">SP3</span><span class="sxs-lookup"><span data-stu-id="16568-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-198">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="16568-199">Requisiti di sistema client App-V</span><span class="sxs-lookup"><span data-stu-id="16568-199">App-V client system requirements</span></span>


<span data-ttu-id="16568-200">La tabella seguente elenca i sistemi operativi supportati per l'installazione del client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-201">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="16568-203">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16568-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-205">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="16568-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-207">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-208">Windows7</span><span class="sxs-lookup"><span data-stu-id="16568-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-209">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-210">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16568-211">Gli scenari di installazione client App-V seguenti non sono supportati, ad eccezione di quanto indicato:</span><span class="sxs-lookup"><span data-stu-id="16568-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="16568-212">Computer che eseguono Windows Server</span><span class="sxs-lookup"><span data-stu-id="16568-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="16568-213">Computer che eseguono App-V 4.6 SP1 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="16568-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="16568-214">Il client di Servizi Desktop remoto di App-V 5,0 SP3 è supportato solo per i server abilitati per RDS</span><span class="sxs-lookup"><span data-stu-id="16568-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="16568-215">Requisiti hardware client App-V</span><span class="sxs-lookup"><span data-stu-id="16568-215">App-V client hardware requirements</span></span>

<span data-ttu-id="16568-216">Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="16568-217">Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="16568-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="16568-218">RAM — 1 GB (32 bit) o 2 GB (64 bit)</span><span class="sxs-lookup"><span data-stu-id="16568-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="16568-219">Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="16568-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="16568-220">Requisiti di sistema client di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="16568-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="16568-221">La tabella seguente elenca i sistemi operativi supportati per l'installazione client di Servizi Desktop remoto (RDS) App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-222">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-223">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="16568-224">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16568-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-226">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16568-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-228">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-230">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-231">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="16568-232">Requisiti hardware client di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="16568-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="16568-233">App-V non aggiunge requisiti aggiuntivi oltre a quelli di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="16568-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="16568-234">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="16568-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="16568-235">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="16568-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="16568-236">Spazio su disco: 200 MB di spazio disponibile su disco rigido</span><span class="sxs-lookup"><span data-stu-id="16568-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="16568-237">Requisiti di sistema sequencer</span><span class="sxs-lookup"><span data-stu-id="16568-237">Sequencer system requirements</span></span>


<span data-ttu-id="16568-238">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione di sequencer App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="16568-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16568-239">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="16568-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="16568-240">Service Pack</span><span class="sxs-lookup"><span data-stu-id="16568-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="16568-241">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="16568-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="16568-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="16568-243">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="16568-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-245">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="16568-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-247">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-248">64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16568-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-250">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16568-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="16568-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="16568-252">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16568-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="16568-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-254">SP1</span><span class="sxs-lookup"><span data-stu-id="16568-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="16568-255">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="16568-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="16568-256">Requisiti hardware sequencer</span><span class="sxs-lookup"><span data-stu-id="16568-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="16568-257">Vedere la documentazione di Windows o Windows Server per i requisiti hardware.</span><span class="sxs-lookup"><span data-stu-id="16568-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="16568-258">App-V non aggiunge requisiti hardware aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="16568-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="16568-259">Versioni supportate di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="16568-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="16568-260">Il client App-V supporta le versioni seguenti di System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="16568-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="16568-261">ConfigurationManager di MicrosoftSystemCenter2012</span><span class="sxs-lookup"><span data-stu-id="16568-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="16568-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="16568-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="16568-263">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="16568-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="16568-264">Per altre informazioni su come si integra Configuration Manager con App-V, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="16568-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="16568-265">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16568-265">Related topics</span></span>


[<span data-ttu-id="16568-266">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="16568-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="16568-267">Prerequisiti di App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="16568-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





