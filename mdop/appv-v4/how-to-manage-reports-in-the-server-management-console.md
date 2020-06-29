---
title: Come gestire i report in Server Management Console
description: Come gestire i report in Server Management Console
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817145"
---
# <span data-ttu-id="a1645-103">Come gestire i report in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="a1645-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="a1645-104">Per gestire in modo efficace il sistema di virtualizzazione delle applicazioni, è possibile usare la console di gestione server Application Virtualization per generare una vasta gamma di report che contengono informazioni sul sistema.</span><span class="sxs-lookup"><span data-stu-id="a1645-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="a1645-105">Queste informazioni includono informazioni sull'uso giornaliero per un'applicazione specifica o per tutte le applicazioni e la verifica degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="a1645-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="a1645-106">Nota</span><span class="sxs-lookup"><span data-stu-id="a1645-106">Note</span></span>**  
-   <span data-ttu-id="a1645-107">Durante l'installazione, lo script di installazione installa solo la versione in lingua inglese del Visualizzatore di report.</span><span class="sxs-lookup"><span data-stu-id="a1645-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="a1645-108">Affinché il Visualizzatore report visualizzi le informazioni corrette in altre lingue, è necessario installare un Language Pack dalla posizione seguente: <https://go.microsoft.com/fwlink/?LinkId=131645> .</span><span class="sxs-lookup"><span data-stu-id="a1645-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="a1645-109">Quando si aggiunge o si modifica un'applicazione nella console di gestione server, è necessario assicurarsi che i nomi e le versioni delle applicazioni corrispondano esattamente a quelli presenti nei file OSD.</span><span class="sxs-lookup"><span data-stu-id="a1645-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="a1645-110">La caratteristica Creazione di report USA i campi dei dati delle versioni e dei nomi delle applicazioni quando identifica i dati sull'utilizzo delle applicazioni su cui segnalare.</span><span class="sxs-lookup"><span data-stu-id="a1645-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="a1645-111">Se i campi dati non corrispondono, i record di utilizzo verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="a1645-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="a1645-112">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="a1645-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="a1645-113">Tipi di report di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="a1645-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="a1645-114">Contiene informazioni sui tipi di report disponibili.</span><span class="sxs-lookup"><span data-stu-id="a1645-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="a1645-115">Come creare un report</span><span class="sxs-lookup"><span data-stu-id="a1645-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="a1645-116">Fornisce una procedura dettagliata per la creazione di un report.</span><span class="sxs-lookup"><span data-stu-id="a1645-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="a1645-117">Come eseguire un report</span><span class="sxs-lookup"><span data-stu-id="a1645-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="a1645-118">Viene fornito un processo dettagliato per l'esecuzione di un report.</span><span class="sxs-lookup"><span data-stu-id="a1645-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="a1645-119">Come stampare un report</span><span class="sxs-lookup"><span data-stu-id="a1645-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="a1645-120">Fornisce una procedura dettagliata per la stampa di un report.</span><span class="sxs-lookup"><span data-stu-id="a1645-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="a1645-121">Come esportare un report</span><span class="sxs-lookup"><span data-stu-id="a1645-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="a1645-122">Fornisce una procedura dettagliata per l'esportazione di un report.</span><span class="sxs-lookup"><span data-stu-id="a1645-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="a1645-123">Come eliminare un report</span><span class="sxs-lookup"><span data-stu-id="a1645-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="a1645-124">Fornisce una procedura dettagliata per l'eliminazione di un report.</span><span class="sxs-lookup"><span data-stu-id="a1645-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="a1645-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1645-125">Related topics</span></span>


[<span data-ttu-id="a1645-126">Report di utilizzo dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a1645-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="a1645-127">Come eseguire attività amministrative in Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="a1645-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="a1645-128">Report sul controllo del software</span><span class="sxs-lookup"><span data-stu-id="a1645-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="a1645-129">Report sugli errori di sistema</span><span class="sxs-lookup"><span data-stu-id="a1645-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="a1645-130">Report sull'uso del sistema</span><span class="sxs-lookup"><span data-stu-id="a1645-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





