---
title: Rimozione di software o funzionalità del server di MBAM
description: Rimozione di software o funzionalità del server di MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824976"
---
# <span data-ttu-id="dc20b-103">Rimozione di software o funzionalità del server di MBAM</span><span class="sxs-lookup"><span data-stu-id="dc20b-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="dc20b-104">Queste istruzioni spiegano come rimuovere software e funzionalità da Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="dc20b-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="dc20b-105">Se si rimuovono le caratteristiche del server MBAM, solo le caratteristiche configurate vengono rimosse dal server, non dal software server MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc20b-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="dc20b-106">Se si rimuove il software MBAM server, il software e tutte le funzionalità di MBAM Server configurate in tale server vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="dc20b-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="dc20b-107">**Nota**  Per evitare la rimozione accidentale dei dati, MBAM non fornisce alcun meccanismo per rimuovere i database; è necessario eseguire questa operazione manualmente.</span><span class="sxs-lookup"><span data-stu-id="dc20b-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="dc20b-108">Rimozione delle caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="dc20b-108">Removing MBAM Server features</span></span>


<span data-ttu-id="dc20b-109">Puoi usare uno dei metodi seguenti per rimuovere le caratteristiche del server MBAM configurate:</span><span class="sxs-lookup"><span data-stu-id="dc20b-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="dc20b-110">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="dc20b-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="dc20b-111">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc20b-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="dc20b-112">Uso della configurazione guidata di MBAM server per rimuovere le caratteristiche</span><span class="sxs-lookup"><span data-stu-id="dc20b-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="dc20b-113">Seguire queste istruzioni per usare la configurazione guidata di MBAM server per rimuovere le caratteristiche del server MBAM configurate da un server.</span><span class="sxs-lookup"><span data-stu-id="dc20b-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="dc20b-114">Per rimuovere le caratteristiche di MBAM tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="dc20b-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="dc20b-115">Nel server in cui si vogliono rimuovere le caratteristiche selezionare la **configurazione di mbam server** per aprire la configurazione guidata.</span><span class="sxs-lookup"><span data-stu-id="dc20b-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="dc20b-116">Fare clic su **Rimuovi funzionalità**, selezionare le caratteristiche da rimuovere e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="dc20b-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="dc20b-117">Una pagina di **Riepilogo** Visualizza le caratteristiche selezionate per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="dc20b-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="dc20b-118">Fare clic su **Rimuovi** per iniziare a rimuovere le funzionalità e quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="dc20b-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="dc20b-119">Uso di Windows PowerShell per rimuovere le caratteristiche</span><span class="sxs-lookup"><span data-stu-id="dc20b-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="dc20b-120">Usare i passaggi seguenti come guida generale per rimuovere le caratteristiche del server MBAM usando i cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc20b-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="dc20b-121">Per rimuovere le caratteristiche di MBAM tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc20b-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="dc20b-122">Prima di rimuovere qualsiasi funzionalità, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc20b-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="dc20b-123">Usare i cmdlet seguenti per rimuovere le caratteristiche del server MBAM:</span><span class="sxs-lookup"><span data-stu-id="dc20b-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="dc20b-124">Disable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="dc20b-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="dc20b-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="dc20b-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="dc20b-126">Disable-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="dc20b-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="dc20b-127">Per ottenere assistenza per i cmdlet di Windows PowerShell, digitare **Get-Help** &lt; *cmdlet* &gt; oppure vedere la pagina [Microsoft Desktop Optimization Pack Automation con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) per i cmdlet di Windows PowerShell di mbam.</span><span class="sxs-lookup"><span data-stu-id="dc20b-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="dc20b-128">Rimozione del software del server MBAM</span><span class="sxs-lookup"><span data-stu-id="dc20b-128">Removing MBAM Server software</span></span>


<span data-ttu-id="dc20b-129">Usare la procedura seguente per rimuovere il software MBAM server e le funzionalità di MBAM Server configurate nel server.</span><span class="sxs-lookup"><span data-stu-id="dc20b-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="dc20b-130">Per rimuovere il software del server MBAM</span><span class="sxs-lookup"><span data-stu-id="dc20b-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="dc20b-131">Nel server in cui si vuole disinstallare il software MBAM Server eseguire **MBAMserversetup.exe** per avviare la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dc20b-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="dc20b-132">Selezionare **Disinstalla**e seguire le istruzioni rimanenti per completare il processo di disinstallazione del software del server mbam.</span><span class="sxs-lookup"><span data-stu-id="dc20b-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="dc20b-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc20b-133">Related topics</span></span>


[<span data-ttu-id="dc20b-134">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc20b-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="dc20b-135">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="dc20b-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dc20b-136">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="dc20b-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="dc20b-137">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="dc20b-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



