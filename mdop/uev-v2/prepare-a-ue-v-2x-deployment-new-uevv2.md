---
title: Preparare una distribuzione UE-V 2. x
description: Preparare una distribuzione UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826425"
---
# <span data-ttu-id="e6f3c-103">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="e6f3c-104">La pianificazione e la preparazione da eseguire prima di distribuire Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1 è una soluzione per la sincronizzazione delle impostazioni tra i dispositivi a cui gli utenti accedono nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="e6f3c-105">Questo argomento consente di determinare il tipo di distribuzione che si sta eseguendo e la preparazione che è possibile eseguire in anticipo in modo che la distribuzione abbia successo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="e6f3c-106">Prima di tutto, esaminiamo le attività da eseguire per distribuire UE-V:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="e6f3c-107">Pianificare la distribuzione di UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="e6f3c-108">Prima di distribuire qualsiasi elemento, un buon primo passaggio consiste nell'eseguire un po' di pianificazione in modo da determinare quali funzionalità di UE-V verranno distribuite.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="e6f3c-109">Quindi, se si lascia questa pagina, assicurarsi di tornare e leggere le informazioni di pianificazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="e6f3c-110">Distribuire le funzionalità necessarie per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="e6f3c-111">Ogni distribuzione UE-V richiede queste attività:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="e6f3c-112">Definire una posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="e6f3c-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="e6f3c-113">Decidere come distribuire l'agente UE-V e gestire le configurazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="e6f3c-114">[Installare l'agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) in tutti i computer degli utenti che necessitano di impostazioni sincronizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="e6f3c-115">Facoltativamente, è possibile [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="e6f3c-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="e6f3c-116">La pianificazione consentirà di capire se si vuole che UE-V supporti la sincronizzazione delle impostazioni per le applicazioni personalizzate (di terze parti o line-of-business), che richiede queste funzionalità di UE-V:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="e6f3c-117">[Installare il generatore di UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) in modo da poter creare, modificare e convalidare i modelli di posizione delle impostazioni personalizzati necessari per sincronizzare le impostazioni delle applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="e6f3c-118">[Creare modelli di posizione delle impostazioni personalizzate](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) usando il generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="e6f3c-119">[Distribuire un catalogo di modelli di impostazioni UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) che si usa per archiviare i modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="e6f3c-120">Questo diagramma flusso di lavoro offre una comprensione di alto livello di una distribuzione UE-V e delle decisioni che determinano la modalità di distribuzione di UE-V nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="e6f3c-122">**Pianificazione di una distribuzione di UE-V:** Prima di tutto, devi pianificare la pianificazione in modo da determinare i componenti UE-V che dovrai distribuire.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="e6f3c-123">La pianificazione di una distribuzione UE-V implica questi elementi:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="e6f3c-124">Decidere se sincronizzare le impostazioni per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="e6f3c-125">In questo modo viene determinato se si installerà il generatore UE-V durante la distribuzione, che consente di creare modelli di posizione delle impostazioni personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="e6f3c-126">Si tratta delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-126">It involves the following:</span></span>

    <span data-ttu-id="e6f3c-127">Esaminare le [Impostazioni sincronizzate automaticamente in una distribuzione di UE-V](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="e6f3c-128">[Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="e6f3c-129">Esaminare [altre considerazioni per la distribuzione di UE-V](#considerations), ad esempio disponibilità elevata e pianificazione della capacità.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="e6f3c-130">Confermare i prerequisiti e le configurazioni supportate per la versione UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="e6f3c-131">Decidere se sincronizzare le impostazioni per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="e6f3c-132">In una distribuzione di UE-V vengono sincronizzate automaticamente molte impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="e6f3c-133">Ma è anche possibile personalizzare UE-V per sincronizzare le impostazioni per altre applicazioni, ad esempio le app line-of-business e di terze parti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="e6f3c-134">Decidere se si vuole che la sincronizzazione delle impostazioni per le applicazioni personalizzate da parte di UE-V sia probabilmente la parte più importante della pianificazione della distribuzione di UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="e6f3c-135">Gli argomenti di questa sezione ti aiuteranno a prendere questa decisione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="e6f3c-136">Impostazioni sincronizzate automaticamente in una distribuzione di UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="e6f3c-137">In questa sezione vengono fornite informazioni sulle impostazioni sincronizzate per impostazione predefinita in UE-V, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="e6f3c-138">Applicazioni desktop le cui impostazioni sono sincronizzate per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e6f3c-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="e6f3c-139">Impostazioni desktop di Windows sincronizzate per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e6f3c-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="e6f3c-140">Dichiarazione di supporto per la sincronizzazione delle impostazioni dell'app Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="e6f3c-141">Vedere [modelli di impostazioni per la virtualizzazione dell'esperienza utente (UE-v) per Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) per scaricare un elenco completo delle impostazioni specifiche di microsoft Office 2013, microsoft Office 2010 e microsoft Office 2007 sincronizzate da UE-v.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="e6f3c-142">Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2,1 e UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="e6f3c-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="e6f3c-143">Quando si installa l'agente UE-V 2,1 o 2,1 SP1, viene registrato un gruppo predefinito di modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="e6f3c-144">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="e6f3c-144">Tip</span></span>**  
<span data-ttu-id="e6f3c-145">**Sincronizzazione delle impostazioni di Microsoft Office 2007** -in UE-V 2,1 e 2,1 SP1, un modello di posizione delle impostazioni non è più incluso per impostazione predefinita per le applicazioni di Office 2007.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="e6f3c-146">Tuttavia, è comunque possibile usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e ottenere i modelli dalla [raccolta modelli di UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e6f3c-147">Categoria applicazione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-149">Applicazioni di Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="e6f3c-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</span><span class="sxs-lookup"><span data-stu-id="e6f3c-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="e6f3c-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="e6f3c-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="e6f3c-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="e6f3c-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="e6f3c-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="e6f3c-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="e6f3c-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="e6f3c-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="e6f3c-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="e6f3c-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="e6f3c-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="e6f3c-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-164">Applicazioni di Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="e6f3c-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</span><span class="sxs-lookup"><span data-stu-id="e6f3c-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="e6f3c-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="e6f3c-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="e6f3c-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="e6f3c-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="e6f3c-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="e6f3c-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="e6f3c-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="e6f3c-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="e6f3c-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="e6f3c-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="e6f3c-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="e6f3c-178">Microsoft Office 2013 Upload Center</span><span class="sxs-lookup"><span data-stu-id="e6f3c-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="e6f3c-179">Microsoft OneDrive for Business 2013</span><span class="sxs-lookup"><span data-stu-id="e6f3c-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="e6f3c-180">I modelli di posizione delle impostazioni di Microsoft Office 2013 della versione UE-V 2,1 e 2,1 SP1 includono il supporto per la firma di Outlook migliorato.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="e6f3c-181">È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e6f3c-182">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-182">Note</span></span></strong><br/><p><span data-ttu-id="e6f3c-183">È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="e6f3c-184">Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-185">Opzioni del browser: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="e6f3c-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-186">Preferiti, Home page, schede e barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e6f3c-187">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-187">Note</span></span></strong><br/><p><span data-ttu-id="e6f3c-188">UE-V non esegue la roaming delle impostazioni per i cookie di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-189">Accessori per Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-190">Microsoft Calculator, blocco note, WordPad.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e6f3c-191">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-191">Note</span></span>**  
<span data-ttu-id="e6f3c-192">UE-V 2,1 SP1 non sincronizza le impostazioni tra la calcolatrice Microsoft in Windows 10 e la calcolatrice Microsoft nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="e6f3c-193">Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="e6f3c-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="e6f3c-194">Quando si installa l'agente UE-V 2,0, viene registrato un gruppo predefinito di modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="e6f3c-195">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="e6f3c-195">Tip</span></span>**  
<span data-ttu-id="e6f3c-196">**Sincronizzazione delle impostazioni di Microsoft office 2013** -in UE-v 2,0 un modello di posizione delle impostazioni non è incluso per impostazione predefinita per le applicazioni di Office 2013, ma è disponibile per il download dalla [raccolta modelli di UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="e6f3c-197">La [sincronizzazione di office 2013 con UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornisce informazioni dettagliate sui modelli supportati che sincronizzano le impostazioni di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e6f3c-198">Categoria applicazione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-200">Applicazioni di Microsoft Office 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="e6f3c-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</span><span class="sxs-lookup"><span data-stu-id="e6f3c-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="e6f3c-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="e6f3c-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="e6f3c-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="e6f3c-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="e6f3c-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="e6f3c-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="e6f3c-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="e6f3c-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="e6f3c-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="e6f3c-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="e6f3c-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="e6f3c-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-214">Applicazioni di Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="e6f3c-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</span><span class="sxs-lookup"><span data-stu-id="e6f3c-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="e6f3c-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="e6f3c-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="e6f3c-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="e6f3c-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="e6f3c-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="e6f3c-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="e6f3c-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="e6f3c-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="e6f3c-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="e6f3c-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="e6f3c-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="e6f3c-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="e6f3c-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-229">Opzioni del browser: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="e6f3c-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-230">Preferiti, Home page, schede e barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e6f3c-231">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-231">Note</span></span></strong><br/><p><span data-ttu-id="e6f3c-232">UE-V non esegue la roaming delle impostazioni per i cookie di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-233">Accessori per Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-234">Microsoft Calculator, blocco note, WordPad.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="e6f3c-235">Impostazioni di Windows sincronizzate per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e6f3c-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="e6f3c-236">UE-V include i modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

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
<th align="left"><span data-ttu-id="e6f3c-237">impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-238">Description</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-239">Applicare il</span><span class="sxs-lookup"><span data-stu-id="e6f3c-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-240">Esporta in</span><span class="sxs-lookup"><span data-stu-id="e6f3c-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-241">Stato predefinito</span><span class="sxs-lookup"><span data-stu-id="e6f3c-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-242">Sfondo del desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-243">Sfondo del desktop attualmente attivo o sfondo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-244">Eventi attività pianificati per l'accesso, l'apertura, la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-245">Disconnessione, blocco, disconnessione remota, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o nell'intervallo di attività pianificato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-246">Abilitato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-247">Accessibilità</span><span class="sxs-lookup"><span data-stu-id="e6f3c-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-248">Impostazioni di accessibilità e input, Microsoft Magnifier, Assistente vocale e tastiera su schermo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-249">Solo accesso.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-250">Disconnessione, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o nell'intervallo di attività pianificato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-251">Abilitato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-252">Impostazioni desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-253">Menu Start e impostazioni della barra delle applicazioni, Opzioni cartella, icone desktop predefinite, clock aggiuntivi e impostazioni area geografica e lingua.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-254">Solo accesso.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-255">Disconnessione, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o in un'attività pianificata</span><span class="sxs-lookup"><span data-stu-id="e6f3c-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-256">Abilitato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e6f3c-257">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-257">Note</span></span>**  
<span data-ttu-id="e6f3c-258">A partire da Windows 8, UE-V non esegue la roaming delle impostazioni relative alla schermata Start, ad esempio gli elementi e le posizioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="e6f3c-259">Inoltre, UE-V non supporta la sincronizzazione di elementi della barra delle applicazioni bloccati o di collegamenti di file di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="e6f3c-260">Importante</span><span class="sxs-lookup"><span data-stu-id="e6f3c-260">Important</span></span>**  
<span data-ttu-id="e6f3c-261">UE-V 2,1 SP1 si aggira sulle impostazioni della barra delle applicazioni tra i dispositivi Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="e6f3c-262">Tuttavia, UE-V non sincronizza le impostazioni della barra delle applicazioni tra dispositivi e dispositivi Windows 10 in cui sono in uso sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e6f3c-263">Gruppo di impostazioni</span><span class="sxs-lookup"><span data-stu-id="e6f3c-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-264">Categoria</span><span class="sxs-lookup"><span data-stu-id="e6f3c-264">Category</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-265">Catturare</span><span class="sxs-lookup"><span data-stu-id="e6f3c-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="e6f3c-266">Applica</span><span class="sxs-lookup"><span data-stu-id="e6f3c-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e6f3c-267">Impostazioni applicazione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-268">App di Windows  </span><span class="sxs-lookup"><span data-stu-id="e6f3c-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-269">Chiudi app</span><span class="sxs-lookup"><span data-stu-id="e6f3c-269">Close app</span></span></p>
<p><span data-ttu-id="e6f3c-270">Evento di modifica delle impostazioni dell'app Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-271">Avviare l'app UE-V monitor all'avvio</span><span class="sxs-lookup"><span data-stu-id="e6f3c-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="e6f3c-272">Aprire l'app</span><span class="sxs-lookup"><span data-stu-id="e6f3c-272">Open app</span></span></p>
<p><span data-ttu-id="e6f3c-273">Evento di modifica delle impostazioni dell'app Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="e6f3c-274">Arrivo di un pacchetto di impostazioni</span><span class="sxs-lookup"><span data-stu-id="e6f3c-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-275">Applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-276">Applicazione chiusa</span><span class="sxs-lookup"><span data-stu-id="e6f3c-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-277">L'applicazione si apre e si chiude</span><span class="sxs-lookup"><span data-stu-id="e6f3c-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e6f3c-278">Impostazioni desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-279">Sfondo del desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-280">Blocco o disconnessione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-281">Accesso, sblocco, connessione remota, notifica del nuovo arrivo del pacchetto, l'utente fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o viene eseguita un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-282">Accesso facilitato (comune-accessibilità, Assistente vocale, lente di ingrandimento, tastiera su schermo)</span><span class="sxs-lookup"><span data-stu-id="e6f3c-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-283">Blocco o disconnessione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-284">Accesso</span><span class="sxs-lookup"><span data-stu-id="e6f3c-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-285">Accesso facilitato (Shell-audio, accessibilità, tastiera, mouse)</span><span class="sxs-lookup"><span data-stu-id="e6f3c-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-286">Blocco o disconnessione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-287">Accesso, sblocco, connessione remota, notifica del nuovo arrivo del pacchetto, l'utente fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o viene eseguita un'attività pianificata</span><span class="sxs-lookup"><span data-stu-id="e6f3c-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-288">Impostazioni desktop</span><span class="sxs-lookup"><span data-stu-id="e6f3c-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-289">Blocco o disconnessione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-290">Accesso</span><span class="sxs-lookup"><span data-stu-id="e6f3c-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e6f3c-291">UE-V-supporto per le app di Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="e6f3c-292">Per le app di Windows, lo sviluppatore di app specifica le impostazioni sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="e6f3c-293">Puoi specificare quali app di Windows sono abilitate per la sincronizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="e6f3c-294">Per visualizzare un elenco di app di Windows che possono sincronizzare le impostazioni in un computer con il nome della famiglia di pacchetti, lo stato abilitato e l'origine abilitata, al prompt dei comandi di Windows PowerShell immettere:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="e6f3c-295">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-295">Note</span></span>**  
<span data-ttu-id="e6f3c-296">A partire da Windows 8, UE-V non sincronizza le impostazioni delle app di Windows se l'utente del dominio collega le proprie credenziali di accesso al proprio account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="e6f3c-297">Questo collegamento sincronizza le impostazioni con Microsoft OneDrive in modo da UE-V, che disabilita la sincronizzazione delle impostazioni delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="e6f3c-298">UE-V-supporto per le stampanti mobili</span><span class="sxs-lookup"><span data-stu-id="e6f3c-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="e6f3c-299">UE-V 2,1 SP1 consente alle stampanti di rete di spostarsi tra i dispositivi in modo che l'utente abbia accesso alle stampanti di rete quando si è connessi a qualsiasi dispositivo della rete.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="e6f3c-300">Questo include il roaming della stampante impostata come predefinita.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="e6f3c-301">La stampante in roaming in UE-V richiede uno di questi scenari:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="e6f3c-302">Il server di stampa può scaricare il driver necessario quando si sposta in roaming su un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="e6f3c-303">Il driver per la stampante di rete mobile è preinstallato in qualsiasi dispositivo che deve accedere alla stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="e6f3c-304">Il driver della stampante può essere ottenuto da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="e6f3c-305">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-305">Note</span></span>**  
<span data-ttu-id="e6f3c-306">La funzionalità di roaming della stampante UE-V **non** esegue la roaming delle impostazioni o delle preferenze della stampante, ad esempio la stampa fronte-retro.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="e6f3c-307">Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni</span><span class="sxs-lookup"><span data-stu-id="e6f3c-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="e6f3c-308">Dopo aver esaminato le impostazioni sincronizzate automaticamente in una distribuzione di UE-V, si vuole decidere se sincronizzare le impostazioni per altre applicazioni, perché determina la modalità di distribuzione di UE-V in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="e6f3c-309">In qualità di amministratore, quando si considerano le applicazioni desktop da includere nella soluzione UE-V, valutare quali impostazioni possono essere personalizzate dagli utenti e come e dove l'applicazione archivia le proprie impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="e6f3c-310">Non tutte le applicazioni desktop hanno impostazioni che possono essere personalizzate o che sono personalizzate in routine dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="e6f3c-311">Inoltre, non tutte le impostazioni delle applicazioni desktop possono essere sincronizzate in modo sicuro in più computer o ambienti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="e6f3c-312">In generale, è possibile sincronizzare le impostazioni che soddisfano i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="e6f3c-313">Impostazioni archiviate in percorsi accessibili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="e6f3c-314">Ad esempio, non sincronizzare le impostazioni archiviate in system32 o all'esterno della sezione HKEY \ _CURRENT \ _USER (HKCU) del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="e6f3c-315">Impostazioni non specifiche per il computer specifico.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="e6f3c-316">Ad esempio, Escludi configurazioni di rete o hardware.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="e6f3c-317">Impostazioni che è possibile sincronizzare tra computer senza rischio di dati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="e6f3c-318">Ad esempio, non usare le impostazioni archiviate in un file di database.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="e6f3c-319">Elenco di controllo per la valutazione delle applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="e6f3c-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="e6f3c-320">Se si è deciso di usare le impostazioni sincronizzate per altre applicazioni, è possibile utilizzare questo elenco di controllo per individuare le applicazioni che si vogliono includere.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="e6f3c-321">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-322">Questa applicazione contiene le impostazioni che l'utente può personalizzare?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-323">È importante per l'utente che queste impostazioni siano sincronizzate?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-324">Queste impostazioni utente sono già gestite da una soluzione dei criteri di gestione o impostazioni delle applicazioni?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="e6f3c-325">UE-V applica le impostazioni dell'applicazione all'avvio dell'applicazione e alle impostazioni di Windows agli eventi logon, Unlock o Connect remoto.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="e6f3c-326">Se si usa UE-V con altre soluzioni di condivisione delle impostazioni, gli utenti potrebbero riscontrare incongruenze tra le impostazioni sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-327">Le impostazioni dell'applicazione sono specifiche per il computer?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="e6f3c-328">Le preferenze e le personalizzazioni dell'applicazione associate all'hardware o a configurazioni di computer specifiche non vengono sincronizzate in modo coerente tra le sessioni e possono causare un'esperienza di applicazione insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-329">Le impostazioni dell'archivio applicazioni si trovano nella directory Program Files o nella directory di file che si trova nella directory Users <strong> </strong> [nome utente] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="e6f3c-330">I dati dell'applicazione archiviati in uno di questi percorsi in genere non devono essere sincronizzati con l'utente, perché questi dati sono specifici del computer o perché i dati sono troppo grandi per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-331">L'applicazione archivia le impostazioni in un file che contiene altri dati dell'applicazione che non devono essere sincronizzati?</span><span class="sxs-lookup"><span data-stu-id="e6f3c-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="e6f3c-332">UE-V sincronizza i file come unità singola.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="e6f3c-333">Se le impostazioni sono archiviate in file che includono dati dell'applicazione diversi dalle impostazioni, la sincronizzazione di questi dati aggiuntivi può causare un'esperienza di applicazione insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="e6f3c-334">Dimensioni dei file che contengono le impostazioni</span><span class="sxs-lookup"><span data-stu-id="e6f3c-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="e6f3c-335">Le prestazioni della sincronizzazione delle impostazioni possono essere influenzate da file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="e6f3c-336">L'inclusione di file di grandi dimensioni può influire sulle prestazioni della sincronizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="e6f3c-337">Altre considerazioni durante la preparazione di una distribuzione UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="e6f3c-338">È consigliabile considerare questi elementi anche quando si sta preparando la distribuzione di UE-V:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="e6f3c-339">Gestione della sincronizzazione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="e6f3c-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="e6f3c-340">Sincronizzazione delle impostazioni dell'app Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="e6f3c-341">Modelli di posizione delle impostazioni UE-V personalizzati</span><span class="sxs-lookup"><span data-stu-id="e6f3c-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="e6f3c-342">Configurazioni delle impostazioni utente non intenzionali</span><span class="sxs-lookup"><span data-stu-id="e6f3c-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="e6f3c-343">Prestazioni e capacità</span><span class="sxs-lookup"><span data-stu-id="e6f3c-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="e6f3c-344">Disponibilità elevata</span><span class="sxs-lookup"><span data-stu-id="e6f3c-344">High availability</span></span>](#high)

-   [<span data-ttu-id="e6f3c-345">Sincronizzazione di un orologio del computer</span><span class="sxs-lookup"><span data-stu-id="e6f3c-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="e6f3c-346">Gestione della sincronizzazione delle credenziali in UE-V 2,1 e UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="e6f3c-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="e6f3c-347">Molte applicazioni aziendali, tra cui Microsoft Outlook e Lync, richiedono agli utenti le credenziali di dominio all'accesso.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="e6f3c-348">Gli utenti hanno la possibilità di salvare le credenziali su disco per evitare di dover immetterle ogni volta che aprono queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="e6f3c-349">Abilitazione della sincronizzazione delle credenziali mobili consente agli utenti di salvare le proprie credenziali in un computer ed evitare di reimmetterle in tutti i computer usati nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="e6f3c-350">Gli utenti possono sincronizzare alcune credenziali di dominio con UE-V 2,1 e 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="e6f3c-351">Importante</span><span class="sxs-lookup"><span data-stu-id="e6f3c-351">Important</span></span>**  
<span data-ttu-id="e6f3c-352">La sincronizzazione delle credenziali è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="e6f3c-353">Per implementare questa funzionalità, è necessario abilitare esplicitamente la sincronizzazione delle credenziali durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="e6f3c-354">UE-V 2,1 e 2,1 SP1 possono sincronizzare le credenziali aziendali, ma non le credenziali di roaming destinate solo all'uso nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="e6f3c-355">Le credenziali sono impostazioni sincrone, ovvero vengono applicate al profilo la prima volta che si accede al computer dopo la sincronizzazione di UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="e6f3c-356">La sincronizzazione delle credenziali è gestita dal modello di posizione delle impostazioni, che è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="e6f3c-357">Puoi abilitare o disabilitare questo modello con gli stessi metodi usati per altri modelli.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="e6f3c-358">L'identificatore di modello per questa caratteristica è RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="e6f3c-359">Importante</span><span class="sxs-lookup"><span data-stu-id="e6f3c-359">Important</span></span>**  
<span data-ttu-id="e6f3c-360">Se si usano le credenziali di Active Directory in roaming nell'ambiente, è consigliabile non abilitare il modello di credenziali comuni UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="e6f3c-361">Usare uno di questi metodi per abilitare la sincronizzazione delle credenziali:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="e6f3c-362">Centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="e6f3c-362">Company Settings Center</span></span>

-   <span data-ttu-id="e6f3c-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6f3c-363">PowerShell</span></span>

-   <span data-ttu-id="e6f3c-364">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e6f3c-364">Group Policy</span></span>

**<span data-ttu-id="e6f3c-365">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-365">Note</span></span>**  
<span data-ttu-id="e6f3c-366">Le credenziali vengono crittografate durante la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="e6f3c-367">[Centro impostazioni società](https://technet.microsoft.com/library/dn458903.aspx)**:** Selezionare la casella di controllo impostazioni credenziali comuni in impostazioni di Windows per abilitare la sincronizzazione delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="e6f3c-368">Deselezionare la casella di controllo per disattivarla.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="e6f3c-369">Questa casella di controllo viene visualizzata solo nel centro impostazioni società se l'account non è configurato per la sincronizzazione delle impostazioni con un account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="e6f3c-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** questo cmdlet di PowerShell consente la sincronizzazione delle credenziali:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="e6f3c-371">Questo cmdlet di PowerShell Disabilita la sincronizzazione delle credenziali:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="e6f3c-372">[Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)**:** è necessario [distribuire il modello ADMX più recente di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) per abilitare la sincronizzazione delle credenziali tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="e6f3c-373">La sincronizzazione delle credenziali viene gestita con le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="e6f3c-374">Per gestire questa caratteristica con criteri di gruppo, abilitare la sincronizzazione dei criteri delle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="e6f3c-375">Aprire Editor criteri di gruppo e passare a **Configurazione utente-modelli amministrativi-Componenti di Windows-virtualizzazione dell'esperienza utente Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="e6f3c-376">Fare doppio clic su **Sincronizza impostazioni di Windows**.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="e6f3c-377">Se questo criterio è abilitato, è possibile abilitare la sincronizzazione delle credenziali controllando la casella di controllo **credenziali mobili** o disabilitare la sincronizzazione delle credenziali deselezionando.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="e6f3c-378">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-378">Click **OK**.</span></span>

### <span data-ttu-id="e6f3c-379">Percorsi delle credenziali sincronizzati da UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="e6f3c-380">I file di credenziali salvati dalle applicazioni nei percorsi seguenti vengono sincronizzati:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="e6f3c-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="e6f3c-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="e6f3c-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="e6f3c-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="e6f3c-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="e6f3c-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="e6f3c-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="e6f3c-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="e6f3c-385">Le credenziali salvate in altre posizioni non vengono sincronizzate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="e6f3c-386">Sincronizzazione delle impostazioni dell'app Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-386">Windows app settings synchronization</span></span>

<span data-ttu-id="e6f3c-387">UE-V gestisce la sincronizzazione delle impostazioni delle app di Windows in tre modi:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="e6f3c-388">**Sincronizzare le app di Windows:** Consentire o negare qualsiasi sincronizzazione delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="e6f3c-389">**Elenco delle app di Windows:** Sincronizzare un elenco di app di Windows</span><span class="sxs-lookup"><span data-stu-id="e6f3c-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="e6f3c-390">**Comportamento di sincronizzazione predefinito non elenco:** Determinare il comportamento di sincronizzazione delle app di Windows non presenti nell'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="e6f3c-391">Per altre informazioni, Vedi l' [elenco delle app di Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="e6f3c-392">Modelli di posizione delle impostazioni UE-V personalizzati</span><span class="sxs-lookup"><span data-stu-id="e6f3c-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="e6f3c-393">Se si sta distribuendo UE-V per sincronizzare le impostazioni per le applicazioni personalizzate, si utilizzerà il generatore UE-V per creare modelli di posizione personalizzati per le applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="e6f3c-394">Dopo aver creato e testato un modello di posizione delle impostazioni personalizzato in un ambiente di test, è possibile distribuire i modelli di posizione delle impostazioni ai computer nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="e6f3c-395">I modelli di posizione delle impostazioni personalizzate devono essere distribuiti con un'infrastruttura di distribuzione esistente, ad esempio un metodo ESD (Enterprise Software Distribution), come System Center Configuration Manager, con preferenze o configurando un catalogo di modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="e6f3c-396">I modelli distribuiti con Configuration Manager o criteri di gruppo devono essere registrati usando WMI-V di UE o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="e6f3c-397">Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="e6f3c-398">Per altre informazioni sull'uso di UE-V con Configuration Manager, vedere [configurazione di UE-v 2. x con System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="e6f3c-399">Impedire la configurazione delle impostazioni utente non intenzionale</span><span class="sxs-lookup"><span data-stu-id="e6f3c-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="e6f3c-400">UE-V Scarica le nuove informazioni sulle impostazioni utente da una posizione di archiviazione delle impostazioni e applica le impostazioni al computer locale in queste istanze:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="e6f3c-401">Ogni volta che viene avviata un'applicazione con un modello UE-V registrato.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="e6f3c-402">Quando un utente accede a un computer.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="e6f3c-403">Quando un utente sblocca un computer.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="e6f3c-404">Quando viene effettuata una connessione a un computer desktop remoto in cui è installata la versione UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="e6f3c-405">Quando viene eseguita l'attività programmata del controller di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="e6f3c-406">Se UE-V è installato nel computer A e nel computer B e le impostazioni desiderate per l'applicazione si trovano nel computer A, il computer A dovrebbe aprire e chiudere prima l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="e6f3c-407">Se l'applicazione viene aperta e chiusa nel computer B, le impostazioni dell'applicazione nel computer A sono configurate per le impostazioni dell'applicazione nel computer B. le impostazioni vengono sincronizzate tra i computer per ogni singola applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="e6f3c-408">Nel tempo le impostazioni diventano coerenti tra i computer quando vengono aperte e chiuse con le impostazioni preferite.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="e6f3c-409">Questo scenario si applica anche alle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="e6f3c-410">Se le impostazioni di Windows nel computer B devono essere le stesse delle impostazioni di Windows nel computer A, l'utente deve eseguire l'accesso e disconnettersi il computer per primo.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="e6f3c-411">Se le impostazioni utente desiderate dall'utente vengono applicate nell'ordine errato, possono essere recuperate eseguendo un'operazione di ripristino per l'applicazione specifica o la configurazione di Windows nel computer in cui sono state sovrascritte le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="e6f3c-412">Per altre informazioni, vedere [gestire il backup e il ripristino amministrativi in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="e6f3c-413">Pianificazione delle prestazioni e della capacità</span><span class="sxs-lookup"><span data-stu-id="e6f3c-413">Performance and capacity planning</span></span>

<span data-ttu-id="e6f3c-414">Specificare i requisiti per UE-V con capacità disco standard e monitoraggio dell'integrità della rete.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="e6f3c-415">UE-V usa una condivisione SMB (Server Message Block) per l'archiviazione dei pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="e6f3c-416">La dimensione dei pacchetti di impostazioni varia in base alle informazioni sulle impostazioni per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="e6f3c-417">Mentre la maggior parte dei pacchetti di impostazioni è di piccole dimensioni, la sincronizzazione di file potenzialmente di grandi dimensioni, ad esempio immagini desktop, può causare scarse prestazioni, in particolare sulle reti più lente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="e6f3c-418">Per ridurre i problemi relativi alla latenza della rete, creare posizioni di archiviazione delle impostazioni nelle stesse reti locali in cui risiedono i computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="e6f3c-419">È consigliabile 20 MB di spazio su disco per ogni utente per la posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="e6f3c-420">Per impostazione predefinita, la sincronizzazione UE-V viene riattivata dopo 2 secondi per evitare eccessivi ritardi dovuti a un pacchetto di impostazioni di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="e6f3c-421">Puoi configurare l'impostazione SyncMethod = SyncProvider usando [gli oggetti Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="e6f3c-422">Disponibilità elevata per UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-422">High Availability for UE-V</span></span>

<span data-ttu-id="e6f3c-423">Il catalogo della posizione e del modello di impostazioni di archiviazione delle impostazioni UE-V supporta l'archiviazione dei dati degli utenti in qualsiasi condivisione modificabile.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="e6f3c-424">Per garantire una disponibilità elevata, seguire questi criteri:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="e6f3c-425">Formattare il volume di archiviazione con un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="e6f3c-426">La condivisione può usare il file System distribuito (DFS), ma esistono restrizioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="e6f3c-427">In particolare, è supportata la replica di file System Distributed (DFS-R), con o senza uno spazio dei nomi di file System distribuito (DFS-N).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="e6f3c-428">Analogamente, è supportata solo la configurazione di una singola destinazione con DFS-N.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="e6f3c-429">Per informazioni dettagliate, vedere [l'istruzione del supporto Microsoft intorno ai dati di profilo utente replicati](https://go.microsoft.com/fwlink/p/?LinkId=313991) e anche [informazioni sui criteri di supporto Microsoft per uno scenario di distribuzione DFS-R e DFS-N](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="e6f3c-430">Inoltre, poiché SYSVOL USA DFS-R per la replica, non è possibile usare SYSVOL per la replica di file di dati UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="e6f3c-431">Configurare le autorizzazioni di condivisione e gli elenchi di controllo di accesso (ACL) NTFS specificati in [distribuzione della posizione di archiviazione delle impostazioni per UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="e6f3c-432">Usa il clustering di file server insieme all'agente UE-V per consentire l'accesso alle copie dei dati sullo stato dell'utente in caso di errori di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="e6f3c-433">È possibile archiviare i dati del percorso di archiviazione delle impostazioni (dati utente) e modelli di catalogo delle impostazioni in condivisioni in cluster, in condivisioni DFS-N o in entrambe.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="e6f3c-434">Sincronizzare gli orologi del computer per la sincronizzazione delle impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="e6f3c-435">I computer che eseguono l'agente UE-V devono usare un server temporale per mantenere un'esperienza di impostazioni coerente.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="e6f3c-436">UE-V usa i timestamp per determinare se le impostazioni devono essere sincronizzate dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="e6f3c-437">Se l'orologio del computer non è accurato, le impostazioni precedenti possono sovrascrivere le impostazioni più recenti o le nuove impostazioni potrebbero non essere salvate nella posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="e6f3c-438">Confermare i prerequisiti e le configurazioni supportate per la versione UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="e6f3c-439">Prima di procedere, verificare che l'ambiente contenga questi requisiti per l'uso di UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e6f3c-440">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e6f3c-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-441">Edizione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-442">Service Pack</span><span class="sxs-lookup"><span data-stu-id="e6f3c-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-443">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="e6f3c-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6f3c-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="e6f3c-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e6f3c-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-446">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6f3c-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-447">Ultimate, Enterprise o Professional Edition</span><span class="sxs-lookup"><span data-stu-id="e6f3c-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-448">SP1</span><span class="sxs-lookup"><span data-stu-id="e6f3c-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-449">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-450">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-451">.NET Framework 4,5 o versione successiva per la versione UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="e6f3c-452">.NET Framework 4 o versione successiva per la versione UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-453">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6f3c-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-454">Standard, Enterprise, Datacenter o server Web</span><span class="sxs-lookup"><span data-stu-id="e6f3c-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-455">SP1</span><span class="sxs-lookup"><span data-stu-id="e6f3c-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-456">64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-457">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-458">.NET Framework 4,5 o versione successiva per la versione UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="e6f3c-459">.NET Framework 4 o versione successiva per la versione UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-460">Windows 8 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="e6f3c-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-461">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="e6f3c-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-462">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6f3c-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-463">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-464">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-465">.NET Framework 4,5 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e6f3c-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-466">Windows 10, versione pre-1607</span><span class="sxs-lookup"><span data-stu-id="e6f3c-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e6f3c-467">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-467">Note</span></span></strong><br/><p><span data-ttu-id="e6f3c-468">Solo UE-V 2,1 SP1 supporta Windows 10, versione pre-1607</span><span class="sxs-lookup"><span data-stu-id="e6f3c-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="e6f3c-469">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="e6f3c-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-470">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6f3c-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-471">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-472">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-473">.NET framework 4.6</span><span class="sxs-lookup"><span data-stu-id="e6f3c-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6f3c-474">Windows Server 2012 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e6f3c-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-475">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="e6f3c-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-476">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6f3c-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-477">64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-478">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-479">.NET Framework 4,5 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e6f3c-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6f3c-480">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e6f3c-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-481">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="e6f3c-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-482">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6f3c-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-483">64 bit</span><span class="sxs-lookup"><span data-stu-id="e6f3c-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-484">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e6f3c-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6f3c-485">.NET Framework 4,6 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e6f3c-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e6f3c-486">Inoltre...</span><span class="sxs-lookup"><span data-stu-id="e6f3c-486">Also…</span></span>

-   <span data-ttu-id="e6f3c-487">**Licenza MDOP:** Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="e6f3c-488">I clienti aziendali possono ottenere MDOP con Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="e6f3c-489">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere come si ottiene MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="e6f3c-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="e6f3c-490">**Credenziali amministrative** per qualsiasi computer in cui verrà installato</span><span class="sxs-lookup"><span data-stu-id="e6f3c-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="e6f3c-491">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-491">Note</span></span>**  

-   <span data-ttu-id="e6f3c-492">A partire da WIndows 10, versione 1607, UE-V è incluso in [Windows 10 per le aziende](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e non fa più parte del Microsoft Desktop Optimization Pack.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="e6f3c-493">La caratteristica UE-V Windows PowerShell dell'agente UE-V richiede .NET Framework 4 o versione successiva e Windows PowerShell 3,0 o versioni successive per essere abilitate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="e6f3c-494">Scaricare Windows PowerShell 3,0 [qui](https://go.microsoft.com/fwlink/?LinkId=309609).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="e6f3c-495">Installare .NET Framework 4 o .NET Framework 4,5 nei computer che eseguono Windows 7 o il sistema operativo Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="e6f3c-496">I sistemi operativi Windows 8, Windows 8,1 e Windows Server 2012 sono installati in .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="e6f3c-497">Il sistema operativo Windows 10 include .NET Framework 4,6 installato.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="e6f3c-498">Il criterio "Elimina cache roaming" per i profili obbligatori non è supportato con UE-V e non deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="e6f3c-499">Non sono previsti particolari requisiti RAM (Random Access Memory) specifici di UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="e6f3c-500">Sincronizzazione delle impostazioni tramite il provider di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="e6f3c-501">Il provider di sincronizzazione è l'impostazione predefinita per gli utenti, che sincronizza una cache locale con la posizione di archiviazione delle impostazioni in queste istanze:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="e6f3c-502">Accesso/fine sessione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-502">Logon/logoff</span></span>

-   <span data-ttu-id="e6f3c-503">Bloccare/sbloccare</span><span class="sxs-lookup"><span data-stu-id="e6f3c-503">Lock/unlock</span></span>

-   <span data-ttu-id="e6f3c-504">Connessione/disconnessione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="e6f3c-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="e6f3c-505">Apertura/chiusura dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="e6f3c-505">Application open/close</span></span>

<span data-ttu-id="e6f3c-506">Un'attività pianificata gestisce questa sincronizzazione delle impostazioni ogni 30 minuti o tramite determinati eventi trigger per alcune applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="e6f3c-507">Per altre informazioni, vedere [modifica della frequenza delle attività pianificate di UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="e6f3c-508">L'agente UE-V consente di sincronizzare le impostazioni utente per i computer che non sono sempre connessi alla rete aziendale (computer remoti e laptop) e computer sempre connessi alla rete (computer che eseguono Windows Server e ospitano sessioni di Virtual Desktop Interface (VDI)).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="e6f3c-509">**Sincronizzazione per i computer con connessioni sempre disponibili:** Quando si usa UE-V in computer sempre connessi alla rete, è necessario configurare l'agente UE-V per sincronizzare le impostazioni usando il parametro *SyncMethod = None* , che tratta il server di archiviazione delle impostazioni come condivisione di rete standard.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="e6f3c-510">In questa configurazione, l'agente UE-V può essere configurato per segnalare se l'importazione delle impostazioni dell'applicazione è ritardata.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="e6f3c-511">Abilitare questa configurazione tramite uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="e6f3c-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="e6f3c-512">Durante l'installazione di UE-V, al prompt dei comandi o in un file batch, imposta il parametro AgentSetup.exe *SyncMethod = None*.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="e6f3c-513">[La distribuzione dell'agente UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fornisce ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="e6f3c-514">Dopo l'installazione di UE-V, usare la caratteristica di gestione delle impostazioni in System Center 2012 Configuration Manager o i modelli ADMX di MDOP per spingere la configurazione *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="e6f3c-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="e6f3c-515">Usare Windows PowerShell o Strumentazione gestione Windows (WMI) per impostare la configurazione *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="e6f3c-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="e6f3c-516">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-516">Note</span></span>**  
    <span data-ttu-id="e6f3c-517">Questi ultimi due metodi non funzionano per gli ambienti VDI (Virtual Desktop Infrastructure) in pool.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="e6f3c-518">È necessario riavviare il computer prima che le impostazioni inizino a essere sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="e6f3c-519">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-519">Note</span></span>**  
<span data-ttu-id="e6f3c-520">Se si imposta *SyncMethod = None*, le eventuali modifiche apportate alle impostazioni vengono salvate direttamente nel server.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="e6f3c-521">Se la connessione di rete al percorso di archiviazione delle impostazioni non viene trovata, le modifiche apportate alle impostazioni vengono memorizzate nella cache del dispositivo e vengono sincronizzate alla successiva esecuzione del provider di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="e6f3c-522">Se il percorso di archiviazione delle impostazioni non viene trovato e il profilo utente viene rimosso da un ambiente VDI in pool durante la disconnessione, le modifiche alle impostazioni vengono perse e l'utente deve riapplicare la modifica quando il computer viene riconnesso al percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="e6f3c-523">**Sincronizzazione per motori di sincronizzazione esterni:** Il parametro *SyncMethod = External* specifica che se le impostazioni di UE-V vengono scritte in una cartella locale nel computer utente, qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, work Folders, SharePoint o Dropbox, può essere usato per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="e6f3c-524">**Supporto per le sessioni VDI condivise:** UE-V 2,1 e 2,1 SP1 consentono di supportare le sessioni VDI condivise tra gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="e6f3c-525">È possibile registrare e configurare uno speciale modello VDI, garantendo che UE-V mantenga intatte tutte le sue funzionalità per le sessioni VDI non persistenti.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="e6f3c-526">Nota</span><span class="sxs-lookup"><span data-stu-id="e6f3c-526">Note</span></span>**  
<span data-ttu-id="e6f3c-527">Se non si Abilita la modalità VDI per le sessioni VDI non persistenti, alcune caratteristiche non funzionano, ad esempio [backup/ripristino e ultimo bene noto (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="e6f3c-528">Il modello VDI è provvisto di UE-V 2,1 e 2,1 SP1 ed è in genere disponibile qui dopo l'installazione: C:\\Programmi \\Programmi\\microsoft User Experience Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="e6f3c-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="e6f3c-529">Prerequisiti per il supporto del generatore di UE-V</span><span class="sxs-lookup"><span data-stu-id="e6f3c-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="e6f3c-530">Installare il generatore UE-V nel computer usato per creare modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="e6f3c-531">Questo computer dovrebbe essere in grado di eseguire le applicazioni le cui impostazioni sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="e6f3c-532">È necessario essere un membro del gruppo Administrators nel computer in cui è in esecuzione il software Generator UE-V.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="e6f3c-533">Il generatore UE-V deve essere installato in un computer che usa un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="e6f3c-534">Il software Generator UE-V richiede .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="e6f3c-535">Per altre informazioni, vedere [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e6f3c-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="e6f3c-536">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="e6f3c-536">Other resources for this product</span></span>


-   [<span data-ttu-id="e6f3c-537">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="e6f3c-538">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="e6f3c-539">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="e6f3c-540">Risoluzione dei problemi relativi a UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="e6f3c-541">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e6f3c-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














