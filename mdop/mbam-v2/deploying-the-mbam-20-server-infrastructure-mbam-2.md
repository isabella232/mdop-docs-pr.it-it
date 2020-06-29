---
title: Distribuzione dell'infrastruttura server di MBAM 2.0
description: Distribuzione dell'infrastruttura server di MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824756"
---
# <span data-ttu-id="929a1-103">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="929a1-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="929a1-104">Le funzionalità del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker per la topologia autonoma possono essere installate in configurazioni diverse in due o più server in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="929a1-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="929a1-105">La configurazione consigliata è due server per un ambiente di produzione, a seconda dei requisiti di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="929a1-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="929a1-106">Usare un singolo server per un'installazione di MBAM solo in ambienti di test.</span><span class="sxs-lookup"><span data-stu-id="929a1-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="929a1-107">Per altre informazioni sulla pianificazione della distribuzione delle funzionalità di MBAM server, vedere [pianificazione della distribuzione di mbam 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="929a1-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="929a1-108">Il diagramma seguente mostra un esempio di come è possibile configurare la distribuzione di MBAM a due server consigliata.</span><span class="sxs-lookup"><span data-stu-id="929a1-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="929a1-109">Questa configurazione supporta fino a 200.000 client MBAM in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="929a1-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="929a1-110">Le caratteristiche e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati sotto il computer o il server in cui è consigliabile installarli.</span><span class="sxs-lookup"><span data-stu-id="929a1-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![MBAM 2 2-topologia di distribuzione server](images/mbam2-3-servers.gif)

## <span data-ttu-id="929a1-112">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="929a1-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="929a1-113">In questo server sono installate le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="929a1-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="929a1-114">**Server di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="929a1-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="929a1-115">La funzionalità Amministrazione e monitoraggio Server è installata in un server Windows ed è costituita dal sito Web dell'help desk e dai servizi Web di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="929a1-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="929a1-116">**Portale self-service**.</span><span class="sxs-lookup"><span data-stu-id="929a1-116">**Self-Service Portal**.</span></span> <span data-ttu-id="929a1-117">Il portale self-service è installato in un server Windows.</span><span class="sxs-lookup"><span data-stu-id="929a1-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="929a1-118">Il portale self-service consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, in cui possono ottenere una chiave di ripristino per recuperare un volume di BitLocker bloccato.</span><span class="sxs-lookup"><span data-stu-id="929a1-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="929a1-119">Server di database</span><span class="sxs-lookup"><span data-stu-id="929a1-119">Database Server</span></span>


<span data-ttu-id="929a1-120">In questo server sono installate le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="929a1-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="929a1-121">**Database di ripristino**.</span><span class="sxs-lookup"><span data-stu-id="929a1-121">**Recovery Database**.</span></span> <span data-ttu-id="929a1-122">Il database di ripristino viene installato in un server Windows e un'istanza supportata di Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="929a1-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="929a1-123">Questo database archivia i dati di recupero raccolti dai computer client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="929a1-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="929a1-124">**Database di conformità e controllo**.</span><span class="sxs-lookup"><span data-stu-id="929a1-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="929a1-125">Il database di conformità e controllo viene installato in un server Windows e un'istanza supportata di SQLServer.</span><span class="sxs-lookup"><span data-stu-id="929a1-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="929a1-126">Questo database archivia i dati di conformità per i computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="929a1-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="929a1-127">Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="929a1-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="929a1-128">**Report di conformità e controllo**.</span><span class="sxs-lookup"><span data-stu-id="929a1-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="929a1-129">I report di conformità e controllo vengono installati in un server Windows e un'istanza supportata di SQLServer con la funzionalità SQL Server Reporting Services (SSRS) installata.</span><span class="sxs-lookup"><span data-stu-id="929a1-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="929a1-130">Questi report includono i report di MBAM a cui è possibile accedere dal sito Web dell'help desk o direttamente dal server SSRS.</span><span class="sxs-lookup"><span data-stu-id="929a1-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="929a1-131">Workstation di gestione</span><span class="sxs-lookup"><span data-stu-id="929a1-131">Management Workstation</span></span>


<span data-ttu-id="929a1-132">La caratteristica seguente è installata nella workstation di gestione, che può essere un computer Windows Server o client.</span><span class="sxs-lookup"><span data-stu-id="929a1-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="929a1-133">**Modello di criteri**.</span><span class="sxs-lookup"><span data-stu-id="929a1-133">**Policy Template**.</span></span> <span data-ttu-id="929a1-134">Il modello di criteri è costituito da criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="929a1-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="929a1-135">È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione, che è un computer Windows Server o client supportato.</span><span class="sxs-lookup"><span data-stu-id="929a1-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="929a1-136">La workstation non deve essere un computer dedicato.</span><span class="sxs-lookup"><span data-stu-id="929a1-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="929a1-137">Client MBAM</span><span class="sxs-lookup"><span data-stu-id="929a1-137">MBAM Client</span></span>


<span data-ttu-id="929a1-138">Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="929a1-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="929a1-139">Usa criteri di gruppo per applicare la crittografia unità BitLocker dei computer client nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="929a1-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="929a1-140">Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).</span><span class="sxs-lookup"><span data-stu-id="929a1-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="929a1-141">Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="929a1-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="929a1-142">Altre risorse per la distribuzione delle funzionalità di MBAM 2,0 Server</span><span class="sxs-lookup"><span data-stu-id="929a1-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="929a1-143">Distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="929a1-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





