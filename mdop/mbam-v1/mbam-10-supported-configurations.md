---
title: Configurazioni supportate di MBAM 1.0
description: Configurazioni supportate di MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825936"
---
# <span data-ttu-id="375cc-103">Configurazioni supportate di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="375cc-103">MBAM 1.0 Supported Configurations</span></span>


<span data-ttu-id="375cc-104">Questo argomento specifica i requisiti necessari per installare ed eseguire l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="375cc-104">This topic specifies the necessary requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) in your environment.</span></span>

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="375cc-105">Requisiti di sistema di MBAM server</span><span class="sxs-lookup"><span data-stu-id="375cc-105">MBAM server system Requirements</span></span>


### <span data-ttu-id="375cc-106">Requisiti del sistema operativo del server</span><span class="sxs-lookup"><span data-stu-id="375cc-106">Server operating system requirements</span></span>

<span data-ttu-id="375cc-107">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="375cc-107">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

**<span data-ttu-id="375cc-108">Nota</span><span class="sxs-lookup"><span data-stu-id="375cc-108">Note</span></span>**  
<span data-ttu-id="375cc-109">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="375cc-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375cc-110">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="375cc-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375cc-111">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="375cc-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375cc-112">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375cc-112">Operating System</span></span></th>
<th align="left"><span data-ttu-id="375cc-113">Edizione</span><span class="sxs-lookup"><span data-stu-id="375cc-113">Edition</span></span></th>
<th align="left"><span data-ttu-id="375cc-114">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375cc-114">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="375cc-115">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="375cc-115">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375cc-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="375cc-116">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-117">Standard, Enterprise, Datacenter o server Web</span><span class="sxs-lookup"><span data-stu-id="375cc-117">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-118">Solo SP2</span><span class="sxs-lookup"><span data-stu-id="375cc-118">SP2 only</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-119">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-119">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375cc-120">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="375cc-120">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-121">Standard, Enterprise, Datacenter o server Web</span><span class="sxs-lookup"><span data-stu-id="375cc-121">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375cc-122">64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-122">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="375cc-123">Warning</span><span class="sxs-lookup"><span data-stu-id="375cc-123">Warning</span></span>**  
<span data-ttu-id="375cc-124">Non è disponibile alcun supporto per l'installazione di servizi, report o database di MBAM in un computer controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="375cc-124">There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>



### <a href="" id="server-random-access-memory--ram--requirements-"></a><span data-ttu-id="375cc-125">Requisiti della RAM (Random Access Memory) del server</span><span class="sxs-lookup"><span data-stu-id="375cc-125">Server random access memory (RAM) requirements</span></span>

<span data-ttu-id="375cc-126">Non ci sono requisiti di RAM specifici per l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="375cc-126">There are no RAM requirements that are specific to MBAM Server installation.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="375cc-127">Requisiti di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="375cc-127">SQL Server Database requirements</span></span>

<span data-ttu-id="375cc-128">La tabella seguente elenca le versioni di SQL Server supportate per l'installazione delle funzionalità di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="375cc-128">The following table lists the SQL Server versions that are supported for the MBAM Server feature installation.</span></span>

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
<th align="left"><span data-ttu-id="375cc-129">Funzionalità del server MBAM</span><span class="sxs-lookup"><span data-stu-id="375cc-129">MBAM Server Feature</span></span></th>
<th align="left"><span data-ttu-id="375cc-130">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="375cc-130">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="375cc-131">Edizione</span><span class="sxs-lookup"><span data-stu-id="375cc-131">Edition</span></span></th>
<th align="left"><span data-ttu-id="375cc-132">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375cc-132">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="375cc-133">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="375cc-133">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375cc-134">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="375cc-134">Compliance and Audit Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-135">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="375cc-135">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="375cc-136">R2, standard, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="375cc-136">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-137">SP2</span><span class="sxs-lookup"><span data-stu-id="375cc-137">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-138">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-138">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375cc-139">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="375cc-139">Recovery and Hardware Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-140">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="375cc-140">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="375cc-141">R2, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="375cc-141">R2, Enterprise, Datacenter, or Developer Edition</span></span></p>
<div class="alert">
<strong><span data-ttu-id="375cc-142">Importante</span><span class="sxs-lookup"><span data-stu-id="375cc-142">Important</span></span></strong><br/><p><span data-ttu-id="375cc-143">Le edizioni standard di SQL Server non sono supportate per l'installazione delle funzionalità del server database hardware e ripristino di MBAM.</span><span class="sxs-lookup"><span data-stu-id="375cc-143">SQL Server Standard Editions are not supported for MBAM Recovery and Hardware Database Server feature installation.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="375cc-144">SP2</span><span class="sxs-lookup"><span data-stu-id="375cc-144">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-145">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375cc-146">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="375cc-146">Compliance and Audit Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-147">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="375cc-147">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="375cc-148">R2, standard, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="375cc-148">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-149">SP2</span><span class="sxs-lookup"><span data-stu-id="375cc-149">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-150">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-150">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="375cc-151">Requisiti di sistema client di MBAM</span><span class="sxs-lookup"><span data-stu-id="375cc-151">MBAM Client system requirements</span></span>


### <span data-ttu-id="375cc-152">Requisiti del sistema operativo client</span><span class="sxs-lookup"><span data-stu-id="375cc-152">Client operating system requirements</span></span>

<span data-ttu-id="375cc-153">La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="375cc-153">The following table lists the operating systems that are supported for MBAM Client installation.</span></span>

**<span data-ttu-id="375cc-154">Nota</span><span class="sxs-lookup"><span data-stu-id="375cc-154">Note</span></span>**  
<span data-ttu-id="375cc-155">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="375cc-155">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375cc-156">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="375cc-156">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375cc-157">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="375cc-157">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375cc-158">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375cc-158">Operating System</span></span></th>
<th align="left"><span data-ttu-id="375cc-159">Edizione</span><span class="sxs-lookup"><span data-stu-id="375cc-159">Edition</span></span></th>
<th align="left"><span data-ttu-id="375cc-160">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375cc-160">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="375cc-161">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="375cc-161">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375cc-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="375cc-162">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-163">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="375cc-163">Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-164">Nessuno, SP1</span><span class="sxs-lookup"><span data-stu-id="375cc-164">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-165">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-165">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375cc-166">Windows 7</span><span class="sxs-lookup"><span data-stu-id="375cc-166">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-167">Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="375cc-167">Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-168">Nessuno, SP1</span><span class="sxs-lookup"><span data-stu-id="375cc-168">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="375cc-169">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="375cc-169">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="375cc-170">Requisiti di RAM client</span><span class="sxs-lookup"><span data-stu-id="375cc-170">Client RAM requirements</span></span>

<span data-ttu-id="375cc-171">Non ci sono requisiti di RAM specifici per l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="375cc-171">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <span data-ttu-id="375cc-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="375cc-172">Related topics</span></span>


[<span data-ttu-id="375cc-173">Pianificazione della distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="375cc-173">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="375cc-174">Prerequisiti per la distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="375cc-174">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)









