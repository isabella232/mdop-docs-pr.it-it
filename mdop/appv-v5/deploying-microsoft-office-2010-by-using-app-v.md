---
title: Distribuzione di Microsoft Office 2010 con App-V
description: Distribuzione di Microsoft Office 2010 con App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805877"
---
# <span data-ttu-id="3d3c6-103">Distribuzione di Microsoft Office 2010 con App-V</span><span class="sxs-lookup"><span data-stu-id="3d3c6-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="3d3c6-104">È possibile creare pacchetti di Office 2010 per Application Virtualization 5,0 usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d3c6-104">You can create Office 2010 packages for Application Virtualization 5.0 using one of the following methods:</span></span>

-   <span data-ttu-id="3d3c6-105">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="3d3c6-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="3d3c6-106">Acceleratore pacchetto Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="3d3c6-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="3d3c6-107">Supporto di App-V per Office 2010</span><span class="sxs-lookup"><span data-stu-id="3d3c6-107">App-V support for Office 2010</span></span>


<span data-ttu-id="3d3c6-108">Nella tabella seguente sono illustrate le versioni di App-V, i metodi di creazione di pacchetti di Office, le licenze supportate e le distribuzioni supportate per Office 2010.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d3c6-109">Elemento supportato</span><span class="sxs-lookup"><span data-stu-id="3d3c6-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="3d3c6-110">Livello di supporto</span><span class="sxs-lookup"><span data-stu-id="3d3c6-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-111">Versioni App-V supportate</span><span class="sxs-lookup"><span data-stu-id="3d3c6-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d3c6-112">4,6</span><span class="sxs-lookup"><span data-stu-id="3d3c6-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="3d3c6-113">5.0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-113">5.0</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-114">Creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="3d3c6-114">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d3c6-115">Sequenziamento</span><span class="sxs-lookup"><span data-stu-id="3d3c6-115">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="3d3c6-116">Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="3d3c6-116">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="3d3c6-117">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="3d3c6-117">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-118">Licenze supportate</span><span class="sxs-lookup"><span data-stu-id="3d3c6-118">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-119">Contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="3d3c6-119">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-120">Distribuzioni supportate</span><span class="sxs-lookup"><span data-stu-id="3d3c6-120">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3d3c6-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="3d3c6-121">Desktop</span></span></p></li>
<li><p><span data-ttu-id="3d3c6-122">VDI personale</span><span class="sxs-lookup"><span data-stu-id="3d3c6-122">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="3d3c6-123">RDS</span><span class="sxs-lookup"><span data-stu-id="3d3c6-123">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3d3c6-124">Creazione di Office 2010 App-V 5,0 con il sequencer</span><span class="sxs-lookup"><span data-stu-id="3d3c6-124">Creating Office 2010 App-V 5.0 using the sequencer</span></span>


<span data-ttu-id="3d3c6-125">La sequenziazione di Office 2010 è uno dei metodi principali per la creazione di un pacchetto di Office 2010 in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-125">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.0.</span></span> <span data-ttu-id="3d3c6-126">Microsoft ha fornito una ricetta dettagliata tramite un articolo della Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-126">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="3d3c6-127">Per creare un pacchetto di Office 2010 in App-V 5,0, vedere il collegamento seguente per istruzioni dettagliate:</span><span class="sxs-lookup"><span data-stu-id="3d3c6-127">To create an Office 2010 package on App-V 5.0, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="3d3c6-128">Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-128">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="3d3c6-129">Creazione di pacchetti di Office 2010 App-V 5,0 con gli acceleratori pacchetto</span><span class="sxs-lookup"><span data-stu-id="3d3c6-129">Creating Office 2010 App-V 5.0 packages using package accelerators</span></span>


<span data-ttu-id="3d3c6-130">I pacchetti di Office 2010 App-V 5,0 possono essere creati tramite acceleratori pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-130">Office 2010 App-V 5.0 packages can be created through package accelerators.</span></span> <span data-ttu-id="3d3c6-131">Microsoft ha fornito gli acceleratori pacchetto per la creazione di Office 2010 in Windows 8 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-131">Microsoft has provided package accelerators for creating Office 2010 on Windows 8 and Windows 7.</span></span> <span data-ttu-id="3d3c6-132">Per creare pacchetti di Office 2010 in App-V con gli acceleratori pacchetto, fare riferimento alle pagine seguenti per accedere all'Acceleratore pacchetto appropriato:</span><span class="sxs-lookup"><span data-stu-id="3d3c6-132">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="3d3c6-133">Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 8</span><span class="sxs-lookup"><span data-stu-id="3d3c6-133">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="3d3c6-134">Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d3c6-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="3d3c6-135">Per istruzioni dettagliate su come creare pacchetti di applicazioni virtuali con gli acceleratori di pacchetti App-V, vedere [come creare un pacchetto di applicazione virtuale usando un Acceleratore pacchetto App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span><span class="sxs-lookup"><span data-stu-id="3d3c6-135">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span></span>

## <span data-ttu-id="3d3c6-136">Distribuzione del pacchetto Microsoft Office per App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-136">Deploying the Microsoft Office package for App-V 5.0</span></span>


<span data-ttu-id="3d3c6-137">È possibile distribuire i pacchetti di Office 2010 usando uno dei metodi di distribuzione di App-V seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d3c6-137">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="3d3c6-138">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3d3c6-138">System Center Configuration Manager</span></span>

-   <span data-ttu-id="3d3c6-139">App-V Server</span><span class="sxs-lookup"><span data-stu-id="3d3c6-139">App-V server</span></span>

-   <span data-ttu-id="3d3c6-140">Autonomo tramite i comandi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="3d3c6-140">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="3d3c6-141">Gestione e personalizzazione dei pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="3d3c6-141">Office App-V package management and customization</span></span>


<span data-ttu-id="3d3c6-142">I pacchetti di Office 2010 possono essere gestiti come qualsiasi altro pacchetto App-V 5,0 attraverso i meccanismi di gestione dei pacchetti noti.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-142">Office 2010 packages can be managed like any other App-V 5.0 packages through known package management mechanisms.</span></span> <span data-ttu-id="3d3c6-143">Non sono necessarie istruzioni speciali, ad esempio per aggiungere, pubblicare, annullare la pubblicazione o rimuovere i pacchetti di Office.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-143">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="3d3c6-144">Integrazione di Microsoft Office con Windows</span><span class="sxs-lookup"><span data-stu-id="3d3c6-144">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="3d3c6-145">La tabella seguente include un elenco completo dei punti di integrazione supportati per Office 2010.</span><span class="sxs-lookup"><span data-stu-id="3d3c6-145">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d3c6-146">Punto di estensione</span><span class="sxs-lookup"><span data-stu-id="3d3c6-146">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="3d3c6-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d3c6-147">Description</span></span></th>
<th align="left"><span data-ttu-id="3d3c6-148">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3d3c6-148">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-149">Plug-in di Lync meeting join per Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="3d3c6-149">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-150">L'utente può partecipare a riunioni Lync da Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="3d3c6-150">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-151">Inviato al driver di stampa di OneNote</span><span class="sxs-lookup"><span data-stu-id="3d3c6-151">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-152">L'utente può stampare in OneNote</span><span class="sxs-lookup"><span data-stu-id="3d3c6-152">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-153">Sì</span><span class="sxs-lookup"><span data-stu-id="3d3c6-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-154">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="3d3c6-154">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-155">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="3d3c6-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-156">Inviare al componente aggiuntivo OneNote Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="3d3c6-156">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-157">L'utente può inviare a OneNote da IE</span><span class="sxs-lookup"><span data-stu-id="3d3c6-157">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-158">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3c6-158">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-159">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3c6-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-160">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3c6-160">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-161">Le app e i componenti aggiuntivi nativi possono interagire con Outlook virtuale tramite MAPI</span><span class="sxs-lookup"><span data-stu-id="3d3c6-161">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-162">Plug-in di SharePoint per Firefox</span><span class="sxs-lookup"><span data-stu-id="3d3c6-162">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-163">L'utente può usare le caratteristiche di SharePoint in Firefox</span><span class="sxs-lookup"><span data-stu-id="3d3c6-163">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-164">Applet del pannello di controllo posta</span><span class="sxs-lookup"><span data-stu-id="3d3c6-164">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-165">L'utente ottiene l'applet del pannello di controllo della posta in Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3c6-165">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-166">Sì</span><span class="sxs-lookup"><span data-stu-id="3d3c6-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-167">Assembly di interoperabilità primari</span><span class="sxs-lookup"><span data-stu-id="3d3c6-167">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-168">Supportare i componenti aggiuntivi gestiti</span><span class="sxs-lookup"><span data-stu-id="3d3c6-168">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-169">Gestore della cache dei documenti di Office</span><span class="sxs-lookup"><span data-stu-id="3d3c6-169">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-170">Consente la cache dei documenti per le applicazioni di Office</span><span class="sxs-lookup"><span data-stu-id="3d3c6-170">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-171">Gestore ricerca protocollo di Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3c6-171">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-172">L'utente può eseguire ricerche in Outlook</span><span class="sxs-lookup"><span data-stu-id="3d3c6-172">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-173">Sì</span><span class="sxs-lookup"><span data-stu-id="3d3c6-173">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3d3c6-174">Controlli Active X:</span><span class="sxs-lookup"><span data-stu-id="3d3c6-174">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-175">Per altre informazioni sui controlli ActiveX, vedere <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> riferimenti alle API dei controlli ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="3d3c6-175">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-176">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="3d3c6-176">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-177">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-177">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-178">PortalConnect. PersonalSite</span><span class="sxs-lookup"><span data-stu-id="3d3c6-178">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-179">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-179">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-180">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="3d3c6-180">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-181">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-181">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-182">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="3d3c6-182">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-183">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-183">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-184">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="3d3c6-184">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-185">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-185">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-186">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="3d3c6-186">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-187">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-187">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-188">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="3d3c6-188">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-189">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-189">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-190">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="3d3c6-190">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-191">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-191">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-192">Sharpoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="3d3c6-192">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-193">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-193">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-194">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="3d3c6-194">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-195">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-195">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-196">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="3d3c6-196">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-197">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-197">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-198">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="3d3c6-198">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-199">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-199">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-200">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="3d3c6-200">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-201">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-201">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-202">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="3d3c6-202">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-203">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-203">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3d3c6-204">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="3d3c6-204">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-205">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="3d3c6-205">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3d3c6-206">Helper del browser OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3d3c6-206">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-207">Controllo Active X]</span><span class="sxs-lookup"><span data-stu-id="3d3c6-207">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3d3c6-208">Sovrapposizioni di icone di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3d3c6-208">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="3d3c6-209">L'icona della shell di Windows Explorer si sovrappone quando gli utenti esaminano le cartelle di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3d3c6-209">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3d3c6-210">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3d3c6-210">Additional resources</span></span>


**<span data-ttu-id="3d3c6-211">Office 2013 App-V 5,0 packages 5,0 risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3d3c6-211">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="3d3c6-212">Scenari supportati per la distribuzione di Microsoft Office come pacchetto di App-V sequenziato</span><span class="sxs-lookup"><span data-stu-id="3d3c6-212">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="3d3c6-213">Pacchetti app di Office 2010-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-213">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="3d3c6-214">Microsoft Office 2010-Kit di sequenziazione per Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-214">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="3d3c6-215">Problemi noti quando si crea o si usa un pacchetto di App-V 5,0 Office 2010</span><span class="sxs-lookup"><span data-stu-id="3d3c6-215">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="3d3c6-216">Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-216">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="3d3c6-217">Gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="3d3c6-217">Connection Groups</span></span>**

[<span data-ttu-id="3d3c6-218">Distribuzione di gruppi di connessioni in Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="3d3c6-218">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="3d3c6-219">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="3d3c6-219">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="3d3c6-220">Configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="3d3c6-220">Dynamic Configuration</span></span>**

[<span data-ttu-id="3d3c6-221">Informazioni sulla configurazione dinamica di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3d3c6-221">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)






 

 





