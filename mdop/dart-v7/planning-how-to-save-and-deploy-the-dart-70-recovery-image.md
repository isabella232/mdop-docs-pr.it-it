---
title: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0
description: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822796"
---
# <span data-ttu-id="b8622-103">Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b8622-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="b8622-104">Usare le informazioni in questa sezione quando si prevede di salvare e distribuire l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="b8622-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="b8622-105">Pianificare come salvare e distribuire l'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="b8622-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="b8622-106">Puoi salvare e distribuire l'immagine di ripristino delle freccette usando i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8622-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="b8622-107">Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="b8622-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="b8622-108">Considera inoltre come vuoi usare il dardo nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="b8622-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="b8622-109">**Nota**  Potresti voler usare più di un metodo nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8622-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="b8622-110">Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="b8622-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="b8622-111">La tabella seguente mostra alcuni vantaggi e svantaggi di ogni metodo per l'uso di DaRT nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8622-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8622-112">Metodo per l'avvio in dardo</span><span class="sxs-lookup"><span data-stu-id="b8622-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="b8622-113">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="b8622-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="b8622-114">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="b8622-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8622-115">Da CD o DVD</span><span class="sxs-lookup"><span data-stu-id="b8622-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-116">Supporta scenari in cui il record di avvio Master (MBR) è danneggiato e non è possibile accedere al disco rigido.</span><span class="sxs-lookup"><span data-stu-id="b8622-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="b8622-117">Supporta anche i casi in cui non è disponibile una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="b8622-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="b8622-118">Questo è il più noto agli utenti di versioni precedenti di DaRT e un CD o DVD può essere masterizzato direttamente dalla <strong> procedura guidata immagine di ripristino di Dart </strong> .</span><span class="sxs-lookup"><span data-stu-id="b8622-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-119">Richiede che qualcuno con accesso al CD o al DVD sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</span><span class="sxs-lookup"><span data-stu-id="b8622-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8622-120">Da un'unità flash USB</span><span class="sxs-lookup"><span data-stu-id="b8622-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-121">Offre gli stessi vantaggi dell'avvio da un CD o DVD e fornisce anche il supporto per i computer che non dispongono di unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="b8622-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-122">È necessario formattare l'unità flash USB prima di poterla usare per l'avvio in DaRT.</span><span class="sxs-lookup"><span data-stu-id="b8622-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="b8622-123">Richiede inoltre che qualcuno con accesso all'unità flash USB sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</span><span class="sxs-lookup"><span data-stu-id="b8622-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8622-124">Da una partizione remota (rete)</span><span class="sxs-lookup"><span data-stu-id="b8622-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-125">Consente di avviare il dardo senza bisogno di un CD, un DVD o un'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="b8622-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="b8622-126">Consente inoltre di aggiornare facilmente le freccette perché è disponibile un solo percorso di file.</span><span class="sxs-lookup"><span data-stu-id="b8622-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-127">Non funziona se il computer dell'utente finale non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="b8622-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="b8622-128">Ampiamente disponibile per gli utenti finali e potrebbe richiedere ulteriori considerazioni sulla sicurezza quando si crea l'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b8622-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8622-129">Da una partizione di ripristino</span><span class="sxs-lookup"><span data-stu-id="b8622-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-130">Consente di avviare il dardo senza bisogno di un CD, un DVD o un'unità flash USB che include istanze in cui non è disponibile una connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="b8622-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="b8622-131">Può inoltre essere implementato e gestito come parte del processo di immagine Windows standard usando strumenti di distribuzione automatici, ad esempio Microsoft endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b8622-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8622-132">Quando si aggiorna il dardo, è necessario aggiornare tutti i computer dell'organizzazione anziché una sola partizione (in rete) o un dispositivo (CD, DVD o memoria flash USB).</span><span class="sxs-lookup"><span data-stu-id="b8622-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b8622-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8622-133">Related topics</span></span>


[<span data-ttu-id="b8622-134">Pianificazione della distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b8622-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





