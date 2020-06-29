---
title: Informazioni su MBAM 2.5
description: Informazioni su MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824215"
---
# <span data-ttu-id="a2fc6-103">Informazioni su MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a2fc6-103">About MBAM 2.5</span></span>


<span data-ttu-id="a2fc6-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 offre un'interfaccia amministrativa semplificata per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="a2fc6-105">BitLocker offre una protezione avanzata per il furto di dati o l'esposizione ai dati per i computer persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="a2fc6-106">BitLocker crittografa tutti i dati archiviati nei volumi e nelle unità del sistema operativo Windows e nelle unità dati configurate.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-106">BitLocker encrypts all data that is stored on the Windows operating system volumes and drives and configured data drives.</span></span>

## <span data-ttu-id="a2fc6-107">Panoramica di MBAM</span><span class="sxs-lookup"><span data-stu-id="a2fc6-107">Overview of MBAM</span></span>


<span data-ttu-id="a2fc6-108">MBAM 2,5 ha le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-108">MBAM 2.5 has the following features:</span></span>

-   <span data-ttu-id="a2fc6-109">Consente agli amministratori di automatizzare il processo di crittografia dei volumi nei computer client in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="a2fc6-110">Consente agli addetti alla sicurezza di determinare rapidamente lo stato di conformità dei singoli computer o anche dell'organizzazione stessa.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="a2fc6-111">Fornisce Reporting centralizzato e gestione hardware con Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="a2fc6-112">Riduce il carico di lavoro nell'help desk per aiutare gli utenti finali con le richieste di chiavi di ripristino e PIN di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="a2fc6-113">Consente agli utenti finali di recuperare i dispositivi crittografati in modo indipendente usando il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="a2fc6-114">Consente agli addetti alla sicurezza di controllare facilmente l'accesso per recuperare le informazioni chiave.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="a2fc6-115">Consente agli utenti di Windows Enterprise di continuare a lavorare ovunque con la garanzia che i loro dati aziendali siano protetti.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="a2fc6-116">MBAM applica le opzioni dei criteri di crittografia di BitLocker impostate per l'organizzazione, monitora la conformità dei computer client con tali criteri e segnala lo stato di crittografia dei computer dell'organizzazione e dell'individuo.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="a2fc6-117">Inoltre, MBAM consente di accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambiano i record del BIOS o del boot.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="a2fc6-118">I gruppi seguenti potrebbero essere interessati all'uso di MBAM per gestire BitLocker:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="a2fc6-119">Amministratori, professionisti IT per la sicurezza e responsabili della conformità che hanno la responsabilità di garantire che i dati riservati non vengano divulgati senza autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a2fc6-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="a2fc6-120">Amministratori responsabili della sicurezza dei computer in uffici remoti o succursali</span><span class="sxs-lookup"><span data-stu-id="a2fc6-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="a2fc6-121">Amministratori responsabili per i computer client che eseguono Windows</span><span class="sxs-lookup"><span data-stu-id="a2fc6-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="a2fc6-122">**Nota**  BitLocker non è spiegato in dettaglio in questa documentazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="a2fc6-123">Per altre informazioni, vedere [Panoramica della crittografia unità BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5"></a><span data-ttu-id="a2fc6-124">Novità di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="a2fc6-124">What’s new in MBAM 2.5</span></span>


<span data-ttu-id="a2fc6-125">Questa sezione descrive le nuove caratteristiche di MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-125">This section describes the new features in MBAM 2.5.</span></span>

### <span data-ttu-id="a2fc6-126">Supporto per Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="a2fc6-126">Support for Microsoft SQL Server 2014</span></span>

<span data-ttu-id="a2fc6-127">MBAM aggiunge il supporto per Microsoft SQL Server 2014, oltre allo stesso software supportato nelle versioni precedenti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-127">MBAM adds support for Microsoft SQL Server 2014, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> <span data-ttu-id="a2fc6-128">Modelli di criteri di gruppo di MBAM scaricati separatamente</span><span class="sxs-lookup"><span data-stu-id="a2fc6-128">MBAM Group Policy Templates downloaded separately</span></span>

<span data-ttu-id="a2fc6-129">I modelli dei criteri di gruppo di MBAM devono essere scaricati separatamente dall'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-129">The MBAM Group Policy Templates must be downloaded separately from the MBAM installation.</span></span> <span data-ttu-id="a2fc6-130">Nelle versioni precedenti di MBAM, il programma di installazione di MBAM includeva un modello di criteri di MBAM, che conteneva gli oggetti Criteri di gruppo specifici per MBAM che definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-130">In previous versions of MBAM, the MBAM installer included an MBAM Policy Template, which contained the required MBAM-specific Group Policy Objects (GPOs) that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="a2fc6-131">Questi GPO sono stati rimossi dal programma di installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-131">These GPOs have been removed from the MBAM installer.</span></span> <span data-ttu-id="a2fc6-132">Ora scarichi i GPO da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation prima di iniziare l'installazione del client mbam.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-132">You now download the GPOs from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation before you begin the MBAM Client installation.</span></span> <span data-ttu-id="a2fc6-133">È possibile copiare i modelli di criteri di gruppo in qualsiasi server o workstation in cui è in esecuzione una versione supportata del sistema operativo Windows Server o Windows.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-133">You can copy the Group Policy Templates to any server or workstation that is running a supported version of the Windows Server or Windows operating system.</span></span>

<span data-ttu-id="a2fc6-134">**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-134">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="a2fc6-135">Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-135">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the BitLocker Drive Encryption settings for you.</span></span>

 

<span data-ttu-id="a2fc6-136">I file di modello che è necessario copiare in un server o una workstation sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-136">The template files that you need to copy to a server or workstation are:</span></span>

-   <span data-ttu-id="a2fc6-137">BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="a2fc6-137">BitLockerManagement.adml</span></span>

-   <span data-ttu-id="a2fc6-138">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="a2fc6-138">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="a2fc6-139">BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="a2fc6-139">BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="a2fc6-140">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="a2fc6-140">BitLockerUserManagement.admx</span></span>

<span data-ttu-id="a2fc6-141">Copiare i file del modello nella posizione più adatta alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-141">Copy the template files to the location that best meets your needs.</span></span> <span data-ttu-id="a2fc6-142">Per i file specifici della lingua, che devono essere copiati in una cartella specifica della lingua, è necessaria la console Gestione criteri di gruppo per visualizzare i file.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-142">For the language-specific files, which must be copied to a language-specific folder, the Group Policy Management Console is required to view the files.</span></span>

- <span data-ttu-id="a2fc6-143">Per installare i file del modello localmente in un server o una workstation, copiare i file in uno dei percorsi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-143">To install the template files locally on a server or workstation, copy the files to one of the following locations.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="a2fc6-144">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="a2fc6-144">File type</span></span></th>
  <th align="left"><span data-ttu-id="a2fc6-145">Percorso del file</span><span class="sxs-lookup"><span data-stu-id="a2fc6-145">File location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="a2fc6-146">lingua indipendente (con estensione ADMX)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-146">language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="a2fc6-147">% SystemRoot% </em> \policyDefinitions</span><span class="sxs-lookup"><span data-stu-id="a2fc6-147">%systemroot%</em>\policyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a2fc6-148">linguaggio specifico (con estensione adml)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-148">language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="a2fc6-149">% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (ad esempio, il file specifico della lingua inglese degli Stati Uniti verrà archiviato in <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-149">%systemroot%</em>\policyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language specific file will be stored in <em>%systemroot%&lt;/em&gt;policyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

- <span data-ttu-id="a2fc6-150">Per rendere i modelli disponibili per tutti gli amministratori dei criteri di gruppo in un dominio, copiare i file in una delle posizioni seguenti in un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-150">To make the templates available to all Group Policy administrators in a domain, copy the files to one of the following locations on a domain controller.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="a2fc6-151">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="a2fc6-151">File type</span></span></th>
  <th align="left"><span data-ttu-id="a2fc6-152">Posizione del file del controller di dominio</span><span class="sxs-lookup"><span data-stu-id="a2fc6-152">Domain controller file location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="a2fc6-153">Lingua indipendente (con estensione ADMX)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-153">Language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="a2fc6-154">% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="a2fc6-154">%systemroot%</em>sysvol\domain\policies\PolicyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="a2fc6-155">Linguaggio specifico (con estensione adml)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-155">Language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="a2fc6-156">% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (ad esempio, il file specifico della lingua inglese degli Stati Uniti verrà archiviato in <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-us)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-156">%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language-specific file will be stored in <em>%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

<span data-ttu-id="a2fc6-157">Per altre informazioni sui file di modello, vedere [gestione dettagliata dei file ADMX di criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=392818).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-157">For more information about template files, see [Managing Group Policy ADMX Files Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=392818).</span></span>

### <span data-ttu-id="a2fc6-158">Possibilità di applicare criteri di crittografia nel sistema operativo e nelle unità dati fisse</span><span class="sxs-lookup"><span data-stu-id="a2fc6-158">Ability to enforce encryption policies on operating system and fixed data drives</span></span>

<span data-ttu-id="a2fc6-159">MBAM 2.5 consente di applicare criteri di crittografia nel sistema operativo e nelle unità dati fisse per i computer dell'organizzazione e limitare il numero di giorni in cui gli utenti finali possono richiedere il rinvio del requisito per conformarsi ai criteri di crittografia di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-159">MBAM2.5 enables you to enforce encryption policies on operating system and fixed data drives for computers in your organization and limit the number of days that end users can request a postponement of the requirement to comply with MBAM encryption policies.</span></span>

<span data-ttu-id="a2fc6-160">Per consentire la configurazione dell'imposizione dei criteri di crittografia, è stata aggiunta una nuova impostazione di criteri di gruppo, denominata impostazioni per l'applicazione di criteri di crittografia, per le unità di sistema operativo e le unità dati fisse.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-160">To enable you to configure encryption policy enforcement, a new Group Policy setting, called Encryption Policy Enforcement Settings, has been added for operating system drives and fixed data drives.</span></span> <span data-ttu-id="a2fc6-161">Questo criterio è descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-161">This policy is described in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2fc6-162">Impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a2fc6-162">Group Policy setting</span></span></th>
<th align="left"><span data-ttu-id="a2fc6-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2fc6-163">Description</span></span></th>
<th align="left"><span data-ttu-id="a2fc6-164">Nodo Criteri di gruppo usato per configurare questa impostazione</span><span class="sxs-lookup"><span data-stu-id="a2fc6-164">Group Policy node used to configure this setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fc6-165">Impostazioni per l'applicazione dei criteri di crittografia (unità del sistema operativo)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-165">Encryption Policy Enforcement Settings (Operating System Drive)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-166">Per questa impostazione, usare l'opzione <strong> Configura il numero di giorni del periodo di tolleranza per la mancata conformità per le unità del sistema operativo </strong> per configurare un periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-166">For this setting, use the option <strong>Configure the number of noncompliance grace period days for operating system drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="a2fc6-167">Il periodo di tolleranza specifica il numero di giorni in cui gli utenti finali possono rinviare la conformità con i criteri di MBAM per l'unità del sistema operativo dopo che l'unità è stata rilevata come non conforme.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-167">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their operating system drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="a2fc6-168">Dopo la scadenza del periodo di tolleranza configurato, gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-168">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="a2fc6-169">Se è necessaria l'interazione dell'utente, ad esempio se si usa il modulo TPM (Trusted Platform Module) + PIN o con una password Protector, viene visualizzata una finestra di dialogo e gli utenti non possono chiuderlo finché non vengono fornite le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-169">If user interaction is required (for example, if you are using the Trusted Platform Module (TPM) + PIN or using a password protector), a dialog box appears, and users cannot close it until they provide the required information.</span></span> <span data-ttu-id="a2fc6-170">Se il Protector è solo TPM, la crittografia inizia immediatamente in background senza l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-170">If the protector is TPM only, encryption begins immediately in the background without user input.</span></span></p>
<p><span data-ttu-id="a2fc6-171">Gli utenti non possono richiedere esenzioni tramite la crittografia guidata BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-171">Users cannot request exemptions through the BitLocker encryption wizard.</span></span> <span data-ttu-id="a2fc6-172">Devono invece contattare il proprio help desk o usare qualsiasi processo che l'organizzazione usa per le richieste di esenzione.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-172">Instead, they must contact their Help Desk or use whatever process their organization uses for exemption requests.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-173">Criteri di configurazione del computer &gt; &gt; modelli amministrativi di &gt; Windows Components &gt; MDOP mbam (BitLocker Management) &gt; drive del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a2fc6-173">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Operating System Drive</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fc6-174">Impostazioni per l'applicazione dei criteri di crittografia (unità dati fisse)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-174">Encryption Policy Enforcement Settings (Fixed Data Drives)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-175">Per questa impostazione, usare l'opzione <strong> Configura il numero di giorni di periodo di tolleranza per le unità fisse per la </strong> configurazione di un periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-175">For this setting, use the option <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="a2fc6-176">Il periodo di tolleranza specifica il numero di giorni in cui gli utenti finali possono rinviare la conformità con i criteri di MBAM per l'unità fissa dopo che l'unità è stata rilevata come non conforme.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-176">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their fixed drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="a2fc6-177">Il periodo di tolleranza inizia quando l'unità fissa viene determinata come non conforme.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-177">The grace period begins when the fixed drive is determined to be noncompliant.</span></span> <span data-ttu-id="a2fc6-178">Se si usa il comando di sblocco automatico, il criterio non verrà applicato finché l'unità del sistema operativo non è conforme.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-178">If you are using auto-unlock, the policy will not be enforced until the operating system drive is compliant.</span></span> <span data-ttu-id="a2fc6-179">Tuttavia, se non si usa l'opzione di sblocco automatico, la crittografia dell'unità dati fisse può iniziare prima che l'unità del sistema operativo sia completamente crittografata.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-179">However, if you are not using auto-unlock, encryption of the fixed data drive can begin before the operating system drive is fully encrypted.</span></span></p>
<p><span data-ttu-id="a2fc6-180">Dopo la scadenza del periodo di tolleranza configurato, gli utenti non possono rinviare l'azione richiesta o richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-180">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span> <span data-ttu-id="a2fc6-181">Se è necessaria l'interazione dell'utente, viene visualizzata una finestra di dialogo e gli utenti non possono chiuderlo finché non vengono fornite le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-181">If user interaction is required, a dialog box appears and users cannot close it until they provide the required information.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-182">Criteri di configurazione del computer &gt; &gt; modelli amministrativi di &gt; Windows Components &gt; MDOP mbam (Gestione BitLocker) &gt; unità fissa</span><span class="sxs-lookup"><span data-stu-id="a2fc6-182">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Fixed Drive</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a2fc6-183">Possibilità di specificare un URL nella configurazione guidata unità BitLocker per selezionare i criteri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="a2fc6-183">Ability to provide a URL in the BitLocker Drive Encryption wizard to point to your security policy</span></span>

<span data-ttu-id="a2fc6-184">Una nuova impostazione di criteri di gruppo, **specificare l'URL del collegamento ai criteri di sicurezza**, consente di configurare un URL che verrà presentato agli utenti finali come collegamento denominato **criteri di sicurezza aziendale**.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-184">A new Group Policy setting, **Provide the URL for the Security Policy link**, enables you to configure a URL that will be presented to end users as a link called **Company Security Policy**.</span></span> <span data-ttu-id="a2fc6-185">Questo link verrà visualizzato quando MBAM richiede agli utenti di crittografare un volume.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-185">This link will appear when MBAM prompts users to encrypt a volume.</span></span>

<span data-ttu-id="a2fc6-186">Se si abilita questa impostazione, è possibile configurare l'URL per il collegamento ai **criteri di sicurezza aziendali** .</span><span class="sxs-lookup"><span data-stu-id="a2fc6-186">If you enable this policy setting, you can configure the URL for the **Company Security Policy** link.</span></span> <span data-ttu-id="a2fc6-187">Se si disattiva o non si configura questa impostazione per i criteri, il collegamento **criteri di sicurezza aziendali** non viene visualizzato agli utenti.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-187">If you disable or do not configure this policy setting, the **Company Security Policy** link is not displayed to users.</span></span>

<span data-ttu-id="a2fc6-188">La nuova impostazione di criteri di gruppo è disponibile nel nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management) &gt; Client Management**.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-188">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management) &gt; Client Management**.</span></span>

### <span data-ttu-id="a2fc6-189">Supporto per le chiavi di ripristino conformi FIPS</span><span class="sxs-lookup"><span data-stu-id="a2fc6-189">Support for FIPS-compliant recovery keys</span></span>

<span data-ttu-id="a2fc6-190">MBAM 2.5 supporta le chiavi di ripristino di BitLocker conformi alla Federal Information Processing Standard (FIPS) nei dispositivi che gestiscono il sistema operativo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-190">MBAM2.5 supports Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices that are running the Windows8.1 operating system.</span></span> <span data-ttu-id="a2fc6-191">La chiave di ripristino non è conforme FIPS nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-191">The recovery key was not FIPS compliant in earlier versions of Windows.</span></span> <span data-ttu-id="a2fc6-192">Questo miglioramento migliora il processo di ripristino delle unità in organizzazioni che richiedono la conformità FIPS perché consente agli utenti finali di usare il portale self-service o il sito Web di amministrazione e monitoraggio (Help desk) per recuperare i propri dischi se dimenticano il PIN o la password o si bloccano i propri computer.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-192">This enhancement improves the drive recovery process in organizations that require FIPS compliance because it enables end users to use the Self-Service Portal or Administration and Monitoring Website (Help Desk) to recover their drives if they forget their PIN or password or get locked out of their computers.</span></span> <span data-ttu-id="a2fc6-193">La nuova funzionalità di conformità FIPS non si estende ai protettori delle password.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-193">The new FIPS compliance feature does not extend to password protectors.</span></span>

<span data-ttu-id="a2fc6-194">Per abilitare la conformità FIPS nell'organizzazione, è necessario configurare le impostazioni dei criteri di gruppo FIPS (Federal Information Processing Standard).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-194">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="a2fc6-195">Per istruzioni sulla configurazione, vedere [impostazioni dei criteri di gruppo di BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-195">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

<span data-ttu-id="a2fc6-196">Per i computer client che eseguono i sistemi operativi Windows8 o Windows7 senza l' [hotfix installato di BitLocker](https://support.microsoft.com/kb/3015477), gli amministratori IT continueranno a usare la protezione DRA per gli agenti di recupero dati in ambienti conformi allo standard FIPS.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-196">For client computers that are running the Windows8 or Windows7 operating systems without the [installed BitLocker hotfix](https://support.microsoft.com/kb/3015477), IT administrators will continue to use the Data Recovery Agents (DRA) protector in FIPS-compliant environments.</span></span> <span data-ttu-id="a2fc6-197">Per informazioni su DRA, vedere [uso di agenti di recupero dati con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-197">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

<span data-ttu-id="a2fc6-198">Vedere [pacchetto hotfix 2 per l'amministrazione e il monitoraggio di bitlocker 2,5](https://support.microsoft.com/kb/3015477) per scaricare e installare i computer hotfix per Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-198">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="a2fc6-199">Supporto per distribuzioni ad alta disponibilità</span><span class="sxs-lookup"><span data-stu-id="a2fc6-199">Support for high availability deployments</span></span>

<span data-ttu-id="a2fc6-200">MBAM supporta i seguenti scenari ad alta disponibilità, oltre alle topologie di integrazione standard di due server e gestione configurazione:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-200">MBAM supports the following high-availability scenarios in addition to the standard two-server and Configuration Manager Integration topologies:</span></span>

-   <span data-ttu-id="a2fc6-201">Gruppi di disponibilità di SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a2fc6-201">SQL Server AlwaysOn availability groups</span></span>

-   <span data-ttu-id="a2fc6-202">Clustering di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2fc6-202">SQL Server clustering</span></span>

-   <span data-ttu-id="a2fc6-203">Bilanciamento del carico di rete (NLB)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-203">Network load balancing (NLB)</span></span>

-   <span data-ttu-id="a2fc6-204">Mirroring di SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2fc6-204">SQL Server mirroring</span></span>

-   <span data-ttu-id="a2fc6-205">Backup del servizio Copia Shadow del volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="a2fc6-205">Volume Shadow Copy Service (VSS) Backup</span></span>

<span data-ttu-id="a2fc6-206">Per altre informazioni su queste funzionalità, vedere [pianificazione per MBAM 2,5 disponibilità elevata](planning-for-mbam-25-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-206">For more information about these features, see [Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md).</span></span>

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a><span data-ttu-id="a2fc6-207">La gestione dei ruoli per il sito Web di amministrazione e monitoraggio è cambiata</span><span class="sxs-lookup"><span data-stu-id="a2fc6-207">Management of roles for Administration and Monitoring Website changed</span></span>

<span data-ttu-id="a2fc6-208">In MBAM 2.5 è necessario creare gruppi di sicurezza in Active Directory Domain Services (aggiunge) per gestire i ruoli che prevedono i diritti di accesso al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-208">In MBAM2.5, you must create security groups in Active Directory Domain Services (ADDS) to manage the roles that provide access rights to the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2fc6-209">I ruoli consentono agli utenti che si trovano in gruppi di sicurezza specifici di eseguire attività diverse nel sito Web, ad esempio la visualizzazione di report o l'assistenza agli utenti finali per recuperare unità crittografate.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-209">Roles enable users who are in specific security groups to perform different tasks in the website such as viewing reports or helping end users recover encrypted drives.</span></span> <span data-ttu-id="a2fc6-210">Nelle versioni precedenti di MBAM i ruoli venivano gestiti tramite gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-210">In previous versions of MBAM, roles were managed by using local groups.</span></span>

<span data-ttu-id="a2fc6-211">In MBAM 2.5, il termine "Roles" sostituisce il termine "ruoli di amministratore", usato nelle versioni precedenti di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-211">In MBAM2.5, the term “roles” replaces the term “administrator roles,” which was used in earlier versions of MBAM.</span></span> <span data-ttu-id="a2fc6-212">Inoltre, in MBAM 2.5 il ruolo "MBAM System Administrators" è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-212">In addition, in MBAM2.5 the “MBAM System Administrators” role has been removed.</span></span>

<span data-ttu-id="a2fc6-213">Nella tabella seguente sono elencati i gruppi di sicurezza che è necessario creare in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-213">The following table lists the security groups that you must create in AD DS.</span></span> <span data-ttu-id="a2fc6-214">Puoi usare qualsiasi nome per i gruppi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-214">You can use any name for the security groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2fc6-215">Ruolo</span><span class="sxs-lookup"><span data-stu-id="a2fc6-215">Role</span></span></th>
<th align="left"><span data-ttu-id="a2fc6-216">Diritti di accesso per questo ruolo nel sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="a2fc6-216">Access rights for this role on the Administration and Monitoring Website</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fc6-217">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="a2fc6-217">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-218">Consente di accedere alle aree Gestisci TPM e recupero unità del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-218">Provides access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="a2fc6-219">Gli utenti che hanno accesso a queste aree devono compilare tutti i campi quando usano un'area qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-219">Users who have access to these areas must fill in all fields when they use either area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fc6-220">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="a2fc6-220">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-221">Consente di accedere ai report nel sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-221">Provides access to the Reports in the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fc6-222">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="a2fc6-222">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-223">Consente di accedere a tutte le aree del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-223">Provides access to all areas in the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2fc6-224">Gli utenti di questo gruppo devono immettere solo la chiave di ripristino, non il dominio e il nome utente dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-224">Users in this group have to enter only the recovery key, not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="a2fc6-225">Se un utente è un membro del gruppo di utenti di MBAM helpdesk e il gruppo di utenti dell'helpdesk Advanced di mbam, le autorizzazioni di gruppo degli utenti del helpdesk avanzato di mbam eseguono l'override delle autorizzazioni del gruppo utenti di MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-225">If a user is a member of the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users group permissions.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a2fc6-226">Dopo aver creato i gruppi di sicurezza in Aggiungi, assegnare utenti e/o gruppi al gruppo di sicurezza appropriato per consentire il livello di accesso corrispondente al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-226">After you create the security groups in ADDS, assign users and/or groups to the appropriate security group to enable the corresponding level of access to the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2fc6-227">Per consentire agli utenti con ogni ruolo di accedere al sito Web di amministrazione e monitoraggio, è necessario specificare ogni gruppo di sicurezza anche quando si configura il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-227">To enable individuals with each role to access the Administration and Monitoring Website, you must also specify each security group when you are configuring the Administration and Monitoring Website.</span></span>

### <span data-ttu-id="a2fc6-228">Cmdlet di Windows PowerShell per la configurazione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="a2fc6-228">Windows PowerShell cmdlets for configuring MBAM Server features</span></span>

<span data-ttu-id="a2fc6-229">I cmdlet di Windows PowerShell per MBAM 2.5 consentono di configurare e gestire le caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-229">Windows PowerShell cmdlets for MBAM2.5 enable you to configure and manage the MBAM Server features.</span></span> <span data-ttu-id="a2fc6-230">Ogni funzionalità include un cmdlet di Windows PowerShell corrispondente che puoi usare per abilitare o disabilitare le funzionalità o per ottenere informazioni sulla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-230">Each feature has a corresponding Windows PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="a2fc6-231">Per i prerequisiti e i prerequisiti per l'uso di Windows PowerShell, vedere [configurazione delle funzionalità del server di MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-231">For prerequisites and prerequisites for using Windows PowerShell, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

**<span data-ttu-id="a2fc6-232">Per caricare la Guida di MBAM 2,5 per i cmdlet di Windows PowerShell dopo l'installazione del software del server MBAM</span><span class="sxs-lookup"><span data-stu-id="a2fc6-232">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="a2fc6-233">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-233">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="a2fc6-234">Digitare **Update-Guida-modulo Microsoft. mbam**.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-234">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

<span data-ttu-id="a2fc6-235">La Guida di Windows PowerShell per MBAM è disponibile nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-235">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2fc6-236">Formato della Guida di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2fc6-236">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="a2fc6-237">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="a2fc6-237">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fc6-238">In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a2fc6-238">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a2fc6-239">Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni della sezione precedente su come caricare la Guida di Windows PowerShell per MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-239">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fc6-240">In TechNet come pagine Web</span><span class="sxs-lookup"><span data-stu-id="a2fc6-240">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fc6-241">Nell'area download come file di Word. docx</span><span class="sxs-lookup"><span data-stu-id="a2fc6-241">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fc6-242">Nell'area download come file PDF</span><span class="sxs-lookup"><span data-stu-id="a2fc6-242">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a2fc6-243">Supporto per pin ASCII e avanzati e possibilità di impedire i caratteri sequenziali e ripetuti</span><span class="sxs-lookup"><span data-stu-id="a2fc6-243">Support for ASCII-only and enhanced PINs and ability to prevent sequential and repeating characters</span></span>

**<span data-ttu-id="a2fc6-244">Consenti PIN avanzati per l'impostazione di criteri di gruppo di avvio</span><span class="sxs-lookup"><span data-stu-id="a2fc6-244">Allow enhanced PINs for startup Group Policy setting</span></span>**

<span data-ttu-id="a2fc6-245">L'impostazione di criteri di gruppo consente di configurare i **PIN avanzati per l'avvio**e di stabilire se usare i pin di avvio avanzati con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-245">The Group Policy setting, **Allow enhanced PINs for startup**, enables you to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="a2fc6-246">I pin di avvio avanzati consentono agli utenti di immettere qualsiasi tasto su una tastiera completa, incluse lettere maiuscole e minuscole, simboli, numeri e spazi.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-246">Enhanced startup PINs permit users to enter any keys on a full keyboard, including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="a2fc6-247">Se si abilita questa impostazione per i criteri, tutti i nuovi PIN di avvio di BitLocker impostati saranno PIN avanzati.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-247">If you enable this policy setting, all new BitLocker startup PINs that are set will be enhanced PINs.</span></span> <span data-ttu-id="a2fc6-248">Se si disattiva o non si configura questa impostazione dei criteri, non è possibile usare i PIN avanzati.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-248">If you disable or do not configure this policy setting, enhanced PINs cannot be used.</span></span>

<span data-ttu-id="a2fc6-249">Non tutti i computer supportano l'immissione di PIN avanzati nell'ambiente PXE (pre-boot Execution Environment).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-249">Not all computers support the entry of enhanced PINs in the Pre-Boot Execution Environment (PXE).</span></span> <span data-ttu-id="a2fc6-250">Prima di abilitare questa impostazione di criteri di gruppo per l'organizzazione, eseguire un controllo di sistema durante il processo di configurazione di BitLocker per verificare che il BIOS del computer supporti l'uso della tastiera completa in PXE.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-250">Before you enable this Group Policy setting for your organization, run a system check during the BitLocker setup process to ensure that the computer’s BIOS supports the use of the full keyboard in PXE.</span></span> <span data-ttu-id="a2fc6-251">Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-251">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

**<span data-ttu-id="a2fc6-252">Richiedere la casella di controllo pin solo ASCII</span><span class="sxs-lookup"><span data-stu-id="a2fc6-252">Require ASCII-only PINs check box</span></span>**

<span data-ttu-id="a2fc6-253">L'impostazione **Consenti i PIN avanzati per i criteri di gruppo di avvio** contiene anche una casella di controllo **Richiedi solo i pin ASCII** .</span><span class="sxs-lookup"><span data-stu-id="a2fc6-253">The **Allow enhanced PINs for startup** Group Policy setting also contains a **Require ASCII-only PINs** check box.</span></span> <span data-ttu-id="a2fc6-254">Se i computer dell'organizzazione non supportano l'uso della tastiera completa in PXE, è possibile abilitare l'impostazione Consenti i **PIN avanzati per** i criteri di gruppo di avvio e quindi selezionare la casella di controllo **Richiedi solo i pin ASCII** per richiedere che i PIN avanzati usino solo caratteri ASCII stampabili.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-254">If the computers in your organization do not support the use of the full keyboard in PXE, you can enable the **Allow enhanced PINs for startup** Group Policy setting, and then select the **Require ASCII-only PINs** check box to require that enhanced PINs use only printable ASCII characters.</span></span>

**<span data-ttu-id="a2fc6-255">Applicazione forzata di caratteri non sequenziali e non ripetitivi</span><span class="sxs-lookup"><span data-stu-id="a2fc6-255">Enforced use of nonsequential and nonrepeating characters</span></span>**

<span data-ttu-id="a2fc6-256">MBAM 2.5 impedisce agli utenti finali di creare pin costituiti da numeri ripetitivi (ad esempio 1111) o numeri sequenziali (ad esempio 1234).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-256">MBAM2.5 prevents end users from creating PINs that consist of repeating numbers (such as 1111) or sequential numbers (such as 1234).</span></span> <span data-ttu-id="a2fc6-257">Se gli utenti finali provano a immettere una password che contiene tre o più numeri ripetuti o sequenziali, la crittografia guidata unità BitLocker Visualizza un messaggio di errore e impedisce agli utenti di immettere un PIN con i caratteri vietati.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-257">If end users try to enter a password that contains three or more repeating or sequential numbers, the Bitlocker Drive Encryption wizard displays an error message and prevents users from entering a PIN with the prohibited characters.</span></span>

### <span data-ttu-id="a2fc6-258">Aggiunta del certificato DRA al report di conformità del computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="a2fc6-258">Addition of DRA Certificate to BitLocker Computer Compliance report</span></span>

<span data-ttu-id="a2fc6-259">Un nuovo tipo di protezione, il certificato DRA (Data Recovery Agent), è stato aggiunto al report conformità computer di BitLocker in Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-259">A new protector type, the Data Recovery Agent (DRA) Certificate, has been added to the BitLocker Computer Compliance Report in Configuration Manager.</span></span> <span data-ttu-id="a2fc6-260">Questo tipo di protezione si applica alle unità del sistema operativo e viene visualizzato nella sezione **volumi computer** nella colonna **tipi di protezione** .</span><span class="sxs-lookup"><span data-stu-id="a2fc6-260">This protector type applies to operating system drives, and it appears in the **Computer Volume(s)** section in the **Protector Types** column.</span></span>

### <span data-ttu-id="a2fc6-261">Supporto per distribuzioni di supporto per più insiemi di strutture</span><span class="sxs-lookup"><span data-stu-id="a2fc6-261">Support for multi-forest support deployments</span></span>

<span data-ttu-id="a2fc6-262">MBAM 2,5 supporta i seguenti tipi di distribuzioni con più foreste:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-262">MBAM 2.5 supports the following types of multi-forest deployments:</span></span>

-   <span data-ttu-id="a2fc6-263">Singola foresta con un singolo dominio</span><span class="sxs-lookup"><span data-stu-id="a2fc6-263">Single forest with single domain</span></span>

-   <span data-ttu-id="a2fc6-264">Singola foresta con un solo albero e più domini</span><span class="sxs-lookup"><span data-stu-id="a2fc6-264">Single forest with a single tree and multiple domains</span></span>

-   <span data-ttu-id="a2fc6-265">Foresta singola con più alberi e spazi dei nomi disgiunti</span><span class="sxs-lookup"><span data-stu-id="a2fc6-265">Single forest with multiple trees and disjoint namespaces</span></span>

-   <span data-ttu-id="a2fc6-266">Più foreste in una topologia di foresta centrale</span><span class="sxs-lookup"><span data-stu-id="a2fc6-266">Multiple forests in a central forest topology</span></span>

-   <span data-ttu-id="a2fc6-267">Più foreste in una topologia di foresta di risorse</span><span class="sxs-lookup"><span data-stu-id="a2fc6-267">Multiple forests in a resource forest topology</span></span>

<span data-ttu-id="a2fc6-268">Non è disponibile alcun supporto per la migrazione delle foreste (passando da singola a multipla, multipla a singola, risorsa in tutta la foresta e così via) o aggiornamento o downgrade.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-268">There is no support for forest migration (going from single to multiple, multiple to single, resource to across the forest, etc.), or upgrade or downgrade.</span></span>

<span data-ttu-id="a2fc6-269">I prerequisiti per la distribuzione di MBAM nelle distribuzioni con più foreste sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2fc6-269">The prerequisites for deploying MBAM in multi-forest deployments are:</span></span>

-   <span data-ttu-id="a2fc6-270">La foresta deve essere in uso nelle versioni supportate di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-270">Forest must be running on supported versions of Windows Server.</span></span>

-   <span data-ttu-id="a2fc6-271">È necessario un trust bidirezionale o unidirezionale.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-271">A two-way or one-way trust is required.</span></span> <span data-ttu-id="a2fc6-272">I trust unidirezionali richiedono che il dominio del server si fidi del dominio del client.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-272">One-way trusts require that the server’s domain trusts the client’s domain.</span></span> <span data-ttu-id="a2fc6-273">In altre parole, il dominio del server è puntato sul dominio del client.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-273">In other words, the server’s domain is pointed at the client’s domain.</span></span>

### <span data-ttu-id="a2fc6-274">Supporto di MBAM client per dischi rigidi crittografati</span><span class="sxs-lookup"><span data-stu-id="a2fc6-274">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="a2fc6-275">MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-275">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="a2fc6-276">Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-276">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="a2fc6-277">Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a2fc6-277">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

## <span data-ttu-id="a2fc6-278">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="a2fc6-278">How to Get MDOP Technologies</span></span>


<span data-ttu-id="a2fc6-279">MBAM fa parte del Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-279">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="a2fc6-280">MDOP fa parte del programma Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="a2fc6-280">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="a2fc6-281">Per altre informazioni sul programma Microsoft Software Assurance e su come acquisire il MDOP, vedere [come si ottiene MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-281">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="---------mbam-2-5-release-notes"></a> <span data-ttu-id="a2fc6-282">Note sulla versione di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="a2fc6-282">MBAM 2.5 Release Notes</span></span>


<span data-ttu-id="a2fc6-283">Per altre informazioni e notizie aggiornate che non sono incluse in questa documentazione, vedere note sulla [versione per MBAM 2,5](release-notes-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-283">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5](release-notes-for-mbam-25.md).</span></span>

## <span data-ttu-id="a2fc6-284">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="a2fc6-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a2fc6-285">Inviare il proprio feedback [qui](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-285">Send your feedback [here](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span></span> 
- <span data-ttu-id="a2fc6-286">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a2fc6-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="a2fc6-287">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2fc6-287">Related topics</span></span>


[<span data-ttu-id="a2fc6-288">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="a2fc6-288">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="a2fc6-289">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a2fc6-289">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





