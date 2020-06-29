---
title: Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione
description: Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827275"
---
# <span data-ttu-id="f9960-103">Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f9960-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="f9960-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 supportano le applicazioni Microsoft Application Virtualization (App-V) senza apportare modifiche necessarie al pacchetto App-V o al modello UE-V.</span><span class="sxs-lookup"><span data-stu-id="f9960-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="f9960-105">Tuttavia, è necessario un passaggio aggiuntivo perché non è possibile eseguire il generatore UE-V direttamente in un'applicazione App-V virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="f9960-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="f9960-106">È invece necessario installare l'applicazione localmente, generare il modello e quindi applicare il modello all'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="f9960-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="f9960-107">UE-V supporta i pacchetti App-V 4,5, App-V 4,6 e App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f9960-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="f9960-108">Sincronizzazione delle impostazioni di UE-V per le applicazioni App-V</span><span class="sxs-lookup"><span data-stu-id="f9960-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="f9960-109">UE-V monitora quando un'applicazione si apre con il nome del programma e, facoltativamente, per i numeri di versione del file e i numeri di versione del prodotto, indipendentemente dal fatto che l'applicazione sia installata localmente o virtualmente usando App-V.</span><span class="sxs-lookup"><span data-stu-id="f9960-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="f9960-110">Quando l'applicazione viene avviata, la UE-V monitora il processo App-V, applica tutte le impostazioni archiviate nel percorso di archiviazione delle impostazioni dell'utente e quindi consente l'avvio normale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9960-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="f9960-111">UE-V monitora le applicazioni App-V e traduce automaticamente i percorsi di file e del registro di sistema pertinenti nella posizione virtualizzata rispetto alla posizione fisica esterna all'ambiente di elaborazione di App-V.</span><span class="sxs-lookup"><span data-stu-id="f9960-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="f9960-112">Per implementare la sincronizzazione delle impostazioni per un'applicazione virtualizzata</span><span class="sxs-lookup"><span data-stu-id="f9960-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="f9960-113">Eseguire il generatore di UE-V per raccogliere le impostazioni dell'applicazione installata localmente di cui si vuole sincronizzare i computer.</span><span class="sxs-lookup"><span data-stu-id="f9960-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="f9960-114">Questo processo crea un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9960-114">This process creates a settings location template.</span></span> <span data-ttu-id="f9960-115">Se si usa un modello predefinito, ad esempio il modello Microsoft Office 2010, ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="f9960-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="f9960-116">Per altre informazioni sull'uso del generatore UE-V, vedere [distribuire UE-v 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="f9960-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="f9960-117">Installare il pacchetto dell'applicazione App-V se non è già stato fatto.</span><span class="sxs-lookup"><span data-stu-id="f9960-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="f9960-118">Pubblicare il modello nella posizione del catalogo del modello di impostazioni o installare manualmente il modello usando il `Register-UEVTemplate` cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9960-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="f9960-119">**Nota**  Se pubblichi il modello appena creato nel catalogo dei modelli di impostazioni, il client non riceverà il modello fino a quando il provider di sincronizzazione non aggiornerà le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9960-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="f9960-120">Per avviare manualmente il processo, aprire **utilità di pianificazione**, espandere **la raccolta**utilità di pianificazione, espandere **Microsoft**ed espandere **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="f9960-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="f9960-121">Nel riquadro risultati fare clic con il pulsante destro del mouse su **aggiornamento automatico modelli**e quindi scegliere **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="f9960-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="f9960-122">Avviare il pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="f9960-122">Start the App-V package.</span></span>






## <span data-ttu-id="f9960-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9960-123">Related topics</span></span>


[<span data-ttu-id="f9960-124">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f9960-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





