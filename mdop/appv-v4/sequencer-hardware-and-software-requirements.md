---
title: Requisiti hardware e software per Sequencer
description: Requisiti hardware e software per Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815535"
---
# <span data-ttu-id="21434-103">Requisiti hardware e software per Sequencer</span><span class="sxs-lookup"><span data-stu-id="21434-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="21434-104">Questo argomento descrive i requisiti hardware e software minimi consigliati per il computer che gestisce Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="21434-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="21434-105">Prima di installare il sequencer e dopo aver sequenziato ogni applicazione, è necessario ripristinare un'immagine del sistema operativo pulito nel computer di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="21434-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="21434-106">Puoi usare uno dei metodi seguenti per ripristinare il computer che sta eseguendo il sequencer:</span><span class="sxs-lookup"><span data-stu-id="21434-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="21434-107">Riformattare il disco rigido e reinstallare il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21434-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="21434-108">Ripristinare il disco rigido nel computer in cui è in uso l'immagine del sequencer usando un altro software per la creazione di immagini disco.</span><span class="sxs-lookup"><span data-stu-id="21434-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="21434-109">L'elenco seguente descrive i requisiti hardware consigliati per l'uso dell'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="21434-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="21434-110">Requisiti hardware</span><span class="sxs-lookup"><span data-stu-id="21434-110">Hardware Requirements</span></span>

-   <span data-ttu-id="21434-111">Processore: Intel Pentium III, 1 GHz (32 bit o 64 bit).</span><span class="sxs-lookup"><span data-stu-id="21434-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="21434-112">Il processo di sequenziazione è un processo a thread singolo e non sfrutta i processori duali.</span><span class="sxs-lookup"><span data-stu-id="21434-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="21434-113">Memoria-1GB o superiore, 2 GB consigliati.</span><span class="sxs-lookup"><span data-stu-id="21434-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="21434-114">Disco rigido: spazio su disco rigido da 40 gigabyte (GB) con un minimo di 15 GB di spazio disponibile su disco rigido.</span><span class="sxs-lookup"><span data-stu-id="21434-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="21434-115">Ti consigliamo di avere almeno tre volte lo spazio sul disco rigido necessario per l'applicazione in sequenza.</span><span class="sxs-lookup"><span data-stu-id="21434-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="21434-116">**Nota**  La sequenziazione richiede l'utilizzo di dischi pesanti.</span><span class="sxs-lookup"><span data-stu-id="21434-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="21434-117">Una velocità del disco veloce può diminuire il tempo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="21434-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="21434-118">Requisiti software</span><span class="sxs-lookup"><span data-stu-id="21434-118">Software Requirements</span></span>

<span data-ttu-id="21434-119">L'elenco seguente descrive i sistemi operativi supportati per l'uso del sequencer.</span><span class="sxs-lookup"><span data-stu-id="21434-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21434-120">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="21434-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="21434-121">Edizione</span><span class="sxs-lookup"><span data-stu-id="21434-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="21434-122">Service Pack</span><span class="sxs-lookup"><span data-stu-id="21434-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="21434-123">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="21434-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21434-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="21434-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-125">Professional</span><span class="sxs-lookup"><span data-stu-id="21434-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-126">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="21434-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-127">x86</span><span class="sxs-lookup"><span data-stu-id="21434-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21434-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21434-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-129">Business, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="21434-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-130">Nessun Service Pack, SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="21434-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-131">x86</span><span class="sxs-lookup"><span data-stu-id="21434-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21434-132">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="21434-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-133">Professionale, aziendale o finale</span><span class="sxs-lookup"><span data-stu-id="21434-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="21434-134">x86</span><span class="sxs-lookup"><span data-stu-id="21434-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21434-135">¹ supportato per App-V 4,5 con SP1 o SP2 e solo App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="21434-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="21434-136">**Nota**  L'Application Virtualization (App-V) 4,6 Sequencer supporta versioni a 32 bit e 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="21434-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="21434-137">È consigliabile configurare i computer che eseguono il sequencer con le stesse applicazioni installate nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21434-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="21434-138">Requisiti software per Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="21434-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21434-139">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="21434-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="21434-140">Edizione</span><span class="sxs-lookup"><span data-stu-id="21434-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="21434-141">Service Pack</span><span class="sxs-lookup"><span data-stu-id="21434-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="21434-142">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="21434-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21434-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="21434-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-144">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="21434-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-145">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="21434-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-146">x86</span><span class="sxs-lookup"><span data-stu-id="21434-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21434-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="21434-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-148">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="21434-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="21434-149">x86</span><span class="sxs-lookup"><span data-stu-id="21434-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21434-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="21434-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-151">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="21434-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-152">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="21434-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21434-153">x86</span><span class="sxs-lookup"><span data-stu-id="21434-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21434-154">**Nota**  Application Virtualization (App-V) 4,6 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="21434-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="21434-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21434-155">Related topics</span></span>


[<span data-ttu-id="21434-156">Panoramica di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="21434-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





