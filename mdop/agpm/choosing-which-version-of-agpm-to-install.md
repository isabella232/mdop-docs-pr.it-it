---
title: Scelta della versione di Gestione avanzata Criteri di gruppo da installare
description: Scelta della versione di Gestione avanzata Criteri di gruppo da installare
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819096"
---
# <span data-ttu-id="c924c-103">Scelta della versione di Gestione avanzata Criteri di gruppo da installare</span><span class="sxs-lookup"><span data-stu-id="c924c-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="c924c-104">Ogni versione di MicrosoftAdvanced (Advanced Group Policy Management) supporta versioni specifiche del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="c924c-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="c924c-105">Ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="c924c-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="c924c-106">Ad esempio, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="c924c-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="c924c-107">È consigliabile installare il server Advanced Group Policy Management nella versione più recente del sistema operativo nel dominio.</span><span class="sxs-lookup"><span data-stu-id="c924c-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="c924c-108">Advanced Group Policy Management (GPMC) usa la console Gestione criteri di gruppo per eseguire il backup e il ripristino degli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c924c-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="c924c-109">Poiché le versioni più recenti di GPMC includono altre impostazioni dei criteri che non sono disponibili nelle versioni precedenti, è possibile gestire altre impostazioni dei criteri usando la versione più recente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c924c-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="c924c-110">Tutte le versioni di Advanced Group Policy Management sono in grado di gestire solo le impostazioni dei criteri introdotte nella stessa versione o in una versione precedente del sistema operativo in cui è in esecuzione Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c924c-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="c924c-111">Ad esempio, se si installa Advanced Group Policy Management 4.0 SP2 in Windows Server 2012, è possibile gestire le impostazioni dei criteri introdotte in Windows Server 2012 o versioni precedenti, ma non è possibile gestire le impostazioni dei criteri introdotte in un secondo momento, in Windows 8.1 o Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c924c-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="c924c-112">Se la versione di GPMC nel server Advanced Group Policy Management è precedente alla versione nei computer usati dagli amministratori per gestire i criteri di gruppo, il server Advanced Group Policy Management non sarà in grado di archiviare le impostazioni dei criteri non disponibili nella versione precedente di GPMC.</span><span class="sxs-lookup"><span data-stu-id="c924c-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="c924c-113">Per il foglio di calcolo delle impostazioni di Criteri di gruppo incluso in Windows, vedi [Informazioni di riferimento per le impostazioni di Criteri di gruppo per Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="c924c-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="c924c-114">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c924c-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="c924c-115">Se si usano computer che eseguono Windows 10 per gestire i GPO, è necessario usare Advanced Group Policy Management 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c924c-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="c924c-116">Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono il sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c924c-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="c924c-117">La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP3 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c924c-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="c924c-118">Tabella 1: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c924c-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c924c-119">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-120">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-121">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="c924c-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-122">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="c924c-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-123">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="c924c-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="c924c-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-126">Windows10</span><span class="sxs-lookup"><span data-stu-id="c924c-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-127">Supportato con i caveat delineati in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="c924c-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-128">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-129">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-131">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-132">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="c924c-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-133">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-134">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-135">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-136">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-137">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-138">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c924c-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-139">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-140">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-141">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-142">Non supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-143">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-144">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-145">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c924c-146">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="c924c-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="c924c-147">Se si usano computer che eseguono Windows Server2012 R2 o Windows 8.1 per gestire i GPO, è necessario usare Advanced Group Policy Management 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c924c-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="c924c-148">Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono tali sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="c924c-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="c924c-149">La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP2 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c924c-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="c924c-150">Tabella 2: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="c924c-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c924c-151">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-152">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-153">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="c924c-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-154">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-155">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-156">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-157">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-158">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="c924c-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-159">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-160">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-161">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-162">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c924c-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-163">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-164">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c924c-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-165">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-166">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-167">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-168">Non supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-169">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-170">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-171">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c924c-172">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="c924c-173">La tabella 2 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 SP1 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c924c-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="c924c-174">Tabella 3: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c924c-175">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-176">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c924c-177">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="c924c-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c924c-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c924c-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-180">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-181">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-182">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-183">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="c924c-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-184">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-185">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-186">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-187">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-188">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-189">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-191">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-192">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c924c-193">Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="c924c-193">AGPM4.0</span></span>


<span data-ttu-id="c924c-194">La tabella 3 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0.</span><span class="sxs-lookup"><span data-stu-id="c924c-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="c924c-195">Tabella 4: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="c924c-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c924c-196">Sistemi operativi supportati per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="c924c-197">Sistemi operativi supportati per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c924c-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="c924c-198">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="c924c-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-199">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-200">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-201">Supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-202">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-203">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-204">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-205">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-206">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-207">Non supportato</span><span class="sxs-lookup"><span data-stu-id="c924c-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-208">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-209">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-210">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c924c-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c924c-211">Versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="c924c-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="c924c-212">La tabella 4 elenca i sistemi operativi in cui è possibile installare le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0.</span><span class="sxs-lookup"><span data-stu-id="c924c-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="c924c-213">Se un sistema operativo non è elencato, non è possibile installare Advanced Group Policy Management in tale sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c924c-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="c924c-214">Tabella 5: sistemi operativi supportati per le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="c924c-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c924c-215">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c924c-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c924c-216">Versione di Advanced Group Policy Management che può essere installata</span><span class="sxs-lookup"><span data-stu-id="c924c-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-217">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="c924c-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-218">3,0</span><span class="sxs-lookup"><span data-stu-id="c924c-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-219">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c924c-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-220">3,0</span><span class="sxs-lookup"><span data-stu-id="c924c-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c924c-221">WindowsVista con nessun Service Pack installato (32 bit)</span><span class="sxs-lookup"><span data-stu-id="c924c-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-222">2,5</span><span class="sxs-lookup"><span data-stu-id="c924c-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c924c-223">Windows Server2003 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="c924c-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c924c-224">2,5</span><span class="sxs-lookup"><span data-stu-id="c924c-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c924c-225">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="c924c-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="c924c-226">Advanced Group Policy Management 4,0 SP2 fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c924c-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c924c-227">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="c924c-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="c924c-228">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="c924c-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="c924c-229">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c924c-229">Related topics</span></span>


[<span data-ttu-id="c924c-230">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c924c-230">Advanced Group Policy Management</span></span>](index.md)

 

 





