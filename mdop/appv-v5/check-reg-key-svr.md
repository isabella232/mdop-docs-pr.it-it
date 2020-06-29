---
title: Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x
description: Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805931"
---
# <span data-ttu-id="47dc6-103">Controllare le chiavi del Registro di sistema prima di installare il server App-V 5.x</span><span class="sxs-lookup"><span data-stu-id="47dc6-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="47dc6-104">Se si sta aggiornando il pacchetto di hotfix App-v 5,0 SP1 3 o versione successiva, eseguire i passaggi descritti in questa sezione prima di installare il server App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="47dc6-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="47dc6-105">Quando è necessario eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="47dc6-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47dc6-106">Si esegue l'aggiornamento da App-V 5,0 SP1 con i successivi pacchetti di hotfix installati usando un file msp.</span><span class="sxs-lookup"><span data-stu-id="47dc6-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="47dc6-107">Quali componenti richiedono di eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="47dc6-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47dc6-108">Solo i componenti di App-V Server che si stanno aggiornando.</span><span class="sxs-lookup"><span data-stu-id="47dc6-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="47dc6-109">Quando è necessario eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="47dc6-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47dc6-110">Prima di aggiornare l'App-V Server in App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="47dc6-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="47dc6-111">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="47dc6-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="47dc6-112">Usando le informazioni nelle tabelle seguenti, aggiornare ogni valore della chiave del registro <code>HKLM\Software\Microsoft\AppV\Server</code> di sistema in con il valore specificato nell'installazione del server originale.</span><span class="sxs-lookup"><span data-stu-id="47dc6-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="47dc6-113">Il completamento di questo passaggio ripristina i valori del registro di sistema che potrebbero essere stati rimossi quando sono stati installati i pacchetti di hotfix di App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="47dc6-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="47dc6-114">Tasto ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="47dc6-114">ManagementDatabase key</span></span>**

<span data-ttu-id="47dc6-115">Se si sta installando il database di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="47dc6-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47dc6-116">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="47dc6-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="47dc6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47dc6-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="47dc6-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-119">Descrive se è necessario un account di accesso pubblico per accedere ai database di gestione non locali.</span><span class="sxs-lookup"><span data-stu-id="47dc6-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="47dc6-120">Il valore è impostato su "1" se necessario.</span><span class="sxs-lookup"><span data-stu-id="47dc6-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="47dc6-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-122">Nome del database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-124">Account usato per l'accesso in lettura (pubblico) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="47dc6-125">Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="47dc6-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="47dc6-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-127">Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="47dc6-128">Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="47dc6-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="47dc6-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-130">Istanza di SQL Server per il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="47dc6-131">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="47dc6-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-133">Account usato per l'accesso in scrittura (amministratore) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="47dc6-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-135">Identificatore sicuro (SID) dell'account usato per l'accesso in scrittura (amministratore) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-137">Account del computer remoto di Management Server (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="47dc6-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-139">Account di accesso dell'amministratore dell'installazione per il server di gestione (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="47dc6-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="47dc6-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-141">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="47dc6-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="47dc6-142">1 </strong> -il servizio di gestione si trova nel computer locale, ovvero MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</span><span class="sxs-lookup"><span data-stu-id="47dc6-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="47dc6-143">0 </strong> - il servizio di gestione si trova in un computer diverso dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="47dc6-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="47dc6-144">Tasto ManagementService</span><span class="sxs-lookup"><span data-stu-id="47dc6-144">ManagementService key</span></span>**

<span data-ttu-id="47dc6-145">Se si sta installando il server di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="47dc6-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47dc6-146">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="47dc6-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="47dc6-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47dc6-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-149">Gruppo o account Active Directory Domain Services (AD DS) autorizzato a gestire App-V (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="47dc6-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="47dc6-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-151">Istanza di SQL Server che contiene il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="47dc6-152">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="47dc6-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="47dc6-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-154">Nome del server SQL remoto con il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="47dc6-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="47dc6-155">Se il valore è vuoto, viene usato il computer locale.</span><span class="sxs-lookup"><span data-stu-id="47dc6-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="47dc6-156">Tasto ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="47dc6-156">ReportingDatabase key</span></span>**

<span data-ttu-id="47dc6-157">Se si sta installando il database delle relazioni, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="47dc6-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47dc6-158">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="47dc6-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="47dc6-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47dc6-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="47dc6-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-161">Descrive se è necessario un account di accesso pubblico per accedere a database di report non locali.</span><span class="sxs-lookup"><span data-stu-id="47dc6-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="47dc6-162">Il valore è impostato su "1" se necessario.</span><span class="sxs-lookup"><span data-stu-id="47dc6-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="47dc6-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-164">Nome del database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-166">Account usato per l'accesso in lettura (pubblico) al database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="47dc6-167">Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="47dc6-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="47dc6-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-169">Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="47dc6-170">Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="47dc6-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="47dc6-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-172">Istanza di SQL Server per il database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="47dc6-173">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="47dc6-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="47dc6-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-177">Account del computer remoto di Reporting Server (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="47dc6-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="47dc6-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-179">Account di accesso dell'amministratore dell'installazione per il server di report (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="47dc6-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="47dc6-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-181">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="47dc6-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="47dc6-182">1 </strong> -il servizio Reporting si trova nel computer locale, ovvero REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</span><span class="sxs-lookup"><span data-stu-id="47dc6-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="47dc6-183">0 </strong> - il servizio Reporting si trova in un computer diverso dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="47dc6-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="47dc6-184">Tasto ReportingService</span><span class="sxs-lookup"><span data-stu-id="47dc6-184">ReportingService key</span></span>**

<span data-ttu-id="47dc6-185">Se si sta installando il server di Reporting, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="47dc6-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47dc6-186">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="47dc6-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="47dc6-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47dc6-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47dc6-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="47dc6-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-189">Istanza di SQL Server per il database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="47dc6-190">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="47dc6-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47dc6-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="47dc6-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="47dc6-192">Nome del server SQL remoto con il database di report.</span><span class="sxs-lookup"><span data-stu-id="47dc6-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="47dc6-193">Se il valore è vuoto, viene usato il computer locale.</span><span class="sxs-lookup"><span data-stu-id="47dc6-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

