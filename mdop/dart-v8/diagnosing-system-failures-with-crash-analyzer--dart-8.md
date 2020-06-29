---
title: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
description: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824545"
---
# <span data-ttu-id="ea556-103">Diagnosi degli errori di sistema con Analizzatore di arresti anomali</span><span class="sxs-lookup"><span data-stu-id="ea556-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="ea556-104">L' **analizzatore crash** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 consente di eseguire il debug di un file di dump della memoria in un computer basato su Windows e quindi di diagnosticare gli eventuali errori del computer correlati.</span><span class="sxs-lookup"><span data-stu-id="ea556-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="ea556-105">L' **analizzatore crash** usa gli strumenti di debug Microsoft per Windows per esaminare un file di dump della memoria per il driver che ha causato il failover del computer.</span><span class="sxs-lookup"><span data-stu-id="ea556-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="ea556-106">È possibile eseguire l'analizzatore crash in un computer dell'utente finale o in modalità autonoma in un computer diverso da un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="ea556-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="ea556-107">Eseguire l'analizzatore crash in un computer con utenti finali</span><span class="sxs-lookup"><span data-stu-id="ea556-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="ea556-108">In genere, l' **analizzatore crash** viene eseguito dalla finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale che sta verificando il problema.</span><span class="sxs-lookup"><span data-stu-id="ea556-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="ea556-109">L' **analizzatore crash** cerca di individuare gli strumenti di debug per Windows nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="ea556-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="ea556-110">Se la finestra di dialogo percorso directory è vuota, è necessario immettere il percorso o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ea556-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="ea556-111">Devi anche specificare il percorso in cui si trovano i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="ea556-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="ea556-112">Se sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di DaRT 8,0, gli strumenti e i file di simboli dovrebbero essere disponibili quando si esegue l' **analizzatore crash** nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="ea556-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="ea556-113">Se non sono stati inclusi nell'immagine di ripristino di freccette o se le dimensioni del disco o i problemi di connettività di rete impediscono di ottenerli, in alternativa è possibile eseguire l'analizzatore crash in modalità autonoma in un computer diverso dal computer dell'utente finale, come descritto nella sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="ea556-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="ea556-114">Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="ea556-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="ea556-115">Eseguire l'analizzatore crash in modalità autonoma in un computer diverso da un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="ea556-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="ea556-116">Anche se in genere si esegue l' **analizzatore crash** nel computer dell'utente finale che sta verificando il problema, è anche possibile eseguire l'analizzatore crash in modalità autonoma, in un computer diverso da un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="ea556-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="ea556-117">Potresti scegliere questa opzione se non hai incluso gli strumenti di debug di Windows nell'immagine di ripristino DaRT o se i problemi di connettività di rete o di dimensione del disco impediscono l'ottenimento degli strumenti di debug.</span><span class="sxs-lookup"><span data-stu-id="ea556-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="ea556-118">In questo caso, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di **Crash Analyzer** , ad esempio nel computer dell'agente del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="ea556-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="ea556-119">Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="ea556-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="ea556-120">Come assicurarsi che l'analizzatore crash possa accedere ai file di simboli</span><span class="sxs-lookup"><span data-stu-id="ea556-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="ea556-121">Per eseguire il debug delle applicazioni che hanno smesso di rispondere, è necessario accedere al file di simboli, che è separato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ea556-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="ea556-122">Anche se i file di simboli vengono scaricati automaticamente quando si esegue l'analizzatore di crash, potrebbe verificarsi un periodo in cui il computer problema non ha accesso a Internet.</span><span class="sxs-lookup"><span data-stu-id="ea556-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="ea556-123">Esistono diversi modi per assicurarti di avere accesso garantito ai file di simboli.</span><span class="sxs-lookup"><span data-stu-id="ea556-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="ea556-124">Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli</span><span class="sxs-lookup"><span data-stu-id="ea556-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="ea556-125">Altre risorse per la diagnosi degli errori di sistema con Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="ea556-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="ea556-126">Operazioni relative a DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="ea556-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





