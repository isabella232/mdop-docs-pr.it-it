---
title: Informazioni sugli ambienti virtuali
description: Informazioni sugli ambienti virtuali
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822395"
---
# <span data-ttu-id="d99c7-103">Informazioni sugli ambienti virtuali</span><span class="sxs-lookup"><span data-stu-id="d99c7-103">About Virtual Environments</span></span>


<span data-ttu-id="d99c7-104">Le applicazioni virtuali vengono eseguite in ambienti virtuali.</span><span class="sxs-lookup"><span data-stu-id="d99c7-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="d99c7-105">Gli ambienti virtuali consentono l'esecuzione di ogni applicazione su un server desktop, portatile o host sessione Desktop remoto (host RDSession) senza l'installazione e l'alterazione del sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="d99c7-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="d99c7-106">Ogni applicazione trasporta le proprie informazioni di configurazione nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="d99c7-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="d99c7-107">Di conseguenza, molte applicazioni vengono eseguite affiancate ad altre applicazioni nello stesso computer senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="d99c7-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="d99c7-108">Le applicazioni virtuali vengono eseguite localmente, in modo che vengano eseguite con prestazioni, funzionalità e accesso completo ai servizi locali che ci si aspetterebbe da qualsiasi applicazione installata localmente.</span><span class="sxs-lookup"><span data-stu-id="d99c7-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="d99c7-109">Poiché ogni applicazione viene eseguita in un ambiente virtuale, vengono ridotti i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d99c7-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="d99c7-110">Conflitti tra applicazioni: in ambienti che non usano la virtualizzazione delle applicazioni, è necessario testare a fondo ogni applicazione per verificare che non interferisca con altre applicazioni installate.</span><span class="sxs-lookup"><span data-stu-id="d99c7-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="d99c7-111">Test di regressione: poiché l'applicazione non modifica il sistema operativo sottostante, viene eliminato un lungo test di regressione.</span><span class="sxs-lookup"><span data-stu-id="d99c7-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="d99c7-112">Incompatibilità della versione: le diverse versioni della stessa applicazione possono essere eseguite contemporaneamente nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="d99c7-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="d99c7-113">Accesso multiutente: le applicazioni che non vengono eseguite in modalità multiutente e pertanto non possono essere eseguite all'interno di un host RDSession, ora possono farlo e funzionare correttamente per più utenti in un singolo host di RDSession.</span><span class="sxs-lookup"><span data-stu-id="d99c7-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="d99c7-114">Problemi di multilocazione: due istanze della stessa applicazione che usano configurazioni diverse possono essere eseguite nello stesso computer nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="d99c7-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="d99c7-115">Server Siloing: viene eliminata la necessità di molte farm server separate.</span><span class="sxs-lookup"><span data-stu-id="d99c7-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="d99c7-116">Gli ambienti virtuali includono un registro di sistema virtuale per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="d99c7-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="d99c7-117">Le impostazioni del registro di sistema create da un'applicazione non possono essere visualizzate da altre applicazioni o utilità, ad esempio Regedit.</span><span class="sxs-lookup"><span data-stu-id="d99c7-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="d99c7-118">Invece di copiare l'intero registro di sistema, il registro di sistema virtuale usa un metodo di *sovrapposizione* .</span><span class="sxs-lookup"><span data-stu-id="d99c7-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="d99c7-119">Gli elementi nel registro di sistema client possono essere letti dall'applicazione purché una copia virtuale dell'elemento del registro di sistema non sia inclusa nel registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d99c7-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="d99c7-120">Tutte le Scritture dell'applicazione nel registro di sistema sono contenute nel registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d99c7-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="d99c7-121">Gli ambienti virtuali includono anche un file system virtuale e altri componenti virtuali, inclusi i servizi virtuali e i COM virtuali.</span><span class="sxs-lookup"><span data-stu-id="d99c7-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="d99c7-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d99c7-122">Related topics</span></span>


[<span data-ttu-id="d99c7-123">Panoramica di Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="d99c7-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





