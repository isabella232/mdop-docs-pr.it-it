---
title: Come determinare lo stato di crittografia BitLocker nei computer smarriti
description: Come determinare lo stato di crittografia BitLocker nei computer smarriti
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824295"
---
# <span data-ttu-id="33eec-103">Come determinare lo stato di crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="33eec-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="33eec-104">Microsoft BitLocker Administration and Monitoring (MBAM) consente di determinare l'ultimo stato di crittografia di BitLocker noto dei computer persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="33eec-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="33eec-105">Usare la procedura seguente per determinare se i volumi sono stati crittografati in computer non più in possesso.</span><span class="sxs-lookup"><span data-stu-id="33eec-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="33eec-106">Determinare lo stato di crittografia ultimo noto di un computer</span><span class="sxs-lookup"><span data-stu-id="33eec-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="33eec-107">Aprire il sito Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="33eec-107">Open the MBAM website.</span></span>

    <span data-ttu-id="33eec-108">**Nota**  L'indirizzo predefinito per il sito Web di MBAM è http://\* &lt; nomecomputer &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="33eec-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="33eec-109">Usare il nome completo del server per ottenere risultati di esplorazione più rapidi.</span><span class="sxs-lookup"><span data-stu-id="33eec-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="33eec-110">Selezionare il nodo del **report** nel riquadro di spostamento e quindi selezionare il **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="33eec-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="33eec-111">Usare i campi filtro nel riquadro destro per restringere i risultati della ricerca e quindi fare clic su **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="33eec-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="33eec-112">I risultati verranno visualizzati sotto la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="33eec-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="33eec-113">Eseguire l'azione appropriata come determinato dal criterio per i dispositivi persi.</span><span class="sxs-lookup"><span data-stu-id="33eec-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="33eec-114">**Nota**  La conformità del dispositivo è determinata dai criteri di BitLocker distribuiti.</span><span class="sxs-lookup"><span data-stu-id="33eec-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="33eec-115">È consigliabile verificare questi criteri distribuiti quando si prova a determinare lo stato di crittografia di BitLocker di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33eec-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="33eec-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33eec-116">Related topics</span></span>


[<span data-ttu-id="33eec-117">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="33eec-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





