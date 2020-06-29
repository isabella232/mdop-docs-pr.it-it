---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP1
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818155"
---
# <span data-ttu-id="8d4eb-103">Novità di Gestione avanzata Criteri di gruppo 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="8d4eb-104">Il contenuto "Novità" descrive i miglioramenti apportati e le configurazioni supportate per Microsoft Advanced Group Policy Management (Advanced criteri di gruppo) 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="8d4eb-105">Se c'è una differenza tra il contenuto e altre documentazioni della Advanced Group Policy Management, questo contenuto deve essere considerato attendibile e deve sostituire il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="8d4eb-106">Novità</span><span class="sxs-lookup"><span data-stu-id="8d4eb-106">What’s new</span></span>


<span data-ttu-id="8d4eb-107">Advanced Group Policy Management 4,0 SP1 supporta i miglioramenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d4eb-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="8d4eb-108">Estensioni lato client nuove e modificate</span><span class="sxs-lookup"><span data-stu-id="8d4eb-108">New and changed client-side extensions</span></span>

<span data-ttu-id="8d4eb-109">Le estensioni lato client di criteri di gruppo (CSEs) sono state aggiunte o modificate per Advanced Group Policy per supportare nuovi criteri di gruppo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="8d4eb-110">Questi criteri di gruppo consentono agli amministratori dei criteri di gruppo di gestire e tenere traccia delle impostazioni di criteri di gruppo specifiche di Windows 8 che cambiano tra due oggetti Criteri di gruppo o modelli.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="8d4eb-111">Puoi anche creare GPO personalizzati, con impostazioni specifiche di Windows 8 e configurare e salvare i GPO come modello.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="8d4eb-112">Per visualizzare il proprio CSEs, usare i report impostazioni e differenze disponibili nel client Advanced Group Policy Management di 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="8d4eb-113">Le nuove estensioni lato client di criteri di gruppo modificate sono:</span><span class="sxs-lookup"><span data-stu-id="8d4eb-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="8d4eb-114">**Criteri di accesso centralizzato:** Consente agli amministratori di criteri di gruppo di specificare criteri di accesso centralizzati nei server dei criteri di gruppo, ad esempio file server.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="8d4eb-115">Criteri di accesso centralizzati è un criterio di autorizzazione specificato da un elemento GPO e applicato alle destinazioni dei criteri per facilitare l'accesso centralizzato e il controllo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="8d4eb-116">Questi criteri di accesso centralizzato devono essere configurati in un computer client di criteri di gruppo in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="8d4eb-117">Un criterio di gruppo distribuisce la conoscenza di un criterio di accesso centralizzato applicabile ai computer che devono imporlo.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="8d4eb-118">**Modifiche ai criteri di risoluzione dei nomi:** Consente agli amministratori di criteri di gruppo di configurare le impostazioni per la sicurezza DNS e DirectAccess nei computer client DNS.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="8d4eb-119">Sono state aggiunte nuove schede per la configurazione delle impostazioni del server DNS generico e delle impostazioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="8d4eb-120">**Modifiche alle preferenze di criteri di gruppo:** Aggiunge il supporto per la configurazione e la gestione delle impostazioni di Internet Explorer 10 aggiunte per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="8d4eb-121">**Connessioni desktop e applicazioni remote:** Consente agli amministratori di criteri di gruppo di specificare l'URL di connessione predefinito usato per le connessioni desktop e dell'applicazione remota.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="8d4eb-122">**Opzioni di avvio di Windows per andare:** Consente agli amministratori di criteri di gruppo di configurare se il computer verrà avviato in Windows per spostarsi se è connesso un dispositivo USB che contiene un'area di lavoro Windows to go.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="8d4eb-123">**Opzioni di sospensione di Windows per andare:** Consente agli amministratori di criteri di gruppo di stabilire se un computer può usare lo stato di sospensione dell'ibernazione (S4) quando il computer viene avviato da un'area di lavoro di Windows to go.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="8d4eb-124">Feedback dei clienti e aggiornamento cumulativo</span><span class="sxs-lookup"><span data-stu-id="8d4eb-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="8d4eb-125">Advanced Group Policy Management 4,0 SP1 include un rollup di correzioni per risolvere i problemi riscontrati dopo la versione di Advanced Group Policy Management 4,0.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="8d4eb-126">Advanced Group Policy Management 4,0 SP1 contiene le correzioni più recenti fino a Microsoft Advanced gruppo criteri di gestione di 4,0 hotfix 1.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="8d4eb-127">Le impostazioni e i report differenze mostrano le nuove estensioni di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8d4eb-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="8d4eb-128">Le nuove estensioni di criteri di gruppo sono state aggiunte ai report impostazioni e differenze.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="8d4eb-129">Modifiche e supporto del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="8d4eb-129">Installer changes and support</span></span>

<span data-ttu-id="8d4eb-130">Le modifiche e il supporto per il programma di installazione di Advanced Group Policy Management 4,0 SP1 sono:</span><span class="sxs-lookup"><span data-stu-id="8d4eb-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="8d4eb-131">Se si installa Advanced Group Policy Manager 4,0 SP1 in Windows 8 o Windows Server 2012, il programma di installazione di Advanced Group Policy Management verifica che sia installato il software prerequisito richiesto (console di gestione dei criteri di gruppo e .NET 3,5 Framework).</span><span class="sxs-lookup"><span data-stu-id="8d4eb-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="8d4eb-132">Se questi prerequisiti non sono installati, l'installazione di Advanced Group Policy Management 4,0 SP1 è bloccata.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="8d4eb-133">Quando si installa Advanced Group Policy 4,0 Management SP1, l'attivazione di WCF, l'attivazione non HTTP e il servizio di attivazione processo Windows vengono abilitati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="8d4eb-134">Nei sistemi operativi client Windows Vista, Windows 7 e Windows 8 scaricare la versione appropriata di Remote System Administration Toolkit per il sistema operativo prima di installare Advanced Group Policy Management SP1 4,0.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="8d4eb-135">È supportata la compatibilità con le versioni precedenti dei sistemi operativi supportati meno recenti.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="8d4eb-136">Possibilità di eseguire l'aggiornamento o l'aggiornamento a Advanced Group Policy Management 4,0 SP1 senza immettere di nuovo i parametri di configurazione</span><span class="sxs-lookup"><span data-stu-id="8d4eb-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="8d4eb-137">È possibile aggiornare il client o il server Advanced Group Policy Management a Advanced Group Policy Management 4,0 SP1 solo da Advanced Group Policy 4,0 Management senza che venga chiesto di immettere di nuovo i parametri di configurazione, definiti "Smart Upgrade", come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="8d4eb-138">Se si esegue l'aggiornamento a Advanced Group Policy Management 4,0 SP1 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'"aggiornamento classico", che richiede di immettere di nuovo i parametri di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="8d4eb-139">Poiché ogni versione di Advanced Group Policy Management è associata a un sistema operativo specifico, vedere [scelta della versione di Advanced Group Policy Management da installare](https://go.microsoft.com/fwlink/?LinkId=254350)e assicurarsi di aggiornare il sistema operativo in modo appropriato prima di eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8d4eb-140">Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8d4eb-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-141">2,5</span><span class="sxs-lookup"><span data-stu-id="8d4eb-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-142">3,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-143">4,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d4eb-145">2,5</span><span class="sxs-lookup"><span data-stu-id="8d4eb-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-146">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-147">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="8d4eb-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-148">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="8d4eb-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-149">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="8d4eb-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d4eb-150">3,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-151">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-152">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-153">Aggiornamento classico</span><span class="sxs-lookup"><span data-stu-id="8d4eb-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-154">L'installazione è bloccata</span><span class="sxs-lookup"><span data-stu-id="8d4eb-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d4eb-155">4,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-156">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-157">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-158">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8d4eb-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-159">Aggiornamento intelligente</span><span class="sxs-lookup"><span data-stu-id="8d4eb-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8d4eb-160">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="8d4eb-160">Supported configurations</span></span>


<span data-ttu-id="8d4eb-161">Advanced Group Policy Management supporta le configurazioni nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="8d4eb-162">Anche se Advanced Group Policy Management supporta configurazioni miste, è consigliabile eseguire il client e il server Advanced Group Policy Management nella stessa famiglia di sistemi operativi, ad esempio Windows 8 con Windows Server 2012, Windows 7 con Windows Server 2008 R2 e così via.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8d4eb-163">Configurazioni supportate per il server Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-164">Configurazioni supportate per il client Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8d4eb-165">Supporto per Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="8d4eb-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d4eb-166">Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d4eb-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-167">Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d4eb-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-168">Supportato</span><span class="sxs-lookup"><span data-stu-id="8d4eb-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d4eb-169">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d4eb-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-170">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d4eb-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-171">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d4eb-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d4eb-172">Windows Server 2008 R2 o Windows 7 o Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d4eb-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-173">Windows Server 2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-174">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows Server 2008 R2 o Windows 7 o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d4eb-175">Windows Server 2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-176">Windows Server 2008 R2 o Windows 7 o Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d4eb-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-177">Supportato</span><span class="sxs-lookup"><span data-stu-id="8d4eb-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d4eb-178">Windows Server 2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-179">Windows Server 2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d4eb-180">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server 2008 R2 o Windows 7 o Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d4eb-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8d4eb-181">Prerequisiti per l'installazione di Advanced Group Policy Management 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="8d4eb-182">La tabella seguente descrive il comportamento in Windows 8 del client e dei programmi di installazione di Advanced Group Policy Management 4,0 SP1 quando non è presente .NET 3,5 o la console di gestione di criteri di gruppo negli strumenti di amministrazione del server remoto.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="8d4eb-183">Client Advanced Group Policy Management 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="8d4eb-184">Advanced Group Policy Management Server 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="8d4eb-185">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8d4eb-185">Operating System</span></span>**

**<span data-ttu-id="8d4eb-186">.NET</span><span class="sxs-lookup"><span data-stu-id="8d4eb-186">.NET</span></span>**

**<span data-ttu-id="8d4eb-187">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="8d4eb-187">RSAT</span></span>**

**<span data-ttu-id="8d4eb-188">.NET</span><span class="sxs-lookup"><span data-stu-id="8d4eb-188">.NET</span></span>**

**<span data-ttu-id="8d4eb-189">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="8d4eb-189">RSAT</span></span>**

**<span data-ttu-id="8d4eb-190">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d4eb-190">Windows 8</span></span>**

<span data-ttu-id="8d4eb-191">Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8d4eb-192">Se GPMC non è abilitato o non è installato nel sistema, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="8d4eb-193">Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8d4eb-194">Se GPMC non è abilitato o non è installato nel sistema, il programma di installazione blocca le installazioni.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="8d4eb-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d4eb-195">Windows Server 2012</span></span>**

<span data-ttu-id="8d4eb-196">Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8d4eb-197">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="8d4eb-198">Se .NET 3,5 non è abilitato o installato, il programma di installazione blocca l'istallazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="8d4eb-199">Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8d4eb-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="8d4eb-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d4eb-200">Related topics</span></span>


[<span data-ttu-id="8d4eb-201">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8d4eb-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="8d4eb-202">Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="8d4eb-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





