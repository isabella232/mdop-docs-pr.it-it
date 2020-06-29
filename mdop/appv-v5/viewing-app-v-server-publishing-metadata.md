---
title: Visualizzazione dei metadati di pubblicazione del server App-V
description: Visualizzazione dei metadati di pubblicazione del server App-V
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804846"
---
# <span data-ttu-id="80847-103">Visualizzazione dei metadati di pubblicazione del server App-V</span><span class="sxs-lookup"><span data-stu-id="80847-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="80847-104">Usare questa procedura per visualizzare i metadati di pubblicazione, che consentono di risolvere i problemi relativi alla pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="80847-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="80847-105">Per usare questa procedura, è necessario usare app-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="80847-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="80847-106">Questo articolo contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="80847-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="80847-107">Requisiti di App-V 5,0 SP3 per la visualizzazione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-107">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>](#bkmk-50sp3-reqs-pub-meta)

-   [<span data-ttu-id="80847-108">Sintassi da usare per la visualizzazione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="80847-109">Valori di query per il sistema operativo client e la versione</span><span class="sxs-lookup"><span data-stu-id="80847-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="80847-110">Definizione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a><span data-ttu-id="80847-111">Requisiti di App-V 5,0 SP3 per la visualizzazione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-111">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="80847-112">In App-V 5,0 SP3 è necessario specificare i valori seguenti nell'indirizzo quando si esegue una query sul server di pubblicazione App-V per i metadati:</span><span class="sxs-lookup"><span data-stu-id="80847-112">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80847-113">Value</span><span class="sxs-lookup"><span data-stu-id="80847-113">Value</span></span></th>
<th align="left"><span data-ttu-id="80847-114">Ulteriori dettagli</span><span class="sxs-lookup"><span data-stu-id="80847-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="80847-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="80847-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="80847-116">Se si omette il <strong> </strong> parametro ClientVersion dalla query, i metadati escludono le nuove funzionalità App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="80847-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="80847-117">Clientos</span><span class="sxs-lookup"><span data-stu-id="80847-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="80847-118">È necessario specificare questo valore solo se si selezionano sistemi operativi client specifici quando si sequenzia il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="80847-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="80847-119">Se si seleziona l'impostazione predefinita (tutti i sistemi operativi), non specificare questo valore nella query.</span><span class="sxs-lookup"><span data-stu-id="80847-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="80847-120">Se si omette il <strong> parametro clientos </strong> dalla query, solo i pacchetti sequenziati per supportare qualsiasi sistema operativo verranno visualizzati nei metadati.</span><span class="sxs-lookup"><span data-stu-id="80847-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="80847-121">Sintassi della query per la visualizzazione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="80847-122">Nella tabella seguente sono disponibili gli esempi di sintassi e query.</span><span class="sxs-lookup"><span data-stu-id="80847-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80847-123">Versione di App-V</span><span class="sxs-lookup"><span data-stu-id="80847-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="80847-124">Sintassi della query</span><span class="sxs-lookup"><span data-stu-id="80847-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="80847-125">Descrizioni dei parametri</span><span class="sxs-lookup"><span data-stu-id="80847-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="80847-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="80847-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-127">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="80847-127">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80847-128">Parametro</span><span class="sxs-lookup"><span data-stu-id="80847-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="80847-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80847-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="80847-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-131">Nome del server di pubblicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="80847-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-132">&lt;Porta di pubblicazione #&gt;</span><span class="sxs-lookup"><span data-stu-id="80847-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-133">Porta al server di pubblicazione App-V, definito al momento della configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="80847-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="80847-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-135">Versione del client App-V.</span><span class="sxs-lookup"><span data-stu-id="80847-135">Version of the App-V client.</span></span> <span data-ttu-id="80847-136">Fare riferimento alla tabella seguente per il valore corretto da usare.</span><span class="sxs-lookup"><span data-stu-id="80847-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-137">Clientos = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="80847-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-138">Sistema operativo del computer in cui è in uso il client App-V.</span><span class="sxs-lookup"><span data-stu-id="80847-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="80847-139">Fare riferimento alla tabella seguente per il valore corretto da usare.</span><span class="sxs-lookup"><span data-stu-id="80847-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="80847-140">Per ottenere il nome del server di pubblicazione e il numero di porta (http:// &lt; PubServer &gt; : &lt; Port Publishing # &gt; ) dal client App-V, vedere la configurazione URL del <strong> cmdlet Get-AppvPublishingServer di </strong> PowerShell.</span><span class="sxs-lookup"><span data-stu-id="80847-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="80847-141">Nell'esempio:</span><span class="sxs-lookup"><span data-stu-id="80847-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="80847-142">Un Windows Server 2012 R2 denominato "pubsvr01" ospita il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="80847-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="80847-143">Il client Windows è Windows 8,1 64 bit.</span><span class="sxs-lookup"><span data-stu-id="80847-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-144">App-V 5,0 tramite App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="80847-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="80847-145">Nota</span><span class="sxs-lookup"><span data-stu-id="80847-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="80847-146">ClientVersion </strong> e <strong> clientos </strong> sono supportati solo in App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="80847-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="80847-147">Vedere le informazioni per App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="80847-147">See the information for App-V 5.0 SP3.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="80847-148">Nell'esempio, un Windows Server 2012 R2 denominato "pubsvr01" ospita i servizi di gestione e pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="80847-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="80847-149">Valori di query per il sistema operativo client e la versione</span><span class="sxs-lookup"><span data-stu-id="80847-149">Query values for client operating system and version</span></span>


<span data-ttu-id="80847-150">Nella query di metadati di pubblicazione immettere i valori stringa che corrispondono al sistema operativo client e alla versione in uso.</span><span class="sxs-lookup"><span data-stu-id="80847-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80847-151">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="80847-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="80847-152">Architettura</span><span class="sxs-lookup"><span data-stu-id="80847-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="80847-153">Valore stringa di stringa operativa</span><span class="sxs-lookup"><span data-stu-id="80847-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-154">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="80847-154">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-155">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-156">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="80847-156">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="80847-157">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-158">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-159">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="80847-159">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-160">Windows 8</span><span class="sxs-lookup"><span data-stu-id="80847-160">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-161">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="80847-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-163">Windows 8</span><span class="sxs-lookup"><span data-stu-id="80847-163">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-164">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="80847-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-166">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="80847-166">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-167">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-168">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="80847-168">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-169">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="80847-169">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-170">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-171">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="80847-171">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80847-172">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-173">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="80847-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80847-175">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-176">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="80847-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-178">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80847-178">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-179">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-180">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="80847-180">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-181">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80847-181">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-182">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-183">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="80847-183">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80847-184">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="80847-184">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-185">64 bit</span><span class="sxs-lookup"><span data-stu-id="80847-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-186">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="80847-186">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80847-187">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="80847-187">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-188">32 bit</span><span class="sxs-lookup"><span data-stu-id="80847-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="80847-189">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="80847-189">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="80847-190">Definizione dei metadati di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="80847-190">Definition of publishing metadata</span></span>


<span data-ttu-id="80847-191">Quando i pacchetti vengono pubblicati in un computer che esegue App-V client, i metadati vengono inviati al computer che indica i pacchetti e i gruppi di connessioni da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="80847-191">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="80847-192">Il client App-V effettua due richieste separate per le seguenti:</span><span class="sxs-lookup"><span data-stu-id="80847-192">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="80847-193">Pacchetti e gruppi di connessioni autorizzati al computer client.</span><span class="sxs-lookup"><span data-stu-id="80847-193">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="80847-194">Pacchetti e gruppi di connessioni autorizzati all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="80847-194">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="80847-195">Il server di pubblicazione comunica con il server di gestione per determinare i pacchetti e i gruppi di connessioni disponibili per il richiedente.</span><span class="sxs-lookup"><span data-stu-id="80847-195">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="80847-196">Il server di pubblicazione deve essere registrato con il server di gestione in modo che i metadati vengano generati.</span><span class="sxs-lookup"><span data-stu-id="80847-196">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="80847-197">È possibile visualizzare i metadati per ogni richiesta in un browser Internet usando una query nel contesto dell'utente o del computer specifico.</span><span class="sxs-lookup"><span data-stu-id="80847-197">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="80847-198">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80847-198">Related topics</span></span>


[<span data-ttu-id="80847-199">Documentazione tecnica per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="80847-199">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)









