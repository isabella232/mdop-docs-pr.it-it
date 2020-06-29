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
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823895"
---
# <span data-ttu-id="2f2a7-103">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2f2a7-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="2f2a7-104">È possibile eseguire Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una topologia autonoma o in una topologia di integrazione di Configuration Manager che si integra con MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="2f2a7-105">Se si usa la configurazione consigliata per una topologia in un ambiente di produzione, MBAM supporta fino a 500.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="2f2a7-106">Per informazioni sull'architettura e le funzionalità consigliate configurate in ogni server per ogni topologia, vedere [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="2f2a7-107">Per altre configurazioni specifiche della topologia di integrazione di Configuration Manager, vedere [versioni di Configuration Manager supportate da mbam](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="2f2a7-108">Nota</span><span class="sxs-lookup"><span data-stu-id="2f2a7-108">Note</span></span>**  
<span data-ttu-id="2f2a7-109">Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2f2a7-110">Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2f2a7-111">Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="2f2a7-112">Lingue supportate da MBAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-112">MBAM Supported Languages</span></span>


<span data-ttu-id="2f2a7-113">Le tabelle seguenti mostrano le lingue supportate per il client MBAM (incluso il portale self-service) e il server MBAM in MBAM 2,5 e MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="2f2a7-114">Lingue supportate in MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="2f2a7-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-115">Lingue client</span><span class="sxs-lookup"><span data-stu-id="2f2a7-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-116">Lingue del server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-117">Ceco (Repubblica Ceca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="2f2a7-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="2f2a7-118">Danese (Danimarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="2f2a7-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="2f2a7-119">Olandese (Paesi Bassi) nl-NL</span><span class="sxs-lookup"><span data-stu-id="2f2a7-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="2f2a7-120">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="2f2a7-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="2f2a7-121">Fi-FI Finlandese (Finlandia)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="2f2a7-122">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="2f2a7-123">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="2f2a7-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="2f2a7-124">Greco (Grecia) el-GR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="2f2a7-125">Ungherese (Ungheria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="2f2a7-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="2f2a7-126">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="2f2a7-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="2f2a7-127">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2f2a7-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="2f2a7-128">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="2f2a7-129">Norvegese, Bokmål (Norvegia) nb-NO</span><span class="sxs-lookup"><span data-stu-id="2f2a7-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="2f2a7-130">Polacco (Polonia) PL-PL</span><span class="sxs-lookup"><span data-stu-id="2f2a7-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="2f2a7-131">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="2f2a7-132">Portoghese (Portogallo) PT-PT</span><span class="sxs-lookup"><span data-stu-id="2f2a7-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="2f2a7-133">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="2f2a7-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="2f2a7-134">Slovacco (Slovacchia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="2f2a7-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="2f2a7-135">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="2f2a7-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="2f2a7-136">Svedese (Svezia) SV-SE</span><span class="sxs-lookup"><span data-stu-id="2f2a7-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="2f2a7-137">Turco (Turchia) tr-TR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="2f2a7-138">Sloveno (Slovenia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="2f2a7-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="2f2a7-139">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="2f2a7-140">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="2f2a7-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2f2a7-141">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="2f2a7-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-142">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-143">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="2f2a7-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-144">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="2f2a7-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-145">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2f2a7-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-146">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-147">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-148">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="2f2a7-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-149">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="2f2a7-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-150">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-151">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="2f2a7-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2f2a7-152">Lingue supportate in MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="2f2a7-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-153">Lingue client</span><span class="sxs-lookup"><span data-stu-id="2f2a7-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-154">Lingue del server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="2f2a7-155">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="2f2a7-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-156">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-157">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="2f2a7-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-158">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="2f2a7-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-159">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2f2a7-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-160">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-161">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-162">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="2f2a7-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-163">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="2f2a7-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-164">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-165">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="2f2a7-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2f2a7-166">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="2f2a7-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-167">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-168">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="2f2a7-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-169">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="2f2a7-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-170">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2f2a7-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-171">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-172">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="2f2a7-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-173">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="2f2a7-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-174">Spagnolo (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="2f2a7-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-175">Zh-CN (cinese semplificato)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2f2a7-176">Cinese tradizionale (Taiwan) ZH-TW</span><span class="sxs-lookup"><span data-stu-id="2f2a7-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="2f2a7-177">Requisiti di sistema di MBAM server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="2f2a7-178">Requisiti del sistema operativo di MBAM server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="2f2a7-179">Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="2f2a7-180">Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="2f2a7-181">La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-182">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-183">Edizione</span><span class="sxs-lookup"><span data-stu-id="2f2a7-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2f2a7-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-185">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2f2a7-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-186">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f2a7-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-187">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2f2a7-188">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-189">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-190">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-191">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-192">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f2a7-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-193">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2f2a7-194">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-195">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-196">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-197">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-198">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2f2a7-199">Il dominio aziendale deve contenere almeno un controller di dominio di Windows Server 2008 (o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="2f2a7-200">Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="2f2a7-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="2f2a7-201">Questi requisiti sono per la topologia autonoma di MBAM.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="2f2a7-202">Per i requisiti della topologia di integrazione di Configuration Manager, vedi la topologia di integrazione di gestione configurazione, per i requisiti di [Disk Processor, RAM e spazio su disco](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-203">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="2f2a7-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-204">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-205">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="2f2a7-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-206">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="2f2a7-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-207">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2f2a7-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-208">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="2f2a7-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-209">RAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-210">8 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-211">12 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-212">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="2f2a7-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-214">2 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="2f2a7-215">Requisiti per il processore, la RAM e lo spazio su disco di MBAM server-topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2f2a7-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="2f2a7-216">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco per i server MBAM quando si usa la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="2f2a7-217">Per i requisiti per la topologia autonoma, vedere [requisiti per il processore, la RAM e lo spazio su disco di mbam server-topologia](#bkmk-stand-alone-ramreqs)autonoma.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-218">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="2f2a7-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-219">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-220">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="2f2a7-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-221">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="2f2a7-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-222">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2f2a7-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-223">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="2f2a7-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-224">RAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-225">4 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-226">8 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-227">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="2f2a7-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-228">1 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-229">2 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="2f2a7-230">Versioni di Configuration Manager supportate da MBAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="2f2a7-231">MBAM supporta le versioni seguenti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-232">Versione supportata</span><span class="sxs-lookup"><span data-stu-id="2f2a7-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-233">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2f2a7-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-234">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2f2a7-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-235">Microsoft System Center Configuration Manager (Current Branch), versioni fino a 1902</span><span class="sxs-lookup"><span data-stu-id="2f2a7-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-236">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="2f2a7-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-238">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-239">Microsoft System Center Configuration Manager (LTSB-versione 1606)</span><span class="sxs-lookup"><span data-stu-id="2f2a7-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-240">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-241">Gestione configurazione di Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="2f2a7-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-242">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-243">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-244">Microsoft System Center Configuration Manager 2007 R2 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="2f2a7-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-245">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-245">64-bit</span></span></p>

<span data-ttu-id="2f2a7-246">&gt;<strong>Nota </strong> anche se Configuration Manager 2007 R2 è 32 bit, è necessario installarlo e SQL Server in un sistema operativo a 64 bit per far corrispondere il software mbam a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="2f2a7-247">Per un elenco delle configurazioni supportate per il Server Configuration Manager, vedere la documentazione appropriata di TechNet per la versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="2f2a7-248">MBAM non ha requisiti di sistema aggiuntivi per il Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="2f2a7-249">Requisiti di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-249">SQL Server database requirements</span></span>

<span data-ttu-id="2f2a7-250">Nella tabella seguente sono elencate le versioni di Microsoft SQL Server supportate per le funzionalità di MBAM server, che includono il database di ripristino, la conformità e il database di audit e la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="2f2a7-251">Le versioni necessarie si applicano alle topologie di integrazione autonoma o Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="2f2a7-252">È necessario installare SQL Server con **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-253">Versione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="2f2a7-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-254">Edizione</span><span class="sxs-lookup"><span data-stu-id="2f2a7-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-255">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2f2a7-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-256">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2f2a7-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="2f2a7-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-258">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-259">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-260">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f2a7-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-261">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-262">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="2f2a7-263">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-264">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="2f2a7-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-265">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-266">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-267">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-268">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f2a7-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-269">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-270">SP3</span><span class="sxs-lookup"><span data-stu-id="2f2a7-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-271">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-273">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="2f2a7-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-274">SP3</span><span class="sxs-lookup"><span data-stu-id="2f2a7-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-275">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="2f2a7-276">Nota</span><span class="sxs-lookup"><span data-stu-id="2f2a7-276">Note</span></span>**  
<span data-ttu-id="2f2a7-277">Per supportare SQL 2016, è necessario installare la versione di manutenzione di marzo 2017 per MDOP https://www.microsoft.com/download/details.aspx?id=54967 e per supportare sql 2017 è necessario installare la versione di manutenzione di luglio 2018 per MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="2f2a7-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="2f2a7-278">In generale, è possibile usare sempre l'aggiornamento della manutenzione più recente, poiché include anche tutti i bug e le nuove caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="2f2a7-279">Requisiti di spazio per processori, RAM e spazi su disco di SQL Server-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="2f2a7-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="2f2a7-280">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco consigliati per il computer SQL Server quando si usa la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="2f2a7-281">Usare questi requisiti come guida.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-281">Use these requirements as a guide.</span></span> <span data-ttu-id="2f2a7-282">I requisiti specifici variano in base al numero di computer client supportati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="2f2a7-283">Per visualizzare i requisiti per la topologia di integrazione di Configuration Manager, vedere [requisiti relativi a SQL Server Processor, RAM e spazio su disco-topologia di integrazione di Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-284">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="2f2a7-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-285">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-286">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="2f2a7-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-287">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="2f2a7-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-288">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2f2a7-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-289">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="2f2a7-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-290">RAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-291">8 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-292">12 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-293">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="2f2a7-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-294">5 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-295">5 GB o superiore</span><span class="sxs-lookup"><span data-stu-id="2f2a7-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="2f2a7-296">Requisiti di spazio su processori, RAM e Space disk per SQL Server-topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2f2a7-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="2f2a7-297">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco del server per il computer Microsoft SQL Server quando si usa la topologia di integrazione di Configuration Manager, vedere Requisiti per la [topologia autonoma di processori, RAM e spazio su disco di SQL Server](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-298">Elemento hardware</span><span class="sxs-lookup"><span data-stu-id="2f2a7-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-299">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-300">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="2f2a7-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-301">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="2f2a7-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-302">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2f2a7-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-303">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="2f2a7-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-304">RAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-305">4 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-306">8 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-307">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="2f2a7-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-308">5 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-309">5 GB</span><span class="sxs-lookup"><span data-stu-id="2f2a7-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="2f2a7-310">Requisiti di sistema client di MBAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="2f2a7-311">Requisiti del sistema operativo client</span><span class="sxs-lookup"><span data-stu-id="2f2a7-311">Client operating system requirements</span></span>

<span data-ttu-id="2f2a7-312">Ti consigliamo vivamente di eseguire il client MBAM e il server MBAM sulla stessa linea di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="2f2a7-313">Ad esempio, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="2f2a7-314">La tabella seguente elenca i sistemi operativi supportati per l'installazione di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="2f2a7-315">Gli stessi requisiti si applicano alle topologie di integrazione autonoma e gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-316">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-317">Edizione</span><span class="sxs-lookup"><span data-stu-id="2f2a7-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-318">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2f2a7-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-319">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2f2a7-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="2f2a7-320">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2f2a7-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2f2a7-321">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="2f2a7-322">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-323">Windows10</span><span class="sxs-lookup"><span data-stu-id="2f2a7-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-324">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-325">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-326">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-327">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-328">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-329">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f2a7-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-330">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="2f2a7-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-331">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-332">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-333">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="2f2a7-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-334">Windows 8,1 e Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="2f2a7-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-335">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="2f2a7-336">Requisiti di RAM client</span><span class="sxs-lookup"><span data-stu-id="2f2a7-336">Client RAM requirements</span></span>

<span data-ttu-id="2f2a7-337">Non ci sono requisiti di RAM specifici per l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="2f2a7-338">Requisiti di sistema per i criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="2f2a7-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="2f2a7-339">La tabella seguente elenca i sistemi operativi supportati per l'installazione dei modelli di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f2a7-340">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2f2a7-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-341">Edizione</span><span class="sxs-lookup"><span data-stu-id="2f2a7-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-342">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2f2a7-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2f2a7-343">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="2f2a7-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="2f2a7-344">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2f2a7-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="2f2a7-345">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="2f2a7-346">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-347">Windows10</span><span class="sxs-lookup"><span data-stu-id="2f2a7-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-348">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-349">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-350">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-351">Funzionalità per le aziende</span><span class="sxs-lookup"><span data-stu-id="2f2a7-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-352">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f2a7-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-354">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="2f2a7-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-355">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-356">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-357">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-358">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-359">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f2a7-360">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f2a7-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-361">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-362">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f2a7-363">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f2a7-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-364">Standard, aziendale o Datacenter</span><span class="sxs-lookup"><span data-stu-id="2f2a7-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-365">SP1</span><span class="sxs-lookup"><span data-stu-id="2f2a7-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f2a7-366">64 bit</span><span class="sxs-lookup"><span data-stu-id="2f2a7-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="2f2a7-367">MBAM in Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="2f2a7-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="2f2a7-368">Il server MBAM può essere distribuito in un'infrastruttura di Azure come servizio (IaaS) in una delle versioni supportate del sistema operativo elencate sopra, che si connettono a una directory ospitata in locale o in Active Directory ospitata anche in Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="2f2a7-369">La documentazione relativa alla configurazione e alla configurazione di Active Directory in Azure IaaS è disponibile [qui](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="2f2a7-370">Il client MBAM non è supportato nelle macchine virtuali e non è supportato anche in Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="2f2a7-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="2f2a7-371">Versioni di servizio</span><span class="sxs-lookup"><span data-stu-id="2f2a7-371">Service releases</span></span> 

- [<span data-ttu-id="2f2a7-372">Hotfix 2016 aprile</span><span class="sxs-lookup"><span data-stu-id="2f2a7-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2f2a7-373">2016 settembre</span><span class="sxs-lookup"><span data-stu-id="2f2a7-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="2f2a7-374">Dicembre 2016</span><span class="sxs-lookup"><span data-stu-id="2f2a7-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="2f2a7-375">Marzo 2017</span><span class="sxs-lookup"><span data-stu-id="2f2a7-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="2f2a7-376">Giugno 2017</span><span class="sxs-lookup"><span data-stu-id="2f2a7-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2f2a7-377">Settembre 2017</span><span class="sxs-lookup"><span data-stu-id="2f2a7-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="2f2a7-378">Marzo 2018</span><span class="sxs-lookup"><span data-stu-id="2f2a7-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2f2a7-379">2018 luglio</span><span class="sxs-lookup"><span data-stu-id="2f2a7-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2f2a7-380">2019 maggio</span><span class="sxs-lookup"><span data-stu-id="2f2a7-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="2f2a7-381">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f2a7-381">Related topics</span></span>


[<span data-ttu-id="2f2a7-382">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2f2a7-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="2f2a7-383">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2f2a7-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="2f2a7-384">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="2f2a7-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2f2a7-385">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2f2a7-386">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2f2a7-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




