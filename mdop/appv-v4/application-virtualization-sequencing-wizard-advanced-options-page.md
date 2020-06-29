---
title: Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni
description: Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819596"
---
# <span data-ttu-id="64dc9-103">Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="64dc9-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="64dc9-104">Usare la pagina **Opzioni avanzate** della procedura guidata di sequenziazione della Application Virtualization (App-V) per specificare le opzioni avanzate per l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc9-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="64dc9-105">La pagina contiene gli elementi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="64dc9-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64dc9-106">Nome</span><span class="sxs-lookup"><span data-stu-id="64dc9-106">Name</span></span></th>
<th align="left"><span data-ttu-id="64dc9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dc9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-108">Dimensione blocco</span><span class="sxs-lookup"><span data-stu-id="64dc9-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-109">Consente di specificare le dimensioni dei blocchi in cui verrà suddiviso il file SFT in caso di flusso in una rete.</span><span class="sxs-lookup"><span data-stu-id="64dc9-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="64dc9-110">Tutti i blocchi equivalgono alle dimensioni specificate; l'ultimo blocco potrebbe tuttavia essere più piccolo di quello specificato.</span><span class="sxs-lookup"><span data-stu-id="64dc9-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="64dc9-111">Selezionare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="64dc9-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="64dc9-112">4 KB</span><span class="sxs-lookup"><span data-stu-id="64dc9-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="64dc9-113">16 KB</span><span class="sxs-lookup"><span data-stu-id="64dc9-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="64dc9-114">32 KB</span><span class="sxs-lookup"><span data-stu-id="64dc9-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="64dc9-115">64 KB</span><span class="sxs-lookup"><span data-stu-id="64dc9-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="64dc9-116">Nota</span><span class="sxs-lookup"><span data-stu-id="64dc9-116">Note</span></span></strong><br/><p><span data-ttu-id="64dc9-117">Quando si seleziona una dimensione di blocco, prendere in considerazione le dimensioni del file SFT e la larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="64dc9-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="64dc9-118">Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="64dc9-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="64dc9-119">I file con dimensioni di blocco più grandi potrebbero essere trasmessi più rapidamente, ma usano più larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="64dc9-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="64dc9-120">Grazie alla sperimentazione, è possibile individuare le dimensioni di blocco ottimali per le applicazioni di streaming della rete.</span><span class="sxs-lookup"><span data-stu-id="64dc9-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="64dc9-121">Abilitare Microsoft Update durante il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="64dc9-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-122">Consente l'installazione di Microsoft Updates durante la sequenziazione guidata&#39;la fase di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="64dc9-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-123">Rebase dll</span><span class="sxs-lookup"><span data-stu-id="64dc9-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-124">Consente di rimappare le raccolte di collegamenti dinamici supportate in uno spazio contiguo della RAM, salvando la memoria e migliorando le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="64dc9-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="64dc9-125">Back</span><span class="sxs-lookup"><span data-stu-id="64dc9-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-126">Accede alla procedura guidata di sequenziazione&#39;s pagina precedente.</span><span class="sxs-lookup"><span data-stu-id="64dc9-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-127">Next</span><span class="sxs-lookup"><span data-stu-id="64dc9-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-128">Accede alla procedura guidata di sequenziazione&#39;s pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="64dc9-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="64dc9-129">Annulla</span><span class="sxs-lookup"><span data-stu-id="64dc9-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-130">Termina l'operazione della procedura guidata di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="64dc9-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="64dc9-131">\ [Valore token modello \]</span><span class="sxs-lookup"><span data-stu-id="64dc9-131">\[Template Token Value\]</span></span>

<span data-ttu-id="64dc9-132">Usare la pagina **Opzioni avanzate** della procedura guidata di sequenziazione App-V per specificare le opzioni avanzate per l'applicazione che si sta sequenziando.</span><span class="sxs-lookup"><span data-stu-id="64dc9-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="64dc9-133">Questa pagina contiene gli elementi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="64dc9-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64dc9-134">Nome</span><span class="sxs-lookup"><span data-stu-id="64dc9-134">Name</span></span></th>
<th align="left"><span data-ttu-id="64dc9-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dc9-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-136">Consentire l'esecuzione di Microsoft Update durante il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="64dc9-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-137">Specifica se gli aggiornamenti software verranno applicati all'applicazione durante la fase di monitoraggio della sequenziazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc9-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="64dc9-138">Questa opzione è utile se è necessario aggiornare gli aggiornamenti per completare correttamente l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc9-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="64dc9-139">Questa opzione non è selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="64dc9-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="64dc9-140">Rebase dll</span><span class="sxs-lookup"><span data-stu-id="64dc9-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-141">Consente di rimappare le raccolte di collegamenti dinamici supportate in uno spazio contiguo della RAM.</span><span class="sxs-lookup"><span data-stu-id="64dc9-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="64dc9-142">La selezione di questa opzione consente di gestire la memoria e migliorare le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc9-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="64dc9-143">Questa opzione non è selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="64dc9-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-144">Back</span><span class="sxs-lookup"><span data-stu-id="64dc9-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-145">Passa alla pagina precedente della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="64dc9-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="64dc9-146">Next</span><span class="sxs-lookup"><span data-stu-id="64dc9-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-147">Passa alla pagina successiva della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="64dc9-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64dc9-148">Annulla</span><span class="sxs-lookup"><span data-stu-id="64dc9-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64dc9-149">Elimina le impostazioni e chiude la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="64dc9-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="64dc9-150">\ [Valore token modello \]</span><span class="sxs-lookup"><span data-stu-id="64dc9-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="64dc9-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64dc9-151">Related topics</span></span>


[<span data-ttu-id="64dc9-152">Procedura di sequenziazione guidata</span><span class="sxs-lookup"><span data-stu-id="64dc9-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









