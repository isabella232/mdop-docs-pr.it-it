---
title: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822666"
---
# <span data-ttu-id="886fb-103">Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="886fb-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="886fb-104">Per eseguire l' **analizzatore crash** dalla finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale in cui si verificano problemi, è necessario che siano installati gli strumenti di debug Microsoft per Windows e i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="886fb-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="886fb-105">Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="886fb-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="886fb-106">Per eseguire l'analizzatore crash in un computer dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="886fb-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="886fb-107">Nella finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale, fare clic su **analizzatore crash**.</span><span class="sxs-lookup"><span data-stu-id="886fb-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="886fb-108">Fornisci le informazioni necessarie per gli strumenti di debug Microsoft per Windows.</span><span class="sxs-lookup"><span data-stu-id="886fb-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="886fb-109">Fornisci le informazioni necessarie per i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="886fb-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="886fb-110">Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="886fb-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span></span>

4.  <span data-ttu-id="886fb-111">Fornisci le informazioni necessarie per un file di dump della memoria.</span><span class="sxs-lookup"><span data-stu-id="886fb-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="886fb-112">Per determinare la posizione del file di dump della memoria:</span><span class="sxs-lookup"><span data-stu-id="886fb-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="886fb-113">Aprire la finestra delle **proprietà del sistema** .</span><span class="sxs-lookup"><span data-stu-id="886fb-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="886fb-114">Fare clic sul pulsante **Start**, digitare **sysdm.cpl**e quindi premere **invio**.</span><span class="sxs-lookup"><span data-stu-id="886fb-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="886fb-115">Fai clic sulla scheda **Avanzate**.</span><span class="sxs-lookup"><span data-stu-id="886fb-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="886fb-116">Nell'area di **avvio e ripristino** fare clic su **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="886fb-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="886fb-117">Se non si ha accesso alla finestra delle **proprietà del sistema** , è possibile cercare i file di dump nel computer dell'utente finale usando lo strumento di **ricerca** in Microsoft Diagnostics and Recovery Toolset (DART) 10.</span><span class="sxs-lookup"><span data-stu-id="886fb-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

    <span data-ttu-id="886fb-118">L' **analizzatore crash** analizza il file di dump della memoria e segnala una causa probabile del problema.</span><span class="sxs-lookup"><span data-stu-id="886fb-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="886fb-119">È possibile visualizzare altre informazioni sull'errore, ad esempio il messaggio di dump della memoria specifico e la descrizione, i driver caricati al momento dell'errore e l'output completo dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="886fb-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="886fb-120">Identificare la strategia appropriata per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="886fb-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="886fb-121">La strategia può richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'errore usando il nodo **Servizi e driver** dello strumento **Gestione computer** in DART 10.</span><span class="sxs-lookup"><span data-stu-id="886fb-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 10.</span></span>

## <span data-ttu-id="886fb-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="886fb-122">Related topics</span></span>


[<span data-ttu-id="886fb-123">Diagnosi degli errori di sistema con Analizzatore di arresti anomali</span><span class="sxs-lookup"><span data-stu-id="886fb-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="886fb-124">Operazioni relative a DaRT 10</span><span class="sxs-lookup"><span data-stu-id="886fb-124">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





