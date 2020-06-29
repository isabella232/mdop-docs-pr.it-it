---
title: Note sulla versione per DaRT 7.0
description: Note sulla versione per DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822765"
---
# <span data-ttu-id="44eb9-103">Note sulla versione per DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="44eb9-103">Release Notes for DaRT 7.0</span></span>


**<span data-ttu-id="44eb9-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="44eb9-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="44eb9-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="44eb9-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span>

## <span data-ttu-id="44eb9-106">Informazioni su Microsoft Diagnostics and Recovery Toolset 7,0</span><span class="sxs-lookup"><span data-stu-id="44eb9-106">About Microsoft Diagnostics and Recovery Toolset 7.0</span></span>


<span data-ttu-id="44eb9-107">Queste note sulla versione contengono informazioni necessarie per installare correttamente DaRT7 e contengono informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="44eb9-107">These release notes contain information that is required to successfully install DaRT7 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="44eb9-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni della piattaforma DaRT, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="44eb9-108">If there is a difference between these release notes and other DaRT platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="44eb9-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="44eb9-109">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="44eb9-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="44eb9-110">About the Product Documentation</span></span>


<span data-ttu-id="44eb9-111">La documentazione per Microsoft Diagnostics and Recovery Toolset (DaRT) 7 viene distribuita con il prodotto e nel sito Connect.</span><span class="sxs-lookup"><span data-stu-id="44eb9-111">Documentation for Microsoft Diagnostics and Recovery Toolset (DaRT)7 is distributed with the product and on the Connect site.</span></span>

<span data-ttu-id="44eb9-112">Per informazioni dettagliate su come usare gli strumenti in DaRT7, vedere il file della Guida disponibile nel menu **strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="44eb9-112">For detailed help about how to use the tools in DaRT7, see the Help file available on the **Diagnostics and Recovery Toolset** menu.</span></span>

## <span data-ttu-id="44eb9-113">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="44eb9-113">Providing feedback</span></span>


<span data-ttu-id="44eb9-114">Siamo interessati a ricevere commenti e suggerimenti su DaRT7.</span><span class="sxs-lookup"><span data-stu-id="44eb9-114">We are interested in your feedback on DaRT7.</span></span> <span data-ttu-id="44eb9-115">È possibile inviare il proprio feedback a dart7feedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="44eb9-115">You can send your feedback to dart7feedback@microsoft.com.</span></span> <span data-ttu-id="44eb9-116">Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future per questi strumenti per renderle più utili in futuro.</span><span class="sxs-lookup"><span data-stu-id="44eb9-116">This email address is not a support channel, but your feedback will help us to plan future changes for these tools to make them more useful to you in the future.</span></span>

## <span data-ttu-id="44eb9-117">Protezione da vulnerabilità e virus della sicurezza</span><span class="sxs-lookup"><span data-stu-id="44eb9-117">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="44eb9-118">Per proteggere le vulnerabilità e i virus della sicurezza, è consigliabile installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare.</span><span class="sxs-lookup"><span data-stu-id="44eb9-118">To help protect against security vulnerabilities and viruses, we recommend that you install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="44eb9-119">Per altre informazioni, vedere [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="44eb9-119">For more information, see [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="44eb9-120">Problemi noti di DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="44eb9-120">Known Issues with DaRT 7.0</span></span>


### <span data-ttu-id="44eb9-121">L'analisi SFC non può essere avviata se la spazzatrice di sistema autonoma è aperta</span><span class="sxs-lookup"><span data-stu-id="44eb9-121">SFC Scan cannot start if Standalone System Sweeper is open</span></span>

<span data-ttu-id="44eb9-122">Se lo strumento di sweep del sistema autonomo è in esecuzione, l'analisi SFC non può essere avviata o eseguita a causa di un conflitto di risorse tra i due strumenti.</span><span class="sxs-lookup"><span data-stu-id="44eb9-122">If the Standalone System Sweeper is running, SFC Scan cannot start or run because of a resource conflict between the two tools.</span></span>

<span data-ttu-id="44eb9-123">**Soluzione alternativa:** Chiudere la spazzatrice di sistema autonomo prima di provare ad aprire o eseguire lo strumento di analisi SFC.</span><span class="sxs-lookup"><span data-stu-id="44eb9-123">**Workaround:** Close the Standalone System Sweeper before you try to open or run the SFC Scan tool.</span></span>

### <span data-ttu-id="44eb9-124">I caratteri Unicode potrebbero non essere visualizzati nei nomi di file</span><span class="sxs-lookup"><span data-stu-id="44eb9-124">Unicode characters may not be displayed in file names</span></span>

<span data-ttu-id="44eb9-125">Se si elimina un file con caratteri Unicode nel nome del file e si prova a ripristinare il file usando lo strumento di ripristino file, il file non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="44eb9-125">If you delete a file that has Unicode characters in its file name and try to restore the file by using the File Restore tool, the file is not found.</span></span> <span data-ttu-id="44eb9-126">Questo problema si verifica solo quando si usano caratteri di una lingua diversa dalla lingua del DVD di Windows usato per creare l'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="44eb9-126">This only occurs when you use characters from a language other than the language of the Windows DVD that was used to create the recovery image.</span></span>

<span data-ttu-id="44eb9-127">**Soluzione alternativa:** Verificare che la lingua usata da DaRT corrisponda alla lingua usata dal sistema operativo da cui sta provando a ripristinare i file.</span><span class="sxs-lookup"><span data-stu-id="44eb9-127">**Workaround:** Make sure that the language that is used by DaRT matches the language that is used by the operating system from which it is trying to restore files.</span></span>

### <span data-ttu-id="44eb9-128">L'installazione della riga di comando DaRT potrebbe non riuscire automaticamente</span><span class="sxs-lookup"><span data-stu-id="44eb9-128">DaRT command-line installation may fail silently</span></span>

<span data-ttu-id="44eb9-129">L'installazione della riga di comando DaRT non riesce automaticamente se eseguita con l'opzione modalità non interattiva, a meno che non venga eseguita usando autorizzazioni di amministratore elevate.</span><span class="sxs-lookup"><span data-stu-id="44eb9-129">DaRT command-line installation fails silently if run with the quiet mode option unless it is run by using elevated administrator permissions.</span></span>

<span data-ttu-id="44eb9-130">**Soluzione alternativa:** Eseguire l'installazione della riga di comando usando le autorizzazioni di amministratore elevate.</span><span class="sxs-lookup"><span data-stu-id="44eb9-130">**Workaround:** Run the command-line installation by using elevated administrator permissions.</span></span> <span data-ttu-id="44eb9-131">L'installazione di DaRT supporta le tipiche opzioni di Windows Installer per l'installazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="44eb9-131">DaRT installation supports the typical Windows Installer options for command-line installation.</span></span> <span data-ttu-id="44eb9-132">Vedere [Opzioni della riga di comando](https://go.microsoft.com/fwlink/?LinkId=160689) per Windows Installer per altre informazioni sulle diverse opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="44eb9-132">Please see [Command-Line Options](https://go.microsoft.com/fwlink/?LinkId=160689) for Windows Installer for more information about the several available switches.</span></span>

### <span data-ttu-id="44eb9-133">La ricerca di file non può trasferire una cartella in un volume diverso</span><span class="sxs-lookup"><span data-stu-id="44eb9-133">File Search cannot move a folder to a different volume</span></span>

<span data-ttu-id="44eb9-134">Lo spostamento delle cartelle tra volumi non è supportato dall'applicazione di ricerca file.</span><span class="sxs-lookup"><span data-stu-id="44eb9-134">Moving folders between volumes is not supported by the File Search application.</span></span> <span data-ttu-id="44eb9-135">Se si prova a trasferire una cartella in un volume diverso nella ricerca file, viene restituito l'errore seguente: "si è verificato un errore durante la scrittura del \* &lt; nome &gt; \*file.</span><span class="sxs-lookup"><span data-stu-id="44eb9-135">If you try to move a folder to a different volume in File Search, the following error is returned: "An error occurred while writing the file *&lt;filename&gt;*.</span></span> <span data-ttu-id="44eb9-136">Verificare che l'unità disponga di spazio sufficiente e che il percorso di destinazione sia accessibile. "</span><span class="sxs-lookup"><span data-stu-id="44eb9-136">Make sure that the drive has sufficient space and the destination path is accessible."</span></span>

<span data-ttu-id="44eb9-137">**Soluzione alternativa:** Usare Esplora risorse per trasferire una cartella in un volume diverso.</span><span class="sxs-lookup"><span data-stu-id="44eb9-137">**Workaround:** Use the Explorer to move a folder to a different volume.</span></span>

### <span data-ttu-id="44eb9-138">Alcuni dati potrebbero non essere disponibili nei computer in cui vengono rimappate le lettere di unità</span><span class="sxs-lookup"><span data-stu-id="44eb9-138">Some data may not be available on computers where the drive letters are remapped</span></span>

<span data-ttu-id="44eb9-139">Questo problema può verificarsi in computer con attivazione BitLocker e multiboot.</span><span class="sxs-lookup"><span data-stu-id="44eb9-139">This problem can occur on BitLocker-enabled computers and multiboot computers.</span></span> <span data-ttu-id="44eb9-140">Questo problema si verifica perché alcune informazioni nel registro di sistema offline includono lettere di unità hardcoded e dardo usa lettere diverse per gli stessi volumi.</span><span class="sxs-lookup"><span data-stu-id="44eb9-140">This occurs because some information in the offline registry has hard-coded drive letters, and DaRT uses different letters for the same volumes.</span></span> <span data-ttu-id="44eb9-141">Gli effetti tipici includono non avere accesso a determinati account utente locali nell'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="44eb9-141">The typical effects include not having access to certain local user accounts in Registry Editor.</span></span> <span data-ttu-id="44eb9-142">Inoltre, alcuni strumenti potrebbero non essere in grado di ottenere proprietà che si basano sulla risoluzione dei percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="44eb9-142">Additionally, some tools may be unable to obtain properties that rely on resolving file paths.</span></span>

<span data-ttu-id="44eb9-143">**Soluzione alternativa:** Usa l'opzione per riassociare le lettere dell'unità all'avvio di DaRT.</span><span class="sxs-lookup"><span data-stu-id="44eb9-143">**Workaround:** Use the option to remap the drive letters as DaRT starts.</span></span> <span data-ttu-id="44eb9-144">In genere le lettere di unità tipiche vengono allineate a quelle previste.</span><span class="sxs-lookup"><span data-stu-id="44eb9-144">This usually aligns the typical drive letters to what is expected.</span></span>

### <span data-ttu-id="44eb9-145">La disinstallazione dell'hotfix potrebbe non disinstallare alcuni aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="44eb9-145">Hotfix Uninstall might not uninstall certain updates</span></span>

<span data-ttu-id="44eb9-146">Alcuni aggiornamenti e Service Pack non possono essere disinstallati perché contrassegnati come non installabili o perché devono essere disinstallati in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44eb9-146">Some updates and service packs cannot be uninstalled because they are marked as un-installable or because they need to be uninstalled from within Windows 7.</span></span> <span data-ttu-id="44eb9-147">In queste istanze, lo strumento di disinstallazione dell'hotfix può indicare che questi aggiornamenti sono stati disinstallati anche se non sono stati.</span><span class="sxs-lookup"><span data-stu-id="44eb9-147">In these instances, the Hotfix Uninstall tool may indicate that these updates have been uninstalled even though they have not been.</span></span>

<span data-ttu-id="44eb9-148">**Soluzione alternativa:** Disinstallare questi aggiornamenti problematici da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44eb9-148">**Workaround:** Uninstall these problematic updates from Windows 7.</span></span>

### <span data-ttu-id="44eb9-149">Cancellazione disco: non è possibile eliminare i dischi con volumi con spanning, volumi a strisce o volumi speculari</span><span class="sxs-lookup"><span data-stu-id="44eb9-149">Disk Wipe: Disks with spanned volumes, striped volumes, or mirrored volumes cannot be deleted</span></span>

<span data-ttu-id="44eb9-150">La cancellazione disco non supporta l'eliminazione di dischi con spanning, mirroring o striping in uno o più volumi.</span><span class="sxs-lookup"><span data-stu-id="44eb9-150">Disk Wipe does not support deleting disks that are spanned, mirrored, or striped across one or more volumes.</span></span>

<span data-ttu-id="44eb9-151">**Soluzione alternativa:** Selezionare ed eliminare ogni disco nel volume separatamente.</span><span class="sxs-lookup"><span data-stu-id="44eb9-151">**Workaround:** Select and delete each disk in the volume separately.</span></span>

## <span data-ttu-id="44eb9-152">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="44eb9-152">Release Notes Copyright Information</span></span>


<span data-ttu-id="44eb9-153">Questo documento viene fornito "così com'è".</span><span class="sxs-lookup"><span data-stu-id="44eb9-153">This document is provided “as-is”.</span></span> <span data-ttu-id="44eb9-154">Le informazioni e le visualizzazioni espresse in questo documento, incluso l'URL e altri riferimenti al sito Web Internet, possono cambiare senza preavviso.</span><span class="sxs-lookup"><span data-stu-id="44eb9-154">Information and views expressed in this document, including URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="44eb9-155">Si rischia di usarlo.</span><span class="sxs-lookup"><span data-stu-id="44eb9-155">You bear the risk of using it.</span></span>

<span data-ttu-id="44eb9-156">Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi.</span><span class="sxs-lookup"><span data-stu-id="44eb9-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span><span data-ttu-id="44eb9-157">Nessuna associazione o connessione reale è destinata o deve essere dedotta.</span><span class="sxs-lookup"><span data-stu-id="44eb9-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="44eb9-158">Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44eb9-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="44eb9-159">Questo documento è riservato e proprietario di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44eb9-159">This document is confidential and proprietary to Microsoft.</span></span> <span data-ttu-id="44eb9-160">Viene divulgato e può essere usato solo in base a un contratto di segretezza.</span><span class="sxs-lookup"><span data-stu-id="44eb9-160">It is disclosed and can be used only pursuant to a nondisclosure agreement.</span></span>



<span data-ttu-id="44eb9-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="44eb9-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="44eb9-162">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="44eb9-162">All other trademarks are property of their respective owners.</span></span>

## <span data-ttu-id="44eb9-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44eb9-163">Related topics</span></span>


[<span data-ttu-id="44eb9-164">Informazioni su DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="44eb9-164">About DaRT 7.0</span></span>](about-dart-70-new-ia.md)

 

 





