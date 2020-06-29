---
title: Considerazioni sulla sicurezza per MBAM 2.0
description: Considerazioni sulla sicurezza per MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823915"
---
# <span data-ttu-id="6b486-103">Considerazioni sulla sicurezza per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6b486-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="6b486-104">Questo argomento contiene una breve panoramica sugli account e i gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="6b486-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="6b486-105">Per altre informazioni, seguire i collegamenti contenuti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="6b486-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="6b486-106">Considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="6b486-106">General Security Considerations</span></span>


**<span data-ttu-id="6b486-107">Comprendere i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6b486-107">Understand the security risks.</span></span>** <span data-ttu-id="6b486-108">Il rischio più grave per l'amministrazione e il monitoraggio di Microsoft BitLocker è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="6b486-109">Tuttavia, la perdita di funzionalità di MBAM per un breve periodo di tempo, a causa di un attacco di tipo Denial of Service, in genere non ha un impatto catastrofico, a differenza, ad esempio, posta elettronica, comunicazioni di rete, luce e alimentazione.</span><span class="sxs-lookup"><span data-stu-id="6b486-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="6b486-110">**Proteggere fisicamente i computer**.</span><span class="sxs-lookup"><span data-stu-id="6b486-110">**Physically secure your computers**.</span></span> <span data-ttu-id="6b486-111">Non c'è sicurezza senza sicurezza fisica.</span><span class="sxs-lookup"><span data-stu-id="6b486-111">There is no security without physical security.</span></span> <span data-ttu-id="6b486-112">Un utente malintenzionato che ottiene l'accesso fisico a un server MBAM può potenzialmente usarlo per attaccare l'intera base client.</span><span class="sxs-lookup"><span data-stu-id="6b486-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="6b486-113">Tutti i potenziali attacchi fisici devono essere considerati ad alto rischio e mitigati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="6b486-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="6b486-114">I server MBAM devono essere archiviati in una sala server sicura con accesso controllato.</span><span class="sxs-lookup"><span data-stu-id="6b486-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="6b486-115">Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.</span><span class="sxs-lookup"><span data-stu-id="6b486-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="6b486-116">**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**.</span><span class="sxs-lookup"><span data-stu-id="6b486-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="6b486-117">Tieniti aggiornato sui nuovi aggiornamenti per i sistemi operativi, Microsoft SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/?LinkId=28819> .</span><span class="sxs-lookup"><span data-stu-id="6b486-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="6b486-118">**Usare password complesse o passare frasi**.</span><span class="sxs-lookup"><span data-stu-id="6b486-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="6b486-119">Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM e MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="6b486-120">Non usare mai password vuote.</span><span class="sxs-lookup"><span data-stu-id="6b486-120">Never use blank passwords.</span></span> <span data-ttu-id="6b486-121">Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="6b486-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="6b486-122">Account e gruppi in MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="6b486-123">La procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente.</span><span class="sxs-lookup"><span data-stu-id="6b486-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="6b486-124">Quindi, Aggiungi gli account globali di dominio ai gruppi di MBAM locali necessari nei server MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="6b486-125">Gruppi di ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="6b486-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="6b486-126">Nessun gruppo di Active Directory viene creato automaticamente durante il processo di configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="6b486-127">Tuttavia, è consigliabile creare i gruppi globali di ActiveDirectoryDomainServices seguenti per gestire le operazioni di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b486-128">Nome del gruppo</span><span class="sxs-lookup"><span data-stu-id="6b486-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6b486-129">Dettagli</span><span class="sxs-lookup"><span data-stu-id="6b486-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-130">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="6b486-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-131">Creare questo gruppo per gestire i membri del gruppo locale degli utenti di MBAM Advanced helpdesk creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-132">Controllo di conformità MBAM per l'accesso DB</span><span class="sxs-lookup"><span data-stu-id="6b486-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-133">Creare questo gruppo per gestire i membri del gruppo di controllo della conformità di MBAM DB Access locale creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-134">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="6b486-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-135">Creare questo gruppo per gestire i membri del gruppo di utenti di MBAM helpdesk locale creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-136">Accesso di MBAM e DB hardware</span><span class="sxs-lookup"><span data-stu-id="6b486-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-137">Crea questo gruppo per gestire i membri del gruppo locale per il recupero e il ripristino di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-138">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-139">Creare questo gruppo per gestire i membri del gruppo di utenti del report MBAM creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-140">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-141">Creare questo gruppo per gestire i membri del gruppo di amministratori di sistema MBAM creato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-142">Esenzioni crittografiche di BitLocker</span><span class="sxs-lookup"><span data-stu-id="6b486-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-143">Creare questo gruppo per gestire gli account utente che devono essere esentati dalla crittografia BitLocker a partire da computer a cui accedono.</span><span class="sxs-lookup"><span data-stu-id="6b486-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="6b486-144">Gruppi locali di MBAM server</span><span class="sxs-lookup"><span data-stu-id="6b486-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="6b486-145">MBAM setup crea gruppi locali per supportare le operazioni di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="6b486-146">Dovresti aggiungere i gruppi globali di ActiveDirectoryDomainServices ai gruppi locali di MBAM appropriati per configurare le autorizzazioni di sicurezza e accesso ai dati di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b486-147">Nome del gruppo</span><span class="sxs-lookup"><span data-stu-id="6b486-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="6b486-148">Dettagli</span><span class="sxs-lookup"><span data-stu-id="6b486-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-149">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="6b486-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-150">I membri di questo gruppo hanno aumentato l'accesso alle funzionalità dell'help desk di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-151">Controllo di conformità MBAM per l'accesso DB</span><span class="sxs-lookup"><span data-stu-id="6b486-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-152">Contiene i computer che hanno accesso al database di controllo e conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-153">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="6b486-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-154">I membri di questo gruppo hanno accesso ad alcune delle funzionalità dell'help desk di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-155">Accesso di MBAM e DB hardware</span><span class="sxs-lookup"><span data-stu-id="6b486-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-156">Contiene i computer che hanno accesso al database di ripristino di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b486-157">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-158">I membri di questo gruppo hanno accesso ai report di conformità e controllo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b486-159">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b486-160">I membri di questo gruppo hanno accesso a tutte le caratteristiche di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6b486-161">Account del servizio report SSRS</span><span class="sxs-lookup"><span data-stu-id="6b486-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="6b486-162">L'account del servizio report SSRS fornisce il contesto di sicurezza per l'esecuzione dei report di MBAM disponibili tramite SSRS.</span><span class="sxs-lookup"><span data-stu-id="6b486-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="6b486-163">È configurato durante la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="6b486-164">Quando si configura l'account del servizio report SSRS, specificare un account utente di dominio e configurare la password per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="6b486-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="6b486-165">**Nota**  Se si modifica il nome dell'account del servizio dopo la distribuzione di MBAM, è necessario riconfigurare l'origine dati dei report per usare le nuove credenziali dell'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="6b486-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="6b486-166">In caso contrario, non sarà possibile accedere al portale help desk.</span><span class="sxs-lookup"><span data-stu-id="6b486-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="6b486-167">File di log di MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-167">MBAM Log Files</span></span>


<span data-ttu-id="6b486-168">I file di log di configurazione di MBAM seguenti vengono creati nella cartella% Temp% dell'utente di installazione durante l'installazione di MBAM:</span><span class="sxs-lookup"><span data-stu-id="6b486-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="6b486-169">File di log configurazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="6b486-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6b486-170">MSI <em> &lt; Five random characters &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6b486-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6b486-171">Registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server.</span><span class="sxs-lookup"><span data-stu-id="6b486-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="6b486-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6b486-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="6b486-173">Registra le azioni intraprese per creare la conformità MBAM e la configurazione del database di audit.</span><span class="sxs-lookup"><span data-stu-id="6b486-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="6b486-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="6b486-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="6b486-175">Registra le azioni intraprese per creare il database di ripristino MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="6b486-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="6b486-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="6b486-177">Registra le azioni intraprese per creare gli account di accesso di SQL Server nel database di controllo e conformità di MBAM e autorizzare il servizio Web HelpDesk nel database per i report.</span><span class="sxs-lookup"><span data-stu-id="6b486-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="6b486-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6b486-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="6b486-179">Registra le azioni intraprese per autorizzare i servizi Web al database per il ripristino delle chiavi e creare account di accesso al database di ripristino MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="6b486-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6b486-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="6b486-181">Registra le azioni intraprese per autorizzare i servizi Web a eseguire MBAM compliance e database di audit per i report di conformità.</span><span class="sxs-lookup"><span data-stu-id="6b486-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="6b486-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="6b486-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="6b486-183">Registra le azioni adottate per autorizzare i servizi Web al database di ripristino di MBAM per il ripristino della chiave.</span><span class="sxs-lookup"><span data-stu-id="6b486-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="6b486-184">**Nota**  Per ottenere ulteriori file di log di MBAM Setup, è necessario installare MBAM usando il pacchetto msiexec e l' &lt; opzione di posizione/l &gt; .</span><span class="sxs-lookup"><span data-stu-id="6b486-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="6b486-185">I file di log vengono creati nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="6b486-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="6b486-186">File di log della configurazione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="6b486-187">MSI <em> &lt; Five random characters &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="6b486-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="6b486-188">Registra le azioni intraprese durante l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="6b486-189">Considerazioni su dati di database di MBAM</span><span class="sxs-lookup"><span data-stu-id="6b486-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="6b486-190">La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server è un'installazione facoltativa per le istanze di database che ospitano le caratteristiche del database MBAM.</span><span class="sxs-lookup"><span data-stu-id="6b486-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="6b486-191">Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="6b486-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="6b486-192">Transparent è la scelta ottimale per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa.</span><span class="sxs-lookup"><span data-stu-id="6b486-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="6b486-193">Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker, entrambi i quali crittografano anche i dati nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="6b486-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="6b486-194">Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6b486-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="6b486-195">Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="6b486-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="6b486-196">È quindi necessario prestare particolare attenzione per verificare che il certificato usato per proteggere la chiave di crittografia del database venga eseguito il backup e la manutenzione del database.</span><span class="sxs-lookup"><span data-stu-id="6b486-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="6b486-197">Se il certificato (o i certificati) viene perduto, i dati saranno illeggibili.</span><span class="sxs-lookup"><span data-stu-id="6b486-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="6b486-198">Eseguire il backup del certificato insieme al database.</span><span class="sxs-lookup"><span data-stu-id="6b486-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="6b486-199">Ogni backup del certificato deve avere due file.</span><span class="sxs-lookup"><span data-stu-id="6b486-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="6b486-200">Entrambi i file devono essere archiviati (in modo ideale separatamente dal file di backup del database per la sicurezza).</span><span class="sxs-lookup"><span data-stu-id="6b486-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="6b486-201">In alternativa, puoi prendere in considerazione l'uso della funzionalità EKM (Extensible Key Management) (Vedi Extensible Key Management) per l'archiviazione e la manutenzione delle chiavi usate per Transparent.</span><span class="sxs-lookup"><span data-stu-id="6b486-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="6b486-202">Per un esempio di come abilitare le istanze di Transparent per il database MBAM, vedere [valutazione di mbam 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="6b486-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="6b486-203">Per altre informazioni su Transparent in SQLServer 2008, vedere [crittografia di SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="6b486-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="6b486-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b486-204">Related topics</span></span>


[<span data-ttu-id="6b486-205">Sicurezza e privacy per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6b486-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





