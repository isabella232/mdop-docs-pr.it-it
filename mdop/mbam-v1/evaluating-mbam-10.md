---
title: Valutazione di MBAM 1.0
description: Valutazione di MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825255"
---
# <span data-ttu-id="bfd9c-103">Valutazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="bfd9c-104">Prima di distribuire l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) in un ambiente di produzione, è consigliabile valutarlo in un ambiente lab.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="bfd9c-105">È possibile usare le informazioni contenute in questo argomento per configurare MBAM in un unico ambiente di Lab server solo per scopi di valutazione.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="bfd9c-106">Mentre i passaggi di distribuzione effettivi sono molto simili allo scenario descritto in [come installare e configurare mbam in un singolo server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), questo argomento contiene informazioni aggiuntive che consentono di configurare un ambiente di valutazione di MBAM nel minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="bfd9c-107">Configurare l'ambiente lab</span><span class="sxs-lookup"><span data-stu-id="bfd9c-107">Set up the Lab Environment</span></span>


<span data-ttu-id="bfd9c-108">Anche quando si configura un'istanza non di produzione di MBAM per la valutazione in un ambiente lab, è comunque necessario verificare che siano stati soddisfatti i prerequisiti per la distribuzione e i requisiti hardware e software.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="bfd9c-109">Per altre informazioni, Vedi [mbam 1,0 prerequisiti](mbam-10-deployment-prerequisites.md) per la distribuzione e [MBAM 1,0 configurazioni supportate](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bfd9c-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="bfd9c-110">Si dovrebbe anche rivedere la [preparazione dell'ambiente per mbam 1,0 prima di](preparing-your-environment-for-mbam-10.md) iniziare la distribuzione di valutazione mbam.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="bfd9c-111">Pianificare una distribuzione di valutazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="bfd9c-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="bfd9c-112">Attività</span><span class="sxs-lookup"><span data-stu-id="bfd9c-112">Task</span></span></th>
<th align="left"><span data-ttu-id="bfd9c-113">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="bfd9c-113">References</span></span></th>
<th align="left"><span data-ttu-id="bfd9c-114">Note</span><span class="sxs-lookup"><span data-stu-id="bfd9c-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-115">Esaminare le informazioni introduttive su MBAM per ottenere una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="bfd9c-116">Attività iniziali di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="bfd9c-117">Preparare l'ambiente di elaborazione per l'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="bfd9c-118">A questo scopo, devi abilitare la crittografia dati trasparente (Transparent Data Encryption) sulle istanze di SQL Server che ospiteranno i database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="bfd9c-119">Per abilitare la funzione Transparent nell'ambiente lab, è possibile creare un file con estensione SQL da eseguire sul database master ospitato nell'istanza di SQL Server che verrà usato da MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bfd9c-120">Nota</span><span class="sxs-lookup"><span data-stu-id="bfd9c-120">Note</span></span></strong><br/><p><span data-ttu-id="bfd9c-121">Puoi usare l'esempio seguente per creare un file con estensione SQL per l'ambiente lab in modo da abilitare rapidamente Transparent per l'istanza di SQL Server che ospita i database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="bfd9c-122">Questi comandi di SQL Server consentiranno a transparent di usare un certificato SQL Server firmato localmente.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="bfd9c-123">Assicurarsi di eseguire il backup del certificato di transcodificazione e della chiave di crittografia associata nel percorso di backup locale di esempio di <em> C:\backup </em> .</span><span class="sxs-lookup"><span data-stu-id="bfd9c-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="bfd9c-124">Il certificato e la chiave di transcodificazione dati sono necessari per recuperare il database o per trasferire il certificato e la chiave in un altro server con crittografia transattiva.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="bfd9c-125">Prerequisiti per la distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="bfd9c-126">Crittografia di database in SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="bfd9c-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-127">Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="bfd9c-128">Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-129">Pianificare e creare i gruppi di sicurezza di servizi di dominio Active Directory necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="bfd9c-130">Pianificazione dei ruoli di amministrazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-131">Pianificare la distribuzione delle funzionalità di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="bfd9c-132">Pianificazione della distribuzione del server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-133">Pianificare la distribuzione di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="bfd9c-134">Pianificazione della distribuzione del client di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="bfd9c-135">Eseguire una distribuzione di valutazione MBAM</span><span class="sxs-lookup"><span data-stu-id="bfd9c-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="bfd9c-136">Dopo aver completato le installazioni necessarie per la pianificazione e il software prerequisito per preparare l'ambiente di elaborazione per un'installazione di MBAM, è possibile iniziare la distribuzione di valutazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-137">Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione della funzionalità MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="bfd9c-138">Configurazioni supportate di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-139">Eseguire la configurazione di MBAM per distribuire le funzionalità di MBAM server su un singolo server a scopo di valutazione.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="bfd9c-140">Come installare e configurare MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="bfd9c-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-141">Aggiungere i gruppi di sicurezza di Active Directory Domain Services creati durante la fase di pianificazione per i gruppi locali appropriati di MBAM server locale nel nuovo server MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="bfd9c-142">Pianificazione per i ruoli di amministratore di MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> come gestire i ruoli di amministratore di mbam</span><span class="sxs-lookup"><span data-stu-id="bfd9c-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-143">Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="bfd9c-144">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bfd9c-145">Distribuire il software del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="bfd9c-146">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bfd9c-147">Configurare computer lab per la valutazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="bfd9c-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="bfd9c-148">È possibile modificare le impostazioni di frequenza nella segnalazione dello stato di MBAM client usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="bfd9c-149">Queste modifiche devono tuttavia essere usate solo per scopi di test.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="bfd9c-150">Warning</span><span class="sxs-lookup"><span data-stu-id="bfd9c-150">Warning</span></span>**  
<span data-ttu-id="bfd9c-151">Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="bfd9c-152">Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="bfd9c-153">Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat).</span><span class="sxs-lookup"><span data-stu-id="bfd9c-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="bfd9c-154">Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="bfd9c-155">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="bfd9c-156">Modificare le impostazioni di frequenza nella segnalazione di stato del client MBAM</span><span class="sxs-lookup"><span data-stu-id="bfd9c-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="bfd9c-157">Le frequenze di attivazione e segnalazione dello stato di MBAM client hanno un valore minimo di 90 minuti quando sono impostate per l'uso dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="bfd9c-158">Puoi modificare queste frequenze nei computer client di MBAM modificando il registro di sistema di Windows in valori più bassi, per velocizzare i test.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="bfd9c-159">Per modificare le impostazioni di frequenza nella segnalazione dello stato di MBAM client, usare un editor del registro di sistema per passare a **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, modificare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1** come valore minimo supportato dal client e quindi riavviare il servizio client di gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="bfd9c-160">Quando si apporta questa modifica, il client MBAM segnala ogni minuto.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="bfd9c-161">Puoi impostare i valori così bassi solo quando lo fai manualmente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="bfd9c-162">Modificare il ritardo di avvio del servizio client MBAM</span><span class="sxs-lookup"><span data-stu-id="bfd9c-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="bfd9c-163">Oltre alle frequenze di attivazione e segnalazione dello stato di MBAM client, c'è un ritardo casuale fino a 90 minuti quando il servizio agente client MBAM viene avviato nei computer client.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="bfd9c-164">Se non si vuole che il ritardo casuale, creare un valore **DWORD** di **NoStartupDelay** in **HKLM\\Software\\Microsoft\\MBAM**, impostarne il valore su **1**e quindi riavviare il servizio client di gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bfd9c-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="bfd9c-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfd9c-165">Related topics</span></span>


[<span data-ttu-id="bfd9c-166">Attività iniziali di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bfd9c-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









