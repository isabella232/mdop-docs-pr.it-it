---
title: Note sulla versione di App-V 4.6 SP1
description: Note sulla versione di App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819836"
---
# <span data-ttu-id="76ac3-103">Note sulla versione di App-V 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="76ac3-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="76ac3-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="76ac3-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="76ac3-105">**Importante**  Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione di Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="76ac3-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="76ac3-106">Queste note sulla versione contengono informazioni che consentono di installare correttamente Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="76ac3-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="76ac3-107">Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="76ac3-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="76ac3-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V, la modifica più recente deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="76ac3-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="76ac3-109">Protezione da vulnerabilità e virus della sicurezza</span><span class="sxs-lookup"><span data-stu-id="76ac3-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="76ac3-110">Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare.</span><span class="sxs-lookup"><span data-stu-id="76ac3-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="76ac3-111">Per altre informazioni, vedere il [sito Web Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="76ac3-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="76ac3-112">Problemi noti di Application Virtualization 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="76ac3-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="76ac3-113">Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="76ac3-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="76ac3-114">Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="76ac3-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="76ac3-115">Quando è possibile, questi problemi verranno risolti in versioni successive.</span><span class="sxs-lookup"><span data-stu-id="76ac3-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="76ac3-116">Il percorso di SPRT viene perso se non termina con Slash (/)</span><span class="sxs-lookup"><span data-stu-id="76ac3-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="76ac3-117">Quando il percorso in un HREF in un modello di progetto non termina con una barra ( **/** ), l'oggetto href generato non include il percorso.</span><span class="sxs-lookup"><span data-stu-id="76ac3-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="76ac3-118">Questo problema si verifica quando l'utente modifica manualmente il file **sprt** .</span><span class="sxs-lookup"><span data-stu-id="76ac3-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="76ac3-119">Se usi il sequencer, la barra () viene sempre aggiunta **/** dopo il percorso.</span><span class="sxs-lookup"><span data-stu-id="76ac3-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="76ac3-120">SOLUZIONE verificare che l'HREF abbia una barra di avanzamento finale ( **/** ).</span><span class="sxs-lookup"><span data-stu-id="76ac3-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="76ac3-121">Il nome della cartella utente non corrisponde al nome del pacchetto</span><span class="sxs-lookup"><span data-stu-id="76ac3-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="76ac3-122">Le cartelle che contengono file utente e Global. pkg non includono più il nome del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="76ac3-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="76ac3-123">In precedenza, il client App-V usato per usare la cartella radice del pacchetto 8,3 nome breve come parte del nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="76ac3-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="76ac3-124">Questo consente di identificarlo facilmente.</span><span class="sxs-lookup"><span data-stu-id="76ac3-124">This lets you easily identify it.</span></span> <span data-ttu-id="76ac3-125">Quando usi il sequencer App-V 4,6 SP1, la cartella radice del pacchetto 8,3 nomi brevi è ora stringhe casuali.</span><span class="sxs-lookup"><span data-stu-id="76ac3-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="76ac3-126">In questo modo è difficile identificare le cartelle che contengono i file con **estensione pkg** del pacchetto nel computer in cui è in uso App-V client.</span><span class="sxs-lookup"><span data-stu-id="76ac3-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="76ac3-127">SOLUZIONE usare uno dei metodi seguenti per identificare più facilmente queste cartelle di pacchetti:</span><span class="sxs-lookup"><span data-stu-id="76ac3-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="76ac3-128">Quando si crea il pacchetto usando il sequencer, specificare il nome di una cartella che segue la convenzione di denominazione di 8,3 per la cartella dell'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="76ac3-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="76ac3-129">Questo nome verrà quindi usato come parte del nome della cartella utente, come nel caso di App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="76ac3-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="76ac3-130">Il file con estensione SPRJ ora contiene un tag che visualizza la stringa usata come inizio del nome della cartella utente.</span><span class="sxs-lookup"><span data-stu-id="76ac3-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="76ac3-131">Puoi usare l'elemento **ShortName** dell'elemento **PACKAGEROOTFOLDER** per determinare il nome.</span><span class="sxs-lookup"><span data-stu-id="76ac3-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="76ac3-132">In uso App-V 4,6 SP1 nei computer con più di 64 processori</span><span class="sxs-lookup"><span data-stu-id="76ac3-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="76ac3-133">Quando si esegue App-V 4,6 SP1 nei computer in cui sono installati più processori 64, il client App-V non riesce.</span><span class="sxs-lookup"><span data-stu-id="76ac3-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="76ac3-134">SOLUZIONE alternativa nessuna.</span><span class="sxs-lookup"><span data-stu-id="76ac3-134">WORKAROUND None.</span></span> <span data-ttu-id="76ac3-135">Questa configurazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76ac3-135">This configuration is not supported.</span></span> <span data-ttu-id="76ac3-136">È necessario eseguire App-V 4,6 SP1on computer con meno di 64 processori.</span><span class="sxs-lookup"><span data-stu-id="76ac3-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="76ac3-137">L'aggiornamento di Application Virtualization 4,6 SP1 non è disponibile in tutte le impostazioni locali che usano Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="76ac3-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="76ac3-138">Quando si usa Microsoft Update, l'aggiornamento per App-V 4,6 SP1 non è disponibile per le impostazioni locali della lingua seguenti:</span><span class="sxs-lookup"><span data-stu-id="76ac3-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="76ac3-139">Kazaco</span><span class="sxs-lookup"><span data-stu-id="76ac3-139">Kazakh</span></span>

-   <span data-ttu-id="76ac3-140">Hindi</span><span class="sxs-lookup"><span data-stu-id="76ac3-140">Hindi</span></span>

-   <span data-ttu-id="76ac3-141">Serbo-cirillico</span><span class="sxs-lookup"><span data-stu-id="76ac3-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="76ac3-142">SOLUZIONE alternativa se si usa Microsoft Windows Server Update Services (WSUS), usare la versione in lingua inglese dell'aggiornamento o scaricare l'aggiornamento dal catalogo Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="76ac3-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="76ac3-143">Dopo l'espansione del pacchetto padre, non è possibile eseguire la sequenza di un plug-in con componenti affiancati</span><span class="sxs-lookup"><span data-stu-id="76ac3-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="76ac3-144">Quando si espande un pacchetto padre usando **strumenti**  /  **Espandi pacchetto nel sistema locale** nella console App-V Sequencer e si sequenzia un plug-in con componenti affiancati, viene restituito un errore di installazione.</span><span class="sxs-lookup"><span data-stu-id="76ac3-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="76ac3-145">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="76ac3-145">For example:</span></span>

-   **<span data-ttu-id="76ac3-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="76ac3-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="76ac3-147">Questo problema si verifica quando il Sequencer scrive il componente affiancato al registro di sistema, ma non cancella il valore per la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="76ac3-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="76ac3-148">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="76ac3-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="76ac3-149">SOLUZIONE alternativa dopo l'espansione del pacchetto padre nel computer che sta eseguendo il sequencer, è necessario eliminare il valore per la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="76ac3-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="76ac3-150">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="76ac3-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="76ac3-151">Dopo aver eliminato il valore, sequenziare il plug-in.</span><span class="sxs-lookup"><span data-stu-id="76ac3-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="76ac3-152">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="76ac3-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="76ac3-153">Questo documento viene fornito "così com'è".</span><span class="sxs-lookup"><span data-stu-id="76ac3-153">This document is provided “as-is”.</span></span> <span data-ttu-id="76ac3-154">Le informazioni e le visualizzazioni espresse in questo documento, ad esempio URL e altri riferimenti al sito Web Internet, possono essere modificate senza preavviso.</span><span class="sxs-lookup"><span data-stu-id="76ac3-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="76ac3-155">Si rischia di usarlo.</span><span class="sxs-lookup"><span data-stu-id="76ac3-155">You bear the risk of using it.</span></span>

<span data-ttu-id="76ac3-156">Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi.</span><span class="sxs-lookup"><span data-stu-id="76ac3-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="76ac3-157">Nessuna associazione o connessione reale è destinata o deve essere dedotta.</span><span class="sxs-lookup"><span data-stu-id="76ac3-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="76ac3-158">Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76ac3-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="76ac3-159">È possibile copiare e usare questo documento per fini di riferimento interno.</span><span class="sxs-lookup"><span data-stu-id="76ac3-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="76ac3-160">È possibile modificare questo documento per gli scopi interni e di riferimento.</span><span class="sxs-lookup"><span data-stu-id="76ac3-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="76ac3-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="76ac3-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="76ac3-162">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="76ac3-162">All other trademarks are property of their respective owners.</span></span>

 

 





