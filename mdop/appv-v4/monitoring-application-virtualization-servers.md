---
title: Monitoraggio di Application Virtualization Server
description: Monitoraggio di Application Virtualization Server
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816145"
---
# <span data-ttu-id="b47f3-103">Monitoraggio di Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="b47f3-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="b47f3-104">Per semplificare la gestione del server Application Virtualization (App-V), è possibile usare System Center Operations Manager2007 Management Pack.</span><span class="sxs-lookup"><span data-stu-id="b47f3-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="b47f3-105">Questo Management Pack supporta solo i server di 4,5 Application Virtualization (App-V); non supporta versioni precedenti del server.</span><span class="sxs-lookup"><span data-stu-id="b47f3-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="b47f3-106">Il Management Pack massimizza la disponibilità di App-V Server per la gestione delle richieste client App-V.</span><span class="sxs-lookup"><span data-stu-id="b47f3-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="b47f3-107">Indicatori di stato</span><span class="sxs-lookup"><span data-stu-id="b47f3-107">Status Indicators</span></span>


<span data-ttu-id="b47f3-108">Gli indicatori di stato di integrità di App-V Server sono contraddistinti da colori.</span><span class="sxs-lookup"><span data-stu-id="b47f3-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="b47f3-109">I colori rappresentano i valori di stato seguenti:</span><span class="sxs-lookup"><span data-stu-id="b47f3-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="b47f3-110">Nessun colore indica che il server è in uso senza errori non risolvibili.</span><span class="sxs-lookup"><span data-stu-id="b47f3-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="b47f3-111">Giallo indica che uno dei componenti non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b47f3-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="b47f3-112">La funzionalità complessiva del server è degradata, ma il server è ancora disponibile.</span><span class="sxs-lookup"><span data-stu-id="b47f3-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="b47f3-113">Rosso indica che il server non è disponibile e che non può concedere servizi chiave o comunicare con le dipendenze del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="b47f3-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="b47f3-114">Criteri di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b47f3-114">Monitoring Criteria</span></span>


<span data-ttu-id="b47f3-115">Il Management Pack monitora gli aspetti seguenti dell'integrità del server:</span><span class="sxs-lookup"><span data-stu-id="b47f3-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="b47f3-116">Stato server: monitora gli eventi del server per verificare che il server stia fornendo i servizi previsti.</span><span class="sxs-lookup"><span data-stu-id="b47f3-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="b47f3-117">Accesso all'archivio dati: consente di tenere traccia della capacità di uno o più server di gestione di App-V di accedere e comunicare con l'App-V Data Store.</span><span class="sxs-lookup"><span data-stu-id="b47f3-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="b47f3-118">Accesso ai dati del contenuto: consente di monitorare l'accesso alla directory \\Content, che potrebbe essere una directory locale o una condivisione di rete, nonché la possibilità di leggere i file richiesti.</span><span class="sxs-lookup"><span data-stu-id="b47f3-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="b47f3-119">Sicurezza: segnala gli errori relativi al certificato e alle comunicazioni sicure del server App-V.</span><span class="sxs-lookup"><span data-stu-id="b47f3-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="b47f3-120">Gestione delle richieste client: monitora la capacità di uno o più server App-V di gestire e rispondere correttamente alle richieste del client.</span><span class="sxs-lookup"><span data-stu-id="b47f3-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="b47f3-121">Queste richieste includono la pubblicazione di elementi come le richieste di configurazione, le richieste di caricamento dei pacchetti e le richieste fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="b47f3-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="b47f3-122">Configurazione server: consente di controllare le impostazioni di configurazione del server App-V.</span><span class="sxs-lookup"><span data-stu-id="b47f3-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="b47f3-123">Queste impostazioni di configurazione includono le impostazioni nel registro di sistema e nell'archivio dati App-V.</span><span class="sxs-lookup"><span data-stu-id="b47f3-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="b47f3-124">Differenze tra server</span><span class="sxs-lookup"><span data-stu-id="b47f3-124">Server Differences</span></span>


<span data-ttu-id="b47f3-125">Le principali differenze tra App-V Management Server e App-V Streaming Server sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="b47f3-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="b47f3-126">I server di gestione di App-V possono creare servizi di pubblicazione, streaming, gestione e Reporting.</span><span class="sxs-lookup"><span data-stu-id="b47f3-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="b47f3-127">Di conseguenza, il Management Pack può gestire più aspetti del server di gestione di App-V che può gestire in App-V Streaming Server, che fornisce solo il flusso di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b47f3-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="b47f3-128">App-V Streaming Server non ha un archivio dati App-V, quindi l'accesso all'archivio dati non viene monitorato.</span><span class="sxs-lookup"><span data-stu-id="b47f3-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="b47f3-129">Le informazioni di configurazione per l'App-V Streaming Server vengono gestite nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b47f3-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="b47f3-130">App-V Streaming Server non usa l'interfaccia della console di gestione di App-V Server; usare altri strumenti per gestire la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b47f3-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="b47f3-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b47f3-131">Related topics</span></span>


[<span data-ttu-id="b47f3-132">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="b47f3-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





