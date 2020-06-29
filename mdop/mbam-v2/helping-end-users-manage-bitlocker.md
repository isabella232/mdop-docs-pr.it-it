---
title: Aiutare gli utenti finali a gestire BitLocker
description: Aiutare gli utenti finali a gestire BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824776"
---
# <span data-ttu-id="ba608-103">Aiutare gli utenti finali a gestire BitLocker</span><span class="sxs-lookup"><span data-stu-id="ba608-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="ba608-104">Il contenuto di un computer smarrito o rubato è vulnerabile all'accesso non autorizzato, che può presentare un rischio per la sicurezza sia per le persone che per le aziende.</span><span class="sxs-lookup"><span data-stu-id="ba608-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="ba608-105">Microsoft BitLocker Administration and Monitoring (MBAM) USA BitLocker per impedire l'accesso non autorizzato bloccando il computer per facilitare la protezione dei dati riservati dagli utenti malintenzionati.</span><span class="sxs-lookup"><span data-stu-id="ba608-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="ba608-106">Che cos'è BitLocker?</span><span class="sxs-lookup"><span data-stu-id="ba608-106">What is BitLocker?</span></span>


<span data-ttu-id="ba608-107">La crittografia unità BitLocker può consentire la protezione delle unità di sistema operativo, delle unità dati e delle unità rimovibili, ad esempio un'unità thumb USB, crittografando le unità.</span><span class="sxs-lookup"><span data-stu-id="ba608-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="ba608-108">A seconda del modo in cui BitLocker è configurato, gli utenti potrebbero dover specificare una chiave (una password o un PIN) per sbloccare le informazioni archiviate nelle unità crittografate.</span><span class="sxs-lookup"><span data-stu-id="ba608-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="ba608-109">Quando si aggiungono nuovi file a un'unità crittografata con BitLocker, BitLocker li crittografa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ba608-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="ba608-110">I file restano crittografati solo quando vengono archiviati nell'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="ba608-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="ba608-111">I file copiati in un'altra unità o computer vengono decrittografati.</span><span class="sxs-lookup"><span data-stu-id="ba608-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="ba608-112">Se si condividono file con altri utenti, ad esempio tramite una rete, questi file vengono crittografati durante l'archiviazione nell'unità crittografata, ma è possibile accedervi in genere dagli utenti autorizzati.</span><span class="sxs-lookup"><span data-stu-id="ba608-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="ba608-113">Se si crittografa l'unità del sistema operativo, BitLocker controlla il computer durante l'avvio per tutte le condizioni che potrebbero rappresentare un rischio per la sicurezza, ad esempio una modifica del BIOS o le modifiche apportate ai file di avvio.</span><span class="sxs-lookup"><span data-stu-id="ba608-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="ba608-114">Se viene rilevato un potenziale rischio di sicurezza, BitLocker bloccherà l'unità del sistema operativo e richiederà una chiave di ripristino di BitLocker speciale per sbloccarla.</span><span class="sxs-lookup"><span data-stu-id="ba608-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="ba608-115">Verificare di aver creato questo tasto di ripristino quando si attiva BitLocker per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="ba608-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="ba608-116">In caso contrario, è possibile perdere definitivamente l'accesso ai file.</span><span class="sxs-lookup"><span data-stu-id="ba608-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="ba608-117">Se si crittografano le unità dati (fisse o rimovibili), è possibile sbloccare un'unità crittografata con una password o una smart card oppure impostare l'unità per l'apertura automatica quando si accede al computer.</span><span class="sxs-lookup"><span data-stu-id="ba608-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="ba608-118">Oltre alle password e ai pin, BitLocker può usare il chip TPM (Trusted Platform Module) fornito in molti computer più recenti.</span><span class="sxs-lookup"><span data-stu-id="ba608-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="ba608-119">Il chip TPM viene usato per verificare che il computer non sia stato manomesso prima che BitLocker sblocchi l'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba608-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="ba608-120">Durante il processo di crittografia potrebbe essere necessario abilitare il chip TPM.</span><span class="sxs-lookup"><span data-stu-id="ba608-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="ba608-121">Quando si avvia il computer, BitLocker chiede al TPM le chiavi per l'unità e lo sblocca.</span><span class="sxs-lookup"><span data-stu-id="ba608-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="ba608-122">Per abilitare il chip TPM, sarà necessario riavviare il computer e quindi modificare un'impostazione nel BIOS, un livello precedente a Windows del software del computer.</span><span class="sxs-lookup"><span data-stu-id="ba608-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="ba608-123">Per altre informazioni sul TPM, vedere [informazioni sul chip TPM per il computer](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="ba608-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="ba608-124">Quando il computer è protetto da BitLocker, potrebbe essere necessario immettere un PIN o una password ogni volta che il computer viene riattivato dalla sospensione o dall'avvio.</span><span class="sxs-lookup"><span data-stu-id="ba608-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="ba608-125">Il supporto tecnico per la società o l'organizzazione può essere utile se si dimentica il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="ba608-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="ba608-126">Per disattivare BitLocker temporaneamente, è possibile sospenderlo o definitivamente decrittografando l'unità.</span><span class="sxs-lookup"><span data-stu-id="ba608-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="ba608-127">**Nota**  Poiché BitLocker crittografa l'intera unità e non solo i singoli file, prestare particolare attenzione quando si muovono dati riservati tra le unità.</span><span class="sxs-lookup"><span data-stu-id="ba608-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="ba608-128">Se si trasferisce un file da un'unità protetta da BitLocker a un'unità non crittografata, il file non sarà più crittografato.</span><span class="sxs-lookup"><span data-stu-id="ba608-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="ba608-129">Informazioni sull'applicazione di opzioni di crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="ba608-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="ba608-130">Per sbloccare le unità disco rigido nel computer e gestire il PIN e le password, usare l'applicazione opzioni di crittografia BitLocker nel pannello di controllo di Windows seguendo la procedura descritta in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="ba608-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="ba608-131">È possibile immettere le password per sbloccare le unità protette e verificare lo stato di BitLocker delle unità collegate tramite questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba608-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="ba608-132">Per aprire l'applicazione opzioni di crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="ba608-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="ba608-133">Fare clic sul pulsante **Start**e selezionare **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="ba608-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="ba608-134">Il pannello di controllo viene aperto in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="ba608-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="ba608-135">Nel **Pannello di controllo**selezionare **sistema e sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="ba608-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="ba608-136">Selezionare le **Opzioni di crittografia BitLocker** per aprire l'applicazione opzioni di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ba608-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="ba608-137">Per una descrizione delle opzioni disponibili, vedere la sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="ba608-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="ba608-138">Opzioni nell'applicazione opzioni di crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="ba608-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="ba608-139">L'applicazione opzioni di crittografia BitLocker nel pannello di controllo consente di gestire il PIN e le password, che BitLocker usa per proteggere il computer.</span><span class="sxs-lookup"><span data-stu-id="ba608-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="ba608-140">Crittografia unità BitLocker-unità disco fisse:</span><span class="sxs-lookup"><span data-stu-id="ba608-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="ba608-141">In questa sezione è possibile visualizzare informazioni sulle unità disco rigido connesse al computer e sullo stato di crittografia di BitLocker corrente.</span><span class="sxs-lookup"><span data-stu-id="ba608-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="ba608-142">**Gestire il pin** : consente di modificare il PIN usato da BitLocker per sbloccare l'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba608-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="ba608-143">**Gestire la password** : consente di modificare la password usata da BitLocker per sbloccare le altre unità interne.</span><span class="sxs-lookup"><span data-stu-id="ba608-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="ba608-144">Crittografia unità BitLocker-unità esterne:</span><span class="sxs-lookup"><span data-stu-id="ba608-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="ba608-145">In questa sezione è possibile visualizzare informazioni sulle unità esterne, ad esempio un'unità thumb USB, connessa al computer e lo stato di crittografia corrente di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ba608-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="ba608-146">**Gestire la password** : consente di modificare la password usata da BitLocker per sbloccare le altre unità interne.</span><span class="sxs-lookup"><span data-stu-id="ba608-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="ba608-147">Avanzate</span><span class="sxs-lookup"><span data-stu-id="ba608-147">Advanced:</span></span>**

-   <span data-ttu-id="ba608-148">**Amministrazione TPM** : apre lo strumento di Amministrazione TPM in una finestra separata.</span><span class="sxs-lookup"><span data-stu-id="ba608-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="ba608-149">Da qui è possibile configurare le attività di TPM comuni e ottenere informazioni sul chipset TPM.</span><span class="sxs-lookup"><span data-stu-id="ba608-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="ba608-150">Per accedere a questo strumento, è necessario disporre delle autorizzazioni amministrative per il computer.</span><span class="sxs-lookup"><span data-stu-id="ba608-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="ba608-151">**Gestione disco** -aprire lo strumento Gestione disco.</span><span class="sxs-lookup"><span data-stu-id="ba608-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="ba608-152">Da qui è possibile visualizzare le informazioni per tutti i dischi rigidi collegati al computer e configurare le partizioni e le opzioni di unità.</span><span class="sxs-lookup"><span data-stu-id="ba608-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="ba608-153">Per accedere a questo strumento, è necessario disporre di diritti amministrativi nel computer.</span><span class="sxs-lookup"><span data-stu-id="ba608-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





