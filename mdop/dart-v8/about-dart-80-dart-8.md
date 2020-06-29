---
title: Informazioni su DaRT 8.0
description: Informazioni su DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821285"
---
# <span data-ttu-id="208e3-103">Informazioni su DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="208e3-103">About DaRT 8.0</span></span>


<span data-ttu-id="208e3-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 consente di risolvere i problemi e ripristinare i computer basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="208e3-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="208e3-105">Sono inclusi i computer che non possono essere avviati.</span><span class="sxs-lookup"><span data-stu-id="208e3-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="208e3-106">DaRT 8,0 è un potente set di strumenti che estendono l'ambiente di ripristino di Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="208e3-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="208e3-107">Usando DaRT, puoi analizzare un problema per determinare la causa, ad esempio controllando il log eventi o il registro di sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="208e3-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="208e3-108">DaRT supporta il ripristino di dischi rigidi di base che contengono partizioni, ad esempio partizioni primarie e unità logiche, e supporta il ripristino dei volumi.</span><span class="sxs-lookup"><span data-stu-id="208e3-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="208e3-109">**Nota**  Dardo non supporta il ripristino dei dischi dinamici.</span><span class="sxs-lookup"><span data-stu-id="208e3-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="208e3-110">DaRT offre anche strumenti che ti aiutano a risolvere un problema non appena ne determini la causa.</span><span class="sxs-lookup"><span data-stu-id="208e3-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="208e3-111">Ad esempio, puoi usare gli strumenti di DaRT per disabilitare un driver di dispositivo difettoso, rimuovere gli hotfix, ripristinare i file eliminati e analizzare il computer per il malware anche quando non puoi o non devi avviare il sistema operativo Windows installato.</span><span class="sxs-lookup"><span data-stu-id="208e3-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="208e3-112">Il dardo consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 8, in genere in meno tempo rispetto alla riimmagine del computer.</span><span class="sxs-lookup"><span data-stu-id="208e3-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="208e3-113">La funzionalità in DaRT consente di creare un'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="208e3-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="208e3-114">L'immagine di ripristino avvia Windows Recovery Environment (Windows RE), da cui è possibile avviare la finestra del **set di strumenti di diagnostica e ripristino** e accedere agli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="208e3-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="208e3-115">Usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="208e3-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="208e3-116">Per impostazione predefinita, la procedura guidata crea un file di immagine ISO (International Organization for Standardizzation) e un file WIM (Windows Imaging Format) e consente di masterizzare l'immagine in un CD, un DVD o un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="208e3-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="208e3-117">È possibile distribuire l'immagine localmente nei computer dell'utente finale oppure distribuirla da una partizione di rete remota o da una partizione di ripristino nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="208e3-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="208e3-118">Novità di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="208e3-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="208e3-119">DaRT 8,0 consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 8, in genere in meno tempo rispetto alla riimmagine del computer.</span><span class="sxs-lookup"><span data-stu-id="208e3-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="208e3-120">Le nuove funzionalità di DaRT 8,0 sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="208e3-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="208e3-121">Creare immagini DaRT usando Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="208e3-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="208e3-122">DaRT 8,0 consente di creare immagini dardo usando Windows® 8 o Windows Server® 2012.</span><span class="sxs-lookup"><span data-stu-id="208e3-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="208e3-123">Per le versioni di Windows precedenti a Windows 8 e Windows Server 2012, i clienti dovrebbero continuare a usare le versioni precedenti di DaRT.</span><span class="sxs-lookup"><span data-stu-id="208e3-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="208e3-124">Generare immagini di bit di 32 e 64 da un computer</span><span class="sxs-lookup"><span data-stu-id="208e3-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="208e3-125">DaRT 8,0 consente di generare immagini sia a 32 che a 64 bit da un singolo computer in cui è in corso il comando DaRT, indipendentemente dal fatto che il computer sia un computer a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="208e3-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="208e3-126">In DaRT7 l'immagine che è stata creata deve essere la stessa, un po' saggia, come il computer in cui è stato eseguito il dardo.</span><span class="sxs-lookup"><span data-stu-id="208e3-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="208e3-127">Creare un'immagine che supporti i computer con un'interfaccia BIOS o UEFI</span><span class="sxs-lookup"><span data-stu-id="208e3-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="208e3-128">Il supporto di DaRT 8.0 sia per l'interfaccia UEFI (Unified Extensible Firmware Interface) che per le interfacce BIOS consente di creare una sola immagine che funziona con i computer che hanno un'interfaccia qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="208e3-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="208e3-129">Usare una tabella di partizione GUID (GPT) per il partizionamento</span><span class="sxs-lookup"><span data-stu-id="208e3-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="208e3-130">Gli strumenti di DaRT 8,0 supportano ora i dischi GPT di Windows 8, che includono un meccanismo più flessibile per partizionare i dischi rispetto allo schema di partizionamento MBR (master boot record) più vecchio.</span><span class="sxs-lookup"><span data-stu-id="208e3-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="208e3-131">Gli strumenti di DaRT 8,0 continuano a supportare il partizionamento MBR.</span><span class="sxs-lookup"><span data-stu-id="208e3-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="208e3-132">Installare Windows 8 e Windows Server 2012 nel disco rigido locale</span><span class="sxs-lookup"><span data-stu-id="208e3-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="208e3-133">Gli strumenti di DaRT 8,0 possono essere usati solo quando Windows 8 e Windows Server 2012 sono installati nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="208e3-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="208e3-134">Attualmente non è disponibile alcun supporto per Windows to go.</span><span class="sxs-lookup"><span data-stu-id="208e3-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="208e3-135">Note sulla versione di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="208e3-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="208e3-136">Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere le [Note sulla versione di DaRT 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="208e3-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="208e3-137">Come ottenere il dardo 8,0</span><span class="sxs-lookup"><span data-stu-id="208e3-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="208e3-138">Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="208e3-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="208e3-139">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="208e3-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="208e3-140">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="208e3-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="208e3-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="208e3-141">Related topics</span></span>


[<span data-ttu-id="208e3-142">Attività iniziali di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="208e3-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="208e3-143">Note sulla versione per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="208e3-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





