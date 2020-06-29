---
title: Pianificazione della disponibilità elevata con App-V 5.0
description: Pianificazione della disponibilità elevata con App-V 5.0
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805019"
---
# <span data-ttu-id="57455-103">Pianificazione della disponibilità elevata con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="57455-103">Planning for High Availability with App-V 5.0</span></span>


<span data-ttu-id="57455-104">Le configurazioni di sistema di Microsoft Application Virtualization 5,0 (App-V 5,0) possono sfruttare le opzioni che mantengono un livello elevato di servizio disponibile.</span><span class="sxs-lookup"><span data-stu-id="57455-104">Microsoft Application Virtualization 5.0 (App-V 5.0) system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="57455-105">Usare le informazioni nelle sezioni seguenti per comprendere le opzioni per la distribuzione di App-V 5,0 in una configurazione altamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="57455-105">Use the information in the following sections to help you understand the options to deploy App-V 5.0 in a highly available configuration.</span></span>

-   [<span data-ttu-id="57455-106">Supporto per il clustering di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="57455-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="57455-107">Supporto per il bilanciamento del carico di rete IIS</span><span class="sxs-lookup"><span data-stu-id="57455-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="57455-108">Supporto per i file server in cluster durante l'uso della modalità SCS</span><span class="sxs-lookup"><span data-stu-id="57455-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="57455-109">Supporto per il mirroring di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="57455-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="57455-110">Supporto per Microsoft SQL Server sempre attivo</span><span class="sxs-lookup"><span data-stu-id="57455-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="57455-111">Supporto per il clustering di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="57455-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="57455-112">È possibile eseguire il database di gestione e la creazione di report di App-V nei computer che eseguono cluster Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57455-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="57455-113">È tuttavia necessario installare i database usando gli script.</span><span class="sxs-lookup"><span data-stu-id="57455-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="57455-114">Per istruzioni, Vedi [come distribuire i database di App-V usando gli script SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="57455-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="57455-115">Supporto per il bilanciamento del carico di rete IIS</span><span class="sxs-lookup"><span data-stu-id="57455-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="57455-116">Puoi usare Internet Information Services (IIS) Network Load Balancing per configurare un ambiente altamente disponibile per i computer che eseguono App-V 5. x Management, Publishing e Reporting Services distribuiti tramite IIS.</span><span class="sxs-lookup"><span data-stu-id="57455-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="57455-117">Per altre informazioni sulla configurazione di IIS e del bilanciamento del carico di rete per i computer che eseguono sistemi operativi Windows Server, vedere la seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="57455-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="57455-118">Fornisce informazioni sulla configurazione di Internet Information Services (IIS) 7,0.</span><span class="sxs-lookup"><span data-stu-id="57455-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="57455-119">[Ottenere elevata disponibilità e scalabilità-ARR e NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="57455-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="57455-120">Configurazione di Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="57455-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="57455-121">[Bilanciamento del carico di rete](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="57455-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="57455-122">Queste informazioni si applicano anche ai cluster di bilanciamento del carico di rete di IIS (NLB) in Windows Server2008, Windows Server2008R2 o Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="57455-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="57455-123">**Nota**  La funzionalità di bilanciamento del carico di rete di IIS in Windows Server2012 è in genere uguale a quella di Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="57455-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="57455-124">Tuttavia, alcuni dettagli dell'attività vengono modificati in Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="57455-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="57455-125">Per informazioni sulle nuove modalità di attività, vedere [attività di gestione comuni e spostamento in Windows server 2012 R2 Preview e Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="57455-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="57455-126">Supporto per i file server in cluster durante l'uso della modalità SCS</span><span class="sxs-lookup"><span data-stu-id="57455-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="57455-127">È supportata la versione in uso di App-V 5,0 in modalità SCS (Share Content Store) con file server raggruppati.</span><span class="sxs-lookup"><span data-stu-id="57455-127">Running App-V 5.0 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="57455-128">Per abilitare questa configurazione, è possibile usare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="57455-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="57455-129">Configura App-V 5,0 per l'esecuzione in modalità SCS client.</span><span class="sxs-lookup"><span data-stu-id="57455-129">Configure App-V 5.0 to run in client SCS mode.</span></span> <span data-ttu-id="57455-130">Per altre informazioni sulla configurazione della modalità SCS App-V 5,0, vedere [come installare il client App-v 5,0 per la modalità di archiviazione di contenuto condiviso](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="57455-130">For more information about configuring App-V 5.0 SCS mode, see [How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="57455-131">Configurare il cluster di file server configurato sia nella modalità di scalabilità orizzontale di Microsoft Server2012 che in quella pre **2012** con una San virtuale.</span><span class="sxs-lookup"><span data-stu-id="57455-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="57455-132">Per convalidare la configurazione, è possibile usare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="57455-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="57455-133">Aggiungere un pacchetto nel server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="57455-133">Add a package on the publishing server.</span></span> <span data-ttu-id="57455-134">Per altre informazioni sull'aggiunta di un pacchetto, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="57455-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="57455-135">Eseguire un aggiornamento della pubblicazione nel computer che esegue il client App-V 5,0 e aprire un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57455-135">Perform a publishing refresh on the computer running the App-V 5.0 client and open an application.</span></span>

3.  <span data-ttu-id="57455-136">Cambiare i nodi del cluster durante l'aggiornamento e il Mid-streaming per verificare che il failover funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="57455-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="57455-137">Per altre informazioni sulla configurazione dei cluster di failover di Windows Server, vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="57455-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="57455-138">[Elenco di controllo: creare un file server in cluster](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="57455-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="57455-139">[Usare volumi condivisi del cluster in un cluster di failover di Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="57455-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="57455-140">Supporto per il mirroring di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="57455-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="57455-141">Usando il mirroring di Microsoft SQL Server, in cui il database del server di gestione di App-V 5,0 viene speculato utilizzando due istanze di SQL Server, per i database di App-V 5,0 Management Server è supportato.</span><span class="sxs-lookup"><span data-stu-id="57455-141">Using Microsoft SQL Server mirroring, where the App-V 5.0 management server database is mirrored utilizing two SQL Server instances, for App-V 5.0 management server databases is supported.</span></span>

<span data-ttu-id="57455-142">Per altre informazioni sulla configurazione del mirroring di Microsoft SQL Server, vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="57455-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="57455-143">[Procedura: preparare un database mirror per il mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="57455-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="57455-144">[Stabilire una sessione di mirroring del database usando l'autenticazione di Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="57455-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="57455-145">Per convalidare la configurazione, è possibile usare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="57455-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="57455-146">Avviare una sessione di mirroring di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57455-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="57455-147">Selezionare **failover** per designare una nuova istanza master di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57455-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="57455-148">Verificare che il server di gestione di App-V 5,0 continui a funzionare come previsto dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="57455-148">Verify that the App-V 5.0 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="57455-149">La stringa di connessione nel server di gestione può essere modificata per includere **failover partner &lt; = &gt; Server2**.</span><span class="sxs-lookup"><span data-stu-id="57455-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="57455-150">Ciò sarà utile solo quando il principale mirror non ha superato il controllo secondario e il computer che esegue il client App-V 5,0 sta eseguendo una nuova connessione (ad esempio dopo il riavvio).</span><span class="sxs-lookup"><span data-stu-id="57455-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.0 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="57455-151">Eseguire la procedura seguente per modificare la stringa di connessione in modo da includere il \*\*failover partner = &lt; Server2 &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="57455-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="57455-152">**Importante**  Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="57455-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="57455-153">Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="57455-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="57455-154">Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat).</span><span class="sxs-lookup"><span data-stu-id="57455-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="57455-155">Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="57455-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="57455-156">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="57455-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="57455-157">Accedere al server di gestione e aprire **Regedit**.</span><span class="sxs-lookup"><span data-stu-id="57455-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="57455-158">Passare a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **appv**  \\  **Server**  \\  **ManagementService**.</span><span class="sxs-lookup"><span data-stu-id="57455-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="57455-159">Modificare il valore di **gestione \ _SQL \ _CONNECTION \ _STRING** con il **partner failover &lt; = &gt; Server2**.</span><span class="sxs-lookup"><span data-stu-id="57455-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="57455-160">Riavviare il servizio di gestione tramite la console IIS.</span><span class="sxs-lookup"><span data-stu-id="57455-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="57455-161">**Nota**  Il mirroring del database è nell'elenco delle caratteristiche deprecate del motore di database per Microsoft SQL Server2012 a causa della funzionalità **AlwaysOn** disponibile in Microsoft sql Server 2012.</span><span class="sxs-lookup"><span data-stu-id="57455-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="57455-162">Per altre informazioni, fare clic su uno dei collegamenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="57455-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="57455-163">[Procedura: preparare un database mirror per il mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="57455-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="57455-164">[Procedura: configurare una sessione di mirroring del database (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="57455-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="57455-165">[Stabilire una sessione di mirroring del database usando l'autenticazione di Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="57455-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="57455-166">[Caratteristiche del motore di database obsolete in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="57455-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="57455-167">Supporto per Microsoft SQL Server sempre nella configurazione</span><span class="sxs-lookup"><span data-stu-id="57455-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="57455-168">Il database del server di gestione di App-V 5,0 supporta le distribuzioni nei computer che eseguono Microsoft SQL Server con la configurazione **Always on** .</span><span class="sxs-lookup"><span data-stu-id="57455-168">The App-V 5.0 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>

## <span data-ttu-id="57455-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57455-169">Related topics</span></span>


[<span data-ttu-id="57455-170">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="57455-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





