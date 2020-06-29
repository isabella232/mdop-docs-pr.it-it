---
title: Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web
description: Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823876"
---
# <span data-ttu-id="4affe-103">Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web</span><span class="sxs-lookup"><span data-stu-id="4affe-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="4affe-104">Microsoft BitLocker Administration and Monitoring (MBAM) offre contatori delle prestazioni che registrano le prestazioni delle richieste inviate ai seguenti servizi Web:</span><span class="sxs-lookup"><span data-stu-id="4affe-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="4affe-105">**StatusReportingService. svc** -servizio che riceve le richieste per lo stato di conformità</span><span class="sxs-lookup"><span data-stu-id="4affe-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="4affe-106">**CoreService. svc** -servizio che riceve le richieste per i tentativi di recupero delle chiavi</span><span class="sxs-lookup"><span data-stu-id="4affe-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="4affe-107">Contatori delle prestazioni forniti da MBAM</span><span class="sxs-lookup"><span data-stu-id="4affe-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="4affe-108">MBAM offre i contatori delle prestazioni seguenti per ognuno dei metodi pubblici implementati dai relativi servizi Web StatusReportingService e CoreService:</span><span class="sxs-lookup"><span data-stu-id="4affe-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4affe-109">Tipo di contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4affe-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="4affe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4affe-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4affe-111">Numero totale di richieste</span><span class="sxs-lookup"><span data-stu-id="4affe-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="4affe-112">Fornisce un conteggio incrementale che inizia da zero quando il server viene avviato o riavviato.</span><span class="sxs-lookup"><span data-stu-id="4affe-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="4affe-113">Offre una visualizzazione complessiva delle attività di sistema.</span><span class="sxs-lookup"><span data-stu-id="4affe-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="4affe-114">Può essere monitorata da strumenti automatizzati per garantire l'integrità del server e per verificare che il contatore venga incrementato continuamente in un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="4affe-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4affe-115">Richieste al secondo</span><span class="sxs-lookup"><span data-stu-id="4affe-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="4affe-116">Indica la velocità effettiva corrente del server MBAM in quanto supporta la base client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="4affe-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="4affe-117">Consente agli amministratori del sito di:</span><span class="sxs-lookup"><span data-stu-id="4affe-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="4affe-118">Calcolare il numero medio di richieste al secondo, in base al numero di client MBAM e alla frequenza di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="4affe-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="4affe-119">Verificare che il numero di richieste al secondo sia ampiamente correlato al numero medio calcolato di richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="4affe-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="4affe-120">Una varianza significativa può indicare che il client MBAM non è installato in una percentuale della base client o che un oggetto Criteri di gruppo di MBAM non è stato distribuito correttamente.</span><span class="sxs-lookup"><span data-stu-id="4affe-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4affe-121">Richiedi durata</span><span class="sxs-lookup"><span data-stu-id="4affe-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="4affe-122">Registra la durata delle richieste in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="4affe-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="4affe-123">Anche se questo contatore viene aggiornato con la durata di ogni richiesta, Windows Performance Monitor lo campiona solo periodicamente (in genere ogni secondo), quindi potresti vedere una certa variabilità nel valore.</span><span class="sxs-lookup"><span data-stu-id="4affe-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="4affe-124">Per questo motivo, è consigliabile usare il valore medio visualizzato da performance monitor.</span><span class="sxs-lookup"><span data-stu-id="4affe-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4affe-125">Risultati e suggerimenti per i contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4affe-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="4affe-126">Man mano che si aggiungono nuovi client MBAM a un server MBAM con capacità di riserva, si prevede di visualizzare un aumento del numero di richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="4affe-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="4affe-127">Questo aumento sarà proporzionale al numero di nuovi computer client.</span><span class="sxs-lookup"><span data-stu-id="4affe-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="4affe-128">La durata della richiesta media rimarrà relativamente statica.</span><span class="sxs-lookup"><span data-stu-id="4affe-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="4affe-129">Man mano che il server raggiunge la sua capacità massima, le richieste al secondo iniziano a livellarsi e la durata della richiesta media inizia a essere più lunga.</span><span class="sxs-lookup"><span data-stu-id="4affe-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="4affe-130">In caso di dubbi sul fatto che i server MBAM possano supportare la propria base client, valutare la possibilità di distribuire MBAM in fasi tra diverse raccolte di computer client.</span><span class="sxs-lookup"><span data-stu-id="4affe-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="4affe-131">Durante la distribuzione di MBAM in ogni raccolta di computer client, è consigliabile eseguire snapshot dei contatori delle prestazioni per vedere l'impatto relativo della distribuzione in ogni nuova raccolta di client.</span><span class="sxs-lookup"><span data-stu-id="4affe-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="4affe-132">Se il numero di richieste al secondo inizia a livellare e la durata media della richiesta aumenta, è consigliabile migliorare l'infrastruttura di MBAM server eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4affe-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="4affe-133">Spostamento del database MBAM su un cluster Microsoft SQL Server o SQL Server dedicato</span><span class="sxs-lookup"><span data-stu-id="4affe-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="4affe-134">MBAM di bilanciamento del carico in più server Web Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="4affe-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="4affe-135">Distribuzione di MBAM su hardware server più potente</span><span class="sxs-lookup"><span data-stu-id="4affe-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="4affe-136">Visualizzazione di contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="4affe-136">Viewing performance counters</span></span>


<span data-ttu-id="4affe-137">Lo strumento consigliato per la visualizzazione dei contatori delle prestazioni di MBAM è Windows Performance Monitor, che include Windows.</span><span class="sxs-lookup"><span data-stu-id="4affe-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="4affe-138">Se si usa Windows PowerShell, non è necessario abilitare i contatori prima della loro visualizzazione, perché vengono automaticamente registrati dal cmdlet **Enable-WebApplication** di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4affe-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="4affe-139">Per istruzioni dettagliate su come visualizzare i contatori delle prestazioni, vedere [come visualizzare i contatori delle prestazioni di mbam](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="4affe-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="4affe-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4affe-140">Related topics</span></span>


[<span data-ttu-id="4affe-141">Manutenzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4affe-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="4affe-142">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="4affe-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4affe-143">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4affe-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4affe-144">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4affe-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


