---
title: Panoramica degli strumenti di DaRT 8.0
description: Panoramica degli strumenti di DaRT 8.0
author: dansimp
ms.assetid: 1766c82e-c099-47d4-b186-4689b026a7e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: a058f6018888f446782aa8f3a18ee89570840c2a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824616"
---
# <span data-ttu-id="61603-103">Panoramica degli strumenti di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="61603-103">Overview of the Tools in DaRT 8.0</span></span>


<span data-ttu-id="61603-104">Dalla finestra del **set di strumenti di diagnostica e ripristino** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 è possibile avviare uno dei singoli strumenti inclusi quando si crea l'immagine di ripristino di Dart 8,0.</span><span class="sxs-lookup"><span data-stu-id="61603-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you can start any of the individual tools that you include when you create the DaRT 8.0 recovery image.</span></span> <span data-ttu-id="61603-105">Per informazioni su come accedere alla finestra del **set di strumenti di diagnostica e ripristino** , vedere [come recuperare i computer locali usando l'immagine di ripristino DaRT](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="61603-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="61603-106">Se è disponibile, è possibile usare la **creazione guidata soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per selezionare lo strumento più adatto per risolvere il problema specifico, in base a una breve intervista fornita dalla procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="61603-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="61603-107">Esplorazione degli strumenti DaRT</span><span class="sxs-lookup"><span data-stu-id="61603-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="61603-108">Segue una descrizione degli strumenti di 8,0 di DaRT.</span><span class="sxs-lookup"><span data-stu-id="61603-108">A description of the DaRT 8.0 tools follows.</span></span>

### <span data-ttu-id="61603-109">Gestione computer</span><span class="sxs-lookup"><span data-stu-id="61603-109">Computer Management</span></span>

<span data-ttu-id="61603-110">**Gestione computer** è una raccolta di strumenti di amministrazione di Windows che consentono di risolvere i problemi di un computer.</span><span class="sxs-lookup"><span data-stu-id="61603-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="61603-111">È possibile usare gli strumenti di gestione dei computer in DaRT per visualizzare le informazioni di sistema e i registri eventi, gestire i dischi, eseguire l'esecuzione di elenchi **automatizzati** e gestire servizi e driver.</span><span class="sxs-lookup"><span data-stu-id="61603-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="61603-112">La console di **Gestione computer** è personalizzata per facilitare la diagnosi e il ripristino di problemi che potrebbero impedire l'avvio del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="61603-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="61603-113">**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61603-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="61603-114">Analizzatore crash</span><span class="sxs-lookup"><span data-stu-id="61603-114">Crash Analyzer</span></span>

<span data-ttu-id="61603-115">Usare la **procedura guidata Analizzatore crash** per determinare rapidamente la causa di un errore del computer analizzando il file di dump della memoria nel sistema operativo Windows che si sta ripristinando.</span><span class="sxs-lookup"><span data-stu-id="61603-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="61603-116">**Analizzatore crash** esamina il file di dump della memoria per il driver che ha causato il failover di un computer.</span><span class="sxs-lookup"><span data-stu-id="61603-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="61603-117">Puoi quindi disabilitare il driver di dispositivo problema usando il nodo **Servizi e driver** nello strumento **Gestione computer** .</span><span class="sxs-lookup"><span data-stu-id="61603-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="61603-118">La **procedura guidata Analizzatore crash** richiede gli strumenti di debug per Windows e i file di simboli per il sistema operativo da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="61603-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="61603-119">Puoi includere entrambi i requisiti quando crei l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="61603-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="61603-120">Se non sono inclusi nell'immagine di ripristino e non è possibile accedervi nel computer in cui si sta effettuando il ripristino, è sufficiente copiare il file di dump della memoria in un altro computer e usare la versione autonoma di **Crash Analyzer** per diagnosticare il problema.</span><span class="sxs-lookup"><span data-stu-id="61603-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="61603-121">L' **analizzatore di crash** in uso è una buona idea anche se si prevede di rieseguire l'immagine del computer.</span><span class="sxs-lookup"><span data-stu-id="61603-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="61603-122">L'immagine potrebbe avere un driver difettoso che causa problemi nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="61603-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="61603-123">Eseguendo **analizzatore crash**è possibile identificare i driver dei problemi e migliorare la stabilità delle immagini.</span><span class="sxs-lookup"><span data-stu-id="61603-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="61603-124">Per altre informazioni su **Crash Analyzer**, vedere [diagnostica degli errori di sistema con Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="61603-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span></span>

### <span data-ttu-id="61603-125">Defender</span><span class="sxs-lookup"><span data-stu-id="61603-125">Defender</span></span>

<span data-ttu-id="61603-126">**Importante**  Gli ambienti con il Defender dardo distribuito dovrebbero invece usare l'immagine di protezione offline di Microsoft Defender (WDO) per il rilevamento di malware.</span><span class="sxs-lookup"><span data-stu-id="61603-126">**Important** Environments with the DaRT Defender deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="61603-127">A causa del modo in cui lo strumento Defender si integra in DaRT, tutte le distribuzioni di versioni di DaRT supportate non possono applicare questi aggiornamenti anti-malware alle loro immagini DaRT.</span><span class="sxs-lookup"><span data-stu-id="61603-127">Because of how the Defender tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span> <span data-ttu-id="61603-128">Per altre informazioni, vedere [Microsoft Diagnostics and Recovery Toolset (DART) gli utenti devono usare Microsoft Defender offline (WDO) per il rilevamento di malware->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span><span class="sxs-lookup"><span data-stu-id="61603-128">For more information, see  [Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span></span>

 

<span data-ttu-id="61603-129">Il **difensore** può aiutare a rilevare il malware e il software indesiderato e avverte i rischi per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="61603-129">**Defender** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="61603-130">Puoi usare questo strumento per analizzare un computer e rimuovere malware anche quando il sistema operativo Windows installato non è in uso.</span><span class="sxs-lookup"><span data-stu-id="61603-130">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="61603-131">Quando **Defender** rileva un software dannoso o indesiderato, viene chiesto di rimuovere, mettere in quarantena o consentire ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="61603-131">When **Defender** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="61603-132">Il malware che usa i rootkit può mascherarsi dal sistema operativo in uso.</span><span class="sxs-lookup"><span data-stu-id="61603-132">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="61603-133">Se un virus o uno spyware abilitato per i rootkit è in un computer, la maggior parte degli strumenti di analisi e rimozione in tempo reale non può più vederla o rimuoverla.</span><span class="sxs-lookup"><span data-stu-id="61603-133">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="61603-134">Poiché si avvia il computer problema in dardo e il sistema operativo installato è offline, è possibile rilevare il rootkit senza che sia in grado di mascherarsi.</span><span class="sxs-lookup"><span data-stu-id="61603-134">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="61603-135">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="61603-135">Disk Commander</span></span>

<span data-ttu-id="61603-136">**Disk Commander** consente di recuperare e ripristinare partizioni o volumi di dischi usando uno dei processi di ripristino seguenti:</span><span class="sxs-lookup"><span data-stu-id="61603-136">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="61603-137">Ripristinare il record di avvio Master (MBR)</span><span class="sxs-lookup"><span data-stu-id="61603-137">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="61603-138">Recuperare uno o più volumi persi</span><span class="sxs-lookup"><span data-stu-id="61603-138">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="61603-139">Ripristinare le tabelle delle partizioni da **Disk Commander** backup</span><span class="sxs-lookup"><span data-stu-id="61603-139">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="61603-140">Salvare le tabelle delle partizioni in **Disk Commander** backup</span><span class="sxs-lookup"><span data-stu-id="61603-140">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="61603-141">**Avviso**  È consigliabile eseguire il backup di un disco prima di usare **Disk Commander** per ripristinarlo.</span><span class="sxs-lookup"><span data-stu-id="61603-141">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="61603-142">Usando **Disk Commander**, puoi potenzialmente danneggiare i volumi e renderli inaccessibili.</span><span class="sxs-lookup"><span data-stu-id="61603-142">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="61603-143">Inoltre, le modifiche apportate a un volume possono influire su altri volumi perché i volumi in un disco condividono una tabella di partizioni.</span><span class="sxs-lookup"><span data-stu-id="61603-143">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="61603-144">**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61603-144">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="61603-145">Cancellazione disco</span><span class="sxs-lookup"><span data-stu-id="61603-145">Disk Wipe</span></span>

<span data-ttu-id="61603-146">È possibile usare il **wipe del disco** per eliminare tutti i dati da un disco o da un volume, anche i dati rimasti dopo la riformattazione di un'unità disco rigido.</span><span class="sxs-lookup"><span data-stu-id="61603-146">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="61603-147">La **cancellazione del disco** consente di selezionare una sovrascrittura a passaggio singolo o una sovrascrittura a quattro passaggi, che soddisfa gli attuali standard del dipartimento della difesa degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="61603-147">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="61603-148">**Avviso**  Dopo aver asciugato un disco o un volume, non è possibile recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="61603-148">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="61603-149">Verificare le dimensioni e l'etichetta di un volume prima di cancellarlo.</span><span class="sxs-lookup"><span data-stu-id="61603-149">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="61603-150">Explorer</span><span class="sxs-lookup"><span data-stu-id="61603-150">Explorer</span></span>

<span data-ttu-id="61603-151">Lo strumento **Esplora risorse** consente di esplorare il file System e le condivisioni di rete del computer in modo da poter rimuovere i dati importanti archiviati dall'utente nell'unità locale prima di provare a ripristinare o riutilizzare il computer.</span><span class="sxs-lookup"><span data-stu-id="61603-151">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="61603-152">Poiché è possibile eseguire il mapping delle lettere delle unità alle condivisioni di rete, è possibile copiare e trasferire facilmente i file dal computer alla rete per la sicurezza o dalla rete al computer per ripristinarli.</span><span class="sxs-lookup"><span data-stu-id="61603-152">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="61603-153">Ripristino file</span><span class="sxs-lookup"><span data-stu-id="61603-153">File Restore</span></span>

<span data-ttu-id="61603-154">Il **ripristino dei file** consente di provare a ripristinare i file che sono stati eliminati accidentalmente o che erano troppo grandi per essere inseriti nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="61603-154">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="61603-155">Il **ripristino dei file** non è limitato ai normali volumi di disco, ma può trovare e ripristinare i file in volumi persi o in volumi crittografati da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="61603-155">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="61603-156">**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61603-156">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="61603-157">Ricerca di file</span><span class="sxs-lookup"><span data-stu-id="61603-157">File Search</span></span>

<span data-ttu-id="61603-158">Prima di ricreare un computer, è importante recuperare i file dal disco rigido locale, in particolare quando l'utente potrebbe non avere eseguito il backup o archiviare i file in un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="61603-158">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="61603-159">Lo strumento di **ricerca** apre una finestra di **ricerca file** che può essere usata per trovare i documenti quando non si conosce il percorso del file o per cercare tipi generali di file in tutti i dischi rigidi locali.</span><span class="sxs-lookup"><span data-stu-id="61603-159">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="61603-160">È possibile cercare modelli di nomi di file specifici in percorsi specifici.</span><span class="sxs-lookup"><span data-stu-id="61603-160">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="61603-161">Puoi anche limitare i risultati a un intervallo di date o a un intervallo di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="61603-161">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="61603-162">Disinstallazione hotfix</span><span class="sxs-lookup"><span data-stu-id="61603-162">Hotfix Uninstall</span></span>

<span data-ttu-id="61603-163">La **procedura guidata per la disinstallazione dell'hotfix** consente di rimuovere gli hotfix o i Service Pack dal sistema operativo Windows nel computer che si sta riparando.</span><span class="sxs-lookup"><span data-stu-id="61603-163">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="61603-164">Usare questo strumento quando si sospetta che sia previsto un hotfix o un Service Pack per impedire l'avvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61603-164">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="61603-165">Ti consigliamo di disinstallare solo un hotfix alla volta, anche se lo strumento ti consente di disinstallare più di uno.</span><span class="sxs-lookup"><span data-stu-id="61603-165">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="61603-166">**Importante**  Le applicazioni installate o aggiornate dopo l'installazione di un hotfix potrebbero non funzionare correttamente dopo la disinstallazione di un hotfix.</span><span class="sxs-lookup"><span data-stu-id="61603-166">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="61603-167">Fabbro</span><span class="sxs-lookup"><span data-stu-id="61603-167">Locksmith</span></span>

<span data-ttu-id="61603-168">La **procedura guidata fabbro** consente di impostare o modificare la password per qualsiasi account locale nel sistema operativo Windows che si sta analizzando o ripristinando.</span><span class="sxs-lookup"><span data-stu-id="61603-168">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="61603-169">Non è necessario conoscere la password corrente.</span><span class="sxs-lookup"><span data-stu-id="61603-169">You do not have to know the current password.</span></span> <span data-ttu-id="61603-170">La password impostata deve tuttavia essere conforme ai requisiti definiti da un oggetto Criteri di gruppo locale.</span><span class="sxs-lookup"><span data-stu-id="61603-170">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="61603-171">Include la lunghezza e la complessità della password.</span><span class="sxs-lookup"><span data-stu-id="61603-171">This includes password length and complexity.</span></span>

<span data-ttu-id="61603-172">È possibile usare **fabbro** quando la password di un account locale, ad esempio l'account di amministratore locale, non è nota.</span><span class="sxs-lookup"><span data-stu-id="61603-172">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="61603-173">Non è possibile usare **fabbro** per impostare le password per gli account di dominio.</span><span class="sxs-lookup"><span data-stu-id="61603-173">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="61603-174">Editor del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="61603-174">Registry Editor</span></span>

<span data-ttu-id="61603-175">È possibile usare l' **Editor del registro** di sistema per accedere e modificare il registro di sistemi operativo Windows che si sta analizzando o riparando.</span><span class="sxs-lookup"><span data-stu-id="61603-175">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="61603-176">Ciò include l'aggiunta, la rimozione e la modifica di chiavi e valori e l'importazione di file del registro di sistema (con estensione reg).</span><span class="sxs-lookup"><span data-stu-id="61603-176">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="61603-177">**Avviso**  Se si modifica il registro di sistema in modo non corretto utilizzando l' **Editor del registro di sistema**, si verificano problemi gravi.</span><span class="sxs-lookup"><span data-stu-id="61603-177">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="61603-178">Questi problemi potrebbero richiedere di reinstallare il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61603-178">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="61603-179">Prima di apportare modifiche al registro di sistema, è consigliabile eseguire il backup di tutti i dati valutati nel computer.</span><span class="sxs-lookup"><span data-stu-id="61603-179">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="61603-180">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="61603-180">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="61603-181">Analisi SFC</span><span class="sxs-lookup"><span data-stu-id="61603-181">SFC Scan</span></span>

<span data-ttu-id="61603-182">Lo strumento di **Analisi SFC** avvia la **procedura guidata di ripristino dei file di sistema** e consente di ripristinare i file di sistema che impediscono l'avvio del sistema operativo Windows installato.</span><span class="sxs-lookup"><span data-stu-id="61603-182">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="61603-183">La **procedura guidata di ripristino dei file di sistema** può ripristinare automaticamente i file di sistema danneggiati o mancanti oppure può richiedere l'assistenza prima di eseguire eventuali riparazioni.</span><span class="sxs-lookup"><span data-stu-id="61603-183">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="61603-184">Creazione guidata soluzione</span><span class="sxs-lookup"><span data-stu-id="61603-184">Solution Wizard</span></span>

<span data-ttu-id="61603-185">La **creazione guidata soluzione** presenta una serie di domande e quindi consiglia lo strumento migliore per la situazione, in base alle proprie risposte.</span><span class="sxs-lookup"><span data-stu-id="61603-185">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="61603-186">Questa procedura guidata consente di determinare lo strumento da usare quando non si ha familiarità con gli strumenti di DaRT.</span><span class="sxs-lookup"><span data-stu-id="61603-186">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="61603-187">Configurazione TCP/IP</span><span class="sxs-lookup"><span data-stu-id="61603-187">TCP/IP Config</span></span>

<span data-ttu-id="61603-188">Quando si avvia un computer con problemi in DaRT, è impostato per ottenere automaticamente la configurazione TCP/IP (indirizzo IP e server DNS) dal protocollo DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="61603-188">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="61603-189">Se DHCP non è disponibile, è possibile configurare manualmente TCP/IP usando lo strumento di **configurazione TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="61603-189">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="61603-190">Prima di tutto selezionare una scheda di rete e quindi configurare l'indirizzo IP e il server DNS per tale adapter.</span><span class="sxs-lookup"><span data-stu-id="61603-190">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="61603-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61603-191">Related topics</span></span>


[<span data-ttu-id="61603-192">Attività iniziali di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="61603-192">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

 

 





