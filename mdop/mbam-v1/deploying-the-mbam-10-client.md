---
title: Distribuzione del client MBAM 1.0
description: Distribuzione del client MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822905"
---
# <span data-ttu-id="eff94-103">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="eff94-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="eff94-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="eff94-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="eff94-105">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite strumenti come servizi di dominio Active Directory oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="eff94-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="eff94-106">A seconda di quando si distribuisce il client MBAM, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima o dopo che l'utente finale riceva il computer.</span><span class="sxs-lookup"><span data-stu-id="eff94-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="eff94-107">Per controllare questa tempistica, puoi configurare criteri di gruppo e distribuire il software del client MBAM usando un sistema di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="eff94-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="eff94-108">Puoi usare uno o entrambi questi metodi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="eff94-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="eff94-109">Se si usano entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.</span><span class="sxs-lookup"><span data-stu-id="eff94-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="eff94-110">Distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="eff94-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="eff94-111">Dopo aver configurato Criteri di gruppo, è possibile distribuire i file di installazione di Windows Installer del client MBAM in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eff94-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="eff94-112">A questo scopo, puoi usare un prodotto del sistema di distribuzione del software aziendale, ad esempio Microsoft System Center 2012 Configuration Manager o Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="eff94-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="eff94-113">I due file di installazione di Windows Installer disponibili per MBAM client sono MBAMClient-64bit.msi e MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="eff94-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="eff94-114">Questi file sono forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="eff94-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="eff94-115">Per altre informazioni su come distribuire gli oggetti dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eff94-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="eff94-116">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="eff94-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="eff94-117">Distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="eff94-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="eff94-118">In alcune organizzazioni i nuovi computer vengono ricevuti e configurati centralmente.</span><span class="sxs-lookup"><span data-stu-id="eff94-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="eff94-119">Questa situazione consente agli amministratori di installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che tutti i dati degli utenti vengano scritti nel computer.</span><span class="sxs-lookup"><span data-stu-id="eff94-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="eff94-120">Questo approccio consente di verificare che i computer siano crittografati correttamente perché l'amministratore esegue l'azione senza affidarsi alle azioni dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="eff94-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="eff94-121">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="eff94-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="eff94-122">Come distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="eff94-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="eff94-123">Altre risorse per la distribuzione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="eff94-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="eff94-124">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="eff94-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="eff94-125">Pianificazione della distribuzione del client di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="eff94-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





