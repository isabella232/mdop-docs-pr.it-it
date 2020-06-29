---
title: Pianificazione della distribuzione di Application Virtualization Client
description: Pianificazione della distribuzione di Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815955"
---
# <span data-ttu-id="e79ca-103">Pianificazione della distribuzione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="e79ca-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="e79ca-104">Dopo aver deciso come pubblicare e distribuire pacchetti di applicazioni virtuali nei computer degli utenti finali, è consigliabile pianificare la distribuzione del software Application Virtualization Client.</span><span class="sxs-lookup"><span data-stu-id="e79ca-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="e79ca-105">Il client di virtualizzazione dell'applicazione è il componente che esegue effettivamente le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="e79ca-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="e79ca-106">L'Application Virtualization Client consente agli utenti di interagire con le icone e fare doppio clic su tipi di file per avviare un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="e79ca-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="e79ca-107">Gestisce anche il flusso del contenuto dell'applicazione da un server di flusso e lo memorizza nella cache prima di avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e79ca-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="e79ca-108">Il contenuto dell'applicazione è strutturato in modo che tutto il contenuto necessario per avviare l'applicazione e gestire l'interazione iniziale dell'utente venga trasmesso prima al computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e79ca-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="e79ca-109">Esistono due tipi diversi di software client per la virtualizzazione delle applicazioni: client di virtualizzazione delle applicazioni per Servizi Desktop remoto (in precedenza Servizi terminal), usato nei sistemi server Host sessione Desktop remoto (host RDSession) e nel client Desktop Application Virtualization, usato per tutti gli altri computer.</span><span class="sxs-lookup"><span data-stu-id="e79ca-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="e79ca-110">Il client di virtualizzazione dell'applicazione deve essere configurato in fase di installazione, nella console di gestione di Application Virtualization o tramite la riga di comando del programma di installazione, con una serie di impostazioni importanti, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e79ca-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="e79ca-111">Posizioni delle icone per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e79ca-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="e79ca-112">Posizione del file OSD che contiene le informazioni sulla definizione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e79ca-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="e79ca-113">Origine contenuto applicazione.</span><span class="sxs-lookup"><span data-stu-id="e79ca-113">The application content source.</span></span>

-   <span data-ttu-id="e79ca-114">Protocollo di comunicazione da usare per il recupero degli elementi precedenti.</span><span class="sxs-lookup"><span data-stu-id="e79ca-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="e79ca-115">Metodo di gestione della dimensione della cache e della dimensione della cache da usare.</span><span class="sxs-lookup"><span data-stu-id="e79ca-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="e79ca-116">Per velocizzare la distribuzione del software Application Virtualization Client quando si usa una soluzione ESD (Electronic Software Distribution), le impostazioni precedenti devono essere definite con attenzione in anticipo.</span><span class="sxs-lookup"><span data-stu-id="e79ca-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="e79ca-117">Questo aspetto è particolarmente importante quando si hanno computer in uffici diversi, in cui i client devono essere configurati per l'uso di percorsi di origine diversi.</span><span class="sxs-lookup"><span data-stu-id="e79ca-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="e79ca-118">Nota</span><span class="sxs-lookup"><span data-stu-id="e79ca-118">Note</span></span>**  
-   <span data-ttu-id="e79ca-119">La posizione dell'icona e i valori dei file OSD sono un fattore importante da tenere in considerazione quando si sceglie il metodo di pubblicazione, se si usa Windows Installer o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="e79ca-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="e79ca-120">L'impostazione per l'origine del contenuto dell'applicazione è definita dal metodo di flusso scelto.</span><span class="sxs-lookup"><span data-stu-id="e79ca-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="e79ca-121">Per assicurarti che la cache disponga di spazio sufficiente per tutti i pacchetti che potrebbero essere distribuiti, usa l'impostazione **USA soglia di spazio libero su disco** quando configuri il client in modo che la cache possa crescere in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="e79ca-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="e79ca-122">In alternativa, determinare in anticipo la quantità di spazio su disco necessaria per la cache di App-V e, al momento dell'installazione, impostare le dimensioni della cache di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="e79ca-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="e79ca-123">Per altre informazioni sulla funzionalità di gestione dello spazio della cache, vedere **come usare la caratteristica gestione dello spazio della cache** nella Guida alle operazioni di Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="e79ca-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="e79ca-124">Durante le operazioni di pubblicazione e di flusso HTTP (S), i client App-V 4,5 SP1 usano le impostazioni del server proxy configurate in Internet Explorer nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e79ca-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="e79ca-125">Per altre informazioni sulla configurazione dei parametri di installazione del client, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e79ca-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="e79ca-126">Infine, devi determinare come distribuire il software client Desktop Application Virtualization per i client desktop.</span><span class="sxs-lookup"><span data-stu-id="e79ca-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="e79ca-127">Anche se è possibile distribuire manualmente il client Desktop Application Virtualization in ogni computer, la maggior parte delle organizzazioni dovrebbe eseguire questa operazione tramite un processo automatizzato.</span><span class="sxs-lookup"><span data-stu-id="e79ca-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="e79ca-128">Un'organizzazione di medie o grandi dimensioni potrebbe avere un sistema ESD in uso e questo sarebbe il modo ideale per distribuire il client.</span><span class="sxs-lookup"><span data-stu-id="e79ca-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="e79ca-129">Se non esiste alcun sistema ESD, è possibile usare il metodo standard per l'installazione del software nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e79ca-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="e79ca-130">Le opzioni includono criteri di gruppo o varie tecniche di scripting.</span><span class="sxs-lookup"><span data-stu-id="e79ca-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="e79ca-131">A seconda del numero e della dimensione degli uffici, questo processo di distribuzione può essere complesso ed è essenziale adottare un approccio strutturato per garantire che tutti i computer vengano installati da un client con la configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="e79ca-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="e79ca-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e79ca-132">Related topics</span></span>


[<span data-ttu-id="e79ca-133">Pianificazione della distribuzione del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="e79ca-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="e79ca-134">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="e79ca-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="e79ca-135">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="e79ca-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="e79ca-136">Come aggiornare Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="e79ca-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="e79ca-137">Come disinstallare il client App-V</span><span class="sxs-lookup"><span data-stu-id="e79ca-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





