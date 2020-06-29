---
title: Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti
description: Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815125"
---
# <span data-ttu-id="bbaf6-103">Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti</span><span class="sxs-lookup"><span data-stu-id="bbaf6-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="bbaf6-104">Se non si dispone di un sistema ESD esistente per distribuire la soluzione di virtualizzazione dell'applicazione o non si vuole usarla, sarà necessario installare uno o più server di gestione della virtualizzazione delle applicazioni come nucleo dell'architettura di sistema.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="bbaf6-105">L'Application Virtualization Management Server richiede un computer server dedicato e necessita di un database di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="bbaf6-106">Il database può essere nello stesso server oppure può essere configurato in un server di database aziendale accessibile per l'Application Virtualization Management Server tramite una connessione LAN ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="bbaf6-107">Inoltre, è necessario installare Microsoft Application Virtualization Management Console, sia nell'Application Virtualization Management Server che in una workstation di gestione designata, e sarà necessario installare il servizio Web Microsoft Application Virtualization Management, che può essere installato anche nel server di gestione della virtualizzazione dell'applicazione o in un server IIS separato.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="bbaf6-108">L'Application Virtualization Management Console viene usato per la connessione al servizio Web Application Virtualization Management, che consente all'amministratore di sistema di interagire con l'Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="bbaf6-109">**Nota**  L'accesso alle applicazioni viene controllato tramite gruppi di sicurezza in servizi di dominio Active Directory, quindi sarà necessario pianificare un processo per configurare un gruppo di sicurezza per ogni applicazione virtualizzata e per la gestione degli utenti aggiunti a ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="bbaf6-110">L'amministratore di Application Virtualization Management Server configura il server per l'uso di questi gruppi di Active Directory e il server controlla automaticamente l'accesso ai pacchetti in base all'appartenenza ai gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="bbaf6-111">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="bbaf6-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="bbaf6-112">Panoramica dei componenti del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bbaf6-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="bbaf6-113">Elenca e descrive i componenti principali di Microsoft Application Virtualization Management System.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="bbaf6-114">Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bbaf6-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="bbaf6-115">Viene fornita una breve panoramica del modo in cui vengono pubblicate le applicazioni virtuali in uno scenario di distribuzione basato su server Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="bbaf6-116">Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="bbaf6-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="bbaf6-117">Descrive le opzioni disponibili per l'uso dei server di streaming Application Virtualization in combinazione con l'implementazione basata su Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="bbaf6-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbaf6-118">Related topics</span></span>


[<span data-ttu-id="bbaf6-119">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="bbaf6-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="bbaf6-120">Pianificazione della distribuzione del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bbaf6-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





