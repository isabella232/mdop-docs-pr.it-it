---
title: Architettura di alto livello per App-V 5.1
description: Architettura di alto livello per App-V 5.1
author: dansimp
ms.assetid: 90406361-55b8-40b7-85c0-449436789d4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8044c6ae9af4673ec12b47cf3b8fa73a134d9cca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805788"
---
# <span data-ttu-id="7d1c7-103">Architettura di alto livello per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7d1c7-103">High Level Architecture for App-V 5.1</span></span>


<span data-ttu-id="7d1c7-104">Usare le informazioni seguenti per semplificare la distribuzione di Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

## <span data-ttu-id="7d1c7-105">Panoramica dell'architettura</span><span class="sxs-lookup"><span data-stu-id="7d1c7-105">Architecture Overview</span></span>


<span data-ttu-id="7d1c7-106">Un'implementazione tipica di App V 5,1 è costituita dagli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-106">A typical App-V 5.1 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7d1c7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7d1c7-107">Element</span></span></th>
<th align="left"><span data-ttu-id="7d1c7-108">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="7d1c7-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d1c7-109">App-V 5,1 Management Server</span><span class="sxs-lookup"><span data-stu-id="7d1c7-109">App-V 5.1 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d1c7-110">App-V 5,1 Management Server offre funzionalità di gestione complessive per l'infrastruttura App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-110">The App-V 5.1 Management server provides overall management functionality for the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="7d1c7-111">Inoltre, è possibile installare più di un'istanza del server di gestione nell'ambiente che offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d1c7-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="7d1c7-112">Tolleranza di errore e disponibilità elevata: l'installazione e la configurazione del server di gestione App-V 5,1 in due computer distinti possono essere utili in situazioni in cui uno dei server non è disponibile o offline.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.1 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="7d1c7-113">Puoi anche migliorare la disponibilità di App-V 5,1 installando il server di gestione in più computer.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-113">You can also help increase App-V 5.1 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="7d1c7-114">In questo scenario dovrebbe essere considerato anche un bilanciamento del carico di rete in modo che le richieste del server siano bilanciate.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="7d1c7-115">Scalabilità: è possibile aggiungere altri server di gestione, se necessario, per supportare un carico elevato, ad esempio è possibile installare più server dietro un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d1c7-116">App-V 5,1 Publishing Server</span><span class="sxs-lookup"><span data-stu-id="7d1c7-116">App-V 5.1 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d1c7-117">Il server di pubblicazione App-V 5,1 offre funzionalità per l'hosting e lo streaming di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-117">The App-V 5.1 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="7d1c7-118">Il server di pubblicazione non richiede una connessione di database e supporta i protocolli seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d1c7-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="7d1c7-119">HTTP e HTTPS</span><span class="sxs-lookup"><span data-stu-id="7d1c7-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="7d1c7-120">Puoi anche migliorare la disponibilità di App-V 5,1 installando il server di pubblicazione in più computer.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-120">You can also help increase App-V 5.1 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="7d1c7-121">Un sistema di bilanciamento del carico di rete deve essere considerato anche in modo che le richieste del server siano bilanciate.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d1c7-122">App-V 5,1 Reporting Server</span><span class="sxs-lookup"><span data-stu-id="7d1c7-122">App-V 5.1 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d1c7-123">Il server di report App-V 5,1 consente agli utenti autorizzati di eseguire e visualizzare report di App-V 5,1 esistenti e report ad hoc che consentono di gestire l'infrastruttura di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-123">The App-V 5.1 Reporting server enables authorized users to run and view existing App-V 5.1 reports and ad hoc reports that can help them manage the App-V 5.1 infrastructure.</span></span> <span data-ttu-id="7d1c7-124">Il server di Reporting richiede una connessione al database di report App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-124">The Reporting server requires a connection to the App-V 5.1 reporting database.</span></span> <span data-ttu-id="7d1c7-125">Puoi anche migliorare la disponibilità di App-V 5,1 installando il server di report in più computer.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-125">You can also help increase App-V 5.1 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="7d1c7-126">Un sistema di bilanciamento del carico di rete deve essere considerato anche in modo che le richieste del server siano bilanciate.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d1c7-127">Client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7d1c7-127">App-V 5.1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d1c7-128">Il client App-V 5,1 consente di eseguire i pacchetti creati con App-V 5,1 per l'esecuzione nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-128">The App-V 5.1 client enables packages created using App-V 5.1 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7d1c7-129">**Nota**  Se si usa App-V 5,1 con Electronic Software Distribution (ESD), non è necessario usare il server di gestione di App-V 5,1, ma è comunque possibile utilizzare le funzionalità di creazione di report e flussi di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7d1c7-129">**Note** If you are using App-V 5.1 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.1 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.1.</span></span>

 






## <span data-ttu-id="7d1c7-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d1c7-130">Related topics</span></span>


[<span data-ttu-id="7d1c7-131">Attività iniziali di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7d1c7-131">Getting Started with App-V 5.1</span></span>](getting-started-with-app-v-51.md)

 

 





