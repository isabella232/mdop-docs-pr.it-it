---
title: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
description: Diagnosi degli errori di sistema con Analizzatore di arresti anomali
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823466"
---
# <span data-ttu-id="0561a-103">Diagnosi degli errori di sistema con Analizzatore di arresti anomali</span><span class="sxs-lookup"><span data-stu-id="0561a-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="0561a-104">L'analizzatore crash in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 consente di eseguire il debug di un file di dump di arresto anomalo in un computer basato su Windows e quindi di diagnosticare gli eventuali errori relativi al computer.</span><span class="sxs-lookup"><span data-stu-id="0561a-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="0561a-105">L'analizzatore crash usa gli strumenti di debug Microsoft per Windows per esaminare un file di dump di arresto anomalo per il driver che ha causato il failover del computer.</span><span class="sxs-lookup"><span data-stu-id="0561a-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="0561a-106">Eseguire l'analizzatore crash in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="0561a-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="0561a-107">In genere, l'analizzatore crash viene eseguito dalla finestra del set di strumenti di diagnostica e ripristino in un computer dell'utente finale che presenta problemi.</span><span class="sxs-lookup"><span data-stu-id="0561a-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="0561a-108">L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="0561a-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="0561a-109">Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0561a-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="0561a-110">Devi anche specificare il percorso in cui si trovano i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="0561a-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="0561a-111">Se sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di DaRT, dovrebbero essere disponibili quando si esegue l'analizzatore crash nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="0561a-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="0561a-112">Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="0561a-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="0561a-113">Eseguire l'analizzatore crash in modalità autonoma in un computer diverso da un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="0561a-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="0561a-114">L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="0561a-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="0561a-115">Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0561a-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="0561a-116">Devi anche specificare il percorso in cui si trovano i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="0561a-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="0561a-117">Se non sono stati inclusi gli strumenti di debug Microsoft per Windows e i file di simboli quando è stata creata l'immagine di ripristino di freccette o se i problemi di connettività di rete o le dimensioni del disco impediscono di ottenerli, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di analizzatore crash. , ad esempio un computer dell'amministratore dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="0561a-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="0561a-118">Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="0561a-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="0561a-119">Verificare che Crash Analyzer possa accedere ai file di simboli</span><span class="sxs-lookup"><span data-stu-id="0561a-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="0561a-120">In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0561a-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="0561a-121">È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="0561a-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="0561a-122">I file di simboli vengono scaricati automaticamente quando si esegue analizzatore crash.</span><span class="sxs-lookup"><span data-stu-id="0561a-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="0561a-123">Se il computer non dispone di una connessione Internet o se la rete richiede che il computer acceda a un server proxy HTTP, non è possibile scaricare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="0561a-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="0561a-124">Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli</span><span class="sxs-lookup"><span data-stu-id="0561a-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="0561a-125">Altre risorse per la diagnosi degli errori di sistema con Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="0561a-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="0561a-126">Operazioni relative a DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="0561a-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





