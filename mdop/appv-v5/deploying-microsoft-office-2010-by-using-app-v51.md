---
title: Distribuzione di Microsoft Office 2010 con App-V
description: Distribuzione di Microsoft Office 2010 con App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805866"
---
# <span data-ttu-id="4f806-103">Distribuzione di Microsoft Office 2010 con App-V</span><span class="sxs-lookup"><span data-stu-id="4f806-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="4f806-104">È possibile creare pacchetti di Office 2010 per Microsoft Application Virtualization (App-V) 5,1 usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f806-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="4f806-105">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="4f806-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="4f806-106">Acceleratore pacchetto Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="4f806-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="4f806-107">Supporto di App-V per Office 2010</span><span class="sxs-lookup"><span data-stu-id="4f806-107">App-V support for Office 2010</span></span>


<span data-ttu-id="4f806-108">Nella tabella seguente sono illustrate le versioni di App-V, i metodi di creazione di pacchetti di Office, le licenze supportate e le distribuzioni supportate per Office 2010.</span><span class="sxs-lookup"><span data-stu-id="4f806-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f806-109">Elemento supportato</span><span class="sxs-lookup"><span data-stu-id="4f806-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="4f806-110">Livello di supporto</span><span class="sxs-lookup"><span data-stu-id="4f806-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-111">Versioni App-V supportate</span><span class="sxs-lookup"><span data-stu-id="4f806-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4f806-112">4,6</span><span class="sxs-lookup"><span data-stu-id="4f806-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="4f806-113">5.0</span><span class="sxs-lookup"><span data-stu-id="4f806-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="4f806-114">5,1</span><span class="sxs-lookup"><span data-stu-id="4f806-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-115">Creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="4f806-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4f806-116">Sequenziamento</span><span class="sxs-lookup"><span data-stu-id="4f806-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="4f806-117">Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="4f806-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="4f806-118">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="4f806-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-119">Licenze supportate</span><span class="sxs-lookup"><span data-stu-id="4f806-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-120">Contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="4f806-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-121">Distribuzioni supportate</span><span class="sxs-lookup"><span data-stu-id="4f806-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4f806-122">Desktop</span><span class="sxs-lookup"><span data-stu-id="4f806-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="4f806-123">VDI personale</span><span class="sxs-lookup"><span data-stu-id="4f806-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="4f806-124">RDS</span><span class="sxs-lookup"><span data-stu-id="4f806-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4f806-125">Creazione di Office 2010 App-V 5,1 con il sequencer</span><span class="sxs-lookup"><span data-stu-id="4f806-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="4f806-126">La sequenziazione di Office 2010 è uno dei metodi principali per la creazione di un pacchetto di Office 2010 in App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f806-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="4f806-127">Microsoft ha fornito una ricetta dettagliata tramite un articolo della Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="4f806-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="4f806-128">Per creare un pacchetto di Office 2010 in App-V 5,1, vedere il collegamento seguente per istruzioni dettagliate:</span><span class="sxs-lookup"><span data-stu-id="4f806-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="4f806-129">Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="4f806-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="4f806-130">Creazione di pacchetti di Office 2010 App-V 5,1 con gli acceleratori pacchetto</span><span class="sxs-lookup"><span data-stu-id="4f806-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="4f806-131">I pacchetti di Office 2010 App-V 5,1 possono essere creati tramite acceleratori pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4f806-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="4f806-132">Microsoft ha fornito gli acceleratori pacchetto per la creazione di Office 2010 in Windows 10, Windows 8 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4f806-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="4f806-133">Per creare pacchetti di Office 2010 in App-V con gli acceleratori pacchetto, fare riferimento alle pagine seguenti per accedere all'Acceleratore pacchetto appropriato:</span><span class="sxs-lookup"><span data-stu-id="4f806-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="4f806-134">Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f806-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="4f806-135">Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f806-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="4f806-136">Per istruzioni dettagliate su come creare pacchetti di applicazioni virtuali con gli acceleratori di pacchetti App-V, vedere [come creare un pacchetto di applicazione virtuale usando un Acceleratore pacchetto App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="4f806-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="4f806-137">Distribuzione del pacchetto Microsoft Office per App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f806-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="4f806-138">È possibile distribuire i pacchetti di Office 2010 usando uno dei metodi di distribuzione di App-V seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f806-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="4f806-139">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4f806-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="4f806-140">App-V Server</span><span class="sxs-lookup"><span data-stu-id="4f806-140">App-V server</span></span>

-   <span data-ttu-id="4f806-141">Autonomo tramite i comandi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f806-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="4f806-142">Gestione e personalizzazione dei pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="4f806-142">Office App-V package management and customization</span></span>


<span data-ttu-id="4f806-143">I pacchetti di Office 2010 possono essere gestiti come qualsiasi altro pacchetto App-V 5,1 attraverso i meccanismi di gestione dei pacchetti noti.</span><span class="sxs-lookup"><span data-stu-id="4f806-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="4f806-144">Non sono necessarie istruzioni speciali, ad esempio per aggiungere, pubblicare, annullare la pubblicazione o rimuovere i pacchetti di Office.</span><span class="sxs-lookup"><span data-stu-id="4f806-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="4f806-145">Integrazione di Microsoft Office con Windows</span><span class="sxs-lookup"><span data-stu-id="4f806-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="4f806-146">La tabella seguente include un elenco completo dei punti di integrazione supportati per Office 2010.</span><span class="sxs-lookup"><span data-stu-id="4f806-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f806-147">Punto di estensione</span><span class="sxs-lookup"><span data-stu-id="4f806-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="4f806-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f806-148">Description</span></span></th>
<th align="left"><span data-ttu-id="4f806-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="4f806-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-150">Plug-in di Lync meeting join per Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="4f806-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-151">L'utente può partecipare a riunioni Lync da Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="4f806-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-152">Inviato al driver di stampa di OneNote</span><span class="sxs-lookup"><span data-stu-id="4f806-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-153">L'utente può stampare in OneNote</span><span class="sxs-lookup"><span data-stu-id="4f806-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-154">Sì</span><span class="sxs-lookup"><span data-stu-id="4f806-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-155">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="4f806-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-156">Note collegate in OneNote</span><span class="sxs-lookup"><span data-stu-id="4f806-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-157">Inviare al componente aggiuntivo OneNote Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4f806-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-158">L'utente può inviare a OneNote da IE</span><span class="sxs-lookup"><span data-stu-id="4f806-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-159">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="4f806-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-160">Eccezione del firewall per Lync e Outlook</span><span class="sxs-lookup"><span data-stu-id="4f806-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-161">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="4f806-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-162">Le app e i componenti aggiuntivi nativi possono interagire con Outlook virtuale tramite MAPI</span><span class="sxs-lookup"><span data-stu-id="4f806-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-163">Plug-in di SharePoint per Firefox</span><span class="sxs-lookup"><span data-stu-id="4f806-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-164">L'utente può usare le caratteristiche di SharePoint in Firefox</span><span class="sxs-lookup"><span data-stu-id="4f806-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-165">Applet del pannello di controllo posta</span><span class="sxs-lookup"><span data-stu-id="4f806-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-166">L'utente ottiene l'applet del pannello di controllo della posta in Outlook</span><span class="sxs-lookup"><span data-stu-id="4f806-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-167">Sì</span><span class="sxs-lookup"><span data-stu-id="4f806-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-168">Assembly di interoperabilità primari</span><span class="sxs-lookup"><span data-stu-id="4f806-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-169">Supportare i componenti aggiuntivi gestiti</span><span class="sxs-lookup"><span data-stu-id="4f806-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-170">Gestore della cache dei documenti di Office</span><span class="sxs-lookup"><span data-stu-id="4f806-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-171">Consente la cache dei documenti per le applicazioni di Office</span><span class="sxs-lookup"><span data-stu-id="4f806-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-172">Gestore ricerca protocollo di Outlook</span><span class="sxs-lookup"><span data-stu-id="4f806-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-173">L'utente può eseguire ricerche in Outlook</span><span class="sxs-lookup"><span data-stu-id="4f806-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-174">Sì</span><span class="sxs-lookup"><span data-stu-id="4f806-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f806-175">Controlli Active X:</span><span class="sxs-lookup"><span data-stu-id="4f806-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-176">Per altre informazioni sui controlli ActiveX, vedere <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> riferimenti alle API dei controlli ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="4f806-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="4f806-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-178">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-179">PortalConnect. PersonalSite</span><span class="sxs-lookup"><span data-stu-id="4f806-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-180">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-181">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="4f806-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-182">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="4f806-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-184">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="4f806-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-186">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="4f806-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-188">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="4f806-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-190">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="4f806-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-192">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-193">Sharpoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="4f806-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-194">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="4f806-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-196">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-197">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="4f806-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-198">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-199">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="4f806-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-200">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-201">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="4f806-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-202">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-203">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="4f806-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-204">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="4f806-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="4f806-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-206">Controllo Active X</span><span class="sxs-lookup"><span data-stu-id="4f806-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="4f806-207">Helper del browser OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="4f806-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-208">Controllo Active X]</span><span class="sxs-lookup"><span data-stu-id="4f806-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f806-209">Sovrapposizioni di icone di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="4f806-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f806-210">L'icona della shell di Windows Explorer si sovrappone quando gli utenti esaminano le cartelle di OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="4f806-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4f806-211">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4f806-211">Additional resources</span></span>


**<span data-ttu-id="4f806-212">Office 2013 App-V pacchetti risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4f806-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="4f806-213">Scenari supportati per la distribuzione di Microsoft Office come pacchetto di App-V sequenziato</span><span class="sxs-lookup"><span data-stu-id="4f806-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="4f806-214">Pacchetti App-V di Office 2010</span><span class="sxs-lookup"><span data-stu-id="4f806-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="4f806-215">Microsoft Office 2010-Kit di sequenziazione per Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="4f806-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="4f806-216">Problemi noti quando si crea o si usa un pacchetto di App-V 5,0 Office 2010</span><span class="sxs-lookup"><span data-stu-id="4f806-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="4f806-217">Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="4f806-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="4f806-218">Gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="4f806-218">Connection Groups</span></span>**

[<span data-ttu-id="4f806-219">Distribuzione di gruppi di connessioni in Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="4f806-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="4f806-220">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="4f806-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="4f806-221">Configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="4f806-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="4f806-222">Informazioni sulla configurazione dinamica di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f806-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





