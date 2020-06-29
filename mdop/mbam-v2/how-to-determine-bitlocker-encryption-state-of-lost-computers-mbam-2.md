---
title: Come determinare lo stato della crittografia BitLocker nei computer smarriti
description: Come determinare lo stato della crittografia BitLocker nei computer smarriti
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824615"
---
# <span data-ttu-id="633d0-103">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="633d0-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="633d0-104">È possibile usare l'amministrazione e il monitoraggio di Microsoft BitLocker per determinare l'ultimo stato di crittografia di BitLocker noto dei computer persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="633d0-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="633d0-105">La procedura seguente spiega come determinare se i volumi in un computer vengono crittografati in caso di perdita o furto.</span><span class="sxs-lookup"><span data-stu-id="633d0-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="633d0-106">Per determinare l'ultimo stato di crittografia noto di BitLocker per i computer persi</span><span class="sxs-lookup"><span data-stu-id="633d0-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="633d0-107">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="633d0-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="633d0-108">**Nota**  Nota: l'indirizzo predefinito per il sito Web di amministrazione e monitoraggio è http://\* &lt; nomecomputer &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="633d0-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="633d0-109">L'uso del nome completo del server consentirà di ottenere risultati di esplorazione più rapidi.</span><span class="sxs-lookup"><span data-stu-id="633d0-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="633d0-110">Seleziona il nodo del **report** dal riquadro di spostamento e seleziona il **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="633d0-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="633d0-111">Usare i campi filtro nel riquadro destro per restringere i risultati della ricerca e quindi fare clic su **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="633d0-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="633d0-112">I risultati vengono visualizzati sotto la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="633d0-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="633d0-113">Eseguire l'azione appropriata, come determinato dai criteri per i dispositivi persi.</span><span class="sxs-lookup"><span data-stu-id="633d0-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="633d0-114">**Nota**  La conformità del dispositivo è determinata dai criteri di BitLocker distribuiti dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="633d0-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="633d0-115">Potrebbe essere necessario verificare i criteri distribuiti prima di provare a determinare lo stato di crittografia di BitLocker di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="633d0-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="633d0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="633d0-116">Related topics</span></span>


[<span data-ttu-id="633d0-117">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="633d0-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





