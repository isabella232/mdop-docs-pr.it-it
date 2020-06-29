---
title: Informazioni su DaRT 7.0
description: Informazioni su DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823275"
---
# <span data-ttu-id="d54f9-103">Informazioni su DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d54f9-103">About DaRT 7.0</span></span>


<span data-ttu-id="d54f9-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 ti aiuta a risolvere i problemi e a ripristinare i desktop basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="d54f9-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="d54f9-105">Sono inclusi i desktop che non possono essere avviati.</span><span class="sxs-lookup"><span data-stu-id="d54f9-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="d54f9-106">DaRT è un potente set di strumenti che estendono l'ambiente di ripristino di Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="d54f9-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="d54f9-107">Usando DaRT, puoi analizzare un problema per determinare la causa, ad esempio controllando il log eventi o il registro di sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="d54f9-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="d54f9-108">DaRT offre anche strumenti che ti aiutano a risolvere un problema non appena ne determini la causa.</span><span class="sxs-lookup"><span data-stu-id="d54f9-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="d54f9-109">Ad esempio, puoi usare gli strumenti di DaRT per disabilitare un driver di dispositivo difettoso, rimuovere gli hotfix, ripristinare i file eliminati e analizzare il computer per il malware anche quando non puoi o non devi avviare il sistema operativo Windows installato.</span><span class="sxs-lookup"><span data-stu-id="d54f9-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="d54f9-110">Il dardo consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 7, in genere in meno tempo rispetto alla riimmagine del computer.</span><span class="sxs-lookup"><span data-stu-id="d54f9-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="d54f9-111">Informazioni sull'immagine di ripristino di DaRT 7</span><span class="sxs-lookup"><span data-stu-id="d54f9-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="d54f9-112">La funzionalità in DaRT consente di creare un'immagine di ripristino basata su WinRE combinata con un set di strumenti forniti da DaRT.</span><span class="sxs-lookup"><span data-stu-id="d54f9-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="d54f9-113">L'immagine di recupero dardo sfrutta WinRE, da cui è possibile accedere alla finestra del **set di strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="d54f9-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="d54f9-114">Usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="d54f9-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="d54f9-115">Per impostazione predefinita, la procedura guidata crea un file di immagine ISO (International Organization for Standardizzation) sul desktop denominato DaRT70. ISO, anche se è possibile specificare un percorso e un nome file diversi.</span><span class="sxs-lookup"><span data-stu-id="d54f9-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="d54f9-116">La procedura guidata consente inoltre di masterizzare l'immagine in un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="d54f9-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="d54f9-117">Dopo aver completato la procedura guidata, è possibile salvare l'immagine di ripristino in un'unità flash USB o salvarla in un formato che può essere usato per creare una partizione remota o una partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d54f9-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="d54f9-118">Quando devi usare DaRT per l'avvio di un computer per utenti finali che non si avvia, puoi seguire le istruzioni su [come recuperare i computer locali usando l'immagine di ripristino DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d54f9-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="d54f9-119">Per informazioni dettagliate sugli strumenti in DaRT, Vedi [Panoramica degli strumenti di dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="d54f9-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="d54f9-120">Novità di DaRT 7</span><span class="sxs-lookup"><span data-stu-id="d54f9-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="d54f9-121">DaRT7 continua a supportare tutti gli scenari inclusi nelle versioni precedenti e aggiunge una nuova funzionalità di connessione remota oltre a tre nuove opzioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d54f9-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="d54f9-122">Creazione di immagini DaRT 7</span><span class="sxs-lookup"><span data-stu-id="d54f9-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="d54f9-123">La procedura guidata che si usa per creare immagini ISO DaRT è ora chiamata **immagine di recupero Dart** e ora supporta un'opzione per abilitare o disabilitare la nuova funzionalità di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="d54f9-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="d54f9-124">Connessione remota consente a un agente dell'helpdesk di eseguire gli strumenti DaRT da una posizione remota.</span><span class="sxs-lookup"><span data-stu-id="d54f9-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="d54f9-125">Nelle versioni precedenti l'agente dell'helpdesk doveva essere fisicamente presente nel computer dell'utente finale per eseguire gli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="d54f9-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="d54f9-126">La procedura guidata consente inoltre di personalizzare il messaggio di benvenuto per la funzionalità di connessione remota (il messaggio viene visualizzato quando gli utenti finali eseguono lo strumento di connessione remota).</span><span class="sxs-lookup"><span data-stu-id="d54f9-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="d54f9-127">Gli amministratori IT possono anche configurare il numero di porta da usare per la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="d54f9-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="d54f9-128">Per altre informazioni sulla creazione **guidata immagine di ripristino delle freccette** o sulla connessione remota, vedere [creare l'immagine di ripristino di DaRT 7,0](creating-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d54f9-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="d54f9-129">Distribuzione ISO di DaRT 7</span><span class="sxs-lookup"><span data-stu-id="d54f9-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="d54f9-130">Oltre alla masterizzazione su CD o DVD, DaRT7 aggiunge tre nuove opzioni quando si distribuisce la ISO che contiene l'immagine di ripristino delle freccette:</span><span class="sxs-lookup"><span data-stu-id="d54f9-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="d54f9-131">Distribuzione di unità flash USB</span><span class="sxs-lookup"><span data-stu-id="d54f9-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="d54f9-132">Distribuzione di partizioni remote</span><span class="sxs-lookup"><span data-stu-id="d54f9-132">Remote partition deployment</span></span>

-   <span data-ttu-id="d54f9-133">Distribuzione della partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="d54f9-133">Recovery partition deployment</span></span>

<span data-ttu-id="d54f9-134">L'opzione di distribuzione dell'unità flash USB consente a una società di usare il dardo in computer in cui non sono disponibili unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="d54f9-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="d54f9-135">Le opzioni di recupero e partizione remota consentono agli utenti finali di accedere facilmente all'immagine DaRT e di abilitare la funzionalità di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="d54f9-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="d54f9-136">Per altre informazioni su come distribuire le immagini di ripristino delle freccette, vedere [distribuzione dell'immagine di ripristino di dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d54f9-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="d54f9-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d54f9-137">Related topics</span></span>


[<span data-ttu-id="d54f9-138">Attività iniziali di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d54f9-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="d54f9-139">Note sulla versione per DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d54f9-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





