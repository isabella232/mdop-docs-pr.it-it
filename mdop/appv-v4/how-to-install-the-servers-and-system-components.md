---
title: Come installare i server e i componenti del sistema
description: Come installare i server e i componenti del sistema
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817245"
---
# <span data-ttu-id="cbbb0-103">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="cbbb0-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="cbbb0-104">Prima di poter consegnare le applicazioni agli utenti, è necessario installare i componenti della piattaforma Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="cbbb0-105">Gli argomenti di questa sezione contengono le informazioni necessarie per installare i server di virtualizzazione dell'applicazione e gli altri componenti del sistema di virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="cbbb0-106">**Nota**  Le procedure descritte in questa sezione consentono di eseguire un'installazione personalizzata, in cui vengono scelti e scelti i componenti da installare in computer separati, come consigliato in un ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="cbbb0-107">Tuttavia, le tue procedure operative potrebbero dettare un approccio diverso e durante il processo di installazione potresti voler raggruppare i componenti.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="cbbb0-108">Indipendentemente dalla posizione in cui vengono installati i componenti, è possibile installarli in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="cbbb0-109">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="cbbb0-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="cbbb0-110">Come installare il server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="cbbb0-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="cbbb0-111">Fornisce una procedura dettagliata per l'installazione di Application Virtualization Management Server e l'assegnazione al gruppo di server appropriato.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="cbbb0-112">Come installare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="cbbb0-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="cbbb0-113">Fornisce una procedura dettagliata per l'installazione di Application Virtualization Streaming Server e l'assegnazione al gruppo di server appropriato.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="cbbb0-114">Come installare il servizio Gestione Web</span><span class="sxs-lookup"><span data-stu-id="cbbb0-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="cbbb0-115">Fornisce una procedura dettagliata per l'installazione del servizio Web Application Virtualization Management in un computer di destinazione della rete.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="cbbb0-116">Come installare la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cbbb0-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="cbbb0-117">Fornisce una procedura dettagliata per l'installazione della console di gestione della virtualizzazione dell'applicazione in un computer di destinazione della rete.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="cbbb0-118">Come installare un database</span><span class="sxs-lookup"><span data-stu-id="cbbb0-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="cbbb0-119">Fornisce una procedura dettagliata per l'installazione di un database per la distribuzione basata su server della virtualizzazione delle applicazioni, se un database non è già disponibile.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="cbbb0-120">Come rimuovere i componenti del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="cbbb0-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="cbbb0-121">Fornisce procedure dettagliate per rimuovere tutti i componenti software di virtualizzazione dell'applicazione o selezionati da un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cbbb0-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="cbbb0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbbb0-122">Related topics</span></span>


[<span data-ttu-id="cbbb0-123">Panoramica di uno scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="cbbb0-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="cbbb0-124">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="cbbb0-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="cbbb0-125">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="cbbb0-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 





