---
title: Come modificare la configurazione client con PowerShell
description: Come modificare la configurazione client con PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805271"
---
# <span data-ttu-id="a8e53-103">Come modificare la configurazione client con PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8e53-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="a8e53-104">Usare la procedura seguente per configurare la configurazione client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a8e53-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="a8e53-105">Per modificare la configurazione client di App-V 5,0 tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8e53-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="a8e53-106">Per configurare le impostazioni del client tramite PowerShell, usare il cmdlet **set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a8e53-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="a8e53-107">Per modificare la configurazione del client, aprire un prompt dei comandi di PowerShell ed eseguire il cmdlet **set-AppvClientConfiguration** seguente con i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="a8e53-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="a8e53-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a8e53-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="a8e53-109">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="a8e53-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a8e53-110">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a8e53-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a8e53-111">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="a8e53-111">Got an App-V issue?</span></span>** <span data-ttu-id="a8e53-112">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a8e53-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a8e53-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8e53-113">Related topics</span></span>


[<span data-ttu-id="a8e53-114">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a8e53-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





