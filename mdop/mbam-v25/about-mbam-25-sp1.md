---
title: Informazioni su MBAM 2.5 SP1
description: Informazioni su MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823785"
---
# <span data-ttu-id="a80a5-103">Informazioni su MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="a80a5-103">About MBAM 2.5 SP1</span></span>


<span data-ttu-id="a80a5-104">MBAM 2,5 SP1 offre un'interfaccia amministrativa semplificata per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a80a5-104">MBAM 2.5 SP1 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="a80a5-105">BitLocker offre una protezione avanzata per il furto di dati o l'esposizione ai dati per i computer persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="a80a5-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="a80a5-106">BitLocker crittografa tutti i dati archiviati nel sistema operativo Windows e in unità e unità dati configurate.</span><span class="sxs-lookup"><span data-stu-id="a80a5-106">BitLocker encrypts all data that is stored on the Windows operating system and drives and configured data drives.</span></span>

## <span data-ttu-id="a80a5-107">Panoramica di MBAM</span><span class="sxs-lookup"><span data-stu-id="a80a5-107">Overview of MBAM</span></span>


<span data-ttu-id="a80a5-108">MBAM 2,5 SP1 ha le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="a80a5-108">MBAM 2.5 SP1 has the following features:</span></span>

-   <span data-ttu-id="a80a5-109">Consente agli amministratori di automatizzare il processo di crittografia dei volumi nei computer client in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a80a5-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="a80a5-110">Consente agli addetti alla sicurezza di determinare rapidamente lo stato di conformità dei singoli computer o anche dell'organizzazione stessa.</span><span class="sxs-lookup"><span data-stu-id="a80a5-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="a80a5-111">Fornisce Reporting centralizzato e gestione hardware con Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a80a5-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="a80a5-112">Riduce il carico di lavoro nell'help desk per aiutare gli utenti finali con le richieste di chiavi di ripristino e PIN di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a80a5-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="a80a5-113">Consente agli utenti finali di recuperare i dispositivi crittografati in modo indipendente usando il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="a80a5-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="a80a5-114">Consente agli addetti alla sicurezza di controllare facilmente l'accesso per recuperare le informazioni chiave.</span><span class="sxs-lookup"><span data-stu-id="a80a5-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="a80a5-115">Consente agli utenti di Windows Enterprise di continuare a lavorare ovunque con la garanzia che i loro dati aziendali siano protetti.</span><span class="sxs-lookup"><span data-stu-id="a80a5-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="a80a5-116">MBAM applica le opzioni dei criteri di crittografia di BitLocker impostate per l'organizzazione, monitora la conformità dei computer client con tali criteri e segnala lo stato di crittografia dei computer dell'organizzazione e dell'individuo.</span><span class="sxs-lookup"><span data-stu-id="a80a5-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="a80a5-117">Inoltre, MBAM consente di accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambiano i record del BIOS o del boot.</span><span class="sxs-lookup"><span data-stu-id="a80a5-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="a80a5-118">I gruppi seguenti potrebbero essere interessati all'uso di MBAM per gestire BitLocker:</span><span class="sxs-lookup"><span data-stu-id="a80a5-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="a80a5-119">Amministratori, professionisti IT per la sicurezza e responsabili della conformità che hanno la responsabilità di garantire che i dati riservati non vengano divulgati senza autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a80a5-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="a80a5-120">Amministratori responsabili della sicurezza dei computer in uffici remoti o succursali</span><span class="sxs-lookup"><span data-stu-id="a80a5-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="a80a5-121">Amministratori responsabili per i computer client che eseguono Windows</span><span class="sxs-lookup"><span data-stu-id="a80a5-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="a80a5-122">**Nota**  BitLocker non è spiegato in dettaglio in questa documentazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="a80a5-123">Per altre informazioni, vedere [Panoramica della crittografia unità BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="a80a5-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a><span data-ttu-id="a80a5-124">Novità di MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="a80a5-124">What’s new in MBAM 2.5 SP1</span></span>


<span data-ttu-id="a80a5-125">Questa sezione descrive le nuove caratteristiche di MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="a80a5-125">This section describes the new features in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="a80a5-126">Lingue appena supportate per il client MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="a80a5-126">Newly Supported Languages for the MBAM 2.5 SP1 Client</span></span>

<span data-ttu-id="a80a5-127">Le seguenti lingue aggiuntive sono ora supportate in MBAM 2,5 SP1 solo per il client MBAM, incluso il portale self-service:</span><span class="sxs-lookup"><span data-stu-id="a80a5-127">The following additional languages are now supported in MBAM 2.5 SP1 for the MBAM Client only, including the Self-Service Portal:</span></span>

<span data-ttu-id="a80a5-128">Ceco (Repubblica Ceca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="a80a5-128">Czech (Czech Republic) cs-CZ</span></span>

<span data-ttu-id="a80a5-129">Danese (Danimarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="a80a5-129">Danish (Denmark) da-DK</span></span>

<span data-ttu-id="a80a5-130">Olandese (Paesi Bassi) nl-NL</span><span class="sxs-lookup"><span data-stu-id="a80a5-130">Dutch (Netherlands) nl-NL</span></span>

<span data-ttu-id="a80a5-131">Fi-FI Finlandese (Finlandia)</span><span class="sxs-lookup"><span data-stu-id="a80a5-131">Finnish (Finland) fi-FI</span></span>

<span data-ttu-id="a80a5-132">Greco (Grecia) el-GR</span><span class="sxs-lookup"><span data-stu-id="a80a5-132">Greek (Greece) el-GR</span></span>

<span data-ttu-id="a80a5-133">Ungherese (Ungheria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="a80a5-133">Hungarian (Hungary) hu-HU</span></span>

<span data-ttu-id="a80a5-134">Norvegese, Bokmål (Norvegia) nb-NO</span><span class="sxs-lookup"><span data-stu-id="a80a5-134">Norwegian, Bokmål (Norway) nb-NO</span></span>

<span data-ttu-id="a80a5-135">Polacco (Polonia) PL-PL</span><span class="sxs-lookup"><span data-stu-id="a80a5-135">Polish (Poland) pl-PL</span></span>

<span data-ttu-id="a80a5-136">Portoghese (Portogallo) PT-PT</span><span class="sxs-lookup"><span data-stu-id="a80a5-136">Portuguese (Portugal) pt-PT</span></span>

<span data-ttu-id="a80a5-137">Slovacco (Slovacchia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="a80a5-137">Slovak (Slovakia) sk-SK</span></span>

<span data-ttu-id="a80a5-138">Sloveno (Slovenia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="a80a5-138">Slovenian (Slovenia) sl-SI</span></span>

<span data-ttu-id="a80a5-139">Svedese (Svezia) SV-SE</span><span class="sxs-lookup"><span data-stu-id="a80a5-139">Swedish (Sweden) sv-SE</span></span>

<span data-ttu-id="a80a5-140">Turco (Turchia) tr-TR</span><span class="sxs-lookup"><span data-stu-id="a80a5-140">Turkish (Turkey) tr-TR</span></span>

<span data-ttu-id="a80a5-141">Per un elenco di tutte le lingue supportate per client e server in MBAM 2,5 e MBAM 2,5 SP1, Vedi le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a80a5-141">For a list of all languages supported for client and server in MBAM 2.5 and MBAM 2.5 SP1, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

### <span data-ttu-id="a80a5-142">Supporto per Windows 10</span><span class="sxs-lookup"><span data-stu-id="a80a5-142">Support for Windows 10</span></span>

<span data-ttu-id="a80a5-143">MBAM 2,5 SP1 aggiunge il supporto per Windows 10 e Windows Server 2016, oltre allo stesso software supportato nelle versioni precedenti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-143">MBAM 2.5 SP1 adds support for Windows 10 and Windows Server 2016, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

<span data-ttu-id="a80a5-144">Windows 10 è supportato in MBAM 2,5 e MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="a80a5-144">Windows 10 is supported in both MBAM 2.5 and MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="a80a5-145">Supporto per Microsoft SQL Server 2014 SP1</span><span class="sxs-lookup"><span data-stu-id="a80a5-145">Support for Microsoft SQL Server 2014 SP1</span></span>

<span data-ttu-id="a80a5-146">MBAM 2,5 SP1 aggiunge il supporto per Microsoft SQL Server 2014 SP1, oltre allo stesso software supportato nelle versioni precedenti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-146">MBAM 2.5 SP1 adds support for Microsoft SQL Server 2014 SP1, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <span data-ttu-id="a80a5-147">MBAM non viene più distribuito con MSI separato</span><span class="sxs-lookup"><span data-stu-id="a80a5-147">MBAM no longer ships with separate MSI</span></span>

<span data-ttu-id="a80a5-148">A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-148">Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="a80a5-149">È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.</span><span class="sxs-lookup"><span data-stu-id="a80a5-149">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

### <span data-ttu-id="a80a5-150">MBAM può le password di OwnerAuth escrow senza possedere il TPM</span><span class="sxs-lookup"><span data-stu-id="a80a5-150">MBAM can escrow OwnerAuth passwords without owning the TPM</span></span>

<span data-ttu-id="a80a5-151">In precedenza, se MBAM non fosse il proprietario del TPM, il TPM OwnerAuth non poteva essere escrowed al database MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-151">Previously, if MBAM did not own the TPM, the TPM OwnerAuth could not be escrowed to the MBAM database.</span></span> <span data-ttu-id="a80a5-152">Per configurare MBAM per il proprio TPM e per archiviare le password, è stato necessario disabilitare il provisioning automatico del TPM e cancellare il TPM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="a80a5-152">To configure MBAM to own the TPM and to store the passwords, you had to disable TPM auto-provisioning and clear the TPM on the client computer.</span></span>

<span data-ttu-id="a80a5-153">In Windows 8 e versioni successive, MBAM 2,5 SP1 può ora escrow le password di OwnerAuth senza possedere il TPM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-153">In Windows 8 and higher, MBAM 2.5 SP1 can now escrow the OwnerAuth passwords without owning the TPM.</span></span> <span data-ttu-id="a80a5-154">Durante l'avvio del servizio, MBAM esegue una query per verificare se il TPM è già di proprietà e, in caso affermativo, richiede le password del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a80a5-154">During service startup, MBAM queries to see if the TPM is already owned and if so, it requests the passwords from the operating system.</span></span> <span data-ttu-id="a80a5-155">Le password vengono poi escrowed al database MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-155">The passwords are then escrowed to the MBAM database.</span></span> <span data-ttu-id="a80a5-156">Inoltre, i criteri di gruppo devono essere impostati per impedire che OwnerAuth venga eliminato localmente.</span><span class="sxs-lookup"><span data-stu-id="a80a5-156">In addition, Group Policy must be set to prevent the OwnerAuth from being deleted locally.</span></span>

<span data-ttu-id="a80a5-157">In Windows 7, MBAM deve possedere il TPM per l'escrow automaticamente le informazioni di OwnerAuth del TPM nel database MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-157">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="a80a5-158">Se MBAM non è il proprietario del TPM e il backup di Active Directory (AD) del TPM è configurato tramite criteri di gruppo, è necessario usare i **cmdlet di importazione di dati di mbam Active Directory (ad)** per copiare il TPM OwnerAuth da un annuncio nel database mbam.</span><span class="sxs-lookup"><span data-stu-id="a80a5-158">If MBAM does not own the TPM and Active Directory (AD) backup of the TPM is configured through Group Policy, you must use the **MBAM Active Directory (AD) Data Import cmdlets** to copy TPM OwnerAuth from AD into the MBAM database.</span></span> <span data-ttu-id="a80a5-159">Questi sono cinque nuovi cmdlet di PowerShell che prepopolano i database di MBAM con le informazioni sul recupero di volume e sul proprietario del TPM archiviate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a80a5-159">These are five new PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="a80a5-160">Per altre informazioni, Vedi [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="a80a5-160">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

### <span data-ttu-id="a80a5-161">MBAM può sbloccare automaticamente il TPM dopo un blocco</span><span class="sxs-lookup"><span data-stu-id="a80a5-161">MBAM can automatically unlock the TPM after a lockout</span></span>

<span data-ttu-id="a80a5-162">Nei computer che eseguono TPM 1,2 è ora possibile configurare MBAM per sbloccare automaticamente il TPM in caso di blocco.</span><span class="sxs-lookup"><span data-stu-id="a80a5-162">On computers running TPM 1.2, you can now configure MBAM to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="a80a5-163">Se la caratteristica di ripristino automatico del blocco TPM è abilitata, MBAM può rilevare che un utente è bloccato e quindi ottenere la password di OwnerAuth dal database MBAM per sbloccare automaticamente il TPM per l'utente.</span><span class="sxs-lookup"><span data-stu-id="a80a5-163">If the TPM lockout auto reset feature is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span>

<span data-ttu-id="a80a5-164">Questa caratteristica deve essere abilitata sia sul lato server che in criteri di gruppo sul lato client.</span><span class="sxs-lookup"><span data-stu-id="a80a5-164">This feature must be enabled on both the server side and in Group Policy on the client side.</span></span> <span data-ttu-id="a80a5-165">Per altre informazioni, Vedi [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).</span><span class="sxs-lookup"><span data-stu-id="a80a5-165">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-autounlock).</span></span>

### <span data-ttu-id="a80a5-166">Supporto per le protezioni per le password numeriche di BitLocker conformi a FIPS</span><span class="sxs-lookup"><span data-stu-id="a80a5-166">Support for FIPS-compliant BitLocker numerical password protectors</span></span>

<span data-ttu-id="a80a5-167">In MBAM 2.5 è stato aggiunto il supporto per le chiavi di ripristino di BitLocker conformi alla Federal Information Processing Standard (FIPS) nei dispositivi che gestiscono il sistema operativo Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="a80a5-167">In MBAM2.5, support was added for Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices running the Windows 8.1 operating system.</span></span> <span data-ttu-id="a80a5-168">Tuttavia, Windows non ha implementato le chiavi di ripristino conformi FIPS in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a80a5-168">However, Windows did not implement FIPS-compliant recovery keys in Windows 7.</span></span> <span data-ttu-id="a80a5-169">Di conseguenza, i dispositivi Windows 7 e Windows 8 richiedevano ancora una protezione DRA (Data Recovery Agent) per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="a80a5-169">Therefore, Windows 7 and Windows 8 devices still required a Data Recovery Agent (DRA) protector for recovery.</span></span>

<span data-ttu-id="a80a5-170">Il team di Windows ha le chiavi di ripristino conformi allo standard FIPS con un hotfix e MBAM 2,5 SP1 ha aggiunto il supporto anche per loro.</span><span class="sxs-lookup"><span data-stu-id="a80a5-170">The Windows team has backported FIPS-compliant recovery keys with a hotfix, and MBAM 2.5 SP1 has added support for them as well.</span></span>

<span data-ttu-id="a80a5-171">**Nota**  I computer client che eseguono il sistema operativo Windows8 richiedono ancora una protezione DRA perché l'hotfix non è stato sottoportato al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a80a5-171">**Note** Client computers that are running the Windows8 operating system still require a DRA protector since the hotfix was not backported to that OS.</span></span> <span data-ttu-id="a80a5-172">Vedere [pacchetto hotfix 2 per l'amministrazione e il monitoraggio di bitlocker 2,5](https://support.microsoft.com/kb/3015477) per scaricare e installare i computer hotfix per Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a80a5-172">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span> <span data-ttu-id="a80a5-173">Per informazioni su DRA, vedere [uso di agenti di recupero dati con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="a80a5-173">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

 

<span data-ttu-id="a80a5-174">Per abilitare la conformità FIPS nell'organizzazione, è necessario configurare le impostazioni dei criteri di gruppo FIPS (Federal Information Processing Standard).</span><span class="sxs-lookup"><span data-stu-id="a80a5-174">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="a80a5-175">Per istruzioni sulla configurazione, vedere [impostazioni dei criteri di gruppo di BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="a80a5-175">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

### <span data-ttu-id="a80a5-176">Personalizzare il messaggio di ripristino di pre-avvio e l'URL con le nuove impostazioni di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a80a5-176">Customize pre-boot recovery message and URL with new Group Policy setting</span></span>

<span data-ttu-id="a80a5-177">Una nuova impostazione di criteri di gruppo, **Configura l'URL e il messaggio di ripristino di pre-avvio**, consente di configurare un messaggio di ripristino personalizzato o di specificare un URL che viene quindi visualizzato nella schermata di ripristino di BitLocker di pre-avvio quando l'unità del sistema operativo è bloccata.</span><span class="sxs-lookup"><span data-stu-id="a80a5-177">A new Group Policy setting, **Configure pre-boot recovery message and URL**, lets you configure a custom recovery message or specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="a80a5-178">Questa impostazione è disponibile solo nei computer client che eseguono Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a80a5-178">This setting is only available on client computers running Windows 10.</span></span>

<span data-ttu-id="a80a5-179">Se si abilita questa impostazione per i criteri, è possibile selezionare una di queste opzioni per il messaggio di ripristino di pre-avvio:</span><span class="sxs-lookup"><span data-stu-id="a80a5-179">If you enable this policy setting, you can you can select one of these options for the pre-boot recovery message:</span></span>

-   <span data-ttu-id="a80a5-180">**Usare il messaggio di ripristino personalizzato**: selezionare questa opzione per includere un messaggio personalizzato nella schermata di ripristino di BitLocker di pre-avvio.</span><span class="sxs-lookup"><span data-stu-id="a80a5-180">**Use custom recovery message**: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="a80a5-181">**Usare l'URL di ripristino personalizzato**: selezionare questa opzione per sostituire l'URL predefinito visualizzato nella schermata di ripristino di BitLocker di pre-avvio.</span><span class="sxs-lookup"><span data-stu-id="a80a5-181">**Use custom recovery URL**: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="a80a5-182">**Usare l'URL e il messaggio di ripristino predefiniti**: selezionare questa opzione per visualizzare il messaggio e l'URL di ripristino di BitLocker predefiniti nella schermata di ripristino di BitLocker di pre-avvio.</span><span class="sxs-lookup"><span data-stu-id="a80a5-182">**Use default recovery message and URL**: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="a80a5-183">Se in precedenza è stato configurato un URL o un messaggio di ripristino personalizzato e si vuole ripristinare il messaggio predefinito, è necessario abilitare questo criterio e selezionare questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a80a5-183">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select this option.</span></span>

<span data-ttu-id="a80a5-184">La nuova impostazione di criteri di gruppo è disponibile nel nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)** &gt; **drive del sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="a80a5-184">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span> <span data-ttu-id="a80a5-185">Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a80a5-185">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="a80a5-186">MBAM ha aggiunto il supporto per la crittografia dello spazio usato</span><span class="sxs-lookup"><span data-stu-id="a80a5-186">MBAM added support for Used Space Encryption</span></span>

<span data-ttu-id="a80a5-187">In MBAM 2,5 SP1, se si Abilita la crittografia dello spazio usato tramite criteri di gruppo di BitLocker, il client MBAM lo onora.</span><span class="sxs-lookup"><span data-stu-id="a80a5-187">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group Policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="a80a5-188">Questa impostazione di criteri di gruppo è denominata **Applica tipo di crittografia unità sulle unità del sistema operativo** e si trova nel nodo GPO seguente: **configurazione di computer** &gt; **modelli amministrativi** &gt; **componenti di Windows** &gt; **unità BitLocker Drive** &gt; **System**Encryption.</span><span class="sxs-lookup"><span data-stu-id="a80a5-188">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="a80a5-189">Se si Abilita questo criterio e si seleziona il tipo di crittografia come **solo spazio usato**per la crittografia, mbam consentirà di rispettare i criteri e BitLocker crittografa solo lo spazio su disco usato nel volume.</span><span class="sxs-lookup"><span data-stu-id="a80a5-189">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

<span data-ttu-id="a80a5-190">Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a80a5-190">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="a80a5-191">Supporto di MBAM client per dischi rigidi crittografati</span><span class="sxs-lookup"><span data-stu-id="a80a5-191">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="a80a5-192">MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="a80a5-192">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="a80a5-193">Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="a80a5-193">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="a80a5-194">Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a80a5-194">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

### <span data-ttu-id="a80a5-195">La configurazione della delega non è più necessaria durante la registrazione di nomi SPN</span><span class="sxs-lookup"><span data-stu-id="a80a5-195">Delegation configuration no longer required when registering SPNs</span></span>

<span data-ttu-id="a80a5-196">Il requisito per configurare la delega vincolata per i nomi SPN registrati per l'account del pool di applicazioni non è più necessario in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="a80a5-196">The requirement to configure constrained delegation for SPNs that you register for the application pool account is no longer necessary in MBAM 2.5 SP1.</span></span> <span data-ttu-id="a80a5-197">Tuttavia, è ancora un requisito per MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a80a5-197">However, it is still a requirement for MBAM 2.5.</span></span>

### <span data-ttu-id="a80a5-198">Abilitare BitLocker tramite MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="a80a5-198">Enable BitLocker using MBAM as Part of a Windows Deployment</span></span>

<span data-ttu-id="a80a5-199">In MBAM 2,5 SP1, è possibile usare uno script di PowerShell per configurare le chiavi di ripristino unità BitLocker e di recupero escrow nel server MBAM.</span><span class="sxs-lookup"><span data-stu-id="a80a5-199">In MBAM 2.5 SP1, you can use a PowerShell script to configure BitLocker drive encryption and escrow recovery keys to the MBAM Server.</span></span>

<span data-ttu-id="a80a5-200">Per altre informazioni, vedere [come abilitare BitLocker tramite mbam come parte di una distribuzione di Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span><span class="sxs-lookup"><span data-stu-id="a80a5-200">For more information, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span></span>

### <span data-ttu-id="a80a5-201">Il portale self-service può essere personalizzato usando PowerShell o la procedura guidata di personalizzazione del provider di servizi condivisi</span><span class="sxs-lookup"><span data-stu-id="a80a5-201">Self-Service Portal can be customized by using either PowerShell or the SSP customization wizard</span></span>

<span data-ttu-id="a80a5-202">A partire da MBAM 2,5 SP1, il portale self-service può essere configurato usando la procedura guidata per la personalizzazione e l'uso di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a80a5-202">As of MBAM 2.5 SP1, the Self-Service Portal can be configured by using the customization wizard as well as by using PowerShell.</span></span> <span data-ttu-id="a80a5-203">Vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a80a5-203">See [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

### <span data-ttu-id="a80a5-204">Il Web browser non viene più eseguito involontariamente come amministratore</span><span class="sxs-lookup"><span data-stu-id="a80a5-204">Web browser no longer unintentionally runs as administrator</span></span>

<span data-ttu-id="a80a5-205">Un problema in MBAM 2,5 ha causato collegamenti della guida nello strumento di configurazione del server per consentire l'apertura delle finestre del browser con i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a80a5-205">An issue in MBAM 2.5 caused help links in the Server Configuration tool to cause browser windows to open with administrator rights.</span></span> <span data-ttu-id="a80a5-206">Questo problema è stato risolto in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="a80a5-206">This issue is fixed in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="a80a5-207">Non è più necessario scaricare i file JavaScript per configurare il portale self-service quando la rete CDN non è accessibile</span><span class="sxs-lookup"><span data-stu-id="a80a5-207">No longer need to download the JavaScript files to configure the Self-Service Portal when the CDN is inaccessible</span></span>

<span data-ttu-id="a80a5-208">In MBAM 2,5 e versioni precedenti, i file jQuery usati per la configurazione del portale self-service dovevano essere scaricati dalla rete CDN in anticipo se i client che accedevano al portale self-service non avevano accesso a Internet.</span><span class="sxs-lookup"><span data-stu-id="a80a5-208">In MBAM 2.5 and earlier, the jQuery files used for configuration of the Self-Service Portal had to be downloaded from the CDN in advance if clients accessing the Self-Service Portal did not have internet access.</span></span> <span data-ttu-id="a80a5-209">In MBAM 2,5 SP1 tutti i file JavaScript sono inclusi nel prodotto, quindi non è necessario scaricarli.</span><span class="sxs-lookup"><span data-stu-id="a80a5-209">In MBAM 2.5 SP1, all JavaScript files are included in the product, so downloading them is unnecessary.</span></span>

### <span data-ttu-id="a80a5-210">I report possono essere aperti in Generatore report 3,0</span><span class="sxs-lookup"><span data-stu-id="a80a5-210">Reports can be opened in Report Builder 3.0</span></span>

<span data-ttu-id="a80a5-211">In MBAM 2,5 SP1 i report sono stati aggiornati allo schema del linguaggio di definizione del report più recente, consentendo agli utenti di aprire e personalizzare i report in Generatore report 3,0 e di salvarli immediatamente senza danneggiare il file di report.</span><span class="sxs-lookup"><span data-stu-id="a80a5-211">In MBAM 2.5 SP1, the reports have been updated to the latest report definition language schema, allowing users to open and customize the reports in Report Builder 3.0 and save them immediately without corrupting the report file.</span></span>

### <span data-ttu-id="a80a5-212">Nuovi cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="a80a5-212">New PowerShell cmdlets</span></span>

<span data-ttu-id="a80a5-213">I nuovi cmdlet di PowerShell per MBAM 2,5 SP1 consentono di configurare e gestire diverse funzionalità di MBAM, tra cui database, report e applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="a80a5-213">New PowerShell cmdlets for MBAM 2.5 SP1 enable you to configure and manage different MBAM features, including databases, reports, and web applications.</span></span> <span data-ttu-id="a80a5-214">Ogni funzionalità include un cmdlet di PowerShell corrispondente che puoi usare per abilitare o disabilitare le funzionalità o per ottenere informazioni sulla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a80a5-214">Each feature has a corresponding PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="a80a5-215">I cmdlet seguenti sono stati implementati per MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="a80a5-215">The following cmdlets have been implemented for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="a80a5-216">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="a80a5-216">Write-MbamTpmInformation</span></span>

-   <span data-ttu-id="a80a5-217">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="a80a5-217">Write-MbamRecoveryInformation</span></span>

-   <span data-ttu-id="a80a5-218">Read-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="a80a5-218">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="a80a5-219">Read-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="a80a5-219">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="a80a5-220">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="a80a5-220">Write-MbamComputerUser</span></span>

<span data-ttu-id="a80a5-221">I parametri seguenti sono stati implementati nei cmdlet Enable-MbamWebApplication e test-MbamWebApplication per MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="a80a5-221">The following parameters have been implemented in the Enable-MbamWebApplication and Test-MbamWebApplication cmdlets for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="a80a5-222">DataMigrationAccessGroup</span><span class="sxs-lookup"><span data-stu-id="a80a5-222">DataMigrationAccessGroup</span></span>

-   <span data-ttu-id="a80a5-223">TpmAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="a80a5-223">TpmAutoUnlock</span></span>

<span data-ttu-id="a80a5-224">Per informazioni sui cmdlet, vedere Considerazioni sulla [sicurezza di MBAM 2,5](mbam-25-security-considerations.md) e [Guida per i cmdlet di amministrazione e monitoraggio di Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).</span><span class="sxs-lookup"><span data-stu-id="a80a5-224">For information about the cmdlets, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md) and [Microsoft Bitlocker Administration and Monitoring Cmdlet Help](https://technet.microsoft.com/library/dn720418.aspx).</span></span>

### <span data-ttu-id="a80a5-225">L'agente MBAM rileva la modalità presentazione</span><span class="sxs-lookup"><span data-stu-id="a80a5-225">MBAM agent detects presentation mode</span></span>

<span data-ttu-id="a80a5-226">L'agente MBAM può rilevare quando il computer è in modalità presentazione ed evitare di richiamare l'interfaccia utente di MBAM in quel momento.</span><span class="sxs-lookup"><span data-stu-id="a80a5-226">The MBAM agent can detect when the computer is in presentation mode and avoid invoking the MBAM UI at that time.</span></span>

### <span data-ttu-id="a80a5-227">Servizio di agente MBAM ora configurato per l'uso dell'avvio ritardato</span><span class="sxs-lookup"><span data-stu-id="a80a5-227">MBAM agent service now configured to use delayed start</span></span>

<span data-ttu-id="a80a5-228">Dopo l'installazione, il servizio imposta il servizio MBAM Agent per l'uso dell'avvio ritardato, diminuendo la quantità di tempo necessaria per avviare Windows.</span><span class="sxs-lookup"><span data-stu-id="a80a5-228">After installation, the service will now set the MBAM agent service to use delayed start, decreasing the amount of time it takes to start Windows.</span></span>

### <span data-ttu-id="a80a5-229">I volumi di dati fissi bloccati vengono ora segnalati come conformi</span><span class="sxs-lookup"><span data-stu-id="a80a5-229">Locked Fixed Data volumes now report as Compliant</span></span>

<span data-ttu-id="a80a5-230">La logica di calcolo della conformità per i volumi "bloccati per i dati fissi" è stata cambiata per segnalare i volumi come "conforme", ma con uno stato di protezione e la crittografia dello stato "sconosciuto" e con un dettaglio dello stato di conformità di "volume bloccato".</span><span class="sxs-lookup"><span data-stu-id="a80a5-230">The compliance calculation logic for "Locked Fixed Data" volumes has been changed to report the volumes as "Compliant," but with a Protector State and Encryption State of "Unknown" and with a Compliance Status Detail of "Volume is locked".</span></span> <span data-ttu-id="a80a5-231">In precedenza, i volumi bloccati venivano segnalati come "non conformi", uno stato di protezione "crittografato", uno stato di crittografia "sconosciuto" e un dettaglio dello stato di conformità di "errore sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="a80a5-231">Previously, locked volumes were reported as “Non-Compliant”, a Protector State of "Encrypted", an Encryption State of "Unknown", and a Compliance Status Detail of "An unknown error".</span></span>


## <span data-ttu-id="a80a5-232">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="a80a5-232">How to Get MDOP Technologies</span></span>


<span data-ttu-id="a80a5-233">MBAM fa parte del Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="a80a5-233">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="a80a5-234">MDOP fa parte del programma Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="a80a5-234">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="a80a5-235">Per altre informazioni sul programma Microsoft Software Assurance e su come acquisire il MDOP, vedere [come si ottiene MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="a80a5-235">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="a80a5-236">Note sulla versione di MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="a80a5-236">MBAM 2.5 SP1 Release Notes</span></span>


<span data-ttu-id="a80a5-237">Per altre informazioni e notizie aggiornate che non sono incluse in questa documentazione, vedere note sulla [versione per MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="a80a5-237">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5 SP1](release-notes-for-mbam-25-sp1.md).</span></span>

## <span data-ttu-id="a80a5-238">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="a80a5-238">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a80a5-239">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a80a5-239">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a80a5-240">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a80a5-240">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="a80a5-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a80a5-241">Related topics</span></span>


[<span data-ttu-id="a80a5-242">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="a80a5-242">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="a80a5-243">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a80a5-243">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





