---
title: Scenario basato sulla distribuzione elettronica del software
description: Scenario basato sulla distribuzione elettronica del software
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821595"
---
# <span data-ttu-id="8ff21-103">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="8ff21-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="8ff21-104">Se si prevede di usare uno scenario di distribuzione ESD (Electronic Software Distribution) per l'ambiente di virtualizzazione delle applicazioni Microsoft, è importante comprendere i fattori che sono interessati da tale decisione.</span><span class="sxs-lookup"><span data-stu-id="8ff21-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="8ff21-105">Gli argomenti in questa sezione descrivono lo scenario ESD e offrono informazioni sui metodi di distribuzione dei pacchetti, i protocolli di trasmissione e i componenti esterni che è necessario considerare nella strategia di implementazione.</span><span class="sxs-lookup"><span data-stu-id="8ff21-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="8ff21-106">È anche possibile usare le procedure descritte in questa sezione per completare la distribuzione, dalla fase di configurazione del server alla fase di verifica della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8ff21-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="8ff21-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="8ff21-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="8ff21-108">Panoramica di uno scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="8ff21-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="8ff21-109">Fornisce informazioni importanti sui metodi di pubblicazione e flusso che è possibile usare per una distribuzione basata su ESD.</span><span class="sxs-lookup"><span data-stu-id="8ff21-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="8ff21-110">Come configurare i server per la distribuzione basata su ESD</span><span class="sxs-lookup"><span data-stu-id="8ff21-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="8ff21-111">Questa sezione contiene le procedure che è possibile usare per configurare l'Application Virtualization Streaming Servers, il server IIS e il file server per la strategia di distribuzione basata sulla distribuzione del software elettronico.</span><span class="sxs-lookup"><span data-stu-id="8ff21-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="8ff21-112">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="8ff21-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="8ff21-113">Fornisce le procedure della riga di comando per installare il client di virtualizzazione dell'applicazione, usando il file setup.exe o setup.msi.</span><span class="sxs-lookup"><span data-stu-id="8ff21-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="8ff21-114">Come disinstallare il client App-V</span><span class="sxs-lookup"><span data-stu-id="8ff21-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="8ff21-115">Fornisce una procedura dettagliata che consente di verificare che il client di virtualizzazione dell'applicazione sia stato installato e funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="8ff21-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="8ff21-116">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="8ff21-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="8ff21-117">Fornisce le procedure della riga di comando per la pubblicazione di un pacchetto dell'applicazione, tramite Windows Installer o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="8ff21-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="8ff21-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8ff21-118">Reference</span></span>


[<span data-ttu-id="8ff21-119">Parametri della riga di comando del programma di installazione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8ff21-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="8ff21-120">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="8ff21-120">Related Sections</span></span>


[<span data-ttu-id="8ff21-121">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="8ff21-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="8ff21-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ff21-122">Related topics</span></span>


[<span data-ttu-id="8ff21-123">Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8ff21-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="8ff21-124">Scenario di recapito autonomo per i Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8ff21-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





