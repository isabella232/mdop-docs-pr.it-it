---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP2
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818146"
---
# <span data-ttu-id="95150-103">Novità di Gestione avanzata Criteri di gruppo 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="95150-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="95150-104">Questo contenuto descrive i miglioramenti e le configurazioni supportate per il servizio Pack2 (Advanced Group Policy Management) 4.0 (SP2).</span><span class="sxs-lookup"><span data-stu-id="95150-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="95150-105">Se c'è una differenza tra questo contenuto e altre documentazioni di Advanced Group Policy Management, considera questo contenuto autorevole e presupponga che sostituisca l'altra documentazione.</span><span class="sxs-lookup"><span data-stu-id="95150-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="95150-106">Novità</span><span class="sxs-lookup"><span data-stu-id="95150-106">What’s new</span></span>


<span data-ttu-id="95150-107">Advanced Group Policy Management 4.0 SP2 supporta le caratteristiche e le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="95150-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="95150-108">Supporto per Windows 8.1 e Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="95150-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="95150-109">Advanced Group Policy Management 4.0 SP2 aggiunge il supporto per i sistemi operativi Windows 8.1 e Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="95150-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="95150-110">Estensioni lato client nuove e modificate</span><span class="sxs-lookup"><span data-stu-id="95150-110">New and changed client-side extensions</span></span>

<span data-ttu-id="95150-111">Le estensioni lato client di criteri di gruppo sono state aggiunte o modificate per Advanced Group Policy Management per supportare le nuove impostazioni dei criteri in Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="95150-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="95150-112">Queste impostazioni dei criteri consentono agli amministratori dei criteri di gruppo di gestire e tenere traccia delle impostazioni dei criteri specifiche di Windows 8.1 che cambiano tra due oggetti Criteri di gruppo o i modelli.</span><span class="sxs-lookup"><span data-stu-id="95150-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="95150-113">Per visualizzare le estensioni lato client, usare i report impostazioni e differenze disponibili nel client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="95150-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="95150-114">Le nuove estensioni lato client di criteri di gruppo modificate sono:</span><span class="sxs-lookup"><span data-stu-id="95150-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="95150-115">**Specificare le impostazioni delle cartelle di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="95150-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="95150-116">Se si abilita questa impostazione, gli amministratori IT possono configurare le cartelle di lavoro per la creazione automatica.</span><span class="sxs-lookup"><span data-stu-id="95150-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="95150-117">La caratteristica cartelle di lavoro consente agli utenti finali di sincronizzare i file dai loro dispositivi desktop Windows con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="95150-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="95150-118">Usa questa impostazione per creare la relazione di sincronizzazione nei dispositivi di un utente finale e per configurare come identificare il file server in cui sono archiviate le cartelle di lavoro dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95150-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="95150-119">Se si seleziona la casella di controllo **sincronizzazione automatica provisioning** , la relazione di sincronizzazione verrà creata senza l'input dell'utente e i dati inizieranno automaticamente la sincronizzazione con il dispositivo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95150-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="95150-120">Se non si seleziona la casella di controllo **sincronizzazione automatica provisioning** , gli utenti devono fornire l'input per avviare la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="95150-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="95150-121">**Forzare la configurazione automatica per tutti gli utenti**.</span><span class="sxs-lookup"><span data-stu-id="95150-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="95150-122">Se si abilita questa impostazione, gli amministratori IT possono determinare se creare automaticamente la partnership delle cartelle di lavoro nei dispositivi dell'utente finale senza input dagli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="95150-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="95150-123">Se si abilita questa impostazione, la sincronizzazione verrà configurata in base alla configurazione dell'impostazione specifica dei criteri **delle impostazioni delle cartelle di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="95150-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="95150-124">Se si imposta l'impostazione **Imponi configurazione automatica per tutti gli utenti** su **disabilitata** o **non configurata**, la partnership delle cartelle di lavoro verrà configurata in base a come si imposta l'opzione di **provisioning automatico** nell'impostazione specifica dei criteri **delle cartelle di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="95150-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="95150-125">Per altre informazioni sulla funzionalità delle cartelle di lavoro, vedere [Panoramica delle cartelle di lavoro](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="95150-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="95150-126">Feedback dei clienti e aggiornamento cumulativo</span><span class="sxs-lookup"><span data-stu-id="95150-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="95150-127">Advanced Group Policy Management 4.0 SP2 include un rollup di hotfix per risolvere i problemi riscontrati dopo la versione del servizio Advanced Group Policy Management 4.0 Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="95150-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="95150-128">Advanced Group Policy Management 4.0 SP2 contiene le correzioni più recenti e include Microsoft Advanced Group Policy Manager 4.0 SP1 Hotfix1.</span><span class="sxs-lookup"><span data-stu-id="95150-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="95150-129">Per altre informazioni, vedere l'articolo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)della Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="95150-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="95150-130">Nuove estensioni dei criteri di gruppo nei report impostazioni e differenze</span><span class="sxs-lookup"><span data-stu-id="95150-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="95150-131">Le nuove estensioni di criteri di gruppo sono state aggiunte ai report impostazioni e differenze.</span><span class="sxs-lookup"><span data-stu-id="95150-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="95150-132">Modifiche e supporto del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="95150-132">Installer changes and support</span></span>

<span data-ttu-id="95150-133">Le modifiche e il supporto per il programma di installazione di Advanced Group Policy Management 4.0 SP2 sono:</span><span class="sxs-lookup"><span data-stu-id="95150-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="95150-134">Se si installa Advanced Group Policy Management 4.0 SP2 nel sistema operativo Windows 8 o Windows Server 2012 o nei sistemi operativi successivi, il programma di installazione della Advanced Group Policy Manager verifica che sia installato il software necessario richiesto, ovvero la console Gestione criteri di gruppo e Microsoft .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="95150-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="95150-135">Se il software prerequisito non è installato, l'installazione di Advanced Group Policy Management 4.0 SP2 è bloccata.</span><span class="sxs-lookup"><span data-stu-id="95150-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="95150-136">Quando si installa il server Advanced Group Policy Management, l'attivazione di WCF, l'attivazione non HTTP e il servizio Attivazione processo Windows vengono abilitati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="95150-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="95150-137">Nel sistema operativo client WindowsVista e nei sistemi operativi successivi scaricare la versione appropriata degli strumenti di amministrazione del sistema remoto per il sistema operativo prima di installare Advanced Group Policy Management 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="95150-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="95150-138">Advanced Group Policy Management 4.0 SP2 supporta la compatibilità con le versioni precedenti dei sistemi operativi supportati.</span><span class="sxs-lookup"><span data-stu-id="95150-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="95150-139">Possibilità di eseguire l'aggiornamento a Advanced Group Policy Management 4.0 SP2 senza immettere nuovamente i parametri di configurazione</span><span class="sxs-lookup"><span data-stu-id="95150-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="95150-140">È possibile eseguire l'aggiornamento del client Advanced Group Policy Management o del server Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP2 senza che venga chiesto di immettere nuovamente i parametri di configurazione, detti Smart Upgrade, solo da Advanced Group Policy Management 4.0, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95150-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="95150-141">Se si esegue l'aggiornamento a Advanced Group Policy Management 4.0 SP2 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'aggiornamento classico, che richiede di immettere nuovamente i parametri di configurazione.</span><span class="sxs-lookup"><span data-stu-id="95150-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="95150-142">Poiché ogni versione di Advanced Group Policy Management è associata a un particolare sistema operativo, vedere [scelta della versione di Advanced Group Policy per l'installazione](https://go.microsoft.com/fwlink/?LinkId=254350) e verificare che il sistema operativo venga aggiornato in modo appropriato prima di aggiornare Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="95150-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="95150-143">Aggiornamenti supportati di Advanced Group Policy Management SP2 4,0</span><span class="sxs-lookup"><span data-stu-id="95150-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95150-144">Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="95150-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95150-145">2,5</span><span class="sxs-lookup"><span data-stu-id="95150-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95150-146">3,0</span><span class="sxs-lookup"><span data-stu-id="95150-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95150-147">4,0</span><span class="sxs-lookup"><span data-stu-id="95150-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95150-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="95150-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95150-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="95150-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95150-150">2,5</span><span class="sxs-lookup"><span data-stu-id="95150-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-151">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-152">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="95150-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-153">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="95150-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-154">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="95150-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-155">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="95150-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95150-156">3,0</span><span class="sxs-lookup"><span data-stu-id="95150-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-157">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-158">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-159">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="95150-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-160">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="95150-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-161">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="95150-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95150-162">4,0</span><span class="sxs-lookup"><span data-stu-id="95150-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-163">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-164">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-165">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-166">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="95150-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-167">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="95150-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95150-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="95150-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-169">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-170">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-171">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-172">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="95150-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-173">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="95150-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="95150-174">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="95150-174">Supported configurations</span></span>


<span data-ttu-id="95150-175">Advanced Group Policy Management 4.0 SP2 supporta le configurazioni della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95150-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="95150-176">Anche se Advanced Group Policy Management supporta configurazioni miste, ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistema operativo, ad esempio Windows 8.1 con Windows Server2012 R2, Windows 8 con Windows Server 2012 e così via.</span><span class="sxs-lookup"><span data-stu-id="95150-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="95150-177">Sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="95150-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="95150-178">Configurazioni supportate per il server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="95150-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="95150-179">Configurazioni supportate per il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="95150-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="95150-180">Supporto per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="95150-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95150-181">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95150-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-182">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95150-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-183">Supportato</span><span class="sxs-lookup"><span data-stu-id="95150-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95150-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="95150-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-185">Windows Server 2012 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="95150-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-186">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95150-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95150-187">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-188">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-189">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="95150-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95150-190">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-191">Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="95150-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-192">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95150-193">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="95150-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-194">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-195">Non supportato</span><span class="sxs-lookup"><span data-stu-id="95150-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95150-196">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="95150-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-197">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="95150-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95150-198">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="95150-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="95150-199">Prerequisiti per l'installazione di Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="95150-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="95150-200">La tabella seguente descrive il comportamento dei programmi di installazione del client e del server di Advanced Group Policy Management 4.0 SP2 in Windows 8.1 quando mancano gli strumenti di amministrazione del server remoto .NET Framework 3.5 o GPMC.</span><span class="sxs-lookup"><span data-stu-id="95150-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="95150-201">Client Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="95150-201">AGPM Client</span></span>**

**<span data-ttu-id="95150-202">Server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="95150-202">AGPM Server</span></span>**

**<span data-ttu-id="95150-203">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="95150-203">Operating system</span></span>**

**<span data-ttu-id="95150-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="95150-204">.NET Framework</span></span>**

**<span data-ttu-id="95150-205">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="95150-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="95150-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="95150-206">.NET Framework</span></span>**

**<span data-ttu-id="95150-207">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="95150-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="95150-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95150-208">Windows8.1</span></span>**

<span data-ttu-id="95150-209">Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="95150-210">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="95150-211">Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="95150-212">Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="95150-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="95150-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="95150-214">Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="95150-215">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="95150-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="95150-216">Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="95150-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="95150-217">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="95150-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="95150-218">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="95150-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="95150-219">Advanced Group Policy Management 4,0 SP2 fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="95150-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="95150-220">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="95150-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="95150-221">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="95150-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="95150-222">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95150-222">Related topics</span></span>


[<span data-ttu-id="95150-223">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="95150-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="95150-224">Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="95150-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="95150-225">Scelta della versione di Gestione avanzata Criteri di gruppo da installare</span><span class="sxs-lookup"><span data-stu-id="95150-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





