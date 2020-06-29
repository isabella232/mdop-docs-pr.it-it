---
title: Considerazioni sulla sicurezza relative ad App-V 5.1
description: Considerazioni sulla sicurezza relative ad App-V 5.1
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805973"
---
# <span data-ttu-id="86cf0-103">Considerazioni sulla sicurezza relative ad App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="86cf0-103">App-V 5.1 Security Considerations</span></span>


<span data-ttu-id="86cf0-104">Questo argomento contiene una breve panoramica degli account e dei gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft Application Virtualization (App-V) 5.1.</span></span>

**<span data-ttu-id="86cf0-105">Importante</span><span class="sxs-lookup"><span data-stu-id="86cf0-105">Important</span></span>**  
<span data-ttu-id="86cf0-106">App-V 5,1 non è un prodotto di sicurezza e non fornisce garanzie per un ambiente sicuro.</span><span class="sxs-lookup"><span data-stu-id="86cf0-106">App-V 5.1 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="86cf0-107">La caratteristica PackageStoreAccessControl (PSAC) è deprecata</span><span class="sxs-lookup"><span data-stu-id="86cf0-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="86cf0-108">A partire da giugno 2014, la caratteristica PackageStoreAccessControl (PSAC) introdotta in Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) è stata deprecata sia in ambienti single-user che multiutente.</span><span class="sxs-lookup"><span data-stu-id="86cf0-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="86cf0-109">Considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="86cf0-109">General security considerations</span></span>


**<span data-ttu-id="86cf0-110">Comprendere i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="86cf0-110">Understand the security risks.</span></span>** <span data-ttu-id="86cf0-111">Il rischio più grave per l'App-V 5,1 è che la sua funzionalità potrebbe essere dirottata da un utente non autorizzato che potrebbe quindi riconfigurare i dati chiave nei client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-111">The most serious risk to App-V 5.1 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.1 clients.</span></span> <span data-ttu-id="86cf0-112">La perdita della funzionalità App-V 5,1 per un breve periodo di tempo a causa di un attacco di tipo Denial of Service non avrebbe in genere un impatto catastrofico.</span><span class="sxs-lookup"><span data-stu-id="86cf0-112">The loss of App-V 5.1 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="86cf0-113">**Proteggere fisicamente i computer**.</span><span class="sxs-lookup"><span data-stu-id="86cf0-113">**Physically secure your computers**.</span></span> <span data-ttu-id="86cf0-114">La sicurezza è incompleta senza sicurezza fisica.</span><span class="sxs-lookup"><span data-stu-id="86cf0-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="86cf0-115">Chiunque abbia accesso fisico a un server App-V 5,1 potrebbe potenzialmente attaccare l'intera base client.</span><span class="sxs-lookup"><span data-stu-id="86cf0-115">Anyone with physical access to an App-V 5.1 server could potentially attack the entire client base.</span></span> <span data-ttu-id="86cf0-116">Eventuali attacchi fisici potenziali devono essere considerati ad alto rischio e mitigati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="86cf0-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="86cf0-117">I server App-V 5,1 devono essere archiviati in una sala server fisicamente sicura con accesso controllato.</span><span class="sxs-lookup"><span data-stu-id="86cf0-117">App-V 5.1 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="86cf0-118">Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.</span><span class="sxs-lookup"><span data-stu-id="86cf0-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="86cf0-119">**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**.</span><span class="sxs-lookup"><span data-stu-id="86cf0-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="86cf0-120">Per essere sempre informati sugli aggiornamenti più recenti per i sistemi operativi, Microsoft SQL Server e App-V 5,1, iscriversi al servizio di notifica della sicurezza ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="86cf0-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.1, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="86cf0-121">**Usare password complesse o passare frasi**.</span><span class="sxs-lookup"><span data-stu-id="86cf0-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="86cf0-122">Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di App-V 5,1 e App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-122">Always use strong passwords with 15 or more characters for all App-V 5.1 and App-V 5.1 administrator accounts.</span></span> <span data-ttu-id="86cf0-123">Non usare mai password vuote.</span><span class="sxs-lookup"><span data-stu-id="86cf0-123">Never use blank passwords.</span></span> <span data-ttu-id="86cf0-124">Per altre informazioni sui concetti relativi alle password, vedere il white paper "account password e criteri" su TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="86cf0-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="86cf0-125">Account e gruppi in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="86cf0-125">Accounts and groups in App-V 5.1</span></span>


<span data-ttu-id="86cf0-126">Una procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente.</span><span class="sxs-lookup"><span data-stu-id="86cf0-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="86cf0-127">Aggiungi quindi gli account globali del dominio ai gruppi locali dell'App-V 5,1 necessari nei server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-127">Then, add the domain global accounts to the necessary App-V 5.1 local groups on the App-V 5.1 servers.</span></span>

**<span data-ttu-id="86cf0-128">Nota</span><span class="sxs-lookup"><span data-stu-id="86cf0-128">Note</span></span>**  
<span data-ttu-id="86cf0-129">Gli account di computer client App-V che devono connettersi al server di pubblicazione devono far parte del gruppo locale **utenti** del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="86cf0-130">Per impostazione predefinita, tutti i computer del dominio fanno parte del gruppo **utenti autorizzati** , che fa parte del gruppo **utenti** locali.</span><span class="sxs-lookup"><span data-stu-id="86cf0-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-1-server-security"></a> <span data-ttu-id="86cf0-131">App-V 5,1 sicurezza del server</span><span class="sxs-lookup"><span data-stu-id="86cf0-131">App-V 5.1 server security</span></span>

<span data-ttu-id="86cf0-132">Nessun gruppo viene creato automaticamente durante l'installazione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-132">No groups are created automatically during App-V 5.1 Setup.</span></span> <span data-ttu-id="86cf0-133">È necessario creare i gruppi globali di servizi di dominio Active Directory seguenti per gestire le operazioni del server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.1 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86cf0-134">Nome gruppo</span><span class="sxs-lookup"><span data-stu-id="86cf0-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="86cf0-135">Dettagli</span><span class="sxs-lookup"><span data-stu-id="86cf0-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86cf0-136">Gruppo di amministrazione di App-V Management</span><span class="sxs-lookup"><span data-stu-id="86cf0-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="86cf0-137">Usato per gestire il server di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-137">Used to manage the App-V 5.1 management server.</span></span> <span data-ttu-id="86cf0-138">Questo gruppo viene creato durante l'installazione del server di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-138">This group is created during the App-V 5.1 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86cf0-139">Importante</span><span class="sxs-lookup"><span data-stu-id="86cf0-139">Important</span></span></strong><br/><p><span data-ttu-id="86cf0-140">Non esiste alcun metodo per creare il gruppo usando la console di gestione dopo aver completato l'installazione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86cf0-141">Account del servizio di lettura/scrittura per database</span><span class="sxs-lookup"><span data-stu-id="86cf0-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="86cf0-142">Fornisce l'accesso in lettura/scrittura al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="86cf0-143">Questo account deve essere creato durante l'installazione di database di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-143">This account should be created during the App-V 5.1 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86cf0-144">App-V Service Management installa l'account di amministratore</span><span class="sxs-lookup"><span data-stu-id="86cf0-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86cf0-145">Nota</span><span class="sxs-lookup"><span data-stu-id="86cf0-145">Note</span></span></strong><br/><p><span data-ttu-id="86cf0-146">Questa operazione è necessaria solo se il database di gestione viene installato separatamente dal servizio.</span><span class="sxs-lookup"><span data-stu-id="86cf0-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="86cf0-147">Fornisce l'accesso pubblico alla tabella della versione dello schema nel database di gestione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="86cf0-148">Questo account deve essere creato durante l'installazione di database di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-148">This account should be created during the App-V 5.1 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86cf0-149">App-V Reporting Service installare l'account di amministratore</span><span class="sxs-lookup"><span data-stu-id="86cf0-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86cf0-150">Nota</span><span class="sxs-lookup"><span data-stu-id="86cf0-150">Note</span></span></strong><br/><p><span data-ttu-id="86cf0-151">Questa operazione è necessaria solo se il database di report viene installato separatamente dal servizio.</span><span class="sxs-lookup"><span data-stu-id="86cf0-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="86cf0-152">Accesso pubblico alla tabella della versione dello schema nel database di report.</span><span class="sxs-lookup"><span data-stu-id="86cf0-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="86cf0-153">Questo account deve essere creato durante l'installazione di un database di report App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="86cf0-153">This account should be created during the App-V 5.1 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="86cf0-154">Prendere in considerazione le informazioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="86cf0-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="86cf0-155">Accesso alle condivisioni del pacchetto: se una condivisione esiste nello stesso computer del server di gestione, il servizio di **rete** richiede l'accesso in lettura alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="86cf0-156">Inoltre, ogni computer client App-V deve avere accesso in lettura alla condivisione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="86cf0-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="86cf0-157">Nota</span><span class="sxs-lookup"><span data-stu-id="86cf0-157">Note</span></span>**  
    <span data-ttu-id="86cf0-158">Nelle versioni precedenti di App-V la condivisione del pacchetto veniva definita condivisione di contenuto.</span><span class="sxs-lookup"><span data-stu-id="86cf0-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="86cf0-159">Registrazione dei server di pubblicazione con server di gestione-un server di pubblicazione deve essere registrato con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="86cf0-160">Ad esempio, deve essere aggiunto al database, in modo che gli account del computer del server di pubblicazione siano in grado di chiamare l'API del servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-1-package-security"></a> <span data-ttu-id="86cf0-161">Sicurezza del pacchetto App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="86cf0-161">App-V 5.1 package security</span></span>

<span data-ttu-id="86cf0-162">La procedura seguente consente di pianificare come verificare che i pacchetti virtualizzati siano protetti.</span><span class="sxs-lookup"><span data-stu-id="86cf0-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="86cf0-163">Se un programma di installazione dell'applicazione applica un elenco di controllo di accesso (ACL, Access Control List) a un file o a una directory, l'ACL non viene mantenuta nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="86cf0-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="86cf0-164">Quando il pacchetto viene distribuito, se il file o la directory viene modificata da un utente, erediterà l'ACL nell' **% USERPROFILE%** o erediterà l'ACL della directory del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="86cf0-165">Il caso precedente si verifica se il file o la directory non esiste in una posizione di file system virtuale; quest'ultimo caso si verifica se il file o la directory esiste in una posizione di file system virtuale, ad esempio **% windir%**.</span><span class="sxs-lookup"><span data-stu-id="86cf0-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-1-log-files"></a> <span data-ttu-id="86cf0-166">File di log di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="86cf0-166">App-V 5.1 log files</span></span>


<span data-ttu-id="86cf0-167">Durante l'installazione di App-V 5,1, i file di log della configurazione vengono creati nella cartella **% Temp%** dell'utente che esegue l'installazione.</span><span class="sxs-lookup"><span data-stu-id="86cf0-167">During App-V 5.1 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>






## <span data-ttu-id="86cf0-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86cf0-168">Related topics</span></span>


[<span data-ttu-id="86cf0-169">Preparazione dell'ambiente per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="86cf0-169">Preparing Your Environment for App-V 5.1</span></span>](preparing-your-environment-for-app-v-51.md)









