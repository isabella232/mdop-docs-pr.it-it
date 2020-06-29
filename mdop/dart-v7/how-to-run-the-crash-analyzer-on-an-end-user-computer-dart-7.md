---
title: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823836"
---
# <span data-ttu-id="f032f-103">Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="f032f-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="f032f-104">In genere, viene eseguito Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer dalla finestra del set di strumenti di diagnostica e ripristino in un computer dell'utente finale che presenta problemi.</span><span class="sxs-lookup"><span data-stu-id="f032f-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="f032f-105">L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema.</span><span class="sxs-lookup"><span data-stu-id="f032f-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="f032f-106">Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f032f-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="f032f-107">Devi anche specificare il percorso in cui si trovano i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="f032f-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="f032f-108">Per aprire ed eseguire l'analizzatore crash in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="f032f-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="f032f-109">Nella finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale, fare clic su **analizzatore crash**.</span><span class="sxs-lookup"><span data-stu-id="f032f-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="f032f-110">Specificare le informazioni necessarie per le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f032f-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="f032f-111">Strumenti di debug Microsoft per Windows</span><span class="sxs-lookup"><span data-stu-id="f032f-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="f032f-112">File di simboli</span><span class="sxs-lookup"><span data-stu-id="f032f-112">Symbol files</span></span>

        <span data-ttu-id="f032f-113">Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f032f-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="f032f-114">Un file di dump di arresto anomalo</span><span class="sxs-lookup"><span data-stu-id="f032f-114">A crash dump file</span></span>

        <span data-ttu-id="f032f-115">Seguire questa procedura per determinare la posizione del file di dump dell'arresto anomalo:</span><span class="sxs-lookup"><span data-stu-id="f032f-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="f032f-116">Aprire la finestra delle **proprietà del sistema** .</span><span class="sxs-lookup"><span data-stu-id="f032f-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="f032f-117">Fare clic sul pulsante **Start**, digitare sysdm.cpl e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="f032f-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="f032f-118">Fai clic sulla scheda **Avanzate**.</span><span class="sxs-lookup"><span data-stu-id="f032f-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="f032f-119">Nell'area di **avvio e ripristino** fare clic su **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="f032f-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="f032f-120">**Nota**  Se non si ha accesso alla finestra delle **proprietà del sistema** , è possibile cercare i file di dump nel computer dell'utente finale usando lo strumento di **ricerca** in DART.</span><span class="sxs-lookup"><span data-stu-id="f032f-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="f032f-121">L' **analizzatore crash** analizza il file di dump di arresto anomalo e segnala una causa probabile dell'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="f032f-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="f032f-122">È possibile visualizzare altre informazioni sull'arresto anomalo, ad esempio il messaggio di arresto anomalo specifico e la descrizione, i driver caricati al momento dell'arresto anomalo e l'output completo dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="f032f-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="f032f-123">Decidere su una strategia appropriata per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="f032f-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="f032f-124">Questo potrebbe richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'arresto anomalo usando il nodo **Servizi e driver** dello strumento **Gestione computer** in DART.</span><span class="sxs-lookup"><span data-stu-id="f032f-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="f032f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f032f-125">Related topics</span></span>


[<span data-ttu-id="f032f-126">Diagnosi degli errori di sistema con Analizzatore di arresti anomali</span><span class="sxs-lookup"><span data-stu-id="f032f-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





