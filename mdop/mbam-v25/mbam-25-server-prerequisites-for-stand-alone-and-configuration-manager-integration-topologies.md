---
title: Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager
description: Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825996"
---
# <span data-ttu-id="8607c-103">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8607c-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="8607c-104">Prima di avviare l'installazione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è necessario completare i prerequisiti elencati in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="8607c-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="8607c-105">Questi prerequisiti si applicano alla topologia MBAM autonoma e all'integrazione di System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8607c-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="8607c-106">Se si sta distribuendo MBAM con System Center Configuration Manager, è necessario completare i prerequisiti aggiuntivi, elencati nei [prerequisiti del server mbam 2,5 che si applicano solo alla topologia di integrazione di Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="8607c-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="8607c-107">Per un elenco dei sistemi operativi e hardware supportati per MBAM, Vedi le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="8607c-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="8607c-108">Importante</span><span class="sxs-lookup"><span data-stu-id="8607c-108">Important</span></span>**  
<span data-ttu-id="8607c-109">Se BitLocker è stato usato senza MBAM, è necessario decrittografare l'unità e quindi cancellare TPM usando TPM. msc.</span><span class="sxs-lookup"><span data-stu-id="8607c-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="8607c-110">MBAM non può assumere la proprietà del TPM se il PC client è già crittografato e la password del proprietario del TPM è stata creata.</span><span class="sxs-lookup"><span data-stu-id="8607c-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="8607c-111">Ruoli e account di MBAM necessari</span><span class="sxs-lookup"><span data-stu-id="8607c-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-113">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-114">Gruppi creati in servizi di dominio Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="8607c-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-115">Vedere <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> pianificazione per i gruppi e gli account di MBAM 2,5 </a> per una descrizione di questi gruppi e account.</span><span class="sxs-lookup"><span data-stu-id="8607c-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8607c-116">Prerequisiti per il database di ripristino</span><span class="sxs-lookup"><span data-stu-id="8607c-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-117">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-118">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-119">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-120">Installare Microsoft SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="8607c-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="8607c-121">Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="8607c-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-122">Autorizzazioni di SQL Server obbligatorie</span><span class="sxs-lookup"><span data-stu-id="8607c-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-123">Autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="8607c-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-124">Ruoli del server di accesso istanza di SQL Server:</span><span class="sxs-lookup"><span data-stu-id="8607c-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="8607c-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="8607c-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="8607c-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="8607c-127">Diritti di istanza di SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="8607c-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-128">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="8607c-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="8607c-129">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="8607c-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-130">Facoltativo: installare la funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-131">La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare leggi, normative e linee guida applicabili a vari settori.</span><span class="sxs-lookup"><span data-stu-id="8607c-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8607c-132">Nota</span><span class="sxs-lookup"><span data-stu-id="8607c-132">Note</span></span></strong><br/><p><span data-ttu-id="8607c-133">Transparent esegue la decrittografia in tempo reale delle informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="8607c-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="8607c-134">Questo significa che, se si stanno visualizzando le informazioni chiave di ripristino nel database di SQL Server e si è connessi con un account che dispone delle autorizzazioni per il database, le informazioni sulla chiave di ripristino sono visibili.</span><span class="sxs-lookup"><span data-stu-id="8607c-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="8607c-135">Per saperne di più su Transparent, vedere <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="8607c-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-136">Servizi motore di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-137">I servizi motore di database di SQL Server devono essere installati e eseguiti durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="8607c-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-138">Windows PowerShell 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8607c-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-139">Windows PowerShell non deve essere installato nel server di database di ripristino se si usa Windows PowerShell per configurare il database da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8607c-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8607c-140">Prerequisiti per il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="8607c-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-141">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-142">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-143">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-144">Installare SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="8607c-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="8607c-145">Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="8607c-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-146">Autorizzazioni di SQL Server obbligatorie</span><span class="sxs-lookup"><span data-stu-id="8607c-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-147">Autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="8607c-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-148">Ruoli del server di accesso istanza di SQL Server:</span><span class="sxs-lookup"><span data-stu-id="8607c-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="8607c-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="8607c-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="8607c-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="8607c-151">Diritti di istanza di SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="8607c-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-152">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="8607c-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="8607c-153">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="8607c-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-154">Facoltativo: installare la funzionalità di crittografia dei dati trasparente (Transparent Data Encryption) in SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-155">La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare leggi, normative e linee guida applicabili a vari settori.</span><span class="sxs-lookup"><span data-stu-id="8607c-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="8607c-156">Transparent esegue la decrittografia in tempo reale delle informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="8607c-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="8607c-157">Questo significa che, se si stanno visualizzando le informazioni chiave di ripristino nel database di SQL Server e si è connessi con un account che dispone delle autorizzazioni per il database, le informazioni sulla chiave di ripristino sono visibili.</span><span class="sxs-lookup"><span data-stu-id="8607c-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="8607c-158">Per saperne di più su Transparent, vedere <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="8607c-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-159">Servizi motore di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-160">I servizi motore di database di SQL Server devono essere installati e eseguiti durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="8607c-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="8607c-161">Tuttavia, SQL Server può essere eseguito in remoto; non deve essere nello stesso server in cui si sta installando il software del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="8607c-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-162">Windows PowerShell 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8607c-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-163">Windows PowerShell non deve essere installato nel server di database di conformità e controllo se si usa Windows PowerShell per configurare il database da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8607c-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8607c-164">Prerequisiti per i report</span><span class="sxs-lookup"><span data-stu-id="8607c-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-165">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-166">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-167">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="8607c-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-168">Installare SQL Server con le regole di confronto SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="8607c-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="8607c-169">Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="8607c-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-170">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="8607c-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-171">SSRS deve essere installato ed eseguito durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="8607c-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="8607c-172">Configurare SSRS in &quot; &quot; modalità nativa e non in modalità non configurata o &quot; SharePoint &quot; .</span><span class="sxs-lookup"><span data-stu-id="8607c-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-173">Diritti delle istanze di SSRS: necessari per la configurazione dei report solo se si installano database in un server separato dal server in cui sono configurati i report.</span><span class="sxs-lookup"><span data-stu-id="8607c-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-174">Diritti di istanza obbligatori:</span><span class="sxs-lookup"><span data-stu-id="8607c-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="8607c-175">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="8607c-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="8607c-176">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="8607c-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-177">Windows PowerShell 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8607c-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-178">Windows PowerShell non deve essere installato in questo server di database se si usa Windows PowerShell per configurare il database da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8607c-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="8607c-179">Prerequisiti per l'amministrazione e il server di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="8607c-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="8607c-180">La tabella seguente elenca i prerequisiti di installazione per l'amministrazione e il server di monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8607c-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-181">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-182">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-183">Ruolo di Windows Server Web Server</span><span class="sxs-lookup"><span data-stu-id="8607c-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-184">Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità di amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="8607c-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-185">Strumenti di gestione di Web Server (IIS)</span><span class="sxs-lookup"><span data-stu-id="8607c-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-186">Fare clic su <strong> script e strumenti di gestione IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="8607c-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8607c-187">Certificato SSL</span><span class="sxs-lookup"><span data-stu-id="8607c-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8607c-188">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8607c-188">Optional.</span></span> <span data-ttu-id="8607c-189">Per proteggere le comunicazioni tra i computer client e i servizi Web, è necessario ottenere e installare un certificato firmato da un'autorità di sicurezza attendibile.</span><span class="sxs-lookup"><span data-stu-id="8607c-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-190">Servizi ruolo server Web</span><span class="sxs-lookup"><span data-stu-id="8607c-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="8607c-191">Caratteristiche HTTP comuni:</span><span class="sxs-lookup"><span data-stu-id="8607c-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="8607c-192">Contenuto statico</span><span class="sxs-lookup"><span data-stu-id="8607c-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="8607c-193">Documento predefinito</span><span class="sxs-lookup"><span data-stu-id="8607c-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="8607c-194">Sviluppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="8607c-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="8607c-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="8607c-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="8607c-196">Estensibilità .NET</span><span class="sxs-lookup"><span data-stu-id="8607c-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="8607c-197">Estensioni ISAPI</span><span class="sxs-lookup"><span data-stu-id="8607c-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="8607c-198">Filtri ISAPI</span><span class="sxs-lookup"><span data-stu-id="8607c-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="8607c-199">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="8607c-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="8607c-200">Autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="8607c-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="8607c-201">Filtro delle richieste</span><span class="sxs-lookup"><span data-stu-id="8607c-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-202">Caratteristiche di Windows Server</span><span class="sxs-lookup"><span data-stu-id="8607c-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="8607c-203">Caratteristiche di .NET Framework 4,5:</span><span class="sxs-lookup"><span data-stu-id="8607c-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="8607c-204">.NET Framework 4,5 o 4,6</span><span class="sxs-lookup"><span data-stu-id="8607c-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="8607c-205">Windows Server 2016 </strong> - .net Framework 4,6 è già installato per queste versioni di Windows Server, ma è necessario abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="8607c-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="8607c-206">Windows Server 2012 o Windows Server 2012 R2 </strong> - .net Framework 4,5 è già installato per queste versioni di Windows Server, ma è necessario abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="8607c-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="8607c-207">Windows Server 2008 R2 </strong> - .net Framework 4,5 non è incluso in windows Server 2008 R2, quindi è necessario <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> scaricare Microsoft .NET Framework 4,5 </a> e installarlo separatamente.</span><span class="sxs-lookup"><span data-stu-id="8607c-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8607c-208">Nota</span><span class="sxs-lookup"><span data-stu-id="8607c-208">Note</span></span></strong><br/><p><span data-ttu-id="8607c-209">Se si esegue l'aggiornamento da MBAM 2,0 o MBAM 2,0 SP1 e si vuole installare .NET Framework 4,5, vedere <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> Note sulla versione per mbam 2,5 </a> per un ulteriore passaggio necessario per far funzionare i siti Web.</span><span class="sxs-lookup"><span data-stu-id="8607c-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="8607c-210">Attivazione di WCF</span><span class="sxs-lookup"><span data-stu-id="8607c-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="8607c-211">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="8607c-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="8607c-212">Attivazione non HTTP (solo per Windows Server 2008, 2012 e 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="8607c-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="8607c-213">Attivazione TCP</span><span class="sxs-lookup"><span data-stu-id="8607c-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="8607c-214">Servizio Attivazione processo Windows:</span><span class="sxs-lookup"><span data-stu-id="8607c-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="8607c-215">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="8607c-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="8607c-216">Ambiente .NET Framework</span><span class="sxs-lookup"><span data-stu-id="8607c-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="8607c-217">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="8607c-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="8607c-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="8607c-219">ASP.NET MVC 4 download</span><span class="sxs-lookup"><span data-stu-id="8607c-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-220">Nome dell'entità servizio (SPN)</span><span class="sxs-lookup"><span data-stu-id="8607c-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-221">Le applicazioni Web richiedono un SPN per il nome host virtuale sotto l'account di dominio usato per i pool di applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="8607c-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="8607c-222">Se i diritti amministrativi consentono di creare nomi SPN in servizi di dominio Active Directory, MBAM crea l'SPN per l'utente.</span><span class="sxs-lookup"><span data-stu-id="8607c-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="8607c-223"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Per informazioni sui diritti necessari per la creazione di nomi SPN, vedere Setspn.</span><span class="sxs-lookup"><span data-stu-id="8607c-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="8607c-224">Se non si hanno diritti amministrativi per la creazione di nomi SPN, è necessario chiedere agli amministratori di Active Directory dell'organizzazione di creare l'SPN usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="8607c-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="8607c-225">Nell'esempio di codice il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="8607c-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8607c-226">Nota</span><span class="sxs-lookup"><span data-stu-id="8607c-226">Note</span></span></strong><br/><p><span data-ttu-id="8607c-227">Se si sta configurando il bilanciamento del carico, usare lo stesso account del pool di applicazioni in tutti i server.</span><span class="sxs-lookup"><span data-stu-id="8607c-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8607c-228">Per altre informazioni sulla registrazione di SPN per nomi host completi, NetBIOS e personalizzati, vedere <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> pianificazione di come proteggere i siti Web di mbam </a> .</span><span class="sxs-lookup"><span data-stu-id="8607c-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8607c-229">Prerequisiti per il portale self-service</span><span class="sxs-lookup"><span data-stu-id="8607c-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-230">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-231">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-232">Versione supportata di Windows Server</span><span class="sxs-lookup"><span data-stu-id="8607c-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-233">Vedi <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> MBAM 2,5 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="8607c-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="8607c-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="8607c-235">ASP.NET MVC 4 download</span><span class="sxs-lookup"><span data-stu-id="8607c-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-236">Strumenti di gestione di IIS per servizi Web</span><span class="sxs-lookup"><span data-stu-id="8607c-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-237">Nome dell'entità servizio (SPN)</span><span class="sxs-lookup"><span data-stu-id="8607c-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-238">Le applicazioni Web richiedono un SPN per il nome host virtuale sotto l'account di dominio usato per i pool di applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="8607c-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="8607c-239">Se i diritti amministrativi consentono di creare nomi SPN in servizi di dominio Active Directory, MBAM crea l'SPN per l'utente.</span><span class="sxs-lookup"><span data-stu-id="8607c-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="8607c-240"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> </a> Per informazioni sui diritti necessari per la creazione di nomi SPN, vedere Setspn.</span><span class="sxs-lookup"><span data-stu-id="8607c-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="8607c-241">Se non si hanno diritti amministrativi per la creazione di nomi SPN, è necessario chiedere agli amministratori di Active Directory degli amministratori dell'organizzazione dell'organizzazione di creare l'SPN usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="8607c-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="8607c-242">Nell'esempio di codice il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="8607c-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8607c-243">Nota</span><span class="sxs-lookup"><span data-stu-id="8607c-243">Note</span></span></strong><br/><p><span data-ttu-id="8607c-244">Se si sta configurando il bilanciamento del carico, usare lo stesso account del pool di applicazioni in tutti i server.</span><span class="sxs-lookup"><span data-stu-id="8607c-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8607c-245">Per altre informazioni sulla registrazione di SPN per nomi host completi, NetBIOS e personalizzati, vedere <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> pianificazione di come proteggere i siti Web di mbam </a> .</span><span class="sxs-lookup"><span data-stu-id="8607c-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8607c-246">Prerequisiti per la workstation di gestione</span><span class="sxs-lookup"><span data-stu-id="8607c-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-247">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8607c-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8607c-248">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8607c-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-249">Prima di installare il client MBAM, scaricare i modelli dei criteri di gruppo di MBAM da <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> come ottenere i modelli di criteri di gruppo di MDOP </a> e configurarli con le impostazioni da implementare nella propria organizzazione per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8607c-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8607c-250">Prima di installare il client MBAM, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8607c-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8607c-251">Operazione da eseguire</span><span class="sxs-lookup"><span data-stu-id="8607c-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="8607c-252">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="8607c-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8607c-253">Copiare i modelli dei criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="8607c-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="8607c-254">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8607c-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8607c-255">Modificare le impostazioni dei criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8607c-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="8607c-256">Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8607c-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="8607c-257">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8607c-257">Related topics</span></span>


[<span data-ttu-id="8607c-258">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8607c-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="8607c-259">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8607c-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="8607c-260">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8607c-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="8607c-261">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8607c-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8607c-262">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8607c-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="8607c-263">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8607c-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




