---
title: Requisiti hardware e software per Application Virtualization Sequencer
description: Requisiti hardware e software per Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819625"
---
# <span data-ttu-id="2fc1f-103">Requisiti hardware e software per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2fc1f-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="2fc1f-104">Questo argomento descrive i requisiti hardware e software minimi consigliati per il computer che gestisce Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="2fc1f-105">**Importante**  Devi eseguire l'App-V Sequencer (**SFTSequencer.exe**) usando un account con privilegi di amministratore a causa delle modifiche apportate dal sequencer al sistema locale.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="2fc1f-106">Queste modifiche possono includere la scrittura di file nella directory **C:\\Programmi files** , le modifiche del registro di sistema, l'avvio e l'arresto dei servizi, l'aggiornamento dei descrittori di sicurezza per i file e la modifica delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="2fc1f-107">Prima di installare il sequencer e dopo aver sequenziato ogni applicazione, è necessario ripristinare un'immagine del sistema operativo pulito nel computer di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="2fc1f-108">Puoi usare uno dei metodi seguenti per ripristinare il computer che sta eseguendo il sequencer:</span><span class="sxs-lookup"><span data-stu-id="2fc1f-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="2fc1f-109">Riformattare il disco rigido e reinstallare il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="2fc1f-110">Ripristinare il disco rigido nel computer in cui è in uso l'immagine del sequencer usando un altro software per la creazione di immagini disco.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="2fc1f-111">Ripristinare un'immagine del sistema operativo virtuale, ad esempio un'immagine di Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="2fc1f-112">L'uso di una macchina virtuale consente di riutilizzare facilmente gli ambienti di sequenziazione con l'amministrazione minima.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="2fc1f-113">L'elenco seguente descrive i requisiti hardware consigliati per l'uso dell'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="2fc1f-114">I requisiti sono elencati per primo per Microsoft Application Virtualization (App-V) 4.6 SP2, seguiti dai requisiti per le versioni che hanno preceduto l'App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="2fc1f-115">Requisiti hardware</span><span class="sxs-lookup"><span data-stu-id="2fc1f-115">Hardware Requirements</span></span>

-   <span data-ttu-id="2fc1f-116">Processore: Intel Pentium III, 1 GHz (32 bit o 64 bit).</span><span class="sxs-lookup"><span data-stu-id="2fc1f-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="2fc1f-117">Il processo di sequenziazione è un processo a thread singolo e non sfrutta i processori duali.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="2fc1f-118">Memoria-1GB o superiore, 2GB consigliata.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="2fc1f-119">Disco rigido: spazio su disco rigido da 40 gigabyte (GB) con un minimo di 15 GB di spazio disponibile su disco rigido.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="2fc1f-120">Ti consigliamo di avere almeno tre volte lo spazio sul disco rigido necessario per l'applicazione in sequenza.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="2fc1f-121">**Nota**  La sequenziazione richiede l'utilizzo di dischi pesanti.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="2fc1f-122">Una velocità del disco veloce può diminuire il tempo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="2fc1f-123">Requisiti software per App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="2fc1f-124">L'elenco seguente descrive i sistemi operativi supportati per l'uso dell'App-V 4,6 SP2 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fc1f-125">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2fc1f-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-126">Edizione</span><span class="sxs-lookup"><span data-stu-id="2fc1f-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2fc1f-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-128">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2fc1f-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="2fc1f-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-130">Professional</span><span class="sxs-lookup"><span data-stu-id="2fc1f-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-131">SP3</span><span class="sxs-lookup"><span data-stu-id="2fc1f-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-132">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fc1f-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-134">Business, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="2fc1f-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-135">SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-136">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-137">Windows7</span><span class="sxs-lookup"><span data-stu-id="2fc1f-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-138">Professionale, aziendale o finale</span><span class="sxs-lookup"><span data-stu-id="2fc1f-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-139">Nessun Service Pack o SP1</span><span class="sxs-lookup"><span data-stu-id="2fc1f-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-140">x86 e x64</span><span class="sxs-lookup"><span data-stu-id="2fc1f-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2fc1f-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-142">Pro o Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-143">x86 e x64</span><span class="sxs-lookup"><span data-stu-id="2fc1f-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fc1f-144">**Nota**  Il sequencer di Application Virtualization (App-V) 4,6 SP2 supporta versioni a 32 bit e 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="2fc1f-145">È consigliabile configurare i computer che eseguono il sequencer con le stesse applicazioni installate nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="2fc1f-146">Requisiti software per le versioni che precedono l'App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="2fc1f-147">L'elenco seguente descrive i sistemi operativi supportati per l'uso del sequencer per le versioni precedenti a App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fc1f-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2fc1f-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-149">Edizione</span><span class="sxs-lookup"><span data-stu-id="2fc1f-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2fc1f-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-151">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2fc1f-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="2fc1f-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-153">Professional</span><span class="sxs-lookup"><span data-stu-id="2fc1f-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-154">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="2fc1f-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-155">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fc1f-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-157">Business, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="2fc1f-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-158">Nessun Service Pack, SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-159">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-160">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="2fc1f-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-161">Professionale, aziendale o finale</span><span class="sxs-lookup"><span data-stu-id="2fc1f-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-162">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fc1f-163">¹ supportato per App-V 4,5 con SP1 o SP2 e solo App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="2fc1f-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="2fc1f-164">**Nota**  L'Application Virtualization (App-V) 4,6 Sequencer supporta versioni a 32 bit e 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="2fc1f-165">È consigliabile configurare i computer che eseguono il sequencer con le stesse applicazioni installate nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="2fc1f-166">Requisiti software per Servizi Desktop remoti per App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fc1f-167">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2fc1f-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-168">Edizione</span><span class="sxs-lookup"><span data-stu-id="2fc1f-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-169">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2fc1f-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-170">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2fc1f-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-172">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-173">SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-174">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="2fc1f-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-176">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-177">SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-178">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-180">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-181">Nessun Service Pack o SP1</span><span class="sxs-lookup"><span data-stu-id="2fc1f-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-182">x64</span><span class="sxs-lookup"><span data-stu-id="2fc1f-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fc1f-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-184">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-185">x86 o x64</span><span class="sxs-lookup"><span data-stu-id="2fc1f-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fc1f-186">**Nota**  Application Virtualization (App-V) 4,6 SP2 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="2fc1f-187">Requisiti software per i Servizi Desktop remoto per le versioni che precedono l'App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fc1f-188">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2fc1f-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-189">Edizione</span><span class="sxs-lookup"><span data-stu-id="2fc1f-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-190">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2fc1f-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2fc1f-191">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2fc1f-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="2fc1f-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-193">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-194">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-195">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-197">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-198">Nessun Service Pack o SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-199">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fc1f-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="2fc1f-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-201">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-202">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-203">x86</span><span class="sxs-lookup"><span data-stu-id="2fc1f-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fc1f-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fc1f-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-205">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2fc1f-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-206">Nessun Service Pack o SP1</span><span class="sxs-lookup"><span data-stu-id="2fc1f-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fc1f-207">x64</span><span class="sxs-lookup"><span data-stu-id="2fc1f-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fc1f-208">**Nota**  Application Virtualization (App-V) 4,6 SP2 per Servizi Desktop remoto supporta versioni a 32 bit e a 64 bit di questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2fc1f-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="2fc1f-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fc1f-209">Related topics</span></span>


[<span data-ttu-id="2fc1f-210">Requisiti hardware e software per Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="2fc1f-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="2fc1f-211">Requisiti di sistema di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2fc1f-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="2fc1f-212">Come installare Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2fc1f-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="2fc1f-213">Come eseguire l'aggiornamento di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2fc1f-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





