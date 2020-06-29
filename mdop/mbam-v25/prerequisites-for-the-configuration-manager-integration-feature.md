---
title: Prerequisiti per la funzionalità di integrazione di Configuration Manager
description: Prerequisiti per la funzionalità di integrazione di Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825015"
---
# <span data-ttu-id="57380-103">Prerequisiti per la funzionalità di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="57380-104">Se si distribuisce MBAM con la topologia di integrazione di System Center Configuration Manager, è consigliabile un'architettura a tre server, come descritto in [architettura di alto livello di mbam 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="57380-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="57380-105">Questa architettura può supportare i computer client di 500.000.</span><span class="sxs-lookup"><span data-stu-id="57380-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="57380-106">Importante</span><span class="sxs-lookup"><span data-stu-id="57380-106">Important</span></span>**  
<span data-ttu-id="57380-107">Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="57380-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="57380-108">Prerequisiti generali per la funzionalità di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="57380-109">Quando si installa MBAM con Configuration Manager, sono necessari i prerequisiti aggiuntivi seguenti, oltre ai prerequisiti per la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="57380-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57380-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="57380-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="57380-111">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="57380-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-112">Il Server Configuration Manager è un sito principale nel sistema di gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="57380-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-113">N/D</span><span class="sxs-lookup"><span data-stu-id="57380-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57380-114">L'agente client Inventory hardware si trova nel server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="57380-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-115">Per System Center 2012 Configuration Manager, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> come configurare l'inventario hardware in Gestione configurazione </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="57380-116">Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> come configurare l'inventario hardware per un sito </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-117">Una delle opzioni seguenti è abilitata, a seconda della versione di Configuration Manager in uso:</span><span class="sxs-lookup"><span data-stu-id="57380-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="57380-118">Impostazioni di conformità-(System Center 2012 Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="57380-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="57380-119">Agente client di gestione della configurazione (DCM) desiderato-(Configuration Manager 2007)</span><span class="sxs-lookup"><span data-stu-id="57380-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="57380-120">Per Gestione configurazione di System Center 2012, vedere configurazione <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> delle impostazioni di conformità in Gestione configurazione </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="57380-121">Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> proprietà dell'agente client di gestione della configurazione desiderata </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57380-122">Un punto di Reporting Services è definito in Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="57380-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="57380-123">Obbligatorio per SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="57380-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-124">Per Gestione configurazione di System Center 2012, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> prerequisiti per la creazione di report in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="57380-125">Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> come creare un punto di Reporting Services per SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="57380-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-126">Configuration Manager 2007 richiede Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="57380-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-127">L'agente client di gestione della configurazione (DCM) desiderato in Configuration Manager 2007 richiede .NET Framework 2,0 per segnalare la conformità.</span><span class="sxs-lookup"><span data-stu-id="57380-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="57380-128">Nota</span><span class="sxs-lookup"><span data-stu-id="57380-128">Note</span></span></strong><br/><p><span data-ttu-id="57380-129">L'installazione di .NET Framework 3,5 viene installata automaticamente in .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="57380-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="57380-130">Autorizzazioni necessarie per installare MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="57380-131">Per installare MBAM con Configuration Manager, è necessario disporre di un utente amministrativo in Configuration Manager che disponga di un ruolo di sicurezza con le autorizzazioni minime elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="57380-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="57380-132">La tabella mostra anche i diritti che è necessario avere, oltre ai diritti di amministratore di Basic computer, per installare il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="57380-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="57380-133">Le autorizzazioni nella tabella seguente sono valide per entrambe le versioni di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="57380-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57380-134">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="57380-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="57380-135">Funzionalità del server MBAM</span><span class="sxs-lookup"><span data-stu-id="57380-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-136">Ruoli del server di accesso istanza di SQL Server:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="57380-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="57380-137">Database di ripristino-database di controllo</span><span class="sxs-lookup"><span data-stu-id="57380-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57380-138">Diritti istanza SSRS:-creare cartelle-pubblicare report</span><span class="sxs-lookup"><span data-stu-id="57380-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="57380-139">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="57380-140">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57380-141">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="57380-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="57380-142">Funzionalità del Server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-143">Diritti del sito di Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="57380-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-144">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57380-145">Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-modifica-Distribuisci elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="57380-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-146">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-147">Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi</span><span class="sxs-lookup"><span data-stu-id="57380-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-148">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="57380-149">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="57380-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57380-150">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="57380-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="57380-151">Funzionalità del Server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-152">Diritti del sito di Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="57380-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-153">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57380-154">Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-ReadResource</span><span class="sxs-lookup"><span data-stu-id="57380-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-155">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57380-156">Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi-Distribuisci</span><span class="sxs-lookup"><span data-stu-id="57380-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="57380-157">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="57380-158">Modifiche obbligatorie per i file MOF</span><span class="sxs-lookup"><span data-stu-id="57380-158">Required changes for the .mof files</span></span>


<span data-ttu-id="57380-159">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof e il file SMS \ _def. mof per System Center 2012 Configuration Manager e Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="57380-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="57380-160">Per istruzioni, Vedi [i prerequisiti del server MBAM 2,5 che si applicano solo alla topologia di integrazione di Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="57380-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="57380-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57380-161">Related topics</span></span>


[<span data-ttu-id="57380-162">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="57380-163">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="57380-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="57380-164">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="57380-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="57380-165">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="57380-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="57380-166">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="57380-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





