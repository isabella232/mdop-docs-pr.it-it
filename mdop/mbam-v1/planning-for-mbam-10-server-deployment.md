---
title: Pianificazione della distribuzione del server di MBAM 1.0
description: Pianificazione della distribuzione del server di MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804221"
---
# <span data-ttu-id="a1fe5-103">Pianificazione della distribuzione del server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a1fe5-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="a1fe5-104">L'infrastruttura del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="a1fe5-105">Pianificazione della distribuzione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="a1fe5-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="a1fe5-106">Le caratteristiche di MBAM seguenti rappresentano l'infrastruttura server per una distribuzione di MBAM server:</span><span class="sxs-lookup"><span data-stu-id="a1fe5-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="a1fe5-107">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="a1fe5-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="a1fe5-108">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="a1fe5-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="a1fe5-109">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="a1fe5-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="a1fe5-110">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="a1fe5-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="a1fe5-111">I database e le funzionalità di MBAM server possono essere installati in configurazioni diverse, a seconda delle esigenze di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="a1fe5-112">Tutte le funzionalità di MBAM server possono essere installate in un singolo server o distribuite in più server.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="a1fe5-113">In generale, ti consigliamo di usare una configurazione a tre server o a cinque server per gli ambienti di produzione, anche se possono essere usate anche configurazioni di due o quattro server, a seconda delle esigenze di calcolo.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="a1fe5-114">**Nota**  Per altre informazioni sulla scalabilità delle prestazioni di MBAM e delle topologie di distribuzione consigliate, vedere la scalabilità di MBAM e l'elevata disponibilità della Guida white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="a1fe5-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="a1fe5-115">Ogni funzionalità di MBAM contiene prerequisiti specifici.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="a1fe5-116">Per un elenco completo dei prerequisiti di funzionalità del server e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe5-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="a1fe5-117">Oltre alle funzionalità di MBAM correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="a1fe5-118">Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="a1fe5-119">Ordine di distribuzione delle funzionalità di MBAM server</span><span class="sxs-lookup"><span data-stu-id="a1fe5-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="a1fe5-120">Quando si distribuiscono le funzionalità di MBAM server, installare le funzionalità nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="a1fe5-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="a1fe5-121">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="a1fe5-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="a1fe5-122">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="a1fe5-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="a1fe5-123">Audit e report di conformità</span><span class="sxs-lookup"><span data-stu-id="a1fe5-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="a1fe5-124">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="a1fe5-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="a1fe5-125">Modello di criteri</span><span class="sxs-lookup"><span data-stu-id="a1fe5-125">Policy Template</span></span>

<span data-ttu-id="a1fe5-126">**Nota**  Tenere traccia dei nomi dei computer in cui si installano le singole funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="a1fe5-127">Si utilizzeranno queste informazioni durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="a1fe5-128">Puoi stampare e usare un elenco di controllo della distribuzione per assisterti nel processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="a1fe5-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="a1fe5-129">Per altre informazioni sull'elenco di controllo della distribuzione di MBAM, vedere [elenco di controllo della distribuzione di mbam 1,0](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="a1fe5-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="a1fe5-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1fe5-130">Related topics</span></span>


[<span data-ttu-id="a1fe5-131">Pianificazione della distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a1fe5-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="a1fe5-132">Distribuzione dell'infrastruttura server di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a1fe5-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





