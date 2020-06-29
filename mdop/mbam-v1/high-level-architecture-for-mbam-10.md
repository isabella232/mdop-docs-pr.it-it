---
title: Architettura di alto livello per MBAM 1.0
description: Architettura di alto livello per MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825236"
---
# <span data-ttu-id="7a7cb-103">Architettura di alto livello per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7a7cb-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="7a7cb-104">Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione per la crittografia dei dati client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report di BitLocker e ridurre i costi di supporto.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="7a7cb-105">MBAM include le caratteristiche descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="7a7cb-106">Inoltre, c'è un video che fornisce una panoramica dell'architettura MBAM e la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="7a7cb-107">Per altre informazioni, Vedi [Panoramica della distribuzione e dell'architettura di mbam](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="7a7cb-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="7a7cb-108">Panoramica dell'architettura</span><span class="sxs-lookup"><span data-stu-id="7a7cb-108">Architecture Overview</span></span>


<span data-ttu-id="7a7cb-109">Il diagramma seguente mostra l'architettura MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="7a7cb-110">La topologia di distribuzione di MBAM a server singolo viene visualizzata per introdurre le caratteristiche di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="7a7cb-111">Tuttavia, questa topologia di distribuzione di MBAM è consigliata solo per gli ambienti Lab.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="7a7cb-112">**Nota**  È consigliabile almeno una topologia di distribuzione di MBAM con tre computer per una distribuzione di produzione.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="7a7cb-113">Per altre informazioni sulle topologie di distribuzione di MBAM, vedere [distribuzione dell'infrastruttura del server mbam 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="7a7cb-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![una topologia di distribuzione di mbam Single Server](images/mbam-1-server.jpg)

1.  <span data-ttu-id="7a7cb-115">**Server di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="7a7cb-116">Il server di amministrazione e monitoraggio di MBAM è installato in un server Windows e ospita il sito Web di amministrazione e gestione di MBAM e i servizi Web di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="7a7cb-117">Il sito Web amministrazione e gestione di MBAM viene usato per determinare lo stato di conformità dell'organizzazione, per controllare le attività, per gestire le funzionalità hardware e per accedere ai dati di ripristino, ad esempio le chiavi di ripristino di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="7a7cb-118">Il server di amministrazione e monitoraggio si connette ai database e ai servizi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a7cb-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="7a7cb-119">Database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="7a7cb-120">Il database di ripristino e hardware viene installato in un server basato su Windows e supporta l'istanza SQLServer.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="7a7cb-121">Questo database archivia i dati di ripristino e le informazioni hardware raccolte dai computer client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="7a7cb-122">Database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-122">Compliance and Audit Database.</span></span> <span data-ttu-id="7a7cb-123">Il database di conformità e controllo viene installato in un server Windows e nell'istanza di SQLServer supportata.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="7a7cb-124">Questo database archivia i dati di conformità per i computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="7a7cb-125">Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="7a7cb-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="7a7cb-126">Report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="7a7cb-127">I report di conformità e controllo sono installati in un server basato su Windows e sono supportate istanze di SQLServer in cui è installata la funzionalità SSRS.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="7a7cb-128">Questi report includono i report di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="7a7cb-129">Questi report sono accessibili dal sito Web di amministrazione e gestione di MBAM o direttamente dal server SSRS.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="7a7cb-130">**Client mbam**.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-130">**MBAM Client**.</span></span> <span data-ttu-id="7a7cb-131">Il client di amministrazione e monitoraggio di Microsoft BitLocker esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a7cb-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="7a7cb-132">Usa criteri di gruppo per applicare la crittografia BitLocker dei computer client nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="7a7cb-133">Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).</span><span class="sxs-lookup"><span data-stu-id="7a7cb-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="7a7cb-134">Raccoglie informazioni di ripristino e informazioni hardware sui computer client.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="7a7cb-135">Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="7a7cb-136">**Modello di criteri**.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-136">**Policy Template**.</span></span> <span data-ttu-id="7a7cb-137">Il modello di criteri di gruppo di MBAM viene installato in un server Windows o un computer client supportato.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="7a7cb-138">Questo modello viene usato per specificare le impostazioni di implementazione di MBAM per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7a7cb-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="7a7cb-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a7cb-139">Related topics</span></span>


[<span data-ttu-id="7a7cb-140">Attività iniziali di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="7a7cb-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





