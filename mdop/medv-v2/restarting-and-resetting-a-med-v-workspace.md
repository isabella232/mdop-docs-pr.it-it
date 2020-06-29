---
title: Riavvio e ripristino di un'area di lavoro MED-V
description: Riavvio e ripristino di un'area di lavoro MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825425"
---
# <span data-ttu-id="88eb9-103">Riavvio e ripristino di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="88eb9-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="88eb9-104">Durante la risoluzione dei problemi, a volte potrebbe essere necessario riavviare o reimpostare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="88eb9-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="88eb9-105">Riavviare l'area di lavoro MED-V è praticamente lo stesso che riavviare un computer fisico.</span><span class="sxs-lookup"><span data-stu-id="88eb9-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="88eb9-106">La reimpostazione dell'area di lavoro MED-V consente di rieseguire la configurazione iniziale ed Elimina tutti i dati archiviati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88eb9-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="88eb9-107">Poiché tutti i dati archiviati vengono eliminati, in genere è consigliabile reimpostare l'area di lavoro MED-V solo per risolvere i problemi di risoluzione dei problemi più gravi o per ripristinare un'area di lavoro di MED-V in precedenza in uno stato lavorativo.</span><span class="sxs-lookup"><span data-stu-id="88eb9-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="88eb9-108">Per informazioni su come aprire il Toolkit di amministrazione MED-V, vedere [risoluzione dei problemi relativi a Med-v tramite Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="88eb9-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="88eb9-109">Riavvio di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="88eb9-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="88eb9-110">Nella finestra **Toolkit di amministrazione MED-v** fare clic su **Riavvia area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="88eb9-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="88eb9-111">Verrà visualizzata una finestra di dialogo in cui è necessario confermare che si vuole riavviare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="88eb9-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="88eb9-112">Fare clic su **Riavvia**.</span><span class="sxs-lookup"><span data-stu-id="88eb9-112">Click **Restart**.</span></span>

    <span data-ttu-id="88eb9-113">Tutte le applicazioni pubblicate in cui vengono eseguiti o reindirizzati i siti Web aperti verranno chiuse quando viene riavviata l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="88eb9-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="88eb9-114">Reimpostazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="88eb9-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="88eb9-115">Nella finestra **Toolkit di amministrazione MED-v** fare clic su **Reimposta area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="88eb9-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="88eb9-116">Verrà visualizzata una finestra di dialogo in cui è necessario confermare che si vuole reimpostare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="88eb9-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="88eb9-117">**Avviso**  La reimpostazione dell'area di lavoro MED-V consente di eseguire di nuovo la configurazione per la prima volta e quindi ricarica il disco rigido virtuale originale.</span><span class="sxs-lookup"><span data-stu-id="88eb9-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="88eb9-118">Tutti i dati archiviati nell'area di lavoro MED-V da quando è stata eseguita la configurazione per la prima volta verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="88eb9-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="88eb9-119">Fai clic su **Reimposta**.</span><span class="sxs-lookup"><span data-stu-id="88eb9-119">Click **Reset**.</span></span>

    <span data-ttu-id="88eb9-120">Tutte le applicazioni pubblicate in cui vengono eseguiti o reindirizzati i siti Web aperti verranno chiuse quando si reimposta l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="88eb9-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="88eb9-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88eb9-121">Related topics</span></span>


[<span data-ttu-id="88eb9-122">Visualizzazione e configurazione dei log MED-V</span><span class="sxs-lookup"><span data-stu-id="88eb9-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="88eb9-123">Visualizzazione delle configurazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="88eb9-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





