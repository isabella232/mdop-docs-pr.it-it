---
title: Distribuzione del client di MBAM 2.5
description: Distribuzione del client di MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826276"
---
# <span data-ttu-id="112c0-103">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="112c0-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="112c0-104">Il software client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="112c0-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="112c0-105">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory, oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="112c0-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="112c0-106">A seconda di quando si distribuisce il software client di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito configurando criteri di gruppo e distribuendo il software del client MBAM usando un sistema di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="112c0-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="112c0-107">Distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="112c0-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="112c0-108">Dopo aver configurato le impostazioni dei criteri di gruppo, è possibile usare un prodotto del sistema di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager o Active Directory Domain Services per distribuire i file di installazione di Windows Installer di MBAM client in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="112c0-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="112c0-109">È possibile usare i file di MbamClientSetup.exe a 32 bit o 64 bit o i file di MBAMClient.msi a 32 bit o 64 bit, forniti con il software client MBAM.</span><span class="sxs-lookup"><span data-stu-id="112c0-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="112c0-110">Per altre informazioni sulla distribuzione delle impostazioni dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 2,5](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="112c0-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="112c0-111">**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM.</span><span class="sxs-lookup"><span data-stu-id="112c0-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="112c0-112">È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.</span><span class="sxs-lookup"><span data-stu-id="112c0-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="112c0-113">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="112c0-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="112c0-114">Distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="112c0-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="112c0-115">Nelle organizzazioni in cui i computer vengono ricevuti e configurati in modo centralizzato, è possibile installare il client MBAM per gestire la crittografia unità BitLocker in ogni computer prima che vengano scritti i dati degli utenti.</span><span class="sxs-lookup"><span data-stu-id="112c0-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="112c0-116">Il vantaggio di questo processo è che tutti i computer sono conformi alla crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="112c0-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="112c0-117">Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer.</span><span class="sxs-lookup"><span data-stu-id="112c0-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="112c0-118">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="112c0-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="112c0-119">Se le impostazioni dei criteri di gruppo sono state configurate per richiedere un PIN, viene chiesto agli utenti di impostare un PIN dopo la ricezione del criterio.</span><span class="sxs-lookup"><span data-stu-id="112c0-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="112c0-120">Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="112c0-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="112c0-121">Come distribuire il client MBAM usando una riga di comando</span><span class="sxs-lookup"><span data-stu-id="112c0-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="112c0-122">Questa sezione spiega come installare il client MBAM usando una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="112c0-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="112c0-123">Come distribuire il client di MBAM usando una riga di comando</span><span class="sxs-lookup"><span data-stu-id="112c0-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="112c0-124">Altre risorse per la distribuzione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="112c0-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="112c0-125">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="112c0-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="112c0-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="112c0-126">Related topics</span></span>


[<span data-ttu-id="112c0-127">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="112c0-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="112c0-128">Pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="112c0-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="112c0-129">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="112c0-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="112c0-130">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="112c0-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="112c0-131">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="112c0-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





