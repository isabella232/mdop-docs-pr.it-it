---
title: Distribuzione del client MBAM 2.0
description: Distribuzione del client MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823446"
---
# <span data-ttu-id="77476-103">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="77476-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="77476-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="77476-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="77476-105">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory, oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="77476-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="77476-106">A seconda di quando si distribuisce il client di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito configurando criteri di gruppo e distribuendo il software del client MBAM usando un sistema di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="77476-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="77476-107">Distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="77476-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="77476-108">Dopo la configurazione dei criteri di gruppo, è possibile usare un prodotto del sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager 2012 o Active Directory Domain Services per distribuire i file di installazione di Windows Installer di MBAM client in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77476-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="77476-109">È possibile distribuire il client usando i file MbamClientSetup.exe a 32 bit o 64 bit oppure i file di MBAMClient.msi a 32 bit o 64 bit, forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="77476-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="77476-110">Per altre informazioni sulla distribuzione di oggetti Criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="77476-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="77476-111">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="77476-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="77476-112">Distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="77476-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="77476-113">Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti.</span><span class="sxs-lookup"><span data-stu-id="77476-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="77476-114">Il vantaggio di questo processo è che ogni computer è quindi conforme alla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="77476-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="77476-115">Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer.</span><span class="sxs-lookup"><span data-stu-id="77476-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="77476-116">Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.</span><span class="sxs-lookup"><span data-stu-id="77476-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="77476-117">Se i criteri di gruppo sono stati configurati per richiedere un PIN, viene chiesto agli utenti di impostare un PIN dopo la ricezione dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="77476-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="77476-118">Come distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="77476-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="77476-119">Come usare una riga di comando per installare il client MBAM</span><span class="sxs-lookup"><span data-stu-id="77476-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="77476-120">Questa sezione spiega come installare il client MBAM usando una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="77476-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="77476-121">Come usare una riga di comando per installare il client MBAM</span><span class="sxs-lookup"><span data-stu-id="77476-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="77476-122">Altre risorse per la distribuzione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="77476-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="77476-123">Distribuzione di [mbam 2,0](deploying-mbam-20-mbam-2.md)[Planning per MBAM 2,0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="77476-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





