---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795815"
---
# <span data-ttu-id="7b15b-103">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="7b15b-104">Questa documentazione è una versione di UE-V inclusa nel Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="7b15b-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7b15b-105">Per informazioni sulla versione più recente di UE-V inclusa in Windows 10 Enterprise, vedere Introduzione a [UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="7b15b-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="7b15b-106">Acquisire e centralizzare le impostazioni delle applicazioni degli utenti e le impostazioni del sistema operativo Windows implementando Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1.</span><span class="sxs-lookup"><span data-stu-id="7b15b-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="7b15b-107">Applica quindi queste impostazioni agli utenti di dispositivi che accedono all'organizzazione, come computer desktop, laptop o sessioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="7b15b-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="7b15b-108">Con UE-V puoi...</span><span class="sxs-lookup"><span data-stu-id="7b15b-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="7b15b-109">Specificare le impostazioni di applicazione e desktop da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="7b15b-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="7b15b-110">Recapitare in qualsiasi momento le impostazioni agli utenti, indipendentemente dalla posizione nell'azienda da cui gli utenti lavorano</span><span class="sxs-lookup"><span data-stu-id="7b15b-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="7b15b-111">Creare modelli personalizzati per le applicazioni di terze parti o line-of-business</span><span class="sxs-lookup"><span data-stu-id="7b15b-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="7b15b-112">Recuperare le impostazioni dopo la sostituzione o l'aggiornamento dell'hardware oppure dopo aver ricreato una macchina virtuale nello stato iniziale</span><span class="sxs-lookup"><span data-stu-id="7b15b-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="7b15b-113">Componenti di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="7b15b-114">Questo diagramma mostra il modo in cui i componenti UE-V distribuiti collaborano per sincronizzare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7b15b-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![diagramma architetturale uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b15b-116">Componente</span><span class="sxs-lookup"><span data-stu-id="7b15b-116">Component</span></span></th>
<th align="left"><span data-ttu-id="7b15b-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="7b15b-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7b15b-118">Agente UE-V</span><span class="sxs-lookup"><span data-stu-id="7b15b-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-119">Installato in tutti i computer che devono sincronizzare le impostazioni, l' <strong> agente UE-V </strong> monitora le applicazioni registrate e il sistema operativo per tutte le modifiche delle impostazioni, quindi Sincronizza le impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="7b15b-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7b15b-120">Pacchetti di impostazioni</span><span class="sxs-lookup"><span data-stu-id="7b15b-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-121">Le impostazioni delle applicazioni e le impostazioni di Windows sono archiviate in <strong> pacchetti </strong> di impostazioni creati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="7b15b-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="7b15b-122">I pacchetti di impostazioni vengono creati, archiviati localmente e copiati nel percorso dell'archivio impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7b15b-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="7b15b-123">I valori delle impostazioni per le <strong> applicazioni desktop </strong> vengono archiviati quando l'utente chiude l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b15b-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="7b15b-124">I valori per <strong> le impostazioni di Windows </strong> vengono archiviati quando l'utente si disconnette, quando il computer è bloccato o quando l'utente si disconnette in remoto da un computer.</span><span class="sxs-lookup"><span data-stu-id="7b15b-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="7b15b-125">Il provider di sincronizzazione determina quando le impostazioni dell'applicazione o del sistema operativo vengono lette dai <strong> pacchetti di impostazioni </strong> e sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="7b15b-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7b15b-126">Posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="7b15b-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-127">Si tratta di una condivisione di rete standard a cui gli utenti possono accedere.</span><span class="sxs-lookup"><span data-stu-id="7b15b-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="7b15b-128">L'agente UE-V Verifica la posizione e crea una cartella di sistema nascosta in cui archiviare e recuperare le impostazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b15b-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7b15b-129">Modelli di posizione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="7b15b-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-130">UE-V usa i file XML come modelli di posizione delle impostazioni per monitorare e sincronizzare le impostazioni delle applicazioni desktop e le impostazioni desktop di Windows tra i computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b15b-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="7b15b-131">Per impostazione predefinita, alcuni modelli di posizione delle impostazioni sono inclusi in UE-V.</span><span class="sxs-lookup"><span data-stu-id="7b15b-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="7b15b-132">È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gestendo la sincronizzazione delle impostazioni per le applicazioni personalizzate </a> .</span><span class="sxs-lookup"><span data-stu-id="7b15b-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7b15b-133">Nota</span><span class="sxs-lookup"><span data-stu-id="7b15b-133">Note</span></span></strong><br/><p><span data-ttu-id="7b15b-134">I modelli di posizione delle impostazioni non sono necessari per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b15b-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7b15b-135">Elenco delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="7b15b-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-136">Le impostazioni per le app di Windows vengono acquisite e applicate in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="7b15b-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="7b15b-137">Lo sviluppatore dell'app specifica le impostazioni sincronizzate per ogni app.</span><span class="sxs-lookup"><span data-stu-id="7b15b-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="7b15b-138">UE-V determina quali app di Windows sono abilitate per la sincronizzazione delle impostazioni usando un elenco gestito di app.</span><span class="sxs-lookup"><span data-stu-id="7b15b-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="7b15b-139">Per impostazione predefinita, questo elenco include la maggior parte delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b15b-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="7b15b-140">Puoi aggiungere o rimuovere applicazioni nell'elenco delle app di Windows seguendo le procedure illustrate in <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> questo articolo </a> .</span><span class="sxs-lookup"><span data-stu-id="7b15b-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="7b15b-141">Gestione della sincronizzazione delle impostazioni per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="7b15b-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="7b15b-142">Usa questi componenti UE-V per creare e gestire modelli personalizzati per le applicazioni di terze parti o line-of-business.</span><span class="sxs-lookup"><span data-stu-id="7b15b-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7b15b-143">Generatore di UE-V</span><span class="sxs-lookup"><span data-stu-id="7b15b-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-144">Usa il <strong> Generatore UE-V </strong> per creare modelli di posizione personalizzati che puoi quindi distribuire ai computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b15b-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="7b15b-145">Il generatore UE-V consente inoltre di modificare un modello esistente o di convalidare un modello creato usando un altro editor XML.</span><span class="sxs-lookup"><span data-stu-id="7b15b-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7b15b-146">Catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="7b15b-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7b15b-147">Il catalogo dei modelli di <strong> impostazioni </strong> è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7b15b-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="7b15b-148">L'agente UE-V controlla questa posizione una volta al giorno, recupera i modelli nuovi o aggiornati e aggiorna il comportamento della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7b15b-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="7b15b-149">Se si usano solo i modelli di posizione predefiniti UE-V, il catalogo di un modello di impostazioni non è necessario.</span><span class="sxs-lookup"><span data-stu-id="7b15b-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="7b15b-150">Per altre informazioni sui cataloghi di distribuzione delle impostazioni, vedere <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurare un catalogo di modelli di impostazioni UE-V </a> .</span><span class="sxs-lookup"><span data-stu-id="7b15b-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![processo generatore di UE-v](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="7b15b-152">Impostazioni sincronizzate per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="7b15b-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="7b15b-153">Per impostazione predefinita, la pagina UE-V sincronizza le impostazioni per queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7b15b-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="7b15b-154">Per un elenco completo e informazioni più dettagliate, vedere [Impostazioni sincronizzate automaticamente in una distribuzione di UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="7b15b-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="7b15b-155">Applicazioni di Microsoft Office 2013 (UE-V 2,1 SP1 e 2,1)</span><span class="sxs-lookup"><span data-stu-id="7b15b-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="7b15b-156">Applicazioni di Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 e 2,0)</span><span class="sxs-lookup"><span data-stu-id="7b15b-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="7b15b-157">Applicazioni di Microsoft Office 2007 (solo UE-V 2,0)</span><span class="sxs-lookup"><span data-stu-id="7b15b-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="7b15b-158">Internet Explorer 8, 9 e 10</span><span class="sxs-lookup"><span data-stu-id="7b15b-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="7b15b-159">Internet Explorer 11 in UE-V 2,1 SP1 e 2,1</span><span class="sxs-lookup"><span data-stu-id="7b15b-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="7b15b-160">Molte applicazioni Windows, ad esempio Xbox</span><span class="sxs-lookup"><span data-stu-id="7b15b-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="7b15b-161">Molte applicazioni desktop di Windows, ad esempio Blocco note</span><span class="sxs-lookup"><span data-stu-id="7b15b-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="7b15b-162">Molte impostazioni di Windows, ad esempio sfondo desktop o wallpaper</span><span class="sxs-lookup"><span data-stu-id="7b15b-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="7b15b-163">Nota</span><span class="sxs-lookup"><span data-stu-id="7b15b-163">Note</span></span>**  
<span data-ttu-id="7b15b-164">È anche possibile [personalizzare l'opzione UE-V per sincronizzare le impostazioni](https://technet.microsoft.com/library/dn458942.aspx) per le applicazioni diverse da quelle sincronizzate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7b15b-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="7b15b-165">Confrontare UE-V con altri prodotti Microsoft</span><span class="sxs-lookup"><span data-stu-id="7b15b-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="7b15b-166">Usare questa tabella per confrontare l'opzione UE-V per sincronizzare i profili in Windows 7, sincronizzare i profili in Windows 8 e la caratteristica Impostazioni PC di sincronizzazione dell'account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b15b-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

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
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b15b-167">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7b15b-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="7b15b-168">Sincronizzare i profili con Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b15b-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="7b15b-169">Sincronizzare i profili con Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b15b-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="7b15b-170">Sincronizzare i profili con Windows 10</span><span class="sxs-lookup"><span data-stu-id="7b15b-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="7b15b-171">Account Microsoft</span><span class="sxs-lookup"><span data-stu-id="7b15b-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="7b15b-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="7b15b-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="7b15b-173">UE-V 2,1 e 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="7b15b-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-174">Sincronizzare le impostazioni tra più computer</span><span class="sxs-lookup"><span data-stu-id="7b15b-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-175">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-176">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-177">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-178">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-179">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-180">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-181">Sincronizzare le impostazioni tra le app fisiche e virtuali</span><span class="sxs-lookup"><span data-stu-id="7b15b-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-182">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-183">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-184">Sincronizzare le impostazioni delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="7b15b-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-185">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-186">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-187">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-188">Gestire tramite WMI</span><span class="sxs-lookup"><span data-stu-id="7b15b-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-189">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-190">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-191">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-192">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-193">Sincronizzare le modifiche delle impostazioni su base regolare</span><span class="sxs-lookup"><span data-stu-id="7b15b-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-194">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-195">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-196">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-197">Configurazione minima per l'installazione</span><span class="sxs-lookup"><span data-stu-id="7b15b-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-198">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-199">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-200">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-201">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-202">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-203">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-204">Supportato in computer non appartenenti a un dominio</span><span class="sxs-lookup"><span data-stu-id="7b15b-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-205">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-206">Supporta l'attributo Primary computer Active Directory</span><span class="sxs-lookup"><span data-stu-id="7b15b-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-207">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-208">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-209">Sincronizza le impostazioni tra Virtual Desktop Infrastructure (VDI)/Remote Desktop Services (RDS) e desktop RTF</span><span class="sxs-lookup"><span data-stu-id="7b15b-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-210">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-211">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-212">Spazio di archiviazione illimitato per l'impostazione</span><span class="sxs-lookup"><span data-stu-id="7b15b-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-213">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-214">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-215">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-216">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-217">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b15b-218">Scelta delle impostazioni dell'app da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="7b15b-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-219">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-220">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b15b-221">Backup/ripristino per professionisti IT</span><span class="sxs-lookup"><span data-stu-id="7b15b-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7b15b-222">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-223">Parziale</span><span class="sxs-lookup"><span data-stu-id="7b15b-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b15b-224">●</span><span class="sxs-lookup"><span data-stu-id="7b15b-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7b15b-225">Note sulla versione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="7b15b-226">Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere</span><span class="sxs-lookup"><span data-stu-id="7b15b-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="7b15b-227">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="7b15b-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="7b15b-228">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="7b15b-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="7b15b-229">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="7b15b-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="7b15b-230">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="7b15b-230">Other resources for this product</span></span>


-   [<span data-ttu-id="7b15b-231">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7b15b-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="7b15b-232">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="7b15b-233">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="7b15b-234">Risoluzione dei problemi relativi a UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7b15b-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="7b15b-235">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7b15b-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="7b15b-236">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="7b15b-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="7b15b-237">[Pagina TechCenter di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Scopri le informazioni e le risorse più recenti di MDOP.</span><span class="sxs-lookup"><span data-stu-id="7b15b-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="7b15b-238">[Esperienza di informazioni su MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Trovare documentazione, video e altre risorse per le tecnologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="7b15b-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="7b15b-239">È anche possibile [inviare commenti e suggerimenti](mailto:MDOPDocs@microsoft.com) per ricevere informazioni sugli aggiornamenti e seguirci su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="7b15b-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














