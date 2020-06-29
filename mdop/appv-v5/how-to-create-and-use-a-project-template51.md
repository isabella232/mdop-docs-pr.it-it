---
title: Come creare e usare un modello di progetto
description: Come creare e usare un modello di progetto
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805584"
---
# <span data-ttu-id="af09e-103">Come creare e usare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="af09e-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="af09e-104">Puoi usare un modello di progetto App-V 5,1 per salvare le impostazioni comunemente applicate associate a un pacchetto di applicazione virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="af09e-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="af09e-105">Queste impostazioni possono quindi essere applicate quando crei nuovi pacchetti di applicazioni virtuali nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="af09e-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="af09e-106">L'uso di un modello di progetto consente di semplificare il processo di creazione di pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="af09e-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="af09e-107">Nota</span><span class="sxs-lookup"><span data-stu-id="af09e-107">Note</span></span>**  
<span data-ttu-id="af09e-108">È possibile e spesso deve applicare un modello di progetto App-V 5,1 durante l'aggiornamento di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="af09e-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="af09e-109">Se ad esempio è stata sequenziata un'applicazione con un elenco di esclusione personalizzato, è consigliabile creare e salvare un modello associato per l'uso successivo durante l'aggiornamento dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="af09e-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="af09e-110">I modelli di progetto di App-V 5,1 si differenziano dagli acceleratori delle applicazioni App-V 5,1 perché gli acceleratori di applicazioni App-V 5,1 sono specifici dell'applicazione e i modelli di progetto di App-V 5,1 possono essere applicati a più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="af09e-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="af09e-111">Usare le procedure seguenti per creare e applicare un nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="af09e-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="af09e-112">Per creare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="af09e-112">To create a project template</span></span>**

1.  <span data-ttu-id="af09e-113">Per avviare l'App-V 5,1 sequencer, nel computer in cui è in corso il Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af09e-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="af09e-114">Nota</span><span class="sxs-lookup"><span data-stu-id="af09e-114">Note</span></span>**  
    <span data-ttu-id="af09e-115">Se il pacchetto di applicazione virtuale è attualmente aperto nella console sequencer di App-V 5,1, passare al passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="af09e-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="af09e-116">Nella console sequencer App-V 5,1 per salvare il file del modello, fare clic su **file**  /  **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="af09e-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="af09e-117">Dopo aver esaminato le impostazioni che verranno salvate con il nuovo modello, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="af09e-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="af09e-118">Specifica un nome che verrà associato al nuovo modello di progetto App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="af09e-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="af09e-119">Fare clic su Salva.</span><span class="sxs-lookup"><span data-stu-id="af09e-119">Click Save.</span></span>

   <span data-ttu-id="af09e-120">Il nuovo modello di progetto App-V 5,1 viene salvato nella directory specificata nel passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="af09e-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="af09e-121">Per applicare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="af09e-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="af09e-122">Importante</span><span class="sxs-lookup"><span data-stu-id="af09e-122">Important</span></span>**  
    <span data-ttu-id="af09e-123">La creazione di un pacchetto di applicazione virtuale con un modello di progetto in combinazione con un Acceleratore pacchetto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="af09e-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="af09e-124">Per creare o aggiornare un nuovo pacchetto di applicazione virtuale usando un modello di progetto App-V 5,1, fare clic su **file**  /  **nuovo da modello**.</span><span class="sxs-lookup"><span data-stu-id="af09e-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="af09e-125">Per selezionare il modello di progetto che si vuole usare, passare alla directory in cui è stato salvato il modello di progetto, selezionare il modello di progetto e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="af09e-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="af09e-126">Creare il nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="af09e-126">Create the new virtual application package.</span></span> <span data-ttu-id="af09e-127">Le impostazioni salvate con il modello specificato verranno applicate al nuovo pacchetto di applicazione virtuale che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="af09e-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="af09e-128">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="af09e-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="af09e-129">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="af09e-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="af09e-130">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="af09e-130">Got an App-V issue?</span></span>** <span data-ttu-id="af09e-131">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="af09e-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="af09e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af09e-132">Related topics</span></span>


[<span data-ttu-id="af09e-133">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="af09e-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









