---
title: Come gestire la cache del client App-V con i contatori delle prestazioni
description: Come gestire la cache del client App-V con i contatori delle prestazioni
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817135"
---
# <span data-ttu-id="b1d8f-103">Come gestire la cache del client App-V con i contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="b1d8f-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="b1d8f-104">È possibile usare la procedura seguente per determinare la quantità di spazio disponibile nella cache client Application Virtualization (App-V) usando Performance Monitor per visualizzare le informazioni graficamente.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="b1d8f-105">Queste informazioni vengono acquisite nel computer client da un contatore delle prestazioni denominato "App Virt client cache", che include i seguenti contatori: "dimensione cache (MB)," "cache spazio disponibile (MB)," e "% spazio libero".</span><span class="sxs-lookup"><span data-stu-id="b1d8f-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="b1d8f-106">Per determinare l'utilizzo dello spazio della cache client</span><span class="sxs-lookup"><span data-stu-id="b1d8f-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="b1d8f-107">Aprire un prompt dei comandi come amministratore oppure fare clic su **Start**, **esegui**, digitare **perfmon.exe**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="b1d8f-108">A seconda del sistema operativo Windows in uso, fare clic sullo strumento Monitoraggio prestazioni o monitor di sistema dopo l'apertura della finestra di MMC.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="b1d8f-109">Per aggiungere contatori, fare clic con il pulsante destro del mouse sull'area del grafico e scegliere **Aggiungi contatori**.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="b1d8f-110">Fare clic sul menu a discesa per visualizzare l'elenco dei contatori disponibili, scorrere fino a individuare l' **App Virt client cache**e quindi aggiungere i tre contatori.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="b1d8f-111">**Importante**  I contatori delle prestazioni di App-V vengono implementati in una DLL a 32 bit, quindi per vederli è necessario usare il comando seguente per avviare la versione a 32 bit di performance monitor: **MMC/32 perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="b1d8f-112">Questo comando deve essere eseguito direttamente nel computer monitorato e non può essere usato per monitorare un computer remoto che esegue un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b1d8f-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="b1d8f-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1d8f-113">Related topics</span></span>


[<span data-ttu-id="b1d8f-114">Come gestire le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="b1d8f-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





