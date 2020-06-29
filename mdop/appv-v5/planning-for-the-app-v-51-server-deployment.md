---
title: Pianificazione della distribuzione del server App-V 5.1
description: Pianificazione della distribuzione del server App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804977"
---
# <span data-ttu-id="e8e59-103">Pianificazione della distribuzione del server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e8e59-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="e8e59-104">L'infrastruttura server di Microsoft Application Virtualization (App-V) 5,1 è costituita da un set di caratteristiche specializzate che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8e59-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="e8e59-105">Pianificazione della distribuzione di App-V 5,1 server</span><span class="sxs-lookup"><span data-stu-id="e8e59-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="e8e59-106">Il server App-V 5,1 è costituito dalle caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8e59-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="e8e59-107">Server di gestione: offre funzionalità di gestione complessive per l'infrastruttura App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="e8e59-108">Database di gestione: consente di semplificare le predistribuzioni di database per la gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="e8e59-109">Publishing Server: offre funzionalità di hosting e flusso per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="e8e59-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="e8e59-110">Reporting Server: offre app-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="e8e59-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="e8e59-111">Database delle relazioni: consente di semplificare le predistribuzioni di database per la creazione di report in App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="e8e59-112">Nell'elenco seguente sono visualizzati i metodi consigliati per l'installazione dell'infrastruttura server App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="e8e59-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="e8e59-113">Installare il server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="e8e59-114">Per altre informazioni, vedere [come distribuire il server App-V 5,1](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="e8e59-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="e8e59-115">Installare le funzionalità di database, creazione di report e gestione in computer distinti.</span><span class="sxs-lookup"><span data-stu-id="e8e59-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="e8e59-116">Per altre informazioni, vedere [come installare i database di gestione e Reporting in computer separati da gestione e Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span><span class="sxs-lookup"><span data-stu-id="e8e59-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="e8e59-117">Usare Electronic Software Distribution (ESD).</span><span class="sxs-lookup"><span data-stu-id="e8e59-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="e8e59-118">Per altre informazioni, Vedi [come distribuire pacchetti App-V 5,1 usando la distribuzione elettronica del software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="e8e59-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="e8e59-119">Installare tutte le funzionalità del server in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="e8e59-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="e8e59-120">Interazione del server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="e8e59-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="e8e59-121">Questa sezione contiene informazioni sul modo in cui i vari ruoli del server App-V 5,1 interagiscono tra loro.</span><span class="sxs-lookup"><span data-stu-id="e8e59-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="e8e59-122">Il server di gestione di App-V 5,1 contiene il repository dei pacchetti e le relative configurazioni assegnate.</span><span class="sxs-lookup"><span data-stu-id="e8e59-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="e8e59-123">Per i server di pubblicazione registrati con il server di gestione, i metadati associati vengono forniti ai server di pubblicazione per l'uso quando le richieste di aggiornamento della pubblicazione vengono ricevute dai computer che eseguono il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="e8e59-124">I server di pubblicazione App-V 5,1 gestiti da un singolo server di gestione possono servire diversi client e possono avere nomi di siti Web e binding di porta diversi.</span><span class="sxs-lookup"><span data-stu-id="e8e59-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="e8e59-125">Inoltre, tutti i server di pubblicazione gestiti dallo stesso server di gestione sono repliche.</span><span class="sxs-lookup"><span data-stu-id="e8e59-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="e8e59-126">**Nota**  Il server di gestione non esegue alcun bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e8e59-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="e8e59-127">I metadati associati vengono semplicemente passati al server di pubblicazione per l'utilizzo durante l'elaborazione delle richieste client.</span><span class="sxs-lookup"><span data-stu-id="e8e59-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="e8e59-128">Protocolli correlati al server e funzionalità esterne</span><span class="sxs-lookup"><span data-stu-id="e8e59-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="e8e59-129">Le informazioni seguenti visualizzano i protocolli relativi al server usati dai server App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e8e59-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="e8e59-130">La tabella include anche il meccanismo di creazione di report per ogni tipo di server.</span><span class="sxs-lookup"><span data-stu-id="e8e59-130">The table also includes the reporting mechanism for each server type.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8e59-131">Tipo di server</span><span class="sxs-lookup"><span data-stu-id="e8e59-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="e8e59-132">Protocolli</span><span class="sxs-lookup"><span data-stu-id="e8e59-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="e8e59-133">Caratteristiche esterne necessarie</span><span class="sxs-lookup"><span data-stu-id="e8e59-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="e8e59-134">Creazione di rapporti</span><span class="sxs-lookup"><span data-stu-id="e8e59-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8e59-135">Server IIS</span><span class="sxs-lookup"><span data-stu-id="e8e59-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="e8e59-136">HTTP</span></span></p>
<p><span data-ttu-id="e8e59-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="e8e59-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-138">Questa combinazione di protocollo server richiede un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso.</span><span class="sxs-lookup"><span data-stu-id="e8e59-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="e8e59-139">Quando si usa HTTP o HTTPS, usare un server IIS e un firewall per proteggere il server dall'esposizione a Internet.</span><span class="sxs-lookup"><span data-stu-id="e8e59-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-140">Interna</span><span class="sxs-lookup"><span data-stu-id="e8e59-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8e59-141">File</span><span class="sxs-lookup"><span data-stu-id="e8e59-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-142">SMB</span><span class="sxs-lookup"><span data-stu-id="e8e59-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-143">Questa combinazione di protocollo server richiede il supporto per sincronizzare il contenuto tra il server di gestione e il server di flusso.</span><span class="sxs-lookup"><span data-stu-id="e8e59-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="e8e59-144">Usare un computer client con funzionalità di condivisione o flusso di file.</span><span class="sxs-lookup"><span data-stu-id="e8e59-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8e59-145">Interna</span><span class="sxs-lookup"><span data-stu-id="e8e59-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="e8e59-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8e59-146">Related topics</span></span>


[<span data-ttu-id="e8e59-147">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="e8e59-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="e8e59-148">Distribuzione del server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e8e59-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





