---
title: Pianificazione della distribuzione del server di MBAM 2.0
description: Pianificazione della distribuzione del server di MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804359"
---
# <span data-ttu-id="ef4c0-103">Pianificazione della distribuzione del server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ef4c0-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="ef4c0-104">L'infrastruttura del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="ef4c0-105">Se si sta installando l'amministrazione e il monitoraggio di Microsoft BitLocker con la topologia di Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="ef4c0-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="ef4c0-106">**Nota**  Le installazioni di amministrazione e monitoraggio di Microsoft BitLocker in un singolo server sono consigliate solo per gli ambienti di test.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="ef4c0-107">Pianificazione della distribuzione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="ef4c0-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="ef4c0-108">L'infrastruttura per una distribuzione di MBAM Server include le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef4c0-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="ef4c0-109">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="ef4c0-109">Recovery Database</span></span>

-   <span data-ttu-id="ef4c0-110">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="ef4c0-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="ef4c0-111">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="ef4c0-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="ef4c0-112">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="ef4c0-112">Self-Service Portal</span></span>

-   <span data-ttu-id="ef4c0-113">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="ef4c0-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="ef4c0-114">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="ef4c0-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="ef4c0-115">I database e le funzionalità di MBAM server possono essere installati in configurazioni diverse, a seconda dei requisiti di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="ef4c0-116">Tutte le funzionalità di MBAM server possono essere installate in un singolo server o distribuite in più server.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="ef4c0-117">È consigliabile usare una configurazione a due server per gli ambienti di produzione, anche se possono essere usate anche configurazioni da due a quattro server, a seconda dei requisiti di calcolo.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="ef4c0-118">Ogni funzionalità di MBAM contiene prerequisiti specifici.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="ef4c0-119">Per un elenco completo dei prerequisiti di funzionalità del server e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ef4c0-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="ef4c0-120">Oltre alle funzionalità di MBAM correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="ef4c0-121">Il modello contiene le impostazioni degli oggetti Criteri di gruppo (GPO) che vengono configurate per gestire la crittografia unità BitLocker nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="ef4c0-122">Questo modello può essere installato in qualsiasi computer che può eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="ef4c0-123">Man mano che pianifichi la distribuzione di MBAM server, tieni presente che le chiavi di ripristino di BitLocker in MBAM sono destinate solo all'uso singolo, dopodiché scadono i tasti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="ef4c0-124">Affinché le chiavi scadano dopo l'uso, devono essere recuperate tramite il portale help desk o il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="ef4c0-125">Ordine di distribuzione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="ef4c0-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="ef4c0-126">Per distribuire le caratteristiche di MBAM in più server, è necessario installare le funzionalità nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="ef4c0-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="ef4c0-127">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="ef4c0-127">Recovery Database</span></span>

2.  <span data-ttu-id="ef4c0-128">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="ef4c0-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="ef4c0-129">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="ef4c0-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="ef4c0-130">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="ef4c0-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="ef4c0-131">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="ef4c0-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="ef4c0-132">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="ef4c0-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="ef4c0-133">**Nota**  Tenere traccia dei nomi dei computer in cui si installano le singole funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="ef4c0-134">È necessario usare queste informazioni durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="ef4c0-135">È possibile stampare e usare un elenco di controllo della distribuzione per facilitare questo sforzo.</span><span class="sxs-lookup"><span data-stu-id="ef4c0-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="ef4c0-136">Per altre informazioni sull'elenco di controllo della distribuzione di MBAM, vedere [elenco di controllo della distribuzione di mbam 2,0](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ef4c0-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="ef4c0-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef4c0-137">Related topics</span></span>


[<span data-ttu-id="ef4c0-138">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ef4c0-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="ef4c0-139">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ef4c0-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





