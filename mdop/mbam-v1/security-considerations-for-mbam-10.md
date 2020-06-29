---
title: Considerazioni sulla sicurezza per MBAM 1.0
description: Considerazioni sulla sicurezza per MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826195"
---
# <span data-ttu-id="1a9a3-103">Considerazioni sulla sicurezza per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1a9a3-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="1a9a3-104">Questo argomento contiene una breve panoramica degli account e dei gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1a9a3-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="1a9a3-105">Per altre informazioni, seguire i collegamenti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="1a9a3-106">Considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="1a9a3-106">General security considerations</span></span>


**<span data-ttu-id="1a9a3-107">Comprendere i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-107">Understand the security risks.</span></span>** <span data-ttu-id="1a9a3-108">Il rischio più grave per MBAM è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="1a9a3-109">Tuttavia, la perdita delle funzionalità di MBAM per un breve periodo di tempo a causa di un attacco di tipo Denial of Service non avrebbe in genere un impatto catastrofico.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="1a9a3-110">**Proteggere fisicamente i computer**.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-110">**Physically secure your computers**.</span></span> <span data-ttu-id="1a9a3-111">La sicurezza è incompleta senza sicurezza fisica.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="1a9a3-112">Chiunque abbia accesso fisico a un server MBAM potrebbe potenzialmente attaccare l'intera base client.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="1a9a3-113">Eventuali attacchi fisici potenziali devono essere considerati ad alto rischio e mitigati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="1a9a3-114">I server MBAM devono essere archiviati in una sala server fisicamente sicura con accesso controllato.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="1a9a3-115">Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="1a9a3-116">**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="1a9a3-117">Tieniti aggiornato sui nuovi aggiornamenti per i sistemi operativi, Microsoft SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/p/?LinkId=28819> .</span><span class="sxs-lookup"><span data-stu-id="1a9a3-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="1a9a3-118">**Usare password complesse o passare frasi**.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="1a9a3-119">Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM e MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="1a9a3-120">Non usare mai password vuote.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-120">Never use blank passwords.</span></span> <span data-ttu-id="1a9a3-121">Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="1a9a3-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="1a9a3-122">Account e gruppi in MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="1a9a3-123">Una procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="1a9a3-124">Quindi, Aggiungi gli account globali di dominio ai gruppi di MBAM locali necessari nei server MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="1a9a3-125">Gruppi di ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="1a9a3-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="1a9a3-126">Nessun gruppo viene creato automaticamente durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="1a9a3-127">Devi tuttavia creare i seguenti gruppi globali di ActiveDirectoryDomainServices per gestire le operazioni di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1a9a3-128">Nome del gruppo</span><span class="sxs-lookup"><span data-stu-id="1a9a3-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="1a9a3-129">Dettagli</span><span class="sxs-lookup"><span data-stu-id="1a9a3-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-130">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="1a9a3-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-131">Crea questo gruppo per gestire i membri del gruppo locale degli utenti di MBAM Advanced helpdesk che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-132">Controllo di conformità MBAM per l'accesso DB</span><span class="sxs-lookup"><span data-stu-id="1a9a3-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-133">Creare questo gruppo per gestire i membri del gruppo di controllo della conformità MBAM di DB Access che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-134">Utenti di hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-135">Creare questo gruppo per gestire i membri del gruppo di utenti hardware MBAM che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-136">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="1a9a3-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-137">Creare questo gruppo per gestire i membri del gruppo di utenti di MBAM helpdesk locale creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-138">Accesso di MBAM e DB hardware</span><span class="sxs-lookup"><span data-stu-id="1a9a3-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-139">Crea questo gruppo per gestire i membri del gruppo locale per il recupero e il ripristino di MBAM e l'hardware che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-140">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-141">Creare questo gruppo per gestire i membri del gruppo di utenti del report MBAM che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-142">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-143">Crea questo gruppo per gestire i membri del gruppo di amministratori di sistema MBAM che è stato creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-144">Esenzioni crittografiche di BitLocker</span><span class="sxs-lookup"><span data-stu-id="1a9a3-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-145">Creare questo gruppo per gestire gli account utente che devono essere esentati dalla crittografia BitLocker a partire da computer a cui accedono.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1a9a3-146">Gruppi locali di MBAM server</span><span class="sxs-lookup"><span data-stu-id="1a9a3-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="1a9a3-147">MBAM setup crea gruppi locali per supportare le operazioni di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="1a9a3-148">Dovresti aggiungere i gruppi globali di ActiveDirectoryDomainServices ai gruppi locali di MBAM appropriati per configurare le autorizzazioni di sicurezza e accesso ai dati di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1a9a3-149">Nome del gruppo</span><span class="sxs-lookup"><span data-stu-id="1a9a3-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="1a9a3-150">Dettagli</span><span class="sxs-lookup"><span data-stu-id="1a9a3-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-151">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="1a9a3-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-152">I membri di questo gruppo hanno esteso l'accesso alle funzionalità dell'helpdesk di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-153">Controllo di conformità MBAM per l'accesso DB</span><span class="sxs-lookup"><span data-stu-id="1a9a3-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-154">Questo gruppo contiene i computer che hanno accesso al database di controllo di conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-155">Utenti di hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-156">I membri di questo gruppo hanno accesso ad alcune delle funzionalità di funzionalità hardware dell'amministrazione e del monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-157">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="1a9a3-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-158">I membri di questo gruppo hanno accesso ad alcune delle funzionalità dell'helpdesk dall'amministrazione e dal monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-159">Accesso di MBAM e DB hardware</span><span class="sxs-lookup"><span data-stu-id="1a9a3-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-160">Questo gruppo contiene i computer che hanno accesso al database di MBAM Recovery e hardware.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1a9a3-161">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-162">I membri di questo gruppo hanno accesso ai report di conformità e controllo dall'amministrazione e dal monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1a9a3-163">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="1a9a3-164">I membri di questo gruppo hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1a9a3-165">Account di accesso di report SSRS</span><span class="sxs-lookup"><span data-stu-id="1a9a3-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="1a9a3-166">L'account del servizio report di SQL Server Reporting Services (SSRS) fornisce il contesto di sicurezza per l'esecuzione dei report di MBAM disponibili tramite SSRS.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="1a9a3-167">Questo account è configurato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="1a9a3-168">File di log di MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-168">MBAM Log Files</span></span>


<span data-ttu-id="1a9a3-169">Durante la configurazione di MBAM, i seguenti file di log di configurazione di MBAM vengono creati nella cartella% Temp% dell'utente che installa il</span><span class="sxs-lookup"><span data-stu-id="1a9a3-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="1a9a3-170">File di log configurazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="1a9a3-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="1a9a3-171">MSI <em> &lt; Five random characters &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="1a9a3-172">Registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="1a9a3-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="1a9a3-174">Registra le azioni intraprese per creare la configurazione del database di stato di conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="1a9a3-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="1a9a3-176">Registra le azioni intraprese per creare il database di ripristino e hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="1a9a3-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="1a9a3-178">Registra le azioni intraprese per creare gli account di accesso di SQL Server nel database di stato della conformità di MBAM e autorizzare il servizio Web Helpdesk nel database per i report.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="1a9a3-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="1a9a3-180">Registra le azioni intraprese per autorizzare i servizi Web al database per il ripristino delle chiavi e creare gli account di accesso al database hardware e ripristino di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="1a9a3-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="1a9a3-182">Registra le azioni intraprese per autorizzare i servizi Web al database di stato di conformità MBAM per la creazione di report di conformità.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="1a9a3-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="1a9a3-184">Registra le azioni intraprese per autorizzare servizi Web per il ripristino di MBAM e il database hardware per il ripristino della chiave.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="1a9a3-185">**Nota**  Per ottenere altri file di log della configurazione di MBAM, è necessario installare l'amministrazione e il monitoraggio di Microsoft BitLocker tramite il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="1a9a3-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="1a9a3-186">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="1a9a3-187">File di log della configurazione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="1a9a3-188">MSI <em> &lt; Five random characters &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="1a9a3-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="1a9a3-189">Registra le azioni intraprese durante l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="1a9a3-190">Considerazioni su dati di database di MBAM</span><span class="sxs-lookup"><span data-stu-id="1a9a3-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="1a9a3-191">La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server 2008 è un requisito necessario per l'installazione delle istanze di database che ospiteranno le caratteristiche del database MBAM.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="1a9a3-192">Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="1a9a3-193">Transparent è una scelta adatta per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="1a9a3-194">Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker, entrambi i quali crittografano anche i dati nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="1a9a3-195">Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="1a9a3-196">Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="1a9a3-197">È quindi necessario prestare particolare attenzione per garantire che il certificato usato per proteggere la chiave di crittografia del database (decifratore) sia supportato e mantenuto con il backup del database.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="1a9a3-198">Senza un certificato, i dati saranno illeggibili.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="1a9a3-199">Eseguire il backup del certificato insieme al database.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="1a9a3-200">Ogni backup del certificato deve avere due file; entrambi i file devono essere archiviati. È consigliabile archiviarli separatamente dal file di backup del database per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a9a3-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="1a9a3-201">Per un esempio di come abilitare le istanze di Transparent per il database MBAM, vedere [valutazione di mbam 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="1a9a3-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="1a9a3-202">Per altre informazioni su Transparent in SQLServer 2008, vedere [crittografia di database in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="1a9a3-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="1a9a3-203">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a9a3-203">Related topics</span></span>


[<span data-ttu-id="1a9a3-204">Sicurezza e privacy per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1a9a3-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





