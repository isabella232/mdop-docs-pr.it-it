---
title: Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione
description: Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816266"
---
# <span data-ttu-id="40806-103">Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="40806-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="40806-104">Questa guida alla sicurezza di Microsoft Application Virtualization (App-V) offre istruzioni per gli amministratori responsabili della configurazione delle funzionalità di sicurezza selezionate per la distribuzione di App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="40806-105">**Nota**  Questa documentazione non fornisce indicazioni per la scelta delle opzioni di sicurezza specifiche.</span><span class="sxs-lookup"><span data-stu-id="40806-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="40806-106">Queste informazioni sono disponibili nel white paper sulle procedure consigliate per l'App-V Security Best Practices <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="40806-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="40806-107">L'amministratore di App-V che usa questa guida deve avere familiarità con le tecnologie correlate alla sicurezza seguenti:</span><span class="sxs-lookup"><span data-stu-id="40806-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="40806-108">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="40806-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="40806-109">Infrastruttura a chiave pubblica (PKI)</span><span class="sxs-lookup"><span data-stu-id="40806-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="40806-110">IPsec (Internet Protocol Security)</span><span class="sxs-lookup"><span data-stu-id="40806-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="40806-111">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="40806-111">Group Policies</span></span>

-   <span data-ttu-id="40806-112">Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="40806-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="40806-113">Componenti dell'infrastruttura APP-V</span><span class="sxs-lookup"><span data-stu-id="40806-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="40806-114">Quando si pianifica un ambiente App-V di sicurezza avanzato, è possibile considerare diversi modelli di infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="40806-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="40806-115">**Nota**  Per altre informazioni sui modelli di infrastruttura di App-V, vedere la documentazione seguente:</span><span class="sxs-lookup"><span data-stu-id="40806-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="40806-116">Guida alla pianificazione e distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="40806-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="40806-117">Serie di guide di progettazione e pianificazione delle infrastrutture</span><span class="sxs-lookup"><span data-stu-id="40806-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="40806-118">Questi modelli usano alcuni ma forse non tutti i componenti App-V descritti nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="40806-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![diagramma di Office Branch App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="40806-120">Application Virtualization (App-V) Management Server</span><span class="sxs-lookup"><span data-stu-id="40806-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="40806-121">App-V Management Server trasmette il contenuto del pacchetto e pubblica i collegamenti e le associazioni di tipi di file al client App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="40806-122">App-V Management Server supporta inoltre l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="40806-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="40806-123">Application Virtualization (App-V) streaming server</span><span class="sxs-lookup"><span data-stu-id="40806-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="40806-124">App-V Streaming Server ospita i pacchetti per lo streaming in client App-V in ambienti come le succursali, in cui la larghezza di banda della connessione al server di gestione di App-V è insufficiente per il flusso di contenuto del pacchetto nei client.</span><span class="sxs-lookup"><span data-stu-id="40806-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="40806-125">Il server di streaming contiene solo funzionalità di flusso e non fornisce la console di gestione di App-V o il servizio Web di gestione App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="40806-126">Archivio dati Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="40806-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="40806-127">L'App-V Data Store, nel database SQL, mantiene le informazioni correlate all'infrastruttura App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="40806-128">Le informazioni nell'archivio dati di App-V includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che gestiscono l'ambiente di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40806-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="40806-129">Servizio di gestione di Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="40806-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="40806-130">Il servizio di gestione App-V comunica le richieste di lettura/scrittura all'archivio dati della virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40806-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="40806-131">Questo componente può essere installato nello stesso computer del server di gestione App-V o in un computer separato con IIS installato.</span><span class="sxs-lookup"><span data-stu-id="40806-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="40806-132">Console di gestione di Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="40806-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="40806-133">App-V Management Console è un'utilità di gestione dello snap-in per l'amministrazione di App-V Server.</span><span class="sxs-lookup"><span data-stu-id="40806-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="40806-134">Questo componente può essere installato nello stesso computer del server App-V o in una workstation separata con MMC 3.0 e. NET 2.0 installato.</span><span class="sxs-lookup"><span data-stu-id="40806-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="40806-135">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="40806-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="40806-136">App-V Sequencer monitora e acquisisce l'installazione delle applicazioni e crea pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="40806-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="40806-137">L'output del sequencer è costituito dall'icona dell'applicazione, dal file OSD che contiene le informazioni sulla definizione dell'applicazione, da un file manifesto del pacchetto e da un file SFT contenente i file di contenuto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40806-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="40806-138">Facoltativamente, è possibile creare un file di Windows Installer per l'installazione del pacchetto senza usare l'infrastruttura App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="40806-139">Client di Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="40806-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="40806-140">Il client App-V è installato nel computer client Desktop App-V o nel computer client di Servizi terminal App-V.</span><span class="sxs-lookup"><span data-stu-id="40806-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="40806-141">Fornisce l'ambiente virtuale per i pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="40806-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="40806-142">Il client App-V gestisce il flusso del pacchetto nella cache, nell'aggiornamento della pubblicazione delle applicazioni virtuali e nell'interazione con i server di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40806-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





