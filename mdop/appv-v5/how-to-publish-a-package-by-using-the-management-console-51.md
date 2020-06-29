---
title: Come pubblicare un pacchetto tramite la console di gestione
description: Come pubblicare un pacchetto tramite la console di gestione
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805224"
---
# <span data-ttu-id="cd7e1-103">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd7e1-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="cd7e1-104">Usare la procedura seguente per pubblicare un pacchetto App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="cd7e1-105">Dopo aver pubblicato un pacchetto, i computer che eseguono il client App-V 5,1 possono accedere ed eseguire le applicazioni in tale pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="cd7e1-106">**Nota**  La possibilità di abilitare solo gli amministratori per la pubblicazione o l'annullamento della pubblicazione di pacchetti (descritti di seguito) è supportata a partire da App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="cd7e1-107">Per pubblicare un pacchetto di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="cd7e1-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="cd7e1-108">Nella console di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="cd7e1-109">Fare clic o fare clic con il pulsante destro del mouse sul nome del pacchetto da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="cd7e1-110">Selezionare **pubblica**.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="cd7e1-111">Esaminare la colonna **stato** per verificare che il pacchetto sia stato pubblicato ed è ora disponibile.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="cd7e1-112">Se il pacchetto è disponibile, viene visualizzato lo stato **pubblicato** .</span><span class="sxs-lookup"><span data-stu-id="cd7e1-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="cd7e1-113">Se il pacchetto non viene pubblicato correttamente, viene visualizzato lo stato non **pubblicato** , insieme al testo dell'errore che spiega perché il pacchetto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="cd7e1-114">Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="cd7e1-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="cd7e1-115">Passare al nodo oggetto Criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="cd7e1-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="cd7e1-116">**Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="cd7e1-117">Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .</span><span class="sxs-lookup"><span data-stu-id="cd7e1-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="cd7e1-118">Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,1 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="cd7e1-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="cd7e1-119">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="cd7e1-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cd7e1-120">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cd7e1-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cd7e1-121">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="cd7e1-121">Got an App-V issue?</span></span>** <span data-ttu-id="cd7e1-122">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cd7e1-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cd7e1-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd7e1-123">Related topics</span></span>


[<span data-ttu-id="cd7e1-124">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="cd7e1-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="cd7e1-125">Come configurare l'accesso ai pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd7e1-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





