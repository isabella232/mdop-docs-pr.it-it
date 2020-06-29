---
title: Pianificazione della distribuzione di MBAM 2.0
description: Pianificazione della distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825635"
---
# <span data-ttu-id="98947-103">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="98947-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="98947-104">Prima di creare il piano di distribuzione per Microsoft BitLocker Administration and Monitoring (MBAM), è consigliabile prendere in considerazione diverse configurazioni e prerequisiti di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="98947-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="98947-105">Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="98947-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="98947-106">Se si sta installando MBAM con la topologia di Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) per altre informazioni sulla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="98947-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="98947-107">Esaminare le configurazioni supportate di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="98947-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="98947-108">Dopo aver preparato l'ambiente di calcolo per l'installazione di MBAM server e client, assicurati di rivedere le configurazioni supportate per verificare che i computer in cui si sta installando MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98947-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="98947-109">Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="98947-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="98947-110">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="98947-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="98947-111">Pianificare la distribuzione di MBAM 2,0 Server e client</span><span class="sxs-lookup"><span data-stu-id="98947-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="98947-112">L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="98947-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="98947-113">Queste funzionalità possono essere installate in una configurazione distribuita in più server.</span><span class="sxs-lookup"><span data-stu-id="98947-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="98947-114">**Nota**  Un'installazione di MBAM su un singolo server è consigliata solo per gli ambienti Lab.</span><span class="sxs-lookup"><span data-stu-id="98947-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="98947-115">Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="98947-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="98947-116">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione del software aziendale o installando l'agente client nei computer client come parte del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="98947-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="98947-117">Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="98947-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="98947-118">Pianificazione della distribuzione del server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="98947-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="98947-119">Pianificazione della distribuzione del client di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="98947-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="98947-120">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="98947-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="98947-121">Pianificazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="98947-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





