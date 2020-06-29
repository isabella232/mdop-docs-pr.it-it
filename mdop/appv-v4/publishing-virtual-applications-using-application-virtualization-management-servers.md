---
title: Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization
description: Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815766"
---
# <span data-ttu-id="7670b-103">Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="7670b-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="7670b-104">In una distribuzione basata su un Application Virtualization Server, i pacchetti di applicazioni virtuali che sono stati sequenziati, testati e trovati distribuibili vengono copiati nella principale condivisione di contenuto per essere usati dall'Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="7670b-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="7670b-105">Dopo aver importato i pacchetti nell'Application Virtualization Management Server, questi possono essere pubblicati agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7670b-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="7670b-106">**Nota**  La condivisione di contenuto deve trovarsi nell'archivio disco allegato del server.</span><span class="sxs-lookup"><span data-stu-id="7670b-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="7670b-107">L'uso di un dispositivo di archiviazione di rete, ad esempio una SAN o una condivisione DFS, deve essere considerato attentamente a causa dell'impatto della rete.</span><span class="sxs-lookup"><span data-stu-id="7670b-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="7670b-108">Le applicazioni vengono provisionate in gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7670b-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="7670b-109">In genere, l'amministratore di Application Virtualization creerà gruppi di Active Directory per ogni applicazione virtuale da pubblicare e quindi aggiungerà gli utenti appropriati a tali gruppi.</span><span class="sxs-lookup"><span data-stu-id="7670b-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="7670b-110">Quando gli utenti accedono alle proprie workstation, l'Application Virtualization Client, per impostazione predefinita, esegue un aggiornamento della pubblicazione usando le credenziali dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="7670b-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="7670b-111">L'utente può quindi avviare le applicazioni ovunque si trovino i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="7670b-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="7670b-112">L'amministratore di Application Virtualization determina la posizione e il numero di tasti di scelta rapida presenti nel sistema client durante la sequenziazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7670b-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="7670b-113">**Nota**  Un *aggiornamento della pubblicazione* è una chiamata al server di virtualizzazione dell'applicazione definita nel client di virtualizzazione dell'applicazione per determinare quali tasti di scelta rapida dell'applicazione virtuale vengono inviati al client per l'uso da parte dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="7670b-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="7670b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7670b-114">Related topics</span></span>


[<span data-ttu-id="7670b-115">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="7670b-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="7670b-116">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="7670b-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="7670b-117">Panoramica dei componenti del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="7670b-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="7670b-118">Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="7670b-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





