---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824806"
---
# <span data-ttu-id="a15ed-103">Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a15ed-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="a15ed-104">Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="a15ed-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="a15ed-105">Pianificazione della creazione dell'immagine di ripristino di DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="a15ed-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="a15ed-106">Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="a15ed-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="a15ed-107">Per prendere la decisione, considera che gli utenti finali possono avere accesso a questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="a15ed-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="a15ed-108">Se i tecnici del supporto accettano il supporto di immagini di ripristino per consentire ai computer degli utenti di diagnosticare i problemi, è consigliabile installare tutti gli strumenti nell'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a15ed-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="a15ed-109">Se si prevede di diagnosticare i computer degli utenti finali in remoto, è consigliabile disabilitare alcuni degli strumenti, ad esempio la cancellazione del disco e l'editor del registro di sistema, e quindi abilitare altri strumenti, inclusa la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="a15ed-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="a15ed-110">Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file.</span><span class="sxs-lookup"><span data-stu-id="a15ed-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="a15ed-111">Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="a15ed-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="a15ed-112">Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti di dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a15ed-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="a15ed-113">Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per DaRT 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a15ed-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="a15ed-114">Prerequisiti per l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="a15ed-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="a15ed-115">Gli elementi seguenti sono obbligatori o consigliati per creare l'immagine di ripristino DaRT:</span><span class="sxs-lookup"><span data-stu-id="a15ed-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a15ed-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a15ed-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a15ed-117">Dettagli</span><span class="sxs-lookup"><span data-stu-id="a15ed-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a15ed-118">File di origine di Windows 8</span><span class="sxs-lookup"><span data-stu-id="a15ed-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="a15ed-119">Necessario per creare l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="a15ed-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="a15ed-120">Fornisci il percorso di un DVD di Windows 8 o di file di origine di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a15ed-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a15ed-121">Strumenti di debug di Windows per la tua piattaforma</span><span class="sxs-lookup"><span data-stu-id="a15ed-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="a15ed-122">Obbligatorio quando si esegue l' <strong> analizzatore crash </strong> per determinare la causa di un errore del computer.</span><span class="sxs-lookup"><span data-stu-id="a15ed-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="a15ed-123">Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="a15ed-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="a15ed-124">Puoi scaricare gli strumenti di debug di Windows qui: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> scaricare e installare gli strumenti di debug per Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="a15ed-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a15ed-125">Facoltativo: <strong> </strong> definizioni Defender</span><span class="sxs-lookup"><span data-stu-id="a15ed-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a15ed-126">Le definizioni più recenti per <strong> Defender </strong> sono necessarie quando si esegue <strong> Defender </strong> .</span><span class="sxs-lookup"><span data-stu-id="a15ed-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="a15ed-127">Anche se è possibile scaricare le definizioni durante l'esecuzione di <strong> Defender </strong> , è consigliabile scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino delle freccette in modo da poter eseguire lo strumento con le definizioni più recenti anche se il computer problema non ha connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="a15ed-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a15ed-128">Facoltativo: file di simboli Windows da usare con <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="a15ed-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a15ed-129">In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a15ed-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="a15ed-130">È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se ha smesso di funzionare.</span><span class="sxs-lookup"><span data-stu-id="a15ed-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="a15ed-131">Per altre informazioni, vedere <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnostica degli errori di sistema con Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="a15ed-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a15ed-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a15ed-132">Related topics</span></span>


[<span data-ttu-id="a15ed-133">Pianificazione della distribuzione di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a15ed-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





