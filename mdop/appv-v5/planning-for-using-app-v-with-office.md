---
title: Pianificazione per l'uso di App-V con Office
description: Pianificazione per l'uso di App-V con Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804966"
---
# <span data-ttu-id="23c47-103">Pianificazione per l'uso di App-V con Office</span><span class="sxs-lookup"><span data-stu-id="23c47-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="23c47-104">Usare le informazioni seguenti per pianificare la distribuzione di Office tramite App-V.</span><span class="sxs-lookup"><span data-stu-id="23c47-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="23c47-105">Questo articolo include:</span><span class="sxs-lookup"><span data-stu-id="23c47-105">This article includes:</span></span>

-   [<span data-ttu-id="23c47-106">Supporto di App-V per i Language Pack</span><span class="sxs-lookup"><span data-stu-id="23c47-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="23c47-107">Versioni supportate di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="23c47-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="23c47-108">Pianificazione dell'uso di App-V con le versioni coesistenti di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="23c47-109">Modalità di integrazione di Office con Windows quando si distribuisce USA App-V per distribuire Office</span><span class="sxs-lookup"><span data-stu-id="23c47-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="23c47-110">Supporto di App-V per i Language Pack</span><span class="sxs-lookup"><span data-stu-id="23c47-110">App-V support for Language Packs</span></span>


<span data-ttu-id="23c47-111">Puoi usare il sequencer App-V 5,0 per creare pacchetti plug-in per Language Pack, Language Interface Pack, strumenti di correzione e lingue delle descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="23c47-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="23c47-112">Puoi quindi includere i pacchetti plug-in in un gruppo di connessioni, insieme al pacchetto di Office 2013 creato tramite Office Deployment Toolkit.</span><span class="sxs-lookup"><span data-stu-id="23c47-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="23c47-113">Le applicazioni di Office e i Language Pack plug-in interagiscono perfettamente nello stesso gruppo di connessioni, come tutti gli altri pacchetti raggruppati in un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="23c47-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="23c47-114">**Nota**  Microsoft Visio e Microsoft Project non consentono di supportare il Language Pack tailandese.</span><span class="sxs-lookup"><span data-stu-id="23c47-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="23c47-115">Versioni supportate di Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="23c47-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="23c47-116">Nella tabella seguente sono elencate le versioni di Microsoft Office supportate da App-V, i metodi di creazione di pacchetti di Office, le licenze supportate e le distribuzioni supportate.</span><span class="sxs-lookup"><span data-stu-id="23c47-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="23c47-117">Versione di Office supportata</span><span class="sxs-lookup"><span data-stu-id="23c47-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="23c47-118">Versioni App-V supportate</span><span class="sxs-lookup"><span data-stu-id="23c47-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="23c47-119">Creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="23c47-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="23c47-120">Licenze supportate</span><span class="sxs-lookup"><span data-stu-id="23c47-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="23c47-121">Distribuzioni supportate</span><span class="sxs-lookup"><span data-stu-id="23c47-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-122">App Microsoft 365 per le aziende</span><span class="sxs-lookup"><span data-stu-id="23c47-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="23c47-123">Supportato anche:</span><span class="sxs-lookup"><span data-stu-id="23c47-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="23c47-124">Visio Pro per Office 365</span><span class="sxs-lookup"><span data-stu-id="23c47-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="23c47-125">Project Pro per Office 365</span><span class="sxs-lookup"><span data-stu-id="23c47-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="23c47-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="23c47-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="23c47-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="23c47-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="23c47-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="23c47-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="23c47-129">Strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-130">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="23c47-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="23c47-131">Desktop</span><span class="sxs-lookup"><span data-stu-id="23c47-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="23c47-132">VDI personale</span><span class="sxs-lookup"><span data-stu-id="23c47-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="23c47-133">VDI in pool</span><span class="sxs-lookup"><span data-stu-id="23c47-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="23c47-134">RDS</span><span class="sxs-lookup"><span data-stu-id="23c47-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-135">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="23c47-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="23c47-136">Supportato anche:</span><span class="sxs-lookup"><span data-stu-id="23c47-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="23c47-137">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="23c47-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="23c47-138">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="23c47-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="23c47-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="23c47-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="23c47-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="23c47-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="23c47-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="23c47-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="23c47-142">Strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-143">Contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="23c47-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="23c47-144">Desktop</span><span class="sxs-lookup"><span data-stu-id="23c47-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="23c47-145">VDI personale</span><span class="sxs-lookup"><span data-stu-id="23c47-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="23c47-146">VDI in pool</span><span class="sxs-lookup"><span data-stu-id="23c47-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="23c47-147">RDS</span><span class="sxs-lookup"><span data-stu-id="23c47-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="23c47-148">Pianificazione dell'uso di App-V con le versioni coesistenti di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="23c47-149">È possibile installare più di una versione di Microsoft Office affiancata nello stesso computer usando "coesistenza di Microsoft Office".</span><span class="sxs-lookup"><span data-stu-id="23c47-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="23c47-150">È possibile implementare la coesistenza di Office con le combinazioni di tutte le versioni principali di Office e con i metodi di installazione, se applicabile, usando la versione di Office basata su Windows Installer (MSi), a portata di clic e App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="23c47-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="23c47-151">Tuttavia, l'uso della coesistenza di Office non è consigliato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="23c47-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="23c47-152">La procedura consigliata di Microsoft è quella di evitare completamente la coesistenza di Office per evitare problemi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="23c47-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="23c47-153">Tuttavia, quando si esegue la migrazione a una versione più recente di Office, si verificano occasionalmente problemi che non possono essere risolti immediatamente, in modo da poter implementare temporaneamente la coesistenza per facilitare una migrazione più rapida alla versione più recente del prodotto.</span><span class="sxs-lookup"><span data-stu-id="23c47-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="23c47-154">L'uso della coesistenza di Office a lungo termine non è mai consigliato e l'organizzazione dovrebbe avere un piano per la transizione completa nell'immediato futuro.</span><span class="sxs-lookup"><span data-stu-id="23c47-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="23c47-155">Prima di implementare la coesistenza di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="23c47-156">Prima di implementare la coesistenza di Office, esaminare la documentazione di Office seguente.</span><span class="sxs-lookup"><span data-stu-id="23c47-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="23c47-157">Scegliere l'articolo che corrisponde alla versione più recente di Office per cui si intende implementare la coesistenza.</span><span class="sxs-lookup"><span data-stu-id="23c47-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="23c47-158">Versione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="23c47-159">Collegamento alle indicazioni</span><span class="sxs-lookup"><span data-stu-id="23c47-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="23c47-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="23c47-161">Informazioni su come usare le suite e i programmi di Office 2013 (distribuzione MSI) in un computer in cui è in esecuzione un'altra versione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="23c47-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="23c47-163">Informazioni sull'uso di Office 2010 Suites e programmi in un computer in cui è in esecuzione un'altra versione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="23c47-164">La documentazione di Office offre indicazioni esaustive sulla coesistenza per le installazioni di Office basate su Windows Installer (MSi) e a portata di clic.</span><span class="sxs-lookup"><span data-stu-id="23c47-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="23c47-165">Questo argomento App-V sulla coesistenza integra le indicazioni di Office con le informazioni più specifiche per le distribuzioni di App-V.</span><span class="sxs-lookup"><span data-stu-id="23c47-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="23c47-166">Scenari di coesistenza di Office supportati</span><span class="sxs-lookup"><span data-stu-id="23c47-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="23c47-167">Le tabelle seguenti riepilogano gli scenari di coesistenza supportati.</span><span class="sxs-lookup"><span data-stu-id="23c47-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="23c47-168">Sono organizzati in base al metodo di versione e distribuzione a cui si sta iniziando e al metodo di versione e distribuzione a cui si sta eseguendo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="23c47-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="23c47-169">Assicurarsi di testare completamente tutte le soluzioni di coesistenza prima di distribuirle a un gruppo di destinatari.</span><span class="sxs-lookup"><span data-stu-id="23c47-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="23c47-170">**Nota**  Microsoft non supporta l'uso di più versioni di Office in ambienti Windows Server in cui è abilitato il servizio ruolo Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="23c47-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="23c47-171">Per eseguire scenari di coesistenza di Office, è necessario disabilitare questo servizio ruolo.</span><span class="sxs-lookup"><span data-stu-id="23c47-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="23c47-172">Integrazioni di Windows & coesistenza di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="23c47-173">I metodi di installazione di Office basati su Windows Installer e a portata di clic vengono integrati con alcuni punti del sistema operativo Windows sottostante.</span><span class="sxs-lookup"><span data-stu-id="23c47-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="23c47-174">Quando si usa la coesistenza, le integrazioni comuni dei sistemi operativi tra due versioni di Office possono essere in conflitto, causando problemi di compatibilità e esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="23c47-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="23c47-175">Con App-V puoi sequenziare alcune versioni di Office per escludere le integrazioni, quindi "isolarle" dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23c47-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="23c47-176">Modalità in cui App-V può sequenziare questa versione di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="23c47-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-178">Sempre non integrati.</span><span class="sxs-lookup"><span data-stu-id="23c47-178">Always non-integrated.</span></span> <span data-ttu-id="23c47-179">App-V non offre integrazioni di sistemi operativi con una versione virtualizzata di Office 2007.</span><span class="sxs-lookup"><span data-stu-id="23c47-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="23c47-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-181">Modalità integrata e non integrata.</span><span class="sxs-lookup"><span data-stu-id="23c47-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="23c47-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-183">Sempre integrata.</span><span class="sxs-lookup"><span data-stu-id="23c47-183">Always integrated.</span></span> <span data-ttu-id="23c47-184">Le integrazioni dei sistemi operativi Windows non possono essere disabilitate.</span><span class="sxs-lookup"><span data-stu-id="23c47-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="23c47-185">Microsoft consiglia di distribuire la coesistenza di Office con una sola istanza di Office integrata.</span><span class="sxs-lookup"><span data-stu-id="23c47-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="23c47-186">Ad esempio, se si usa App-V per distribuire Office 2010 e Office 2013, è necessario sequenziare Office 2010 in modalità non integrata.</span><span class="sxs-lookup"><span data-stu-id="23c47-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="23c47-187">Per altre informazioni sulla sequenziazione di Office in modalità non di integrazione (isolata), vedere [come sequenziare Microsoft office 2010 in Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="23c47-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="23c47-188">Limitazioni note degli scenari di coesistenza di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="23c47-189">Le sezioni seguenti descrivono alcuni problemi che potresti riscontrare quando usi App-V per implementare la coesistenza con Office.</span><span class="sxs-lookup"><span data-stu-id="23c47-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="23c47-190">Limitazioni comuni agli scenari di coesistenza di Windows Installer e a portata di clic e App-V Office</span><span class="sxs-lookup"><span data-stu-id="23c47-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="23c47-191">Quando si installano le versioni seguenti di Office nello stesso computer, è possibile che siano presenti le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c47-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="23c47-192">Office 2010 tramite la versione basata su Windows Installer</span><span class="sxs-lookup"><span data-stu-id="23c47-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="23c47-193">Office 2013 tramite App-V</span><span class="sxs-lookup"><span data-stu-id="23c47-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="23c47-194">Dopo aver pubblicato Office 2013 tramite App-V affiancata a una versione precedente di Office 2010 basato su Windows Installer, potrebbe essere necessario avviare Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="23c47-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="23c47-195">Il motivo è che la versione basata su Windows Installer o a portata di clic di Office 2010 sta provando a eseguire automaticamente la registrazione nel computer.</span><span class="sxs-lookup"><span data-stu-id="23c47-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="23c47-196">Per ignorare l'operazione di registrazione automatica per Word 2010 nativo, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c47-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="23c47-197">Uscire da Word 2010.</span><span class="sxs-lookup"><span data-stu-id="23c47-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="23c47-198">Avviare l'editor del registro di sistema eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c47-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="23c47-199">In Windows 7: fare clic sul pulsante **Start**, digitare **Regedit** nella casella Inizia ricerca e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="23c47-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="23c47-200">In Windows 8 digitare **Regedit** premere INVIO nella pagina iniziale e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="23c47-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="23c47-201">Se viene richiesta una password di amministratore o per una conferma, digitare la password oppure fare clic su **continua**.</span><span class="sxs-lookup"><span data-stu-id="23c47-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="23c47-202">Individuare e quindi selezionare la sottochiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="23c47-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="23c47-203">Scegliere **nuovo**dal menu **modifica** e quindi fare clic su **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="23c47-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="23c47-204">Digitare **NoReReg**e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="23c47-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="23c47-205">Fare clic con il pulsante destro del mouse su **NoReReg** e quindi scegliere **modifica**.</span><span class="sxs-lookup"><span data-stu-id="23c47-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="23c47-206">Nella casella **Dativalore** Digitare **1**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="23c47-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="23c47-207">Nel menu file fare clic su **Esci** per chiudere l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="23c47-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="23c47-208">Modalità di integrazione di Office con Windows quando si usa App-V per distribuire Office</span><span class="sxs-lookup"><span data-stu-id="23c47-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="23c47-209">Quando si distribuisce Office 2013 tramite App-V, Office è completamente integrato con il sistema operativo, che fornisce agli utenti finali le stesse funzionalità e funzionalità di Office quando viene distribuita senza App-V.</span><span class="sxs-lookup"><span data-stu-id="23c47-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="23c47-210">Il pacchetto Office 2013 App-V supporta i punti di integrazione seguenti con il sistema operativo Windows:</span><span class="sxs-lookup"><span data-stu-id="23c47-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="23c47-211">Punto di estensione</span><span class="sxs-lookup"><span data-stu-id="23c47-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="23c47-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23c47-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-213">Plug-in di Lync meeting join per Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="23c47-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-214">L'utente può partecipare a riunioni Lync da Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="23c47-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-215">Inviato al driver di stampa di OneNote</span><span class="sxs-lookup"><span data-stu-id="23c47-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-216">L'utente può stampare in OneNote</span><span class="sxs-lookup"><span data-stu-id="23c47-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-217">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="23c47-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-218">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="23c47-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-219">Inviare al componente aggiuntivo OneNote Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="23c47-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-220">L'utente può inviare a OneNote da IE</span><span class="sxs-lookup"><span data-stu-id="23c47-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-221">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="23c47-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-222">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="23c47-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-223">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="23c47-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-224">Le app e i componenti aggiuntivi nativi possono interagire con Outlook virtuale tramite MAPI</span><span class="sxs-lookup"><span data-stu-id="23c47-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-225">Plug-in di SharePoint per Firefox</span><span class="sxs-lookup"><span data-stu-id="23c47-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-226">L'utente può usare le caratteristiche di SharePoint in Firefox</span><span class="sxs-lookup"><span data-stu-id="23c47-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-227">Applet del pannello di controllo posta</span><span class="sxs-lookup"><span data-stu-id="23c47-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-228">L'utente ottiene l'applet del pannello di controllo della posta in Outlook</span><span class="sxs-lookup"><span data-stu-id="23c47-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-229">Assembly di interoperabilità primari</span><span class="sxs-lookup"><span data-stu-id="23c47-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-230">Supportare i componenti aggiuntivi gestiti</span><span class="sxs-lookup"><span data-stu-id="23c47-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-231">Gestore della cache dei documenti di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-232">Consente la cache dei documenti per le applicazioni di Office</span><span class="sxs-lookup"><span data-stu-id="23c47-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-233">Gestore ricerca protocollo di Outlook</span><span class="sxs-lookup"><span data-stu-id="23c47-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-234">L'utente può eseguire ricerche in Outlook</span><span class="sxs-lookup"><span data-stu-id="23c47-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-235">Controlli Active X:</span><span class="sxs-lookup"><span data-stu-id="23c47-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-236">Per altre informazioni sui controlli ActiveX, vedere <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> riferimenti alle API dei controlli ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="23c47-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="23c47-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-238">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-239">PortalConnect. PersonalSite</span><span class="sxs-lookup"><span data-stu-id="23c47-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-240">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-241">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="23c47-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-242">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="23c47-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-244">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="23c47-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-246">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="23c47-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-248">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="23c47-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-250">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="23c47-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-252">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-253">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="23c47-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-254">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="23c47-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-256">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-257">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="23c47-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-258">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-259">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="23c47-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-260">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-261">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="23c47-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-262">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-263">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="23c47-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-264">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="23c47-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="23c47-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-266">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="23c47-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="23c47-267">Helper del browser OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="23c47-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-268">Controllo Active X]</span><span class="sxs-lookup"><span data-stu-id="23c47-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-269">Sovrapposizioni di icone di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="23c47-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="23c47-270">L'icona della shell di Windows Explorer si sovrappone quando gli utenti esaminano le cartelle di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="23c47-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-271">Estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="23c47-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="23c47-272">Scorciatoie</span><span class="sxs-lookup"><span data-stu-id="23c47-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="23c47-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="23c47-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





