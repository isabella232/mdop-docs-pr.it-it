---
title: Pianificazione della distribuzione di MBAM 1.0
description: Pianificazione della distribuzione di MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823186"
---
# <span data-ttu-id="27732-103">Pianificazione della distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="27732-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="27732-104">Prima di creare il piano di distribuzione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 1,0, è necessario considerare un certo numero di configurazioni e prerequisiti di distribuzione diversi.</span><span class="sxs-lookup"><span data-stu-id="27732-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="27732-105">Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="27732-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="27732-106">Esaminare le configurazioni supportate di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="27732-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="27732-107">Dopo aver preparato l'ambiente di elaborazione per l'installazione di MBAM client e server, assicurati di rivedere le informazioni sulle configurazioni supportate per MBAM per verificare che i computer in cui si installano MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="27732-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="27732-108">Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="27732-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="27732-109">Configurazioni supportate di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="27732-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="27732-110">Pianificare la distribuzione di MBAM 1,0 Server e client</span><span class="sxs-lookup"><span data-stu-id="27732-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="27732-111">L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="27732-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="27732-112">Queste funzionalità possono essere installate in un singolo server o distribuite in più server.</span><span class="sxs-lookup"><span data-stu-id="27732-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="27732-113">Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="27732-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="27732-114">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite strumenti come servizi di dominio Active Directory oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.</span><span class="sxs-lookup"><span data-stu-id="27732-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="27732-115">Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito usando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="27732-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="27732-116">Puoi usare uno o entrambi i metodi dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="27732-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="27732-117">Se si sceglie di usare entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.</span><span class="sxs-lookup"><span data-stu-id="27732-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="27732-118">Pianificazione della distribuzione del server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="27732-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="27732-119">Pianificazione della distribuzione del client di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="27732-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="27732-120">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="27732-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="27732-121">Pianificazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="27732-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





