---
title: Come pubblicare un pacchetto tramite la console di gestione
description: Come pubblicare un pacchetto tramite la console di gestione
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805236"
---
# <span data-ttu-id="53a6d-103">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="53a6d-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="53a6d-104">Usare la procedura seguente per pubblicare un pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="53a6d-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="53a6d-105">Dopo aver pubblicato un pacchetto, i computer che eseguono il client App-V 5,0 possono accedere ed eseguire le applicazioni in tale pacchetto.</span><span class="sxs-lookup"><span data-stu-id="53a6d-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="53a6d-106">**Nota**  La possibilità di abilitare solo gli amministratori per la pubblicazione o l'annullamento della pubblicazione di pacchetti (descritti di seguito) è supportata a partire da App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="53a6d-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="53a6d-107">Per pubblicare un pacchetto di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="53a6d-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="53a6d-108">Nella console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="53a6d-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="53a6d-109">fare clic con il pulsante destro del mouse sul nome del pacchetto da pubblicare e scegliere **pubblica**.</span><span class="sxs-lookup"><span data-stu-id="53a6d-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="53a6d-110">Esaminare la colonna **stato** per verificare che il pacchetto sia stato pubblicato ed è ora disponibile.</span><span class="sxs-lookup"><span data-stu-id="53a6d-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="53a6d-111">Se il pacchetto è disponibile, viene visualizzato lo stato **pubblicato** .</span><span class="sxs-lookup"><span data-stu-id="53a6d-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="53a6d-112">Se il pacchetto non viene pubblicato correttamente, viene visualizzato lo stato non **pubblicato** , insieme al testo dell'errore che spiega perché il pacchetto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="53a6d-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="53a6d-113">Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="53a6d-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="53a6d-114">Passare al nodo oggetto Criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="53a6d-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="53a6d-115">**Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="53a6d-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="53a6d-116">Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .</span><span class="sxs-lookup"><span data-stu-id="53a6d-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="53a6d-117">Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,0 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="53a6d-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="53a6d-118">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="53a6d-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="53a6d-119">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="53a6d-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="53a6d-120">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="53a6d-120">Got an App-V issue?</span></span>** <span data-ttu-id="53a6d-121">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="53a6d-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="53a6d-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53a6d-122">Related topics</span></span>


[<span data-ttu-id="53a6d-123">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="53a6d-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="53a6d-124">Come configurare l'accesso ai pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="53a6d-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





