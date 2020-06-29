---
title: Pianificazione della distribuzione del client di MBAM 2.5
description: Pianificazione della distribuzione del client di MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825995"
---
# <span data-ttu-id="0e7bd-103">Pianificazione della distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0e7bd-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="0e7bd-104">A seconda di quando si distribuisce il software client di amministrazione e monitoraggio di Microsoft BitLocker (MBAM), è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="0e7bd-105">Sia per MBAM stand-alone che per le topologie di integrazione di System Center Configuration Manager, è necessario configurare le impostazioni dei criteri di gruppo per MBAM.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="0e7bd-106">Se si usa la topologia di MBAM autonoma, è consigliabile usare un sistema di distribuzione del software aziendale per distribuire il software client MBAM ai computer degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="0e7bd-107">Se si distribuisce MBAM con la topologia di integrazione di Configuration Manager, è possibile usare Gestione configurazione per distribuire il software del client MBAM ai computer degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="0e7bd-108">In Configuration Manager, l'installazione di MBAM crea una raccolta di computer che MBAM può gestire.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="0e7bd-109">Questa raccolta include workstation e dispositivi che non dispongono di un TPM (Trusted Platform Module), ma che eseguono Windows 8, Windows 8,1 o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="0e7bd-110">**Nota**  Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="0e7bd-111">Distribuzione del client MBAM per abilitare la crittografia unità BitLocker dopo la distribuzione del computer agli utenti finali</span><span class="sxs-lookup"><span data-stu-id="0e7bd-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="0e7bd-112">Dopo aver configurato Criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager o Active Directory Domain Services (AD DS) per distribuire i file di Windows Installer dell'installazione del client MBAM in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="0e7bd-113">Per distribuire il client MBAM, è possibile usare i file di MbamClientSetup.exe o di MBAMClient.msi bit a 32 o 64, forniti con il software client MBAM.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="0e7bd-114">**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="0e7bd-115">È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="0e7bd-116">Quando si distribuisce il client MBAM dopo la distribuzione di computer ai computer client, agli utenti finali viene richiesto di crittografare il computer.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="0e7bd-117">Questa azione consente a MBAM di raccogliere i dati, che includono il PIN e la password (se necessario per i criteri) e quindi per iniziare il processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="0e7bd-118">**Nota**  In questo approccio gli utenti finali che hanno computer con un chip TPM viene richiesto di attivare e inizializzare il chip TPM se il chip non è stato attivato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="0e7bd-119">Uso del client MBAM per abilitare la crittografia unità BitLocker prima della distribuzione del computer per gli utenti finali</span><span class="sxs-lookup"><span data-stu-id="0e7bd-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="0e7bd-120">Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente e in cui i computer hanno un chip TPM conforme, è possibile usare il client MBAM per gestire la crittografia unità BitLocker in ogni computer prima che vengano scritti i dati degli utenti.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="0e7bd-121">Il vantaggio di questo processo è che ogni computer è quindi conforme.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="0e7bd-122">Questo metodo non si basa sull'azione dell'utente finale perché l'amministratore ha già crittografato il computer.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="0e7bd-123">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="0e7bd-124">Se l'organizzazione vuole usare il chip TPM per crittografare i computer, l'amministratore aggiunge la protezione TPM per crittografare il volume del sistema operativo del computer.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="0e7bd-125">Se l'organizzazione vuole usare il chip TPM e un dispositivo di protezione PIN, l'amministratore crittografa il volume del sistema operativo con la protezione TPM e quindi gli utenti finali selezionano un PIN quando accedono per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="0e7bd-126">Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="0e7bd-127">Quando gli utenti finali accedono, l'amministrazione e il monitoraggio di Microsoft BitLocker richiede loro di specificare un PIN oppure un PIN e una password da usare nei riavvii di un computer successivo.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="0e7bd-128">**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima che il computer venga recapitato all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="0e7bd-129">Supporto di MBAM client per dischi rigidi crittografati</span><span class="sxs-lookup"><span data-stu-id="0e7bd-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="0e7bd-130">MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="0e7bd-131">Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="0e7bd-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="0e7bd-132">Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e7bd-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="0e7bd-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e7bd-133">Related topics</span></span>


[<span data-ttu-id="0e7bd-134">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0e7bd-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="0e7bd-135">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0e7bd-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="0e7bd-136">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="0e7bd-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0e7bd-137">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0e7bd-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0e7bd-138">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0e7bd-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




