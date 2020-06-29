---
title: Pianificazione di gruppi e account di MBAM 2.5
description: Pianificazione di gruppi e account di MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825805"
---
# <span data-ttu-id="9f930-103">Pianificazione di gruppi e account di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9f930-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="9f930-104">Questo argomento elenca i ruoli e gli account che è necessario creare in servizi di dominio Active Directory per specificare i diritti di sicurezza e di accesso per i database di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, i report e le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="9f930-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="9f930-105">Per ogni ruolo e account, viene fornito il campo corrispondente nella configurazione guidata di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="9f930-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="9f930-106">Per un elenco di cmdlet e parametri di Windows PowerShell che corrispondono a questi account, vedere [configurazione delle funzionalità del server di MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="9f930-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="9f930-107">Nota</span><span class="sxs-lookup"><span data-stu-id="9f930-107">Note</span></span>**  
<span data-ttu-id="9f930-108">MBAM non supporta l'uso di account di servizio gestiti.</span><span class="sxs-lookup"><span data-stu-id="9f930-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="9f930-109">Account di database</span><span class="sxs-lookup"><span data-stu-id="9f930-109">Database accounts</span></span>


<span data-ttu-id="9f930-110">Creare gli account seguenti per il database di conformità e controllo e il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9f930-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f930-111">Nome dell'account e scopo</span><span class="sxs-lookup"><span data-stu-id="9f930-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="9f930-112">Tipo di account</span><span class="sxs-lookup"><span data-stu-id="9f930-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="9f930-113">Campo configurazione guidata server di MBAM che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="9f930-114">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f930-115">Utente o gruppo di lettura/scrittura di database di conformità e controllo e database di ripristino per i report</span><span class="sxs-lookup"><span data-stu-id="9f930-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-116">Utente o gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-117">Utente o gruppo di dominio di accesso in lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9f930-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-118">Utente o gruppo di dominio che ha accesso in lettura/scrittura al database di conformità e controllo e al database di ripristino per consentire alle applicazioni Web di accedere ai dati e ai report in questi database.</span><span class="sxs-lookup"><span data-stu-id="9f930-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="9f930-119">Se si immette un nome utente in questo campo, deve essere lo stesso valore del <strong> campo account del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="9f930-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="9f930-120">Se si immette un nome di gruppo in questo campo, il valore nel <strong> campo account di dominio del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> deve essere un membro del gruppo immesso in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9f930-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f930-121">Utente o gruppo di sola lettura per i report per il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9f930-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-122">Utente o gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-123">Utente o gruppo di dominio di Access di sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f930-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-124">Nome dell'utente o del gruppo che avrà accesso di sola lettura al database di conformità e controllo per consentire ai report di accedere ai dati di conformità e controllo in questo database.</span><span class="sxs-lookup"><span data-stu-id="9f930-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="9f930-125">Se si immette un nome utente in questo campo, deve essere lo stesso utente di quello specificato nel <strong> campo conformità e controllo del dominio del database nella </strong> <strong> pagina Configura report </strong> .</span><span class="sxs-lookup"><span data-stu-id="9f930-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="9f930-126">Se si immette un nome di gruppo in questo campo, il valore specificato nel <strong> campo account di dominio del database di conformità e controllo nella </strong> <strong> pagina Configura report </strong> deve essere un membro del gruppo specificato in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9f930-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9f930-127">Account per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="9f930-127">Reporting accounts</span></span>


<span data-ttu-id="9f930-128">Creare gli account seguenti per la caratteristica report.</span><span class="sxs-lookup"><span data-stu-id="9f930-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f930-129">Nome account/scopo</span><span class="sxs-lookup"><span data-stu-id="9f930-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="9f930-130">Tipo di account</span><span class="sxs-lookup"><span data-stu-id="9f930-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="9f930-131">Campo configurazione guidata server di MBAM che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="9f930-132">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f930-133">Report di gruppo di Access per il dominio di sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f930-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-134">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-135">Gruppo di Domain Role Reporting</span><span class="sxs-lookup"><span data-stu-id="9f930-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-136">Specifica il gruppo di utenti del dominio che ha accesso in sola lettura ai report nel sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9f930-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="9f930-137">Il gruppo specificato deve essere lo stesso gruppo specificata per il parametro di gruppo di Access di sola lettura di report quando le app Web sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="9f930-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f930-138">Account utente del dominio del database di conformità e audit</span><span class="sxs-lookup"><span data-stu-id="9f930-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-139">Utente</span><span class="sxs-lookup"><span data-stu-id="9f930-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-140">Account di dominio del database di conformità e audit</span><span class="sxs-lookup"><span data-stu-id="9f930-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-141">Account utente e password di dominio che l'istanza di SQL Server Reporting Services locale usa per accedere al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9f930-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="9f930-142">Questo account richiede <strong> l'accesso come </strong> diritti batch al server SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="9f930-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="9f930-143">Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un nome utente, è necessario immettere lo stesso valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9f930-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="9f930-144">Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un nome di gruppo, il valore immesso in questo campo deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="9f930-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="9f930-145">Configurare la password per l'account per non scadere mai.</span><span class="sxs-lookup"><span data-stu-id="9f930-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="9f930-146">L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="9f930-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="9f930-147">Account di amministrazione e monitoraggio del sito Web (Help desk)</span><span class="sxs-lookup"><span data-stu-id="9f930-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="9f930-148">Creare gli account seguenti per il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9f930-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f930-149">Nome account/scopo</span><span class="sxs-lookup"><span data-stu-id="9f930-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="9f930-150">Tipo di account</span><span class="sxs-lookup"><span data-stu-id="9f930-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="9f930-151">Campo configurazione guidata server di MBAM che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="9f930-152">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</span><span class="sxs-lookup"><span data-stu-id="9f930-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f930-153">Account di dominio del pool di applicazioni Web Service</span><span class="sxs-lookup"><span data-stu-id="9f930-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-154">Utente</span><span class="sxs-lookup"><span data-stu-id="9f930-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-155">Account di dominio del pool di applicazioni Web Service</span><span class="sxs-lookup"><span data-stu-id="9f930-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-156">Account utente di dominio che deve essere usato dal pool di applicazioni per le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="9f930-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="9f930-157">Se si immette un nome utente nel <strong> campo utente o gruppo di dominio di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , è necessario immettere lo stesso valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9f930-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="9f930-158">Se si immette un nome di gruppo nel <strong> campo utente o gruppo di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , il valore immesso in questo campo deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="9f930-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="9f930-159">Se non specifichi le credenziali, verranno usate le credenziali specificate per qualsiasi applicazione Web abilitata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9f930-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="9f930-160">Tutte le applicazioni Web devono usare le stesse credenziali del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9f930-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="9f930-161">Se si specificano credenziali diverse per diverse applicazioni Web, verrà usato il valore specificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="9f930-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="9f930-162">Importante</span><span class="sxs-lookup"><span data-stu-id="9f930-162">Important</span></span></strong><br/><p><span data-ttu-id="9f930-163">Per una maggiore sicurezza, imposta l'account specificato nelle credenziali per avere diritti utente limitati.</span><span class="sxs-lookup"><span data-stu-id="9f930-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f930-164">MBAM Advanced helpdesk utenti di Access Group</span><span class="sxs-lookup"><span data-stu-id="9f930-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-165">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-166">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="9f930-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-167">Gruppo di utenti di dominio i cui membri hanno accesso a tutte le aree di ripristino del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9f930-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="9f930-168">Gli utenti che hanno questo ruolo devono immettere solo la chiave di ripristino e non il dominio e il nome utente dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità.</span><span class="sxs-lookup"><span data-stu-id="9f930-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="9f930-169">Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti dell'helpdesk avanzato MBAM eseguono l'override delle autorizzazioni di MBAM Group helpdesk.</span><span class="sxs-lookup"><span data-stu-id="9f930-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f930-170">Gruppo di Access per gli utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="9f930-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-171">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-172">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="9f930-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-173">Gruppo di utenti di dominio i cui membri hanno accesso alle aree Manage TPM e unità di ripristino del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9f930-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="9f930-174">Gli utenti che hanno questo ruolo devono compilare tutti i campi, incluso il dominio dell'utente finale e il nome dell'account, quando usano entrambe le opzioni.</span><span class="sxs-lookup"><span data-stu-id="9f930-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="9f930-175">Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti dell'helpdesk avanzato MBAM eseguono l'override delle autorizzazioni di MBAM Group helpdesk.</span><span class="sxs-lookup"><span data-stu-id="9f930-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9f930-176">Gruppo di Access report MBAM utenti</span><span class="sxs-lookup"><span data-stu-id="9f930-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-177">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-178">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="9f930-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-179">Gruppo di utenti di dominio i cui membri hanno accesso in sola lettura ai report nell'area report del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9f930-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f930-180">Gruppo utenti di migrazione dei dati di MBAM</span><span class="sxs-lookup"><span data-stu-id="9f930-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-181">Gruppo</span><span class="sxs-lookup"><span data-stu-id="9f930-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-182">Utenti di migrazione dei dati di MBAM</span><span class="sxs-lookup"><span data-stu-id="9f930-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f930-183">Gruppo di utenti di dominio facoltativo i cui membri hanno le autorizzazioni per scrivere i dati in MBAM usando il servizio di ripristino e hardware di MBAM in uso nel server MBAM.</span><span class="sxs-lookup"><span data-stu-id="9f930-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="9f930-184">Questo account viene in genere usato con i cmdlet Write-mbam \* per scrivere i dati di ripristino e TPM da Active Directory nel database MBAM.</span><span class="sxs-lookup"><span data-stu-id="9f930-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="9f930-185">Per altre informazioni, Vedi <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="9f930-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="9f930-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f930-186">Related topics</span></span>


[<span data-ttu-id="9f930-187">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9f930-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="9f930-188">Prerequisiti per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9f930-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="9f930-189">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="9f930-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9f930-190">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="9f930-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9f930-191">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9f930-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





