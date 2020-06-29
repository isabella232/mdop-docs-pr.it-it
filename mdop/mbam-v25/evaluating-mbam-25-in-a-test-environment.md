---
title: Valutazione di MBAM 2.5 in un ambiente di test
description: Valutazione di MBAM 2.5 in un ambiente di test
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823155"
---
# <span data-ttu-id="f13e4-103">Valutazione di MBAM 2.5 in un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="f13e4-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="f13e4-104">Questo argomento descrive come configurare un ambiente di test per valutare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) 2,5 nella topologia di integrazione autonoma o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f13e4-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="f13e4-105">Valutazione di MBAM 2,5 tramite la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="f13e4-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="f13e4-106">Per valutare MBAM usando la topologia autonoma, usare le informazioni nelle tabelle seguenti per installare il software MBAM server e quindi configurare le caratteristiche del server MBAM nell'ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f13e4-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="f13e4-107">Per valutare MBAM 2,5 usando la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="f13e4-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="f13e4-108">Prima di installare MBAM, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-109">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-110">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-111">Verificare di avere installato tutto il software prerequisito.</span><span class="sxs-lookup"><span data-stu-id="f13e4-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f13e4-112">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-113">Verificare l'hardware, la RAM e altre specifiche richieste.</span><span class="sxs-lookup"><span data-stu-id="f13e4-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f13e4-114">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-115">Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare MBAM.</span><span class="sxs-lookup"><span data-stu-id="f13e4-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="f13e4-116">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f13e4-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f13e4-117">Installare il software MBAM server e quindi configurare le caratteristiche desiderate.</span><span class="sxs-lookup"><span data-stu-id="f13e4-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-118">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-119">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-120">Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="f13e4-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f13e4-121">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-122">Configurare il database di conformità e controllo e il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f13e4-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f13e4-123">Come configurare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-124">Configurare la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="f13e4-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f13e4-125">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-126">Configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="f13e4-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f13e4-127">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f13e4-128">In un computer client eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f13e4-129">Installare il client MBAM in un computer client.</span><span class="sxs-lookup"><span data-stu-id="f13e4-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="f13e4-130">Applicare gli oggetti Criteri di gruppo di MBAM al computer.</span><span class="sxs-lookup"><span data-stu-id="f13e4-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="f13e4-131">Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli regolari:</span><span class="sxs-lookup"><span data-stu-id="f13e4-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f13e4-132">Nota</span><span class="sxs-lookup"><span data-stu-id="f13e4-132">Note</span></span>**  
       <span data-ttu-id="f13e4-133">Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f13e4-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="f13e4-134">Riavviare il **servizio client di gestione di BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="f13e4-135">Valutazione di MBAM 2,5 tramite la topologia di integrazione di System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="f13e4-136">Per valutare MBAM usando la topologia di integrazione di Configuration Manager, usare le informazioni nelle tabelle seguenti per installare il software di MBAM server e quindi configurare le caratteristiche del server MBAM nell'ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f13e4-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="f13e4-137">Dopo l'installazione del client MBAM su un computer client, verranno completate le procedure aggiuntive per forzare il client MBAM a segnalare lo stato del computer a MBAM più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f13e4-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="f13e4-138">Per valutare MBAM 2,5 usando la topologia di integrazione di System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="f13e4-139">Prima di installare MBAM, rivedere il software prerequisito e la configurazione supportata.</span><span class="sxs-lookup"><span data-stu-id="f13e4-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-140">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-141">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-142">Verificare di avere installato tutto il software prerequisito.</span><span class="sxs-lookup"><span data-stu-id="f13e4-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f13e4-143">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="f13e4-144">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-145">Verificare l'hardware, la RAM e altre specifiche richieste.</span><span class="sxs-lookup"><span data-stu-id="f13e4-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f13e4-146">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-147">Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare MBAM.</span><span class="sxs-lookup"><span data-stu-id="f13e4-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="f13e4-148">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f13e4-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-149">Creare o modificare i file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="f13e4-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="f13e4-150">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="f13e4-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="f13e4-151">Creare o modificare il file Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="f13e4-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f13e4-152">Installare il software MBAM server e quindi configurare le caratteristiche desiderate.</span><span class="sxs-lookup"><span data-stu-id="f13e4-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-153">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-154">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-155">Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="f13e4-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f13e4-156">Nota</span><span class="sxs-lookup"><span data-stu-id="f13e4-156">Note</span></span></strong><br/><p><span data-ttu-id="f13e4-157">È possibile installare i database in un computer SQL Server remoto tramite Windows PowerShell o un pacchetto di applicazione a livello di dati esportato (DAC).</span><span class="sxs-lookup"><span data-stu-id="f13e4-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="f13e4-158">Per altre informazioni sui pacchetti DAC, vedere <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applicazioni a livello di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="f13e4-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f13e4-159">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-160">Configurare il database di conformità e controllo e il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f13e4-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f13e4-161">Come configurare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-162">Configurare la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="f13e4-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f13e4-163">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-164">Configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="f13e4-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f13e4-165">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-166">Configurare System Center Configuration Manager per installare gli oggetti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f13e4-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="f13e4-167">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f13e4-168">In un computer client eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f13e4-169">Installare il client MBAM e il client Configuration Manager in un computer client.</span><span class="sxs-lookup"><span data-stu-id="f13e4-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="f13e4-170">Applicare gli oggetti Criteri di gruppo di MBAM al computer.</span><span class="sxs-lookup"><span data-stu-id="f13e4-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="f13e4-171">Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli regolari:</span><span class="sxs-lookup"><span data-stu-id="f13e4-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f13e4-172">Nota</span><span class="sxs-lookup"><span data-stu-id="f13e4-172">Note</span></span>**  
       <span data-ttu-id="f13e4-173">Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f13e4-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="f13e4-174">Riavviare il **servizio client di gestione di BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="f13e4-175">Nel pannello di controllo aprire **Gestione configurazione**e quindi fare clic sulla scheda **azioni** .</span><span class="sxs-lookup"><span data-stu-id="f13e4-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="f13e4-176">Selezionare **ciclo di inventario hardware**e quindi fare clic su **Esegui ora**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="f13e4-177">Questo passaggio esegue l'inventario hardware usando le nuove classi importate nei file MOF e quindi invia i dati al Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f13e4-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="f13e4-178">Selezionare **recupero criteri computer & ciclo di valutazione**e quindi fare clic su **Esegui ora** per applicare gli oggetti Criteri di gruppo rilevanti per il computer client.</span><span class="sxs-lookup"><span data-stu-id="f13e4-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="f13e4-179">Nella console di Configuration Manager eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="f13e4-180">Nel riquadro di spostamento fare clic con il pulsante destro del mouse su **computer supportati mbam**, scegliere **Aggiorna appartenenza**e quindi fare clic su **Sì** per forzare il computer client a segnalare immediatamente l'appartenenza.</span><span class="sxs-lookup"><span data-stu-id="f13e4-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="f13e4-181">Nel riquadro di spostamento fare clic su **mbam computer supportati** per verificare che il computer client venga visualizzato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="f13e4-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="f13e4-182">Nel pannello di controllo del computer client riaprire **Configuration Manager** ed eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="f13e4-183">Fare clic sulla scheda **azioni** e quindi rieseguire il **recupero dei criteri del computer & ciclo di valutazione**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="f13e4-184">Fare clic sulla scheda **configurazioni** , selezionare la previsione di BitLocker e quindi fare clic su **valuta**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="f13e4-185">Nella console di Configuration Manager verificare che il computer client venga visualizzato nel report conformità aziendale: come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f13e4-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="f13e4-186">Nel riquadro di spostamento selezionare l'area di lavoro **monitoraggio** .</span><span class="sxs-lookup"><span data-stu-id="f13e4-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="f13e4-187">Nell'albero della console espandere **Panoramica** &gt; **report** &gt; **Reports** &gt; **mbam**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="f13e4-188">Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro risultati.</span><span class="sxs-lookup"><span data-stu-id="f13e4-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="f13e4-189">Valutazione di MBAM 2,5 tramite la topologia di integrazione di System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f13e4-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="f13e4-190">Per valutare MBAM usando la topologia di integrazione di Configuration Manager, seguire la stessa procedura per installare e configurare MBAM nell'ambiente di test durante l'uso in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="f13e4-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="f13e4-191">Dopo l'installazione del client MBAM in un computer client, completare i passaggi aggiuntivi in questo argomento per consentire al client MBAM di iniziare a segnalare lo stato del computer a MBAM più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f13e4-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="f13e4-192">Per valutare MBAM usando la topologia di integrazione di Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f13e4-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="f13e4-193">Prima di installare MBAM, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-194">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-195">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-196">Verificare di avere installato tutto il software prerequisito.</span><span class="sxs-lookup"><span data-stu-id="f13e4-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f13e4-197">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="f13e4-198">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-199">Verificare l'hardware, la RAM e altre specifiche richieste.</span><span class="sxs-lookup"><span data-stu-id="f13e4-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f13e4-200">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-201">Creare o modificare i file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="f13e4-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="f13e4-202">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="f13e4-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="f13e4-203">Creare o modificare il file Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="f13e4-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f13e4-204">Installare il software MBAM server e quindi configurare le caratteristiche desiderate.</span><span class="sxs-lookup"><span data-stu-id="f13e4-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f13e4-205">Attività</span><span class="sxs-lookup"><span data-stu-id="f13e4-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="f13e4-206">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="f13e4-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-207">Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="f13e4-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f13e4-208">Nota</span><span class="sxs-lookup"><span data-stu-id="f13e4-208">Note</span></span></strong><br/><p><span data-ttu-id="f13e4-209">È possibile installare i database in un computer SQL Server remoto tramite Windows PowerShell o un pacchetto di applicazione a livello di dati esportato (DAC).</span><span class="sxs-lookup"><span data-stu-id="f13e4-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="f13e4-210">Per altre informazioni sui pacchetti DAC, vedere <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applicazioni a livello di dati </a> .</span><span class="sxs-lookup"><span data-stu-id="f13e4-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f13e4-211">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-212">Configurare il database di conformità e controllo e il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f13e4-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="f13e4-213">Come configurare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-214">Configurare la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="f13e4-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="f13e4-215">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f13e4-216">Configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="f13e4-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="f13e4-217">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f13e4-218">Configurare System Center Configuration Manager per installare gli oggetti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f13e4-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="f13e4-219">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f13e4-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f13e4-220">In un computer client eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="f13e4-221">Installare il client MBAM in un computer client.</span><span class="sxs-lookup"><span data-stu-id="f13e4-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="f13e4-222">Applicare gli oggetti Criteri di gruppo di MBAM al computer.</span><span class="sxs-lookup"><span data-stu-id="f13e4-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="f13e4-223">Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli più rapidi:</span><span class="sxs-lookup"><span data-stu-id="f13e4-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="f13e4-224">Nota</span><span class="sxs-lookup"><span data-stu-id="f13e4-224">Note</span></span>**  
       <span data-ttu-id="f13e4-225">Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di valutazione.</span><span class="sxs-lookup"><span data-stu-id="f13e4-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="f13e4-226">Riavviare il **servizio client di gestione di BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="f13e4-227">Nel pannello di controllo aprire **Gestione configurazione**e quindi fare clic sulla scheda **azioni** .</span><span class="sxs-lookup"><span data-stu-id="f13e4-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="f13e4-228">Selezionare **recupero criteri computer & ciclo di valutazione**e quindi fare clic su **Esegui ora** per applicare gli oggetti Criteri di gruppo rilevanti per il computer client.</span><span class="sxs-lookup"><span data-stu-id="f13e4-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="f13e4-229">Selezionare **ciclo di inventario hardware**e quindi fare clic su **Esegui ora**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="f13e4-230">Questo passaggio esegue l'inventario hardware usando le nuove classi importate nei file MOF e quindi invia i dati al Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f13e4-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="f13e4-231">Nella console di Configuration Manager eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="f13e4-232">Nel riquadro di spostamento fare clic con il pulsante destro del mouse su **computer supportati mbam**, scegliere **Aggiorna appartenenza**e quindi fare clic su **Sì** per forzare il computer client a segnalare immediatamente l'appartenenza.</span><span class="sxs-lookup"><span data-stu-id="f13e4-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="f13e4-233">Nel riquadro di spostamento fare clic su **mbam computer supportati** per verificare che il computer client venga visualizzato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="f13e4-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="f13e4-234">Nel pannello di controllo del computer client riaprire **Configuration Manager** ed eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f13e4-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="f13e4-235">Fare clic sulla scheda **azioni** e quindi rieseguire il **recupero dei criteri del computer & ciclo di valutazione**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="f13e4-236">Fare clic sulla scheda **configurazioni** , selezionare la previsione di BitLocker e fare clic su **valuta**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="f13e4-237">Nella console di Configuration Manager verificare che il computer client venga visualizzato nel report conformità aziendale, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f13e4-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="f13e4-238">Nel riquadro di spostamento espandere **Gestione computer** &gt; **Reporting** &gt; **Services** &gt; \*\* &lt; server &gt; mbam\*\*.</span><span class="sxs-lookup"><span data-stu-id="f13e4-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="f13e4-239">All'interno del nodo **mbam** selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro risultati.</span><span class="sxs-lookup"><span data-stu-id="f13e4-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="f13e4-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f13e4-240">Related topics</span></span>


[<span data-ttu-id="f13e4-241">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f13e4-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="f13e4-242">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="f13e4-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f13e4-243">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f13e4-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="f13e4-244">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f13e4-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





