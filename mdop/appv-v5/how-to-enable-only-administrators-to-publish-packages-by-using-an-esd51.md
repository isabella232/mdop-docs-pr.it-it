---
title: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
description: Come consentire solo agli amministratori di pubblicare i pacchetti con ESD
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805469"
---
# <span data-ttu-id="05795-103">Come consentire solo agli amministratori di pubblicare i pacchetti con ESD</span><span class="sxs-lookup"><span data-stu-id="05795-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="05795-104">A partire da App-V 5,0 SP3 puoi configurare il client App-V in modo che solo gli amministratori (non gli utenti finali) possano pubblicare o annullare la pubblicazione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="05795-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="05795-105">Nelle versioni precedenti di App-V non è stato possibile impedire agli utenti finali di eseguire queste attività.</span><span class="sxs-lookup"><span data-stu-id="05795-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="05795-106">Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="05795-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="05795-107">Passare al nodo oggetto Criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="05795-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="05795-108">**Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="05795-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="05795-109">Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .</span><span class="sxs-lookup"><span data-stu-id="05795-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="05795-110">Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,1 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="05795-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="05795-111">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="05795-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="05795-112">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="05795-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="05795-113">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="05795-113">Got an App-V issue?</span></span>** <span data-ttu-id="05795-114">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="05795-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





