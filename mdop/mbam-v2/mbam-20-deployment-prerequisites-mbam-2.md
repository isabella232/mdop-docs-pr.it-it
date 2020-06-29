---
title: Prerequisiti per la distribuzione di MBAM 2.0
description: Prerequisiti per la distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826015"
---
# <span data-ttu-id="a2c43-103">Prerequisiti per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a2c43-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="a2c43-104">Prima di avviare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), è necessario assicurarsi di avere soddisfatto i prerequisiti per installare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="a2c43-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="a2c43-105">Questa sezione contiene informazioni utili per pianificare correttamente l'ambiente di elaborazione prima di distribuire le funzionalità e i client del server di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2c43-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="a2c43-106">Se si sta installando MBAM con Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) per i prerequisiti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="a2c43-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="a2c43-107">Prerequisiti di installazione per le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="a2c43-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="a2c43-108">Ogni funzionalità di MBAM Server include prerequisiti specifici che devono essere soddisfatti prima che le funzionalità di MBAM possano essere installate correttamente.</span><span class="sxs-lookup"><span data-stu-id="a2c43-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="a2c43-109">La configurazione di MBAM controlla che tutti i prerequisiti vengano soddisfatti prima che l'installazione venga avviata.</span><span class="sxs-lookup"><span data-stu-id="a2c43-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="a2c43-110">Prerequisiti per l'amministrazione e il server di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="a2c43-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a2c43-113">Ruolo di Windows Server Web Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a2c43-114">Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità di amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="a2c43-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a2c43-115">Strumenti di gestione di Web Server (IIS)</span><span class="sxs-lookup"><span data-stu-id="a2c43-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a2c43-116">Selezionare <strong> script e strumenti di gestione di IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="a2c43-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a2c43-117">Certificato SSL</span><span class="sxs-lookup"><span data-stu-id="a2c43-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a2c43-118">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a2c43-118">Optional.</span></span> <span data-ttu-id="a2c43-119">Per proteggere le comunicazioni tra i client e i servizi Web, è necessario ottenere e installare un certificato firmato da un'autorità di sicurezza attendibile.</span><span class="sxs-lookup"><span data-stu-id="a2c43-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a2c43-120">Servizi ruolo server Web</span><span class="sxs-lookup"><span data-stu-id="a2c43-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a2c43-121">Caratteristiche HTTP comuni:</span><span class="sxs-lookup"><span data-stu-id="a2c43-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a2c43-122">Contenuto statico</span><span class="sxs-lookup"><span data-stu-id="a2c43-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="a2c43-123">Documento predefinito</span><span class="sxs-lookup"><span data-stu-id="a2c43-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="a2c43-124">Sviluppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="a2c43-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a2c43-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="a2c43-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="a2c43-126">Estensibilità .NET</span><span class="sxs-lookup"><span data-stu-id="a2c43-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="a2c43-127">Estensioni ISAPI</span><span class="sxs-lookup"><span data-stu-id="a2c43-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="a2c43-128">Filtri ISAPI</span><span class="sxs-lookup"><span data-stu-id="a2c43-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="a2c43-129">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="a2c43-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a2c43-130">Autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="a2c43-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="a2c43-131">Filtro delle richieste</span><span class="sxs-lookup"><span data-stu-id="a2c43-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a2c43-132">Caratteristiche di Windows Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a2c43-133">Caratteristiche di .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="a2c43-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a2c43-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="a2c43-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="a2c43-135">Attivazione di WCF</span><span class="sxs-lookup"><span data-stu-id="a2c43-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-136">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="a2c43-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="a2c43-137">Attivazione non HTTP</span><span class="sxs-lookup"><span data-stu-id="a2c43-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="a2c43-138">Servizio Attivazione processo Windows:</span><span class="sxs-lookup"><span data-stu-id="a2c43-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a2c43-139">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="a2c43-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="a2c43-140">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="a2c43-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="a2c43-141">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="a2c43-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a2c43-142">Nota</span><span class="sxs-lookup"><span data-stu-id="a2c43-142">Note</span></span>**  
<span data-ttu-id="a2c43-143">Per un elenco dei sistemi operativi supportati, Vedi le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a2c43-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="a2c43-144">Prerequisiti per i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="a2c43-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-145">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-146">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-147">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="a2c43-148">Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a2c43-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-149">Installare SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="a2c43-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-150">SQL_Latin1_General_CP1_CI_AS regole di confronto</span><span class="sxs-lookup"><span data-stu-id="a2c43-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-151">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="a2c43-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-152">Diritti delle istanze di SSRS: necessari per l'installazione di report solo se si stanno installando database in un server separato dai report.</span><span class="sxs-lookup"><span data-stu-id="a2c43-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-153">Diritti di istanza obbligatori:</span><span class="sxs-lookup"><span data-stu-id="a2c43-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-154">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="a2c43-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="a2c43-155">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="a2c43-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="a2c43-156">SSRS deve essere installato ed eseguito durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="a2c43-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="a2c43-157">Configurare SSRS in modalità "nativa" e non in modalità non configurata o "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="a2c43-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a2c43-158">Prerequisiti per il database di ripristino</span><span class="sxs-lookup"><span data-stu-id="a2c43-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-159">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-160">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-161">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="a2c43-162">Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a2c43-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-163">Installare SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="a2c43-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-164">SQL_Latin1_General_CP1_CI_AS regole di confronto</span><span class="sxs-lookup"><span data-stu-id="a2c43-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="a2c43-165">Strumenti di gestione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-166">Autorizzazioni di SQL Server obbligatorie</span><span class="sxs-lookup"><span data-stu-id="a2c43-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-167">Autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="a2c43-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-168">Ruoli del server di accesso alle istanze SQL:</span><span class="sxs-lookup"><span data-stu-id="a2c43-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="a2c43-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="a2c43-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="a2c43-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="a2c43-171">Diritti di istanza di SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="a2c43-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-172">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="a2c43-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="a2c43-173">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="a2c43-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-174">Funzionalità di crittografia dei dati trasparente facoltativa-install disponibile in SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-175">La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare numerose leggi, normative e linee guida stabilite in diversi settori.</span><span class="sxs-lookup"><span data-stu-id="a2c43-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2c43-176">Nota</span><span class="sxs-lookup"><span data-stu-id="a2c43-176">Note</span></span></strong><br/><p><span data-ttu-id="a2c43-177">Transparent esegue la decrittografia in tempo reale delle informazioni sul database, il che significa che, se l'account in cui è stato effettuato l'accesso ha le autorizzazioni per il database mentre si visualizzano le informazioni chiave di ripristino nelle tabelle di SQL Server, le informazioni sulla chiave di ripristino sono visibili.</span><span class="sxs-lookup"><span data-stu-id="a2c43-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a2c43-178">Altre informazioni su Transparence: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerazioni sulla sicurezza </a> .</span><span class="sxs-lookup"><span data-stu-id="a2c43-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a2c43-179">Prerequisiti per il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="a2c43-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-180">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-181">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-182">Versione supportata di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="a2c43-183">Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a2c43-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-184">Installare SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="a2c43-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-185">SQL_Latin1_General_CP1_CI_AS regole di confronto</span><span class="sxs-lookup"><span data-stu-id="a2c43-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="a2c43-186">Strumenti di gestione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-187">Autorizzazioni di SQL Server obbligatorie</span><span class="sxs-lookup"><span data-stu-id="a2c43-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-188">Autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="a2c43-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-189">Ruoli del server di accesso alle istanze SQL:</span><span class="sxs-lookup"><span data-stu-id="a2c43-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="a2c43-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="a2c43-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="a2c43-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="a2c43-192">Diritti di istanza di SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="a2c43-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-193">Creare cartelle</span><span class="sxs-lookup"><span data-stu-id="a2c43-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="a2c43-194">Pubblicare report</span><span class="sxs-lookup"><span data-stu-id="a2c43-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-195">Opzione-install Transparent Data Encryption (facoltativa) in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2c43-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-196">La funzionalità SQL Server di transcription esegue la crittografia di I/O in tempo reale e la decrittografia dei file di dati e di log, che possono aiutarti a rispettare numerose leggi, normative e linee guida stabilite in diversi settori.</span><span class="sxs-lookup"><span data-stu-id="a2c43-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2c43-197">Nota</span><span class="sxs-lookup"><span data-stu-id="a2c43-197">Note</span></span></strong><br/><p><span data-ttu-id="a2c43-198">Transparent esegue la decrittografia in tempo reale delle informazioni sul database, il che significa che, se l'account in cui è stato effettuato l'accesso ha le autorizzazioni per il database mentre si visualizzano le informazioni chiave di ripristino nelle tabelle di SQL Server, le informazioni sulla chiave di ripristino sono visibili.</span><span class="sxs-lookup"><span data-stu-id="a2c43-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a2c43-199">Altre informazioni su Transparent: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerazioni sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="a2c43-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-200">In SQL Server devono essere installati e eseguiti i servizi motore di database durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="a2c43-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-201">Il servizio SQL Server Agent deve essere in funzione e impostato su avvio automatico nelle istanze selezionate di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2c43-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a2c43-202">Prerequisiti per il portale self-service</span><span class="sxs-lookup"><span data-stu-id="a2c43-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-203">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-204">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-205">Versione supportata di Windows Server</span><span class="sxs-lookup"><span data-stu-id="a2c43-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="a2c43-206">Vedi <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> MBAM 2,0 configurazioni supportate </a> per le versioni supportate.</span><span class="sxs-lookup"><span data-stu-id="a2c43-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="a2c43-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="a2c43-208">Download di ASP.NET MVC 2</span><span class="sxs-lookup"><span data-stu-id="a2c43-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2c43-209">Strumenti di gestione di IIS per servizi Web</span><span class="sxs-lookup"><span data-stu-id="a2c43-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a2c43-210">Prerequisiti per i client MBAM</span><span class="sxs-lookup"><span data-stu-id="a2c43-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2c43-211">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a2c43-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a2c43-212">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a2c43-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a2c43-213">I client Windows 7 </strong> - devono avere solo funzionalità Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="a2c43-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-214">La versione TPM deve essere 1,2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a2c43-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2c43-215">Il chip TPM deve essere attivato nel BIOS e può essere ripristinato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a2c43-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2c43-216">Per altre informazioni, vedere la documentazione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="a2c43-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a2c43-217">Solo client Windows 8 </strong> : per avere mbam Store e gestire le chiavi di ripristino del TPM: il provisioning automatico TPM deve essere disattivato e mbam deve essere impostato come proprietario del TPM prima di distribuire mbam.</span><span class="sxs-lookup"><span data-stu-id="a2c43-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="a2c43-218">Per disattivare il provisioning automatico TPM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="a2c43-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="a2c43-219">Il provisioning automatico TPM deve essere disattivato.</span><span class="sxs-lookup"><span data-stu-id="a2c43-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="a2c43-220">MBAM deve essere impostato come proprietario del TPM prima di distribuire MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2c43-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a2c43-221">Per disattivare il provisioning automatico TPM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="a2c43-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a2c43-222">Nota</span><span class="sxs-lookup"><span data-stu-id="a2c43-222">Note</span></span></strong><br/><p><span data-ttu-id="a2c43-223">Verificare che la tastiera, il video o il mouse siano direttamente connessi e non gestiti tramite una tastiera, un video o un interruttore del mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="a2c43-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="a2c43-224">Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="a2c43-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a2c43-225">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2c43-225">Related topics</span></span>


[<span data-ttu-id="a2c43-226">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a2c43-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="a2c43-227">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a2c43-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









