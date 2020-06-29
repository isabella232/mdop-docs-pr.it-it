---
title: Report sull'uso del sistema
description: Report sull'uso del sistema
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815255"
---
# <span data-ttu-id="da686-103">Report sull'uso del sistema</span><span class="sxs-lookup"><span data-stu-id="da686-103">System Utilization Report</span></span>


<span data-ttu-id="da686-104">Usare il report utilizzo sistema per rappresentare il grafico dell'utilizzo totale del sistema giornaliero.</span><span class="sxs-lookup"><span data-stu-id="da686-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="da686-105">Puoi usare questo report per determinare il carico nel sistema di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="da686-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="da686-106">Questo report rileva l'utilizzo nel tempo durante il periodo di riferimento per il server specificato o per il gruppo di server.</span><span class="sxs-lookup"><span data-stu-id="da686-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="da686-107">Il report utilizzo sistema rappresenta anche il seguente utilizzo del sistema:</span><span class="sxs-lookup"><span data-stu-id="da686-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="da686-108">Utilizzo per giorno della settimana</span><span class="sxs-lookup"><span data-stu-id="da686-108">Usage by day of the week</span></span>

-   <span data-ttu-id="da686-109">Utilizzo per ora del giorno</span><span class="sxs-lookup"><span data-stu-id="da686-109">Usage by hour of the day</span></span>

<span data-ttu-id="da686-110">Il report utilizzo sistema include anche un riepilogo dell'utilizzo totale del sistema per gli utenti specifici e per i conteggi totali delle sessioni.</span><span class="sxs-lookup"><span data-stu-id="da686-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="da686-111">Quando si crea un report, è necessario specificare i parametri usati per raccogliere i dati quando il report viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da686-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="da686-112">I report non vengono eseguiti automaticamente; è necessario eseguirli in modo esplicito per generare i dati di output.</span><span class="sxs-lookup"><span data-stu-id="da686-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="da686-113">Il periodo di tempo necessario per l'esecuzione del report è determinato dalla quantità di dati raccolti nell'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="da686-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="da686-114">Dopo l'esecuzione di un report e l'output visualizzato nella console di gestione di Application Virtualization Server, è possibile esportare il report nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="da686-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="da686-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="da686-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="da686-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="da686-116">Microsoft Office Excel</span></span>

<span data-ttu-id="da686-117">**Nota**  Il nome dell'App-V Server segnalato dai client deve far parte del gruppo predefinito del server in modo che il report di utilizzo del sistema visualizzi i dati.</span><span class="sxs-lookup"><span data-stu-id="da686-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="da686-118">Se ad esempio si usano più server con un bilanciamento del carico di rete (NLB), è necessario aggiungere il nome del cluster NLB al gruppo di server predefinito.</span><span class="sxs-lookup"><span data-stu-id="da686-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="da686-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da686-119">Related topics</span></span>


[<span data-ttu-id="da686-120">Come creare un report</span><span class="sxs-lookup"><span data-stu-id="da686-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="da686-121">Come eliminare un report</span><span class="sxs-lookup"><span data-stu-id="da686-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="da686-122">Come esportare un report</span><span class="sxs-lookup"><span data-stu-id="da686-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="da686-123">Come stampare un report</span><span class="sxs-lookup"><span data-stu-id="da686-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="da686-124">Come eseguire un report</span><span class="sxs-lookup"><span data-stu-id="da686-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





