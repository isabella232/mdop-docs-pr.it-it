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
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905603"
---
# <span data-ttu-id="42c5a-103">Scelta della versione di Gestione avanzata Criteri di gruppo da installare</span><span class="sxs-lookup"><span data-stu-id="42c5a-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="42c5a-104">Ogni versione di MicrosoftAdvanced (Advanced Group Policy Management) supporta versioni specifiche del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="42c5a-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="42c5a-105">Ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="42c5a-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="42c5a-106">Ad esempio, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="42c5a-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="42c5a-107">È consigliabile installare il server Advanced Group Policy Management nella versione più recente del sistema operativo nel dominio.</span><span class="sxs-lookup"><span data-stu-id="42c5a-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="42c5a-108">Advanced Group Policy Management (GPMC) usa la console Gestione criteri di gruppo per eseguire il backup e il ripristino degli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="42c5a-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="42c5a-109">Poiché le versioni più recenti di GPMC includono altre impostazioni dei criteri che non sono disponibili nelle versioni precedenti, è possibile gestire altre impostazioni dei criteri usando la versione più recente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42c5a-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="42c5a-110">Tutte le versioni di Advanced Group Policy Management sono in grado di gestire solo le impostazioni dei criteri introdotte nella stessa versione o in una versione precedente del sistema operativo in cui è in esecuzione Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="42c5a-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="42c5a-111">Ad esempio, se si installa Advanced Group Policy Management 4.0 SP2 in Windows Server 2012, è possibile gestire le impostazioni dei criteri introdotte in Windows Server 2012 o versioni precedenti, ma non è possibile gestire le impostazioni dei criteri introdotte in un secondo momento, in Windows 8.1 o Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="42c5a-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="42c5a-112">Se la versione di GPMC nel server Advanced Group Policy Management è precedente alla versione nei computer usati dagli amministratori per gestire i criteri di gruppo, il server Advanced Group Policy Management non sarà in grado di archiviare le impostazioni dei criteri non disponibili nella versione precedente di GPMC.</span><span class="sxs-lookup"><span data-stu-id="42c5a-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="42c5a-113">Per il foglio di calcolo delle impostazioni di Criteri di gruppo incluso in Windows, vedi [Informazioni di riferimento per le impostazioni di Criteri di gruppo per Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="42c5a-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="42c5a-114">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="42c5a-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="42c5a-115">Se si usano computer che eseguono Windows 10 per gestire i GPO, è necessario usare Advanced Group Policy Management 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="42c5a-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="42c5a-116">Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono il sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42c5a-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="42c5a-117">La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP3 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="42c5a-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="42c5a-118">Tabella 1: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="42c5a-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="42c5a-119">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-120">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-121">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="42c5a-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-122">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="42c5a-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-123">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="42c5a-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-125">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="42c5a-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-126">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="42c5a-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="42c5a-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="42c5a-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-129">Windows10</span><span class="sxs-lookup"><span data-stu-id="42c5a-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-130">Supportato con i caveat delineati in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="42c5a-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-131">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-132">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-134">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-135">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="42c5a-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-136">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-137">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-138">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-139">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-140">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-141">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="42c5a-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-142">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-143">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-144">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-145">Non supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-146">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-147">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-148">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42c5a-149">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="42c5a-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="42c5a-150">Se si usano computer che eseguono Windows Server2012 R2 o Windows 8.1 per gestire i GPO, è necessario usare Advanced Group Policy Management 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="42c5a-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="42c5a-151">Non è possibile installare versioni precedenti di Advanced Group Policy Management nei computer che eseguono tali sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="42c5a-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="42c5a-152">La tabella 1 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4.0 SP2 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="42c5a-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="42c5a-153">Tabella 2: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="42c5a-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="42c5a-154">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-155">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-156">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="42c5a-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-157">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-158">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-159">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-160">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-161">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="42c5a-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-162">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-163">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-164">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-165">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="42c5a-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-166">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-167">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="42c5a-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-168">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-169">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-170">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-171">Non supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-172">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-173">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-174">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42c5a-175">ADVANCED GROUP POLICY MANAGEMENT 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="42c5a-176">La tabella 2 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 SP1 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="42c5a-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="42c5a-177">Tabella 3: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="42c5a-178">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-179">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="42c5a-180">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="42c5a-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42c5a-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42c5a-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-183">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-184">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-185">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-186">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="42c5a-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-187">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-188">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-189">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-191">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-192">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-193">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-194">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-195">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42c5a-196">Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="42c5a-196">AGPM4.0</span></span>


<span data-ttu-id="42c5a-197">La tabella 3 elenca i sistemi operativi in cui è possibile installare Advanced Group Policy Management 4,0 e le impostazioni dei criteri che è possibile gestire tramite Advanced Group Policy Management 4.0.</span><span class="sxs-lookup"><span data-stu-id="42c5a-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="42c5a-198">Tabella 4: sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="42c5a-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="42c5a-199">Sistemi operativi supportati per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="42c5a-200">Sistemi operativi supportati per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="42c5a-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="42c5a-201">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="42c5a-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-202">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-203">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-204">Supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-205">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-206">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-207">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-208">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-209">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-210">Non supportato</span><span class="sxs-lookup"><span data-stu-id="42c5a-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-211">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-212">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-213">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="42c5a-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42c5a-214">Versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="42c5a-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="42c5a-215">La tabella 4 elenca i sistemi operativi in cui è possibile installare le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0.</span><span class="sxs-lookup"><span data-stu-id="42c5a-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="42c5a-216">Se un sistema operativo non è elencato, non è possibile installare Advanced Group Policy Management in tale sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42c5a-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="42c5a-217">Tabella 5: sistemi operativi supportati per le versioni di Advanced Group Policy Management che precedono Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="42c5a-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="42c5a-218">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="42c5a-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="42c5a-219">Versione di Advanced Group Policy Management che può essere installata</span><span class="sxs-lookup"><span data-stu-id="42c5a-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="42c5a-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-221">3,0</span><span class="sxs-lookup"><span data-stu-id="42c5a-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-222">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="42c5a-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-223">3,0</span><span class="sxs-lookup"><span data-stu-id="42c5a-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42c5a-224">WindowsVista con nessun Service Pack installato (32 bit)</span><span class="sxs-lookup"><span data-stu-id="42c5a-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-225">2,5</span><span class="sxs-lookup"><span data-stu-id="42c5a-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42c5a-226">Windows Server2003 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="42c5a-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42c5a-227">2,5</span><span class="sxs-lookup"><span data-stu-id="42c5a-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42c5a-228">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="42c5a-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="42c5a-229">Advanced Group Policy Management 4,0 SP2 fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="42c5a-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="42c5a-230">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="42c5a-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="42c5a-231">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="42c5a-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="42c5a-232">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42c5a-232">Related topics</span></span>


[<span data-ttu-id="42c5a-233">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="42c5a-233">Advanced Group Policy Management</span></span>](index.md)

 

 





