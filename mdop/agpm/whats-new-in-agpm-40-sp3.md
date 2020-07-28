---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP3
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895766"
---
# <span data-ttu-id="6fd99-103">Novità di Gestione avanzata Criteri di gruppo 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6fd99-103">What's New in AGPM 4.0 SP3</span></span>


<span data-ttu-id="6fd99-104">Questo contenuto descrive i miglioramenti e le configurazioni supportate per il servizio Pack3 (Advanced Group Policy Management) 4.0 (SP3).</span><span class="sxs-lookup"><span data-stu-id="6fd99-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="6fd99-105">Se c'è una differenza tra questo contenuto e altre documentazioni di Advanced Group Policy Management, considera questo contenuto autorevole e presupponga che sostituisca l'altra documentazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="6fd99-106">Novità</span><span class="sxs-lookup"><span data-stu-id="6fd99-106">What’s new</span></span>


<span data-ttu-id="6fd99-107">Advanced Group Policy Management 4.0 SP3 supporta le caratteristiche e le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="6fd99-107">AGPM4.0 SP3 supports the following features and functionality.</span></span>

### <span data-ttu-id="6fd99-108">Supporto per Windows10</span><span class="sxs-lookup"><span data-stu-id="6fd99-108">Support for Windows10</span></span>

<span data-ttu-id="6fd99-109">Advanced Group Policy Management 4.0 SP3 aggiunge il supporto per i sistemi operativi Windows10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="6fd99-109">AGPM4.0 SP3 adds support for the Windows10 and Windows Server 2016 operating systems.</span></span>

### <span data-ttu-id="6fd99-110">Supporto per PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fd99-110">Support for PowerShell</span></span>

<span data-ttu-id="6fd99-111">Advanced Group Policy Management 4.0 SP3 aggiunge il supporto per i cmdlet di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fd99-111">AGPM4.0 SP3 adds support for PowerShell cmdlets.</span></span> <span data-ttu-id="6fd99-112">Per un elenco dei cmdlet disponibili in Advanced Group Policy Management 4.0 SP3, incluse le descrizioni e la sintassi, vedere [automazione di Microsoft Desktop Optimization Pack con Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span><span class="sxs-lookup"><span data-stu-id="6fd99-112">For a list of the cmdlets available in AGPM4.0 SP3, including descriptions and syntax, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span></span>

### <span data-ttu-id="6fd99-113">Feedback dei clienti e aggiornamento cumulativo</span><span class="sxs-lookup"><span data-stu-id="6fd99-113">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="6fd99-114">Advanced Group Policy Management 4,0 SP3 include un rollup di tutte le correzioni fino a Microsoft Advanced Group Policy Manager 4,0 SP2 e tutte le correzioni per i problemi rilevati da Advanced Management Packers 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="6fd99-114">AGPM 4.0 SP3 includes a rollup of all fixes up to and including Microsoft Advanced Group Policy Management 4.0 SP2 and any fixes for issues found since AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="6fd99-115">Possibilità di eseguire l'aggiornamento a Advanced Group Policy Management 4.0 SP3 senza immettere di nuovo i parametri di configurazione</span><span class="sxs-lookup"><span data-stu-id="6fd99-115">Ability to upgrade to AGPM4.0 SP3 without re-entering configuration parameters</span></span>

<span data-ttu-id="6fd99-116">È possibile aggiornare il client Advanced Group Policy Management o il server Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP3 senza che venga chiesto di immettere di nuovo i parametri di configurazione, detti Smart Upgrade, solo da Advanced Group Policy Management 4.0 e versioni successive, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6fd99-116">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP3 without being prompted to re-enter configuration parameters (called the Smart Upgrade) only from AGPM4.0 and later, as shown in the following table.</span></span> <span data-ttu-id="6fd99-117">Se si esegue l'aggiornamento a Advanced Group Policy Management 4.0 SP3 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'aggiornamento classico, che richiede di immettere di nuovo i parametri di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-117">If you are upgrading to AGPM4.0 SP3 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="6fd99-118">Poiché ogni versione di Advanced Group Policy Management è associata a un particolare sistema operativo, vedere [scelta della versione di Advanced Group Policy per l'installazione](https://go.microsoft.com/fwlink/?LinkId=254350) e verificare che il sistema operativo venga aggiornato in modo appropriato prima di aggiornare Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="6fd99-118">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="6fd99-119">Aggiornamenti supportati per Advanced Group Policy Management SP3 4,0</span><span class="sxs-lookup"><span data-stu-id="6fd99-119">AGPM 4.0 SP3 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6fd99-120">Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6fd99-120">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-121">2,5</span><span class="sxs-lookup"><span data-stu-id="6fd99-121">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-122">3,0</span><span class="sxs-lookup"><span data-stu-id="6fd99-122">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-123">4,0</span><span class="sxs-lookup"><span data-stu-id="6fd99-123">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-124">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6fd99-124">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-125">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6fd99-125">4.0 SP2</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6fd99-126">4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6fd99-126">4.0 SP3</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-127">2,5</span><span class="sxs-lookup"><span data-stu-id="6fd99-127">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-128">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-128">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-129">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="6fd99-129">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-130">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="6fd99-130">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-131">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-131">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-132">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-132">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-133">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-133">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-134">3,0</span><span class="sxs-lookup"><span data-stu-id="6fd99-134">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-135">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-135">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-136">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-136">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-137">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="6fd99-137">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-138">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-138">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-139">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-139">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-140">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="6fd99-140">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-141">4,0</span><span class="sxs-lookup"><span data-stu-id="6fd99-141">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-142">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-142">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-143">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-143">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-144">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-144">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-145">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-145">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-146">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-146">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-147">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-147">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6fd99-148">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-149">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-149">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-150">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-150">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-151">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-152">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-152">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-153">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-153">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-154">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-154">Smart Upgrade</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-155">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6fd99-155">4.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-156">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-156">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-157">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-158">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-159">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-159">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-160">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="6fd99-160">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-161">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="6fd99-161">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6fd99-162">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="6fd99-162">Supported configurations</span></span>


<span data-ttu-id="6fd99-163">Advanced Group Policy Management 4.0 SP3 supporta le configurazioni nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6fd99-163">AGPM4.0 SP3 supports the configurations in the following table.</span></span> <span data-ttu-id="6fd99-164">Anche se Advanced Group Policy Management supporta configurazioni miste, ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistema operativo, ad esempio Windows10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="6fd99-164">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

**<span data-ttu-id="6fd99-165">Sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6fd99-165">AGPM4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="6fd99-166">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="6fd99-166">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6fd99-167">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="6fd99-167">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6fd99-168">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="6fd99-168">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-169">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="6fd99-169">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-170">Windows10</span><span class="sxs-lookup"><span data-stu-id="6fd99-170">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-171">Supportato</span><span class="sxs-lookup"><span data-stu-id="6fd99-171">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-172">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="6fd99-172">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-173">Windows10</span><span class="sxs-lookup"><span data-stu-id="6fd99-173">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-174">Supportato</span><span class="sxs-lookup"><span data-stu-id="6fd99-174">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-175">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-175">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-176">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-176">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-177">Supportato</span><span class="sxs-lookup"><span data-stu-id="6fd99-177">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-178">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-178">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fd99-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-180">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-180">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-181">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-182">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-183">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-183">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-184">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-185">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="6fd99-185">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-186">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6fd99-187">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="6fd99-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-188">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-189">Non supportato</span><span class="sxs-lookup"><span data-stu-id="6fd99-189">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6fd99-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="6fd99-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-191">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="6fd99-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6fd99-192">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="6fd99-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6fd99-193">Prerequisiti per l'installazione di Advanced Group Policy Management 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6fd99-193">Prerequisites for installing AGPM4.0 SP3</span></span>

<span data-ttu-id="6fd99-194">La tabella seguente descrive il comportamento dei programmi di installazione del client e del server di Advanced Group Policy Management 4.0 SP3 quando mancano le funzionalità di .NET Framework 4.5.1, PowerShell 3,0 o GPMC negli strumenti di amministrazione del server remoto.</span><span class="sxs-lookup"><span data-stu-id="6fd99-194">The following table describes the behavior of AGPM4.0 SP3 Client and Server installers when the .NET Framework4.5.1, PowerShell 3.0, or the GPMC in the Remote Server Administration Tools is missing.</span></span>

| <span data-ttu-id="6fd99-195">Client Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="6fd99-195">AGPM Client</span></span>            |                                                                                                 |                                                                            | <span data-ttu-id="6fd99-196">Server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="6fd99-196">AGPM Server</span></span>                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6fd99-197">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6fd99-197">Operating system</span></span>       | <span data-ttu-id="6fd99-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6fd99-198">.NET Framework</span></span>                                                                                  | <span data-ttu-id="6fd99-199">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fd99-199">PowerShell</span></span>                                                                 | <span data-ttu-id="6fd99-200">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="6fd99-200">Remote Server Administration Tools</span></span>                                              | <span data-ttu-id="6fd99-201">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6fd99-201">.NET Framework</span></span>                                                                                  | <span data-ttu-id="6fd99-202">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="6fd99-202">Remote Server Administration Tools</span></span>                                              |
| <span data-ttu-id="6fd99-203">Windows10</span><span class="sxs-lookup"><span data-stu-id="6fd99-203">Windows 10</span></span>             | <span data-ttu-id="6fd99-204">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-204">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-205">Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-205">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-206">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="6fd99-206">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-207">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-207">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-208">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="6fd99-208">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="6fd99-209">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6fd99-209">Windows 8.1</span></span>            | <span data-ttu-id="6fd99-210">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-210">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-211">Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-211">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-212">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="6fd99-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-213">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-213">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-214">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="6fd99-214">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="6fd99-215">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6fd99-215">Windows Server 2012 R2</span></span> | <span data-ttu-id="6fd99-216">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-216">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-217">Se PowerShell 3,0 non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-217">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-218">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-218">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   | <span data-ttu-id="6fd99-219">Se .NET Framework 4.5.1 non è abilitato o non è installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-219">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="6fd99-220">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6fd99-220">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   |

 

## <span data-ttu-id="6fd99-221">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="6fd99-221">How to Get MDOP Technologies</span></span>


<span data-ttu-id="6fd99-222">Advanced Group Policy Management 4,0 SP3 fa parte del Microsoft Desktop Optimization Pack (MDOP) a partire da MDOP 2015.</span><span class="sxs-lookup"><span data-stu-id="6fd99-222">AGPM 4.0 SP3 is a part of the Microsoft Desktop Optimization Pack (MDOP) since MDOP 2015.</span></span> <span data-ttu-id="6fd99-223">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="6fd99-223">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="6fd99-224">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="6fd99-224">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="6fd99-225">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fd99-225">Related topics</span></span>


[<span data-ttu-id="6fd99-226">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6fd99-226">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="6fd99-227">Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6fd99-227">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[<span data-ttu-id="6fd99-228">Scelta della versione di Gestione avanzata Criteri di gruppo da installare</span><span class="sxs-lookup"><span data-stu-id="6fd99-228">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





