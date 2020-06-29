---
title: Visualizzazione e configurazione dei log MED-V
description: Visualizzazione e configurazione dei log MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823726"
---
# <span data-ttu-id="a38b8-103">Visualizzazione e configurazione dei log MED-V</span><span class="sxs-lookup"><span data-stu-id="a38b8-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="a38b8-104">Durante la risoluzione dei problemi di MED-V, potrebbe essere utile o necessario accedere ai registri eventi di MED-V.</span><span class="sxs-lookup"><span data-stu-id="a38b8-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="a38b8-105">È possibile aprire il Visualizzatore eventi per il computer host e la macchina virtuale guest tramite il Toolkit di amministrazione MED-V.</span><span class="sxs-lookup"><span data-stu-id="a38b8-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="a38b8-106">È anche possibile usare il Toolkit di amministrazione MED-V per impostare il livello di registrazione in cui i registri eventi MED-V segnalano gli eventi MED-V.</span><span class="sxs-lookup"><span data-stu-id="a38b8-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="a38b8-107">Per informazioni su come aprire il Toolkit di amministrazione MED-V, vedere [risoluzione dei problemi relativi a Med-v tramite Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="a38b8-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="a38b8-108">Visualizzazione dei registri eventi di MED-V</span><span class="sxs-lookup"><span data-stu-id="a38b8-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="a38b8-109">Nella finestra **Toolkit di amministrazione MED-V** fare clic su **eventi host** per aprire il Visualizzatore eventi per il computer host.</span><span class="sxs-lookup"><span data-stu-id="a38b8-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="a38b8-110">In alternativa, fare clic su **eventi Guest** per aprire il Visualizzatore eventi per la macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="a38b8-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="a38b8-111">Il Visualizzatore eventi viene aperto e Visualizza i registri eventi corrispondenti che è possibile usare per risolvere i problemi che possono verificarsi durante la distribuzione o la gestione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="a38b8-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="a38b8-112">Per impostazione predefinita, vengono visualizzati solo gli errori e gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="a38b8-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="a38b8-113">Per altre informazioni su specifici ID evento e messaggi, vedere [messaggi del log eventi di MED-V](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a38b8-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="a38b8-114">**Nota**  Gli utenti finali possono salvare solo i file del log eventi nel Guest se hanno autorizzazioni amministrative.</span><span class="sxs-lookup"><span data-stu-id="a38b8-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="a38b8-115">Per aprire manualmente il Visualizzatore eventi nel computer host</span><span class="sxs-lookup"><span data-stu-id="a38b8-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="a38b8-116">Fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **strumenti di amministrazione**.</span><span class="sxs-lookup"><span data-stu-id="a38b8-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="a38b8-117">Fare doppio clic su **Visualizzatore eventi**e quindi su **registri applicazioni e servizi**.</span><span class="sxs-lookup"><span data-stu-id="a38b8-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="a38b8-118">Fare doppio clic su **MEDV**.</span><span class="sxs-lookup"><span data-stu-id="a38b8-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="a38b8-119">Configurazione dei log eventi di MED-V</span><span class="sxs-lookup"><span data-stu-id="a38b8-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="a38b8-120">Puoi specificare il livello di registrazione eventi MED-V selezionando il pulsante di opzione corrispondente nel Toolkit di amministrazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="a38b8-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="a38b8-121">È possibile decidere se la registrazione degli eventi include solo errori, errori e avvisi o errori, avvisi e messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="a38b8-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="a38b8-122">Il livello di registrazione degli eventi specificato è impostato sia per il computer host che per la macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="a38b8-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="a38b8-123">Puoi anche specificare il livello di registrazione degli eventi modificando il valore del registro di sistema EventLogLevel.</span><span class="sxs-lookup"><span data-stu-id="a38b8-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="a38b8-124">Per altre informazioni, vedere [gestione delle impostazioni di configurazione dell'area di lavoro MED-V](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a38b8-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="a38b8-125">**Nota**  Il livello specificato nella finestra **Toolkit di amministrazione di Med-v** si applica alla registrazione eventi futura di Med-v.</span><span class="sxs-lookup"><span data-stu-id="a38b8-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="a38b8-126">Se si imposta il livello per acquisire tutti gli errori, gli avvisi e i messaggi informativi, i log eventi si riempiono più rapidamente e gli eventi meno recenti vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="a38b8-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="a38b8-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a38b8-127">Related topics</span></span>


[<span data-ttu-id="a38b8-128">Riavvio e ripristino di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="a38b8-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="a38b8-129">Visualizzazione delle configurazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="a38b8-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





