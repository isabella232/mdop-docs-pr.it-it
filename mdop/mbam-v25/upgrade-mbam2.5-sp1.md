---
title: Aggiornamento da MBAM 2,5 a MBAM 2,5 SP1 Service Update Release
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804474"
---
# <span data-ttu-id="da5d3-102">Aggiornamento da MBAM 2,5 a MBAM 2,5 SP1 aggiornamento della versione di manutenzione</span><span class="sxs-lookup"><span data-stu-id="da5d3-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="da5d3-103">Questo articolo fornisce istruzioni dettagliate per aggiornare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 per MBAM 2,5 Service Pack 1 (SP1) insieme a [Microsoft Desktop Optimization Pack (MDOP) maggio 2019 manutenzione aggiornamento](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in una configurazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="da5d3-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="da5d3-104">In questa guida useremo una configurazione a due server.</span><span class="sxs-lookup"><span data-stu-id="da5d3-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="da5d3-105">Un server sarà un server di database che sta usando Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="da5d3-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="da5d3-106">Questo server ospiterà i database e i report di MBAM.</span><span class="sxs-lookup"><span data-stu-id="da5d3-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="da5d3-107">L'altro server sarà un server Web di Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="da5d3-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="da5d3-108">Questo server ospiterà "amministrazione e monitoraggio" e "portale self-service".</span><span class="sxs-lookup"><span data-stu-id="da5d3-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="da5d3-109">Preparare l'aggiornamento MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="da5d3-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="da5d3-110">Conoscere i server MBAM nell'ambiente</span><span class="sxs-lookup"><span data-stu-id="da5d3-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="da5d3-111">Motore di database di SQL Server: server che ospita i database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="da5d3-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="da5d3-112">SQL Server Reporting Services: server che ospita i report di MBAM.</span><span class="sxs-lookup"><span data-stu-id="da5d3-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="da5d3-113">Server Web di Internet Information Services (IIS): server che ospita le applicazioni Web MBAM e i servizi MBAM.</span><span class="sxs-lookup"><span data-stu-id="da5d3-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="da5d3-114">Opzionale Server del sito principale di Microsoft System Center Configuration Manager: l'applicazione di configurazione MBAM viene eseguita su questo server per integrare i report di MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="da5d3-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="da5d3-115">Questi report vengono quindi Uniti con i report di gestione configurazione esistenti nell'istanza di SQL Server Reporting Services (SSRS) di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="da5d3-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="da5d3-116">Identificare gli account del servizio, i gruppi, il nome del server e l'URL report</span><span class="sxs-lookup"><span data-stu-id="da5d3-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="da5d3-117">Identificare l'account del servizio di pool di applicazioni MBAM usato dai server Web IIS per leggere e scrivere dati nei database di MBAM.</span><span class="sxs-lookup"><span data-stu-id="da5d3-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="da5d3-118">Identificare i gruppi usati durante la configurazione delle caratteristiche Web di MBAM e l'URL del servizio Web report.</span><span class="sxs-lookup"><span data-stu-id="da5d3-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="da5d3-119">Identificare il nome e il nome dell'istanza di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da5d3-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="da5d3-120">Guarda questo video per saperne di più.</span><span class="sxs-lookup"><span data-stu-id="da5d3-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="da5d3-121">Identificare l'account di SQL Server Reporting Services usato per leggere i dati di conformità dal database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="da5d3-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="da5d3-122">Guarda questo video per saperne di più.</span><span class="sxs-lookup"><span data-stu-id="da5d3-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="da5d3-123">Aggiornare l'infrastruttura MBAM all'ultima versione disponibile</span><span class="sxs-lookup"><span data-stu-id="da5d3-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="da5d3-124">L'installazione o l'aggiornamento di MBAM Server Infrastructure viene sempre eseguito nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="da5d3-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="da5d3-125">Motore di database di SQL Server: database</span><span class="sxs-lookup"><span data-stu-id="da5d3-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="da5d3-126">SQL Server Reporting Services: report</span><span class="sxs-lookup"><span data-stu-id="da5d3-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="da5d3-127">Server Web: applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="da5d3-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="da5d3-128">Server SCCM: report integrati di SCCM se applicabile</span><span class="sxs-lookup"><span data-stu-id="da5d3-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="da5d3-129">Client: agente MBAM o aggiornamento client</span><span class="sxs-lookup"><span data-stu-id="da5d3-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="da5d3-130">Modelli di criteri di gruppo: aggiornare i criteri di gruppo esistenti con i nuovi modelli e abilitare le nuove impostazioni per i criteri di gruppo di MBAM esistenti</span><span class="sxs-lookup"><span data-stu-id="da5d3-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="da5d3-131">È consigliabile creare un backup completo dei database MBAM prima di eseguire gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="da5d3-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="da5d3-132">Aggiornare il MBAM SQL Server</span><span class="sxs-lookup"><span data-stu-id="da5d3-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="da5d3-133">Guardare questo video per informazioni su come eseguire l'aggiornamento di MBAM SQL Server:</span><span class="sxs-lookup"><span data-stu-id="da5d3-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="da5d3-134">Aggiornare il server Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="da5d3-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="da5d3-135">Guardare questo video per informazioni su come aggiornare il server Web di MBAM:</span><span class="sxs-lookup"><span data-stu-id="da5d3-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="da5d3-136">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="da5d3-136">More information</span></span>

<span data-ttu-id="da5d3-137">Per altre informazioni sui problemi noti di MBAM 2,5 SP1, vedere [Note sulla versione per mbam 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="da5d3-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
