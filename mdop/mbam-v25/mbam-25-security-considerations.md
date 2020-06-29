---
title: Considerazioni sulla sicurezza per MBAM 2.5
description: Considerazioni sulla sicurezza per MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826836"
---
# <span data-ttu-id="7ba1a-103">Considerazioni sulla sicurezza per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7ba1a-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="7ba1a-104">Questo argomento contiene le informazioni seguenti su come proteggere l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM):</span><span class="sxs-lookup"><span data-stu-id="7ba1a-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="7ba1a-105">Configurare MBAM per escrow il TPM e archiviare le password di OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="7ba1a-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="7ba1a-106">Configurare MBAM per sbloccare automaticamente il TPM dopo un blocco</span><span class="sxs-lookup"><span data-stu-id="7ba1a-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="7ba1a-107">Connessioni sicure a SQL Server</span><span class="sxs-lookup"><span data-stu-id="7ba1a-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="7ba1a-108">Creare account e gruppi</span><span class="sxs-lookup"><span data-stu-id="7ba1a-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="7ba1a-109">Usare i file di log di MBAM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="7ba1a-110">Esaminare le considerazioni di database per i dati di MBAM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="7ba1a-111">Informazioni sulle considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="7ba1a-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="7ba1a-112">Configurare MBAM per escrow il TPM e archiviare le password di OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="7ba1a-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="7ba1a-113">**Nota** Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="7ba1a-114">Inoltre, Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="7ba1a-115">Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="7ba1a-116">A seconda della configurazione in uso, il TPM (Trusted Platform Module) si bloccherà in determinate situazioni, ad esempio quando vengono immesse troppe password errate ─ e può rimanere bloccato per un periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="7ba1a-117">Durante il blocco TPM, BitLocker non può accedere alle chiavi di crittografia per eseguire operazioni di sblocco o decrittografia, richiedendo all'utente di immettere la chiave di ripristino di BitLocker per accedere all'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="7ba1a-118">Per reimpostare il blocco TPM, è necessario specificare la password di OwnerAuth TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="7ba1a-119">MBAM può archiviare la password di OwnerAuth TPM nel database MBAM se è proprietaria del TPM o se ha escrowed la password.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="7ba1a-120">Le password di OwnerAuth sono quindi facilmente accessibili nel sito Web di amministrazione e monitoraggio quando è necessario eseguire il ripristino da un blocco TPM, eliminando la necessità di attendere che il blocco venga risolto autonomamente.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="7ba1a-121">Garanzia del TPM OwnerAuth in Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="7ba1a-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="7ba1a-122">**Nota** Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="7ba1a-123">In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="7ba1a-124">Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="7ba1a-125">In Windows 8 o versioni successive, MBAM non deve più possedere il TPM per archiviare la password di OwnerAuth, purché il OwnerAuth sia disponibile nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="7ba1a-126">Per abilitare MBAM a escrow e quindi archiviare le password di OwnerAuth TPM, è necessario configurare queste impostazioni di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ba1a-127">Impostazione di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="7ba1a-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="7ba1a-128">Configurazione</span><span class="sxs-lookup"><span data-stu-id="7ba1a-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ba1a-129">Attivare il backup TPM in servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="7ba1a-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ba1a-130">Disabilitata o non configurata</span><span class="sxs-lookup"><span data-stu-id="7ba1a-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ba1a-131">Configurare il livello delle informazioni di autorizzazione del proprietario del TPM disponibili per il sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7ba1a-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ba1a-132">Delegata/nessuna o non configurata</span><span class="sxs-lookup"><span data-stu-id="7ba1a-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7ba1a-133">La posizione di queste impostazioni di criteri di gruppo è la **configurazione dei computer** &gt; **modelli amministrativi** di &gt; **sistema** &gt; **Trusted Platform Module Services**.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="7ba1a-134">**Nota**  Windows rimuove il OwnerAuth localmente dopo che MBAM l'ha esposta con successo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="7ba1a-135">Garanzia del TPM OwnerAuth in Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ba1a-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="7ba1a-136">In Windows 7, MBAM deve possedere il TPM per l'escrow automaticamente le informazioni di OwnerAuth del TPM nel database MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="7ba1a-137">Se MBAM non è il proprietario del TPM, è necessario usare i cmdlet di importazione di dati di MBAM Active Directory (AD) per copiare il TPM OwnerAuth da Active Directory nel database MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="7ba1a-138">MBAM cmdlet di importazione di dati di Active Directory</span><span class="sxs-lookup"><span data-stu-id="7ba1a-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="7ba1a-139">I cmdlet di importazione dei dati di MBAM Active Directory consentono di recuperare i pacchetti chiave di ripristino e le password di OwnerAuth archiviate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="7ba1a-140">Il server MBAM 2,5 SP1 viene fornito con quattro cmdlet di PowerShell che prepopolano i database di MBAM con le informazioni di ripristino del volume e del proprietario del TPM archiviate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="7ba1a-141">Per le chiavi e i pacchetti di ripristino del volume:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="7ba1a-142">Read-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="7ba1a-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="7ba1a-143">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="7ba1a-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="7ba1a-144">Per informazioni sul proprietario del TPM:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="7ba1a-145">Read-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="7ba1a-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="7ba1a-146">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="7ba1a-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="7ba1a-147">Per associare utenti ai computer:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="7ba1a-148">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="7ba1a-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="7ba1a-149">I cmdlet Read-AD \ \* leggono le informazioni da Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="7ba1a-150">I cmdlet Write-mbam \ \* spingono i dati nei database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="7ba1a-151">Per informazioni dettagliate su questi cmdlet, ad esempio sintassi, parametri ed esempi, vedere [riferimenti ai cmdlet per l'amministrazione e il monitoraggio di Microsoft Bitlocker 2,5](https://technet.microsoft.com/library/dn459018.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="7ba1a-152">**Creare associazioni da utente a computer:** I cmdlet di importazione dei dati di MBAM Active Directory raccolgono informazioni da Active Directory e inseriscono i dati in database MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="7ba1a-153">Tuttavia, non associano gli utenti ai volumi.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="7ba1a-154">È possibile scaricare lo script di PowerShell Add-ComputerUser.ps1 per creare associazioni da utente a computer, che consentono agli utenti di recuperare l'accesso a un computer tramite il sito Web di amministrazione e monitoraggio oppure usando il portale self-service per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="7ba1a-155">Lo script Add-ComputerUser.ps1 raccoglie i dati dall'attributo **Managed by** in Active Directory (ad), il proprietario dell'oggetto in un annuncio o da un file CSV personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="7ba1a-156">Lo script aggiunge quindi gli utenti individuati all'oggetto della pipeline delle informazioni di ripristino, che deve essere passato a Write-MbamRecoveryInformation per inserire i dati nel database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="7ba1a-157">Scaricare lo script di PowerShell Add-ComputerUser.ps1 dall' [area download Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="7ba1a-158">Puoi specificare la **guida Add-ComputerUser.ps1** per ottenere assistenza per lo script, inclusi esempi su come usare i cmdlet e lo script.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="7ba1a-159">Per creare associazioni da utente a computer dopo aver installato il server MBAM, usare il cmdlet di PowerShell Write-MbamComputerUser.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="7ba1a-160">In modo analogo allo script di PowerShell Add-ComputerUser.ps1, questo cmdlet consente di specificare gli utenti che possono usare il portale self-service per ottenere le informazioni OwnerAuth di TPM o le password di ripristino del volume per il computer specificato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="7ba1a-161">**Nota**  L'agente MBAM eseguirà l'override delle associazioni utente-computer quando il computer inizia a segnalare fino al server.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="7ba1a-162">**Prerequisiti:** I cmdlet Read-AD \ \* possono recuperare informazioni da Active Directory solo se vengono eseguiti come account utente con privilegi elevati, ad esempio un amministratore di dominio, o eseguiti come account in un gruppo di sicurezza personalizzato concesso l'accesso in lettura alle informazioni (scelta consigliata).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="7ba1a-163">[Guida alle operazioni di crittografia unità BitLocker: il recupero dei volumi crittografati con servizi di dominio Active Directory](https://technet.microsoft.com/library/cc771778(WS.10).aspx) fornisce informazioni dettagliate sulla creazione di un gruppo di sicurezza personalizzato o di più gruppi con accesso in lettura alle informazioni sugli annunci.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="7ba1a-164">**Autorizzazioni di scrittura per il recupero e il servizio Web hardware per mbam:** I cmdlet Write-mbam \ \* accettano l'URL del servizio di ripristino e hardware di MBAM, usato per pubblicare le informazioni di ripristino o TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="7ba1a-165">In genere, solo un account del servizio computer di dominio può comunicare con il servizio di ripristino e hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="7ba1a-166">In MBAM 2,5 SP1 è possibile configurare il servizio di ripristino e hardware di MBAM con un gruppo di sicurezza denominato DataMigrationAccessGroup i cui membri sono autorizzati a ignorare il controllo dell'account del servizio di computer del dominio.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="7ba1a-167">I cmdlet Write-mbam \ \* devono essere eseguiti come utenti appartenenti a questo gruppo configurato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="7ba1a-168">In alternativa, le credenziali di un singolo utente nel gruppo configurato possono essere specificate usando il parametro – Credential nei cmdlet Write-mbam \ \*.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="7ba1a-169">È possibile configurare il servizio di ripristino e hardware di MBAM con il nome del gruppo di sicurezza in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="7ba1a-170">Specificare il nome del gruppo di sicurezza (o individuale) nel parametro-DataMigrationAccessGroup del cmdlet Enable-MbamWebApplication-AgentService di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="7ba1a-171">Configurare il gruppo dopo che il servizio di ripristino e hardware di MBAM è stato installato modificando il file di web.config nella &lt; &gt; cartella \\Microsoft di Solution\\Recovery e hardware Service\\ di Inetpub.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="7ba1a-172">dove &lt; GroupName &gt; viene sostituito con il dominio e il nome del gruppo (o il singolo utente) che verrà usato per consentire la migrazione dei dati da Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="7ba1a-173">Usare l'editor di configurazione in Gestione IIS per modificare questo appSetting.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="7ba1a-174">Nell'esempio seguente il comando, quando viene eseguito come membro del gruppo ADRecoveryInformation e del gruppo utenti migrazione dati, tirerà le informazioni di ripristino del volume dai computer nell'unità organizzativa WORKSTATION nel dominio contoso.com e li scriverà in MBAM usando il servizio di ripristino e hardware di MBAM in esecuzione nel server di mbam.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="7ba1a-175">**Read-ad \ \* cmdlet** accetta il nome o l'indirizzo IP di un computer server di hosting Active Directory in cui eseguire una query per le informazioni di ripristino o TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="7ba1a-176">Ti consigliamo di fornire i nomi distinti dei contenitori di annunci in cui l'oggetto computer risiede come valore del parametro SearchBase.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="7ba1a-177">Se i computer sono archiviati in più unità organizzative, i cmdlet possono accettare l'input della pipeline da eseguire una sola volta per ogni contenitore.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="7ba1a-178">Il nome distinto di un contenitore di annunci avrà un aspetto simile a OU = machines, DC = contoso, DC = com.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="7ba1a-179">L'esecuzione di una ricerca mirata a specifici contenitori offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="7ba1a-180">Riduce il rischio di timeout durante l'esecuzione di query su un set di dati di grandi dimensioni per gli oggetti computer.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="7ba1a-181">Può omettere le UO che contengono Server Datacenter o altre classi di computer per cui il backup potrebbe non essere desiderato o necessario.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="7ba1a-182">Un'altra opzione consiste nel specificare il flag-recurse con o senza il SearchBase facoltativo per cercare oggetti computer in tutti i contenitori in SearchBase specificato o nell'intero dominio rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="7ba1a-183">Quando usi il flag-recurse, puoi anche usare il parametro-MaxPageSize per controllare la quantità di memoria locale e remota necessaria per il servizio della query.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="7ba1a-184">Questi cmdlet scrivono agli oggetti pipeline di tipo PsObject.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="7ba1a-185">Ogni istanza di PsObject contiene una sola chiave di ripristino del volume o una stringa del proprietario del TPM con il nome del computer associato, il timestamp e altre informazioni necessarie per pubblicarlo nell'archivio dati di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="7ba1a-186">**Write-mbam \ \* i cmdlet** accettano i valori dei parametri delle informazioni di ripristino dalla pipeline per nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="7ba1a-187">In questo modo, i cmdlet Write-mbam \ \* accettano l'output della pipeline dei cmdlet Read-AD \ \*, ad esempio Read-ADRecoveryInformation-server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="7ba1a-188">I \*\*cmdlet Write-mbam \ \*\*\* includono parametri facoltativi che offrono opzioni per la tolleranza di errore, la registrazione dettagliata e le preferenze per WhatIf e Confirm.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="7ba1a-189">I \*\*cmdlet Write-mbam \ \*\*\* includono anche un parametro di *ora* facoltativo il cui valore è un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="7ba1a-190">Questo oggetto include un attributo *Kind* che può essere impostato su `Local` , `UTC` o `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="7ba1a-191">Quando il parametro *Time* viene popolato da dati presi da Active Directory, l'ora viene convertita in UTC e questo attributo *Kind* viene impostato automaticamente su `UTC` .</span><span class="sxs-lookup"><span data-stu-id="7ba1a-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="7ba1a-192">Tuttavia, quando si popola il parametro *Time* usando un'altra origine, ad esempio un file di testo, è necessario impostare esplicitamente l'attributo *Kind* sul relativo valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="7ba1a-193">**Nota**  I cmdlet Read-AD \ \* non hanno la possibilità di individuare gli account utente che rappresentano gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="7ba1a-194">Le associazioni di account utente sono necessarie per le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="7ba1a-195">Utenti per recuperare le password di volume/pacchetti usando il portale self-service</span><span class="sxs-lookup"><span data-stu-id="7ba1a-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="7ba1a-196">Utenti che non fanno parte del gruppo di sicurezza MBAM Advanced helpdesk Users come definito durante l'installazione, che si riprenderà per conto di altri utenti</span><span class="sxs-lookup"><span data-stu-id="7ba1a-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="7ba1a-197">Configurare MBAM per sbloccare automaticamente il TPM dopo un blocco</span><span class="sxs-lookup"><span data-stu-id="7ba1a-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="7ba1a-198">È possibile configurare MBAM 2,5 SP1 per sbloccare automaticamente il TPM in caso di blocco.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="7ba1a-199">Se l'opzione di ripristino automatico del blocco TPM è abilitata, MBAM può rilevare che un utente è bloccato e quindi ottenere la password di OwnerAuth dal database MBAM per sbloccare automaticamente il TPM per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="7ba1a-200">Blocco TPM il ripristino automatico è disponibile solo se la chiave di ripristino del sistema operativo per il computer è stata recuperata tramite il portale self service o il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="7ba1a-201">**Importante**  Per abilitare la reimpostazione automatica del blocco TPM, è necessario configurare questa funzionalità sia nel lato server che in criteri di gruppo sul lato client.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="7ba1a-202">Per abilitare la reimpostazione automatica del blocco TPM sul lato client, configurare l'impostazione di criteri di gruppo "Configura ripristino automatico di blocco TPM" disponibile in **Configurazione computer** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam** &gt; **Client Management**.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="7ba1a-203">Per abilitare il ripristino automatico del blocco TPM sul lato server, è possibile selezionare "Abilita ripristino automatico del blocco TPM" nella configurazione guidata del server MBAM durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="7ba1a-204">È anche possibile abilitare il ripristino automatico del blocco TPM in PowerShell specificando l'opzione "-TPM lockout auto reset" quando si Abilita il componente Web del servizio agente.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="7ba1a-205">Dopo che un utente immette la chiave di ripristino di BitLocker ottenuta dal portale self service o dal sito Web di amministrazione e monitoraggio, l'agente di MBAM determinerà se il TPM è bloccato. Se è bloccata, tenterà di recuperare il OwnerAuth TPM per il computer dal database MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="7ba1a-206">Se il OwnerAuth TPM viene recuperato correttamente, verrà usato per sbloccare il TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="7ba1a-207">Lo sblocco del TPM rende il TPM completamente funzionante e l'utente non verrà costretto a immettere la password di ripristino durante il riavvio successivo da un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="7ba1a-208">Il ripristino automatico del blocco TPM è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="7ba1a-209">**Nota**  Blocco TPM il ripristino automatico è supportato solo nei computer che eseguono il TPM versione 1,2.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="7ba1a-210">TPM 2,0 offre funzionalità di reimpostazione automatica del blocco predefinito.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="7ba1a-211">**Il report di controllo del ripristino** include gli eventi correlati alla reimpostazione automatica del blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="7ba1a-212">Se viene effettuata una richiesta dal client MBAM per recuperare una password di OwnerAuth TPM, viene registrato un evento per indicare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="7ba1a-213">Le voci di controllo includono gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ba1a-214">Voce</span><span class="sxs-lookup"><span data-stu-id="7ba1a-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="7ba1a-215">Value</span><span class="sxs-lookup"><span data-stu-id="7ba1a-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ba1a-216">Origine della richiesta di controllo</span><span class="sxs-lookup"><span data-stu-id="7ba1a-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ba1a-217">Sblocco TPM agente</span><span class="sxs-lookup"><span data-stu-id="7ba1a-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ba1a-218">Tipo di chiave</span><span class="sxs-lookup"><span data-stu-id="7ba1a-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ba1a-219">Hash della password TPM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ba1a-220">Descrizione motivo</span><span class="sxs-lookup"><span data-stu-id="7ba1a-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ba1a-221">Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="7ba1a-222">Connessioni sicure a SQL Server</span><span class="sxs-lookup"><span data-stu-id="7ba1a-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="7ba1a-223">In MBAM, SQL Server comunica con SQL Server Reporting Services e con i servizi Web per il sito Web di amministrazione e monitoraggio e il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="7ba1a-224">È consigliabile proteggere la comunicazione con SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="7ba1a-225">Per altre informazioni, vedere [crittografia di connessioni a SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="7ba1a-226">Per altre informazioni su come proteggere i siti Web di MBAM, vedere [pianificazione di come proteggere i siti Web di mbam](planning-how-to-secure-the-mbam-websites.md).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="7ba1a-227">Creare account e gruppi</span><span class="sxs-lookup"><span data-stu-id="7ba1a-227">Create accounts and groups</span></span>


<span data-ttu-id="7ba1a-228">La procedura consigliata per la gestione degli account utente consiste nel creare gruppi globali di dominio e aggiungere gli account utente.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="7ba1a-229">Per una descrizione degli account e dei gruppi consigliati, vedere [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="7ba1a-230">Usare i file di log di MBAM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-230">Use MBAM log files</span></span>


<span data-ttu-id="7ba1a-231">Questa sezione descrive i file di log di MBAM server e MBAM client.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="7ba1a-232">File di log configurazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="7ba1a-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="7ba1a-233">Il file **MBAMServerSetup.exe** genera i file di log seguenti nella cartella **% Temp%** dell'utente durante l'installazione di mbam:</span><span class="sxs-lookup"><span data-stu-id="7ba1a-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="7ba1a-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log</span><span class="sxs-lookup"><span data-stu-id="7ba1a-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="7ba1a-235">Registra le azioni intraprese durante l'installazione di MBAM e la configurazione della funzionalità del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="7ba1a-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="7ba1a-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="7ba1a-237">Registra altre azioni intraprese durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="7ba1a-238">File di log di configurazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="7ba1a-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="7ba1a-239">Registri delle applicazioni e dei servizi/Microsoft Windows/MBAM-Setup</span><span class="sxs-lookup"><span data-stu-id="7ba1a-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="7ba1a-240">Registra gli errori che si verificano quando si utilizzano i cmdlet di Windows PowerShell o la configurazione guidata server MBAM per configurare le caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="7ba1a-241">File di log della configurazione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="7ba1a-242">MSI &lt; Five random characters &gt; . log</span><span class="sxs-lookup"><span data-stu-id="7ba1a-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="7ba1a-243">Registra le azioni intraprese durante l'installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="7ba1a-244">MBAM-file di log Web</span><span class="sxs-lookup"><span data-stu-id="7ba1a-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="7ba1a-245">Mostra le attività dei portali e dei servizi Web.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="7ba1a-246">Esaminare le considerazioni di database per i dati di MBAM</span><span class="sxs-lookup"><span data-stu-id="7ba1a-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="7ba1a-247">La funzionalità di crittografia dati trasparente (Transparent Data Encryption) disponibile in SQL Server è un'installazione facoltativa per le istanze di database che ospitano le caratteristiche del database MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="7ba1a-248">Con Transparent, è possibile eseguire una crittografia a livello di database completa in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="7ba1a-249">Transparent è la scelta ottimale per la crittografia in blocco per soddisfare gli standard di sicurezza dei dati aziendali o conformità normativa.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="7ba1a-250">Transparent funziona a livello di file, che è simile a due caratteristiche di Windows: EFS (Encrypting File System) e crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="7ba1a-251">Entrambe le funzionalità crittografano anche i dati nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="7ba1a-252">Transparent non sostituisce crittografia a livello di cella, EFS o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="7ba1a-253">Quando la funzionalità di crittografia è abilitata in un database, tutti i backup vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="7ba1a-254">È quindi necessario prestare particolare attenzione per verificare che il certificato usato per proteggere la chiave di crittografia del database venga eseguito il backup e la manutenzione del database.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="7ba1a-255">Se il certificato (o i certificati) viene perduto, i dati saranno illeggibili.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="7ba1a-256">Eseguire il backup del certificato con il database.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-256">Back up the certificate with the database.</span></span> <span data-ttu-id="7ba1a-257">Ogni backup del certificato deve avere due file.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="7ba1a-258">Entrambi i file devono essere archiviati.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-258">Both of these files should be archived.</span></span> <span data-ttu-id="7ba1a-259">Idealmente per la sicurezza, è consigliabile eseguire il backup separatamente dal file di backup del database.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="7ba1a-260">In alternativa, puoi prendere in considerazione l'uso della funzionalità EKM (Extensible Key Management) (Vedi Extensible Key Management) per l'archiviazione e la manutenzione delle chiavi usate per Transparent.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="7ba1a-261">Per un esempio di come abilitare Transparent per le istanze di database di MBAM, vedere [informazioni sulla crittografia dei dati trasparente](https://technet.microsoft.com/library/bb934049.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ba1a-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="7ba1a-262">Informazioni sulle considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="7ba1a-262">Understand general security considerations</span></span>


**<span data-ttu-id="7ba1a-263">Comprendere i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-263">Understand the security risks.</span></span>** <span data-ttu-id="7ba1a-264">Il rischio più grave quando si usa l'amministrazione e il monitoraggio di Microsoft BitLocker è che la sua funzionalità potrebbe essere compromessa da un utente non autorizzato che potrebbe quindi riconfigurare la crittografia unità BitLocker e ottenere i dati della chiave di crittografia BitLocker nei client MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="7ba1a-265">Tuttavia, la perdita delle funzionalità di MBAM per un breve periodo di tempo, a causa di un attacco di tipo Denial of Service, in genere non ha un impatto catastrofico, a differenza, ad esempio, di perdere posta elettronica o comunicazioni di rete o di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="7ba1a-266">**Proteggere fisicamente i computer**.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-266">**Physically secure your computers**.</span></span> <span data-ttu-id="7ba1a-267">Non c'è sicurezza senza sicurezza fisica.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-267">There is no security without physical security.</span></span> <span data-ttu-id="7ba1a-268">Un utente malintenzionato che ottiene l'accesso fisico a un server MBAM può potenzialmente usarlo per attaccare l'intera base client.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="7ba1a-269">Tutti i potenziali attacchi fisici devono essere considerati ad alto rischio e mitigati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="7ba1a-270">I server MBAM devono essere archiviati in una sala server sicura con accesso controllato.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="7ba1a-271">Proteggere questi computer quando gli amministratori non sono fisicamente presenti quando il sistema operativo blocca il computer oppure usando uno screen saver protetto.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="7ba1a-272">**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="7ba1a-273">Rimanere informati sui nuovi aggiornamenti per sistemi operativi Windows, SQL Server e MBAM iscrivendoti al servizio di notifica della sicurezza presso il [TechCenter di sicurezza](https://go.microsoft.com/fwlink/?LinkId=28819).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="7ba1a-274">**Usare password complesse o passare frasi**.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="7ba1a-275">Usa sempre password complesse con 15 o più caratteri per tutti gli account di amministratore di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="7ba1a-276">Non usare mai password vuote.</span><span class="sxs-lookup"><span data-stu-id="7ba1a-276">Never use blank passwords.</span></span> <span data-ttu-id="7ba1a-277">Per altre informazioni sui concetti relativi alle password, vedere [criteri password](https://technet.microsoft.com/library/hh994572.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="7ba1a-278">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ba1a-278">Related topics</span></span>


[<span data-ttu-id="7ba1a-279">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7ba1a-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="7ba1a-280">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="7ba1a-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7ba1a-281">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="7ba1a-282">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7ba1a-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





