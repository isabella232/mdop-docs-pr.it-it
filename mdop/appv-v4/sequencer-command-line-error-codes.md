---
title: Codici di errore della riga di comando di Sequencer
description: Codici di errore della riga di comando di Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815556"
---
# <span data-ttu-id="6152a-103">Codici di errore della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="6152a-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="6152a-104">Usare l'elenco seguente per identificare gli errori correlati alla sequenziazione delle applicazioni tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6152a-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="6152a-105">Queste informazioni possono essere visualizzate anche visualizzando il file di log sequencer di App-V associato.</span><span class="sxs-lookup"><span data-stu-id="6152a-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="6152a-106">**Nota**  Durante la sequenziazione si possono verificare più errori e, in questo caso, il codice di errore visualizzato potrebbe essere la somma di due codici di errore.</span><span class="sxs-lookup"><span data-stu-id="6152a-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="6152a-107">Ad esempio, se mancano i parametri */InstallPath* e */outputfile* , l'App-V sequencer restituirà **96**, ovvero la somma dei due codici di errore.</span><span class="sxs-lookup"><span data-stu-id="6152a-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="6152a-108">01</span><span class="sxs-lookup"><span data-stu-id="6152a-108">01</span></span>  
<span data-ttu-id="6152a-109">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="6152a-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="6152a-110">02</span><span class="sxs-lookup"><span data-stu-id="6152a-110">02</span></span>  
<span data-ttu-id="6152a-111">La directory di installazione specificata (/INSTALLPACKAGE) non è valida.</span><span class="sxs-lookup"><span data-stu-id="6152a-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="6152a-112">04</span><span class="sxs-lookup"><span data-stu-id="6152a-112">04</span></span>  
<span data-ttu-id="6152a-113">La directory radice del pacchetto specificata (/INSTALLPATH) non è valida.</span><span class="sxs-lookup"><span data-stu-id="6152a-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="6152a-114">08</span><span class="sxs-lookup"><span data-stu-id="6152a-114">08</span></span>  
<span data-ttu-id="6152a-115">Il parametro */outputfile* specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="6152a-116">16</span><span class="sxs-lookup"><span data-stu-id="6152a-116">16</span></span>  
<span data-ttu-id="6152a-117">La directory di installazione (/INSTALLPACKAGE) non è specificata.</span><span class="sxs-lookup"><span data-stu-id="6152a-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="6152a-118">32</span><span class="sxs-lookup"><span data-stu-id="6152a-118">32</span></span>  
<span data-ttu-id="6152a-119">La directory radice del pacchetto (/INSTALLPATH) non è specificata.</span><span class="sxs-lookup"><span data-stu-id="6152a-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="6152a-120">64</span><span class="sxs-lookup"><span data-stu-id="6152a-120">64</span></span>  
<span data-ttu-id="6152a-121">Il parametro */outputfile* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="6152a-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="6152a-122">128</span><span class="sxs-lookup"><span data-stu-id="6152a-122">128</span></span>  
<span data-ttu-id="6152a-123">L'unità di virtualizzazione dell'applicazione specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="6152a-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="6152a-124">256</span><span class="sxs-lookup"><span data-stu-id="6152a-124">256</span></span>  
<span data-ttu-id="6152a-125">Il programma di installazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6152a-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="6152a-126">512</span><span class="sxs-lookup"><span data-stu-id="6152a-126">512</span></span>  
<span data-ttu-id="6152a-127">La sequenziazione dell'applicazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6152a-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="6152a-128">1024</span><span class="sxs-lookup"><span data-stu-id="6152a-128">1024</span></span>  
<span data-ttu-id="6152a-129">La valutazione delle scelte rapide installate non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6152a-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="6152a-130">2048</span><span class="sxs-lookup"><span data-stu-id="6152a-130">2048</span></span>  
<span data-ttu-id="6152a-131">Non è possibile salvare il pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="6152a-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="6152a-132">4096</span><span class="sxs-lookup"><span data-stu-id="6152a-132">4096</span></span>  
<span data-ttu-id="6152a-133">Il nome del pacchetto specificato (/PACKAGENAME) non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="6152a-134">8192</span><span class="sxs-lookup"><span data-stu-id="6152a-134">8192</span></span>  
<span data-ttu-id="6152a-135">La dimensione del blocco specificata (/BLOCKSIZE) non è valida.</span><span class="sxs-lookup"><span data-stu-id="6152a-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="6152a-136">16384</span><span class="sxs-lookup"><span data-stu-id="6152a-136">16384</span></span>  
<span data-ttu-id="6152a-137">Il tipo di compressione specificato (/COMPRESSION) non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="6152a-138">32768</span><span class="sxs-lookup"><span data-stu-id="6152a-138">32768</span></span>  
<span data-ttu-id="6152a-139">Il percorso del progetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="6152a-140">65536</span><span class="sxs-lookup"><span data-stu-id="6152a-140">65536</span></span>  
<span data-ttu-id="6152a-141">Il parametro di aggiornamento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="6152a-142">131072</span><span class="sxs-lookup"><span data-stu-id="6152a-142">131072</span></span>  
<span data-ttu-id="6152a-143">Il parametro del progetto di aggiornamento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="6152a-144">262144</span><span class="sxs-lookup"><span data-stu-id="6152a-144">262144</span></span>  
<span data-ttu-id="6152a-145">Il parametro path Decode specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6152a-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="6152a-146">525288</span><span class="sxs-lookup"><span data-stu-id="6152a-146">525288</span></span>  
<span data-ttu-id="6152a-147">Il nome del pacchetto non è specificato.</span><span class="sxs-lookup"><span data-stu-id="6152a-147">The package name is not specified.</span></span>

## <span data-ttu-id="6152a-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6152a-148">Related topics</span></span>


[<span data-ttu-id="6152a-149">Riferimento per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6152a-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="6152a-150">Parametri della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="6152a-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





