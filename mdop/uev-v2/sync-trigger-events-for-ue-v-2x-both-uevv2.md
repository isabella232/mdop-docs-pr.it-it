---
title: Eventi di attivazione di sincronizzazione per UE-V 2.x
description: Eventi di attivazione di sincronizzazione per UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826796"
---
# <span data-ttu-id="1a7fc-103">Eventi di attivazione di sincronizzazione per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="1a7fc-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="1a7fc-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 consente di sincronizzare l'applicazione e le impostazioni di Windows in tutti i dispositivi collegati al dominio.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="1a7fc-105">*Gli eventi trigger di sincronizzazione* definiscono quando l'agente UE-V sincronizza queste impostazioni con il percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="1a7fc-106">UE-V 2 introduce un nuovo *metodo di sincronizzazione* denominato *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="1a7fc-107">Per altre informazioni sulla configurazione del metodo di sincronizzazione, vedere [metodi di sincronizzazione per UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="1a7fc-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="1a7fc-108">Eventi trigger di sincronizzazione di UE-V 2</span><span class="sxs-lookup"><span data-stu-id="1a7fc-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="1a7fc-109">La tabella seguente illustra gli eventi trigger per le applicazioni classiche e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1a7fc-110">Evento trigger UE-V 2</span><span class="sxs-lookup"><span data-stu-id="1a7fc-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1a7fc-111">SyncMethod = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="1a7fc-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1a7fc-112">SyncMethod = None</span><span class="sxs-lookup"><span data-stu-id="1a7fc-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1a7fc-113">Accesso di Windows</span><span class="sxs-lookup"><span data-stu-id="1a7fc-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1a7fc-114">Le impostazioni dell'applicazione e di Windows vengono importate nella cache locale dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="1a7fc-115">Vengono applicate le impostazioni di Windows asincrone </a> .</span><span class="sxs-lookup"><span data-stu-id="1a7fc-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-116">Le impostazioni di Windows sincrone verranno applicate durante il successivo accesso di Windows.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-117">Le impostazioni dell'applicazione verranno applicate all'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1a7fc-118">Le impostazioni dell'applicazione e di Windows vengono lette direttamente dal percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-119">Vengono applicate le impostazioni di Windows asincrone e sincrone.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-120">Le impostazioni dell'applicazione verranno applicate all'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1a7fc-121">Fine sessione di Windows</span><span class="sxs-lookup"><span data-stu-id="1a7fc-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-122">Archiviare le modifiche localmente e memorizzare nella cache e copiare le impostazioni di Windows asincrone e sincrone nel server della posizione di archiviazione delle impostazioni, se disponibile</span><span class="sxs-lookup"><span data-stu-id="1a7fc-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-123">Archiviare le modifiche nel percorso di archiviazione delle impostazioni di Windows asincrono e sincrono</span><span class="sxs-lookup"><span data-stu-id="1a7fc-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1a7fc-124">Windows Connect (RDP)/Sblocca</span><span class="sxs-lookup"><span data-stu-id="1a7fc-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-125">Sincronizza le impostazioni di Windows asincrone dalla posizione di archiviazione delle impostazioni alla cache locale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="1a7fc-126">Applicare le impostazioni di Windows memorizzate nella cache</span><span class="sxs-lookup"><span data-stu-id="1a7fc-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-127">Scaricare e applicare le impostazioni di Windows asincrone dalla posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="1a7fc-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1a7fc-128">Windows Disconnect (RDP)/Lock</span><span class="sxs-lookup"><span data-stu-id="1a7fc-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-129">Archiviare le modifiche delle impostazioni di Windows asincrone nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="1a7fc-130">Sincronizzare eventuali impostazioni di Windows asincrone dalla cache locale alla posizione di archiviazione delle impostazioni, se disponibile</span><span class="sxs-lookup"><span data-stu-id="1a7fc-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-131">Archiviare le impostazioni di Windows asincrone nella posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="1a7fc-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1a7fc-132">Inizio applicazione</span><span class="sxs-lookup"><span data-stu-id="1a7fc-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-133">Applicare le impostazioni dell'applicazione dalla cache locale durante l'avvio dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1a7fc-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-134">Applicare le impostazioni dell'applicazione dalla posizione di archiviazione delle impostazioni durante l'avvio dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1a7fc-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1a7fc-135">Applicazione chiusa</span><span class="sxs-lookup"><span data-stu-id="1a7fc-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-136">Archiviare eventuali modifiche delle impostazioni dell'applicazione nella cache locale e copiare le impostazioni nella posizione di archiviazione delle impostazioni, se disponibile</span><span class="sxs-lookup"><span data-stu-id="1a7fc-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-137">Archiviare le modifiche delle impostazioni dell'applicazione nella posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="1a7fc-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1a7fc-138">L'attività pianificata del controller di sincronizzazione o "Sincronizza ora" viene eseguita dal centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="1a7fc-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-139">Le impostazioni dell'applicazione e di Windows vengono sincronizzate tra la posizione di archiviazione delle impostazioni e la cache locale.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1a7fc-140">Nota</span><span class="sxs-lookup"><span data-stu-id="1a7fc-140">Note</span></span></strong><br/><p><span data-ttu-id="1a7fc-141">Le modifiche alle impostazioni non vengono memorizzate nella cache locale finché non viene chiusa un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="1a7fc-142">Questo trigger non esporterà le modifiche apportate a un'applicazione attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="1a7fc-143">Per le impostazioni di Windows, ciò significa che le eventuali modifiche non verranno memorizzate nella cache localmente ed esportate fino al blocco successivo (asincrono) o alla disconnessione (asincrono e sincrono).</span><span class="sxs-lookup"><span data-stu-id="1a7fc-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="1a7fc-144">Le impostazioni vengono applicate in questi casi:</span><span class="sxs-lookup"><span data-stu-id="1a7fc-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="1a7fc-145">Le impostazioni di Windows asincrone vengono applicate direttamente.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-146">Le impostazioni dell'applicazione vengono applicate all'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-147">Le impostazioni di Windows asincrone e sincrone vengono applicate durante l'accesso successivo di Windows.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="1a7fc-148">Le impostazioni dell'app Windows (AppX) vengono applicate durante l'aggiornamento successivo.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="1a7fc-149"><a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Per altre informazioni, vedere monitorare le impostazioni dell'applicazione </a> .</span><span class="sxs-lookup"><span data-stu-id="1a7fc-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1a7fc-150">N/D</span><span class="sxs-lookup"><span data-stu-id="1a7fc-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1a7fc-151">Impostazioni asincrone aggiornate in un archivio remoto \*</span><span class="sxs-lookup"><span data-stu-id="1a7fc-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-152">Caricare e applicare nuove impostazioni asincrone dalla cache.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a7fc-153">Caricare e applicare le impostazioni da server centrale</span><span class="sxs-lookup"><span data-stu-id="1a7fc-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="1a7fc-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a7fc-154">Related topics</span></span>


[<span data-ttu-id="1a7fc-155">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="1a7fc-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="1a7fc-156">Modifica della frequenza delle attività pianificate di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1a7fc-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="1a7fc-157">Scegliere il metodo di configurazione per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1a7fc-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









