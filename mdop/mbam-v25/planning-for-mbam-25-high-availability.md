---
title: Pianificazione della disponibilità elevata per MBAM 2.5
description: Pianificazione della disponibilità elevata per MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826945"
---
# <span data-ttu-id="a4d13-103">Pianificazione della disponibilità elevata per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a4d13-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="a4d13-104">Microsoft BitLocker Administration and Monitoring (MBAM) può mantenere elevata la disponibilità con l'uso di una o più delle tecnologie seguenti, descritte nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4d13-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="a4d13-105">Gruppi di disponibilità di SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a4d13-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="a4d13-106">Clustering di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4d13-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="a4d13-107">Bilanciamento del carico di rete IIS</span><span class="sxs-lookup"><span data-stu-id="a4d13-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="a4d13-108">Mirroring del database in SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4d13-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="a4d13-109">Backup dei database di MBAM tramite il servizio Copia Shadow del volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="a4d13-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="a4d13-110">Usare le informazioni nelle sezioni seguenti per comprendere le opzioni per la distribuzione di MBAM in una configurazione a disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="a4d13-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="a4d13-111">Supporto per i gruppi di disponibilità di SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a4d13-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="a4d13-112">MBAM consente di configurare e gestire i gruppi di disponibilità per i database in Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4d13-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="a4d13-113">Un gruppo di disponibilità per MBAM supporta un ambiente di failover in cui il database di conformità e controllo e il database di ripristino non vengono più Uniti, invece che separatamente.</span><span class="sxs-lookup"><span data-stu-id="a4d13-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="a4d13-114">Un gruppo di disponibilità supporta un set di database primari di lettura/scrittura e uno-quattro set di database secondari corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a4d13-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="a4d13-115">Facoltativamente, i database secondari possono essere resi disponibili per le autorizzazioni di sola lettura, alcune operazioni di backup o per entrambi.</span><span class="sxs-lookup"><span data-stu-id="a4d13-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="a4d13-116">Per informazioni su come configurare i gruppi di disponibilità, vedere [gruppi di disponibilità AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="a4d13-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="a4d13-117">Clustering di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4d13-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="a4d13-118">È possibile eseguire il database di conformità e controllo di MBAM 2,5 e il database di ripristino nei computer che eseguono cluster di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4d13-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="a4d13-119">Bilanciamento del carico di rete IIS</span><span class="sxs-lookup"><span data-stu-id="a4d13-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="a4d13-120">È possibile usare il bilanciamento del carico di rete per configurare un ambiente altamente disponibile per i computer che eseguono il sito Web di amministrazione e monitoraggio (noto anche come Help desk), il portale self-service e i servizi Web distribuiti tramite Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="a4d13-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="a4d13-121">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a4d13-121">Prerequisites</span></span>

<span data-ttu-id="a4d13-122">Prima di configurare il bilanciamento del carico, verificare di avere soddisfatto i prerequisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4d13-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="a4d13-123">Un bilanciamento del carico deve essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d13-123">A load balancer must be available.</span></span> <span data-ttu-id="a4d13-124">È possibile usare il bilanciamento del carico da Microsoft o da un'altra società.</span><span class="sxs-lookup"><span data-stu-id="a4d13-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="a4d13-125">Per altre informazioni sulla tecnologia di bilanciamento del carico Microsoft, vedere [creare una Web farm con i server IIS](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="a4d13-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="a4d13-126">Almeno due server stanno usando IIS e hanno soddisfatto tutti i prerequisiti di MBAM per supportare le caratteristiche Web, tra cui ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="a4d13-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="a4d13-127">I database e i report MBAM sono in uso in un server.</span><span class="sxs-lookup"><span data-stu-id="a4d13-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="a4d13-128">Modifiche specifiche per MBAM necessarie per abilitare il bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a4d13-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="a4d13-129">Completare le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4d13-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="a4d13-130">Registrare un nome dell'entità servizio (SPN) per il nome host virtuale nell'account di dominio in uso per i pool di applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="a4d13-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="a4d13-131">Ad esempio, se il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\\mbamapppooluser, il comando seguente registra l'SPN in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a4d13-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="a4d13-132">Configurare le caratteristiche Web di MBAM seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4d13-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="a4d13-133">In ogni server che ospiterà le caratteristiche Web di MBAM, USA lo stesso account di dominio per le credenziali amministrative del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a4d13-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="a4d13-134">Specificare un nome host che corrisponda al nome host virtuale (nome DNS) del cluster di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a4d13-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="a4d13-135">Ad esempio, quando si installa MBAM in un server denominato "NLB1" con un nome host virtuale di **mbamvirtual.contoso.com**, assicurarsi che il nome host specificato nel cmdlet di Windows PowerShell sia **mbamvirtual.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="a4d13-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="a4d13-136">Se si configurano i siti Web in una Web farm con un dispositivo di bilanciamento del carico, è necessario configurare i siti Web in modo da usare la stessa chiave del computer.</span><span class="sxs-lookup"><span data-stu-id="a4d13-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="a4d13-137">Per altre informazioni, vedere le sezioni seguenti in [elemento machineKey (schema delle impostazioni di ASP.NET)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span><span class="sxs-lookup"><span data-stu-id="a4d13-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="a4d13-138">Spiegazione della chiave del computer</span><span class="sxs-lookup"><span data-stu-id="a4d13-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="a4d13-139">Considerazioni sulla distribuzione di Web farm</span><span class="sxs-lookup"><span data-stu-id="a4d13-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="a4d13-140">Per istruzioni su come generare automaticamente una chiave, vedere [generare una chiave del computer (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4d13-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="a4d13-141">Le informazioni sul bilanciamento del carico si applicano anche ai cluster di bilanciamento del carico di rete di IIS (NLB) in Windows Server 2012 o Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="a4d13-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="a4d13-142">La funzionalità di bilanciamento del carico di rete di IIS in Windows Server 2012 è in genere uguale a quella di Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="a4d13-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="a4d13-143">Tuttavia, alcuni dettagli delle attività sono diversi in Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a4d13-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="a4d13-144">Per informazioni sulle nuove modalità di attività, vedere [attività di gestione comuni e spostamento in Windows server 2012 R2 Preview e Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="a4d13-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="a4d13-145">Mirroring del database in SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4d13-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="a4d13-146">MBAM supporta l'uso di mirroring di SQL Server, in cui il database di conformità e controllo e il database di ripristino vengono speculati utilizzando due istanze di SQL Server per ogni database.</span><span class="sxs-lookup"><span data-stu-id="a4d13-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="a4d13-147">Prima di implementare il mirroring, tenere presente che il mirroring viene gradualmente eliminato, a favore dei gruppi di disponibilità, descritti più indietro in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a4d13-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="a4d13-148">Per implementare il mirroring per MBAM, devi specificare le stringhe di connessione appropriate per la configurazione del database con mirroring usando il cmdlet di Windows PowerShell **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="a4d13-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="a4d13-149">Per altre informazioni sui cmdlet di Windows PowerShell per MBAM 2,5, vedere [configurazione delle funzionalità del server di mbam 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a4d13-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="a4d13-150">Esempi di implementazione del mirroring di SQL Server tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4d13-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="a4d13-151">Gli esempi seguenti illustrano come implementare il mirroring di SQL Server usando i cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4d13-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="a4d13-152">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4d13-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="a4d13-153">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a4d13-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="a4d13-154">Altre informazioni sul mirroring di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4d13-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="a4d13-155">I collegamenti seguenti includono ulteriori informazioni sulla configurazione del mirroring di SQL Server:</span><span class="sxs-lookup"><span data-stu-id="a4d13-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="a4d13-156">Procedura: preparare un database mirror per il mirroring (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="a4d13-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="a4d13-157">Stabilire una sessione di mirroring del database con l'autenticazione di Windows (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="a4d13-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="a4d13-158">Backup dei database di MBAM tramite il servizio Copia Shadow del volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="a4d13-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="a4d13-159">MBAM offre un writer del servizio Copia Shadow del volume (VSS), denominato Microsoft BitLocker Administration and Management writer.</span><span class="sxs-lookup"><span data-stu-id="a4d13-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="a4d13-160">Questo writer VSS semplifica il backup del database di conformità e di controllo e del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a4d13-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="a4d13-161">Il writer VSS è registrato in tutti i server in cui si Abilita un'applicazione Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="a4d13-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="a4d13-162">MBAM VSS Writer dipende da SQL Server VSS Writer, registrato come parte dell'installazione di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4d13-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="a4d13-163">Qualsiasi tecnologia di backup che usa writer VSS per eseguire il backup può individuare il writer di MBAM VSS.</span><span class="sxs-lookup"><span data-stu-id="a4d13-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="a4d13-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4d13-164">Related topics</span></span>


[<span data-ttu-id="a4d13-165">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a4d13-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="a4d13-166">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="a4d13-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a4d13-167">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a4d13-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="a4d13-168">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a4d13-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




