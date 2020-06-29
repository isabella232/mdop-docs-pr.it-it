---
title: Come configurare i report di MBAM 2.5
description: Come configurare i report di MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826616"
---
# <span data-ttu-id="644df-103">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="644df-104">In questo argomento viene illustrato come configurare la funzionalità di report di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 tramite:</span><span class="sxs-lookup"><span data-stu-id="644df-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="644df-105">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="644df-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="644df-106">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="644df-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="644df-107">Le istruzioni si basano sull'architettura consigliata nell' [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="644df-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="644df-108">Prima di iniziare la configurazione:</span><span class="sxs-lookup"><span data-stu-id="644df-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="644df-109">Passaggio</span><span class="sxs-lookup"><span data-stu-id="644df-109">Step</span></span></th>
<th align="left"><span data-ttu-id="644df-110">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="644df-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="644df-111">Esaminare l'architettura consigliata per MBAM.</span><span class="sxs-lookup"><span data-stu-id="644df-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="644df-112">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="644df-113">Esaminare le configurazioni supportate per MBAM.</span><span class="sxs-lookup"><span data-stu-id="644df-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="644df-114">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="644df-115">Completare i prerequisiti necessari per ogni server.</span><span class="sxs-lookup"><span data-stu-id="644df-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="644df-116">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="644df-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="644df-117">Prerequisiti di MBAM 2,5 server che si applicano solo alla topologia di integrazione di Configuration Manager </a> (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="644df-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="644df-118">Installare il software MBAM server su ogni server in cui si prevede di configurare una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="644df-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="644df-119">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="644df-120">Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet di Windows PowerShell per configurare le caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="644df-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="644df-121">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="644df-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="644df-122">Per configurare i report tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="644df-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="644df-123">Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="644df-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="644df-124">Usare il cmdlet **Enable-MbamReport** di Windows PowerShell per configurare i report.</span><span class="sxs-lookup"><span data-stu-id="644df-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="644df-125">Per ottenere informazioni su questo cmdlet di Windows PowerShell, digitare **Get-Help Enable-MbamReport**.</span><span class="sxs-lookup"><span data-stu-id="644df-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="644df-126">Per configurare i report tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="644df-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="644df-127">Nel server in cui si vogliono configurare i report avviare la configurazione guidata del **Server mbam** .</span><span class="sxs-lookup"><span data-stu-id="644df-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="644df-128">È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="644df-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="644df-129">Fare clic su **Aggiungi nuove funzionalità**, selezionare **report**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="644df-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="644df-130">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per i report.</span><span class="sxs-lookup"><span data-stu-id="644df-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="644df-131">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="644df-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="644df-132">Usando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:</span><span class="sxs-lookup"><span data-stu-id="644df-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="644df-133">Campo</span><span class="sxs-lookup"><span data-stu-id="644df-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="644df-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="644df-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="644df-135">Istanza di SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="644df-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-136">Istanza di SQL Server Reporting Services in cui verranno configurati i report.</span><span class="sxs-lookup"><span data-stu-id="644df-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="644df-137">Gruppo di Domain Role Reporting</span><span class="sxs-lookup"><span data-stu-id="644df-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-138">Nome del gruppo Domain Users i cui membri hanno diritti di accesso ai report nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="644df-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="644df-139">Nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="644df-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-140">Nome del server in cui è configurato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="644df-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="644df-141">Istanza di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="644df-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-142">Nome dell'istanza di SQL Server, ad esempio MSSQLSERVER, <em> in </em> cui è configurato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="644df-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="644df-143">Nota</span><span class="sxs-lookup"><span data-stu-id="644df-143">Note</span></span></strong><br/><p><span data-ttu-id="644df-144">È necessario aggiungere un'eccezione nel computer report per abilitare il traffico in ingresso sulla porta del server di report (la porta predefinita è 80).</span><span class="sxs-lookup"><span data-stu-id="644df-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="644df-145">Nome database</span><span class="sxs-lookup"><span data-stu-id="644df-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-146">Nome del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="644df-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="644df-147">Per impostazione predefinita, il nome del database è <strong> lo stato di conformità di mbam </strong> , anche se è possibile modificare il nome quando si configura il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="644df-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="644df-148">Nota</span><span class="sxs-lookup"><span data-stu-id="644df-148">Note</span></span></strong><br/><p><span data-ttu-id="644df-149">Se si esegue l'aggiornamento da una versione precedente di MBAM, è necessario usare lo stesso nome del database del nome usato nella distribuzione precedente.</span><span class="sxs-lookup"><span data-stu-id="644df-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="644df-150">Account di dominio del database di conformità e audit</span><span class="sxs-lookup"><span data-stu-id="644df-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="644df-151">Account utente e password di dominio per accedere al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="644df-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="644df-152">Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un utente, è necessario immettere lo stesso valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="644df-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="644df-153">Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un gruppo, il valore immesso in questo campo deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="644df-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="644df-154">Configurare la password per l'account per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="644df-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="644df-155">L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="644df-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="644df-156">Dopo aver completato le voci, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="644df-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="644df-157">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="644df-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="644df-158">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="644df-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="644df-159">Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.</span><span class="sxs-lookup"><span data-stu-id="644df-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="644df-160">Nota</span><span class="sxs-lookup"><span data-stu-id="644df-160">Note</span></span>**  
   <span data-ttu-id="644df-161">Per creare uno script di Windows PowerShell delle voci appena effettuate, fare clic su **Esporta script di PowerShell**e quindi salvare lo script.</span><span class="sxs-lookup"><span data-stu-id="644df-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="644df-162">Fare clic su **Aggiungi** per aggiungere i report nel server e quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="644df-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="644df-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="644df-163">Related topics</span></span>


[<span data-ttu-id="644df-164">Registri eventi del server</span><span class="sxs-lookup"><span data-stu-id="644df-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="644df-165">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="644df-166">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="644df-167">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="644df-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="644df-168">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="644df-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="644df-169">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="644df-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="644df-170">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="644df-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






