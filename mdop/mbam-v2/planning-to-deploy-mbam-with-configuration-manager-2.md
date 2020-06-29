---
title: Pianificazione della distribuzione di MBAM con Configuration Manager
description: Pianificazione della distribuzione di MBAM con Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825626"
---
# <span data-ttu-id="a7670-103">Pianificazione della distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="a7670-104">Per distribuire MBAM con la topologia di Configuration Manager, è consigliata un'architettura a tre server, che supporta i client di 200.000.</span><span class="sxs-lookup"><span data-stu-id="a7670-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="a7670-105">Usare un server separato per eseguire Configuration Manager e installare le funzionalità di amministrazione e monitoraggio di base su due server, come illustrato nell'immagine dell'architettura in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a7670-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="a7670-106">Importante</span><span class="sxs-lookup"><span data-stu-id="a7670-106">Important</span></span>**  
<span data-ttu-id="a7670-107">Windows to go non è supportato quando si installa la topologia integrata di MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="a7670-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="a7670-108">Prerequisiti di distribuzione per l'installazione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="a7670-109">Verificare di avere soddisfatto i prerequisiti seguenti prima di installare MBAM con Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="a7670-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a7670-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a7670-111">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="a7670-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-112">Verificare che il Server Configuration Manager sia un sito principale nel sistema di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-113">N/D</span><span class="sxs-lookup"><span data-stu-id="a7670-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-114">Abilitare l'agente client Inventory hardware nel server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-115">Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> come configurare l'inventario hardware per un sito </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="a7670-116">Per System Center 2012 Configuration Manager, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> come configurare l'inventario hardware in Gestione configurazione </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-117">Abilitare l'agente di gestione della configurazione (DCM) o le impostazioni di conformità, a seconda della versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="a7670-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-118">Per Configuration Manager 2007, abilitare la visualizzazione delle <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> proprietà dell'agente client di gestione della configurazione desiderata </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="a7670-119">Per Gestione configurazione di System Center 2012, vedere configurazione <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> delle impostazioni di conformità in Gestione configurazione </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-120">Definire un punto di Reporting Services in Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="a7670-121">Obbligatorio per SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a7670-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-122">Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> come creare un punto di Reporting Services per SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="a7670-123">Per Gestione configurazione di System Center 2012, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> prerequisiti per la creazione di report in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="a7670-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="a7670-124">Versioni supportate di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="a7670-125">MBAM supporta le versioni seguenti di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="a7670-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-126">Versione supportata</span><span class="sxs-lookup"><span data-stu-id="a7670-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="a7670-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a7670-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a7670-128">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="a7670-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="a7670-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-130">SP1 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a7670-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-131">64 bit</span><span class="sxs-lookup"><span data-stu-id="a7670-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a7670-132">Nota</span><span class="sxs-lookup"><span data-stu-id="a7670-132">Note</span></span></strong><br/><p><span data-ttu-id="a7670-133">Anche se Configuration Manager 2007 è 32 bit, è necessario installarlo e SQL Server in un sistema operativo a 64 bit per far corrispondere il software MBAM a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a7670-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-134">Gestione configurazione di Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="a7670-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-135">SP1</span><span class="sxs-lookup"><span data-stu-id="a7670-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-136">64 bit</span><span class="sxs-lookup"><span data-stu-id="a7670-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a7670-137">Per un elenco delle configurazioni supportate per il Server Configuration Manager, vedere la pagina Web appropriata per la versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="a7670-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="a7670-138">MBAM non ha requisiti di sistema aggiuntivi per il Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="a7670-139">Requisiti di sistema MBAM e SQL Server</span><span class="sxs-lookup"><span data-stu-id="a7670-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="a7670-140">Le configurazioni e i requisiti di sistema supportati per i server MBAM e SQL Server per la topologia di Configuration Manager corrispondono a quelli per la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="a7670-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="a7670-141">Per i requisiti di sistema autonomi, Vedi le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a7670-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="a7670-142">Per gli uffici MBAM server e SQL Server Processor, RAM e spazio su disco per la topologia di Configuration Manager, vedere le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7670-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="a7670-143">MBAM Server Processor, RAM e spazio su disco requisiti per MBAM</span><span class="sxs-lookup"><span data-stu-id="a7670-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="a7670-144">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco per i server MBAM quando si usa la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-145">Componente hardware</span><span class="sxs-lookup"><span data-stu-id="a7670-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="a7670-146">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="a7670-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="a7670-147">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="a7670-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-148">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="a7670-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-149">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="a7670-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-150">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="a7670-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-151">RAM</span><span class="sxs-lookup"><span data-stu-id="a7670-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-152">4 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-153">8 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-154">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="a7670-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-155">1 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-156">2 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a7670-157">Requisiti per processori, RAM e spazio su disco per SQL Server</span><span class="sxs-lookup"><span data-stu-id="a7670-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="a7670-158">Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco del server per il computer SQL Server quando si usa la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-159">Componente hardware</span><span class="sxs-lookup"><span data-stu-id="a7670-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="a7670-160">Requisito minimo</span><span class="sxs-lookup"><span data-stu-id="a7670-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="a7670-161">Requisito consigliato</span><span class="sxs-lookup"><span data-stu-id="a7670-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-162">Responsabile del trattamento</span><span class="sxs-lookup"><span data-stu-id="a7670-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-163">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="a7670-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-164">2,33 GHz o superiore</span><span class="sxs-lookup"><span data-stu-id="a7670-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-165">RAM</span><span class="sxs-lookup"><span data-stu-id="a7670-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-166">4 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-167">8 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-168">Spazio disponibile su disco</span><span class="sxs-lookup"><span data-stu-id="a7670-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-169">5 GB</span><span class="sxs-lookup"><span data-stu-id="a7670-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-170">5 GB o superiore</span><span class="sxs-lookup"><span data-stu-id="a7670-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a7670-171">Autorizzazioni necessarie per installare il server MBAM</span><span class="sxs-lookup"><span data-stu-id="a7670-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="a7670-172">Per installare MBAM con Configuration Manager, è necessario disporre di un utente amministrativo in Configuration Manager che disponga di un ruolo di sicurezza con le autorizzazioni minime elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a7670-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="a7670-173">La tabella mostra anche i diritti che è necessario avere, oltre ai diritti di amministratore di Basic computer, per installare il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7670-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-174">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="a7670-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="a7670-175">Funzionalità del server MBAM</span><span class="sxs-lookup"><span data-stu-id="a7670-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-176">Ruoli del server di accesso alle istanze SQL:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="a7670-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="a7670-177">Database di ripristino-database di controllo</span><span class="sxs-lookup"><span data-stu-id="a7670-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-178">Diritti di istanza di SQL Server Reporting Services:-creare cartelle-pubblicare report</span><span class="sxs-lookup"><span data-stu-id="a7670-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="a7670-179">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a7670-180">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-181">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="a7670-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="a7670-182">Funzionalità del Server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-183">Diritti del sito di Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="a7670-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-184">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-185">Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-modifica-Distribuisci elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="a7670-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-186">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-187">Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi</span><span class="sxs-lookup"><span data-stu-id="a7670-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-188">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a7670-189">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="a7670-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7670-190">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="a7670-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="a7670-191">Funzionalità del Server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-192">Diritti del sito di Configuration Manager:-Read</span><span class="sxs-lookup"><span data-stu-id="a7670-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-193">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7670-194">Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-ReadResource</span><span class="sxs-lookup"><span data-stu-id="a7670-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-195">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7670-196">Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi-Distribuisci</span><span class="sxs-lookup"><span data-stu-id="a7670-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-197">Integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a7670-198">Ordine di distribuzione delle funzionalità di MBAM per la topologia di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="a7670-199">Quando si distribuisce MBAM nel server Configuration Manager, è necessario completare le attività di distribuzione nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="a7670-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="a7670-200">Modificare il file Configuration. mof nel server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="a7670-201">Creare o modificare il server di gestione configurazione file SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="a7670-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="a7670-202">Installare MBAM nel server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="a7670-203">Installare il database di ripristino e il database di controllo nel server di database.</span><span class="sxs-lookup"><span data-stu-id="a7670-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="a7670-204">Installare le funzionalità di MBAM nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a7670-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="a7670-205">Elenco di controllo pianificazione per l'installazione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="a7670-206">Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da considerare quando si pianifica una distribuzione di amministrazione e monitoraggio di Microsoft BitLocker con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a7670-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="a7670-207">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="a7670-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="a7670-208">Attività</span><span class="sxs-lookup"><span data-stu-id="a7670-208">Task</span></span></th>
<th align="left"><span data-ttu-id="a7670-209">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="a7670-209">References</span></span></th>
<th align="left"><span data-ttu-id="a7670-210">Note</span><span class="sxs-lookup"><span data-stu-id="a7670-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a7670-211">Esaminare le informazioni introduttive, che illustrano la modalità di funzionamento di Configuration Manager con MBAM e l'architettura di alto livello consigliata.</span><span class="sxs-lookup"><span data-stu-id="a7670-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="a7670-212">Attività iniziali: uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a7670-213">Esaminare le informazioni di pianificazione, che descrivono i prerequisiti di distribuzione, le configurazioni supportate, le autorizzazioni necessarie e l'ordine di distribuzione per ogni caratteristica.</span><span class="sxs-lookup"><span data-stu-id="a7670-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7670-214">Pianificazione della distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a7670-215">Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7670-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="a7670-216">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a7670-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a7670-217">Pianificare e creare gruppi di sicurezza di servizi di dominio Active Directory necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7670-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="a7670-218">Pianificazione dei ruoli di amministrazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a7670-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a7670-219">Pianificare la distribuzione di MBAM Client Deployment.</span><span class="sxs-lookup"><span data-stu-id="a7670-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="a7670-220">Pianificazione della distribuzione del client di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a7670-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a7670-221">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7670-221">Related topics</span></span>


[<span data-ttu-id="a7670-222">Uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a7670-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









