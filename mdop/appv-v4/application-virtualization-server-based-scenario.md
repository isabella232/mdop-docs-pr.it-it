---
title: Scenario basato su Application Virtualization Server
description: Scenario basato su Application Virtualization Server
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819526"
---
# <span data-ttu-id="3a31e-103">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3a31e-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="3a31e-104">Se si prevede di usare uno scenario di distribuzione basato su server per l'ambiente di Microsoft Application Virtualization (App-V), è necessario comprendere le differenze tra Application Virtualization Management Server e Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="3a31e-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="3a31e-105">Gli argomenti di questa sezione descrivono queste differenze e contengono anche informazioni sui metodi di recapito dei pacchetti, sui protocolli di trasmissione e sui componenti esterni da tenere in considerazione quando si continua la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3a31e-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="3a31e-106">Questa sezione contiene anche procedure dettagliate per l'installazione e la configurazione di App-V Management Server e dei server di streaming Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="3a31e-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="3a31e-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="3a31e-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="3a31e-108">Panoramica di uno scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="3a31e-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="3a31e-109">Fornisce informazioni importanti sulla distribuzione su Application Virtualization Management Server, Application Virtualization Streaming Server e i metodi di distribuzione dei pacchetti, i protocolli e i componenti esterni rilevanti per il piano di distribuzione basato su server.</span><span class="sxs-lookup"><span data-stu-id="3a31e-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="3a31e-110">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="3a31e-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="3a31e-111">Descrive come installare i componenti della piattaforma Microsoft Application Virtualization necessari per la distribuzione basata su server.</span><span class="sxs-lookup"><span data-stu-id="3a31e-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="3a31e-112">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="3a31e-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="3a31e-113">Descrive come configurare l'Application Virtualization Management Server, l'Application Virtualization Streaming Server, il server IIS (Internet Information Integration) e il file server.</span><span class="sxs-lookup"><span data-stu-id="3a31e-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="3a31e-114">Come configurare una cache di sola lettura sul client App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="3a31e-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="3a31e-115">Descrive come configurare il client App-V per l'uso della cache di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3a31e-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="3a31e-116">Come configurare una cache di sola lettura sul client App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="3a31e-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="3a31e-117">Descrive come configurare il client App-V per l'uso della cache di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3a31e-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="3a31e-118">Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V</span><span class="sxs-lookup"><span data-stu-id="3a31e-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="3a31e-119">Descrive come configurare il mirroring del database usando Microsoft SQL Server per il sistema App-V.</span><span class="sxs-lookup"><span data-stu-id="3a31e-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="3a31e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3a31e-120">Reference</span></span>


[<span data-ttu-id="3a31e-121">Parametri della riga di comando del programma di installazione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="3a31e-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="3a31e-122">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="3a31e-122">Related Sections</span></span>


[<span data-ttu-id="3a31e-123">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="3a31e-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="3a31e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a31e-124">Related topics</span></span>


[<span data-ttu-id="3a31e-125">Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="3a31e-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="3a31e-126">Scenario di recapito autonomo per i Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="3a31e-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





