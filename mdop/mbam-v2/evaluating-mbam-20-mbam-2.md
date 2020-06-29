---
title: Valutazione di MBAM 2.0
description: Valutazione di MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824736"
---
# <span data-ttu-id="f88c4-103">Valutazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="f88c4-104">Prima di distribuire Microsoft BitLocker Administration and Monitoring (MBAM) in un ambiente di produzione, è consigliabile valutarlo in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f88c4-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="f88c4-105">Le informazioni contenute in questo argomento possono essere usate per configurare l'amministrazione e il monitoraggio di Microsoft BitLocker con una topologia autonoma in un ambiente di test a server singolo per scopi di valutazione.</span><span class="sxs-lookup"><span data-stu-id="f88c4-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="f88c4-106">Una topologia a server singolo non è consigliata per gli ambienti di produzione.</span><span class="sxs-lookup"><span data-stu-id="f88c4-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="f88c4-107">Per istruzioni sulla distribuzione di MBAM in un ambiente di test, vedere [come installare e configurare mbam in un singolo server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f88c4-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="f88c4-108">Configurazione dell'ambiente di test</span><span class="sxs-lookup"><span data-stu-id="f88c4-108">Setting up the Test Environment</span></span>


<span data-ttu-id="f88c4-109">Anche se si sta configurando un'istanza non di produzione di MBAM per la valutazione in un ambiente di test, è comunque necessario verificare che siano stati soddisfatti i prerequisiti e i requisiti hardware e software.</span><span class="sxs-lookup"><span data-stu-id="f88c4-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="f88c4-110">Prima di avviare l'installazione, vedere [mbam 2,0 prerequisiti di distribuzione](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 configurazioni supportate](mbam-20-supported-configurations-mbam-2.md)e [preparare l'ambiente per MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f88c4-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="f88c4-111">Pianificare una distribuzione di valutazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="f88c4-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="f88c4-112">Attività</span><span class="sxs-lookup"><span data-stu-id="f88c4-112">Task</span></span></th>
<th align="left"><span data-ttu-id="f88c4-113">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="f88c4-113">References</span></span></th>
<th align="left"><span data-ttu-id="f88c4-114">Note</span><span class="sxs-lookup"><span data-stu-id="f88c4-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-115">Esaminare le informazioni introduttive su MBAM per ottenere una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f88c4-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="f88c4-116">Attività iniziali di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-117">Pianificare i prerequisiti per la distribuzione di MBAM 2,0 e preparare l'ambiente di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f88c4-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="f88c4-118">Prerequisiti per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-119">Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="f88c4-120">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-121">Pianificare e creare gruppi di sicurezza di ActiveDirectoryDomainServices necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="f88c4-122">Pianificazione dei ruoli di amministrazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-123">Pianificare la distribuzione della funzionalità MBAM Server Deployment.</span><span class="sxs-lookup"><span data-stu-id="f88c4-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="f88c4-124">Pianificazione della distribuzione del server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-125">Pianificare la distribuzione di MBAM Client Deployment.</span><span class="sxs-lookup"><span data-stu-id="f88c4-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="f88c4-126">Pianificazione della distribuzione del client di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f88c4-127">Eseguire una distribuzione di valutazione MBAM</span><span class="sxs-lookup"><span data-stu-id="f88c4-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="f88c4-128">Dopo aver completato le necessarie installazioni per la pianificazione e il software prerequisito per preparare l'ambiente di calcolo per l'installazione di MBAM, è possibile iniziare la distribuzione di valutazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

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
<td align="left"><p><span data-ttu-id="f88c4-129">Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="f88c4-130">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-131">Eseguire la configurazione di MBAM per distribuire le funzionalità di MBAM server su un singolo server a scopo di valutazione.</span><span class="sxs-lookup"><span data-stu-id="f88c4-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="f88c4-132">Come installare e configurare MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="f88c4-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-133">Aggiungere gruppi di sicurezza di ActiveDirectoryDomainServices, creati durante la fase di pianificazione, per i gruppi locali appropriati di MBAM server locale nel nuovo server MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="f88c4-134">Pianificazione per i ruoli di amministratore di MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> come gestire i ruoli di amministratore di mbam</span><span class="sxs-lookup"><span data-stu-id="f88c4-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-135">Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="f88c4-136">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f88c4-137">Distribuire il software del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f88c4-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="f88c4-138">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f88c4-139">Configurare computer lab per la valutazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="f88c4-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="f88c4-140">Questa sezione contiene informazioni che possono essere usate per velocizzare la segnalazione dello stato di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="f88c4-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="f88c4-141">Queste modifiche devono tuttavia essere usate solo per scopi di test.</span><span class="sxs-lookup"><span data-stu-id="f88c4-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="f88c4-142">**Nota**  Le informazioni nella sezione seguente illustrano come modificare il registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="f88c4-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="f88c4-143">L'uso errato dell'editor del registro di sistema può causare seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="f88c4-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="f88c4-144">Microsoft non può garantire che i problemi causati dall'uso errato dell'editor del registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="f88c4-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="f88c4-145">Usare l'editor del registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="f88c4-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="f88c4-146">Modificare le impostazioni di frequenza di segnalazione dello stato del client MBAM</span><span class="sxs-lookup"><span data-stu-id="f88c4-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="f88c4-147">Le frequenze di attivazione e segnalazione dello stato di MBAM client hanno un valore minimo di 90 minuti quando vengono impostate tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f88c4-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="f88c4-148">Puoi usare il registro di sistema di Windows per modificare queste frequenze in un valore inferiore nei computer client di MBAM per velocizzare i test.</span><span class="sxs-lookup"><span data-stu-id="f88c4-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="f88c4-149">Per modificare le impostazioni di frequenza per la segnalazione dello stato del client MBAM:</span><span class="sxs-lookup"><span data-stu-id="f88c4-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="f88c4-150">Usare un editor del registro di sistema per passare a **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="f88c4-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="f88c4-151">Modificare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1** come valore minimo supportato dal client.</span><span class="sxs-lookup"><span data-stu-id="f88c4-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="f88c4-152">Questa modifica fa sì che il client MBAM riferisca ogni minuto.</span><span class="sxs-lookup"><span data-stu-id="f88c4-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="f88c4-153">Riavviare il **servizio client di gestione di BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f88c4-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="f88c4-154">**Nota**  Per impostare valori così bassi, è necessario impostarli manualmente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f88c4-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="f88c4-155">Modificare il ritardo di avvio del servizio client MBAM</span><span class="sxs-lookup"><span data-stu-id="f88c4-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="f88c4-156">Oltre alle frequenze di attivazione e segnalazione dello stato di MBAM client, c'è un ritardo casuale fino a 90 minuti quando il servizio agente client MBAM viene avviato nei computer client.</span><span class="sxs-lookup"><span data-stu-id="f88c4-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="f88c4-157">Se non si vuole che il ritardo casuale, creare un valore **DWORD** di **NoStartupDelay** in **HKLM\\Software\\Microsoft\\MBAM**, impostarne il valore su **1**e quindi riavviare il **servizio client di gestione di BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f88c4-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="f88c4-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f88c4-158">Related topics</span></span>


[<span data-ttu-id="f88c4-159">Attività iniziali di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f88c4-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





