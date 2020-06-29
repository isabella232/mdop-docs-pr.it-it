---
title: Note sulla versione per DaRT 8.0 SP1
description: Note sulla versione per DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824775"
---
# <span data-ttu-id="cefba-103">Note sulla versione per DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="cefba-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="cefba-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="cefba-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="cefba-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cefba-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="cefba-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente la diagnostica e il set di strumenti di ripristino 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="cefba-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="cefba-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="cefba-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="cefba-108">Se c'è una differenza tra queste note sulla versione e altra documentazione DaRT, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="cefba-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="cefba-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="cefba-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="cefba-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="cefba-110">About the product documentation</span></span>


<span data-ttu-id="cefba-111">Per informazioni sulla documentazione per DaRT, vedere la [Home page di Dart](https://go.microsoft.com/fwlink/?LinkID=252096) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="cefba-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="cefba-112">Problemi noti di DaRT 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="cefba-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="cefba-113">Ripristino configurazione di sistema non riesce quando si esegue un fabbro o un editor del registro</span><span class="sxs-lookup"><span data-stu-id="cefba-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="cefba-114">Se si esegue fabbro, editor del registro di sistema e, eventualmente, altri strumenti, ripristino configurazione di rete non riesce.</span><span class="sxs-lookup"><span data-stu-id="cefba-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="cefba-115">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="cefba-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="cefba-116">L'analisi SFC non viene eseguita dopo l'avvio e la chiusura di fabbro o Gestione computer</span><span class="sxs-lookup"><span data-stu-id="cefba-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="cefba-117">Se si avvia e quindi si chiudono gli strumenti di gestione del fabbro o del computer, non è possibile eseguire Verifica file di sistema.</span><span class="sxs-lookup"><span data-stu-id="cefba-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="cefba-118">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare SFC.</span><span class="sxs-lookup"><span data-stu-id="cefba-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="cefba-119">Il programma di installazione di DaRT non ha esito negativo quando ADK non è stato installato</span><span class="sxs-lookup"><span data-stu-id="cefba-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="cefba-120">Se si installa DaRT 8,0 SP1 usando la riga di comando per eseguire il file MSI e il ADK non è stato installato, l'installazione di DaRT dovrebbe avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cefba-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="cefba-121">Attualmente, il programma di installazione di DaRT 8,0 SP1 installa tutti i componenti tranne l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="cefba-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="cefba-122">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="cefba-122">**Workaround:** None.</span></span>

### <span data-ttu-id="cefba-123">Il difensore non può essere lanciato dopo il lancio di fabbro, RegEdit, Crash Analyzer e gestione computer</span><span class="sxs-lookup"><span data-stu-id="cefba-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="cefba-124">Il difensore non viene avviato se sono già stati avviati fabbro, RegEdit, Crash Analyzer e gestione computer.</span><span class="sxs-lookup"><span data-stu-id="cefba-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="cefba-125">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Defender.</span><span class="sxs-lookup"><span data-stu-id="cefba-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="cefba-126">Il difensore potrebbe essere lento all'avvio</span><span class="sxs-lookup"><span data-stu-id="cefba-126">Defender may be slow to launch</span></span>

<span data-ttu-id="cefba-127">Il difensore a volte richiede alcuni minuti per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="cefba-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="cefba-128">La barra di stato indica lo stato di caricamento corrente.</span><span class="sxs-lookup"><span data-stu-id="cefba-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="cefba-129">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="cefba-129">**Workaround:** None.</span></span>

## <span data-ttu-id="cefba-130">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="cefba-130">Release notes copyright information</span></span>


<span data-ttu-id="cefba-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="cefba-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="cefba-132">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="cefba-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="cefba-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cefba-133">Related topics</span></span>


[<span data-ttu-id="cefba-134">Informazioni su DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="cefba-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





