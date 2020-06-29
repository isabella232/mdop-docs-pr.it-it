---
title: Configurazioni supportate di MBAM 2.0
description: Configurazioni supportate di MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823906"
---
# <span data-ttu-id="c6cd3-103">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c6cd3-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="c6cd3-104">In questo argomento vengono specificati i requisiti per l'installazione e l'esecuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 nell'ambiente tramite la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="c6cd3-105">Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="c6cd3-106">Se si prevede di installare MBAM 2,0 usando la topologia di Configuration Manager e si vuole rivedere un elenco dei requisiti di sistema, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="c6cd3-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="c6cd3-107">La configurazione consigliata per l'uso di MBAM in un ambiente di produzione è con due server, a seconda dei requisiti di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="c6cd3-108">Questa configurazione supporta fino a 200.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="c6cd3-109">Per un'immagine e le descrizioni dell'infrastruttura server di MBAM autonoma, vedere [architettura di alto livello per mbam 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c6cd3-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="c6cd3-110">**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="c6cd3-111">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="c6cd3-112">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="c6cd3-113">Requisiti di sistema di MBAM server</span><span class="sxs-lookup"><span data-stu-id="c6cd3-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="c6cd3-114">Requisiti del sistema operativo del server</span><span class="sxs-lookup"><span data-stu-id="c6cd3-114">Server Operating System Requirements</span></span>

<span data-ttu-id="c6cd3-115">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del server di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-116">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6cd3-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-117">Edizione</span><span class="sxs-lookup"><span data-stu-id="c6cd3-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-118">Service Pack</span><span class="sxs-lookup"><span data-stu-id="c6cd3-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-119">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="c6cd3-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6cd3-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-121">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-122">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-123">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="c6cd3-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-125">Versione standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="c6cd3-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="c6cd3-126">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c6cd3-127">**Nota**  Non è disponibile alcun supporto per l'installazione di servizi, report o database di MBAM in un computer controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="c6cd3-128">Requisiti per Server Processor, RAM e spazio su disco</span><span class="sxs-lookup"><span data-stu-id="c6cd3-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-129">Componente hardware</span><span class="sxs-lookup"><span data-stu-id="c6cd3-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-130">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="c6cd3-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-131">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="c6cd3-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-132">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="c6cd3-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-133">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="c6cd3-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-134">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="c6cd3-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-135">RAM</span><span class="sxs-lookup"><span data-stu-id="c6cd3-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-136">8 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-137">12 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-138">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="c6cd3-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-139">1 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-140">2 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="c6cd3-141">Requisiti per i database SQLServer</span><span class="sxs-lookup"><span data-stu-id="c6cd3-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="c6cd3-142">Nella tabella seguente sono elencate le versioni di SQLServer supportate per l'installazione delle funzionalità di amministrazione e monitoraggio del server, che include il database di ripristino, il database di conformità e di controllo e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="c6cd3-143">I database richiedono inoltre l'installazione di strumenti di gestione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="c6cd3-144">**Nota**  MBAM non supporta nativamente il clustering SQL, il mirroring o i gruppi di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="c6cd3-145">Per installare i database, è necessario eseguire l'installazione di MBAM server in un server SQL autonomo.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-146">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="c6cd3-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-147">Edizione</span><span class="sxs-lookup"><span data-stu-id="c6cd3-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-148">Service Pack</span><span class="sxs-lookup"><span data-stu-id="c6cd3-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-149">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="c6cd3-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6cd3-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-151">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-152">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-153">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="c6cd3-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-155">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-156">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-157">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-158">Componente hardware</span><span class="sxs-lookup"><span data-stu-id="c6cd3-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-159">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="c6cd3-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-160">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="c6cd3-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-161">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="c6cd3-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-162">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="c6cd3-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-163">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="c6cd3-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-164">RAM</span><span class="sxs-lookup"><span data-stu-id="c6cd3-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-165">8 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-166">12 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-167">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="c6cd3-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-168">5 GB</span><span class="sxs-lookup"><span data-stu-id="c6cd3-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-169">5 GB o superiore</span><span class="sxs-lookup"><span data-stu-id="c6cd3-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="c6cd3-170">Requisiti di sistema client di MBAM</span><span class="sxs-lookup"><span data-stu-id="c6cd3-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="c6cd3-171">Requisiti del sistema operativo client</span><span class="sxs-lookup"><span data-stu-id="c6cd3-171">Client Operating System Requirements</span></span>

<span data-ttu-id="c6cd3-172">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del client e il monitoraggio dell'amministrazione di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-173">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6cd3-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-174">Edizione</span><span class="sxs-lookup"><span data-stu-id="c6cd3-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-175">Service Pack</span><span class="sxs-lookup"><span data-stu-id="c6cd3-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-176">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="c6cd3-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-177">Windows7</span><span class="sxs-lookup"><span data-stu-id="c6cd3-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-178">Enterprise o Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-179">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-180">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-181">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6cd3-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-182">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-183">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-184">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="c6cd3-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-185">Windows 8 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-186">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="c6cd3-187">Requisiti di RAM client</span><span class="sxs-lookup"><span data-stu-id="c6cd3-187">Client RAM Requirements</span></span>

<span data-ttu-id="c6cd3-188">Non sono previsti requisiti di RAM specifici dell'installazione del client di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="c6cd3-189">Requisiti di sistema per i criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="c6cd3-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="c6cd3-190">Nella tabella seguente sono elencati i sistemi operativi supportati per l'installazione del modello di criteri di gruppo di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6cd3-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6cd3-191">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6cd3-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-192">Edizione</span><span class="sxs-lookup"><span data-stu-id="c6cd3-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-193">Service Pack</span><span class="sxs-lookup"><span data-stu-id="c6cd3-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="c6cd3-194">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="c6cd3-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-195">Windows7</span><span class="sxs-lookup"><span data-stu-id="c6cd3-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-196">Enterprise o Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-197">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-198">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-199">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6cd3-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-200">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-201">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6cd3-202">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6cd3-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-203">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c6cd3-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-204">SP1</span><span class="sxs-lookup"><span data-stu-id="c6cd3-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-205">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6cd3-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6cd3-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-207">Versione standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="c6cd3-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c6cd3-208">64 bit</span><span class="sxs-lookup"><span data-stu-id="c6cd3-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c6cd3-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6cd3-209">Related topics</span></span>


[<span data-ttu-id="c6cd3-210">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c6cd3-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="c6cd3-211">Prerequisiti per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c6cd3-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





