---
title: Note sulla versione di App-V 4.6 SP2
description: Note sulla versione di App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822345"
---
# <span data-ttu-id="0a176-103">Note sulla versione di App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="0a176-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="0a176-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="0a176-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="0a176-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Application Virtualization (App-V) 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="0a176-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="0a176-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente Application Virtualization 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="0a176-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="0a176-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0a176-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="0a176-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V 4.6 SP2, la modifica più recente deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="0a176-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="0a176-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="0a176-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="0a176-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="0a176-110">About the Product Documentation</span></span>


<span data-ttu-id="0a176-111">Per altre informazioni sulla documentazione per App-V, vedere la pagina [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="0a176-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="0a176-112">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="0a176-112">Providing feedback</span></span>


<span data-ttu-id="0a176-113">Siamo interessati a ricevere commenti e suggerimenti su App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="0a176-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="0a176-114">È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="0a176-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="0a176-115">**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future per la documentazione e i rilasci del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0a176-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="0a176-116">Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="0a176-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="0a176-117">Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="0a176-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="0a176-118">Problemi noti di App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="0a176-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="0a176-119">Il supporto dei nomi di file brevi è disabilitato per le unità fisiche non di sistema quando si sequenzia</span><span class="sxs-lookup"><span data-stu-id="0a176-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="0a176-120">Quando si sequenzia in Windows 8 o Windows Server 2012, il supporto per i nomi di file brevi (8,3) è disabilitato per impostazione predefinita per le unità fisiche non di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a176-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="0a176-121">L'unità fisica sottostante associata alla directory principale dell'applicazione virtuale (ad esempio, "Q:\\appname") nella stazione di sequenziazione deve fornire il supporto per il nome di file breve (8,3) in modo che l'App-V 4.6 SP2 sequencer generi i nomi di file brevi durante la creazione di pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="0a176-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="0a176-122">Il supporto del nome file breve (8,3) è disabilitato per impostazione predefinita per le unità fisiche non di sistema in Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0a176-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="0a176-123">**Soluzione alternativa:** Abilitare il supporto per il nome file breve (8,3) sulle unità fisiche non di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a176-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="0a176-124">Puoi usare il comando seguente per abilitare il supporto dei nomi di file brevi in Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0a176-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="0a176-125">Ad esempio, usa il comando seguente se la lettera dell'unità è "Q:":</span><span class="sxs-lookup"><span data-stu-id="0a176-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="0a176-126">**Nota**  Non è necessario modificare questa impostazione nel client App-V perché il file System App-V gestisce correttamente i percorsi brevi in Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0a176-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="0a176-127">App-V non esegue l'override del gestore predefinito per il tipo di file o le associazioni di protocollo in Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a176-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="0a176-128">Se selezioni un'applicazione predefinita usando **programmi predefiniti** nel pannello di **controllo** di Windows 8, App-V non eseguirà l'override delle associazioni di tipi di file associate per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a176-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="0a176-129">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="0a176-129">**Workaround:** None.</span></span>

### <span data-ttu-id="0a176-130">Outlook 2010 virtualizzato non è offerto come opzione per i collegamenti selezionabili di mailto in Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a176-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="0a176-131">L'estensione della shell mailto non offre Outlook 2010 virtualizzato in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a176-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="0a176-132">Ad esempio, se si fa clic su un collegamento mailto: da Outlook 2010 virtualizzato in uso in Windows 8, non viene creata una nuova finestra di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="0a176-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="0a176-133">Questa opzione funziona correttamente in Windows 7 e nelle versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0a176-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="0a176-134">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="0a176-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="0a176-135">L'aggiornamento di Application Virtualization 4,6 SP2 non è disponibile in tutte le impostazioni locali che usano Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="0a176-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="0a176-136">Quando si usa Microsoft Update, l'aggiornamento per App-V 4.6 SP2 non è disponibile per le impostazioni locali della lingua seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a176-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="0a176-137">Kazaco</span><span class="sxs-lookup"><span data-stu-id="0a176-137">Kazakh</span></span>

-   <span data-ttu-id="0a176-138">Hindi</span><span class="sxs-lookup"><span data-stu-id="0a176-138">Hindi</span></span>

-   <span data-ttu-id="0a176-139">Serbo-cirillico</span><span class="sxs-lookup"><span data-stu-id="0a176-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="0a176-140">**Soluzione alternativa:** Se si usa Microsoft Windows Server Update Services (WSUS), usare la versione in lingua inglese dell'aggiornamento o scaricare l'aggiornamento dal catalogo Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="0a176-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="0a176-141">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="0a176-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="0a176-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="0a176-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="0a176-143">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="0a176-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="0a176-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a176-144">Related topics</span></span>


[<span data-ttu-id="0a176-145">Informazioni su Microsoft Application Virtualization 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="0a176-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 





