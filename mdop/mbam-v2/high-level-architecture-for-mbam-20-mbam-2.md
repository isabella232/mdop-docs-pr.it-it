---
title: Architettura di alto livello per MBAM 2.0
description: Architettura di alto livello per MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824705"
---
# <span data-ttu-id="b67d6-103">Architettura di alto livello per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b67d6-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="b67d6-104">Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report su BitLocker e ridurre i costi di supporto.</span><span class="sxs-lookup"><span data-stu-id="b67d6-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="b67d6-105">L'amministrazione e il monitoraggio di Microsoft BitLocker includono le caratteristiche descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="b67d6-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="b67d6-106">L'amministrazione e il monitoraggio di Microsoft BitLocker possono essere distribuiti nella topologia autonoma o in una topologia integrata con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="b67d6-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="b67d6-107">Questo argomento descrive l'architettura per la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="b67d6-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="b67d6-108">Per informazioni sulla distribuzione nella topologia di Configuration Manager integrata, vedere [uso di mbam con Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="b67d6-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="b67d6-109">Il diagramma seguente mostra l'architettura di MBAM recommended per un ambiente di produzione, costituito da due server e una workstation di gestione.</span><span class="sxs-lookup"><span data-stu-id="b67d6-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="b67d6-110">Questa architettura supporta fino a 200.000 client MBAM.</span><span class="sxs-lookup"><span data-stu-id="b67d6-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="b67d6-111">Le caratteristiche e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati sotto il computer o il server in cui è consigliabile installarli.</span><span class="sxs-lookup"><span data-stu-id="b67d6-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="b67d6-112">**Nota**  Un'architettura a server singolo deve essere usata solo in ambienti di test.</span><span class="sxs-lookup"><span data-stu-id="b67d6-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![MBAM 2 2-topologia di distribuzione server](images/mbam2-3-servers.gif)

## <span data-ttu-id="b67d6-114">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b67d6-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="b67d6-115">In questo server sono installate le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="b67d6-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="b67d6-116">**Server di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="b67d6-117">La funzionalità Amministrazione e monitoraggio Server è installata in un server Windows ed è costituita dal sito Web di amministrazione e monitoraggio, che include i report e il portale help desk e i servizi Web di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b67d6-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="b67d6-118">**Portale self-service**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-118">**Self-Service Portal**.</span></span> <span data-ttu-id="b67d6-119">Il portale self-service è installato in un server Windows.</span><span class="sxs-lookup"><span data-stu-id="b67d6-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="b67d6-120">Il portale self-service consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, in cui possono ottenere una chiave di ripristino per recuperare un volume di BitLocker bloccato.</span><span class="sxs-lookup"><span data-stu-id="b67d6-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="b67d6-121">Server di database</span><span class="sxs-lookup"><span data-stu-id="b67d6-121">Database Server</span></span>


<span data-ttu-id="b67d6-122">In questo server sono installate le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="b67d6-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="b67d6-123">**Database di ripristino**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-123">**Recovery Database**.</span></span> <span data-ttu-id="b67d6-124">Il database di ripristino viene installato in un server Windows e un'istanza supportata di Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="b67d6-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="b67d6-125">Questo database archivia i dati di recupero raccolti dai computer client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="b67d6-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="b67d6-126">**Database di conformità e controllo**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="b67d6-127">Il database di conformità e controllo viene installato in un server Windows e un'istanza supportata di SQLServer.</span><span class="sxs-lookup"><span data-stu-id="b67d6-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="b67d6-128">Questo database archivia i dati di conformità per i computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="b67d6-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="b67d6-129">Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="b67d6-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="b67d6-130">**Report di conformità e controllo**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="b67d6-131">I report di conformità e controllo vengono installati in un server Windows e un'istanza supportata di SQLServer con la funzionalità SQL Server Reporting Services (SSRS) installata.</span><span class="sxs-lookup"><span data-stu-id="b67d6-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="b67d6-132">Questi report includono i report di MBAM a cui è possibile accedere dal sito Web di amministrazione e monitoraggio o direttamente dal server SSRS.</span><span class="sxs-lookup"><span data-stu-id="b67d6-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="b67d6-133">Workstation di gestione</span><span class="sxs-lookup"><span data-stu-id="b67d6-133">Management Workstation</span></span>


<span data-ttu-id="b67d6-134">La caratteristica seguente è installata nella workstation di gestione, che può essere un computer Windows Server o client.</span><span class="sxs-lookup"><span data-stu-id="b67d6-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="b67d6-135">**Modello di criteri**.</span><span class="sxs-lookup"><span data-stu-id="b67d6-135">**Policy Template**.</span></span> <span data-ttu-id="b67d6-136">Il modello di criteri è costituito da impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b67d6-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="b67d6-137">È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione, che è un computer Windows Server o client supportato.</span><span class="sxs-lookup"><span data-stu-id="b67d6-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="b67d6-138">La workstation non deve essere un computer dedicato.</span><span class="sxs-lookup"><span data-stu-id="b67d6-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="b67d6-139">Client MBAM</span><span class="sxs-lookup"><span data-stu-id="b67d6-139">MBAM Client</span></span>


<span data-ttu-id="b67d6-140">Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="b67d6-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="b67d6-141">Usa criteri di gruppo per applicare la crittografia unità BitLocker dei computer client nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b67d6-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="b67d6-142">Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).</span><span class="sxs-lookup"><span data-stu-id="b67d6-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="b67d6-143">Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="b67d6-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="b67d6-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b67d6-144">Related topics</span></span>


[<span data-ttu-id="b67d6-145">Attività iniziali di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b67d6-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





