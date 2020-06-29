---
title: Come configurare i database di MBAM 2.5
description: Come configurare i database di MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826625"
---
# <span data-ttu-id="a5bcf-103">Come configurare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="a5bcf-104">Questo argomento spiega come configurare il database di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 per la conformità e l'audit e il database di ripristino tramite:</span><span class="sxs-lookup"><span data-stu-id="a5bcf-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="a5bcf-105">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5bcf-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="a5bcf-106">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="a5bcf-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="a5bcf-107">Le istruzioni si basano sull'architettura consigliata nell' [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="a5bcf-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="a5bcf-108">Prima di iniziare la configurazione:</span><span class="sxs-lookup"><span data-stu-id="a5bcf-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5bcf-109">Passaggio</span><span class="sxs-lookup"><span data-stu-id="a5bcf-109">Step</span></span></th>
<th align="left"><span data-ttu-id="a5bcf-110">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="a5bcf-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5bcf-111">Esaminare l'architettura consigliata per MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="a5bcf-112">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5bcf-113">Esaminare le configurazioni supportate per MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="a5bcf-114">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5bcf-115">Completare i prerequisiti necessari per ogni server.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="a5bcf-116">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a5bcf-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="a5bcf-117">Prerequisiti di MBAM 2,5 server che si applicano solo alla topologia di integrazione di Configuration Manager </a> (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5bcf-118">Installare il software MBAM server su ogni server in cui si prevede di configurare una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a5bcf-119">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-119">Note</span></span></strong><br/><p><span data-ttu-id="a5bcf-120">È possibile installare i database in un computer SQL Server remoto tramite Windows PowerShell o un pacchetto di applicazione a livello di dati esportato (DAC).</span><span class="sxs-lookup"><span data-stu-id="a5bcf-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="a5bcf-121">Per altre informazioni sui pacchetti DAC, vedere <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applicazioni a livello di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="a5bcf-122">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5bcf-123">Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet di Windows PowerShell per configurare le caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="a5bcf-124">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5bcf-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a5bcf-125">Per configurare i database tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5bcf-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="a5bcf-126">Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="a5bcf-127">Usare il cmdlet **Enable-MbamDatabase** di Windows PowerShell per configurare i database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="a5bcf-128">Per ottenere informazioni su questo cmdlet di Windows PowerShell, digitare **Get-Help Enable-MbamDatabase**.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="a5bcf-129">Per configurare il database di conformità e controllo tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="a5bcf-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="a5bcf-130">Nel server in cui si vogliono configurare i database avviare la configurazione guidata del **Server mbam** .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="a5bcf-131">È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="a5bcf-132">Fare clic su **Aggiungi nuove funzionalità**, selezionare database di **conformità e controllo** e database di **ripristino**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="a5bcf-133">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per i database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="a5bcf-134">Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="a5bcf-135">In caso contrario, risolvere i prerequisiti mancanti e quindi fare di **nuovo clic su Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="a5bcf-136">Usando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:</span><span class="sxs-lookup"><span data-stu-id="a5bcf-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a5bcf-137">Campo</span><span class="sxs-lookup"><span data-stu-id="a5bcf-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="a5bcf-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5bcf-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-139">Nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a5bcf-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-140">Nome del server in cui si sta configurando il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a5bcf-141">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-141">Note</span></span></strong><br/><p><span data-ttu-id="a5bcf-142">Per abilitare il traffico in ingresso nella porta di Microsoft SQL Server, è necessario aggiungere un'eccezione nel computer di database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="a5bcf-143">Il numero di porta predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-144">Istanza di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a5bcf-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-145">Nome dell'istanza del database in cui verranno archiviati i dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="a5bcf-146">Devi anche specificare la posizione in cui verranno individuate le informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-147">Nome database</span><span class="sxs-lookup"><span data-stu-id="a5bcf-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-148">Nome del database in cui verranno archiviati i dati di conformità.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a5bcf-149">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-149">Note</span></span></strong><br/><p><span data-ttu-id="a5bcf-150">Se si esegue l'aggiornamento da una versione precedente di MBAM, è necessario usare lo stesso nome del database usato nella distribuzione precedente.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-151">Utente o gruppo di dominio di accesso in lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bcf-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-152">Utente o gruppo di dominio che ha l'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report in questo database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="a5bcf-153">Se si immette un utente in questo campo, deve essere lo stesso valore del <strong> campo account del pool di applicazioni Web Service nella </strong> <strong> pagina Configura applicazioni Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="a5bcf-154">Se si immette un gruppo in questo campo, il valore nel <strong> campo account di dominio del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> deve essere un membro del gruppo immesso in questo campo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-155">Utente o gruppo di dominio di Access di sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5bcf-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-156">Nome dell'utente o del gruppo che avrà l'autorizzazione di sola lettura per il database per consentire ai report di accedere ai dati di conformità in questo database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="a5bcf-157">Se si immette un utente in questo campo, deve essere lo stesso utente di quello specificato nel <strong> campo conformità e controllo del dominio del database </strong> nella <strong> pagina Configura report </strong> .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="a5bcf-158">Se si immette un gruppo in questo campo, il valore specificato nel <strong> campo account di dominio del database di conformità e controllo nella </strong> <strong> pagina Configura report </strong> deve essere un membro del gruppo specificato in questo campo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="a5bcf-159">Passare alla sezione successiva per configurare il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="a5bcf-160">Per configurare il database di ripristino tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="a5bcf-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="a5bcf-161">Usando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:</span><span class="sxs-lookup"><span data-stu-id="a5bcf-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a5bcf-162">Campo</span><span class="sxs-lookup"><span data-stu-id="a5bcf-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="a5bcf-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5bcf-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-164">Nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a5bcf-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-165">Nome del server in cui si sta configurando il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a5bcf-166">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-166">Note</span></span></strong><br/><p><span data-ttu-id="a5bcf-167">È necessario aggiungere un'eccezione nel computer del database di ripristino per abilitare il traffico in ingresso nella porta di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="a5bcf-168">Il numero di porta predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-169">Istanza di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a5bcf-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-170">Nome dell'istanza del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="a5bcf-171">Devi anche specificare la posizione in cui verranno individuate le informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-172">Nome database</span><span class="sxs-lookup"><span data-stu-id="a5bcf-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-173">Nome del database in cui verranno archiviati i dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a5bcf-174">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-174">Note</span></span></strong><br/><p><span data-ttu-id="a5bcf-175">Se si esegue l'aggiornamento da una versione precedente di MBAM, è necessario usare lo stesso nome del database usato nella distribuzione precedente.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a5bcf-176">Utente o gruppo di dominio di accesso in lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bcf-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a5bcf-177">Utente o gruppo di dominio che ha l'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report in questo database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="a5bcf-178">Se si immette un utente in questo campo, deve essere lo stesso valore del <strong> campo account del pool di applicazioni Web Service nella </strong> <strong> pagina Configura applicazioni Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="a5bcf-179">Se si immette un gruppo in questo campo, il valore nel <strong> campo account di dominio del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> deve essere un membro del gruppo immesso in questo campo.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a5bcf-180">Dopo aver completato le voci, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="a5bcf-181">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per i database.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="a5bcf-182">Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="a5bcf-183">In caso contrario, risolvere eventuali prerequisiti mancanti e quindi fare di nuovo clic su **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="a5bcf-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="a5bcf-184">Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="a5bcf-185">Nota</span><span class="sxs-lookup"><span data-stu-id="a5bcf-185">Note</span></span>**  
   <span data-ttu-id="a5bcf-186">Per creare uno script di Windows PowerShell delle voci appena effettuate, fare clic su **Esporta script di PowerShell**e quindi salvare lo script.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="a5bcf-187">Fare clic su **Aggiungi** per aggiungere i database MBAM nel server e quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="a5bcf-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5bcf-188">Related topics</span></span>


[<span data-ttu-id="a5bcf-189">Registri eventi del server</span><span class="sxs-lookup"><span data-stu-id="a5bcf-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="a5bcf-190">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="a5bcf-191">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="a5bcf-192">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="a5bcf-193">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="a5bcf-194">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="a5bcf-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a5bcf-195">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a5bcf-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="a5bcf-196">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a5bcf-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





