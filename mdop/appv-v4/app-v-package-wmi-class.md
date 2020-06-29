---
title: Classe WMI del pacchetto App-V
description: Classe WMI del pacchetto App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819796"
---
# <span data-ttu-id="6c4cb-103">Classe WMI del pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="6c4cb-103">App-V Package WMI Class</span></span>


<span data-ttu-id="6c4cb-104">Nel client Application Virtualization (App-V) la classe **Package** è una classe WMI (Windows Management Instrumentation) che rappresenta tutti i pacchetti virtuali nel client.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="6c4cb-105">I pacchetti virtuali possono contenere molte applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="6c4cb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c4cb-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="6c4cb-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c4cb-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="6c4cb-108">Nome</span><span class="sxs-lookup"><span data-stu-id="6c4cb-108">Name</span></span>**  
<span data-ttu-id="6c4cb-109">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-109">Data type: **String**</span></span>

<span data-ttu-id="6c4cb-110">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-110">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-111">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-111">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-112">Nome descrittivo del pacchetto virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="6c4cb-113">Versione</span><span class="sxs-lookup"><span data-stu-id="6c4cb-113">Version</span></span>**  
<span data-ttu-id="6c4cb-114">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-114">Data type: **String**</span></span>

<span data-ttu-id="6c4cb-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-115">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-116">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-116">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-117">Versione del pacchetto virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="6c4cb-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="6c4cb-118">PackageGUID</span></span>**  
<span data-ttu-id="6c4cb-119">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-119">Data type: **String**</span></span>

<span data-ttu-id="6c4cb-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-120">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-121">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="6c4cb-121">Qualifiers: Key</span></span>

<span data-ttu-id="6c4cb-122">Identificatore GUID della configurazione del pacchetto e dei file di origine.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="6c4cb-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="6c4cb-123">SftPath</span></span>**  
<span data-ttu-id="6c4cb-124">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-124">Data type: **String**</span></span>

<span data-ttu-id="6c4cb-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-125">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-126">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-126">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-127">Percorso del file SFT.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="6c4cb-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="6c4cb-128">TotalSize</span></span>**  
<span data-ttu-id="6c4cb-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-129">Data type: **UInt64**</span></span>

<span data-ttu-id="6c4cb-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-130">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-131">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-131">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-132">Dimensione totale del pacchetto virtuale, espressa in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="6c4cb-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="6c4cb-133">CachedSize</span></span>**  
<span data-ttu-id="6c4cb-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-134">Data type: **UInt64**</span></span>

<span data-ttu-id="6c4cb-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-135">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-136">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-136">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-137">Dimensione totale della cache per il pacchetto virtuale, espressa in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="6c4cb-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="6c4cb-138">LaunchSize</span></span>**  
<span data-ttu-id="6c4cb-139">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-139">Data type: **UInt64**</span></span>

<span data-ttu-id="6c4cb-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-140">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-141">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-141">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-142">Dimensione totale del blocco di funzionalità principale del pacchetto virtuale, espressa in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="6c4cb-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="6c4cb-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="6c4cb-144">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-144">Data type: **UInt64**</span></span>

<span data-ttu-id="6c4cb-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-145">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-146">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-146">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-147">Dimensione totale del blocco di funzionalità principale del pacchetto virtuale memorizzato nella cache, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="6c4cb-148">InUse</span><span class="sxs-lookup"><span data-stu-id="6c4cb-148">InUse</span></span>**  
<span data-ttu-id="6c4cb-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-149">Data type: **Boolean**</span></span>

<span data-ttu-id="6c4cb-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-150">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-151">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-151">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-152">**true** se è in corso un'applicazione virtuale nel pacchetto virtuale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="6c4cb-153">Bloccato</span><span class="sxs-lookup"><span data-stu-id="6c4cb-153">Locked</span></span>**  
<span data-ttu-id="6c4cb-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-154">Data type: **Boolean**</span></span>

<span data-ttu-id="6c4cb-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-155">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-156">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-156">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-157">**true** se il pacchetto virtuale è bloccato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="6c4cb-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="6c4cb-158">CachedPercentage</span></span>**  
<span data-ttu-id="6c4cb-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-159">Data type: **UInt16**</span></span>

<span data-ttu-id="6c4cb-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-160">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-161">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-161">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-162">Percentuale dei file di cache.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-162">The percentage of the cache files.</span></span> <span data-ttu-id="6c4cb-163">In base alla formula seguente: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="6c4cb-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="6c4cb-164">VersionGUID</span></span>**  
<span data-ttu-id="6c4cb-165">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6c4cb-165">Data type: **String**</span></span>

<span data-ttu-id="6c4cb-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c4cb-166">Access type: Read-only</span></span>

<span data-ttu-id="6c4cb-167">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="6c4cb-167">Qualifiers: None</span></span>

<span data-ttu-id="6c4cb-168">Identificatore GUID della versione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6c4cb-168">The GUID identifier of the package version.</span></span>

 

 





