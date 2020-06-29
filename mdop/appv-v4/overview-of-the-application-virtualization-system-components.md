---
title: Panoramica dei componenti del sistema Application Virtualization
description: Panoramica dei componenti del sistema Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816055"
---
# <span data-ttu-id="8a246-103">Panoramica dei componenti del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8a246-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="8a246-104">La tabella seguente descrive i componenti principali di Microsoft Application Virtualization Management System.</span><span class="sxs-lookup"><span data-stu-id="8a246-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="8a246-105">Per altre informazioni sulla distribuzione di questi componenti di sistema, Vedi [scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="8a246-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a246-106">Componente</span><span class="sxs-lookup"><span data-stu-id="8a246-106">Component</span></span></th>
<th align="left"><span data-ttu-id="8a246-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="8a246-107">Function</span></span></th>
<th align="left"><span data-ttu-id="8a246-108">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="8a246-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a246-109">Microsoft Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="8a246-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-110">Il componente responsabile per lo streaming del contenuto del pacchetto e la pubblicazione dei collegamenti e delle associazioni di tipi di file nel client di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a246-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-111">L'Application Virtualization Management Server supporta l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="8a246-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8a246-112"></strong>Cartella contenuto</span><span class="sxs-lookup"><span data-stu-id="8a246-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-113">Posizione dei pacchetti di virtualizzazione dell'applicazione per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="8a246-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-114">Questa cartella può essere posizionata in una condivisione inserita o disattivata dall'Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="8a246-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="8a246-115">La cartella può essere posizionata anche in una rete di archiviazione (SAN).</span><span class="sxs-lookup"><span data-stu-id="8a246-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a246-116">Microsoft Application Virtualization Management Console</span><span class="sxs-lookup"><span data-stu-id="8a246-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-117">Un'utilità di gestione degli snap-in MMC 3,0 per l'amministrazione di Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="8a246-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-118">Questo componente può essere installato nel server Microsoft Application Virtualization o posizionato in una workstation separata con MMC 3.0 e. NET 2.0 installato.</span><span class="sxs-lookup"><span data-stu-id="8a246-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a246-119">Servizio Web Microsoft Application Virtualization Management</span><span class="sxs-lookup"><span data-stu-id="8a246-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-120">Il componente responsabile per comunicare eventuali richieste di lettura/scrittura all'archivio dati di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a246-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-121">Questo componente può essere installato nel server Microsoft Application Virtualization o in un computer separato con IIS installato.</span><span class="sxs-lookup"><span data-stu-id="8a246-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a246-122">Archivio dati di Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8a246-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-123">Il componente archiviato nel database SQL e responsabile dell'archiviazione di tutte le informazioni relative all'infrastruttura di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a246-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-124">Queste informazioni includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che hanno la responsabilità di gestire l'ambiente di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a246-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a246-125">Microsoft Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="8a246-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-126">Il componente responsabile dell'hosting dei pacchetti di virtualizzazione dell'applicazione per il flusso di lavoro ai client in una filiale, in cui il collegamento all'Application Virtualization Management Server è considerato un WAN.</span><span class="sxs-lookup"><span data-stu-id="8a246-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-127">Questo server contiene solo funzionalità di flusso e non fornisce né l'Application Virtualization Management Console né il servizio Web Application Virtualization Management.</span><span class="sxs-lookup"><span data-stu-id="8a246-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a246-128">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8a246-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-129">Il componente usato per monitorare e acquisire l'installazione di applicazioni per creare pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="8a246-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-130">L'output è costituito dalle icone dell'applicazione, da un file OSD che contiene informazioni sulla definizione del pacchetto, da un file manifesto del pacchetto e dal file SFT che contiene i file di contenuto del programma applicativo.</span><span class="sxs-lookup"><span data-stu-id="8a246-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a246-131">Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8a246-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-132">Il componente installato nel client Desktop Application Virtualization o nel client di virtualizzazione dell'applicazione per Servizi Desktop remoto (in precedenza Servizi terminal) e che fornisce l'ambiente virtuale per le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="8a246-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a246-133">Il client Microsoft Application Virtualization gestisce il flusso del pacchetto in cache, aggiornamento della pubblicazione, trasporto e tutte le interazioni con i server di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a246-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8a246-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a246-134">Related topics</span></span>


[<span data-ttu-id="8a246-135">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="8a246-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="8a246-136">Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="8a246-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="8a246-137">Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8a246-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





