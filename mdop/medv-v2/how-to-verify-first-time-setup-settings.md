---
title: Come verificare le impostazioni della prima configurazione
description: Come verificare le impostazioni della prima configurazione
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804666"
---
# <span data-ttu-id="c207e-103">Come verificare le impostazioni della prima configurazione</span><span class="sxs-lookup"><span data-stu-id="c207e-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="c207e-104">Durante l'esecuzione del test di configurazione per la prima volta o dopo il completamento, è possibile verificare le impostazioni configurate nell'area di lavoro MED-V eseguendo le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="c207e-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="c207e-105">**Nota**  Per informazioni su come monitorare il completamento della configurazione per la prima volta in tutta l'organizzazione dopo la distribuzione, vedere [monitoraggio delle distribuzioni dell'area di lavoro MED-V](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="c207e-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="c207e-106">Per verificare le impostazioni durante la configurazione per la prima volta</span><span class="sxs-lookup"><span data-stu-id="c207e-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="c207e-107">Durante l'esecuzione della configurazione per la prima volta, verificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c207e-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="c207e-108">Se è stata specificata la modalità **automatica** , verificare che la macchina virtuale non venga visualizzata quando viene eseguita la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="c207e-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="c207e-109">Se è stata specificata la modalità assistita, verificare che la macchina virtuale venga visualizzata e che siano visualizzati tutti i campi che richiedono l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c207e-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="c207e-110">È anche possibile monitorare la procedura di configurazione completa per la prima volta visualizzando la macchina virtuale quando è in esecuzione la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="c207e-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="c207e-111">A tale scopo, effettua quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c207e-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="c207e-112">Aprire la console PC virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="c207e-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="c207e-113">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.</span><span class="sxs-lookup"><span data-stu-id="c207e-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="c207e-114">Avviare MED-V se non è già in uso.</span><span class="sxs-lookup"><span data-stu-id="c207e-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="c207e-115">Se non è già presente, in breve tempo viene visualizzata una macchina virtuale con il nome dell'area di lavoro MED-V distribuita nell'elenco delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c207e-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="c207e-116">Fare doppio clic sulla macchina virtuale MED-V per aprirla.</span><span class="sxs-lookup"><span data-stu-id="c207e-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="c207e-117">È possibile osservare la macchina virtuale MED-V quando è in fase di configurazione ed è possibile risolvere i problemi della procedura di configurazione minima.</span><span class="sxs-lookup"><span data-stu-id="c207e-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="c207e-118">Verificare le informazioni nelle diverse schermate, ad esempio la configurazione delle impostazioni di rete, le informazioni di join del dominio del computer, la configurazione dell'agente guest, l'impostazione delle impostazioni personali e l'arresto.</span><span class="sxs-lookup"><span data-stu-id="c207e-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="c207e-119">La macchina virtuale si chiude automaticamente al termine della configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="c207e-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="c207e-120">**Nota**  È possibile chiudere la finestra della macchina virtuale in qualsiasi momento e la configurazione della prima volta continua.</span><span class="sxs-lookup"><span data-stu-id="c207e-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="c207e-121">Per verificare le impostazioni al termine della configurazione per la prima volta</span><span class="sxs-lookup"><span data-stu-id="c207e-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="c207e-122">Verificare che la configurazione per la prima volta sia stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c207e-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="c207e-123">Verificare che l'area di lavoro MED-V sia configurata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c207e-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="c207e-124">Aprire la console PC virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="c207e-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="c207e-125">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.</span><span class="sxs-lookup"><span data-stu-id="c207e-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="c207e-126">Fare doppio clic sull'area di lavoro MED-V installata.</span><span class="sxs-lookup"><span data-stu-id="c207e-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="c207e-127">Se l'area di lavoro MED-V è già in uso, potrebbe essere richiesto di chiudere l'applicazione prima di poter aprire la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c207e-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="c207e-128">Nell'area di lavoro MED-V fare clic con il pulsante destro del mouse su **risorse del computer**e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="c207e-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="c207e-129">Verificare che l'area di lavoro MED-V sia stata aggiunta al dominio corretto.</span><span class="sxs-lookup"><span data-stu-id="c207e-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="c207e-130">Se applicabile per l'organizzazione, provare a partecipare al dominio specificando due diversi domini per verificare che il dominio guest venga sottoposto a override dal dominio host.</span><span class="sxs-lookup"><span data-stu-id="c207e-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="c207e-131">Verificare che l'area di lavoro MED-V sia stata aggiunta all'unità organizzativa del dominio specificata.</span><span class="sxs-lookup"><span data-stu-id="c207e-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="c207e-132">Se è stata specificata la maschera nome computer, verificare che il nome del nuovo computer corrisponda a quello specificato.</span><span class="sxs-lookup"><span data-stu-id="c207e-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="c207e-133">Verificare che le impostazioni locali specificate siano corrette.</span><span class="sxs-lookup"><span data-stu-id="c207e-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="c207e-134">Nell'area di lavoro MED-V fare clic su **Start** e quindi su **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="c207e-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="c207e-135">Verificare le impostazioni di configurazione specificate, ad esempio **data e ora** , **internazionali e della lingua**.</span><span class="sxs-lookup"><span data-stu-id="c207e-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="c207e-136">**Nota**  In caso di problemi durante la verifica delle impostazioni di configurazione per la prima volta, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="c207e-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="c207e-137">Dopo avere verificato che le impostazioni di configurazione per la prima volta sono corrette, è possibile verificare altre configurazioni dell'area di lavoro MED-V per verificarne il funzionamento, ad esempio la pubblicazione di applicazioni e il reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="c207e-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="c207e-138">Dopo aver completato tutti i test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c207e-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="c207e-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c207e-139">Related topics</span></span>


[<span data-ttu-id="c207e-140">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="c207e-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="c207e-141">Come verificare il reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="c207e-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="c207e-142">Distribuzione del pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c207e-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="c207e-143">Gestire le impostazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="c207e-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





