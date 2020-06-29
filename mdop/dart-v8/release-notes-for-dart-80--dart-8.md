---
title: Note sulla versione per DaRT 8.0
description: Note sulla versione per DaRT 8.0
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824786"
---
# <span data-ttu-id="00711-103">Note sulla versione per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="00711-103">Release Notes for DaRT 8.0</span></span>


**<span data-ttu-id="00711-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="00711-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="00711-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="00711-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span>

<span data-ttu-id="00711-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente il dardo 8,0.</span><span class="sxs-lookup"><span data-stu-id="00711-106">These release notes contain information that is required to successfully install DaRT 8.0.</span></span> <span data-ttu-id="00711-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="00711-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="00711-108">Se c'è una differenza tra queste note sulla versione e altra documentazione DaRT, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="00711-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="00711-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="00711-109">These release notes supersede the content that is included with this product.</span></span>

<span data-ttu-id="00711-110">Per ottenere il software DaRT, Vedi [come ottenere MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="00711-110">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="00711-111">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="00711-111">About the product documentation</span></span>


<span data-ttu-id="00711-112">Per informazioni sulla documentazione per DaRT, vedere la [Home page di Dart](https://go.microsoft.com/fwlink/?LinkID=252096) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="00711-112">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

<span data-ttu-id="00711-113">Per ottenere una copia scaricabile della documentazione di DaRT, vedere nell' <https://go.microsoft.com/fwlink/?LinkID=267420> area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="00711-113">To obtain a downloadable copy of DaRT documentation, see <https://go.microsoft.com/fwlink/?LinkID=267420> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="00711-114">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="00711-114">Providing feedback</span></span>


<span data-ttu-id="00711-115">Siamo interessati al feedback su DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="00711-115">We are interested in your feedback on DaRT 8.0.</span></span> <span data-ttu-id="00711-116">È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="00711-116">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="00711-117">**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future per la documentazione e i rilasci del prodotto.</span><span class="sxs-lookup"><span data-stu-id="00711-117">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="00711-118">Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="00711-118">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="00711-119">Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="00711-119">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="00711-120">Problemi noti di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="00711-120">Known issues with DaRT 8.0</span></span>


### <span data-ttu-id="00711-121">Ripristino configurazione di sistema non riesce quando si esegue un fabbro o un editor del registro</span><span class="sxs-lookup"><span data-stu-id="00711-121">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="00711-122">Se si esegue fabbro, editor del registro di sistema e, eventualmente, altri strumenti, ripristino configurazione di rete non riesce.</span><span class="sxs-lookup"><span data-stu-id="00711-122">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="00711-123">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="00711-123">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="00711-124">L'analisi SFC non viene eseguita dopo l'avvio e la chiusura di fabbro o Gestione computer</span><span class="sxs-lookup"><span data-stu-id="00711-124">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="00711-125">Se si avvia e quindi si chiudono gli strumenti di gestione del fabbro o del computer, non è possibile eseguire Verifica file di sistema.</span><span class="sxs-lookup"><span data-stu-id="00711-125">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="00711-126">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare SFC.</span><span class="sxs-lookup"><span data-stu-id="00711-126">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="00711-127">Il programma di installazione di DaRT non ha esito negativo quando ADK non è stato installato</span><span class="sxs-lookup"><span data-stu-id="00711-127">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="00711-128">Se si installa DaRT 8,0 usando la riga di comando per eseguire il file MSI e il ADK non è stato installato, l'installazione di DaRT dovrebbe avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="00711-128">If you install DaRT 8.0 by using the command line to execute the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="00711-129">Attualmente, il programma di installazione di DaRT 8,0 installa tutti i componenti tranne l'immagine di ripristino di DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="00711-129">Currently, the DaRT 8.0 installer installs all components except the DaRT 8.0 recovery image.</span></span>

<span data-ttu-id="00711-130">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="00711-130">**Workaround:** None.</span></span>

### <span data-ttu-id="00711-131">Il difensore non può essere lanciato dopo il lancio di fabbro, RegEdit, Crash Analyzer e gestione computer</span><span class="sxs-lookup"><span data-stu-id="00711-131">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="00711-132">Il difensore non viene avviato se sono già stati avviati fabbro, RegEdit, Crash Analyzer e gestione computer.</span><span class="sxs-lookup"><span data-stu-id="00711-132">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="00711-133">**Soluzione alternativa:** Chiudere e riavviare il dardo e quindi avviare Defender.</span><span class="sxs-lookup"><span data-stu-id="00711-133">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="00711-134">Il difensore potrebbe essere lento all'avvio</span><span class="sxs-lookup"><span data-stu-id="00711-134">Defender may be slow to launch</span></span>

<span data-ttu-id="00711-135">Il difensore a volte richiede alcuni minuti per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="00711-135">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="00711-136">La barra di stato indica lo stato di caricamento corrente.</span><span class="sxs-lookup"><span data-stu-id="00711-136">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="00711-137">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="00711-137">**Workaround:** None.</span></span>

## <span data-ttu-id="00711-138">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="00711-138">Release notes copyright information</span></span>


<span data-ttu-id="00711-139">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="00711-139">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="00711-140">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="00711-140">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="00711-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00711-141">Related topics</span></span>


[<span data-ttu-id="00711-142">Informazioni su DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="00711-142">About DaRT 8.0</span></span>](about-dart-80-dart-8.md)

 

 





