---
title: Parametri della riga di comando
description: Parametri della riga di comando
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819405"
---
# <span data-ttu-id="1beb1-103">Parametri della riga di comando</span><span class="sxs-lookup"><span data-stu-id="1beb1-103">Command-Line Parameters</span></span>


<span data-ttu-id="1beb1-104">Usare i parametri sequencer di Application Virtualization seguenti per sequenziare un'applicazione e aggiornare un pacchetto di applicazione sequenziata al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1beb1-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="1beb1-105">Nella directory Microsoft Application Virtualization Sequencer Immetti **SFTSequencer**, seguito dal parametro appropriato.</span><span class="sxs-lookup"><span data-stu-id="1beb1-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="1beb1-106">*/Help* o */?*</span><span class="sxs-lookup"><span data-stu-id="1beb1-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="1beb1-107">Consente di visualizzare l'elenco dei parametri disponibili per la sequenza della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1beb1-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="1beb1-108">*/InstallPackage* o */i*</span><span class="sxs-lookup"><span data-stu-id="1beb1-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="1beb1-109">Consente di specificare il programma di installazione o un file batch per cui l'applicazione deve essere sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1beb1-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="1beb1-110">*/InstallPath* o */p*</span><span class="sxs-lookup"><span data-stu-id="1beb1-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="1beb1-111">Consente di specificare la directory radice del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1beb1-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="1beb1-112">*/Outputfile* o */o*</span><span class="sxs-lookup"><span data-stu-id="1beb1-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="1beb1-113">Consente di specificare il percorso e il nome file del file SPRJ che verrà generato.</span><span class="sxs-lookup"><span data-stu-id="1beb1-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="1beb1-114">**Importante**  Il parametro */outputfile* non è disponibile quando si apre un pacchetto che non si vuole aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1beb1-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="1beb1-115">*/FULLLOAD* o */f*</span><span class="sxs-lookup"><span data-stu-id="1beb1-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="1beb1-116">Consente di specificare se inserire tutto nel blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="1beb1-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="1beb1-117">*/PackageName* o */K*</span><span class="sxs-lookup"><span data-stu-id="1beb1-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="1beb1-118">Consente di specificare il nome del pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1beb1-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="1beb1-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="1beb1-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="1beb1-120">Specifica la dimensione del blocco di file SFT che verrà usata per trasmettere il pacchetto ai computer client.</span><span class="sxs-lookup"><span data-stu-id="1beb1-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="1beb1-121">È possibile selezionare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1beb1-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="1beb1-122">4 KB</span><span class="sxs-lookup"><span data-stu-id="1beb1-122">4 KB</span></span>

-   <span data-ttu-id="1beb1-123">16 KB</span><span class="sxs-lookup"><span data-stu-id="1beb1-123">16 KB</span></span>

-   <span data-ttu-id="1beb1-124">32 KB</span><span class="sxs-lookup"><span data-stu-id="1beb1-124">32 KB</span></span>

-   <span data-ttu-id="1beb1-125">64 KB</span><span class="sxs-lookup"><span data-stu-id="1beb1-125">64 KB</span></span>

<span data-ttu-id="1beb1-126">Quando si specifica la dimensione del blocco, è consigliabile prendere in considerazione le dimensioni del file SFT.</span><span class="sxs-lookup"><span data-stu-id="1beb1-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="1beb1-127">Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="1beb1-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="1beb1-128">I file con dimensioni di blocco più grandi usano più larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="1beb1-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="1beb1-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="1beb1-129">/COMPRESSION</span></span>*  
<span data-ttu-id="1beb1-130">Consente di specificare il metodo per la compressione del file SFT mentre viene trasmesso al client.</span><span class="sxs-lookup"><span data-stu-id="1beb1-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="1beb1-131">*/MSI* o */m*</span><span class="sxs-lookup"><span data-stu-id="1beb1-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="1beb1-132">Consente di specificare la generazione di un pacchetto di Microsoft Windows Installer per l'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1beb1-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="1beb1-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1beb1-133">/DEFAULT</span></span>*  
<span data-ttu-id="1beb1-134">Specifica il file SPRJ predefinito che verrà usato per la creazione di un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="1beb1-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="1beb1-135">Questo file viene usato come modello. sprj quando l'applicazione viene sequenziata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="1beb1-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="1beb1-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="1beb1-136">/UPGRADE</span></span>*  
<span data-ttu-id="1beb1-137">Specifica il percorso e il nome file del file SPRJ che verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1beb1-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="1beb1-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="1beb1-138">/DECODEPATH</span></span>*  
<span data-ttu-id="1beb1-139">Specifica la directory nel computer di sequenziazione in cui sono installati i file associati al pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1beb1-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="1beb1-140">Quando si specifica la directory, usare uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="1beb1-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="1beb1-141">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="1beb1-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="1beb1-142">/DECODEPATH: D:.</span><span class="sxs-lookup"><span data-stu-id="1beb1-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="1beb1-143">/DECODEPATH: "D:."</span><span class="sxs-lookup"><span data-stu-id="1beb1-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="1beb1-144">/DECODEPATH: "d:"</span><span class="sxs-lookup"><span data-stu-id="1beb1-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="1beb1-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1beb1-145">Related topics</span></span>


[<span data-ttu-id="1beb1-146">Informazioni sull'utilizzo della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="1beb1-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="1beb1-147">Come aprire un'applicazione sequenziata usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="1beb1-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="1beb1-148">Come aggiornare un pacchetto usando il comando Apri pacchetto</span><span class="sxs-lookup"><span data-stu-id="1beb1-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





