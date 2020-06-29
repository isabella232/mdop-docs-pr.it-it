---
title: Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet
description: Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805361"
---
# <span data-ttu-id="15160-103">Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet</span><span class="sxs-lookup"><span data-stu-id="15160-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="15160-104">Argomenti illustrati in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="15160-104">What this topic covers:</span></span>

-   [<span data-ttu-id="15160-105">Requisiti per l'uso dei cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="15160-106">Caricamento dei cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="15160-107">Ottenere assistenza per i cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="15160-108">Visualizzazione della Guida per un cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="15160-109">Requisiti per l'uso dei cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="15160-110">Esaminare i requisiti seguenti per l'uso dei cmdlet di PowerShell per App-V:</span><span class="sxs-lookup"><span data-stu-id="15160-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15160-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="15160-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="15160-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="15160-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-113">Gli utenti possono eseguire cmdlet App-V Server solo se si concede loro l'accesso usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="15160-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15160-114">Quando si distribuisce e si configura il server App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="15160-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="15160-115">Specificare un gruppo di Active Directory o un singolo utente che disponga delle autorizzazioni per la gestione dell'ambiente App-V.</span><span class="sxs-lookup"><span data-stu-id="15160-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="15160-116">Vedere <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> come distribuire il server App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="15160-116">See <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="15160-117">Dopo aver distribuito App-V Server </strong> :</span><span class="sxs-lookup"><span data-stu-id="15160-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="15160-118">Usare la console di gestione di App-V per aggiungere un altro gruppo o utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15160-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="15160-119">Vedere <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> come aggiungere o rimuovere un amministratore tramite la console di gestione </a> .</span><span class="sxs-lookup"><span data-stu-id="15160-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15160-120">Cmdlet che richiedono un prompt dei comandi con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="15160-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="15160-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="15160-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="15160-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="15160-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="15160-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="15160-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="15160-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="15160-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="15160-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="15160-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="15160-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="15160-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="15160-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="15160-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="15160-128">Send-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="15160-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="15160-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="15160-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="15160-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="15160-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="15160-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="15160-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-132">I cmdlet che gli utenti finali possono eseguire, a meno che non vengano configurati per richiedere un prompt dei comandi con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="15160-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="15160-133">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="15160-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="15160-134">Annulla pubblicazione-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="15160-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="15160-135">Per configurare questi cmdlet in modo da richiedere un prompt dei comandi con privilegi elevati, usare uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="15160-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15160-136">Metodo</span><span class="sxs-lookup"><span data-stu-id="15160-136">Method</span></span></th>
<th align="left"><span data-ttu-id="15160-137">Altre risorse</span><span class="sxs-lookup"><span data-stu-id="15160-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-138">Eseguire il <strong> cmdlet Set-AppvClientConfiguration </strong> con il <strong> parametro-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="15160-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="15160-139">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="15160-140">Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-140">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15160-141">Abilitare l'impostazione di criteri di gruppo "Richiedi pubblica come amministratore" per i client App-V.</span><span class="sxs-lookup"><span data-stu-id="15160-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)"><span data-ttu-id="15160-142">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="15160-142">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="15160-143">Caricamento dei cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-143">Loading the PowerShell cmdlets</span></span>

<span data-ttu-id="15160-144">Per caricare i moduli cmdlet di PowerShell:</span><span class="sxs-lookup"><span data-stu-id="15160-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="15160-145">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="15160-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="15160-146">Digitare uno dei comandi seguenti per caricare i cmdlet per il modulo desiderato:</span><span class="sxs-lookup"><span data-stu-id="15160-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15160-147">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="15160-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="15160-148">Comando per digitare</span><span class="sxs-lookup"><span data-stu-id="15160-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-149">App-V Server</span><span class="sxs-lookup"><span data-stu-id="15160-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-150">Import-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="15160-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15160-151">Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="15160-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-152">Import-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="15160-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-153">Client App-V</span><span class="sxs-lookup"><span data-stu-id="15160-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-154">Import-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="15160-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="15160-155">Ottenere assistenza per i cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="15160-156">A partire da App-V 5,0 SP3, la guida per i cmdlet è disponibile in due formati:</span><span class="sxs-lookup"><span data-stu-id="15160-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15160-157">Formato</span><span class="sxs-lookup"><span data-stu-id="15160-157">Format</span></span></th>
<th align="left"><span data-ttu-id="15160-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15160-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-159">Come modulo scaricabile</span><span class="sxs-lookup"><span data-stu-id="15160-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-160">Per scaricare la guida più recente dopo il download del modulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15160-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="15160-161">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="15160-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="15160-162">Digitare uno dei comandi seguenti per caricare i cmdlet per il modulo desiderato:</span><span class="sxs-lookup"><span data-stu-id="15160-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15160-163">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="15160-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="15160-164">Comando per digitare</span><span class="sxs-lookup"><span data-stu-id="15160-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-165">App-V Server</span><span class="sxs-lookup"><span data-stu-id="15160-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-166">Update-Guida-modulo AppvServer</span><span class="sxs-lookup"><span data-stu-id="15160-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15160-167">Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="15160-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-168">Update-Guida-modulo AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="15160-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15160-169">Client App-V</span><span class="sxs-lookup"><span data-stu-id="15160-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-170">Update-Guida-modulo AppvClient</span><span class="sxs-lookup"><span data-stu-id="15160-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15160-171">In TechNet come pagine Web</span><span class="sxs-lookup"><span data-stu-id="15160-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="15160-172">Vedere il nodo App-V in <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automazione di Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="15160-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="15160-173">Visualizzazione della Guida per un cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="15160-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="15160-174">Per visualizzare la Guida di un cmdlet di PowerShell specifico:</span><span class="sxs-lookup"><span data-stu-id="15160-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="15160-175">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="15160-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="15160-176">Digitare **Get-Help** &lt; *cmdlet* &gt; , ad esempio **Get-Help Publish-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="15160-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="15160-177">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="15160-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="15160-178">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="15160-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="15160-179">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="15160-179">Got an App-V issue?</span></span>** <span data-ttu-id="15160-180">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="15160-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 




