---
title: Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale
description: Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817505"
---
# <span data-ttu-id="e7c23-103">Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="e7c23-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="e7c23-104">Usare la tabella seguente per determinare se un pacchetto di applicazione virtuale può essere aperto per la modifica, se è necessario creare una nuova versione del pacchetto o se è disponibile un'opzione, usando l'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="e7c23-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e7c23-105">Azione</span><span class="sxs-lookup"><span data-stu-id="e7c23-105">Action</span></span></th>
<th align="left"><span data-ttu-id="e7c23-106">Apri per la modifica</span><span class="sxs-lookup"><span data-stu-id="e7c23-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="e7c23-107">Apri per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e7c23-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-108">Visualizzare le proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e7c23-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-109">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-110">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-111">Visualizzare la cronologia delle modifiche del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e7c23-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-112">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-113">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-114">Visualizzare i file di pacchetto associati.</span><span class="sxs-lookup"><span data-stu-id="e7c23-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-115">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-116">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-117">Modificare le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e7c23-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-118">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-119">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-120">Rivedere le impostazioni aggiuntive del pacchetto (ad eccezione delle proprietà del file di sistema operativo).</span><span class="sxs-lookup"><span data-stu-id="e7c23-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-121">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-122">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-123">Creare Windows Installer (MSI) associato.</span><span class="sxs-lookup"><span data-stu-id="e7c23-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-124">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-125">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-126">Modificare il file OSD.</span><span class="sxs-lookup"><span data-stu-id="e7c23-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-127">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-128">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-129">Comprimere e decomprimere il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e7c23-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-130">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-131">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-132">Aggiungere associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="e7c23-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-133">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-134">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-135">Rinominare i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e7c23-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-136">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-137">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-138">Impostare lo stato della chiave del registro di sistema virtualizzato (override/merge).</span><span class="sxs-lookup"><span data-stu-id="e7c23-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-139">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-140">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-141">Impostare lo stato della cartella virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="e7c23-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-142">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-143">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-144">Modificare i mapping di file system virtuali.</span><span class="sxs-lookup"><span data-stu-id="e7c23-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-145">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-146">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-147">Esaminare tutte le proprietà del file del sistema operativo associato per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e7c23-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-148">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-149">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-150">Aggiungere altri servizi.</span><span class="sxs-lookup"><span data-stu-id="e7c23-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-151">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-152">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-153">Aggiungere altri file.</span><span class="sxs-lookup"><span data-stu-id="e7c23-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-154">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-155">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-156">Raccogliere e configurare i descrittori di sicurezza associati.</span><span class="sxs-lookup"><span data-stu-id="e7c23-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-157">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-158">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-159">Applicare gli aggiornamenti della sicurezza o eseguire l'aggiornamento a una nuova versione.</span><span class="sxs-lookup"><span data-stu-id="e7c23-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-160">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-161">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-162">Aggiungere un'applicazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="e7c23-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-163">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-164">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7c23-165">Applicare gli aggiornamenti che richiedono l'apertura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7c23-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-166">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-167">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7c23-168">Applicare gli aggiornamenti che richiedono il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="e7c23-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-169">No</span><span class="sxs-lookup"><span data-stu-id="e7c23-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7c23-170">Sì</span><span class="sxs-lookup"><span data-stu-id="e7c23-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e7c23-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7c23-171">Related topics</span></span>


[<span data-ttu-id="e7c23-172">Come modificare un'applicazione virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e7c23-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="e7c23-173">Come eseguire l'aggiornamento di un'applicazione virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="e7c23-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





