---
title: Pianificazione della distribuzione del client di MBAM 1.0
description: Pianificazione della distribuzione del client di MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825876"
---
# <span data-ttu-id="23dc9-103">Pianificazione della distribuzione del client di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="23dc9-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="23dc9-104">A seconda di quando si distribuisce il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito.</span><span class="sxs-lookup"><span data-stu-id="23dc9-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="23dc9-105">Per abilitare la crittografia BitLocker dopo che l'utente finale ha ricevuto il computer, configurare criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="23dc9-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="23dc9-106">Per abilitare la crittografia BitLocker prima che l'utente finale riceva il computer, distribuire il software del client MBAM usando un sistema di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="23dc9-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="23dc9-107">Puoi usare uno o entrambi i metodi dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="23dc9-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="23dc9-108">Se si usano entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.</span><span class="sxs-lookup"><span data-stu-id="23dc9-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="23dc9-109">**Nota**  Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="23dc9-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="23dc9-110">Distribuzione del client MBAM per abilitare la crittografia BitLocker dopo la distribuzione del computer agli utenti finali</span><span class="sxs-lookup"><span data-stu-id="23dc9-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="23dc9-111">Dopo aver configurato i criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager 2012 o Active Directory Domain Services, per distribuire i file di installazione di Windows Installer di MBAM client nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="23dc9-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="23dc9-112">I due file di installazione di Windows Installer di MBAM client sono MBAMClient-64bit.msi e MBAMClient-32bit.msi, forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="23dc9-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="23dc9-113">Per altre informazioni su come distribuire gli oggetti dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="23dc9-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="23dc9-114">Quando si distribuisce il client MBAM, dopo aver distribuito i computer agli utenti finali, viene chiesto agli utenti finali di crittografare i propri computer.</span><span class="sxs-lookup"><span data-stu-id="23dc9-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="23dc9-115">In questo modo MBAM raccoglie i dati, includendo il PIN e la password e quindi inizia il processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="23dc9-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="23dc9-116">**Nota**  In questo approccio agli utenti viene richiesto di attivare e inizializzare il chip Trusted Platform Module (TPM), se non è stato attivato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="23dc9-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="23dc9-117">Uso del client MBAM per abilitare la crittografia BitLocker prima della distribuzione del computer per gli utenti finali</span><span class="sxs-lookup"><span data-stu-id="23dc9-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="23dc9-118">Nelle organizzazioni in cui i computer vengono ricevuti e configurati in modo centralizzato, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti.</span><span class="sxs-lookup"><span data-stu-id="23dc9-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="23dc9-119">Il vantaggio di questo processo è che ogni computer sarà conforme alla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="23dc9-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="23dc9-120">Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer.</span><span class="sxs-lookup"><span data-stu-id="23dc9-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="23dc9-121">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="23dc9-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="23dc9-122">Se l'organizzazione vuole usare (TPM) per crittografare i computer, l'amministratore deve crittografare il volume del sistema operativo del computer con TPM Protector.</span><span class="sxs-lookup"><span data-stu-id="23dc9-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="23dc9-123">Se l'organizzazione vuole usare il chip TPM e una protezione PIN, l'amministratore deve crittografare il volume di sistema con la protezione TPM, quindi gli utenti selezionano un PIN la prima volta che accedono.</span><span class="sxs-lookup"><span data-stu-id="23dc9-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="23dc9-124">Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume.</span><span class="sxs-lookup"><span data-stu-id="23dc9-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="23dc9-125">Quando gli utenti accedono ai propri computer, MBAM chiede di specificare un PIN o un PIN e una password che utilizzeranno quando riavviano il computer in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="23dc9-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="23dc9-126">**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima di consegnare il computer all'utente.</span><span class="sxs-lookup"><span data-stu-id="23dc9-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="23dc9-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23dc9-127">Related topics</span></span>


[<span data-ttu-id="23dc9-128">Pianificazione della distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="23dc9-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="23dc9-129">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="23dc9-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





