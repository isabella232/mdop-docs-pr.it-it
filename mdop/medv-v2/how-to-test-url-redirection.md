---
title: Come verificare il reindirizzamento URL
description: Come verificare il reindirizzamento URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824446"
---
# <span data-ttu-id="a7e52-103">Come verificare il reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="a7e52-103">How to Test URL Redirection</span></span>


<span data-ttu-id="a7e52-104">Dopo l'esecuzione del test della configurazione prima volta, è possibile verificare che la funzionalità di reindirizzamento degli URL funzioni come previsto eseguendo le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7e52-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="a7e52-105">**Importante**  L'agente host MED-V deve essere in funzione in modo che il reindirizzamento degli URL funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="a7e52-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="a7e52-106">Per testare il reindirizzamento degli URL</span><span class="sxs-lookup"><span data-stu-id="a7e52-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="a7e52-107">Aprire un browser Internet Explorer nel computer host e immettere un URL specificato per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="a7e52-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="a7e52-108">Verificare che la pagina Web sia aperta in Internet Explorer nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="a7e52-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="a7e52-109">Ripetere questa procedura per ogni URL che si vuole testare.</span><span class="sxs-lookup"><span data-stu-id="a7e52-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="a7e52-110">Per verificare che sia possibile aggiungere o rimuovere un URL</span><span class="sxs-lookup"><span data-stu-id="a7e52-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="a7e52-111">Aggiungere o rimuovere un URL dall'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="a7e52-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="a7e52-112">Per informazioni su come aggiungere e rimuovere URL per il reindirizzamento in un'area di lavoro MED-V, vedere [gestire il reindirizzamento degli URL di Med-v](manage-med-v-url-redirection.md).</span><span class="sxs-lookup"><span data-stu-id="a7e52-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="a7e52-113">Se è stato aggiunto un URL all'elenco di reindirizzamento, ripetere i passaggi [per testare il reindirizzamento degli URL](#bkmk-urlredir) per verificare che il nuovo URL venga reindirizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="a7e52-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="a7e52-114">Se è stato rimosso un URL dall'elenco di reindirizzamento, verificare che venga rimosso eseguendo la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="a7e52-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="a7e52-115">Aprire un browser Internet Explorer nel computer host e immettere l'URL rimosso dall'elenco di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="a7e52-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="a7e52-116">Verificare che la pagina Web sia aperta in Internet Explorer nel computer host anziché nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="a7e52-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="a7e52-117">**Nota**  Può essere necessario attendere alcuni secondi prima che le modifiche al reindirizzamento degli URL avvengano.</span><span class="sxs-lookup"><span data-stu-id="a7e52-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="a7e52-118">**Nota**  In caso di problemi durante la verifica delle impostazioni di reindirizzamento degli URL, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="a7e52-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="a7e52-119">Dopo aver completato i test di reindirizzamento degli URL nell'area di lavoro MED-V, è possibile testare altre configurazioni per verificare che funzionino come previsto.</span><span class="sxs-lookup"><span data-stu-id="a7e52-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="a7e52-120">Dopo aver completato il test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a7e52-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="a7e52-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7e52-121">Related topics</span></span>

[<span data-ttu-id="a7e52-122">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="a7e52-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="a7e52-123">Come verificare le impostazioni della prima configurazione</span><span class="sxs-lookup"><span data-stu-id="a7e52-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="a7e52-124">Distribuzione del pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="a7e52-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





