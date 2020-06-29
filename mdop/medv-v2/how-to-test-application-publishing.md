---
title: Come verificare la pubblicazione delle applicazioni
description: Come verificare la pubblicazione delle applicazioni
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826915"
---
# <span data-ttu-id="67157-103">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="67157-103">How to Test Application Publishing</span></span>


<span data-ttu-id="67157-104">Dopo la fine del test di configurazione per la prima volta, è possibile verificare che la funzionalità di pubblicazione dell'applicazione funzioni come previsto eseguendo le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="67157-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="67157-105">Per testare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="67157-105">To test application publishing</span></span>**

1.  <span data-ttu-id="67157-106">Verificare che le applicazioni specificate per la pubblicazione siano visibili.</span><span class="sxs-lookup"><span data-stu-id="67157-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="67157-107">Fare clic sul pulsante **Start** e quindi scegliere **tutti i programmi** e cercare le applicazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="67157-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="67157-108">In alcuni casi è possibile che la stessa applicazione sia installata due volte, una sola volta nel computer host e una sola volta nel guest.</span><span class="sxs-lookup"><span data-stu-id="67157-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="67157-109">Se un'applicazione pubblicata con lo stesso nome viene pubblicata nella stessa posizione nel menu **Start** dell'host, si distingue dal collegamento all'applicazione host aggiungendo il nome della macchina virtuale al nome del collegamento.</span><span class="sxs-lookup"><span data-stu-id="67157-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="67157-110">Ad esempio, per una macchina virtuale denominata "MEDVHost1", un'applicazione host potrebbe essere "Notepad" e un'applicazione pubblicata potrebbe essere "Notepad (MEDVHost1)".</span><span class="sxs-lookup"><span data-stu-id="67157-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="67157-111">Verificare che le applicazioni funzionino come previsto.</span><span class="sxs-lookup"><span data-stu-id="67157-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="67157-112">Nel computer host avviare le applicazioni pubblicate e verificare che vengano aperte in Windows XP SP3 per l'ospite.</span><span class="sxs-lookup"><span data-stu-id="67157-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="67157-113">L'applicazione deve essere visualizzata in una finestra in stile Windows XP nel desktop del computer host.</span><span class="sxs-lookup"><span data-stu-id="67157-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="67157-114">Se applicabile, verificare che il reindirizzamento dei documenti funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="67157-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="67157-115">Se un'applicazione pubblicata per l'ospite deve aprire una cartella nell'unità host System, verificare che sia possibile aprire la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="67157-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="67157-116">**Importante**  Dato che Windows Virtual PC non supporta la creazione di una condivisione da una cartella già condivisa, il reindirizzamento non si verifica per i documenti che si aprono da una cartella condivisa, ad esempio una cartella documenti che si trova nella rete.</span><span class="sxs-lookup"><span data-stu-id="67157-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="67157-117">Per altre informazioni, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="67157-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="67157-118">Dopo avere verificato che le applicazioni pubblicate sono installate e funzionanti correttamente, è possibile verificare se le applicazioni possono essere aggiunte o rimosse dall'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67157-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="67157-119">Per verificare che un'applicazione possa essere aggiunta o rimossa</span><span class="sxs-lookup"><span data-stu-id="67157-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="67157-120">Aggiungere o rimuovere un'applicazione dall'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67157-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="67157-121">Per informazioni su come aggiungere e rimuovere applicazioni da un'area di lavoro MED-V, vedere [gestione delle applicazioni distribuite nelle aree di lavoro MED-v](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="67157-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="67157-122">Se è stata aggiunta un'applicazione, ripetere i passaggi [per testare la pubblicazione dell'applicazione](#bkmk-apppub) per verificare che la nuova applicazione funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="67157-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="67157-123">Se è stata rimossa un'applicazione, fare clic su **Start** e quindi su **tutti i programmi** e verificare che le applicazioni rimosse non siano più elencate.</span><span class="sxs-lookup"><span data-stu-id="67157-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="67157-124">**Nota**  In caso di problemi durante la verifica delle impostazioni di pubblicazione delle applicazioni, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="67157-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="67157-125">Dopo aver completato il test di pubblicazione delle applicazioni, è possibile testare altre configurazioni dell'area di lavoro MED-V per verificare che funzionino come previsto.</span><span class="sxs-lookup"><span data-stu-id="67157-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="67157-126">Dopo aver completato il test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.</span><span class="sxs-lookup"><span data-stu-id="67157-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="67157-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67157-127">Related topics</span></span>

[<span data-ttu-id="67157-128">Come verificare il reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="67157-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="67157-129">Come verificare le impostazioni della prima configurazione</span><span class="sxs-lookup"><span data-stu-id="67157-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="67157-130">Distribuzione del pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="67157-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





