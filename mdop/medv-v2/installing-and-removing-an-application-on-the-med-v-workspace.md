---
title: Installazione e rimozione di un'applicazione nell'area di lavoro MED-V
description: Installazione e rimozione di un'applicazione nell'area di lavoro MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827216"
---
# <span data-ttu-id="1df3b-103">Installazione e rimozione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1df3b-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="1df3b-104">Le applicazioni che non sono compatibili con il sistema operativo host possono essere eseguite nell'area di lavoro MED-V e aperte nell'area di lavoro MED-V nello stesso modo in cui vengono aperte dal computer host, nel menu **Start** o usando un collegamento a localhost.</span><span class="sxs-lookup"><span data-stu-id="1df3b-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="1df3b-105">Dopo aver distribuito un'area di lavoro MED-V, sono disponibili diverse opzioni per l'installazione e la rimozione delle applicazioni nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1df3b-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="1df3b-106">Queste opzioni includono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="1df3b-106">These options include the following:</span></span>

-   [<span data-ttu-id="1df3b-107">Uso di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1df3b-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="1df3b-108">Uso di un sistema elettronico di distribuzione del software</span><span class="sxs-lookup"><span data-stu-id="1df3b-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="1df3b-109">Uso della virtualizzazione delle applicazioni (APP-V)</span><span class="sxs-lookup"><span data-stu-id="1df3b-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="1df3b-110">Aggiornamento dell'immagine di base</span><span class="sxs-lookup"><span data-stu-id="1df3b-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="1df3b-111">**Importante**  Per assicurarsi che un'applicazione installata venga pubblicata automaticamente nell'host, installare l'applicazione nella macchina virtuale per **tutti gli utenti**.</span><span class="sxs-lookup"><span data-stu-id="1df3b-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="1df3b-112">Per altre informazioni sulla pubblicazione delle applicazioni, vedere [come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1df3b-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="1df3b-113">**Suggerimento**  MED-V non supporta il reindirizzamento Guest-to-host per la gestione del contenuto, ad esempio fare doppio clic su un documento di Microsoft Word in Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1df3b-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="1df3b-114">Di conseguenza, le applicazioni necessarie, ad esempio Microsoft Word, devono essere installate nell'area di lavoro MED-V per specificare le funzionalità di gestione del contenuto predefinite che un utente finale può aspettarsi.</span><span class="sxs-lookup"><span data-stu-id="1df3b-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="1df3b-115">Aggiunta e rimozione di applicazioni tramite criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1df3b-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="1df3b-116">Puoi usare gli oggetti Criteri di gruppo e criteri di gruppo per assegnare o pubblicare applicazioni in tutte le aree di lavoro di MED-V nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="1df3b-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="1df3b-117">Per le applicazioni assegnate, quando un utente finale accede al proprio computer, l'applicazione viene visualizzata nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="1df3b-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="1df3b-118">Quando si seleziona la nuova applicazione per la prima volta, l'applicazione viene installata ed è pronta per l'uso.</span><span class="sxs-lookup"><span data-stu-id="1df3b-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="1df3b-119">Per le applicazioni pubblicate, l'applicazione non viene visualizzata nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="1df3b-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="1df3b-120">È disponibile solo per l'installazione da parte dell'utente finale utilizzando installazione **applicazioni** nel pannello di **controllo** o aprendo un file associato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1df3b-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="1df3b-121">È anche possibile usare i criteri di gruppo e gli oggetti Criteri di gruppo allo stesso modo per rimuovere le applicazioni dall'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1df3b-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="1df3b-122">Per altre informazioni su come aggiungere e rimuovere applicazioni tramite criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="1df3b-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="1df3b-123">Aggiunta e rimozione di applicazioni tramite un sistema ESD</span><span class="sxs-lookup"><span data-stu-id="1df3b-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="1df3b-124">Un sistema ESD (Electronic Software Distribution) è progettato per distribuire efficacemente il software e altre informazioni a molti computer diversi tramite connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="1df3b-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="1df3b-125">Se l'organizzazione usa un sistema ESD per distribuire il software, è possibile usarlo per aggiungere e rimuovere applicazioni nelle aree di lavoro MED-V così come si aggiungono e si rimuovono applicazioni in computer fisici.</span><span class="sxs-lookup"><span data-stu-id="1df3b-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="1df3b-126">Aggiunta e rimozione di applicazioni tramite APP-V</span><span class="sxs-lookup"><span data-stu-id="1df3b-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="1df3b-127">Microsoft Application Virtualization (App-V) offre la funzionalità amministrativa per rendere le applicazioni disponibili per i computer degli utenti finali senza dover installare le applicazioni direttamente in tali computer.</span><span class="sxs-lookup"><span data-stu-id="1df3b-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="1df3b-128">Potresti voler usare MED-V e App-V insieme se, ad esempio, l'organizzazione ha applicazioni sequenziate con App-V in Windows XP e la loro ripetizione sequenziale ritarderà la migrazione a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1df3b-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="1df3b-129">Puoi usare MED-V insieme a App-V per aggiungere e rimuovere applicazioni virtuali in un'area di lavoro MED-V distribuita.</span><span class="sxs-lookup"><span data-stu-id="1df3b-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="1df3b-130">Per gestire le applicazioni in questo modo, devi prima installare l'agente App-V nel sistema operativo guest MED-V.</span><span class="sxs-lookup"><span data-stu-id="1df3b-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="1df3b-131">Puoi quindi usare app-V nell'area di lavoro MED-V per aggiungere e rimuovere le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="1df3b-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="1df3b-132">Per informazioni su come installare e usare app-V, vedere [virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="1df3b-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="1df3b-133">**Importante**  Le applicazioni App-V pubblicate nell'area di lavoro MED-V hanno associazioni di tipi di file che non possono essere reindirizzate dal computer host alla macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="1df3b-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="1df3b-134">Tuttavia, l'utente finale può comunque accedere a questi tipi di file facendo clic su **file**e quindi facendo clic su **Apri** nell'applicazione App-V pubblicata.</span><span class="sxs-lookup"><span data-stu-id="1df3b-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="1df3b-135">Per forzare il reindirizzamento delle associazioni di tipi di file, eseguire una query in App-V per le associazioni di tipi di file mappati digitando quanto segue al prompt dei comandi nella macchina virtuale Guest: **SFTMIME/query obj: Type**.</span><span class="sxs-lookup"><span data-stu-id="1df3b-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="1df3b-136">Eseguire quindi il mapping delle associazioni di tipi di file nel computer host.</span><span class="sxs-lookup"><span data-stu-id="1df3b-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="1df3b-137">Aggiunta e rimozione di applicazioni nell'immagine principale</span><span class="sxs-lookup"><span data-stu-id="1df3b-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="1df3b-138">Anche se non è considerata una procedura consigliata per MED-V, è possibile aggiungere e rimuovere applicazioni direttamente nell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1df3b-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="1df3b-139">Dopo aver aggiunto o rimosso un'applicazione, è possibile ridistribuire l'area di lavoro MED-V nell'organizzazione proprio come è stata distribuita in origine.</span><span class="sxs-lookup"><span data-stu-id="1df3b-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="1df3b-140">Per altre informazioni su come aggiungere o rimuovere applicazioni nell'immagine principale, vedere installazione di [applicazioni in un'immagine di Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="1df3b-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="1df3b-141">**Importante**  Questo metodo di gestione delle applicazioni non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="1df3b-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="1df3b-142">Se si aggiungono o si rimuovono applicazioni nell'immagine principale e si ridistribuisce l'area di lavoro MED-V nell'organizzazione, è necessario eseguire di nuovo la configurazione per la prima volta e tutti i dati salvati nella macchina virtuale andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="1df3b-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="1df3b-143">**Nota**  Anche se un'applicazione viene installata in un'area di lavoro MED-V, potrebbe essere necessario pubblicare l'applicazione anche prima che diventi disponibile per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1df3b-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="1df3b-144">Ad esempio, potrebbe essere necessario pubblicare un'applicazione installata se l'installazione non crea automaticamente un collegamento nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="1df3b-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="1df3b-145">Allo stesso modo, per annullare la pubblicazione di un'applicazione, potrebbe essere necessario rimuovere manualmente un collegamento dal menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="1df3b-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="1df3b-146">Per impostazione predefinita, la maggior parte delle applicazioni viene pubblicata al momento dell'installazione, quando i tasti di scelta rapida vengono creati e abilitati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1df3b-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="1df3b-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1df3b-147">Related topics</span></span>


[<span data-ttu-id="1df3b-148">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="1df3b-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="1df3b-149">Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1df3b-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





