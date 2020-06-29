---
title: Distribuzione dell'infrastruttura server di MBAM 1.0
description: Distribuzione dell'infrastruttura server di MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825176"
---
# <span data-ttu-id="38c53-103">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="38c53-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="38c53-104">È possibile installare le caratteristiche del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in diverse configurazioni usando uno-cinque server.</span><span class="sxs-lookup"><span data-stu-id="38c53-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="38c53-105">In genere, è consigliabile usare una configurazione di tre-cinque server per gli ambienti di produzione, a seconda delle esigenze di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="38c53-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="38c53-106">Per altre informazioni sulla scalabilità delle prestazioni di MBAM e delle topologie di distribuzione consigliate, vedere la [scalabilità di mbam e la Guida di alta disponibilità di white paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="38c53-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="38c53-107">Distribuire tutti i MBAM 1,0 su un singolo server</span><span class="sxs-lookup"><span data-stu-id="38c53-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="38c53-108">In questa configurazione tutte le funzionalità di MBAM sono installate in un singolo server.</span><span class="sxs-lookup"><span data-stu-id="38c53-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="38c53-109">Questa topologia di distribuzione per MBAM Server Infrastructure supporta fino a 21.000 computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="38c53-110">**Importante**  Questa configurazione è supportata, ma è consigliabile solo per i test.</span><span class="sxs-lookup"><span data-stu-id="38c53-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="38c53-111">Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM in un singolo server.</span><span class="sxs-lookup"><span data-stu-id="38c53-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="38c53-112">Come installare e configurare MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="38c53-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="38c53-113">Distribuire MBAM 1,0 nei server distribuiti</span><span class="sxs-lookup"><span data-stu-id="38c53-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="38c53-114">Le funzionalità di MBAM possono essere installate in diverse configurazioni, a seconda delle esigenze di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="38c53-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="38c53-115">Per altre informazioni su come pianificare la distribuzione delle funzionalità di MBAM server, vedere [pianificazione della distribuzione di mbam 1,0 Server](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="38c53-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="38c53-116">Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM nei server distribuiti.</span><span class="sxs-lookup"><span data-stu-id="38c53-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="38c53-117">Configurazione con tre computer</span><span class="sxs-lookup"><span data-stu-id="38c53-117">Three-computer configuration</span></span>

<span data-ttu-id="38c53-118">Il diagramma seguente mostra la topologia di distribuzione di tre computer per MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="38c53-119">Questa topologia è consigliata per gli ambienti di produzione che supportano fino a 55.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![mbam tre topologia di distribuzione del computer](images/mbam-3-server.jpg)

<span data-ttu-id="38c53-121">In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:</span><span class="sxs-lookup"><span data-stu-id="38c53-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="38c53-122">Database di ripristino e hardware, database di conformità e controllo e report di conformità e controllo sono installati in un server.</span><span class="sxs-lookup"><span data-stu-id="38c53-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="38c53-123">La funzionalità Amministrazione e monitoraggio Server è installata in un server.</span><span class="sxs-lookup"><span data-stu-id="38c53-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="38c53-124">Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38c53-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="38c53-125">Configurazione a quattro computer</span><span class="sxs-lookup"><span data-stu-id="38c53-125">Four-computer configuration</span></span>

<span data-ttu-id="38c53-126">Il diagramma seguente mostra la topologia di distribuzione di quattro computer per MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="38c53-127">Questa topologia è stata consigliata per gli ambienti di produzione che supportano fino a 110.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![mbam Four computer topologia di distribuzione.](images/mbam-4-computer.jpg)

<span data-ttu-id="38c53-129">In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:</span><span class="sxs-lookup"><span data-stu-id="38c53-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="38c53-130">Database di ripristino e hardware, database di conformità e controllo e report di conformità e controllo sono installati in un server.</span><span class="sxs-lookup"><span data-stu-id="38c53-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="38c53-131">La funzionalità Amministrazione e monitoraggio Server è installata in un server configurato in un cluster di server NLB (Network Load Balancing).</span><span class="sxs-lookup"><span data-stu-id="38c53-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="38c53-132">Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38c53-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="38c53-133">Configurazione a cinque computer</span><span class="sxs-lookup"><span data-stu-id="38c53-133">Five-computer configuration</span></span>

<span data-ttu-id="38c53-134">Il diagramma seguente mostra la topologia di distribuzione di cinque computer per MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="38c53-135">Questa topologia è consigliata per gli ambienti di produzione che supportano fino a 135.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="38c53-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![la topologia di distribuzione del computer mbam Five.](images/mbam-5-computer.jpg)

<span data-ttu-id="38c53-137">In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:</span><span class="sxs-lookup"><span data-stu-id="38c53-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="38c53-138">Il database di ripristino e hardware viene installato in un server.</span><span class="sxs-lookup"><span data-stu-id="38c53-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="38c53-139">Il database di conformità e controllo e i report di conformità e controllo sono installati in un server.</span><span class="sxs-lookup"><span data-stu-id="38c53-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="38c53-140">La funzionalità Amministrazione e monitoraggio Server è installata in un server configurato in un cluster di server NLB (Network Load Balancing).</span><span class="sxs-lookup"><span data-stu-id="38c53-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="38c53-141">Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="38c53-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="38c53-142">Come installare e configurare MBAM su server distribuiti</span><span class="sxs-lookup"><span data-stu-id="38c53-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="38c53-143">Come configurare Bilanciamento carico di rete per MBAM</span><span class="sxs-lookup"><span data-stu-id="38c53-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="38c53-144">Altre risorse per la distribuzione delle funzionalità di MBAM 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="38c53-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="38c53-145">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="38c53-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





