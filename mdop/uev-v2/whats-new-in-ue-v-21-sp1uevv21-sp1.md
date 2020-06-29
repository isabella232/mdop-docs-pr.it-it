---
title: Novità in UE-V 2.1 SP1
description: Novità in UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827426"
---
# <span data-ttu-id="62007-103">Novità in UE-V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="62007-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="62007-104">Esperienza utente virtualizzazione 2,1 SP1 offre queste nuove funzionalità e funzionalità rispetto a UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="62007-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="62007-105">Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) contengono ulteriori informazioni sulla versione UE-v 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="62007-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="62007-106">Supporto per Windows 10</span><span class="sxs-lookup"><span data-stu-id="62007-106">Support for Windows 10</span></span>


<span data-ttu-id="62007-107">UE-V 2,1 SP1 aggiunge il supporto per Windows 10, oltre allo stesso software supportato nelle versioni precedenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="62007-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="62007-108">Compatibilità con Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="62007-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="62007-109">Windows 10 consente agli utenti aziendali di sincronizzare le impostazioni delle app di Windows e le impostazioni del sistema operativo Windows in Azure anziché in OneDrive.</span><span class="sxs-lookup"><span data-stu-id="62007-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="62007-110">Puoi usare la funzionalità di sincronizzazione di Windows 10 Enterprise insieme a UE-V solo per i computer locali uniti al dominio.</span><span class="sxs-lookup"><span data-stu-id="62007-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="62007-111">Per consentire la coesistenza tra Windows 10 e UE-V, è necessario disabilitare i modelli UE-V seguenti usando PowerShell per ogni client o criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="62007-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="62007-112">In criteri di gruppo, in Microsoft User Experience Virtualization node, configurare queste impostazioni dei criteri:</span><span class="sxs-lookup"><span data-stu-id="62007-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="62007-113">Abilitare "non sincronizzare le app di Windows"</span><span class="sxs-lookup"><span data-stu-id="62007-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="62007-114">Disabilitare "Sincronizza impostazioni di Windows"</span><span class="sxs-lookup"><span data-stu-id="62007-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="62007-115">Comportamento della sincronizzazione delle impostazioni modificato per il supporto di Windows 10</span><span class="sxs-lookup"><span data-stu-id="62007-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="62007-116">UE-V 2,1 SP1 si aggira sulle impostazioni della barra delle applicazioni tra i dispositivi Windows 10.</span><span class="sxs-lookup"><span data-stu-id="62007-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="62007-117">Tuttavia, UE-V non sincronizza le impostazioni della barra delle applicazioni tra dispositivi e dispositivi Windows 10 in cui sono in uso sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="62007-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="62007-118">Inoltre, UE-V 2,1 SP1 non sincronizza le impostazioni tra la calcolatrice Microsoft in Windows 10 e la calcolatrice Microsoft nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="62007-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="62007-119">Supporto aggiunto per le stampanti di rete mobili</span><span class="sxs-lookup"><span data-stu-id="62007-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="62007-120">UE-V 2,1 SP1 consente alle stampanti di rete di spostarsi tra i dispositivi in modo che l'utente abbia accesso alle stampanti di rete quando si è connessi a qualsiasi dispositivo della rete.</span><span class="sxs-lookup"><span data-stu-id="62007-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="62007-121">Questo include il roaming della stampante impostata come predefinita.</span><span class="sxs-lookup"><span data-stu-id="62007-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="62007-122">La stampante in roaming in UE-V richiede uno di questi scenari:</span><span class="sxs-lookup"><span data-stu-id="62007-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="62007-123">Il server di stampa può scaricare il driver necessario quando si sposta in roaming su un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62007-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="62007-124">Il driver per la stampante di rete mobile è preinstallato in qualsiasi dispositivo che deve accedere alla stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="62007-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="62007-125">Il driver della stampante può essere ottenuto da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="62007-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="62007-126">**Nota**  La funzionalità di roaming della stampante UE-V **non** esegue la roaming delle impostazioni o delle preferenze della stampante, ad esempio la stampa fronte-retro.</span><span class="sxs-lookup"><span data-stu-id="62007-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="62007-127">Modello di posizione delle impostazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="62007-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="62007-128">UE-V 2,1 e 2,1 SP1 includono il modello di posizione delle impostazioni di Microsoft Office 2013 con il supporto per la firma di Outlook migliorato.</span><span class="sxs-lookup"><span data-stu-id="62007-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="62007-129">È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati.</span><span class="sxs-lookup"><span data-stu-id="62007-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="62007-130">I clienti non devono più scegliere le impostazioni predefinite della firma.</span><span class="sxs-lookup"><span data-stu-id="62007-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="62007-131">**Nota**  È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook.</span><span class="sxs-lookup"><span data-stu-id="62007-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="62007-132">Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.</span><span class="sxs-lookup"><span data-stu-id="62007-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="62007-133">In precedenza la versione UE-V includeva i modelli di posizione delle impostazioni di Microsoft Office 2010 distribuiti automaticamente e registrati con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="62007-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="62007-134">UE-V 2,1 funziona con Office 365 per determinare se le impostazioni di Office 2013 sono in roaming da Office 365.</span><span class="sxs-lookup"><span data-stu-id="62007-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="62007-135">Se le impostazioni sono in roaming con Office 365, non vengono spostate in roaming da UE-V.</span><span class="sxs-lookup"><span data-stu-id="62007-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="62007-136">[Panoramica delle impostazioni utente e roaming per Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) offre ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="62007-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="62007-137">Per abilitare la sincronizzazione delle impostazioni tramite UE-V 2,1, eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="62007-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="62007-138">Usare criteri di gruppo per disabilitare la sincronizzazione di Office 365</span><span class="sxs-lookup"><span data-stu-id="62007-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="62007-139">Non abilitare l'esperienza di sincronizzazione di Office 365 durante l'installazione di Office 2013</span><span class="sxs-lookup"><span data-stu-id="62007-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="62007-140">UE-V 2,1 include i [modelli di office 2013 e office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="62007-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="62007-141">Questa versione rimuove i modelli di Office 2007.</span><span class="sxs-lookup"><span data-stu-id="62007-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="62007-142">Gli utenti possono ancora usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e possono ancora ottenere i modelli dalla raccolta modelli di UE-V che si trova [qui](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="62007-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="62007-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62007-143">Related topics</span></span>


[<span data-ttu-id="62007-144">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="62007-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="62007-145">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="62007-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="62007-146">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="62007-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





