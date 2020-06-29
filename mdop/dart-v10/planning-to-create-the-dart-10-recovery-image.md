---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 10
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822976"
---
# <span data-ttu-id="87388-103">Pianificazione per la creazione dell'immagine di ripristino di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="87388-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="87388-104">Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="87388-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="87388-105">Pianificazione della creazione dell'immagine di ripristino di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="87388-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="87388-106">Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="87388-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="87388-107">Per prendere la decisione, considera che gli utenti finali possono avere accesso a questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="87388-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="87388-108">Se i tecnici del supporto accettano il supporto di immagini di ripristino per consentire ai computer degli utenti di diagnosticare i problemi, è consigliabile installare tutti gli strumenti nell'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="87388-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="87388-109">Se si prevede di diagnosticare i computer degli utenti finali in remoto, è consigliabile disabilitare alcuni degli strumenti, ad esempio la cancellazione del disco e l'editor del registro di sistema, e quindi abilitare altri strumenti, inclusa la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="87388-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="87388-110">Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file.</span><span class="sxs-lookup"><span data-stu-id="87388-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="87388-111">Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="87388-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="87388-112">Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="87388-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="87388-113">Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per Dart 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="87388-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="87388-114">Prerequisiti per l'immagine di ripristino</span><span class="sxs-lookup"><span data-stu-id="87388-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="87388-115">Gli elementi seguenti sono obbligatori o consigliati per creare l'immagine di ripristino DaRT:</span><span class="sxs-lookup"><span data-stu-id="87388-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="87388-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="87388-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="87388-117">Dettagli</span><span class="sxs-lookup"><span data-stu-id="87388-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87388-118">File di origine di Windows 10</span><span class="sxs-lookup"><span data-stu-id="87388-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="87388-119">Necessario per creare l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="87388-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="87388-120">Fornisci il percorso di un DVD di Windows 10 o di file di origine Windows 10.</span><span class="sxs-lookup"><span data-stu-id="87388-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87388-121">Strumenti di debug di Windows per la tua piattaforma</span><span class="sxs-lookup"><span data-stu-id="87388-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="87388-122">Obbligatorio quando si esegue l' <strong> analizzatore crash </strong> per determinare la causa di un errore del computer.</span><span class="sxs-lookup"><span data-stu-id="87388-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="87388-123">Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="87388-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="87388-124">Puoi scaricare gli strumenti di debug di Windows qui: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> scaricare e installare gli strumenti di debug per Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="87388-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87388-125">Facoltativo: file di simboli Windows da usare con <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="87388-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87388-126">In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="87388-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="87388-127">È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se ha smesso di funzionare.</span><span class="sxs-lookup"><span data-stu-id="87388-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="87388-128">Per altre informazioni, vedere <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnostica degli errori di sistema con Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="87388-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87388-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87388-129">Related topics</span></span>

[<span data-ttu-id="87388-130">Pianificazione della distribuzione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="87388-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




