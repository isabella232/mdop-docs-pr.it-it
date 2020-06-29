---
title: Configurazioni supportate di App-V 5.0
description: Configurazioni supportate di App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805991"
---
# <span data-ttu-id="0636c-103">Configurazioni supportate di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0636c-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="0636c-104">Questo argomento specifica i requisiti necessari per installare ed eseguire Microsoft Application Virtualization (App-V) 5,0 nell'ambiente in uso.</span><span class="sxs-lookup"><span data-stu-id="0636c-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="0636c-105">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-105">Important</span></span>**  
<span data-ttu-id="0636c-106">**Le configurazioni supportate in questo articolo si applicano solo a App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="0636c-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="0636c-107">Per le configurazioni supportate che si applicano ai Service Pack App-V 5,0, vedere le pagine Web seguenti:</span><span class="sxs-lookup"><span data-stu-id="0636c-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="0636c-108">Novità in App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="0636c-109">Informazioni su App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="0636c-110">Configurazioni supportate da App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="0636c-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="0636c-111">Requisiti di sistema server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="0636c-112">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-112">Important</span></span>**  
<span data-ttu-id="0636c-113">Il server App-V 5,0 non supporta gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="0636c-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="0636c-114">Distribuzione in un computer che esegue Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="0636c-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="0636c-115">Distribuzione in un computer in cui è in esecuzione una versione precedente di componenti server App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="0636c-116">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-116">Note</span></span>**  
    <span data-ttu-id="0636c-117">È possibile installare l'App-V 5,0 affiancata con il solo server App-V 4,5 Lightweight streaming server (garanzia).</span><span class="sxs-lookup"><span data-stu-id="0636c-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="0636c-118">La distribuzione di App-V 5,0 affiancata al server HWS (Application Virtualization Management Service) App-V 4,5 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0636c-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="0636c-119">Distribuzione in un computer che esegue Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="0636c-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="0636c-120">Distribuzione remota del database del server di gestione o del database di report.</span><span class="sxs-lookup"><span data-stu-id="0636c-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="0636c-121">Il programma di installazione deve essere eseguito direttamente nel computer in cui è in esecuzione Microsoft SQL per l'installazione del database per avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0636c-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="0636c-122">Distribuzione a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="0636c-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="0636c-123">I percorsi brevi non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0636c-123">Short paths are not supported.</span></span> <span data-ttu-id="0636c-124">Se si prevede di usare un breve percorso, è necessario creare un nuovo volume.</span><span class="sxs-lookup"><span data-stu-id="0636c-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="0636c-125">Requisiti del sistema operativo del server di gestione</span><span class="sxs-lookup"><span data-stu-id="0636c-125">Management Server operating system requirements</span></span>

<span data-ttu-id="0636c-126">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di gestione App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="0636c-127">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-127">Note</span></span>**  
<span data-ttu-id="0636c-128">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-129">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-130">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-131">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0636c-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0636c-132">Edizione</span><span class="sxs-lookup"><span data-stu-id="0636c-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="0636c-133">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-134">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-135">Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</span><span class="sxs-lookup"><span data-stu-id="0636c-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-136">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-137">SP1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="0636c-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-138">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-139">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-140">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-141">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-142">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-143">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="0636c-144">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-144">Important</span></span>**  
<span data-ttu-id="0636c-145">La distribuzione del ruolo del server di gestione in un computer con funzionalità RDS (Remote Desktop Sharing) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0636c-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="0636c-146">Requisiti hardware del server di gestione</span><span class="sxs-lookup"><span data-stu-id="0636c-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="0636c-147">Processore-1,4 GHz o più veloce, processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="0636c-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="0636c-148">RAM — 1 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="0636c-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="0636c-149">Spazio su disco: 200 MB di spazio disponibile su disco rigido, senza includere la directory di contenuto.</span><span class="sxs-lookup"><span data-stu-id="0636c-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="0636c-150">Requisiti del sistema operativo di Publishing Server</span><span class="sxs-lookup"><span data-stu-id="0636c-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="0636c-151">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di pubblicazione App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="0636c-152">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-152">Note</span></span>**  
<span data-ttu-id="0636c-153">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-154">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-155">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-156">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0636c-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0636c-157">Edizione</span><span class="sxs-lookup"><span data-stu-id="0636c-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="0636c-158">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-159">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-160">Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</span><span class="sxs-lookup"><span data-stu-id="0636c-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-161">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-162">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-163">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-164">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-165">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-166">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-167">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="0636c-168">Requisiti hardware del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="0636c-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="0636c-169">Processore: 1,4 GHz o più veloce.</span><span class="sxs-lookup"><span data-stu-id="0636c-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="0636c-170">processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="0636c-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="0636c-171">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="0636c-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="0636c-172">Spazio su disco: 200 MB di spazio disponibile su disco rigido.</span><span class="sxs-lookup"><span data-stu-id="0636c-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="0636c-173">non inclusa la directory di contenuto</span><span class="sxs-lookup"><span data-stu-id="0636c-173">not including content directory</span></span>

### <span data-ttu-id="0636c-174">Requisiti del sistema operativo per Reporting Server</span><span class="sxs-lookup"><span data-stu-id="0636c-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="0636c-175">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di report App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="0636c-176">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-176">Note</span></span>**  
<span data-ttu-id="0636c-177">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-178">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-179">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-180">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0636c-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0636c-181">Edizione</span><span class="sxs-lookup"><span data-stu-id="0636c-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="0636c-182">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-183">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-184">Microsoft Windows Server 2008 (standard, Enterprise, Datacenter o server Web)</span><span class="sxs-lookup"><span data-stu-id="0636c-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-185">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-186">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-187">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-188">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-189">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-190">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-191">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="0636c-192">Requisiti hardware del server di Reporting</span><span class="sxs-lookup"><span data-stu-id="0636c-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="0636c-193">Processore: 1,4 GHz o più veloce.</span><span class="sxs-lookup"><span data-stu-id="0636c-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="0636c-194">processore a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="0636c-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="0636c-195">RAM — 2 GB di RAM (64 bit)</span><span class="sxs-lookup"><span data-stu-id="0636c-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="0636c-196">Spazio su disco: 200 MB di spazio disponibile su disco rigido</span><span class="sxs-lookup"><span data-stu-id="0636c-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="0636c-197">Requisiti di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="0636c-197">SQL Server database requirements</span></span>

<span data-ttu-id="0636c-198">Nella tabella seguente sono elencate le versioni di SQL Server supportate per l'installazione di database e server di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-199">Tipo di server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="0636c-200">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="0636c-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="0636c-201">Edizione</span><span class="sxs-lookup"><span data-stu-id="0636c-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="0636c-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-203">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-204">Gestione/creazione di report</span><span class="sxs-lookup"><span data-stu-id="0636c-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="0636c-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="0636c-206">(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</span><span class="sxs-lookup"><span data-stu-id="0636c-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-207">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-208">Gestione/creazione di report</span><span class="sxs-lookup"><span data-stu-id="0636c-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="0636c-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="0636c-210">(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</span><span class="sxs-lookup"><span data-stu-id="0636c-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-211">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-212">SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-213">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-214">Gestione/creazione di report</span><span class="sxs-lookup"><span data-stu-id="0636c-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="0636c-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="0636c-216">(Standard, Enterprise, Datacenter o Developer Edition con la caratteristica seguente: <strong> Servizi motore di database </strong> .)</span><span class="sxs-lookup"><span data-stu-id="0636c-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-217">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="0636c-218">Requisiti di sistema client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="0636c-219">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="0636c-220">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-220">Note</span></span>**  
<span data-ttu-id="0636c-221">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-222">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-223">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-224">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0636c-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0636c-225">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-226">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="0636c-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-228">SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-229">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="0636c-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-231">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="0636c-232">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-232">Important</span></span></strong><br/><p><span data-ttu-id="0636c-233">Windows 8,1 è supportato solo da App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="0636c-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0636c-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-235">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0636c-236">Gli scenari di installazione client App-V seguenti non sono supportati, ad eccezione di quanto indicato:</span><span class="sxs-lookup"><span data-stu-id="0636c-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="0636c-237">Computer che eseguono Windows Server</span><span class="sxs-lookup"><span data-stu-id="0636c-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="0636c-238">Computer che eseguono App-V 4,6 SP1 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="0636c-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="0636c-239">Il client Servizi Desktop remoto di App-V 5,0 è supportato solo per i server abilitati per RDS</span><span class="sxs-lookup"><span data-stu-id="0636c-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="0636c-240">Requisiti hardware client</span><span class="sxs-lookup"><span data-stu-id="0636c-240">Client hardware requirements</span></span>

<span data-ttu-id="0636c-241">Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="0636c-242">Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="0636c-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="0636c-243">RAM — 1 GB (32 bit) o 2 GB (64 bit)</span><span class="sxs-lookup"><span data-stu-id="0636c-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="0636c-244">Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="0636c-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="0636c-245">Requisiti di sistema client desktop remoto App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="0636c-246">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client desktop remoto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="0636c-247">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-247">Note</span></span>**  
<span data-ttu-id="0636c-248">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-249">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-250">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="0636c-251">Sistema operativo Edition Service Pack Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0636c-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="0636c-252">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-252">R2</span></span>

<span data-ttu-id="0636c-253">SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-253">SP1</span></span>

<span data-ttu-id="0636c-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0636c-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="0636c-255">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-255">Important</span></span>**  
<span data-ttu-id="0636c-256">Windows Server 2012 R2 è supportato solo da App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="0636c-257">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="0636c-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="0636c-258">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-258">R2</span></span>

<span data-ttu-id="0636c-259">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="0636c-260">Requisiti hardware client desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0636c-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="0636c-261">Nell'elenco seguente viene visualizzata la configurazione hardware supportata per l'installazione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="0636c-262">Processore-1,4 GHz o più veloce a 32 bit (x86) o a 64 bit (x64)</span><span class="sxs-lookup"><span data-stu-id="0636c-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="0636c-263">RAM — 1 GB (32 bit) o 2 GB (64 bit)</span><span class="sxs-lookup"><span data-stu-id="0636c-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="0636c-264">Disk-100 MB per l'installazione, senza includere lo spazio su disco usato dalle applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="0636c-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="0636c-265">Requisiti di sistema sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="0636c-266">La tabella seguente elenca i sistemi operativi supportati per l'installazione di Sequencer in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0636c-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="0636c-267">Nota</span><span class="sxs-lookup"><span data-stu-id="0636c-267">Note</span></span>**  
<span data-ttu-id="0636c-268">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="0636c-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="0636c-269">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="0636c-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="0636c-270">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0636c-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-271">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0636c-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0636c-272">Edizione</span><span class="sxs-lookup"><span data-stu-id="0636c-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="0636c-273">Service Pack</span><span class="sxs-lookup"><span data-stu-id="0636c-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="0636c-274">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="0636c-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="0636c-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-276">SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-277">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="0636c-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-279">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="0636c-280">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-280">Important</span></span></strong><br/><p><span data-ttu-id="0636c-281">Windows 8,1 è supportato solo da App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="0636c-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0636c-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-283">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0636c-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-285">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-286">SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-287">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0636c-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="0636c-289">32 bit e 64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="0636c-290">Importante</span><span class="sxs-lookup"><span data-stu-id="0636c-290">Important</span></span></strong><br/><p><span data-ttu-id="0636c-291">Windows Server 2012 R2 è supportato solo da App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="0636c-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0636c-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="0636c-293">R2</span><span class="sxs-lookup"><span data-stu-id="0636c-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="0636c-294">64 bit</span><span class="sxs-lookup"><span data-stu-id="0636c-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="0636c-295">Versioni supportate di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0636c-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="0636c-296">È possibile usare Microsoft System Center 2012 Configuration Manager o System Center 2012 R2 Configuration Manager per gestire le applicazioni virtuali App-V, i report e altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="0636c-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="0636c-297">La tabella seguente elenca le versioni supportate di Configuration Manager per ogni versione applicabile di App-V.</span><span class="sxs-lookup"><span data-stu-id="0636c-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0636c-298">Versione di Configuration Manager supportata</span><span class="sxs-lookup"><span data-stu-id="0636c-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="0636c-299">Versione App-V</span><span class="sxs-lookup"><span data-stu-id="0636c-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0636c-300">Gestione configurazione di Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="0636c-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0636c-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="0636c-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="0636c-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0636c-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0636c-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0636c-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="0636c-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="0636c-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="0636c-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="0636c-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="0636c-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0636c-308">Per altre informazioni su come si integra Configuration Manager con App-V, vedere [pianificazione dell'integrazione di App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="0636c-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="0636c-309">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0636c-309">Related topics</span></span>


[<span data-ttu-id="0636c-310">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="0636c-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="0636c-311">Prerequisiti di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0636c-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









