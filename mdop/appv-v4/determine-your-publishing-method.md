---
title: Determinare il metodo di pubblicazione
description: Determinare il metodo di pubblicazione
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821676"
---
# <span data-ttu-id="bc78c-103">Determinare il metodo di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="bc78c-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="bc78c-104">Dopo aver sequenziato un'applicazione usando l'Application Virtualization Sequencer, è necessario *pubblicare* l'applicazione per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="bc78c-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="bc78c-105">La pubblicazione dell'applicazione consiste nell'offrire le icone, le informazioni sulla definizione dei pacchetti e la posizione dell'origine contenuto in ogni computer in cui è stato installato il client di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc78c-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="bc78c-106">La tabella seguente descrive i metodi di pubblicazione supportati quando si distribuisce la virtualizzazione delle applicazioni tramite un sistema ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="bc78c-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc78c-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc78c-107">Method</span></span></th>
<th align="left"><span data-ttu-id="bc78c-108">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="bc78c-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="bc78c-109">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="bc78c-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc78c-110">Genera un file di Windows Installer durante la sequenziazione, come soluzione autonoma.</span><span class="sxs-lookup"><span data-stu-id="bc78c-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-111">Molto semplice da usare.</span><span class="sxs-lookup"><span data-stu-id="bc78c-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-112">Pacchetto caricato nella cache localmente in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="bc78c-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-113">Icone visualizzate per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bc78c-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-114">Simile alla distribuzione tradizionale del software.</span><span class="sxs-lookup"><span data-stu-id="bc78c-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-115">Non è necessario per i server di streaming.</span><span class="sxs-lookup"><span data-stu-id="bc78c-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-116">Nessuna flessibilità nella posizione del contenuto del pacchetto nei computer, stessa posizione in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="bc78c-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-117">Per rimuovere le applicazioni, è necessario usare solo Aggiungi/Rimuovi programmi o msiexec.</span><span class="sxs-lookup"><span data-stu-id="bc78c-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-118">Rimozione e sostituzione con la nuova versione necessaria per l'aggiornamento dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bc78c-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc78c-119">Genera un file di Windows Installer durante la sequenziazione, usato con le proprietà della riga di comando modalità, carica e OVERRIDEURL e il manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bc78c-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-120">Semplice da usare, ma con maggiore flessibilità.</span><span class="sxs-lookup"><span data-stu-id="bc78c-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-121">Icone visualizzate per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bc78c-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-122">Il file SFT che contiene le applicazioni può essere posizionato in una posizione di origine di flusso, con i client configurati per l'uso di tale posizione.</span><span class="sxs-lookup"><span data-stu-id="bc78c-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-123">Flessibilità limitata: solo la posizione del contenuto del pacchetto può essere controllata in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bc78c-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-124">Per rimuovere l'applicazione, è necessario usare solo Aggiungi/Rimuovi programmi o msiexec.</span><span class="sxs-lookup"><span data-stu-id="bc78c-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-125">Rimozione e sostituzione con la nuova versione necessaria per l'aggiornamento dei pacchetti, a meno che non si usi streaming server.</span><span class="sxs-lookup"><span data-stu-id="bc78c-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc78c-126">Eseguire i comandi di SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="bc78c-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-127">Flessibilità completa: controllo completo di tutte le funzioni di gestione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bc78c-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc78c-128">I comandi devono essere scritti per l'uso con il sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="bc78c-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-129">I comandi devono essere eseguiti in ogni computer in sequenza corretta.</span><span class="sxs-lookup"><span data-stu-id="bc78c-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="bc78c-130">Informazioni dettagliate sul linguaggio dei comandi e su una pianificazione accurata.</span><span class="sxs-lookup"><span data-stu-id="bc78c-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bc78c-131">Per altre informazioni sull'uso di questi metodi di pubblicazione, vedere [come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="bc78c-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="bc78c-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc78c-132">Related topics</span></span>


[<span data-ttu-id="bc78c-133">Determinare il metodo di streaming</span><span class="sxs-lookup"><span data-stu-id="bc78c-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="bc78c-134">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="bc78c-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="bc78c-135">Panoramica di uno scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="bc78c-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="bc78c-136">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="bc78c-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="bc78c-137">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="bc78c-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





