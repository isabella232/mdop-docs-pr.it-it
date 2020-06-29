---
title: Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti
description: Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804462"
---
# <span data-ttu-id="829d5-103">Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="829d5-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="829d5-104">Questo argomento descrive il processo per l'aggiornamento del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) e del client MBAM dalle versioni precedenti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="829d5-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="829d5-105">**Nota**  È possibile eseguire l'aggiornamento direttamente a MBAM 2,5 o MBAM 2,5 SP1 da qualsiasi versione precedente di MBAM.</span><span class="sxs-lookup"><span data-stu-id="829d5-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="829d5-106">Prima di iniziare l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="829d5-106">Before you start the upgrade</span></span>


<span data-ttu-id="829d5-107">Prima di iniziare l'aggiornamento, esaminare le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="829d5-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="829d5-108">Informazioni da conoscere prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="829d5-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="829d5-109">Dettagli</span><span class="sxs-lookup"><span data-stu-id="829d5-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="829d5-110">Se si stanno installando i siti Web di MBAM su un server e i servizi Web in un altro server, è necessario usare i cmdlet di Windows PowerShell per configurarli.</span><span class="sxs-lookup"><span data-stu-id="829d5-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="829d5-111">La configurazione guidata di MBAM server non supporta la configurazione dei siti Web in un server e i servizi Web in un server diverso.</span><span class="sxs-lookup"><span data-stu-id="829d5-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="829d5-112">Se si esegue l'aggiornamento a MBAM 2.5 o 2,5 SP1 da MBAM 2.0 o 2,0 SP1 in Windows Server2008 R2:</span><span class="sxs-lookup"><span data-stu-id="829d5-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="829d5-113">Il sito Web di amministrazione e monitoraggio e il portale self-service non funzioneranno se si installa il software .NET Framework 4.5 richiesto dopo l'installazione di Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="829d5-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="829d5-114">Questo problema si verifica perché ASP.NET non può essere registrato correttamente con IIS se .NET Framework è installato dopo che IIS è già stato installato.</span><span class="sxs-lookup"><span data-stu-id="829d5-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="829d5-115">Per risolvere il problema:</span><span class="sxs-lookup"><span data-stu-id="829d5-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="829d5-116">Eseguire <strong> aspnet_regiis-i </strong> dalla posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="829d5-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="829d5-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="829d5-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="829d5-118">Per altre informazioni, vedere: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> strumento di registrazione di IIS ASP.NET </a> .</span><span class="sxs-lookup"><span data-stu-id="829d5-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="829d5-119">Registrare un nome SPN nell'account del pool di applicazioni se sono vere tutte le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="829d5-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="829d5-120">Si esegue l'aggiornamento da una versione precedente di MBAM.</span><span class="sxs-lookup"><span data-stu-id="829d5-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="829d5-121">Attualmente, non si eseguono i siti Web MBAM in una configurazione con bilanciamento del carico o distribuiti, ma si vuole farlo quando si esegue l'aggiornamento a MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="829d5-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="829d5-122">Per istruzioni, vedere <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> pianificazione di come proteggere i siti Web di mbam </a> .</span><span class="sxs-lookup"><span data-stu-id="829d5-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="829d5-123">Cosa consigliamo</span><span class="sxs-lookup"><span data-stu-id="829d5-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="829d5-124">Registrare un nome dell'entità servizio (SPN) per l'account del pool di applicazioni, anche se per l'account del computer potrebbero essere già presenti SPN registrati.</span><span class="sxs-lookup"><span data-stu-id="829d5-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="829d5-125">Perché è consigliabile</span><span class="sxs-lookup"><span data-stu-id="829d5-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="829d5-126">È necessario registrare un nome SPN nell'account del pool di applicazioni per configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.</span><span class="sxs-lookup"><span data-stu-id="829d5-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="829d5-127">Cosa succede se i nomi SPN sono già configurati in un account del computer?</span><span class="sxs-lookup"><span data-stu-id="829d5-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="829d5-128">MBAM utilizzerà i nomi SPN già registrati e non è necessario configurare altri nomi SPN, ma non è possibile configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.</span><span class="sxs-lookup"><span data-stu-id="829d5-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="829d5-129">Procedura per aggiornare l'infrastruttura del server MBAM</span><span class="sxs-lookup"><span data-stu-id="829d5-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="829d5-130">Usare i passaggi descritti nelle sezioni seguenti per aggiornare MBAM per la topologia autonoma o la topologia di integrazione di System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="829d5-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="829d5-131">Per aggiornare l'infrastruttura di MBAM server per la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="829d5-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="829d5-132">Disinstallare versioni precedenti di MBAM da **programmi e funzionalità** e da server Web per assicurarsi che le informazioni non vengano scritte da client mbam per l'infrastruttura mbam.</span><span class="sxs-lookup"><span data-stu-id="829d5-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="829d5-133">Per istruzioni, Vedi [rimozione delle funzionalità o del software di mbam server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="829d5-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="829d5-134">Eseguire il backup dei database.</span><span class="sxs-lookup"><span data-stu-id="829d5-134">Back up your databases.</span></span>

3.  <span data-ttu-id="829d5-135">Disinstallare le versioni precedenti di MBAM da SQL Server usando **programmi e funzionalità**, tra cui SQL Server che ospitano i report di mbam tramite SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="829d5-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="829d5-136">Rimuovere eventuali cartelle o file temporanei di MBAM rimanenti dal server di database e Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="829d5-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="829d5-137">**Nota**  I database non verranno rimossi e tutti i dati di conformità e ripristino vengono mantenuti nel database.</span><span class="sxs-lookup"><span data-stu-id="829d5-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="829d5-138">Installare e configurare i database MBAM 2.5 o 2,5 SP1, i report e le applicazioni Web, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="829d5-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="829d5-139">I database vengono aggiornati in posizione.</span><span class="sxs-lookup"><span data-stu-id="829d5-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="829d5-140">Aggiornare gli oggetti Criteri di gruppo usando i modelli di MBAM 2,5 per sfruttare le nuove funzionalità di MBAM, ad esempio la crittografia forzata.</span><span class="sxs-lookup"><span data-stu-id="829d5-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="829d5-141">Se non si aggiornano gli oggetti Criteri di stato e il client MBAM per MBAM 2,5, le versioni precedenti dei client MBAM continueranno a segnalare i criteri di GPO correnti con funzionalità ridotte.</span><span class="sxs-lookup"><span data-stu-id="829d5-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="829d5-142">Vedere [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://www.microsoft.com/download/details.aspx?id=41183) per scaricare i modelli ADMX più recenti.</span><span class="sxs-lookup"><span data-stu-id="829d5-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="829d5-143">Dopo l'aggiornamento dell'infrastruttura di MBAM server, i computer client esistenti continuano a segnalare correttamente il server MBAM 2.5 o 2,5 SP1 e i dati di ripristino continuano a essere archiviati.</span><span class="sxs-lookup"><span data-stu-id="829d5-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="829d5-144">Installare l'ultimo client di MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="829d5-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="829d5-145">Dopo la distribuzione, non è necessario riavviare i computer client.</span><span class="sxs-lookup"><span data-stu-id="829d5-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="829d5-146">Per aggiornare l'infrastruttura MBAM per la topologia di integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="829d5-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="829d5-147">Disinstallare versioni precedenti di MBAM da **programmi e funzionalità** e da server Web per assicurarsi che le informazioni non vengano scritte da client mbam per l'infrastruttura mbam.</span><span class="sxs-lookup"><span data-stu-id="829d5-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="829d5-148">Per istruzioni, Vedi [rimozione delle funzionalità o del software di mbam server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="829d5-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="829d5-149">Eseguire il backup dei database.</span><span class="sxs-lookup"><span data-stu-id="829d5-149">Back up your databases.</span></span>

3.  <span data-ttu-id="829d5-150">Disinstallare le versioni precedenti di MBAM da SQL Server usando **programmi e funzionalità**, tra cui SQL Server che ospitano i report di mbam tramite SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="829d5-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="829d5-151">Rimuovere eventuali cartelle o file temporanei di MBAM rimanenti dal server di database e Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="829d5-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="829d5-152">Disinstallare MBAM dal Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="829d5-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="829d5-153">**Nota**  I database e gli oggetti Configuration Manager (Baseline, MBAM supported Computers Collection e Reports) non verranno rimossi e tutti i dati di conformità e ripristino vengono mantenuti nel database.</span><span class="sxs-lookup"><span data-stu-id="829d5-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="829d5-154">Aggiornare i file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="829d5-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="829d5-155">Installare e configurare i database MBAM 2.5 o 2,5 SP1, i report, le applicazioni Web e l'integrazione di Configuration Manager in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="829d5-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="829d5-156">Gli oggetti database e Configuration Manager vengono aggiornati in posizione.</span><span class="sxs-lookup"><span data-stu-id="829d5-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="829d5-157">Facoltativamente, aggiornare gli oggetti Criteri di gruppo e modificare le impostazioni se si vogliono implementare nuove funzionalità in MBAM, ad esempio la crittografia imposta.</span><span class="sxs-lookup"><span data-stu-id="829d5-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="829d5-158">Se non si aggiornano i GPO, MBAM continuerà a segnalare i criteri di GPO correnti.</span><span class="sxs-lookup"><span data-stu-id="829d5-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="829d5-159">Vedere [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) per scaricare i modelli ADMX più recenti.</span><span class="sxs-lookup"><span data-stu-id="829d5-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="829d5-160">Dopo l'aggiornamento dell'infrastruttura di MBAM server, i computer client esistenti continuano a segnalare correttamente il server MBAM 2.5 o 2,5 SP1 e i dati di ripristino continuano a essere archiviati.</span><span class="sxs-lookup"><span data-stu-id="829d5-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="829d5-161">Installare l'ultimo client di MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="829d5-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="829d5-162">Dopo la distribuzione, non è necessario riavviare i computer client.</span><span class="sxs-lookup"><span data-stu-id="829d5-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="829d5-163">Supporto per l'aggiornamento per il client MBAM</span><span class="sxs-lookup"><span data-stu-id="829d5-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="829d5-164">MBAM supporta gli aggiornamenti per il client MBAM 2.5 da qualsiasi versione precedente del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="829d5-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="829d5-165">Modalità di installazione del client MBAM:</span><span class="sxs-lookup"><span data-stu-id="829d5-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="829d5-166">Aggiornare i computer che eseguono il client MBAM tutto in una volta o gradualmente dopo aver installato l'infrastruttura del server MBAM 2.5.</span><span class="sxs-lookup"><span data-stu-id="829d5-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="829d5-167">Installare il client MBAM tramite un sistema elettronico di distribuzione del software o tramite strumenti come servizi di dominio Active Directory o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="829d5-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="829d5-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="829d5-168">Related topics</span></span>


[<span data-ttu-id="829d5-169">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="829d5-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="829d5-170">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="829d5-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="829d5-171">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="829d5-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="829d5-172">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="829d5-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="829d5-173">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="829d5-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="829d5-174">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="829d5-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





