---
title: Panoramica di uno scenario basato sulla distribuzione elettronica del software
description: Panoramica di uno scenario basato sulla distribuzione elettronica del software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821596"
---
# <span data-ttu-id="fca56-103">Panoramica di uno scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="fca56-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="fca56-104">Se si prevede di usare una soluzione ESD (Electronic Software Distribution) per distribuire applicazioni virtuali, è importante comprendere i fattori che entrano e sono interessati da tale decisione.</span><span class="sxs-lookup"><span data-stu-id="fca56-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="fca56-105">Questo argomento descrive i vantaggi derivanti dall'uso di uno scenario basato su ESD e fornisce informazioni sui metodi di pubblicazione e flusso di pacchetti che è necessario considerare mentre si procede alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fca56-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="fca56-106">**Importante**  Qualsiasi soluzione ESD si usi, è necessario avere familiarità con i requisiti della soluzione specifica.</span><span class="sxs-lookup"><span data-stu-id="fca56-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="fca56-107">Se si usa Microsoft endpoint Configuration Manager, vedere la documentazione di Configuration Manager in <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="fca56-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="fca56-108">L'uso di un sistema ESD esistente offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fca56-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="fca56-109">Elimina le infrastrutture di gestione duale</span><span class="sxs-lookup"><span data-stu-id="fca56-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="fca56-110">Riduce il costo di hardware aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="fca56-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="fca56-111">Riduce il costo delle licenze aggiuntive per il sistema operativo e il database</span><span class="sxs-lookup"><span data-stu-id="fca56-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="fca56-112">Metodi di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="fca56-112">Publishing Methods</span></span>


<span data-ttu-id="fca56-113">Quando si usa uno scenario basato su ESD, sono disponibili le opzioni seguenti per pubblicare l'applicazione nei client:</span><span class="sxs-lookup"><span data-stu-id="fca56-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="fca56-114">Windows Installer autonomo.</span><span class="sxs-lookup"><span data-stu-id="fca56-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="fca56-115">Il file di Windows Installer contiene il manifesto e i file OSD e ICO che i client usano per configurare un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fca56-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="fca56-116">Il file di Windows Installer copia anche il file SFT nel client perché questo scenario non usa un server.</span><span class="sxs-lookup"><span data-stu-id="fca56-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="fca56-117">Windows Installer con il manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fca56-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="fca56-118">Il file di Windows Installer contiene il manifesto e i file OSD e ICO che i client usano per configurare un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fca56-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="fca56-119">Il file SFT è archiviato in un server.</span><span class="sxs-lookup"><span data-stu-id="fca56-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="fca56-120">Un parametro della riga di comando indirizza il client alla posizione del file SFT.</span><span class="sxs-lookup"><span data-stu-id="fca56-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="fca56-121">Comandi di SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="fca56-121">SFTMIME commands.</span></span>** <span data-ttu-id="fca56-122">I comandi di SFTMIME vengono usati con i file manifest, OSD, ICO e SFT per aggiungere pacchetti al client.</span><span class="sxs-lookup"><span data-stu-id="fca56-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="fca56-123">Il file manifesto deve essere nel computer client oppure deve essere accessibile tramite un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="fca56-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="fca56-124">A seconda della configurazione del client e delle opzioni della riga di comando, i file OSD, ICO e SFT possono essere presenti nel computer client o in un server.</span><span class="sxs-lookup"><span data-stu-id="fca56-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="fca56-125">Per informazioni più dettagliate sui metodi di pubblicazione precedenti, vedere [determinare il metodo di pubblicazione](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="fca56-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="fca56-126">Metodi di flusso del pacchetto</span><span class="sxs-lookup"><span data-stu-id="fca56-126">Package Streaming Methods</span></span>


<span data-ttu-id="fca56-127">Dovrai determinare il metodo che il sistema di virtualizzazione dell'applicazione userà per trasmettere i pacchetti di applicazioni virtuali o i file SFT dal server ai client.</span><span class="sxs-lookup"><span data-stu-id="fca56-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="fca56-128">Sono disponibili le opzioni di flusso seguenti:</span><span class="sxs-lookup"><span data-stu-id="fca56-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="fca56-129">Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="fca56-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="fca56-130">Se usi una Application Virtualization Streaming Server nella tua configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="fca56-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="fca56-131">È necessario installare il software server in un computer ed è necessario configurarlo tramite il registro di sistema, ma questa configurazione non dipende da servizi come SQL o servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fca56-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="fca56-132">I file SFT sono archiviati nel server in una posizione accessibile dai client.</span><span class="sxs-lookup"><span data-stu-id="fca56-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="fca56-133">Le informazioni di pubblicazione possono essere distribuite ai client tramite qualsiasi meccanismo di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fca56-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="fca56-134">Tuttavia, quando è configurato, il client riceve gli aggiornamenti del pacchetto automaticamente e l'aggiornamento attivo è supportato.</span><span class="sxs-lookup"><span data-stu-id="fca56-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="fca56-135">Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="fca56-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="fca56-136">Se usi un Application Virtualization Management Server nella tua configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="fca56-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="fca56-137">Puoi gestire questo server tramite la console di gestione di Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="fca56-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="fca56-138">Questa configurazione usa un database SQL e servizi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fca56-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="fca56-139">Il server può distribuire le informazioni di pubblicazione ai client, quindi non sono necessari meccanismi di pubblicazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fca56-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="fca56-140">File server.</span><span class="sxs-lookup"><span data-stu-id="fca56-140">File server.</span></span>** <span data-ttu-id="fca56-141">Se si usa un file server nella configurazione, i file SFT vengono trasmessi agli altri computer client usando i protocolli SMB.</span><span class="sxs-lookup"><span data-stu-id="fca56-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="fca56-142">I file server usati in questa configurazione vengono gestiti creando elenchi di controllo di accesso (ACL) nei file condivisioni e SFT.</span><span class="sxs-lookup"><span data-stu-id="fca56-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="fca56-143">È necessario prestare attenzione per indirizzare i client ai file corretti nel file server.</span><span class="sxs-lookup"><span data-stu-id="fca56-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="fca56-144">Server IIS.</span><span class="sxs-lookup"><span data-stu-id="fca56-144">IIS server.</span></span>** <span data-ttu-id="fca56-145">Se si usa un server IIS nella propria configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fca56-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="fca56-146">Il server IIS è facile da configurare e gestire.</span><span class="sxs-lookup"><span data-stu-id="fca56-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="fca56-147">È necessario prestare attenzione per indirizzare i client ai file corretti nel server IIS.</span><span class="sxs-lookup"><span data-stu-id="fca56-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="fca56-148">Per informazioni più dettagliate sui metodi di flusso precedenti, vedere [determinare il metodo di flusso](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="fca56-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="fca56-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fca56-149">Related topics</span></span>


[<span data-ttu-id="fca56-150">Parametri della riga di comando del programma di installazione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fca56-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="fca56-151">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="fca56-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="fca56-152">Determinare il metodo di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="fca56-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="fca56-153">Determinare il metodo di streaming</span><span class="sxs-lookup"><span data-stu-id="fca56-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="fca56-154">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="fca56-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="fca56-155">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="fca56-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





