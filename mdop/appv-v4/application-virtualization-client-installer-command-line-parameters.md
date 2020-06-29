---
title: Parametri della riga di comando del programma di installazione di Application Virtualization Client
description: Parametri della riga di comando del programma di installazione di Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819716"
---
# <span data-ttu-id="e5ed7-103">Parametri della riga di comando del programma di installazione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="e5ed7-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="e5ed7-104">Nella tabella seguente sono elencati tutti i parametri della riga di comando di Microsoft Application Virtualization Client Installer disponibili, i relativi valori e una breve descrizione di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="e5ed7-105">I parametri sono maiuscole/minuscole e devono essere immessi come lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="e5ed7-106">Tutti i valori dei parametri devono essere racchiusi tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="e5ed7-107">Nota</span><span class="sxs-lookup"><span data-stu-id="e5ed7-107">Note</span></span>**  
-   <span data-ttu-id="e5ed7-108">Per App-V versione 4,6, i parametri della riga di comando non possono essere usati durante l'aggiornamento del client.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="e5ed7-109">I parametri *SWICACHESIZE* e *MINFREESPACEMB* non possono essere combinati nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="e5ed7-110">Se vengono usati entrambi, il parametro *SWICACHESIZE* verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5ed7-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="e5ed7-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e5ed7-112">Valori</span><span class="sxs-lookup"><span data-stu-id="e5ed7-112">Values</span></span></th>
<th align="left"><span data-ttu-id="e5ed7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5ed7-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="e5ed7-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-115">TRUE</span></span></p>
<p><span data-ttu-id="e5ed7-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-117">Indica se lo streaming da file verrà abilitato indipendentemente dal modo in cui il client è stato configurato con il <em> </em> parametro APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="e5ed7-118">Se impostato su FALSE, il trasporto non consentirà lo streaming da file, anche se l'OSD HREF o il <em> </em> parametro APPLICATIONSOURCEROOT contiene un percorso di file.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="e5ed7-119">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-120">TRUE: l'applicazione distribuita manualmente può essere caricata da disco.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-121">FALSE: tutte le applicazioni devono provenire da server di flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="e5ed7-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-123"><em>URL RTSP:// </em> (per il recapito dinamico del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="e5ed7-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="e5ed7-124"><em>URL file:// </em> o <em> UNC </em> (per il caricamento dal pacchetto di distribuzione di file)</span><span class="sxs-lookup"><span data-stu-id="e5ed7-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-125">Per consentire a un amministratore o a un sistema di distribuzione elettronica del software di assicurarsi che il caricamento dell'applicazione venga eseguito in conformità con lo schema di gestione della topologia, consente l'override della BASE di codice OSD per l'elemento HREF dell'applicazione (la posizione di origine).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="e5ed7-126">Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="e5ed7-127">Un URL include diverse parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="e5ed7-128">&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="e5ed7-129">Un percorso UNC include tre parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="e5ed7-130">&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="e5ed7-131">Se il <em> </em> parametro APPLICATIONSOURCEROOT è specificato in un client, il client suddividerà l'URL o il percorso UNC da un file OSD nelle parti costituenti e sostituirà le sezioni OSD con le <em> sezioni ApplicationSourceRoot corrispondenti </em> .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-132">Importante</span><span class="sxs-lookup"><span data-stu-id="e5ed7-132">Important</span></span></strong><br/><p><span data-ttu-id="e5ed7-133">Assicurarsi di usare il formato corretto quando si usa file://con un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="e5ed7-134">Il formato corretto è file:// &amp; lt; server &gt; &amp; lt; share &gt; .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="e5ed7-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="e5ed7-136">UNC</span><span class="sxs-lookup"><span data-stu-id="e5ed7-136">UNC</span></span></em></p>
<p><span data-ttu-id="e5ed7-137">URL <em> http:// </em> o <em> URL https://</span><span class="sxs-lookup"><span data-stu-id="e5ed7-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-138">Consente a un amministratore di specificare una posizione di origine per il recupero delle icone per un pacchetto di applicazione sequenziata durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="e5ed7-139">Le radici di origine delle icone supportano i percorsi UNC e gli URL (HTTP o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="e5ed7-140">Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="e5ed7-141">Un URL include diverse parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="e5ed7-142">&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="e5ed7-143">Un percorso UNC include tre parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="e5ed7-144">&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-145">Importante</span><span class="sxs-lookup"><span data-stu-id="e5ed7-145">Important</span></span></strong><br/><p><span data-ttu-id="e5ed7-146">Assicurarsi di usare il formato corretto quando si usa un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="e5ed7-147">I formati accettabili sono &amp; lt; server &gt; &amp; lt; lettera di condivisione &gt; o &lt; unità &gt; : &amp; lt; cartella &gt; .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="e5ed7-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="e5ed7-149">UNC</span><span class="sxs-lookup"><span data-stu-id="e5ed7-149">UNC</span></span></em></p>
<p><span data-ttu-id="e5ed7-150">URL <em> http:// </em> o <em> URL https://</span><span class="sxs-lookup"><span data-stu-id="e5ed7-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-151">Consente a un amministratore di specificare una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="e5ed7-152">Le radici di origine OSD supportano i percorsi UNC e gli URL (HTTP o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="e5ed7-153">Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="e5ed7-154">Un URL include diverse parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="e5ed7-155">&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="e5ed7-156">Un percorso UNC include tre parti:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="e5ed7-157">&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-158">Importante</span><span class="sxs-lookup"><span data-stu-id="e5ed7-158">Important</span></span></strong><br/><p><span data-ttu-id="e5ed7-159">Assicurarsi di usare il formato corretto quando si usa un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="e5ed7-160">I formati accettabili sono &amp; lt; server &gt; &amp; lt; lettera di condivisione &gt; o &lt; unità &gt; : &amp; lt; cartella &gt; .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="e5ed7-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="e5ed7-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="e5ed7-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="e5ed7-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="e5ed7-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="e5ed7-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-165">Trigger AutoLoad che definiscono gli eventi che avviano il caricamento automatico delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="e5ed7-166">Autoload USA in modo implicito lo streaming in background per consentire il caricamento completo dell'applicazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="e5ed7-167">Il blocco di funzionalità principale verrà caricato il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="e5ed7-168">I blocchi di funzionalità rimanenti verranno caricati in background per abilitare le operazioni in primo piano, ad esempio l'interazione dell'utente con le applicazioni, per avere priorità e ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-169">Nota</span><span class="sxs-lookup"><span data-stu-id="e5ed7-169">Note</span></span></strong><br/><p><span data-ttu-id="e5ed7-170">Il <em> </em> parametro AUTOLOADTARGET determina le applicazioni caricate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="e5ed7-171">Per impostazione predefinita, i pacchetti che sono stati usati vengono caricati automaticamente, a meno che non <em> </em> sia impostato AUTOLOADTARGET.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e5ed7-172">Ogni parametro ha effetto sul comportamento del caricamento nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="e5ed7-173">AUTOLOADONLOGIN </em> -il caricamento viene avviato quando l'utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="e5ed7-174">AUTOLOADONLAUNCH </em> -il caricamento viene avviato quando l'utente avvia un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="e5ed7-175">AUTOLOADONREFRESH </em> -il caricamento viene avviato quando si verifica un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="e5ed7-176">I tre valori possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-176">The three values can be combined.</span></span> <span data-ttu-id="e5ed7-177">Nell'esempio seguente, i trigger di autoload sono abilitati sia all'accesso dell'utente che quando si verifica l'aggiornamento della pubblicazione:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="e5ed7-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="e5ed7-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-179">Nota</span><span class="sxs-lookup"><span data-stu-id="e5ed7-179">Note</span></span></strong><br/><p><span data-ttu-id="e5ed7-180">Se il client è configurato per la prima volta con questi valori, il comando AutoLoad non verrà attivato fino alla successiva disattivazione dell'utente e non viene eseguito il log.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="e5ed7-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-182">NESSUNO</span><span class="sxs-lookup"><span data-stu-id="e5ed7-182">NONE</span></span></p>
<p><span data-ttu-id="e5ed7-183">TUTTI</span><span class="sxs-lookup"><span data-stu-id="e5ed7-183">ALL</span></span></p>
<p><span data-ttu-id="e5ed7-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="e5ed7-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-185">Indica cosa verrà caricato automaticamente quando si verificherà un trigger di caricamento automatico specifico.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="e5ed7-186">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-187">Nessuno: nessun caricamento automatico, indipendentemente dai trigger che potrebbero essere impostati.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-188">TUTTO: se è abilitato un trigger di autoload, tutti i pacchetti vengono caricati automaticamente, indipendentemente dal fatto che siano stati o meno avviati.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-189">Nota</span><span class="sxs-lookup"><span data-stu-id="e5ed7-189">Note</span></span></strong><br/><p><span data-ttu-id="e5ed7-190">Questa impostazione è configurata per i singoli pacchetti usando il <strong> pacchetto SFTMIME Add Package </strong> e configura i comandi del <strong> pacchetto </strong> .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="e5ed7-191">Per altre informazioni su questi comandi, vedere <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> riferimento al comando SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="e5ed7-192">PREVUSED-Se è abilitato un trigger di autoload, carica solo i pacchetti in cui almeno un'applicazione nel pacchetto è stata usata in precedenza, ovvero avviata o prememorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="e5ed7-193">Nota</span><span class="sxs-lookup"><span data-stu-id="e5ed7-193">Note</span></span></strong><br/><p><span data-ttu-id="e5ed7-194">Quando si installa il client App-V per usare una cache di sola lettura (ad esempio, come implementazione di un server VDI), è necessario impostare il <em> </em> parametro AUTOLOADTARGET su None per impedire al client di provare ad aggiornare le applicazioni nella cache di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="e5ed7-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-196">29600 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5ed7-196">29600 (default)</span></span></p>
<p><span data-ttu-id="e5ed7-197">1-1439998560 minuti (intervallo)</span><span class="sxs-lookup"><span data-stu-id="e5ed7-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-198">Indica il numero di minuti in cui un'applicazione può essere usata nell'operazione disconnessa.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="e5ed7-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-200">&lt;percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-201">Specifica la directory di installazione del client App-V.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="e5ed7-202">Esempio: INSTALLDIR = &quot; C:\Programmi\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-203">OPTIN</span><span class="sxs-lookup"><span data-stu-id="e5ed7-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-204">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-204">“TRUE”</span></span></p>
<p><span data-ttu-id="e5ed7-205">“”</span><span class="sxs-lookup"><span data-stu-id="e5ed7-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-206">I componenti di Microsoft Application Virtualization Client saranno aggiornabili tramite Microsoft Update quando gli aggiornamenti vengono resi disponibili per il pubblico in generale.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="e5ed7-207">Microsoft Update Agent installato nei sistemi operativi Windows richiede a un utente di accettare esplicitamente di usare il servizio.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="e5ed7-208">Questo opt-in è necessario una sola volta per tutte le applicazioni nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="e5ed7-209">Se hai già optato per Microsoft Update, i componenti Microsoft Application Virtualization nel dispositivo approfitteranno automaticamente del servizio.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="e5ed7-210">Per l'installazione della riga di comando, l'uso di Microsoft Update è per impostazione predefinita opt-out (a meno che un'applicazione precedente non abbia già consentito l'inserimento del dispositivo) a causa del requisito di optare manualmente in Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="e5ed7-211">Di conseguenza, l'opt-in deve essere esplicito per le installazioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="e5ed7-212">Impostando il parametro della riga <em> di comando optin </em> su true, viene impostato l'opt-in Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="e5ed7-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-214">TRUE</span></span></p>
<p><span data-ttu-id="e5ed7-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-216">Indica se l'autorizzazione è sempre necessaria, indipendentemente dal fatto che un'applicazione sia già nella cache.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="e5ed7-217">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-218">TRUE: l'applicazione deve sempre essere autorizzata all'avvio.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="e5ed7-219">Per le applicazioni in streaming RTSP, il token di autorizzazione utente viene inviato al server per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="e5ed7-220">Per le applicazioni basate su file, gli ACL dei file determinano se un utente può accedere all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-221">FALSE: provare sempre a connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="e5ed7-222">Se non è possibile stabilire una connessione al server, il client consente comunque all'utente di avviare un'applicazione precedentemente caricata nella cache.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-224">Dimensioni della cache in MB</span><span class="sxs-lookup"><span data-stu-id="e5ed7-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-225">Specifica le dimensioni in megabyte della cache client.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="e5ed7-226">La dimensione predefinita è 4096 MB e la dimensione massima è 1.048.576 MB (1 TB).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="e5ed7-227">Il sistema verifica lo spazio disponibile al momento dell'installazione, ma lo spazio non è riservato.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="e5ed7-228">Esempio: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="e5ed7-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-230">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="e5ed7-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-231">Specifica il nome visualizzato del server di pubblicazione; obbligatorio quando <em> </em> viene usato SWIPUBSVRHOST.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="e5ed7-232">Esempio: <strong> SWIPUBSVRDISPLAY = &quot; ambiente di produzione&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-234">[HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="e5ed7-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-235">Specifica il tipo di server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-235">Specifies the publishing server type.</span></span> <span data-ttu-id="e5ed7-236">Il tipo di server predefinito è Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="e5ed7-237">L' <strong> opzione/Secure non fa distinzione tra maiuscole e </strong> minuscole.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-238">HTTP-server HTTP standard</span><span class="sxs-lookup"><span data-stu-id="e5ed7-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-239">HTTP <strong> /Secure </strong> — Server http di sicurezza avanzato</span><span class="sxs-lookup"><span data-stu-id="e5ed7-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-240">RTSP — Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e5ed7-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-241">RTSP <strong> /Secure </strong> — Enhanced Security Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e5ed7-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="e5ed7-242">Esempio: <strong> SWIPUBSVRTYPE = &quot; http/secure&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="e5ed7-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-244">Indirizzo IP | nome host</span><span class="sxs-lookup"><span data-stu-id="e5ed7-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-245">Specifica l'indirizzo IP del server di virtualizzazione dell'applicazione o un nome host del server che viene risolto nell'indirizzo IP del server&#39;s; obbligatorio quando <em> </em> viene usato SWIPUBSVRDISPLAY.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="e5ed7-246">Esempio: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="e5ed7-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-248">Numero di porta</span><span class="sxs-lookup"><span data-stu-id="e5ed7-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-249">Specifica la porta logica usata da questo server di virtualizzazione dell'applicazione per ascoltare le richieste dal client (impostazione predefinita = 554).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-250">Server HTTP standard: impostazione predefinita = 80.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-251">Server HTTP di sicurezza avanzato-impostazione predefinita = 443.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-252">Application Virtualization Server-default = 554.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-253">Enhanced Security Application Virtualization Server-default = 322.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="e5ed7-254">Esempio: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="e5ed7-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-256">Nome percorso</span><span class="sxs-lookup"><span data-stu-id="e5ed7-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-257">Specifica la posizione nel server di pubblicazione del file che definisce le associazioni di tipi di file (impostazione predefinita =/); obbligatorio quando il <em> </em> valore del parametro SWIPUBSVRTYPE è http.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="e5ed7-258">Esempio: <strong> SWIPUBSVRPATH = &quot; /APPVIRT/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="e5ed7-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-260">[Attivato | DISATTIVARE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-261">Specifica se il client esegue automaticamente una query nel server di pubblicazione per le associazioni di tipi di file e le applicazioni quando un utente accede al client (impostazione predefinita = attivata).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="e5ed7-262">Esempio: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="e5ed7-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-264">Directory dati globale</span><span class="sxs-lookup"><span data-stu-id="e5ed7-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-265">Specifica la directory in cui verranno archiviati i dati non specifici per gli utenti particolari (impostazione predefinita = C:\Documents and Settings\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="e5ed7-266">Esempio: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="e5ed7-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-268">Directory dati utente</span><span class="sxs-lookup"><span data-stu-id="e5ed7-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-269">Specifica la directory in cui verranno archiviati i dati specifici di determinati utenti (default =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="e5ed7-270">Esempio: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="e5ed7-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-272">Lettera di unità preferita</span><span class="sxs-lookup"><span data-stu-id="e5ed7-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-273">Corrisponde alla lettera dell'unità selezionata per l'unità virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="e5ed7-274">Esempio: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="e5ed7-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="e5ed7-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="e5ed7-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-277">Indica il livello di registrazione in cui i messaggi di log vengono scritti nel log eventi di NT.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="e5ed7-278">Il valore indica una soglia di ciò che viene registrato, ovvero tutto ciò che è uguale o minore di quel valore viene registrato.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="e5ed7-279">Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</span><span class="sxs-lookup"><span data-stu-id="e5ed7-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="e5ed7-280">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5ed7-281">0 = = None</span><span class="sxs-lookup"><span data-stu-id="e5ed7-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-282">1 = = critico</span><span class="sxs-lookup"><span data-stu-id="e5ed7-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-283">2 = = errore</span><span class="sxs-lookup"><span data-stu-id="e5ed7-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-284">3 = = avviso</span><span class="sxs-lookup"><span data-stu-id="e5ed7-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="e5ed7-285">4 = = informazioni</span><span class="sxs-lookup"><span data-stu-id="e5ed7-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="e5ed7-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="e5ed7-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-287">In MB</span><span class="sxs-lookup"><span data-stu-id="e5ed7-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-288">Specifica la quantità di spazio libero (in megabyte) che deve essere disponibile nell'host prima che le dimensioni della cache possano aumentare.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="e5ed7-289">L'esempio seguente consente di configurare il client per garantire almeno 5 GB di spazio disponibile sul disco prima di consentire l'aumento delle dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="e5ed7-290">Il valore predefinito è 5000 MB di spazio disponibile su disco in fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="e5ed7-291">Esempio: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</span><span class="sxs-lookup"><span data-stu-id="e5ed7-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="e5ed7-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="e5ed7-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="e5ed7-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5ed7-294">Viene usato quando si applicano le impostazioni del registro di sistema prima della distribuzione di un client, ad esempio tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="e5ed7-295">Quando si distribuisce un client, impostare questo parametro su un valore pari a 1 in modo che non sovrascriva le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5ed7-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e5ed7-296">Importante</span><span class="sxs-lookup"><span data-stu-id="e5ed7-296">Important</span></span></strong><br/><p><span data-ttu-id="e5ed7-297">Se impostato su un valore pari a 1, i parametri della riga di comando del programma di installazione client seguenti vengono ignorati:</span><span class="sxs-lookup"><span data-stu-id="e5ed7-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="e5ed7-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, </strong> SWIFSDRIVE, <strong> AUTOLOADTARGET, </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> AUTOLOADTRIGGERS </strong> e <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="e5ed7-299">Per altre informazioni sull'impostazione di questi valori dopo l'installazione, vedere "come configurare le impostazioni del registro di sistema client App-V usando la riga di comando" nella Guida operativa di Application Virtualization (App-V) <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</span><span class="sxs-lookup"><span data-stu-id="e5ed7-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e5ed7-300">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5ed7-300">Related topics</span></span>


[<span data-ttu-id="e5ed7-301">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="e5ed7-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="e5ed7-302">Come aggiornare Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="e5ed7-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="e5ed7-303">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="e5ed7-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









