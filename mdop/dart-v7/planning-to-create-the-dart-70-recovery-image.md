---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821335"
---
# <span data-ttu-id="cc8d4-103">Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="cc8d4-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="cc8d4-104">Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="cc8d4-105">Pianificazione della creazione dell'immagine di ripristino di DaRT 7</span><span class="sxs-lookup"><span data-stu-id="cc8d4-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="cc8d4-106">Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="cc8d4-107">Quando si decide, tenere presente che gli utenti finali potrebbero avere accesso occasionalmente ai vari strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="cc8d4-108">Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti di dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d4-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="cc8d4-109">Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per DaRT 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d4-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="cc8d4-110">Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="cc8d4-111">Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="cc8d4-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="cc8d4-112">Prerequisites</span></span>


<span data-ttu-id="cc8d4-113">Gli elementi seguenti sono obbligatori o consigliati per creare l'immagine di ripristino DaRT:</span><span class="sxs-lookup"><span data-stu-id="cc8d4-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="cc8d4-114">File di origine di Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc8d4-114">Windows 7 source files</span></span>

    <span data-ttu-id="cc8d4-115">Devi specificare il percorso di un DVD di Windows 7 o di file di origine di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="cc8d4-116">I file di origine di Windows 7 sono necessari per creare l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="cc8d4-117">Strumenti di debug di Windows per la tua piattaforma</span><span class="sxs-lookup"><span data-stu-id="cc8d4-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="cc8d4-118">Gli strumenti di debug di Windows sono necessari quando si esegue **analizzatore crash** per determinare la causa di un arresto anomalo del computer.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="cc8d4-119">Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="cc8d4-120">Se necessario, è possibile scaricare gli strumenti di debug di Windows qui: [scaricare e installare gli strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="cc8d4-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="cc8d4-121">Facoltativo: definizioni di **Sweep System autonome**</span><span class="sxs-lookup"><span data-stu-id="cc8d4-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="cc8d4-122">Quando si esegue questo strumento, sono necessarie le definizioni più recenti per la **spazzatrice di sistema autonoma** .</span><span class="sxs-lookup"><span data-stu-id="cc8d4-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="cc8d4-123">Anche se è possibile scaricare le definizioni quando si esegue una **spazzatrice di sistema autonoma**, è consigliabile scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="cc8d4-124">In questo modo, è comunque possibile eseguire lo strumento con le definizioni più recenti anche se il computer problema non ha connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="cc8d4-125">Facoltativo: file di simboli Windows da usare con **Crash Analyzer**</span><span class="sxs-lookup"><span data-stu-id="cc8d4-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="cc8d4-126">In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="cc8d4-127">È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="cc8d4-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="cc8d4-128">Per altre informazioni, vedere [diagnostica degli errori di sistema con Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d4-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="cc8d4-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc8d4-129">Related topics</span></span>


[<span data-ttu-id="cc8d4-130">Pianificazione della distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="cc8d4-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





