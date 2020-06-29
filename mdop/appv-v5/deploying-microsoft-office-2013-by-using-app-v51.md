---
title: Distribuzione di Microsoft Office 2013 tramite App-V
description: Distribuzione di Microsoft Office 2013 tramite App-V
author: dansimp
ms.assetid: 9a7be05e-2a7a-4874-af25-09c0f5037876
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: f6a54cadce79ff3680fd69206eba8ac3fbe83a68
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805871"
---
# <span data-ttu-id="7ef35-103">Distribuzione di Microsoft Office 2013 tramite App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="7ef35-104">Usare le informazioni in questo articolo per usare Microsoft Application Virtualization (App-V) 5,1 o versioni successive per offrire Microsoft Office 2013 come applicazione virtualizzata ai computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="7ef35-105">Per informazioni sull'uso di App-V per consegnare Office 2010, vedere [distribuzione di Microsoft office 2010 tramite App-v](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="7ef35-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span> <span data-ttu-id="7ef35-106">Per distribuire correttamente Office 2013 con App-V, è necessario avere familiarità con Office 2013 e App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and App-V.</span></span>

<span data-ttu-id="7ef35-107">Questo argomento contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ef35-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="7ef35-108">Informazioni da conoscere prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="7ef35-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="7ef35-109">Creazione di un pacchetto di Office 2013 per App-V con lo strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="7ef35-110">Pubblicazione del pacchetto di Office per App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7ef35-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="7ef35-111">Personalizzazione e gestione dei pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="7ef35-112">Informazioni da conoscere prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="7ef35-112">What to know before you start</span></span>


<span data-ttu-id="7ef35-113">Prima di distribuire Office 2013 tramite App-V, esaminare le informazioni di pianificazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="7ef35-114">Versioni di Office supportate e coesistenza di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="7ef35-115">Usare la tabella seguente per ottenere informazioni sulle versioni supportate di Office e sull'utilizzo di versioni coesistenti di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-116">Informazioni da rivedere</span><span class="sxs-lookup"><span data-stu-id="7ef35-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="7ef35-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ef35-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="7ef35-118">Pianificazione per l'uso di App-V con Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-119">Versioni supportate di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="7ef35-120">Tipi di distribuzione supportati, ad esempio desktop, Personal Virtual Desktop Infrastructure (VDI), pool VDI)</span><span class="sxs-lookup"><span data-stu-id="7ef35-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="7ef35-121">Opzioni di gestione licenze di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting)"><span data-ttu-id="7ef35-122">Pianificazione per l'uso di App-V con Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="7ef35-123">Considerazioni per l'installazione di versioni diverse di Office nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="7ef35-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>


### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="7ef35-124">Requisiti per l'imballaggio, la pubblicazione e la distribuzione</span><span class="sxs-lookup"><span data-stu-id="7ef35-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="7ef35-125">Prima di distribuire Office tramite App-V, esaminare i requisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-126">Attività</span><span class="sxs-lookup"><span data-stu-id="7ef35-126">Task</span></span></th>
<th align="left"><span data-ttu-id="7ef35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef35-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-128">Imballaggio</span><span class="sxs-lookup"><span data-stu-id="7ef35-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-129">Tutte le applicazioni di Office che si desidera distribuire agli utenti devono essere in un unico pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-130">In App-V 5,1 e versioni successive è necessario usare lo strumento di distribuzione di Office per creare pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="7ef35-131">Non è possibile usare il sequencer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-132">Se si distribuisce Microsoft Visio 2013 e Microsoft Project 2013 insieme a Office, è necessario includerli nello stesso pacchetto con Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="7ef35-133">Per altre informazioni, vedere <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> distribuzione di Visio 2013 e Project 2013 con Office </a> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-134">Pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7ef35-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-135">È possibile pubblicare un solo pacchetto di Office in ogni computer client.</span><span class="sxs-lookup"><span data-stu-id="7ef35-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-136">È necessario pubblicare il pacchetto di Office a livello globale.</span><span class="sxs-lookup"><span data-stu-id="7ef35-136">You must publish the Office package globally.</span></span> <span data-ttu-id="7ef35-137">Non è possibile pubblicare l'utente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-138">Distribuire uno dei prodotti seguenti in un computer condiviso, ad esempio tramite Servizi Desktop remoto:</span><span class="sxs-lookup"><span data-stu-id="7ef35-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="7ef35-139">App Microsoft 365 per le aziende</span><span class="sxs-lookup"><span data-stu-id="7ef35-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="7ef35-140">Visio Pro per Office 365</span><span class="sxs-lookup"><span data-stu-id="7ef35-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="7ef35-141">Project Pro per Office 365</span><span class="sxs-lookup"><span data-stu-id="7ef35-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7ef35-142">È necessario abilitare l' <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> attivazione di computer condivisi </a> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="7ef35-143">Non si usa l'attivazione di computer condivisi se si sta distribuendo un prodotto con contratto multilicenza, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7ef35-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="7ef35-144">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="7ef35-145">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="7ef35-146">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7ef35-147">Esclusione di applicazioni di Office da un pacchetto</span><span class="sxs-lookup"><span data-stu-id="7ef35-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="7ef35-148">La tabella seguente descrive i metodi consigliati per l'esclusione di specifiche applicazioni di Office da un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-149">Attività</span><span class="sxs-lookup"><span data-stu-id="7ef35-149">Task</span></span></th>
<th align="left"><span data-ttu-id="7ef35-150">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ef35-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-151">Usa l' <strong> </strong> impostazione ExcludeApp quando crei il pacchetto usando lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-152">Consente di escludere specifiche applicazioni di Office dal pacchetto quando lo strumento di distribuzione di Office crea il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="7ef35-153">Ad esempio, puoi usare questa impostazione per creare un pacchetto che contiene solo Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="7ef35-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-154">Per altre informazioni, Vedi <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-155">Modificare il file di DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="7ef35-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-156">Modificare il file DeploymentConfig.xml dopo la creazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="7ef35-157">Questo file contiene le impostazioni predefinite del pacchetto per tutti gli utenti in un computer in cui è in uso App-V client.</span><span class="sxs-lookup"><span data-stu-id="7ef35-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-158">Per altre informazioni, vedere <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> disabilitare le applicazioni di Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="7ef35-159">Creazione di un pacchetto di Office 2013 per App-V con lo strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="7ef35-160">Completare la procedura seguente per creare un pacchetto di Office 2013 per App-V 5,1 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7ef35-160">Complete the following steps to create an Office 2013 package for App-V 5.1 or later.</span></span>

**<span data-ttu-id="7ef35-161">Importante</span><span class="sxs-lookup"><span data-stu-id="7ef35-161">Important</span></span>**  
<span data-ttu-id="7ef35-162">In App-V 5,1 e versioni successive è necessario lo strumento di distribuzione di Office per creare un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-162">In App-V 5.1 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="7ef35-163">Non è possibile usare il sequencer per creare pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-163">You cannot use the Sequencer to create packages.</span></span>



### <span data-ttu-id="7ef35-164">Rivedere i prerequisiti per l'uso dello strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="7ef35-165">Il computer in cui si sta installando lo strumento di distribuzione di Office deve avere:</span><span class="sxs-lookup"><span data-stu-id="7ef35-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-166">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7ef35-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="7ef35-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ef35-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-168">Software prerequisito</span><span class="sxs-lookup"><span data-stu-id="7ef35-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="7ef35-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-170">Sistemi operativi supportati</span><span class="sxs-lookup"><span data-stu-id="7ef35-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7ef35-171">versione a 64 bit di Windows 8 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="7ef35-171">64-bit version of Windows 8 or later</span></span></p></li>
<li><p><span data-ttu-id="7ef35-172">versione di Windows 7 a 64 bit</span><span class="sxs-lookup"><span data-stu-id="7ef35-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7ef35-173">Nota</span><span class="sxs-lookup"><span data-stu-id="7ef35-173">Note</span></span>**  
<span data-ttu-id="7ef35-174">In questo argomento, il termine "Office 2013 App-V Package" si riferisce alle licenze per gli abbonamenti e a contratti multilicenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>



### <span data-ttu-id="7ef35-175">Creare pacchetti di Office 2013 App-V usando lo strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="7ef35-176">Puoi creare pacchetti di Office 2013 App-V usando lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="7ef35-177">Le istruzioni seguenti spiegano come creare un pacchetto di Office 2013 App-V con contratti multilicenza o abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7ef35-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="7ef35-178">Creare pacchetti di Office 2013 App-V in computer Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7ef35-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="7ef35-179">Una volta creato, il pacchetto di Office 2013 App-V verrà eseguito in computer con Windows 7, Windows 8,1 e Windows 10 a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7ef35-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="7ef35-180">Scaricare lo strumento di distribuzione di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="7ef35-181">I pacchetti App-V di Office 2013 vengono creati con lo strumento di distribuzione di Office, che genera un pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="7ef35-182">Il pacchetto non può essere creato o modificato tramite App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="7ef35-183">Per iniziare la creazione del pacchetto:</span><span class="sxs-lookup"><span data-stu-id="7ef35-183">To begin package creation:</span></span>

1.  <span data-ttu-id="7ef35-184">Scaricare lo [strumento di distribuzione di Office per l'esecuzione a](https://www.microsoft.com/download/details.aspx?id=36778)portata di clic.</span><span class="sxs-lookup"><span data-stu-id="7ef35-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="7ef35-185">Eseguire il file con estensione exe ed estrarne le caratteristiche nella posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="7ef35-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="7ef35-186">Per semplificare la procedura, è possibile creare una cartella di rete condivisa in cui verranno salvate le caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="7ef35-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="7ef35-187">Esempio: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="7ef35-188">Verificare che esistano un setup.exe e un file di configuration.xml e che si trovino nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7ef35-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="7ef35-189">Scaricare le applicazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-189">Download Office 2013 applications</span></span>

<span data-ttu-id="7ef35-190">Dopo aver scaricato lo strumento di distribuzione di Office, è possibile usarlo per ottenere le più recenti applicazioni di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="7ef35-191">Dopo aver ottenuto le applicazioni di Office, è possibile creare il pacchetto App-V di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="7ef35-192">Il file XML incluso nello strumento di distribuzione di Office specifica i dettagli del prodotto, ad esempio le lingue e le applicazioni di Office incluse.</span><span class="sxs-lookup"><span data-stu-id="7ef35-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1.  <span data-ttu-id="7ef35-193">**Personalizzare il file di configurazione XML di esempio:** Usare il file di configurazione XML di esempio scaricato con lo strumento di distribuzione di Office per personalizzare le applicazioni di Office:</span><span class="sxs-lookup"><span data-stu-id="7ef35-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

    1.  <span data-ttu-id="7ef35-194">Aprire il file XML di esempio in blocco note o nell'editor di testo preferito.</span><span class="sxs-lookup"><span data-stu-id="7ef35-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

    2.  <span data-ttu-id="7ef35-195">Con l'esempio configuration.xml file aperto e pronto per la modifica, è possibile specificare i prodotti, le lingue e il percorso in cui si salvano le applicazioni di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="7ef35-196">Di seguito è riportato un esempio di base del file configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="7ef35-196">The following is a basic example of the configuration.xml file:</span></span>

        ```xml
        <Configuration>
           <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
            <Product ID="O365ProPlusRetail ">
              <Language ID="en-us" />
            </Product>
            <Product ID="VisioProRetail">
              <Language ID="en-us" />
            </Product>
          </Add>
        </Configuration>
        ```

        **<span data-ttu-id="7ef35-197">Nota</span><span class="sxs-lookup"><span data-stu-id="7ef35-197">Note</span></span>**  
        <span data-ttu-id="7ef35-198">La configurazione XML è un file XML di esempio.</span><span class="sxs-lookup"><span data-stu-id="7ef35-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="7ef35-199">Il file include righe commentate. Puoi "rimuovere il commento" da queste righe per personalizzare le impostazioni aggiuntive con il file.</span><span class="sxs-lookup"><span data-stu-id="7ef35-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>



~~~
    The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to. Note that the Product ID of the applications will not affect the final licensing of Office. Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage. The table below summarizes the customizable attributes and elements of XML file:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Input</th>
    <th align="left">Description</th>
    <th align="left">Example</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Add element</p></td>
    <td align="left"><p>Specifies the products and languages to include in the package.</p></td>
    <td align="left"><p>N/A</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>OfficeClientEdition (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the edition of Office 2013 product to use: 32-bit or 64-bit. The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</p></td>
    <td align="left"><p><strong>OfficeClientEdition</strong>=&quot;32&quot;</p>
    <p><strong>OfficeClientEdition</strong>=&quot;64&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Product element</p></td>
    <td align="left"><p>Specifies the application. Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</p></td>
    <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
    <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
    <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
    <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Language element</p></td>
    <td align="left"><p>Specifies the language supported in the applications</p></td>
    <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Version (attribute of Add element)</p></td>
    <td align="left"><p>Optional. Specifies a build to use for the package</p>
    <p>Defaults to latest advertised build (as defined in v32.CAB at the Office source).</p></td>
    <td align="left"><p><code>15.1.2.3</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>SourcePath (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the location in which the applications will be saved to.</p></td>
    <td align="left"><p><code>Sourcepath = &quot;\\Server\Office2013”</code></p></td>
    </tr>
    </tbody>
    </table>



    After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.
~~~

2. <span data-ttu-id="7ef35-200">**Scaricare le applicazioni nella posizione specificata:** Usare un prompt dei comandi con privilegi elevati e un sistema operativo di 64 bit per scaricare le applicazioni di Office 2013 che verranno in seguito convertite in un pacchetto di App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-200">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="7ef35-201">Di seguito è riportato un comando di esempio con descrizione dei dettagli:</span><span class="sxs-lookup"><span data-stu-id="7ef35-201">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="7ef35-202">Nell'esempio:</span><span class="sxs-lookup"><span data-stu-id="7ef35-202">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-203">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-203">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-204">è il percorso di condivisione di rete che contiene lo strumento di distribuzione di Office e il file Configuration.xml personalizzato Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-204">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-205">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="7ef35-205">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-206">è lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-206">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-207">/Download</span><span class="sxs-lookup"><span data-stu-id="7ef35-207">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-208">Scarica le applicazioni di Office 2013 specificate nel file customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-208">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="7ef35-209">Questi bit possono essere convertiti in seguito in un pacchetto di Office 2013 App-V con contratti multilicenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-209">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-210">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="7ef35-210">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-211">passa il file di configurazione XML necessario per completare il processo di download, in questo esempio customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-211">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="7ef35-212">Dopo aver usato il comando Scarica, le applicazioni di Office devono essere trovate nella posizione specificata nel file XML di configurazione, in questo esempio \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-212">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="7ef35-213">Convertire le applicazioni di Office in un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-213">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="7ef35-214">Dopo aver scaricato le applicazioni di Office 2013 tramite lo strumento di distribuzione di Office, usare lo strumento di distribuzione di Office per convertirle in un pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-214">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="7ef35-215">Completare i passaggi che corrispondono al modello di licenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-215">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="7ef35-216">Riepilogo delle operazioni che è necessario eseguire:</span><span class="sxs-lookup"><span data-stu-id="7ef35-216">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="7ef35-217">Creare i pacchetti App-V di Office 2013 nei computer Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7ef35-217">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="7ef35-218">Il pacchetto verrà tuttavia eseguito in computer con Windows 7, Windows 8 e Windows 10 a 32 bit e 64.</span><span class="sxs-lookup"><span data-stu-id="7ef35-218">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8, and Windows 10 computers.</span></span>

-   <span data-ttu-id="7ef35-219">Creare un pacchetto di Office App-V per il pacchetto di licenze di sottoscrizione o per contratti multilicenza usando lo strumento di distribuzione di Office e quindi modificare il file di configurazione di CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-219">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="7ef35-220">Nella tabella seguente sono riepilogati i valori che è necessario immettere nel file CustomConfig.xml per il modello di licenza in uso.</span><span class="sxs-lookup"><span data-stu-id="7ef35-220">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="7ef35-221">I passaggi descritti nelle sezioni che seguono la tabella specificano le voci esatte che è necessario apportare.</span><span class="sxs-lookup"><span data-stu-id="7ef35-221">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-222">ID prodotto</span><span class="sxs-lookup"><span data-stu-id="7ef35-222">Product ID</span></span></th>
<th align="left"><span data-ttu-id="7ef35-223">Contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="7ef35-223">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="7ef35-224">Licenze per gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="7ef35-224">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ef35-225">Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-225">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ef35-226">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-226">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-227">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-227">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7ef35-228">Office 2013 con Visio 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-228">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ef35-229">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-229">ProPlusVolume</span></span></p>
<p><span data-ttu-id="7ef35-230">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-230">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-231">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-231">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="7ef35-232">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-232">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ef35-233">Office 2013 con Visio 2013 e Project 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-233">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ef35-234">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-234">ProPlusVolume</span></span></p>
<p><span data-ttu-id="7ef35-235">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-235">VisioProVolume</span></span></p>
<p><span data-ttu-id="7ef35-236">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="7ef35-236">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-237">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-237">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="7ef35-238">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-238">VisioProRetail</span></span></p>
<p><span data-ttu-id="7ef35-239">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="7ef35-239">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7ef35-240">Come convertire le applicazioni di Office in un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-240">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="7ef35-241">In blocco note riaprire il file CustomConfig.xml e apportare le modifiche seguenti al file:</span><span class="sxs-lookup"><span data-stu-id="7ef35-241">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7ef35-242">Parametro</span><span class="sxs-lookup"><span data-stu-id="7ef35-242">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="7ef35-243">Informazioni su come modificare il valore in</span><span class="sxs-lookup"><span data-stu-id="7ef35-243">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7ef35-244">SourcePath</span><span class="sxs-lookup"><span data-stu-id="7ef35-244">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-245">Selezionare le applicazioni di Office scaricate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-245">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7ef35-246">ProductID</span><span class="sxs-lookup"><span data-stu-id="7ef35-246">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-247">Specificare il tipo di licenza, come illustrato negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ef35-247">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="7ef35-248">Licenze per gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="7ef35-248">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="7ef35-249">In questo esempio sono state apportate le modifiche seguenti per creare un pacchetto con licenze di sottoscrizione:</span><span class="sxs-lookup"><span data-stu-id="7ef35-249">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-250">SourcePath</span><span class="sxs-lookup"><span data-stu-id="7ef35-250">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-251">è il percorso, che è stato modificato in modo che punti alle applicazioni di Office scaricate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-251">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-252">ID prodotto</span><span class="sxs-lookup"><span data-stu-id="7ef35-252">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-253">per Office è stato modificato in <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-253">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-254">ID prodotto</span><span class="sxs-lookup"><span data-stu-id="7ef35-254">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-255">per Visio è stato modificato in <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-255">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="7ef35-256">Contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="7ef35-256">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="7ef35-257">In questo esempio sono state apportate le modifiche seguenti per creare un pacchetto con contratti multilicenza:</span><span class="sxs-lookup"><span data-stu-id="7ef35-257">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-258">SourcePath</span><span class="sxs-lookup"><span data-stu-id="7ef35-258">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-259">è il percorso, che è stato modificato in modo che punti alle applicazioni di Office scaricate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-259">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-260">ID prodotto</span><span class="sxs-lookup"><span data-stu-id="7ef35-260">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-261">per Office è stato modificato in <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-261">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-262">ID prodotto</span><span class="sxs-lookup"><span data-stu-id="7ef35-262">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-263">per Visio è stato modificato in <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-263">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7ef35-264">ExcludeApp (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="7ef35-264">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-265">Consente di specificare le applicazioni di Office che non si desidera includere nel pacchetto App-V creato dallo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-265">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="7ef35-266">Ad esempio, è possibile escludere Access e InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7ef35-266">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7ef35-267">PACKAGEGUID (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="7ef35-267">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-268">Per impostazione predefinita, tutti i pacchetti App-V creati dallo strumento di distribuzione di Office condividono lo stesso ID pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-268">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="7ef35-269">Puoi usare PACKAGEGUID per specificare un ID pacchetto diverso per ogni pacchetto, che ti permette di pubblicare più pacchetti App-V, creati dallo strumento di distribuzione di Office e di gestirli usando App-V Server.</span><span class="sxs-lookup"><span data-stu-id="7ef35-269">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="7ef35-270">Un esempio di quando usare questo parametro è creare pacchetti diversi per utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="7ef35-270">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="7ef35-271">Ad esempio, è possibile creare un pacchetto con solo Office 2013 per alcuni utenti e creare un altro pacchetto con Office 2013 e Visio 2013 per un altro gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-271">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="7ef35-272">Nota</span><span class="sxs-lookup"><span data-stu-id="7ef35-272">Note</span></span></strong><br/><p><span data-ttu-id="7ef35-273">Anche se usi ID pacchetto univoci, puoi comunque distribuire solo un pacchetto di App-V in un singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ef35-273">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="7ef35-274">Usare il comando/Packager per convertire le applicazioni di Office in un pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-274">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="7ef35-275">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7ef35-275">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="7ef35-276">Nell'esempio:</span><span class="sxs-lookup"><span data-stu-id="7ef35-276">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-277">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-277">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-278">è il percorso di condivisione di rete che contiene lo strumento di distribuzione di Office e il file Configuration.xml personalizzato Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-278">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-279">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="7ef35-279">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-280">è lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-280">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-281">/packager</span><span class="sxs-lookup"><span data-stu-id="7ef35-281">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-282">Crea il pacchetto App-V di Office 2013 con contratti multilicenza, come specificato nel file customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="7ef35-282">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="7ef35-283">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="7ef35-283">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-284">passa il file XML di configurazione (in questo caso customConfig) che è stato preparato per la fase di assemblaggio.</span><span class="sxs-lookup"><span data-stu-id="7ef35-284">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7ef35-285">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="7ef35-285">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7ef35-286">Specifica la posizione del pacchetto di Office App-V appena creato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-286">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="7ef35-287">Verificare che il pacchetto Office 2013 App-V funzioni correttamente:</span><span class="sxs-lookup"><span data-stu-id="7ef35-287">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="7ef35-288">Pubblicare il pacchetto App-V di Office 2013, creato globalmente, in un computer di test e verificare che vengano visualizzati i tasti di scelta rapida di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-288">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="7ef35-289">Avviare alcune applicazioni di Office 2013, ad esempio Excel o Word, per verificare che il pacchetto funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-289">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="7ef35-290">Pubblicazione del pacchetto di Office per App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7ef35-290">Publishing the Office package for App-V 5.1</span></span>


<span data-ttu-id="7ef35-291">Usare le informazioni seguenti per pubblicare un pacchetto di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-291">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="7ef35-292">Metodi per la pubblicazione di pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-292">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="7ef35-293">Distribuire il pacchetto App-V per Office 2013 usando gli stessi metodi usati per qualsiasi altro pacchetto:</span><span class="sxs-lookup"><span data-stu-id="7ef35-293">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="7ef35-294">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7ef35-294">System Center Configuration Manager</span></span>

-   <span data-ttu-id="7ef35-295">App-V Server</span><span class="sxs-lookup"><span data-stu-id="7ef35-295">App-V Server</span></span>

-   <span data-ttu-id="7ef35-296">Autonomo tramite i comandi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ef35-296">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="7ef35-297">Prerequisiti e requisiti per la pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7ef35-297">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-298">Prerequisito o requisito</span><span class="sxs-lookup"><span data-stu-id="7ef35-298">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="7ef35-299">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ef35-299">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-300">Abilitare gli script di PowerShell nei client App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-300">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-301">Per pubblicare i pacchetti di Office 2013, è necessario eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="7ef35-301">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="7ef35-302">Gli script di pacchetto sono disabilitati per impostazione predefinita nei client App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-302">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="7ef35-303">Per abilitare gli script, eseguire il comando di PowerShell seguente:</span><span class="sxs-lookup"><span data-stu-id="7ef35-303">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-304">Pubblicare il pacchetto Office 2013 globalmente</span><span class="sxs-lookup"><span data-stu-id="7ef35-304">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-305">I punti di estensione nel pacchetto di Office App-V richiedono l'installazione a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-305">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="7ef35-306">Quando si pubblica a livello di computer, non sono necessarie azioni prerequisitive o ridistribuibili e il pacchetto Office 2013 consente a livello globale le proprie applicazioni di funzionare come Office installato nativamente, eliminando la necessità per gli amministratori di personalizzare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-306">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7ef35-307">Come pubblicare un pacchetto di Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-307">How to publish an Office package</span></span>

<span data-ttu-id="7ef35-308">Eseguire il comando seguente per pubblicare un pacchetto di Office a livello globale:</span><span class="sxs-lookup"><span data-stu-id="7ef35-308">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="7ef35-309">Dalla console di gestione Web in App-V Server è possibile aggiungere le autorizzazioni a un gruppo di computer anziché a un gruppo di utenti per consentire la pubblicazione globale dei pacchetti nei computer del gruppo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-309">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="7ef35-310">Personalizzazione e gestione dei pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-310">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="7ef35-311">Per gestire i pacchetti di Office App-V, USA le stesse operazioni che vuoi per qualsiasi altro pacchetto, ma esistono alcune eccezioni, come descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-311">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="7ef35-312">Attivazione dei plug-in di Office tramite i gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="7ef35-312">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="7ef35-313">Disabilitazione delle applicazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-313">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="7ef35-314">Disabilitazione di tasti di scelta rapida di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-314">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="7ef35-315">Gestione degli aggiornamenti del pacchetto di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-315">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="7ef35-316">Gestione degli aggiornamenti delle licenze di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-316">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="7ef35-317">Distribuzione di Visio 2013 e Project 2013 con Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-317">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="7ef35-318">Attivazione dei plug-in di Office tramite i gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="7ef35-318">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="7ef35-319">Usare la procedura descritta in questa sezione per abilitare i plug-in di Office con il pacchetto di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-319">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="7ef35-320">Per usare i plug-in di Office, devi usare app-V Sequencer per creare un pacchetto distinto che contiene solo i plug-in. Non è possibile usare lo strumento di distribuzione di Office per creare il pacchetto plug-in.</span><span class="sxs-lookup"><span data-stu-id="7ef35-320">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="7ef35-321">Viene quindi creato un gruppo di connessioni contenente il pacchetto di Office e il pacchetto plug-in, come descritto nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-321">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="7ef35-322">Per abilitare i plug-in per i pacchetti di Office App-V</span><span class="sxs-lookup"><span data-stu-id="7ef35-322">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="7ef35-323">Aggiungere un gruppo di connessioni tramite App-V Server, System Center Configuration Manager o un cmdlet di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ef35-323">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="7ef35-324">Sequenziare i plug-in usando l'App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-324">Sequence your plug-ins using the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="7ef35-325">Assicurarsi che Office 2013 sia installato nel computer usato per sequenziare il plug-in.</span><span class="sxs-lookup"><span data-stu-id="7ef35-325">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="7ef35-326">È consigliabile usare le app Microsoft 365 per le aziende (non virtuali) nel computer di sequenziazione quando si sequenziano i plug-in di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-326">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="7ef35-327">Crea un pacchetto di App-V 5,1 che include i plug-in desiderati.</span><span class="sxs-lookup"><span data-stu-id="7ef35-327">Create an App-V 5.1 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="7ef35-328">Aggiungere un gruppo di connessioni tramite App-V Server, System Center Configuration Manager o un cmdlet di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ef35-328">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="7ef35-329">Aggiungere il pacchetto App-V di Office 2013 e il pacchetto plug-in sequenziato al gruppo di connessioni creato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-329">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="7ef35-330">Importante</span><span class="sxs-lookup"><span data-stu-id="7ef35-330">Important</span></span>**  
    <span data-ttu-id="7ef35-331">L'ordine dei pacchetti nel gruppo di connessioni determina l'ordine in cui il contenuto del pacchetto viene Unito.</span><span class="sxs-lookup"><span data-stu-id="7ef35-331">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="7ef35-332">Nel file del descrittore del gruppo di connessioni aggiungere prima il pacchetto Office 2013 App-V e quindi aggiungere il pacchetto App-V plug-in.</span><span class="sxs-lookup"><span data-stu-id="7ef35-332">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="7ef35-333">Assicurarsi che entrambi i pacchetti vengano pubblicati nel computer di destinazione e che il pacchetto di plug-in venga pubblicato globalmente in modo che corrisponda alle impostazioni globali del pacchetto pubblicato App-V di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-333">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="7ef35-334">Verificare che il file di configurazione della distribuzione del pacchetto di plug-in abbia le stesse impostazioni del pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-334">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="7ef35-335">Poiché il pacchetto App-V di Office 2013 è integrato con il sistema operativo, le impostazioni del pacchetto plug-in dovrebbero corrispondere.</span><span class="sxs-lookup"><span data-stu-id="7ef35-335">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="7ef35-336">È possibile eseguire una ricerca nel file di configurazione della distribuzione per "modalità COM" e verificare che il pacchetto plug-in disponga di tale valore impostato come "Integrated" e che sia "InProcessEnabled" che "OutOfProcessEnabled" corrispondano alle impostazioni del pacchetto di App-V di Office 2013 pubblicato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-336">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="7ef35-337">Aprire il file di configurazione della distribuzione e impostare il valore per **gli oggetti Enabled** su **false**.</span><span class="sxs-lookup"><span data-stu-id="7ef35-337">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="7ef35-338">Se sono state apportate modifiche al file di configurazione della distribuzione dopo la sequenziazione, verificare che il pacchetto di plug-in venga pubblicato con il file.</span><span class="sxs-lookup"><span data-stu-id="7ef35-338">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="7ef35-339">Verificare che il gruppo di connessioni creato sia abilitato nel computer desiderato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-339">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="7ef35-340">Il gruppo di connessioni creato sarà probabilmente "pend" Se il pacchetto App-V di Office 2013 è in uso quando il gruppo di connessioni è abilitato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-340">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="7ef35-341">In questo caso, è necessario riavviare il file per abilitare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="7ef35-341">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="7ef35-342">Dopo aver correttamente pubblicato entrambi i pacchetti e aver abilitato il gruppo di connessioni, avviare l'applicazione di Office 2013 di destinazione e verificare che il plug-in pubblicato e aggiunto al gruppo di connessioni funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-342">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="7ef35-343">Disabilitazione delle applicazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-343">Disabling Office 2013 applications</span></span>

<span data-ttu-id="7ef35-344">Potrebbe essere necessario disabilitare applicazioni specifiche nel pacchetto di Office App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-344">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="7ef35-345">Ad esempio, puoi disabilitare Access, ma lascia tutte le altre applicazioni principali di Office disponibili.</span><span class="sxs-lookup"><span data-stu-id="7ef35-345">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="7ef35-346">Quando si disattiva un'applicazione, l'utente finale non vedrà più il collegamento per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-346">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="7ef35-347">Non è necessario ripetere la sequenza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-347">You do not have to re-sequence the application.</span></span> <span data-ttu-id="7ef35-348">Quando si modifica il file di configurazione della distribuzione dopo la pubblicazione del pacchetto di Office 2013 App-V, si salvano le modifiche, si aggiunge il pacchetto App-V di Office 2013 e lo si ripubblica con il nuovo file di configurazione della distribuzione per applicare le nuove impostazioni alle applicazioni di pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-348">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="7ef35-349">Nota</span><span class="sxs-lookup"><span data-stu-id="7ef35-349">Note</span></span>**  
<span data-ttu-id="7ef35-350">Per escludere specifiche applicazioni di Office, ad esempio Access e InfoPath, quando si crea il pacchetto App-V con lo strumento di distribuzione di Office, usare l'impostazione **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="7ef35-350">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="7ef35-351">Per altre informazioni, vedere [riferimento per il file configuration.xml a portata di clic](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ef35-351">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="7ef35-352">Per disabilitare un'applicazione di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-352">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="7ef35-353">Aprire un file di configurazione della distribuzione con un editor di testo, ad esempio **blocco note** , e cercare "applicazioni".</span><span class="sxs-lookup"><span data-stu-id="7ef35-353">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="7ef35-354">Cercare l'applicazione di Office che si vuole disabilitare, ad esempio Access 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-354">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="7ef35-355">Cambiare il valore di "Enabled" da "true" a "false".</span><span class="sxs-lookup"><span data-stu-id="7ef35-355">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="7ef35-356">Salvare il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-356">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="7ef35-357">Aggiungere il pacchetto App-V di Office 2013 con il nuovo file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-357">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="7ef35-358">Aggiungere di nuovo il pacchetto Office 2013 App-V e ripubblicarlo con il nuovo file di configurazione della distribuzione per applicare le nuove impostazioni alle applicazioni di pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-358">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="7ef35-359">Disabilitazione di tasti di scelta rapida di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-359">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="7ef35-360">Potrebbe essere necessario disabilitare i tasti di scelta rapida per alcune applicazioni di Office invece di depubblicare o rimuovere il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7ef35-360">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="7ef35-361">L'esempio seguente mostra come disabilitare i tasti di scelta rapida per Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7ef35-361">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="7ef35-362">Per disabilitare i collegamenti per le applicazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-362">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="7ef35-363">Aprire un file di configurazione della distribuzione in blocco note e cercare "tasti di scelta rapida".</span><span class="sxs-lookup"><span data-stu-id="7ef35-363">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="7ef35-364">Per disabilitare alcuni tasti di scelta rapida, eliminare o impostare come commento i tasti di scelta rapida specifici che non si desidera.</span><span class="sxs-lookup"><span data-stu-id="7ef35-364">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="7ef35-365">È necessario conservare il sottosistema presente e abilitato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-365">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="7ef35-366">Ad esempio, nell'esempio seguente elimina i tasti di scelta rapida di Microsoft Access, mantenendo &lt; intatto il collegamento &gt; &lt; di/Shortcut &gt; per disabilitare il collegamento a Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7ef35-366">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="7ef35-367">Salvare il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-367">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="7ef35-368">Ripubblicare il pacchetto di Office 2013 App-V con il nuovo file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-368">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="7ef35-369">Molte altre impostazioni possono essere modificate modificando la configurazione della distribuzione per i pacchetti App-V, ad esempio le associazioni di tipi di file, il file system virtuale e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="7ef35-369">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="7ef35-370">Per altre informazioni su come usare i file di configurazione della distribuzione per modificare le impostazioni del pacchetto App-V, vedere la sezione risorse aggiuntive alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="7ef35-370">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="7ef35-371">Gestione degli aggiornamenti del pacchetto di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-371">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="7ef35-372">Per aggiornare un pacchetto di Office 2013, usare lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-372">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="7ef35-373">Per aggiornare un pacchetto di Office 2013 distribuito in precedenza, eseguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-373">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="7ef35-374">Come aggiornare un pacchetto di Office 2013 distribuito in precedenza</span><span class="sxs-lookup"><span data-stu-id="7ef35-374">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="7ef35-375">Creare un nuovo pacchetto di Office 2013 tramite lo strumento di distribuzione di Office che usa il più recente software applicativo di Office 2013.</span><span class="sxs-lookup"><span data-stu-id="7ef35-375">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="7ef35-376">I bit più recenti di Office 2013 possono essere sempre ottenuti attraverso la fase di download della creazione di un pacchetto di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-376">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="7ef35-377">Il pacchetto di Office 2013 appena creato includerà gli aggiornamenti più recenti e un nuovo ID versione.</span><span class="sxs-lookup"><span data-stu-id="7ef35-377">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="7ef35-378">Tutti i pacchetti creati con lo strumento di distribuzione di Office hanno lo stesso lignaggio.</span><span class="sxs-lookup"><span data-stu-id="7ef35-378">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="7ef35-379">Nota</span><span class="sxs-lookup"><span data-stu-id="7ef35-379">Note</span></span>**  
    <span data-ttu-id="7ef35-380">I pacchetti di Office App-V hanno due ID versione:</span><span class="sxs-lookup"><span data-stu-id="7ef35-380">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="7ef35-381">Un ID versione del pacchetto di Office 2013 App-V univoco in tutti i pacchetti creati con lo strumento di distribuzione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-381">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="7ef35-382">Un secondo ID versione del pacchetto App-V, x. x.x. x, ad esempio, nel manifesto di AppX che verrà modificato solo se è presente una nuova versione di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-382">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="7ef35-383">Ad esempio, se è disponibile una nuova versione di Office 2013 con gli aggiornamenti e viene creato un pacchetto tramite lo strumento di distribuzione di Office per incorporare questi aggiornamenti, l'ID versione x. X.x. x verrà modificato in modo che la versione di Office sia cambiata.</span><span class="sxs-lookup"><span data-stu-id="7ef35-383">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="7ef35-384">Il server App-V utilizzerà l'ID versione x. X.x. x per distinguere questo pacchetto e riconoscerà che contiene nuovi aggiornamenti al pacchetto pubblicato in precedenza e, di conseguenza, lo pubblicherà come aggiornamento al pacchetto di Office 2013 esistente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-384">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="7ef35-385">Pubblicare globalmente i pacchetti di Office 2013 App-V appena creati nei computer in cui si desidera applicare i nuovi aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-385">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="7ef35-386">Dato che il nuovo pacchetto ha lo stesso lignaggio del pacchetto di Office 2013 App-V più vecchio, la pubblicazione del nuovo pacchetto con gli aggiornamenti consentirà di applicare solo le nuove modifiche al vecchio pacchetto e quindi sarà veloce.</span><span class="sxs-lookup"><span data-stu-id="7ef35-386">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="7ef35-387">Gli aggiornamenti verranno applicati allo stesso modo dei pacchetti App-V pubblicati a livello globale.</span><span class="sxs-lookup"><span data-stu-id="7ef35-387">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="7ef35-388">Dato che le applicazioni saranno probabilmente in uso, gli aggiornamenti potrebbero essere ritardati finché non viene riavviato il computer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-388">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="7ef35-389">Gestione degli aggiornamenti delle licenze di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-389">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="7ef35-390">Se un nuovo pacchetto di Office 2013 App-V ha una licenza diversa rispetto al pacchetto di Office 2013 App-V attualmente distribuito.</span><span class="sxs-lookup"><span data-stu-id="7ef35-390">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="7ef35-391">Ad esempio, il pacchetto di Office 2013 distribuito è un abbonamento basato su Office 2013 e il nuovo pacchetto di Office 2013 è basato su contratti multilicenza, le istruzioni seguenti devono essere seguite per garantire un aggiornamento agevole delle licenze:</span><span class="sxs-lookup"><span data-stu-id="7ef35-391">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="7ef35-392">Come aggiornare una licenza di Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ef35-392">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="7ef35-393">Annullare la pubblicazione del pacchetto App-V già distribuito in Office 2013 Subscription Licensing.</span><span class="sxs-lookup"><span data-stu-id="7ef35-393">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="7ef35-394">Rimuovere il pacchetto di App-V per l'abbonamento a Office 2013 non pubblicato.</span><span class="sxs-lookup"><span data-stu-id="7ef35-394">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="7ef35-395">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="7ef35-395">Restart the computer.</span></span>

4.  <span data-ttu-id="7ef35-396">Aggiungere il nuovo pacchetto di contratti multilicenza di Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="7ef35-396">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="7ef35-397">Pubblicare il pacchetto di Office 2013 App-V aggiunto con contratti multilicenza.</span><span class="sxs-lookup"><span data-stu-id="7ef35-397">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="7ef35-398">Un pacchetto di Office 2013 App-V con le licenze scelte verrà distribuito correttamente.</span><span class="sxs-lookup"><span data-stu-id="7ef35-398">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="7ef35-399">Distribuzione di Visio 2013 e Project 2013 con Office</span><span class="sxs-lookup"><span data-stu-id="7ef35-399">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="7ef35-400">La tabella seguente descrive i requisiti e le opzioni per la distribuzione di Visio 2013 e Project 2013 con Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-400">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-401">Attività</span><span class="sxs-lookup"><span data-stu-id="7ef35-401">Task</span></span></th>
<th align="left"><span data-ttu-id="7ef35-402">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ef35-402">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-403">Come si impacca e pubblica Visio 2013 e Project 2013 con Office?</span><span class="sxs-lookup"><span data-stu-id="7ef35-403">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-404">È necessario includere Visio 2013 e Project 2013 nello stesso pacchetto con Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-404">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="7ef35-405">Se non si sta distribuendo Office, è possibile creare un pacchetto che contiene Visio e/o Project, purché si segua la <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> distribuzione di Microsoft office 2010 tramite App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="7ef35-405">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-406">Come è possibile distribuire Visio 2013 e Project 2013 a utenti specifici?</span><span class="sxs-lookup"><span data-stu-id="7ef35-406">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-407">Usare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ef35-407">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ef35-408">Se vuoi...</span><span class="sxs-lookup"><span data-stu-id="7ef35-408">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="7ef35-409">... quindi usa questo metodo</span><span class="sxs-lookup"><span data-stu-id="7ef35-409">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ef35-410">Creare due pacchetti diversi e distribuirli a un gruppo di utenti diverso</span><span class="sxs-lookup"><span data-stu-id="7ef35-410">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-411">Creare e distribuire i pacchetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ef35-411">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="7ef35-412">Pacchetto che contiene solo la distribuzione di Office in computer i cui utenti necessitano solo di Office.</span><span class="sxs-lookup"><span data-stu-id="7ef35-412">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-413">Pacchetto che contiene Office, Visio e Project-deploy per i computer i cui utenti hanno bisogno di tutte e tre le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ef35-413">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ef35-414">Se si vuole solo un pacchetto per l'intera organizzazione o se si hanno utenti che condividono computer:</span><span class="sxs-lookup"><span data-stu-id="7ef35-414">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ef35-415">Segue questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7ef35-415">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="7ef35-416">Creare un pacchetto che contiene Office, Visio e Project.</span><span class="sxs-lookup"><span data-stu-id="7ef35-416">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-417">Distribuire il pacchetto a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="7ef35-417">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="7ef35-418">Usare <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> per impedire a utenti specifici di usare Visio e Project.</span><span class="sxs-lookup"><span data-stu-id="7ef35-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7ef35-419">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7ef35-419">Additional resources</span></span>


**<span data-ttu-id="7ef35-420">Office 2013 App-V pacchetti risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7ef35-420">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="7ef35-421">Strumento di distribuzione di Office per l'esecuzione a portata di clic</span><span class="sxs-lookup"><span data-stu-id="7ef35-421">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="7ef35-422">Scenari supportati per la distribuzione di Microsoft Office come pacchetto di App-V sequenziato</span><span class="sxs-lookup"><span data-stu-id="7ef35-422">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="7ef35-423">Pacchetti App-V di Office 2010</span><span class="sxs-lookup"><span data-stu-id="7ef35-423">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="7ef35-424">Microsoft Office 2010-Kit di sequenziazione per Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="7ef35-424">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="7ef35-425">Problemi noti quando si crea o si usa un pacchetto di App-V 5,0 Office 2010</span><span class="sxs-lookup"><span data-stu-id="7ef35-425">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="7ef35-426">Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="7ef35-426">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="7ef35-427">Gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="7ef35-427">Connection Groups</span></span>**

[<span data-ttu-id="7ef35-428">Distribuzione di gruppi di connessioni in Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="7ef35-428">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="7ef35-429">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="7ef35-429">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="7ef35-430">Configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="7ef35-430">Dynamic Configuration</span></span>**

[<span data-ttu-id="7ef35-431">Informazioni sulla configurazione dinamica di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7ef35-431">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)














