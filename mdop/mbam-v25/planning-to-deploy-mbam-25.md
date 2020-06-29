---
title: Pianificazione della distribuzione di MBAM 2.5
description: Pianificazione della distribuzione di MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826695"
---
# <span data-ttu-id="e5cec-103">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5cec-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="e5cec-104">Prima di creare il piano di distribuzione per Microsoft BitLocker Administration and Monitoring (MBAM), è consigliabile prendere in considerazione diverse configurazioni e prerequisiti di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e5cec-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="e5cec-105">Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="e5cec-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="e5cec-106">Esaminare le configurazioni supportate di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="e5cec-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="e5cec-107">Dopo aver preparato l'ambiente di elaborazione per il server MBAM e la distribuzione di funzionalità client, assicurati di rivedere le configurazioni supportate per verificare che i computer in cui si sta installando MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5cec-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="e5cec-108">Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 2,5](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="e5cec-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="e5cec-109">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5cec-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="e5cec-110">Pianificare la distribuzione di MBAM 2,5 Server e client</span><span class="sxs-lookup"><span data-stu-id="e5cec-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="e5cec-111">L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere configurate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e5cec-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="e5cec-112">Queste funzionalità possono essere configurate in una configurazione distribuita in più server.</span><span class="sxs-lookup"><span data-stu-id="e5cec-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="e5cec-113">**Nota**  Un'installazione di MBAM su un singolo server è consigliata solo per gli ambienti Lab.</span><span class="sxs-lookup"><span data-stu-id="e5cec-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="e5cec-114">Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e5cec-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="e5cec-115">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione del software aziendale o installando il client nei computer client come parte del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="e5cec-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="e5cec-116">Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e5cec-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="e5cec-117">Pianificazione della distribuzione del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5cec-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="e5cec-118">Pianificazione della distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5cec-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="e5cec-119">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="e5cec-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="e5cec-120">Pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5cec-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="e5cec-121">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="e5cec-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e5cec-122">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e5cec-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e5cec-123">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e5cec-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





