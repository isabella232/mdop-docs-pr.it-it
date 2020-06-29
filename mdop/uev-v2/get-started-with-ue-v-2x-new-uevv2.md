---
title: Introduzione a UE-V 2.x
description: Introduzione a UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823286"
---
# <span data-ttu-id="21447-103">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="21447-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="21447-104">Seguire i passaggi descritti in questa guida per distribuire rapidamente Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1 in un ambiente di test ridotto.</span><span class="sxs-lookup"><span data-stu-id="21447-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="21447-105">In questo modo, puoi determinare se UE-V è la soluzione più adatta per gestire le impostazioni utente in più dispositivi all'interno dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="21447-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="21447-106">**Nota**  Le informazioni in questa sezione vengono ripetute in modo più dettagliato in tutto il resto della documentazione.</span><span class="sxs-lookup"><span data-stu-id="21447-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="21447-107">Quindi, se si sa già che l'UE-V 2 è la soluzione giusta e non è necessario valutarla, è sufficiente andare a destra per [preparare una distribuzione UE-v 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="21447-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="21447-108">L'installazione standard di UE-V sincronizza le impostazioni predefinite di Microsoft Windows e Office e molte impostazioni delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="21447-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="21447-109">Verificare che l'ambiente di test includa due o più computer utente che condividono l'accesso alla rete e si valuterà la valutazione di UE-V in poco tempo.</span><span class="sxs-lookup"><span data-stu-id="21447-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="21447-110">[Passaggio 1: confermare i prerequisiti](#step1): verificare che l'ambiente sia in grado di eseguire la versione UE-V, inclusi i dettagli sulle configurazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="21447-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="21447-111">[Passaggio 2: distribuire il percorso di archiviazione delle impostazioni per la versione UE-v 2](#step2): tutte le distribuzioni UE-v richiedono una posizione per i pacchetti di impostazioni che contengono i valori di impostazione sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="21447-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="21447-112">[Passaggio 3: distribuire l'agente UE-v 2](#step3): per sincronizzare le impostazioni con UE-v, i dispositivi devono avere l'agente UE-v installato ed eseguito.</span><span class="sxs-lookup"><span data-stu-id="21447-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="21447-113">[Passaggio 4: verificare la distribuzione della valutazione UE-v 2](#step4): eseguire alcuni test su due computer in cui è installato l'agente UE-v e verificare la modalità di funzionamento di UE-v.</span><span class="sxs-lookup"><span data-stu-id="21447-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="21447-114">Questo è tutto!</span><span class="sxs-lookup"><span data-stu-id="21447-114">That’s it!</span></span> <span data-ttu-id="21447-115">Dopo aver eseguito la procedura, sarà possibile valutare l'utilizzo di UE-V nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="21447-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="21447-116">**Ulteriore valutazione:** È anche possibile eseguire ulteriori passaggi per configurare alcune applicazioni di terze parti e line-of-business per sincronizzare le proprie impostazioni con UE-V come descritto in dettaglio in [distribuire UE-v 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="21447-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="21447-117">Passaggio 1: confermare i prerequisiti</span><span class="sxs-lookup"><span data-stu-id="21447-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="21447-118">Prima di procedere, verificare che l'ambiente contenga questi requisiti per l'uso di UE-V.</span><span class="sxs-lookup"><span data-stu-id="21447-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="21447-119">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="21447-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21447-120">Edizione</span><span class="sxs-lookup"><span data-stu-id="21447-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21447-121">Service Pack</span><span class="sxs-lookup"><span data-stu-id="21447-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21447-122">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="21447-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21447-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="21447-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21447-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="21447-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21447-125">Windows7</span><span class="sxs-lookup"><span data-stu-id="21447-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-126">Ultimate, Enterprise o Professional Edition</span><span class="sxs-lookup"><span data-stu-id="21447-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-127">SP1</span><span class="sxs-lookup"><span data-stu-id="21447-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-128">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-129">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-130">.NET Framework 4 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21447-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="21447-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-132">Standard, Enterprise, Datacenter o server Web</span><span class="sxs-lookup"><span data-stu-id="21447-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-133">SP1</span><span class="sxs-lookup"><span data-stu-id="21447-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-134">64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-135">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-136">.NET Framework 4 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21447-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21447-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-138">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="21447-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21447-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-140">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-141">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-142">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="21447-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21447-143">Windows Server 2012 R2 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21447-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-144">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="21447-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21447-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-146">64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-147">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-148">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="21447-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21447-149">Windows 10, pre-1607 versione</span><span class="sxs-lookup"><span data-stu-id="21447-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-150">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="21447-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="21447-151">32 o 64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-152">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-153">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="21447-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21447-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="21447-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-155">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="21447-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21447-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-157">64 bit</span><span class="sxs-lookup"><span data-stu-id="21447-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-158">Windows PowerShell 3,0 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="21447-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="21447-159">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="21447-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="21447-160">**Nota:** A partire da Windows 10, versione 1607, UE-V è incluso in [Windows 10 per le aziende](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e non fa più parte del Microsoft Desktop Optimization Pack</span><span class="sxs-lookup"><span data-stu-id="21447-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="21447-161">Inoltre...</span><span class="sxs-lookup"><span data-stu-id="21447-161">Also…</span></span>

-   <span data-ttu-id="21447-162">**Licenza MDOP:** Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="21447-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="21447-163">I clienti aziendali possono ottenere MDOP con Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="21447-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="21447-164">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere come si ottiene MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="21447-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="21447-165">**Credenziali amministrative** per qualsiasi computer in cui verrà installato</span><span class="sxs-lookup"><span data-stu-id="21447-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="21447-166">Passaggio 2: distribuire il percorso di archiviazione delle impostazioni per UE-V 2</span><span class="sxs-lookup"><span data-stu-id="21447-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="21447-167">È necessario distribuire un percorso di archiviazione delle impostazioni, una condivisione di rete standard in cui le impostazioni utente sono archiviate in un file del pacchetto di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21447-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="21447-168">Quando si crea la condivisione di archiviazione delle impostazioni, è necessario limitare l'accesso agli utenti che lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="21447-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="21447-169">[Distribuire una posizione di archiviazione delle impostazioni](https://technet.microsoft.com/library/dn458891.aspx#ssl) fornisce informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="21447-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="21447-170">Creare una condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="21447-170">Create a network share</span></span>**

1.  <span data-ttu-id="21447-171">Creare un nuovo gruppo di sicurezza e aggiungere gli utenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="21447-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="21447-172">Creare una nuova cartella nel computer situato in posizione centrale in cui sono archiviati i pacchetti di impostazioni UE-V e quindi concedere agli utenti di UE-V l'accesso con le autorizzazioni di gruppo alla cartella.</span><span class="sxs-lookup"><span data-stu-id="21447-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="21447-173">L'amministratore che supporta UE-V deve disporre delle autorizzazioni per questa cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="21447-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="21447-174">Assegnare agli utenti di UE-V l'autorizzazione per creare una directory quando si connettono.</span><span class="sxs-lookup"><span data-stu-id="21447-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="21447-175">Concedere l'autorizzazione completa a tutte le sottodirectory di tale cartella, ma bloccare l'accesso a qualsiasi elemento di cui sopra.</span><span class="sxs-lookup"><span data-stu-id="21447-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="21447-176">Impostare le autorizzazioni SMB (Server Message Block) di livello di condivisione seguenti per la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21447-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="21447-177">Account utente</span><span class="sxs-lookup"><span data-stu-id="21447-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="21447-178">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="21447-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="21447-179">Tutti</span><span class="sxs-lookup"><span data-stu-id="21447-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-180">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="21447-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="21447-181">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="21447-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-182">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="21447-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="21447-183">Impostare le autorizzazioni di file system NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21447-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="21447-184">Account utente</span><span class="sxs-lookup"><span data-stu-id="21447-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="21447-185">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="21447-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="21447-186">Cartella</span><span class="sxs-lookup"><span data-stu-id="21447-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="21447-187">Creatore/proprietario</span><span class="sxs-lookup"><span data-stu-id="21447-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-188">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="21447-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-189">Solo sottocartelle e file</span><span class="sxs-lookup"><span data-stu-id="21447-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="21447-190">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="21447-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-191">Cartella di elenco/dati letti, creare cartelle/accodare dati</span><span class="sxs-lookup"><span data-stu-id="21447-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="21447-192">Solo questa cartella</span><span class="sxs-lookup"><span data-stu-id="21447-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="21447-193">Nota sulla sicurezza:</span><span class="sxs-lookup"><span data-stu-id="21447-193">Security Note:</span></span>**

<span data-ttu-id="21447-194">Se si crea la condivisione di archiviazione delle impostazioni in un computer che esegue un sistema operativo Windows Server, configurare UE-V per verificare che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21447-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="21447-195">Per abilitare questa ulteriore sicurezza, specificare questa impostazione nell'editor del registro di sistema di Windows Server:</span><span class="sxs-lookup"><span data-stu-id="21447-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="21447-196">Aggiungere una chiave **reg \ _DWORD** del registro di sistema denominata **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="21447-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="21447-197">Impostare il valore della chiave del registro di sistema su *1*.</span><span class="sxs-lookup"><span data-stu-id="21447-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="21447-198">Passaggio 3: distribuire l'agente UE-V 2</span><span class="sxs-lookup"><span data-stu-id="21447-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="21447-199">L'agente UE-V sincronizza le impostazioni dell'applicazione e di Windows tra i computer e i dispositivi degli utenti.</span><span class="sxs-lookup"><span data-stu-id="21447-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="21447-200">Per scopi di valutazione, installare l'agente in almeno due computer nell'ambiente di test che appartengono allo stesso utente.</span><span class="sxs-lookup"><span data-stu-id="21447-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="21447-201">Eseguire il file AgentSetup.exe dalla riga di comando per installare l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="21447-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="21447-202">Viene installato nei sistemi operativi 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="21447-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="21447-203">Devi specificare il parametro della riga di comando SettingsStoragePath come condivisione di rete del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="21447-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="21447-204">[Distribuire un agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fornisce informazioni più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="21447-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="21447-205">Passaggio 4: testare la distribuzione della valutazione UE-V 2</span><span class="sxs-lookup"><span data-stu-id="21447-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="21447-206">È ora possibile eseguire alcuni test sulla distribuzione della valutazione UE-V per vedere come funziona l'UE-V.</span><span class="sxs-lookup"><span data-stu-id="21447-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="21447-207">Nel primo computer (computer A) eseguire una o più delle modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="21447-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="21447-208">Aprire a Windows desktop e spostarla in una posizione diversa nella finestra.</span><span class="sxs-lookup"><span data-stu-id="21447-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="21447-209">Modificare i tipi di carattere predefiniti.</span><span class="sxs-lookup"><span data-stu-id="21447-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="21447-210">Aprire la calcolatrice e impostarla su **Scientific**.</span><span class="sxs-lookup"><span data-stu-id="21447-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="21447-211">Modificare il comportamento di qualsiasi app di Windows, come descritto in dettaglio nella sezione [gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="21447-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="21447-212">Disabilitare la sincronizzazione e i profili di roaming delle impostazioni dell'account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21447-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="21447-213">Disconnettersi dal computer A. le impostazioni vengono salvate in un pacchetto di impostazioni di UE-V quando gli utenti bloccano, disconnessione, terminano un'applicazione o quando il provider di sincronizzazione viene eseguito (ogni 30 minuti per impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="21447-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="21447-214">Accedere al secondo computer (computer B) come stesso utente del computer A.</span><span class="sxs-lookup"><span data-stu-id="21447-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="21447-215">Aprire a Windows desktop e verificare che la posizione della barra delle applicazioni corrisponda a quella del computer A. Verificare che i tipi di carattere predefiniti corrispondano e che la calcolatrice sia impostata su **Scientific**.</span><span class="sxs-lookup"><span data-stu-id="21447-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="21447-216">Verifica anche la modifica apportata a qualsiasi app di Windows.</span><span class="sxs-lookup"><span data-stu-id="21447-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="21447-217">È possibile modificare le impostazioni del computer B di nuovo nel computer originale in impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21447-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="21447-218">Quindi Disconnetti il computer B ed effettua l'accesso al computer a per verificare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="21447-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="21447-219">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="21447-219">Other resources for this product</span></span>


-   [<span data-ttu-id="21447-220">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="21447-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="21447-221">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="21447-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="21447-222">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="21447-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="21447-223">Risoluzione dei problemi relativi a UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="21447-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="21447-224">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="21447-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





