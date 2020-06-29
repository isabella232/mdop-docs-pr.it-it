---
title: Note sulla versione per DaRT 8.1
description: Note sulla versione per DaRT 8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824765"
---
# <span data-ttu-id="c6245-103">Note sulla versione per DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="c6245-103">Release Notes for DaRT 8.1</span></span>


**<span data-ttu-id="c6245-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="c6245-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="c6245-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 8,1.</span><span class="sxs-lookup"><span data-stu-id="c6245-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1.</span></span>

<span data-ttu-id="c6245-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente la diagnostica e il set di strumenti di ripristino 8,1.</span><span class="sxs-lookup"><span data-stu-id="c6245-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.1.</span></span> <span data-ttu-id="c6245-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c6245-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="c6245-108">Se c'è una differenza tra queste note sulla versione e altra documentazione DaRT, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="c6245-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="c6245-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="c6245-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="c6245-110">Problemi noti di DaRT 8,1</span><span class="sxs-lookup"><span data-stu-id="c6245-110">Known issues with DaRT 8.1</span></span>


### <span data-ttu-id="c6245-111">Disk Commander non è in grado di ripristinare un record di avvio master danneggiato in una partizione fisica in Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="c6245-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 8.1</span></span>

<span data-ttu-id="c6245-112">In Windows 8,1 l'opzione "Ripristina il record di avvio Master (MBR) o l'intestazione della tabella di partizione GUID (GPT)" in Disk Commander non è in grado di ripristinare un record di avvio master danneggiato in una partizione fisica e quindi non è in grado di avviare il computer client.</span><span class="sxs-lookup"><span data-stu-id="c6245-112">In Windows 8.1, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="c6245-113">**Soluzione alternativa:** Avviare **ripristino avvio**, fare clic su **risoluzione dei problemi**, fare clic su **Opzioni avanzate**e quindi su **Avvia ripristino**.</span><span class="sxs-lookup"><span data-stu-id="c6245-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="c6245-114">Più istanze di cancellazione disco destinate alla stessa unità causano tutte le istanze eccetto l'ultima per segnalare un errore</span><span class="sxs-lookup"><span data-stu-id="c6245-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="c6245-115">Se si avviano più istanze di wipe del disco e quindi si prova a pulire la stessa unità usando due istanze separate di cancellazione del disco, tutte le istanze eccetto l'ultima segnalano un errore di cancellazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="c6245-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="c6245-116">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="c6245-116">**Workaround:** None.</span></span>

### <span data-ttu-id="c6245-117">La cancellazione del disco potrebbe non cancellare tutti i dati sulle unità a stato solido che hanno memoria flash</span><span class="sxs-lookup"><span data-stu-id="c6245-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="c6245-118">Se si usa la cancellazione disco per cancellare i dati in un'unità SSD (Solid-State Drive) con memoria flash, non è possibile cancellare tutti i dati.</span><span class="sxs-lookup"><span data-stu-id="c6245-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="c6245-119">Questo problema si verifica perché il firmware SSD controlla la posizione fisica delle Scritture durante l'esecuzione del disco Wipe.</span><span class="sxs-lookup"><span data-stu-id="c6245-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="c6245-120">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="c6245-120">**Workaround:** None.</span></span>

### <span data-ttu-id="c6245-121">Ripristino configurazione di sistema non riesce quando si esegue la procedura guidata o l'editor del registro</span><span class="sxs-lookup"><span data-stu-id="c6245-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="c6245-122">Se si esegue la procedura guidata fabbro, l'editor del registro di sistema e, eventualmente, altri strumenti, ripristino configurazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="c6245-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="c6245-123">**Soluzione alternativa:** Chiudere e riavviare il dardo, quindi avviare Ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6245-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="c6245-124">L'analisi del file di sistema (SFC) non viene eseguita dopo l'avvio e la chiusura guidata di fabbro o Gestione computer</span><span class="sxs-lookup"><span data-stu-id="c6245-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="c6245-125">Se si avvia e quindi si chiude la procedura guidata o gli strumenti di gestione dei computer, il controllo file di sistema non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6245-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="c6245-126">**Soluzione alternativa:** Chiudere e riavviare il dardo, quindi avviare Controllo file di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6245-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="c6245-127">Il programma di installazione di DaRT non viene superato quando il kit di valutazione e distribuzione di Windows non è installato</span><span class="sxs-lookup"><span data-stu-id="c6245-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="c6245-128">Se si installa DaRT 8,1 usando la riga di comando per eseguire il programma di installazione di Windows (con estensione msi) e il kit di valutazione e distribuzione di Windows (WindowsADK) non è stato installato, l'installazione di DaRT dovrebbe avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c6245-128">If you install DaRT 8.1 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="c6245-129">Attualmente, il programma di installazione di DaRT 8,1 installa tutti i componenti tranne l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="c6245-129">Currently, the DaRT 8.1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="c6245-130">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="c6245-130">**Workaround:** None.</span></span>

### <span data-ttu-id="c6245-131">Windows Defender non può iniziare dopo la creazione guidata fabbro, l'editor del registro di sistema, l'analizzatore di crash e la gestione dei computer</span><span class="sxs-lookup"><span data-stu-id="c6245-131">Windows Defender cannot start after Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management are started</span></span>

<span data-ttu-id="c6245-132">Windows Defender non si avvia se è già stata avviata la procedura guidata, l'editor del registro di sistema, l'analizzatore di crash e la gestione dei computer.</span><span class="sxs-lookup"><span data-stu-id="c6245-132">Windows Defender does not start if you have already started Locksmith Wizard, Registry Editor, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="c6245-133">**Soluzione alternativa:** Chiudere e riavviare il dardo, quindi avviare Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="c6245-133">**Workaround:** Close and restart DaRT, and then start Windows Defender.</span></span>

### <span data-ttu-id="c6245-134">Windows Defender può essere lento per iniziare</span><span class="sxs-lookup"><span data-stu-id="c6245-134">Windows Defender may be slow to start</span></span>

<span data-ttu-id="c6245-135">Windows Defender a volte richiede alcuni minuti per iniziare.</span><span class="sxs-lookup"><span data-stu-id="c6245-135">Windows Defender sometimes takes a few minutes to start.</span></span> <span data-ttu-id="c6245-136">La barra di stato indica lo stato di caricamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c6245-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="c6245-137">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="c6245-137">**Workaround:** None.</span></span>

## <span data-ttu-id="c6245-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6245-138">Related topics</span></span>


[<span data-ttu-id="c6245-139">Informazioni su DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="c6245-139">About DaRT 8.1</span></span>](about-dart-81.md)

 

 





