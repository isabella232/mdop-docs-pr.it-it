---
title: Classe WMI dell'applicazione App-V
description: Classe WMI dell'applicazione App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822325"
---
# <span data-ttu-id="07b45-103">Classe WMI dell'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="07b45-103">App-V Application WMI Class</span></span>


<span data-ttu-id="07b45-104">Nel client Application Virtualization (App-V) la classe **Application** è una classe WMI (Windows Management Instrumentation) che rappresenta tutte le applicazioni virtuali nel client.</span><span class="sxs-lookup"><span data-stu-id="07b45-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="07b45-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="07b45-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="07b45-106">Il codice include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="07b45-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="07b45-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07b45-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="07b45-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07b45-108">Requirements</span></span>


## <span data-ttu-id="07b45-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07b45-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="07b45-110">Nome</span><span class="sxs-lookup"><span data-stu-id="07b45-110">Name</span></span>**  
<span data-ttu-id="07b45-111">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="07b45-111">Data type: **String**</span></span>

<span data-ttu-id="07b45-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-112">Access type: Read-only</span></span>

<span data-ttu-id="07b45-113">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="07b45-113">Qualifiers: Key</span></span>

<span data-ttu-id="07b45-114">Nome visualizzato dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="07b45-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="07b45-115">Versione</span><span class="sxs-lookup"><span data-stu-id="07b45-115">Version</span></span>**  
<span data-ttu-id="07b45-116">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="07b45-116">Data type: **String**</span></span>

<span data-ttu-id="07b45-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-117">Access type: Read-only</span></span>

<span data-ttu-id="07b45-118">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="07b45-118">Qualifiers: Key</span></span>

<span data-ttu-id="07b45-119">Versione dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="07b45-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="07b45-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="07b45-120">PackageGUID</span></span>**  
<span data-ttu-id="07b45-121">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="07b45-121">Data type: **String**</span></span>

<span data-ttu-id="07b45-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-122">Access type: Read-only</span></span>

<span data-ttu-id="07b45-123">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-123">Qualifiers: None</span></span>

<span data-ttu-id="07b45-124">GUID del pacchetto a cui è associata l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="07b45-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="07b45-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="07b45-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="07b45-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07b45-126">Data type: **DateTime**</span></span>

<span data-ttu-id="07b45-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-127">Access type: Read-only</span></span>

<span data-ttu-id="07b45-128">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-128">Qualifiers: None</span></span>

<span data-ttu-id="07b45-129">Ultima data e ora in cui è stata avviata l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="07b45-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="07b45-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="07b45-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="07b45-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b45-131">Data type: **UInt32**</span></span>

<span data-ttu-id="07b45-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-132">Access type: Read-only</span></span>

<span data-ttu-id="07b45-133">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-133">Qualifiers: None</span></span>

<span data-ttu-id="07b45-134">Conteggio delle istanze in uso dell'applicazione virtuale avviate direttamente.</span><span class="sxs-lookup"><span data-stu-id="07b45-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="07b45-135">Caricamento in corso</span><span class="sxs-lookup"><span data-stu-id="07b45-135">Loading</span></span>**  
<span data-ttu-id="07b45-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="07b45-136">Data type: **Boolean**</span></span>

<span data-ttu-id="07b45-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-137">Access type: Read-only</span></span>

<span data-ttu-id="07b45-138">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-138">Qualifiers: None</span></span>

<span data-ttu-id="07b45-139">**true** se l'applicazione virtuale viene avviata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="07b45-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="07b45-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="07b45-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="07b45-141">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="07b45-141">Data type: **String**</span></span>

<span data-ttu-id="07b45-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-142">Access type: Read-only</span></span>

<span data-ttu-id="07b45-143">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-143">Qualifiers: None</span></span>

<span data-ttu-id="07b45-144">Percorso del file originale del file OSD registrato con il client App-V.</span><span class="sxs-lookup"><span data-stu-id="07b45-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="07b45-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="07b45-145">CachedOsdPath</span></span>**  
<span data-ttu-id="07b45-146">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="07b45-146">Data type: **String**</span></span>

<span data-ttu-id="07b45-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b45-147">Access type: Read-only</span></span>

<span data-ttu-id="07b45-148">Qualificatori: nessuno</span><span class="sxs-lookup"><span data-stu-id="07b45-148">Qualifiers: None</span></span>

<span data-ttu-id="07b45-149">Il percorso del file OSD se il client App-V ha memorizzato la cache del file OSD localmente.</span><span class="sxs-lookup"><span data-stu-id="07b45-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





