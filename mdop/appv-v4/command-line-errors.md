---
title: Errori della riga di comando
description: Errori della riga di comando
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819406"
---
# <span data-ttu-id="b018c-103">Errori della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b018c-103">Command-Line Errors</span></span>


<span data-ttu-id="b018c-104">Usare l'elenco di errori seguente per identificare i motivi per cui la sequenziazione della riga di comando non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="b018c-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="b018c-105">È anche possibile visualizzare questi errori visualizzando il file di log del sequencer.</span><span class="sxs-lookup"><span data-stu-id="b018c-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="b018c-106">**Nota**  Durante la sequenziazione potrebbe essere visualizzato più di un errore.</span><span class="sxs-lookup"><span data-stu-id="b018c-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="b018c-107">Inoltre, il codice di errore visualizzato può essere la somma di due codici di errore.</span><span class="sxs-lookup"><span data-stu-id="b018c-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="b018c-108">Ad esempio, se i parametri */InstallPath* e */outputfile* sono mancanti, Microsoft System Center Application Virtualization Sequencer restituirà 96, ovvero la somma dei due codici di errore.</span><span class="sxs-lookup"><span data-stu-id="b018c-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="b018c-109">01</span><span class="sxs-lookup"><span data-stu-id="b018c-109">01</span></span>  
<span data-ttu-id="b018c-110">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b018c-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="b018c-111">02</span><span class="sxs-lookup"><span data-stu-id="b018c-111">02</span></span>  
<span data-ttu-id="b018c-112">La directory di installazione specificata (/INSTALLPACKAGE) specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="b018c-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="b018c-113">04</span><span class="sxs-lookup"><span data-stu-id="b018c-113">04</span></span>  
<span data-ttu-id="b018c-114">La directory radice del pacchetto specificata (/INSTALLPATH) non è valida.</span><span class="sxs-lookup"><span data-stu-id="b018c-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="b018c-115">08</span><span class="sxs-lookup"><span data-stu-id="b018c-115">08</span></span>  
<span data-ttu-id="b018c-116">Il parametro */outputfile* specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="b018c-117">16</span><span class="sxs-lookup"><span data-stu-id="b018c-117">16</span></span>  
<span data-ttu-id="b018c-118">La directory di installazione (/INSTALLPACKAGE) non è stata specificata.</span><span class="sxs-lookup"><span data-stu-id="b018c-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="b018c-119">32</span><span class="sxs-lookup"><span data-stu-id="b018c-119">32</span></span>  
<span data-ttu-id="b018c-120">La directory radice del pacchetto (/INSTALLPATH) non è stata specificata.</span><span class="sxs-lookup"><span data-stu-id="b018c-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="b018c-121">64</span><span class="sxs-lookup"><span data-stu-id="b018c-121">64</span></span>  
<span data-ttu-id="b018c-122">Il parametro */outputfile* non è stato specificato.</span><span class="sxs-lookup"><span data-stu-id="b018c-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="b018c-123">128</span><span class="sxs-lookup"><span data-stu-id="b018c-123">128</span></span>  
<span data-ttu-id="b018c-124">L'unità di virtualizzazione dell'applicazione specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="b018c-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="b018c-125">256</span><span class="sxs-lookup"><span data-stu-id="b018c-125">256</span></span>  
<span data-ttu-id="b018c-126">Il programma di installazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b018c-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="b018c-127">512</span><span class="sxs-lookup"><span data-stu-id="b018c-127">512</span></span>  
<span data-ttu-id="b018c-128">La sequenziazione dell'applicazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b018c-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="b018c-129">1024</span><span class="sxs-lookup"><span data-stu-id="b018c-129">1024</span></span>  
<span data-ttu-id="b018c-130">La valutazione delle scelte rapide installate non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b018c-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="b018c-131">2048</span><span class="sxs-lookup"><span data-stu-id="b018c-131">2048</span></span>  
<span data-ttu-id="b018c-132">Non è possibile salvare il pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="b018c-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="b018c-133">4096</span><span class="sxs-lookup"><span data-stu-id="b018c-133">4096</span></span>  
<span data-ttu-id="b018c-134">Il nome del pacchetto specificato (/PACKAGENAME) non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="b018c-135">8192</span><span class="sxs-lookup"><span data-stu-id="b018c-135">8192</span></span>  
<span data-ttu-id="b018c-136">La dimensione del blocco specificata (/BLOCKSIZE <em> ) </em> non è valida.</span><span class="sxs-lookup"><span data-stu-id="b018c-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="b018c-137">16384</span><span class="sxs-lookup"><span data-stu-id="b018c-137">16384</span></span>  
<span data-ttu-id="b018c-138">Il tipo di compressione specificato (/COMPRESSION) non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="b018c-139">32768</span><span class="sxs-lookup"><span data-stu-id="b018c-139">32768</span></span>  
<span data-ttu-id="b018c-140">Il percorso del progetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="b018c-141">65536</span><span class="sxs-lookup"><span data-stu-id="b018c-141">65536</span></span>  
<span data-ttu-id="b018c-142">Il parametro di aggiornamento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="b018c-143">131072</span><span class="sxs-lookup"><span data-stu-id="b018c-143">131072</span></span>  
<span data-ttu-id="b018c-144">Il parametro del progetto di aggiornamento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="b018c-145">262144</span><span class="sxs-lookup"><span data-stu-id="b018c-145">262144</span></span>  
<span data-ttu-id="b018c-146">Il parametro path Decode specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="b018c-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="b018c-147">525288</span><span class="sxs-lookup"><span data-stu-id="b018c-147">525288</span></span>  
<span data-ttu-id="b018c-148">Il nome del pacchetto non è stato specificato.</span><span class="sxs-lookup"><span data-stu-id="b018c-148">The package name was not specified.</span></span>

## <span data-ttu-id="b018c-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b018c-149">Related topics</span></span>


[<span data-ttu-id="b018c-150">Informazioni sull'utilizzo della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="b018c-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="b018c-151">Parametri della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b018c-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





