---
title: Prerequisiti per la distribuzione di MBAM 1.0
description: Prerequisiti per la distribuzione di MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822665"
---
# <span data-ttu-id="c19fa-103">Prerequisiti per la distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c19fa-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="c19fa-104">Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di soddisfare i prerequisiti necessari per installare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="c19fa-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="c19fa-105">Questa sezione contiene informazioni utili per preparare correttamente l'ambiente di elaborazione prima di distribuire i client e le funzionalità del server di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c19fa-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="c19fa-106">Prerequisiti di installazione per le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="c19fa-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="c19fa-107">Ogni funzionalità di MBAM Server include prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente.</span><span class="sxs-lookup"><span data-stu-id="c19fa-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="c19fa-108">MBAM setup verifica se tutti i prerequisiti vengono soddisfatti prima che l'installazione venga avviata.</span><span class="sxs-lookup"><span data-stu-id="c19fa-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="c19fa-109">Prerequisiti di installazione per l'amministrazione e il server di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c19fa-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="c19fa-110">La tabella seguente contiene i prerequisiti di installazione per l'amministrazione e il server di monitoraggio di MBAM:</span><span class="sxs-lookup"><span data-stu-id="c19fa-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c19fa-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c19fa-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="c19fa-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c19fa-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c19fa-113">Ruolo del server di Windows ServerWeb</span><span class="sxs-lookup"><span data-stu-id="c19fa-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c19fa-114">Questo ruolo deve essere aggiunto a un sistema operativo server supportato per la funzionalità mbam Administration e Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="c19fa-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c19fa-115">Strumenti di gestione di Web Server (IIS)</span><span class="sxs-lookup"><span data-stu-id="c19fa-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c19fa-116">Script e strumenti di gestione di IIS</span><span class="sxs-lookup"><span data-stu-id="c19fa-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c19fa-117">Servizi ruolo server Web</span><span class="sxs-lookup"><span data-stu-id="c19fa-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c19fa-118">Caratteristiche HTTP comuni:</span><span class="sxs-lookup"><span data-stu-id="c19fa-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c19fa-119">Contenuto statico</span><span class="sxs-lookup"><span data-stu-id="c19fa-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="c19fa-120">Documento predefinito</span><span class="sxs-lookup"><span data-stu-id="c19fa-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c19fa-121">Sviluppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="c19fa-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c19fa-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c19fa-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="c19fa-123">Estensibilità .NET</span><span class="sxs-lookup"><span data-stu-id="c19fa-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="c19fa-124">Estensioni ISAPI</span><span class="sxs-lookup"><span data-stu-id="c19fa-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="c19fa-125">Filtri ISAPI</span><span class="sxs-lookup"><span data-stu-id="c19fa-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c19fa-126">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="c19fa-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c19fa-127">Autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="c19fa-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="c19fa-128">Filtro delle richieste</span><span class="sxs-lookup"><span data-stu-id="c19fa-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c19fa-129">Caratteristiche di Windows Server</span><span class="sxs-lookup"><span data-stu-id="c19fa-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c19fa-130">Caratteristiche di Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="c19fa-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c19fa-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="c19fa-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="c19fa-132">Attivazione di WCF</span><span class="sxs-lookup"><span data-stu-id="c19fa-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="c19fa-133">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="c19fa-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="c19fa-134">Attivazione non HTTP</span><span class="sxs-lookup"><span data-stu-id="c19fa-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="c19fa-135">Servizio Attivazione dei processi Windows</span><span class="sxs-lookup"><span data-stu-id="c19fa-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c19fa-136">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="c19fa-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="c19fa-137">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="c19fa-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="c19fa-138">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="c19fa-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c19fa-139">**Nota**  Per un elenco dei sistemi operativi supportati, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c19fa-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="c19fa-140">Prerequisiti di installazione per i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="c19fa-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="c19fa-141">I report di conformità e controllo devono essere installati in una versione supportata di SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c19fa-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="c19fa-142">I prerequisiti di installazione per questa funzionalità includono SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="c19fa-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="c19fa-143">SSRS deve essere installato ed eseguito durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="c19fa-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="c19fa-144">La funzione SSRS deve essere configurata anche in modalità "nativa", non nella modalità "non configurata" o "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="c19fa-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="c19fa-145">**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c19fa-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="c19fa-146">Prerequisiti di installazione per il database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="c19fa-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="c19fa-147">Il database di ripristino e hardware deve essere installato in una versione supportata di SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c19fa-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="c19fa-148">SQL Server deve avere installato ed eseguito i servizi motore di database durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="c19fa-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="c19fa-149">È necessario abilitare la caratteristica Transparent Data Encryption.</span><span class="sxs-lookup"><span data-stu-id="c19fa-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="c19fa-150">**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c19fa-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="c19fa-151">La caratteristica di Transcript SQLServer consente di eseguire la crittografia di input/output (I/O) in tempo reale dei file di dati e di log.</span><span class="sxs-lookup"><span data-stu-id="c19fa-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="c19fa-152">Transparent protegge i dati "a riposo", che includono i dati e i file di log.</span><span class="sxs-lookup"><span data-stu-id="c19fa-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="c19fa-153">Offre la possibilità di rispettare numerose leggi, normative e linee guida stabilite in diversi settori.</span><span class="sxs-lookup"><span data-stu-id="c19fa-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="c19fa-154">**Nota**  Dato che la crittografia in tempo reale viene eseguita per la decrittazione delle informazioni sul database, le informazioni sulla chiave di ripristino saranno visibili se l'account in cui è stato effettuato l'accesso dispone delle autorizzazioni per il database quando si visualizzano le tabelle SQL delle informazioni chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c19fa-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="c19fa-155">Prerequisiti di installazione per il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="c19fa-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="c19fa-156">Il database di conformità e controllo deve essere installato in una versione supportata di SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c19fa-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="c19fa-157">In SQL Server devono essere installati e eseguiti i servizi motore di database durante l'installazione di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="c19fa-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="c19fa-158">**Nota**  Per un elenco dei sistemi operativi supportati e delle versioni di SQLServer, Vedi le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c19fa-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="c19fa-159">Prerequisiti di installazione per i client MBAM</span><span class="sxs-lookup"><span data-stu-id="c19fa-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="c19fa-160">I prerequisiti necessari che è necessario soddisfare prima di iniziare l'installazione del client MBAM sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c19fa-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="c19fa-161">Funzionalità TPM (Trusted Platform Module) v 1.2</span><span class="sxs-lookup"><span data-stu-id="c19fa-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="c19fa-162">Il chip TPM deve essere attivato nel BIOS e deve essere ripristinato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c19fa-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="c19fa-163">Per altre informazioni, vedere la documentazione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="c19fa-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="c19fa-164">**Avviso**  Verificare che la tastiera, il mouse e il video siano collegati direttamente al computer, anziché a un interruttore di tastiera, video, mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="c19fa-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="c19fa-165">Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="c19fa-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="c19fa-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c19fa-166">Related topics</span></span>


[<span data-ttu-id="c19fa-167">Pianificazione della distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c19fa-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="c19fa-168">Configurazioni supportate di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c19fa-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





