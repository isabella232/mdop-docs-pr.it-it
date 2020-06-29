---
title: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 4.0
description: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820196"
---
# <span data-ttu-id="c34a5-103">Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 4.0</span><span class="sxs-lookup"><span data-stu-id="c34a5-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="c34a5-104">Questa guida dettagliata illustra le tecniche avanzate per la gestione dei criteri di gruppo che usano la console Gestione criteri di gruppo e la gestione avanzata Criteri di gruppo di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c34a5-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="c34a5-105">Advanced Group Policy Management aumenta le funzionalità di GPMC, fornendo:</span><span class="sxs-lookup"><span data-stu-id="c34a5-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="c34a5-106">Ruoli standard per la delega delle autorizzazioni per la gestione degli oggetti Criteri di gruppo (GPO) in più amministratori di criteri di gruppo, oltre alla possibilità di delegare l'accesso a GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="c34a5-107">Un archivio per consentire agli amministratori dei criteri di gruppo di creare e modificare i GPO offline prima della distribuzione degli oggetti Criteri di rete in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="c34a5-108">Possibilità di ripristinare una versione precedente di un GPO nell'archivio e limitare il numero di versioni archiviate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="c34a5-109">Funzionalità di archiviazione e estrazione per i GPO per assicurarsi che gli amministratori dei criteri di gruppo non sovrascrivano involontariamente il lavoro reciproco.</span><span class="sxs-lookup"><span data-stu-id="c34a5-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="c34a5-110">Possibilità di cercare gli oggetti Criteri di ricerca con attributi specifici e filtrare l'elenco dei GPO visualizzati.</span><span class="sxs-lookup"><span data-stu-id="c34a5-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="c34a5-111">Panoramica degli scenari Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-111">AGPM scenario overview</span></span>


<span data-ttu-id="c34a5-112">Per questo scenario, si utilizzerà un account utente distinto per ogni ruolo in Advanced Group Policy Management per dimostrare in che modo i criteri di gruppo possono essere gestiti in un ambiente che include più amministratori di criteri di gruppo con livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="c34a5-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="c34a5-113">In particolare, verranno eseguite le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="c34a5-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="c34a5-114">L'uso di un account membro del gruppo Domain Admins consente di installare Advanced Group Policy Management e assegnare il ruolo di amministratore Advanced Group Policy Management a un account o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="c34a5-115">Uso degli account a cui assegnare i ruoli di Advanced Group Policy Management, installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="c34a5-116">Se si usa un account con il ruolo di amministratore Advanced Group Policy Management, configurare Advanced Group Policy Management e delegare l'accesso a GPO assegnando ruoli ad altri account.</span><span class="sxs-lookup"><span data-stu-id="c34a5-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="c34a5-117">Da un account che ha il ruolo di editor, Richiedi che venga creato un nuovo oggetto Criteri di stato per l'approvazione usando un account con il ruolo di responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="c34a5-118">Usare l'account dell'editor per verificare che l'oggetto Criteri di ricerca sia fuori dall'archivio, modificare l'oggetto Criteri di controllo, selezionare l'oggetto Criteri di ricerca nell'archivio e quindi richiedere la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="c34a5-119">Se si usa un account con il ruolo di approvazione, esaminare l'oggetto Criteri di controllo e distribuirlo nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="c34a5-120">Usando un account con il ruolo di editor, crea un modello di GPO e usalo come punto di partenza per creare un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="c34a5-121">Usando un account con il ruolo di responsabile approvazione, eliminare e ripristinare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![processo di sviluppo degli oggetti Criteri di gruppo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="c34a5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c34a5-123">Requirements</span></span>


<span data-ttu-id="c34a5-124">I computer in cui si vuole installare Advanced Group Policy Management devono soddisfare i requisiti seguenti ed è necessario creare account per l'uso in questo scenario.</span><span class="sxs-lookup"><span data-stu-id="c34a5-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="c34a5-125">**Nota**  Se è installato Advanced Group Policy Management 2,5 e si esegue l'aggiornamento da Windows Server® 2003 a Windows Server2008R2 o Windows Server2008 o si esegue l'aggiornamento da WindowsVista senza Service Pack installati in Windows7 o WindowsVista® con Service Pack1 (SP1), è necessario aggiornare il sistema operativo prima di poter eseguire l'aggiornamento a Advanced Group Policy Management 4.0.</span><span class="sxs-lookup"><span data-stu-id="c34a5-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="c34a5-126">Se è installato Advanced Group Policy Management 3,0, non è necessario aggiornare il sistema operativo prima di eseguire l'aggiornamento a Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="c34a5-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="c34a5-127">In un ambiente misto che include sia sistemi operativi più recenti che vecchi, esistono alcune limitazioni alla funzionalità, come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c34a5-128">Sistema operativo in cui viene eseguito Advanced Server Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="c34a5-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="c34a5-129">Sistema operativo in cui viene eseguito il client Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="c34a5-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="c34a5-130">Stato del supporto per Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="c34a5-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c34a5-131">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-132">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="c34a5-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c34a5-134">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-135">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c34a5-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-136">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c34a5-137">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c34a5-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-138">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-139">File modifiche disco non supportato</span><span class="sxs-lookup"><span data-stu-id="c34a5-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c34a5-140">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c34a5-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-141">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="c34a5-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c34a5-142">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="c34a5-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c34a5-143">Requisiti del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-143">AGPM Server requirements</span></span>

<span data-ttu-id="c34a5-144">Advanced Group Policy Management 4.0 richiede Windows Server2008R2, Windows Server2008, Windows7 e GPMC da Remote Server Administration Tools (strumenti di amministrazione remota) o Windows Vista con SP1 e la console GPMC installata.</span><span class="sxs-lookup"><span data-stu-id="c34a5-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="c34a5-145">Sono supportate entrambe le versioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c34a5-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="c34a5-146">Prima di installare Advanced Group Policy Management Server, è necessario essere un membro del gruppo Domain Admins e le caratteristiche di Windows seguenti devono essere presenti, se non diversamente specificato:</span><span class="sxs-lookup"><span data-stu-id="c34a5-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="c34a5-147">GPMC</span><span class="sxs-lookup"><span data-stu-id="c34a5-147">GPMC</span></span>

    -   <span data-ttu-id="c34a5-148">Windows Server2008R2 o Windows Server2008: se la GPMC non è presente, viene automaticamente installata da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="c34a5-149">Windows7: prima di installare Advanced Group Policy Management, è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="c34a5-150">Per altre informazioni, vedere [strumenti di amministrazione di server remoti per Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="c34a5-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="c34a5-151">Windows Vista con SP1: prima di installare Advanced Group Policy Management è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="c34a5-152">Per altre informazioni, vedere [strumenti di amministrazione di server remoti per Windows Vista con Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="c34a5-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="c34a5-153">.NET Framework 3,5 o versioni successive</span><span class="sxs-lookup"><span data-stu-id="c34a5-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="c34a5-154">Windows Server2008R2 o Windows7: se .NET Framework 3,5 o versione successiva non è presente, .NET Framework 3,5 viene installato automaticamente da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="c34a5-155">Windows Server2008 o Windows Vista con SP1: è necessario installare .NET Framework 3,5 o una versione successiva prima di installare Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="c34a5-156">Le funzionalità di Windows seguenti sono richieste dal server Advanced Group Policy Management e verranno installate automaticamente se non sono presenti:</span><span class="sxs-lookup"><span data-stu-id="c34a5-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="c34a5-157">Attivazione di WCF; Attivazione non HTTP</span><span class="sxs-lookup"><span data-stu-id="c34a5-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="c34a5-158">Servizio Attivazione dei processi Windows</span><span class="sxs-lookup"><span data-stu-id="c34a5-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="c34a5-159">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="c34a5-159">Process Model</span></span>

    -   <span data-ttu-id="c34a5-160">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="c34a5-160">The .NET Environment</span></span>

    -   <span data-ttu-id="c34a5-161">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="c34a5-161">Configuration APIs</span></span>

### <span data-ttu-id="c34a5-162">Requisiti client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-162">AGPM Client requirements</span></span>

<span data-ttu-id="c34a5-163">Il client Advanced Group Policy Management 4.0 richiede Windows Server2008R2, Windows Server2008, Windows7 e GPMC da parte di amministrazione remota o Windows Vista con SP1 e la console Gestione criteri di amministrazione di Microsoft installato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="c34a5-164">Sono supportate entrambe le versioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c34a5-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="c34a5-165">Il client Advanced Group Policy Management può essere installato in un computer in cui è in uso Advanced Management Server.</span><span class="sxs-lookup"><span data-stu-id="c34a5-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="c34a5-166">Le funzionalità di Windows seguenti sono richieste dal client Advanced Group Policy Management e, se non diversamente specificato, non vengono installate automaticamente se non sono presenti:</span><span class="sxs-lookup"><span data-stu-id="c34a5-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="c34a5-167">GPMC</span><span class="sxs-lookup"><span data-stu-id="c34a5-167">GPMC</span></span>

    -   <span data-ttu-id="c34a5-168">Windows Server2008R2 o Windows Server2008: se la GPMC non è presente, viene automaticamente installata da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="c34a5-169">Windows7: prima di installare Advanced Group Policy Management, è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="c34a5-170">Per altre informazioni, vedere [strumenti di amministrazione di server remoti per Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="c34a5-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="c34a5-171">Windows Vista con SP1: prima di installare Advanced Group Policy Management è necessario installare la console Gestione criteri di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="c34a5-172">Per altre informazioni, vedere [strumenti di amministrazione di server remoti per Windows Vista con Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="c34a5-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="c34a5-173">.NET Framework 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c34a5-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="c34a5-174">Windows Server2008R2 o Windows7: se .NET Framework 3,0 o versione successiva non è presente, .NET Framework 3,5 viene installato automaticamente da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="c34a5-175">Windows Server2008 o Windows Vista con SP1: se .NET Framework 3,0 o versione successiva non è presente, .NET Framework 3,0 viene installato automaticamente da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="c34a5-176">Requisiti per lo scenario</span><span class="sxs-lookup"><span data-stu-id="c34a5-176">Scenario requirements</span></span>

<span data-ttu-id="c34a5-177">Prima di iniziare questo scenario, creare quattro account utente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="c34a5-178">Durante lo scenario, verrà assegnato uno dei ruoli di Advanced Group Policy Management seguenti a ognuno di questi account: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore.</span><span class="sxs-lookup"><span data-stu-id="c34a5-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="c34a5-179">Questi account devono essere in grado di inviare e ricevere messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="c34a5-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="c34a5-180">Assegnare l'autorizzazione **collegamento GPO** agli account con l'amministratore, l'approvatore della gestione avanzata Criteri di amministrazione e i ruoli di Editor (facoltativamente).</span><span class="sxs-lookup"><span data-stu-id="c34a5-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="c34a5-181">**Nota** 
 L'autorizzazione **collegamento GPO** viene assegnata ai membri di amministratori di dominio e amministratori aziendali per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c34a5-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="c34a5-182">Per assegnare l'autorizzazione **collegamento GPO** ad altri utenti o gruppi, ad esempio account che hanno il ruolo di amministratore o approvatore della gestione avanzata, fare clic sul nodo per il dominio e quindi fare clic sulla scheda **delega** , selezionare **Collega oggetti Criteri**di gruppo, fare clic su **Aggiungi**e selezionare gli utenti o i gruppi a cui si vuole assegnare l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="c34a5-183">Procedura per l'installazione e la configurazione di Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="c34a5-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="c34a5-184">Per installare e configurare Advanced Group Policy Management, è necessario completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="c34a5-185">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="c34a5-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="c34a5-186">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="c34a5-187">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="c34a5-188">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="c34a5-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="c34a5-189">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="c34a5-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="c34a5-190">Passaggio 1: installare Advanced Group Policy Management Server</span><span class="sxs-lookup"><span data-stu-id="c34a5-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="c34a5-191">In questo passaggio verrà installato il server Advanced Group Policy Management nel server membro o controller di dominio che eseguirà il servizio Advanced Group Policy Management e si configurerà l'archivio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="c34a5-192">Tutte le operazioni Advanced Group Policy Management vengono gestite tramite questo servizio Windows e vengono eseguite con le credenziali del servizio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="c34a5-193">L'archivio gestito da un server Advanced Group Policy Management può essere ospitato in tale server o in un altro server della stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="c34a5-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="c34a5-194">Per installare Advanced Group Policy Management Server nel computer in cui è ospitato il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="c34a5-195">Accedere con un account membro del gruppo Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="c34a5-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="c34a5-196">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-server**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="c34a5-197">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="c34a5-198">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="c34a5-199">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="c34a5-200">Il computer in cui è installato il server Advanced Group Policy Management ospita il servizio Advanced Group Policy Management e gestisce l'archivio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="c34a5-201">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-201">Click **Next**.</span></span>

6.  <span data-ttu-id="c34a5-202">Nella finestra di dialogo **percorso di archiviazione** selezionare una posizione per l'archivio in relazione al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="c34a5-203">Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o in un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="c34a5-204">Devi tuttavia selezionare una posizione con spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="c34a5-205">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-205">Click **Next**.</span></span>

7.  <span data-ttu-id="c34a5-206">Nella finestra di dialogo **account del servizio Advanced Group Policy Management** selezionare un account del servizio in cui verrà eseguito il servizio Advanced Group Policy Management e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="c34a5-207">Questo account deve essere un membro del gruppo Domain Admins oppure, per una configurazione con privilegi minimi, i gruppi seguenti di ogni dominio gestiti dal server Advanced Group Policy Management:</span><span class="sxs-lookup"><span data-stu-id="c34a5-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="c34a5-208">Proprietari di autori di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c34a5-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="c34a5-209">Operatori di backup</span><span class="sxs-lookup"><span data-stu-id="c34a5-209">Backup Operators</span></span>

    <span data-ttu-id="c34a5-210">Questo account richiede inoltre l'autorizzazione controllo completo per le cartelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="c34a5-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="c34a5-211">Cartella di archiviazione Advanced Group Policy Management, per cui questa autorizzazione viene concessa automaticamente durante l'installazione del server Advanced Group Policy Management se è installata in un'unità locale.</span><span class="sxs-lookup"><span data-stu-id="c34a5-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="c34a5-212">Cartella Temp di sistema locale, in genere%windir%\\temp.</span><span class="sxs-lookup"><span data-stu-id="c34a5-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="c34a5-213">Nella finestra di dialogo **proprietario archivio** selezionare un account o un gruppo a cui assegnare il ruolo amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="c34a5-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="c34a5-214">Gli amministratori Advanced Group Policy Management possono assegnare i ruoli e le autorizzazioni di Advanced Policy Management ad altri amministratori dei criteri di gruppo, in modo che in seguito sia possibile assegnare il ruolo di amministratore Advanced Group Policy per altri amministratori</span><span class="sxs-lookup"><span data-stu-id="c34a5-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="c34a5-215">Per questo scenario, selezionare l'account da usare nel ruolo amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="c34a5-216">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-216">Click **Next**.</span></span>

9.  <span data-ttu-id="c34a5-217">Nella finestra di dialogo **configurazione porta** Digitare una porta in cui deve essere ascoltato il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="c34a5-218">Non deselezionare la casella **di controllo Aggiungi eccezione alla porta al firewall** a meno che non si configuri manualmente le eccezioni della porta o non si usi regole per configurare le eccezioni della porta.</span><span class="sxs-lookup"><span data-stu-id="c34a5-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="c34a5-219">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-219">Click **Next**.</span></span>

10. <span data-ttu-id="c34a5-220">Nella finestra di dialogo **lingue** selezionare una o più lingue di visualizzazione da installare per il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="c34a5-221">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="c34a5-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="c34a5-222">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="c34a5-223">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="c34a5-224">Per informazioni su come modificare le impostazioni per il servizio, vedere la guida per la gestione avanzata dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="c34a5-225">Passaggio 2: installare il client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="c34a5-226">Ogni amministratore dei criteri di gruppo, tutti gli utenti che creano, modifica, distribuisce, esamina o Elimina GPO, deve avere installato client Advanced Group Policy Management in computer che usano per gestire i GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="c34a5-227">Il nodo cambia controllo, che si usa per eseguire molte delle attività di gestione degli oggetti Criteri di gruppo, viene visualizzato nella console di gestione dei criteri di raggruppamento solo se si installa il client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="c34a5-228">Per questo scenario, è possibile installare il client Advanced Group Policy in almeno un computer.</span><span class="sxs-lookup"><span data-stu-id="c34a5-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="c34a5-229">Non è necessario installare il client Advanced Group Policy Management nei computer degli utenti finali che non eseguono l'amministrazione dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="c34a5-230">Per installare il client Advanced Group Policy Management nel computer di un amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c34a5-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="c34a5-231">Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione criteri di gruppo avanzati-client**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="c34a5-232">Nella finestra di dialogo **Introduzione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="c34a5-233">Nella finestra di dialogo **condizioni di licenza software Microsoft** accettare i termini e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="c34a5-234">Nella finestra di dialogo **percorso applicazione** selezionare una posizione in cui installare client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="c34a5-235">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-235">Click **Next**.</span></span>

5.  <span data-ttu-id="c34a5-236">Nella finestra di dialogo **server Advanced Group Policy Management** Digitare il nome DNS o l'indirizzo IP per il server Advanced Group Policy Management e la porta a cui si desidera connettersi.</span><span class="sxs-lookup"><span data-stu-id="c34a5-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="c34a5-237">La porta predefinita per il servizio Advanced Group Policy Management è 4600.</span><span class="sxs-lookup"><span data-stu-id="c34a5-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="c34a5-238">Non deselezionare la casella di controllo **Consenti Microsoft Management Console tramite il firewall** a meno che tu non configuri manualmente le eccezioni della porta o usi regole per configurare le eccezioni della porta.</span><span class="sxs-lookup"><span data-stu-id="c34a5-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="c34a5-239">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-239">Click **Next**.</span></span>

6.  <span data-ttu-id="c34a5-240">Nella finestra di dialogo **lingue** selezionare una o più lingue di visualizzazione da installare per il client Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="c34a5-241">Fare clic su **Installa**e quindi su **fine** per uscire dalla configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="c34a5-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="c34a5-242">Passaggio 3: configurare una connessione al server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="c34a5-243">La Advanced Group Policy Management archivia tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato, ovvero ogni GPO per cui Advanced Group Policy Management fornisce il controllo delle modifiche in un archivio centrale.</span><span class="sxs-lookup"><span data-stu-id="c34a5-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="c34a5-244">In questo modo gli amministratori di criteri di gruppo visualizzano e modificano i GPO offline senza influire immediatamente sulla versione distribuita di ogni GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="c34a5-245">In questo passaggio si configura una connessione al server Advanced Group Policy Management e si assicura che tutti gli amministratori di criteri di gruppo si connettano allo stesso server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="c34a5-246">Per informazioni su come configurare più server Advanced Group Policy Management, vedere Guida per la gestione avanzata di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="c34a5-247">Per configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c34a5-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="c34a5-248">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con l'account utente selezionato come proprietario dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="c34a5-249">Questo utente ha il ruolo di amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="c34a5-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="c34a5-250">Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **Gestione criteri di gruppo** per aprire la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="c34a5-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="c34a5-251">Modificare un GPO applicato a tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="c34a5-252">Nella finestra **Editor gestione criteri di gruppo** fare doppio clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="c34a5-253">Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="c34a5-254">Nella finestra **Proprietà** selezionare **abilitato** e digitare il nome DNS o l'indirizzo IP e la porta, ad esempio **Server.contoso.com:4600**, per il server che ospita l'archivio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="c34a5-255">Per impostazione predefinita, il servizio Advanced Group Policy Management usa la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="c34a5-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="c34a5-256">Fare clic su **OK**e quindi chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="c34a5-257">Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management viene configurata per ogni amministratore di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="c34a5-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="c34a5-258">Passaggio 4: configurare la notifica tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="c34a5-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="c34a5-259">In qualità di amministratore Advanced Group Policy Management (controllo completo), designa gli indirizzi di posta elettronica degli approvatori e degli amministratori della Advanced Group Policy per cui viene inviato un messaggio di posta elettronica che contiene una richiesta quando un editor prova a creare, distribuire o eliminare un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="c34a5-260">Puoi anche determinare l'alias da cui vengono inviati questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="c34a5-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="c34a5-261">Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="c34a5-262">In **Editor gestione criteri di gruppo** passare alla cartella **Cambia controllo**</span><span class="sxs-lookup"><span data-stu-id="c34a5-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="c34a5-263">Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="c34a5-264">Nel campo **da indirizzo di posta elettronica** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="c34a5-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="c34a5-265">Nel campo **indirizzo di posta elettronica** Digitare l'indirizzo di posta elettronica per l'account utente a cui si vuole assegnare il ruolo di approvatore.</span><span class="sxs-lookup"><span data-stu-id="c34a5-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="c34a5-266">Nel campo **server SMTP** Digitare un server di posta SMTP valido.</span><span class="sxs-lookup"><span data-stu-id="c34a5-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="c34a5-267">Nei campi **nome utente** e **password** digitare le credenziali di un utente che ha accesso al servizio SMTP.</span><span class="sxs-lookup"><span data-stu-id="c34a5-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="c34a5-268">Fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="c34a5-269">Passaggio 5: delega dell'accesso</span><span class="sxs-lookup"><span data-stu-id="c34a5-269">Step 5: Delegate access</span></span>

<span data-ttu-id="c34a5-270">In qualità di amministratore Advanced Group Policy Management (controllo completo) deleghi l'accesso a livello di dominio a GPO, assegnando ruoli all'account di ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="c34a5-271">**Nota**  È anche possibile delegare l'accesso a livello di GPO invece che a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="c34a5-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="c34a5-272">Per altre informazioni, vedere la guida per la gestione avanzata dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="c34a5-273">**Importante**  È necessario limitare l'appartenenza al gruppo proprietari creatori di criteri di gruppo in modo che non possa essere usato per eludere la gestione di Access a GPO per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="c34a5-274">Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="c34a5-275">Per delegare l'accesso a tutti i GPO in un dominio</span><span class="sxs-lookup"><span data-stu-id="c34a5-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="c34a5-276">Nella scheda **delega del dominio** fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da responsabile approvazione e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="c34a5-277">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo **approvatore** per assegnare il ruolo all'account e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="c34a5-278">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="c34a5-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="c34a5-279">Fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da Editor e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="c34a5-280">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo di **Editor** per assegnare il ruolo all'account e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="c34a5-281">Questo ruolo include il ruolo di revisore.</span><span class="sxs-lookup"><span data-stu-id="c34a5-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="c34a5-282">Fare clic sul pulsante **Aggiungi** , selezionare l'account utente dell'amministratore dei criteri di gruppo per fungere da revisore e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="c34a5-283">Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare il ruolo **revisore** per assegnare solo il ruolo all'account.</span><span class="sxs-lookup"><span data-stu-id="c34a5-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="c34a5-284">Procedura per la gestione dei GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-284">Steps for managing GPOs</span></span>


<span data-ttu-id="c34a5-285">Per creare, modificare, rivedere e distribuire GPO tramite Advanced Group Policy, è necessario completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="c34a5-286">Verrà inoltre creato un modello, eliminato un oggetto Criteri di stato e il ripristino di un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="c34a5-287">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="c34a5-288">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="c34a5-289">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="c34a5-290">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="c34a5-291">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="c34a5-292">Passaggio 1: creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="c34a5-293">In un ambiente che include più amministratori di criteri di gruppo, gli utenti con il ruolo Editor possono richiedere la creazione di nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="c34a5-294">Tuttavia, tale richiesta deve essere approvata da un utente con il ruolo di approvatore.</span><span class="sxs-lookup"><span data-stu-id="c34a5-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="c34a5-295">In questo passaggio si usa un account che ha il ruolo di editor per richiedere la creazione di un nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="c34a5-296">Usando un account con il ruolo di responsabile approvazione, approvare la richiesta per creare l'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="c34a5-297">Per richiedere che un nuovo GPO venga creato e gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="c34a5-298">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è stato assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="c34a5-299">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="c34a5-300">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="c34a5-301">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="c34a5-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="c34a5-302">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="c34a5-303">Digitare **MioGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="c34a5-304">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c34a5-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="c34a5-305">Fare clic su **Crea Live** in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="c34a5-306">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="c34a5-307">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-308">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="c34a5-309">Per approvare la richiesta in sospeso per creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="c34a5-310">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente con il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="c34a5-311">Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con la richiesta dell'editor per creare un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c34a5-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="c34a5-312">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="c34a5-313">Nella scheda **contenuto** fare clic sulla scheda **in sospeso** per visualizzare gli oggetti Criteri di stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c34a5-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="c34a5-314">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="c34a5-315">Fare clic su **Sì** per confermare l'approvazione e portare il GPO nella scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="c34a5-316">Passaggio 2: modificare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="c34a5-317">Puoi usare i GPO per configurare le impostazioni di computer o utenti e distribuirle a molti computer o utenti.</span><span class="sxs-lookup"><span data-stu-id="c34a5-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="c34a5-318">In questo passaggio si usa un account con il ruolo di editor per estrarre un GPO dall'archivio, modificare l'oggetto Criteri di controllo offline, controllare l'oggetto Criteri di controllo modificato nell'archivio e richiedere la distribuzione del GPO all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="c34a5-319">Per questo scenario, devi configurare un'impostazione nell'oggetto Criteri di ricerca per richiedere che la password sia lunga almeno otto caratteri.</span><span class="sxs-lookup"><span data-stu-id="c34a5-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="c34a5-320">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="c34a5-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="c34a5-321">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente con il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="c34a5-322">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="c34a5-323">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="c34a5-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="c34a5-324">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="c34a5-325">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="c34a5-326">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-327">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="c34a5-328">Per modificare l'oggetto Criteri di stato offline e configurare la lunghezza minima della password</span><span class="sxs-lookup"><span data-stu-id="c34a5-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="c34a5-329">Nella scheda **controllo** , fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **modifica** per aprire la finestra dell' **Editor gestione criteri di gruppo** e modificare una copia offline dell'oggetto GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="c34a5-330">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="c34a5-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="c34a5-331">In **Configurazione computer**fare doppio clic su **criteri**, **impostazioni di Windows**, **impostazioni di sicurezza**, criteri **account**e **criteri password**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="c34a5-332">Nel riquadro dei dettagli fare doppio clic su **lunghezza minima password**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="c34a5-333">Nella finestra Proprietà selezionare la casella di controllo **Definisci l'impostazione del criterio** , impostare il numero di caratteri su **8**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="c34a5-334">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="c34a5-335">Per controllare l'oggetto Criteri di ricerca nell'archivio</span><span class="sxs-lookup"><span data-stu-id="c34a5-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="c34a5-336">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Archivia**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="c34a5-337">Digitare un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="c34a5-338">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-339">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="c34a5-340">Per richiedere la distribuzione del GPO all'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="c34a5-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="c34a5-341">Nella scheda **controllato** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **Distribuisci**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="c34a5-342">Poiché questo account non è un approvatore o un amministratore della Advanced Group Policy Management, è necessario inviare una richiesta di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="c34a5-343">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="c34a5-344">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="c34a5-345">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-346">**MioGPO** viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="c34a5-347">Passaggio 3: rivedere e distribuire un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="c34a5-348">In questo passaggio si funge da approvatore, si creano report e si analizzano le impostazioni e le modifiche apportate alle impostazioni nell'oggetto Criteri di stato per determinare se è necessario approvarle.</span><span class="sxs-lookup"><span data-stu-id="c34a5-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="c34a5-349">Dopo aver valutato l'oggetto Criteri di gruppo, è necessario distribuirlo nell'ambiente di produzione e collegare il GPO a un dominio o a un'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="c34a5-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="c34a5-350">L'oggetto Criteri di gruppo ha effetto quando i criteri di raggruppamento vengono aggiornati per i computer in tale dominio o OU.</span><span class="sxs-lookup"><span data-stu-id="c34a5-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="c34a5-351">Per rivedere le impostazioni nel GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="c34a5-352">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è assegnato il ruolo di responsabile approvazione in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="c34a5-353">Qualsiasi amministratore di criteri di gruppo con il ruolo revisore, incluso in tutti gli altri ruoli, può rivedere le impostazioni di un oggetto Criteri di tipo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="c34a5-354">Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias Advanced Group Policy Management con una richiesta dell'editor per distribuire un oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c34a5-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="c34a5-355">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="c34a5-356">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="c34a5-357">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="c34a5-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="c34a5-358">Esaminare le impostazioni della versione più recente di MioGPO:</span><span class="sxs-lookup"><span data-stu-id="c34a5-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="c34a5-359">Nella finestra **cronologia** fare clic con il pulsante destro del mouse sulla versione del GPO con l'indicatore di data e ora più recente, scegliere **Impostazioni**e quindi fare clic su **report HTML** per visualizzare un riepilogo delle impostazioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="c34a5-360">Nel Web browser fare clic su **Mostra tutto** per visualizzare tutte le impostazioni nel GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="c34a5-361">Chiudi il browser.</span><span class="sxs-lookup"><span data-stu-id="c34a5-361">Close the browser.</span></span>

7. <span data-ttu-id="c34a5-362">Confrontare la versione più recente di MioGPO con la prima versione archiviata:</span><span class="sxs-lookup"><span data-stu-id="c34a5-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="c34a5-363">Nella finestra **cronologia** fare clic sulla versione del GPO con l'indicatore di data e ora più recente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="c34a5-364">Premere CTRL e quindi fare clic sulla versione più recente del GPO per cui la **versione del computer** non è \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="c34a5-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="c34a5-365">Fare clic sul pulsante **differenze** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-365">Click the **Differences** button.</span></span> <span data-ttu-id="c34a5-366">La sezione criteri **account/criteri password** è evidenziata in verde e preceduta da **\ [+ \]**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="c34a5-367">Ciò indica che l'impostazione è configurata solo nella seconda versione dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="c34a5-368">Fare clic su **criteri account/password**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="c34a5-369">L'impostazione **lunghezza minima password** viene evidenziata anche in verde e preceduta da **\ [+ \]**, che indica che è configurata solo nella seconda versione del GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="c34a5-370">Chiudere il Web browser.</span><span class="sxs-lookup"><span data-stu-id="c34a5-370">Close the Web browser.</span></span>

**<span data-ttu-id="c34a5-371">Per distribuire il GPO nell'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="c34a5-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="c34a5-372">Nella scheda **in sospeso** fare clic con il pulsante destro del mouse su **MioGPO** e quindi scegliere **approva**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="c34a5-373">Digitare un commento da includere nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="c34a5-374">Fai clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-374">Click **Yes**.</span></span> <span data-ttu-id="c34a5-375">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-376">Il GPO viene distribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="c34a5-377">Per collegare l'oggetto Criteri di gruppo a un dominio o un'unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="c34a5-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="c34a5-378">In GPMC fare clic con il pulsante destro del mouse sul dominio o su un'unità organizzativa a cui si vuole applicare il GPO configurato e quindi scegliere **collega un oggetto Criteri**di gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="c34a5-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="c34a5-379">Nella finestra di dialogo **Seleziona GPO** fare clic su **MioGPO**e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="c34a5-380">Passaggio 4: usare un modello per creare un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="c34a5-381">In questo passaggio si usa un account che ha il ruolo di editor per creare e usare un modello.</span><span class="sxs-lookup"><span data-stu-id="c34a5-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="c34a5-382">Questo modello è una versione statica di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="c34a5-383">Anche se non è possibile modificare un modello, è possibile creare un nuovo GPO basato su un modello.</span><span class="sxs-lookup"><span data-stu-id="c34a5-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="c34a5-384">I modelli sono utili per creare rapidamente più oggetti Criteri di gruppo che includono molte delle stesse impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c34a5-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="c34a5-385">Per creare un modello basato su un oggetto Criteri di lavoro esistente</span><span class="sxs-lookup"><span data-stu-id="c34a5-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="c34a5-386">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="c34a5-387">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="c34a5-388">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="c34a5-389">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Salva come modello** per creare un modello che incorpora tutte le impostazioni attualmente in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="c34a5-390">Digitare **MyTemplate** come nome per il modello e un commento e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="c34a5-391">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-392">Il nuovo modello viene visualizzato nella scheda **modelli** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="c34a5-393">Per richiedere che un nuovo GPO venga creato e gestito tramite Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c34a5-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="c34a5-394">Fare clic sulla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="c34a5-395">Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="c34a5-396">Nella finestra di dialogo **nuovo GPO controllato** :</span><span class="sxs-lookup"><span data-stu-id="c34a5-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="c34a5-397">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="c34a5-398">Digitare **MioaltroGPO** come nome per il nuovo oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="c34a5-399">Digitare un commento per il nuovo oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c34a5-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="c34a5-400">Fare clic su **Crea Live** in modo che il nuovo GPO venga distribuito nell'ambiente di produzione immediatamente dopo l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="c34a5-401">Per **da modello GPO**selezionare **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="c34a5-402">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="c34a5-403">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-404">Il nuovo GPO viene visualizzato nella scheda **in sospeso** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="c34a5-405">Usare un account a cui è assegnato il ruolo di approvatore per approvare la richiesta in sospeso per creare l'oggetto Criteri di stato nel [passaggio 1: creare un oggetto Criteri](#bkmk-manage1)di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="c34a5-406">MyTemplate incorpora tutte le impostazioni configurate in MioGPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="c34a5-407">Poiché MioaltroGPO è stato creato con MyTemplate, contiene inizialmente tutte le impostazioni contenute in MioGPO nel momento in cui è stato creato MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="c34a5-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="c34a5-408">Puoi confermare questa operazione generando un report differenza per confrontare MioaltroGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="c34a5-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="c34a5-409">Per controllare l'oggetto Criteri di ricerca dall'archivio per la modifica</span><span class="sxs-lookup"><span data-stu-id="c34a5-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="c34a5-410">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è assegnato il ruolo di editor in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c34a5-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="c34a5-411">Fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **Estrai**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="c34a5-412">Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="c34a5-413">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-414">Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **Estratto**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="c34a5-415">Per modificare l'oggetto Criteri di stato offline e configurare la durata del blocco dell'account</span><span class="sxs-lookup"><span data-stu-id="c34a5-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="c34a5-416">Nella scheda **controllo** , fare clic con il pulsante destro del mouse su **MioaltroGPO**e quindi scegliere **modifica** per aprire la finestra dell' **Editor gestione criteri di gruppo** e modificare una copia offline dell'oggetto GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="c34a5-417">Per questo scenario, configurare la lunghezza minima della password:</span><span class="sxs-lookup"><span data-stu-id="c34a5-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="c34a5-418">In **Configurazione computer**fare doppio clic su **criteri**, **impostazioni di Windows**, **impostazioni di sicurezza**, criteri **account**e criteri di **blocco degli account**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="c34a5-419">Nel riquadro dei dettagli fare doppio clic sulla **durata del blocco dell'account**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="c34a5-420">Nella finestra Proprietà selezionare la casella di controllo **Definisci questa impostazione**, impostare la durata su **30** minuti e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="c34a5-421">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="c34a5-422">Selezionare MioaltroGPO nell'archivio e richiedere la distribuzione come per MioGPO nel [passaggio 2: modificare un oggetto Criteri](#bkmk-manage2)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c34a5-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="c34a5-423">Puoi confrontare MioaltroGPO con MioGPO o MyTemplate usando i report differenze.</span><span class="sxs-lookup"><span data-stu-id="c34a5-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="c34a5-424">Tutti gli account che includono il ruolo di revisore (amministratore della gestione avanzata Criteri di amministrazione \ [controllo completo \], approvatore, editor o revisore) possono generare report.</span><span class="sxs-lookup"><span data-stu-id="c34a5-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="c34a5-425">Per confrontare un oggetto Criteri di confronto a un altro GPO e a un modello</span><span class="sxs-lookup"><span data-stu-id="c34a5-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="c34a5-426">Per confrontare MioGPO e MioaltroGPO:</span><span class="sxs-lookup"><span data-stu-id="c34a5-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="c34a5-427">Nella scheda **controllata** fare clic su **MioGPO**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="c34a5-428">Premere CTRL e quindi fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="c34a5-429">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e quindi fare clic su **report HTML**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="c34a5-430">Per confrontare MioaltroGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="c34a5-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="c34a5-431">Nella scheda **controllata** fare clic su **MioaltroGPO**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="c34a5-432">Fare clic con il pulsante destro del mouse su **MioaltroGPO**, scegliere **differenze**e quindi fare clic su **modello**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="c34a5-433">Selezionare **MyTemplate** e **report HTML**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="c34a5-434">Passaggio 5: eliminare e ripristinare un GPO</span><span class="sxs-lookup"><span data-stu-id="c34a5-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="c34a5-435">In questo passaggio si funge da approvatore per eliminare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="c34a5-436">Per eliminare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="c34a5-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="c34a5-437">In un computer in cui è stato installato il client Advanced Group Policy Management, accedere con un account utente a cui è assegnato il ruolo di responsabile approvazione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="c34a5-438">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="c34a5-439">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="c34a5-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="c34a5-440">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="c34a5-441">Fare clic su **Elimina GPO da archiviazione e produzione** per eliminare sia la versione nell'archivio che la versione distribuita del GPO nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="c34a5-442">Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="c34a5-443">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-444">Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto.</span><span class="sxs-lookup"><span data-stu-id="c34a5-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="c34a5-445">Occasionalmente potresti scoprire dopo l'eliminazione di un GPO che è ancora necessario.</span><span class="sxs-lookup"><span data-stu-id="c34a5-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="c34a5-446">In questo passaggio si funge da approvatore per ripristinare un oggetto Criteri di stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="c34a5-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="c34a5-447">Per ripristinare un oggetto Criteri di stato eliminato</span><span class="sxs-lookup"><span data-stu-id="c34a5-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="c34a5-448">Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare i GPO eliminati.</span><span class="sxs-lookup"><span data-stu-id="c34a5-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="c34a5-449">Fare clic con il pulsante destro del mouse su **MioGPO**e quindi scegliere **Ripristina**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="c34a5-450">Digitare un commento da visualizzare nella cronologia del GPO e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="c34a5-451">Quando la finestra **stato Advanced Group Policy Management** indica che lo stato di avanzamento complessivo è completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-452">L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .</span><span class="sxs-lookup"><span data-stu-id="c34a5-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="c34a5-453">**Nota**  Il ripristino di un GPO nell'archivio non viene automaticamente ridistribuito nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="c34a5-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="c34a5-454">Per restituire il GPO all'ambiente di produzione, distribuire il GPO come nel [passaggio 3: rivedere e distribuire un oggetto Criteri di controllo](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="c34a5-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="c34a5-455">Dopo la modifica e la distribuzione di un oggetto Criteri di ricerca, potresti scoprire che le recenti modifiche apportate al GPO causano un problema.</span><span class="sxs-lookup"><span data-stu-id="c34a5-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="c34a5-456">In questo passaggio si funge da approvatore per eseguire il rollback a una versione precedente dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="c34a5-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="c34a5-457">È possibile eseguire il rollback a qualsiasi versione nella cronologia del GPO.</span><span class="sxs-lookup"><span data-stu-id="c34a5-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="c34a5-458">È possibile usare i commenti e le etichette per identificare le versioni valide note e quando sono state apportate modifiche specifiche.</span><span class="sxs-lookup"><span data-stu-id="c34a5-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="c34a5-459">Per eseguire il rollback a una versione precedente di un oggetto Criteri di controllo</span><span class="sxs-lookup"><span data-stu-id="c34a5-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="c34a5-460">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="c34a5-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="c34a5-461">Fare doppio clic su **MioGPO** per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="c34a5-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="c34a5-462">Fare clic con il pulsante destro del mouse sulla versione da distribuire, scegliere **Distribuisci**e quindi fare clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="c34a5-463">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c34a5-464">Nella finestra **cronologia** fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="c34a5-465">**Nota**  Per verificare che la versione ridistribuita sia la versione progettata, esaminare un report di differenza per le due versioni.</span><span class="sxs-lookup"><span data-stu-id="c34a5-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="c34a5-466">Nella finestra **cronologia** del GPO selezionare le due versioni, fare clic con il pulsante destro del mouse su di esse, scegliere **differenza**e quindi fare clic su **report HTML** o **report XML**.</span><span class="sxs-lookup"><span data-stu-id="c34a5-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





