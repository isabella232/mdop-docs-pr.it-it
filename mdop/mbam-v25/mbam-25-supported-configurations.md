---
title: Configurazioni supportate di MBAM 2.5
description: Configurazioni supportate di MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182928"
---
# <span data-ttu-id="22705-103">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22705-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="22705-104">È possibile eseguire Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una topologia autonoma o in una topologia di integrazione di Configuration Manager che si integra con MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="22705-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="22705-105">Se si usa la configurazione consigliata per una topologia in un ambiente di produzione, MBAM supporta fino a 500.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="22705-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="22705-106">Per informazioni sull'architettura e le funzionalità consigliate configurate in ogni server per ogni topologia, vedere [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="22705-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="22705-107">Per altre configurazioni specifiche della topologia di integrazione di Configuration Manager, vedere [versioni di Configuration Manager supportate da mbam](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="22705-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="22705-108">Nota</span><span class="sxs-lookup"><span data-stu-id="22705-108">Note</span></span>**  
<span data-ttu-id="22705-109">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="22705-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="22705-110">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="22705-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="22705-111">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22705-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="22705-112">Lingue supportate da MBAM</span><span class="sxs-lookup"><span data-stu-id="22705-112">MBAM Supported Languages</span></span>


<span data-ttu-id="22705-113">Le tabelle seguenti mostrano le lingue supportate per il client MBAM (incluso il portale Self-Service) e il server MBAM in MBAM 2,5 e MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="22705-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="22705-114">Lingue supportate in MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="22705-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-115">Lingue client</span><span class="sxs-lookup"><span data-stu-id="22705-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="22705-116">Lingue del server</span><span class="sxs-lookup"><span data-stu-id="22705-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-117">Ceco (Repubblica Ceca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="22705-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="22705-118">Danese (Danimarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="22705-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="22705-119">Olandese (Paesi Bassi) nl-NL</span><span class="sxs-lookup"><span data-stu-id="22705-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="22705-120">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="22705-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="22705-121">Fi-FI Finlandese (Finlandia)</span><span class="sxs-lookup"><span data-stu-id="22705-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="22705-122">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="22705-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="22705-123">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="22705-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="22705-124">Greco (Grecia) el-GR</span><span class="sxs-lookup"><span data-stu-id="22705-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="22705-125">Ungherese (Ungheria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="22705-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="22705-126">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="22705-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="22705-127">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="22705-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="22705-128">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="22705-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="22705-129">Norvegese, Bokmål (Norvegia) nb-NO</span><span class="sxs-lookup"><span data-stu-id="22705-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="22705-130">Polacco (Polonia) PL-PL</span><span class="sxs-lookup"><span data-stu-id="22705-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="22705-131">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="22705-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="22705-132">Portoghese (Portogallo) PT-PT</span><span class="sxs-lookup"><span data-stu-id="22705-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="22705-133">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="22705-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="22705-134">Slovacco (Slovacchia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="22705-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="22705-135">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="22705-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="22705-136">Svedese (Svezia) SV-SE</span><span class="sxs-lookup"><span data-stu-id="22705-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="22705-137">Turco (Turchia) tr-TR</span><span class="sxs-lookup"><span data-stu-id="22705-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="22705-138">Sloveno (Slovenia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="22705-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="22705-139">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="22705-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="22705-140">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="22705-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-141">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="22705-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="22705-142">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="22705-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="22705-143">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="22705-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="22705-144">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="22705-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="22705-145">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="22705-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="22705-146">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="22705-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="22705-147">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="22705-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="22705-148">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="22705-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="22705-149">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="22705-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="22705-150">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="22705-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="22705-151">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="22705-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="22705-152">Lingue supportate in MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="22705-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-153">Lingue client</span><span class="sxs-lookup"><span data-stu-id="22705-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="22705-154">Lingue del server</span><span class="sxs-lookup"><span data-stu-id="22705-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="22705-155">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="22705-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="22705-156">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="22705-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="22705-157">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="22705-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="22705-158">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="22705-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="22705-159">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="22705-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="22705-160">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="22705-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="22705-161">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="22705-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="22705-162">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="22705-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="22705-163">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="22705-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="22705-164">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="22705-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="22705-165">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="22705-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-166">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="22705-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="22705-167">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="22705-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="22705-168">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="22705-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="22705-169">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="22705-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="22705-170">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="22705-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="22705-171">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="22705-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="22705-172">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="22705-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="22705-173">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="22705-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="22705-174">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="22705-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="22705-175">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="22705-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="22705-176">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="22705-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="22705-177">Requisiti di sistema di MBAM server</span><span class="sxs-lookup"><span data-stu-id="22705-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="22705-178">Requisiti del sistema operativo di MBAM server</span><span class="sxs-lookup"><span data-stu-id="22705-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="22705-179">Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="22705-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="22705-180">Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22705-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="22705-181">La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="22705-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-182">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="22705-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="22705-183">Edizione</span><span class="sxs-lookup"><span data-stu-id="22705-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="22705-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="22705-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="22705-185">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="22705-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-186">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="22705-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-187">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="22705-188">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="22705-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-190">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="22705-191">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-192">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="22705-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-193">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-194">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22705-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-196">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="22705-197">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-198">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="22705-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-199">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-200">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-201">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="22705-202">Il dominio aziendale deve contenere almeno un controller di dominio di Windows Server 2008 (o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="22705-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="22705-203">Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="22705-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="22705-204">Questi requisiti sono per la topologia autonoma di MBAM.</span><span class="sxs-lookup"><span data-stu-id="22705-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="22705-205">Per i requisiti della topologia di integrazione di Configuration Manager, vedi la topologia di integrazione di gestione configurazione, per i requisiti di [Disk Processor, RAM e spazio su disco](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="22705-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-206">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="22705-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="22705-207">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="22705-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="22705-208">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="22705-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-209">Processore</span><span class="sxs-lookup"><span data-stu-id="22705-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-210">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="22705-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-211">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="22705-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-212">RAM</span><span class="sxs-lookup"><span data-stu-id="22705-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-213">8 GB</span><span class="sxs-lookup"><span data-stu-id="22705-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-214">12 GB</span><span class="sxs-lookup"><span data-stu-id="22705-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-215">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="22705-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-216">1 GB</span><span class="sxs-lookup"><span data-stu-id="22705-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-217">2 GB</span><span class="sxs-lookup"><span data-stu-id="22705-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="22705-218">Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="22705-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="22705-219">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco per i server MBAM quando si usa la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="22705-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="22705-220">Per i requisiti per la topologia autonoma, vedere [requisiti per il processore, la RAM e lo spazio su disco di mbam server-topologia](#bkmk-stand-alone-ramreqs)autonoma.</span><span class="sxs-lookup"><span data-stu-id="22705-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-221">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="22705-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="22705-222">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="22705-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="22705-223">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="22705-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-224">Processore</span><span class="sxs-lookup"><span data-stu-id="22705-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-225">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="22705-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-226">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="22705-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-227">RAM</span><span class="sxs-lookup"><span data-stu-id="22705-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-228">4 GB</span><span class="sxs-lookup"><span data-stu-id="22705-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-229">8 GB</span><span class="sxs-lookup"><span data-stu-id="22705-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-230">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="22705-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-231">1 GB</span><span class="sxs-lookup"><span data-stu-id="22705-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="22705-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="22705-233">Versioni di Configuration Manager supportate da MBAM</span><span class="sxs-lookup"><span data-stu-id="22705-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="22705-234">MBAM supporta le versioni seguenti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="22705-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-235">Versione supportata</span><span class="sxs-lookup"><span data-stu-id="22705-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="22705-236">Service Pack</span><span class="sxs-lookup"><span data-stu-id="22705-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="22705-237">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="22705-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-238">Microsoft System Center Configuration Manager (Current Branch), versioni fino a 1902</span><span class="sxs-lookup"><span data-stu-id="22705-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-239">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="22705-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-241">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-242">Microsoft System Center Configuration Manager (LTSB-versione 1606)</span><span class="sxs-lookup"><span data-stu-id="22705-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-243">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-244">Gestione configurazione di Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="22705-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-245">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-246">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-247">Microsoft System Center Configuration Manager 2007 R2 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="22705-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-248">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-248">64-bit</span></span></p>

<span data-ttu-id="22705-249">&gt;<strong>Nota </strong> anche se Configuration Manager 2007 R2 è 32 bit, è necessario installarlo e SQL Server in un sistema operativo a 64 bit per far corrispondere il software mbam a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="22705-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="22705-250">Per un elenco delle configurazioni supportate per il Server Configuration Manager, vedere la documentazione appropriata di TechNet per la versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="22705-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="22705-251">MBAM non ha requisiti di sistema aggiuntivi per il Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="22705-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="22705-252">Requisiti di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="22705-252">SQL Server database requirements</span></span>

<span data-ttu-id="22705-253">Nella tabella seguente sono elencate le versioni di Microsoft SQL Server supportate per le funzionalità di MBAM server, che includono il database di ripristino, la conformità e il database di audit e la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="22705-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="22705-254">Le versioni necessarie si applicano alle topologie di integrazione autonoma o Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="22705-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="22705-255">È necessario installare SQL Server con **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="22705-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-256">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="22705-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="22705-257">Edizione</span><span class="sxs-lookup"><span data-stu-id="22705-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="22705-258">Service Pack</span><span class="sxs-lookup"><span data-stu-id="22705-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="22705-259">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="22705-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="22705-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-261">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-262">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="22705-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="22705-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-264">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-265">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="22705-266">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="22705-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-267">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-268">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="22705-269">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="22705-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-271">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="22705-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-273">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="22705-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-275">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-276">SP3</span><span class="sxs-lookup"><span data-stu-id="22705-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-277">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22705-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-279">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="22705-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-280">SP3</span><span class="sxs-lookup"><span data-stu-id="22705-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-281">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="22705-282">Nota</span><span class="sxs-lookup"><span data-stu-id="22705-282">Note</span></span>**  
<span data-ttu-id="22705-283">MBAM ha un livello di compatibilità supportato massimo di 140.</span><span class="sxs-lookup"><span data-stu-id="22705-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="22705-284">Il livello di compatibilità predefinito per i nuovi database creati in SQL Server 2019 è 150 che deve essere modificato in 140 o inferiore, usando il comando ALTER DATABASE, dopo la creazione del database.</span><span class="sxs-lookup"><span data-stu-id="22705-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="22705-285">I database esistenti migrati da SQL Server 2017 o inferiore rimarranno al livello di compatibilità precedente e non devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="22705-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="22705-286">Per supportare SQL 2016, è necessario installare la versione di manutenzione di marzo 2017 per MDOP https://www.microsoft.com/download/details.aspx?id=54967  e per supportare sql 2017 è necessario installare la versione di manutenzione di luglio 2018 per MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="22705-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="22705-287">In generale, è possibile usare sempre l'aggiornamento della manutenzione più recente, poiché include anche tutti i bug e le nuove caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="22705-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="22705-288">Requisiti di spazio per processori, RAM e spazi su disco di SQL Server-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="22705-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="22705-289">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco consigliati per il computer SQL Server quando si usa la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="22705-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="22705-290">Usare questi requisiti come guida.</span><span class="sxs-lookup"><span data-stu-id="22705-290">Use these requirements as a guide.</span></span> <span data-ttu-id="22705-291">I requisiti specifici variano in base al numero di computer client supportati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="22705-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="22705-292">Per visualizzare i requisiti per la topologia di integrazione di Configuration Manager, vedere [requisiti relativi a SQL Server Processor, RAM e spazio su disco-topologia di integrazione di Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="22705-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-293">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="22705-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="22705-294">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="22705-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="22705-295">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="22705-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-296">Processore</span><span class="sxs-lookup"><span data-stu-id="22705-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-297">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="22705-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-298">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="22705-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-299">RAM</span><span class="sxs-lookup"><span data-stu-id="22705-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-300">8 GB</span><span class="sxs-lookup"><span data-stu-id="22705-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-301">12 GB</span><span class="sxs-lookup"><span data-stu-id="22705-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-302">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="22705-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-303">5 GB</span><span class="sxs-lookup"><span data-stu-id="22705-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-304">5 GB o superiore</span><span class="sxs-lookup"><span data-stu-id="22705-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="22705-305">Requisiti di spazio su processori, RAM e Space disk per SQL Server-topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="22705-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="22705-306">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco del server per il computer Microsoft SQL Server quando si usa la topologia di integrazione di Configuration Manager, vedere Requisiti per la [topologia autonoma di processori, RAM e spazio su disco di SQL Server](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="22705-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-307">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="22705-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="22705-308">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="22705-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="22705-309">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="22705-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-310">Processore</span><span class="sxs-lookup"><span data-stu-id="22705-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-311">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="22705-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-312">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="22705-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-313">RAM</span><span class="sxs-lookup"><span data-stu-id="22705-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-314">4 GB</span><span class="sxs-lookup"><span data-stu-id="22705-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-315">8 GB</span><span class="sxs-lookup"><span data-stu-id="22705-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-316">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="22705-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-317">5 GB</span><span class="sxs-lookup"><span data-stu-id="22705-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-318">5 GB</span><span class="sxs-lookup"><span data-stu-id="22705-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="22705-319">Requisiti di sistema client di MBAM</span><span class="sxs-lookup"><span data-stu-id="22705-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="22705-320">Requisiti del sistema operativo client</span><span class="sxs-lookup"><span data-stu-id="22705-320">Client operating system requirements</span></span>

<span data-ttu-id="22705-321">Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="22705-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="22705-322">Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="22705-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="22705-323">La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="22705-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="22705-324">Gli stessi requisiti si applicano alle topologie di integrazione autonoma e gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="22705-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-325">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="22705-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="22705-326">Edizione</span><span class="sxs-lookup"><span data-stu-id="22705-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="22705-327">Service Pack</span><span class="sxs-lookup"><span data-stu-id="22705-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="22705-328">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="22705-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="22705-329">Windows 10</span><span class="sxs-lookup"><span data-stu-id="22705-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="22705-330">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="22705-331">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="22705-332">Windows10</span><span class="sxs-lookup"><span data-stu-id="22705-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-333">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-334">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="22705-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-336">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-337">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-338">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22705-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-339">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="22705-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-340">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-341">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-342">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="22705-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-343">Windows 8,1 e Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="22705-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-344">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="22705-345">Requisiti di RAM client</span><span class="sxs-lookup"><span data-stu-id="22705-345">Client RAM requirements</span></span>

<span data-ttu-id="22705-346">Non ci sono requisiti di RAM specifici per l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="22705-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="22705-347">Requisiti di sistema per i criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="22705-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="22705-348">La tabella seguente elenca i sistemi operativi supportati per l'installazione dei modelli di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="22705-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22705-349">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="22705-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="22705-350">Edizione</span><span class="sxs-lookup"><span data-stu-id="22705-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="22705-351">Service Pack</span><span class="sxs-lookup"><span data-stu-id="22705-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="22705-352">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="22705-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="22705-353">Windows 10</span><span class="sxs-lookup"><span data-stu-id="22705-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="22705-354">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="22705-355">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-356">Windows10</span><span class="sxs-lookup"><span data-stu-id="22705-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-357">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-358">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="22705-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-360">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="22705-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-361">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-362">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22705-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-363">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="22705-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-364">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-365">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-366">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="22705-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-367">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-368">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22705-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-370">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="22705-371">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-372">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="22705-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-373">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="22705-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-374">SP1</span><span class="sxs-lookup"><span data-stu-id="22705-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-375">64 bit</span><span class="sxs-lookup"><span data-stu-id="22705-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="22705-376">MBAM in Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="22705-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="22705-377">Il server MBAM può essere distribuito in un'infrastruttura di Azure come servizio (IaaS) in una delle versioni supportate del sistema operativo elencate sopra, che si connettono a una directory ospitata in locale o in Active Directory ospitata anche in Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="22705-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="22705-378">La documentazione relativa alla configurazione e alla configurazione di Active Directory in Azure IaaS è disponibile [qui](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="22705-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="22705-379">Il client MBAM non è supportato nelle macchine virtuali e non è supportato anche in Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="22705-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="22705-380">Versioni di servizio</span><span class="sxs-lookup"><span data-stu-id="22705-380">Service releases</span></span> 

- [<span data-ttu-id="22705-381">Hotfix 2016 aprile</span><span class="sxs-lookup"><span data-stu-id="22705-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="22705-382">2016 settembre</span><span class="sxs-lookup"><span data-stu-id="22705-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="22705-383">Dicembre 2016</span><span class="sxs-lookup"><span data-stu-id="22705-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="22705-384">Marzo 2017</span><span class="sxs-lookup"><span data-stu-id="22705-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="22705-385">Giugno 2017</span><span class="sxs-lookup"><span data-stu-id="22705-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="22705-386">Settembre 2017</span><span class="sxs-lookup"><span data-stu-id="22705-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="22705-387">Marzo 2018</span><span class="sxs-lookup"><span data-stu-id="22705-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="22705-388">2018 luglio</span><span class="sxs-lookup"><span data-stu-id="22705-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="22705-389">2019 maggio</span><span class="sxs-lookup"><span data-stu-id="22705-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="22705-390">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22705-390">Related topics</span></span>


[<span data-ttu-id="22705-391">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22705-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="22705-392">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22705-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="22705-393">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="22705-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="22705-394">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="22705-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="22705-395">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="22705-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




