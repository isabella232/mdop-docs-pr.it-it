---
title: Come determinare lo stato della crittografia BitLocker nei computer smarriti
description: Come determinare lo stato della crittografia BitLocker nei computer smarriti
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824475"
---
# <span data-ttu-id="64fea-103">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="64fea-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="64fea-104">Usare questa procedura con il sito Web amministrazione e monitoraggio per determinare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="64fea-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="64fea-105">Ultimo stato di crittografia noto di BitLocker per i computer persi o rubati</span><span class="sxs-lookup"><span data-stu-id="64fea-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="64fea-106">Se i volumi di un computer smarrito o rubato sono stati crittografati</span><span class="sxs-lookup"><span data-stu-id="64fea-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="64fea-107">Per completare questa attività, è necessario accedere all'area **report** del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="64fea-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="64fea-108">Per accedere a questa area, è necessario che il ruolo utenti del report MBAM venga assegnato.</span><span class="sxs-lookup"><span data-stu-id="64fea-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="64fea-109">Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli.</span><span class="sxs-lookup"><span data-stu-id="64fea-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="64fea-110">Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="64fea-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="64fea-111">**Nota**  La conformità del dispositivo è determinata dai criteri di BitLocker distribuiti dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="64fea-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="64fea-112">Potrebbe essere necessario verificare i criteri distribuiti prima di provare a determinare lo stato di crittografia di BitLocker di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64fea-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="64fea-113">Per determinare l'ultimo stato di crittografia noto di BitLocker per i computer persi</span><span class="sxs-lookup"><span data-stu-id="64fea-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="64fea-114">Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="64fea-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="64fea-115">Nel riquadro sinistro selezionare **report** per aprire la pagina report.</span><span class="sxs-lookup"><span data-stu-id="64fea-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="64fea-116">Selezionare il **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="64fea-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="64fea-117">Usare i campi filtro nel riquadro destro per restringere i risultati della ricerca e quindi fare clic su **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="64fea-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="64fea-118">I risultati vengono visualizzati nella query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="64fea-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="64fea-119">Eseguire l'azione appropriata, come determinato dai criteri per i dispositivi persi.</span><span class="sxs-lookup"><span data-stu-id="64fea-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="64fea-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64fea-120">Related topics</span></span>


[<span data-ttu-id="64fea-121">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="64fea-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="64fea-122">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="64fea-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="64fea-123">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="64fea-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="64fea-124">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="64fea-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





