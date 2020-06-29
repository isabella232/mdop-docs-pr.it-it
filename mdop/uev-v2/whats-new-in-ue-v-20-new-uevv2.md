---
title: Novità in UE-V 2.0
description: Novità in UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824965"
---
# <span data-ttu-id="b0d95-103">Novità in UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="b0d95-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="b0d95-104">Microsoft User Experience Virtualization (UE-V) 2,0 offre queste nuove caratteristiche e funzionalità rispetto a UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="b0d95-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="b0d95-105">Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) contengono ulteriori informazioni sulla versione UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="b0d95-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="b0d95-106">La cache lato client (CSC) non è più necessaria</span><span class="sxs-lookup"><span data-stu-id="b0d95-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="b0d95-107">Questa versione di UE-V introduce il **provider di sincronizzazione**, che sostituisce il requisito della funzionalità file offline di Windows per supportare una cache lato client di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b0d95-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="b0d95-108">Mentre UE-V consente di sincronizzare le impostazioni solo quando un'applicazione è stata aperta, chiusa o quando Windows è stato bloccato o sbloccato oppure all'accesso o alla disconnessione, anche il provider di sincronizzazione...</span><span class="sxs-lookup"><span data-stu-id="b0d95-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="b0d95-109">Sincronizza l'applicazione locale e le impostazioni di Windows fuori banda usando "**eventi trigger**"</span><span class="sxs-lookup"><span data-stu-id="b0d95-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="b0d95-110">Usa un' **attività pianificata** per sincronizzare il pacchetto di archiviazione delle impostazioni in qualsiasi intervallo scelto per i requisiti aziendali (ogni 30 minuti per impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0d95-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="b0d95-111">Alcune condizioni garantiscono una sincronizzazione più frequente.</span><span class="sxs-lookup"><span data-stu-id="b0d95-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="b0d95-112">Le impostazioni vengono sincronizzate quando l'utente fa clic sul pulsante **Sincronizza ora** nell'applicazione nuovo centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="b0d95-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="b0d95-113">Il provider di sincronizzazione può anche iniziare per una singola applicazione senza attendere l'attività di sincronizzazione pianificata.</span><span class="sxs-lookup"><span data-stu-id="b0d95-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="b0d95-114">Ad esempio, quando un'applicazione viene chiusa, le modifiche apportate alle impostazioni vengono scritte nella cache locale e il processo del provider di sincronizzazione viene eseguito in modo asincrono per trasferire le nuove impostazioni nella posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b0d95-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="b0d95-115">Sincronizzazione delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="b0d95-115">Windows app synchronization</span></span>


<span data-ttu-id="b0d95-116">Lo sviluppatore di un'app di Windows può definire le impostazioni, se presenti, da sincronizzare e queste impostazioni ora possono essere acquisite e sincronizzate con UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0d95-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="b0d95-117">Per impostazione predefinita, UE-V sincronizza le impostazioni di molte delle app di Windows incluse in Windows 8 e Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="b0d95-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="b0d95-118">Puoi modificare l'elenco delle app sincronizzate con Windows PowerShell, Strumentazione gestione Windows (WMI) o criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b0d95-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="b0d95-119">**Nota**  UE-V non sincronizza le impostazioni delle app di Windows se gli utenti del dominio collegano le credenziali di accesso al proprio account Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0d95-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="b0d95-120">Questo collegamento sincronizza le impostazioni con Microsoft OneDrive in modo che UE-V Sincronizza solo le applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="b0d95-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="b0d95-121">Collegamento a un account Microsoft</span><span class="sxs-lookup"><span data-stu-id="b0d95-121">Microsoft account linking</span></span>


<span data-ttu-id="b0d95-122">La sincronizzazione delle impostazioni tramite OneDrive è una novità di Windows 8 quando è stato effettuato l'accesso con un account Microsoft o se si collega l'account Microsoft al proprio account di dominio.</span><span class="sxs-lookup"><span data-stu-id="b0d95-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="b0d95-123">Se un utente di dominio USA UE-V e ha eseguito l'accesso a un account Microsoft, allora...</span><span class="sxs-lookup"><span data-stu-id="b0d95-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="b0d95-124">UE-V Sincronizza solo le impostazioni per le applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="b0d95-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="b0d95-125">L'account Microsoft gestisce le impostazioni delle app di Windows e le impostazioni desktop di Windows</span><span class="sxs-lookup"><span data-stu-id="b0d95-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="b0d95-126">Centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="b0d95-126">Company Settings Center</span></span>


<span data-ttu-id="b0d95-127">Puoi offrire agli utenti un certo controllo sulle impostazioni sincronizzate tramite un'applicazione in UE-V 2 denominata centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="b0d95-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="b0d95-128">Il centro impostazioni società viene installato insieme all'agente UE-V e gli utenti possono accedervi dal pannello di controllo, dal menu **Start** o dalla schermata **Start** e dall'icona dell'area di notifica UE-v.</span><span class="sxs-lookup"><span data-stu-id="b0d95-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="b0d95-129">Il centro impostazioni società Visualizza le impostazioni sincronizzate e consente agli utenti di visualizzare lo stato di sincronizzazione di UE-V.</span><span class="sxs-lookup"><span data-stu-id="b0d95-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="b0d95-130">Se si consente loro, gli utenti possono usare il centro impostazioni società per selezionare le impostazioni da sincronizzare.</span><span class="sxs-lookup"><span data-stu-id="b0d95-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="b0d95-131">Possono anche fare clic sul pulsante **Sincronizza ora** per sincronizzare tutte le impostazioni immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b0d95-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="b0d95-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0d95-132">Related topics</span></span>


[<span data-ttu-id="b0d95-133">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b0d95-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="b0d95-134">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b0d95-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="b0d95-135">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="b0d95-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





