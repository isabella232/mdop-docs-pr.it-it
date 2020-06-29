---
title: Pianificazione della distribuzione del client di MBAM 2.0
description: Pianificazione della distribuzione del client di MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804365"
---
# <span data-ttu-id="e22b0-103">Pianificazione della distribuzione del client di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e22b0-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="e22b0-104">A seconda di quando si distribuisce il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito.</span><span class="sxs-lookup"><span data-stu-id="e22b0-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="e22b0-105">Sia per il MBAM autonomo che per le topologie di Configuration Manager, è necessario configurare le impostazioni dei criteri di gruppo per MBAM.</span><span class="sxs-lookup"><span data-stu-id="e22b0-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="e22b0-106">Se si usa la topologia autonoma di MBAM, è consigliabile usare un sistema di distribuzione del software aziendale per distribuire il software client MBAM ai computer degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="e22b0-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="e22b0-107">Se si distribuisce MBAM con la topologia di Configuration Manager, è possibile usare Configuration Manager per distribuire il software client MBAM ai computer degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="e22b0-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="e22b0-108">In Configuration Manager, l'installazione di MBAM crea una raccolta di computer che MBAM può gestire.</span><span class="sxs-lookup"><span data-stu-id="e22b0-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="e22b0-109">Questa raccolta include workstation e dispositivi che non dispongono di un TPM (Trusted Platform Module), ma che eseguono Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e22b0-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="e22b0-110">**Nota**  Windows to go non è supportato per le installazioni di gestione configurazione integrata di MBAM se si usa Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="e22b0-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="e22b0-111">Distribuzione del client MBAM per abilitare la crittografia BitLocker dopo la distribuzione del computer agli utenti finali</span><span class="sxs-lookup"><span data-stu-id="e22b0-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="e22b0-112">Dopo aver configurato Criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager o Active Directory Domain Services (AD DS) per distribuire i file di Windows Installer dell'installazione del client MBAM in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e22b0-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="e22b0-113">Per distribuire il client MBAM, è possibile usare i file di MbamClientSetup.exe o di MBAMClient.msi bit a 32 o 64, forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="e22b0-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="e22b0-114">Quando si distribuisce il client MBAM dopo la distribuzione di computer ai computer client, agli utenti finali viene richiesto di crittografare il computer.</span><span class="sxs-lookup"><span data-stu-id="e22b0-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="e22b0-115">Questo consente a MBAM di raccogliere i dati, che includono il PIN e la password e quindi di iniziare il processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e22b0-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="e22b0-116">**Nota**  In questo approccio gli utenti che dispongono di computer con un chip TPM viene richiesto di attivare e inizializzare il chip TPM se il chip non è stato attivato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e22b0-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="e22b0-117">Uso del client MBAM per abilitare la crittografia BitLocker prima della distribuzione del computer per gli utenti finali</span><span class="sxs-lookup"><span data-stu-id="e22b0-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="e22b0-118">Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente e in cui i computer hanno un chip TPM conforme, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e22b0-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="e22b0-119">Il vantaggio di questo processo consiste nel fare in modo che tutti i computer siano conformi alla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e22b0-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="e22b0-120">Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer.</span><span class="sxs-lookup"><span data-stu-id="e22b0-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="e22b0-121">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="e22b0-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="e22b0-122">Se l'organizzazione vuole usare il chip TPM per crittografare i computer, l'amministratore aggiunge la protezione TPM per crittografare il volume del sistema operativo del computer.</span><span class="sxs-lookup"><span data-stu-id="e22b0-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="e22b0-123">Se l'organizzazione vuole usare il chip TPM e una protezione PIN, l'amministratore crittografa il volume del sistema operativo con la protezione TPM e quindi gli utenti selezionano un PIN durante l'accesso per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="e22b0-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="e22b0-124">Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume.</span><span class="sxs-lookup"><span data-stu-id="e22b0-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="e22b0-125">Quando gli utenti accedono all'accesso, l'amministrazione e il monitoraggio di Microsoft BitLocker richiedono loro di specificare un PIN oppure un PIN e una password da usare nei riavvii di un computer successivo.</span><span class="sxs-lookup"><span data-stu-id="e22b0-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="e22b0-126">**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="e22b0-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="e22b0-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e22b0-127">Related topics</span></span>


[<span data-ttu-id="e22b0-128">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e22b0-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="e22b0-129">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e22b0-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





