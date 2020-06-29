---
title: Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822786"
---
# <span data-ttu-id="13acc-103">Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="13acc-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="13acc-104">Se non è possibile accedere agli strumenti di debug Microsoft per Windows o ai file di simboli nel computer dell'utente finale, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di Crash Analyzer, ad esempio un computer dell'amministratore dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="13acc-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="13acc-105">Per eseguire l'analizzatore crash in modalità autonoma</span><span class="sxs-lookup"><span data-stu-id="13acc-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="13acc-106">In un computer in cui è installato DaRT7, fare clic su **Avvia**  /  **tutti i programmi**  /  **Microsoft DaRT 7**.</span><span class="sxs-lookup"><span data-stu-id="13acc-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="13acc-107">Specificare le informazioni necessarie per le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="13acc-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="13acc-108">Strumenti di debug Microsoft per Windows</span><span class="sxs-lookup"><span data-stu-id="13acc-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="13acc-109">File di simboli</span><span class="sxs-lookup"><span data-stu-id="13acc-109">Symbol files</span></span>

        <span data-ttu-id="13acc-110">Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="13acc-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="13acc-111">Un file di dump di arresto anomalo</span><span class="sxs-lookup"><span data-stu-id="13acc-111">A crash dump file</span></span>

        <span data-ttu-id="13acc-112">**Nota**  Usare lo strumento di ricerca in DaRT7 per individuare il file di dump dell'arresto anomalo copiato.</span><span class="sxs-lookup"><span data-stu-id="13acc-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="13acc-113">L' **analizzatore crash** analizza il file di dump di arresto anomalo e segnala una causa probabile dell'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="13acc-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="13acc-114">È possibile visualizzare altre informazioni sull'arresto anomalo, ad esempio il messaggio di arresto anomalo specifico e la descrizione, i driver caricati al momento dell'arresto anomalo e l'output completo dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="13acc-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="13acc-115">Decidere su una strategia appropriata per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="13acc-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="13acc-116">Questo potrebbe richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'arresto anomalo usando il nodo **Servizi e driver** dello strumento **Gestione computer** in DART.</span><span class="sxs-lookup"><span data-stu-id="13acc-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="13acc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13acc-117">Related topics</span></span>


[<span data-ttu-id="13acc-118">Diagnosi degli errori di sistema con Analizzatore di arresti anomali</span><span class="sxs-lookup"><span data-stu-id="13acc-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





