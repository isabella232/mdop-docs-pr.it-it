---
title: Come modificare la configurazione client con PowerShell
description: Come modificare la configurazione client con PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805259"
---
# <span data-ttu-id="6a475-103">Come modificare la configurazione client con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a475-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="6a475-104">Usare la procedura seguente per configurare la configurazione client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a475-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="6a475-105">Per modificare la configurazione client di App-V 5,1 tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a475-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="6a475-106">Per configurare le impostazioni del client tramite PowerShell, usare il cmdlet **set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6a475-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="6a475-107">Per altre informazioni sull'installazione di PowerShell e un elenco di cmdlet, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span><span class="sxs-lookup"><span data-stu-id="6a475-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="6a475-108">Per modificare la configurazione del client, aprire un prompt dei comandi di PowerShell ed eseguire il cmdlet **set-AppvClientConfiguration** seguente con i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="6a475-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="6a475-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6a475-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="6a475-110">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="6a475-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6a475-111">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6a475-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6a475-112">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="6a475-112">Got an App-V issue?</span></span>** <span data-ttu-id="6a475-113">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6a475-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6a475-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a475-114">Related topics</span></span>


[<span data-ttu-id="6a475-115">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6a475-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





