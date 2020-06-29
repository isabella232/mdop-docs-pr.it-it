---
title: Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization
description: Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization
author: dansimp
ms.assetid: c3c38930-0da3-43e6-b240-945edfd00a01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09e6943c74c7f17b6a61bc7be4bcde925a54be56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822275"
---
# <span data-ttu-id="33841-103">Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="33841-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="33841-104">Prima di iniziare la distribuzione di Microsoft Application Virtualization (App-V), potrebbe essere necessario rivedere i requisiti di ambiente che includono i requisiti hardware e software per l'installazione dei vari componenti di virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="33841-104">Before you begin the deployment of Microsoft Application Virtualization (App-V), you might have to review your environment requirements that includes the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="33841-105">Inoltre, se si esegue l'aggiornamento da una versione precedente, gli argomenti in questa sezione contengono informazioni su come eseguire l'aggiornamento delle versioni correnti di Sequencer, server e client.</span><span class="sxs-lookup"><span data-stu-id="33841-105">Also, if you are upgrading from an earlier version, the topics in this section provide information about how to upgrade your current Sequencer, Server, and Client versions.</span></span>

## <span data-ttu-id="33841-106">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="33841-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="33841-107">Requisiti per la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="33841-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="33841-108">Fornisce informazioni generali sui requisiti di sistema e sulle considerazioni sull'aggiornamento per la distribuzione della virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="33841-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-checklists"></a>[<span data-ttu-id="33841-109">Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="33841-109">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)  
<span data-ttu-id="33841-110">Fornisce elenchi dettagliati delle attività di installazione e aggiornamento con collegamenti alle procedure specifiche.</span><span class="sxs-lookup"><span data-stu-id="33841-110">Provides detailed lists of installation and upgrade tasks with links to the specific procedures.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="33841-111">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="33841-111">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="33841-112">Descrive come installare i componenti della piattaforma Application Virtualization (App-V) necessari per la distribuzione basata su server.</span><span class="sxs-lookup"><span data-stu-id="33841-112">Describes how to install the Application Virtualization (App-V) platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-manually-install-the-application-virtualization-client"></a>[<span data-ttu-id="33841-113">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="33841-113">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)  
<span data-ttu-id="33841-114">Descrive come installare il software Application Virtualization Client.</span><span class="sxs-lookup"><span data-stu-id="33841-114">Describes how to install the Application Virtualization Client software.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="33841-115">Come installare Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="33841-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="33841-116">Descrive come installare l'Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="33841-116">Describes how to install the Application Virtualization Sequencer.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="33841-117">Come aggiornare Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="33841-117">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="33841-118">Descrive come aggiornare il client Desktop Application Virtualization o l'Application Virtualization Client per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="33841-118">Describes how to upgrade the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="33841-119">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="33841-119">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="33841-120">Descrive come aggiornare i componenti software installati in tutti i computer del sistema di gestione della virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="33841-120">Describes how to upgrade the software components installed on all Application Virtualization Management System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="33841-121">Come eseguire l'aggiornamento di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="33841-121">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="33841-122">Descrive come aggiornare il sequencer nei computer che eseguono WindowsVista o WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="33841-122">Describes how to upgrade the Sequencer on computers that are running WindowsVista or WindowsXP.</span></span>

## <span data-ttu-id="33841-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33841-123">Related topics</span></span>


[<span data-ttu-id="33841-124">Riferimento per Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="33841-124">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="33841-125">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="33841-125">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="33841-126">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="33841-126">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="33841-127">Scenario di recapito autonomo per i Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="33841-127">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





