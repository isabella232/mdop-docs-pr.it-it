---
title: Parametri della riga di comando di Sequencer
description: Parametri della riga di comando di Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815555"
---
# <span data-ttu-id="be6d9-103">Parametri della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="be6d9-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="be6d9-104">Puoi usare i parametri di sequencer di Application Virtualization (App-V) seguenti per sequenziare un'applicazione e aggiornare un'applicazione virtuale esistente usando una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="be6d9-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="be6d9-105">Per altre informazioni sulla sequenziazione di un'applicazione tramite una riga di comando, vedere [come sequenziare una nuova applicazione usando la riga di comando](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="be6d9-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="be6d9-106">Parametri della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="be6d9-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="be6d9-107">/HELP o/?</span><span class="sxs-lookup"><span data-stu-id="be6d9-107">/HELP or /?</span></span>**  
<span data-ttu-id="be6d9-108">Visualizza informazioni sui parametri disponibili per l'uso di una riga di comando per sequenziare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="be6d9-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="be6d9-109">/INSTALLPACKAGE o/I</span><span class="sxs-lookup"><span data-stu-id="be6d9-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="be6d9-110">Specifica il Windows Installer o un file batch che verrà usato per installare un'applicazione in modo che possa essere sequenziata.</span><span class="sxs-lookup"><span data-stu-id="be6d9-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="be6d9-111">/INSTALLPATH o/P</span><span class="sxs-lookup"><span data-stu-id="be6d9-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="be6d9-112">Specifica la directory radice del pacchetto per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="be6d9-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="be6d9-113">/OUTPUTFILE o/O</span><span class="sxs-lookup"><span data-stu-id="be6d9-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="be6d9-114">Specifica il percorso e il nome file del file SPRJ che verrà generato.</span><span class="sxs-lookup"><span data-stu-id="be6d9-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="be6d9-115">/FULLLOAD o/F</span><span class="sxs-lookup"><span data-stu-id="be6d9-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="be6d9-116">Specifica se tutti i file saranno contenuti nel blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="be6d9-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="be6d9-117">Se il parametro **/FULLLOAD** è specificato nella riga di comando, tutti i dati dell'applicazione associata vengono aggiunti al blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="be6d9-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="be6d9-118">Se il parametro **/FULLLOAD** non è specificato nella riga di comando, nessuno dei dati dell'applicazione associata verrà aggiunto al blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="be6d9-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="be6d9-119">/PACKAGENAME o/K</span><span class="sxs-lookup"><span data-stu-id="be6d9-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="be6d9-120">Specifica il nome del pacchetto che verrà assegnato all'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="be6d9-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="be6d9-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="be6d9-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="be6d9-122">Specifica la dimensione del blocco di file SFT che verrà usata per trasmettere il pacchetto ai computer client.</span><span class="sxs-lookup"><span data-stu-id="be6d9-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="be6d9-123">È possibile selezionare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="be6d9-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="be6d9-124">4 KB</span><span class="sxs-lookup"><span data-stu-id="be6d9-124">4 KB</span></span>

-   <span data-ttu-id="be6d9-125">16 KB</span><span class="sxs-lookup"><span data-stu-id="be6d9-125">16 KB</span></span>

-   <span data-ttu-id="be6d9-126">32 KB</span><span class="sxs-lookup"><span data-stu-id="be6d9-126">32 KB</span></span>

-   <span data-ttu-id="be6d9-127">64 KB</span><span class="sxs-lookup"><span data-stu-id="be6d9-127">64 KB</span></span>

<span data-ttu-id="be6d9-128">Quando si specifica la dimensione del blocco, è consigliabile prendere in considerazione le dimensioni del file SFT.</span><span class="sxs-lookup"><span data-stu-id="be6d9-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="be6d9-129">Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="be6d9-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="be6d9-130">I file con dimensioni di blocco più grandi usano più larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="be6d9-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="be6d9-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="be6d9-131">/COMPRESSION</span></span>**  
<span data-ttu-id="be6d9-132">Specifica il metodo per la compressione del file SFT che verrà trasmesso al client.</span><span class="sxs-lookup"><span data-stu-id="be6d9-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="be6d9-133">/MSI o/M</span><span class="sxs-lookup"><span data-stu-id="be6d9-133">/MSI or /M</span></span>**  
<span data-ttu-id="be6d9-134">Specifica se deve essere creato un Windows Installer per l'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="be6d9-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="be6d9-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="be6d9-135">/DEFAULT</span></span>**  
<span data-ttu-id="be6d9-136">Specifica il file SPRJ predefinito che verrà usato per la creazione di un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="be6d9-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="be6d9-137">Questo file viene usato come modello. sprj quando l'applicazione viene sequenziata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="be6d9-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="be6d9-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="be6d9-138">/UPGRADE</span></span>**  
<span data-ttu-id="be6d9-139">Specifica il percorso e il nome file del file SPRJ che verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="be6d9-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="be6d9-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="be6d9-140">/DECODEPATH</span></span>**  
<span data-ttu-id="be6d9-141">Specifica la directory nel computer di sequenziazione in cui sono installati i file associati al pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="be6d9-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="be6d9-142">Quando si specifica la directory, usare uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="be6d9-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="be6d9-143">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="be6d9-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="be6d9-144">/DECODEPATH: D:.</span><span class="sxs-lookup"><span data-stu-id="be6d9-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="be6d9-145">/DECODEPATH: "D:."</span><span class="sxs-lookup"><span data-stu-id="be6d9-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="be6d9-146">/DECODEPATH: "d:"</span><span class="sxs-lookup"><span data-stu-id="be6d9-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="be6d9-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be6d9-147">Related topics</span></span>


[<span data-ttu-id="be6d9-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="be6d9-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="be6d9-149">Codici di errore della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="be6d9-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





