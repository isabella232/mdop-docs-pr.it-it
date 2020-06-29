---
title: Come creare e usare un modello di progetto
description: Come creare e usare un modello di progetto
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805595"
---
# <span data-ttu-id="f3d77-103">Come creare e usare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="f3d77-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="f3d77-104">Puoi usare un modello di progetto App-V 5,0 per salvare le impostazioni comunemente applicate associate a un pacchetto di applicazione virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="f3d77-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="f3d77-105">Queste impostazioni possono quindi essere applicate quando crei nuovi pacchetti di applicazioni virtuali nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="f3d77-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="f3d77-106">L'uso di un modello di progetto consente di semplificare il processo di creazione di pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="f3d77-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="f3d77-107">**Nota**  È possibile e spesso deve applicare un modello di progetto App-V 5,0 durante l'aggiornamento di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f3d77-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="f3d77-108">Se ad esempio è stata sequenziata un'applicazione con un elenco di esclusione personalizzato, è consigliabile creare e salvare un modello associato per l'uso successivo durante l'aggiornamento dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="f3d77-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="f3d77-109">I modelli di progetto di App-V 5,0 si differenziano dagli acceleratori delle applicazioni App-V 5,0 perché gli acceleratori di applicazioni App-V 5,0 sono specifici dell'applicazione e i modelli di progetto di App-V 5,0 possono essere applicati a più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3d77-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="f3d77-110">Usare le procedure seguenti per creare e applicare un nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="f3d77-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="f3d77-111">Per creare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="f3d77-111">To create a project template</span></span>**

1.  <span data-ttu-id="f3d77-112">Per avviare l'App-V 5,0 sequencer, nel computer in cui è in corso il Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3d77-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="f3d77-113">**Nota**  Se il pacchetto di applicazione virtuale è attualmente aperto nella console sequencer di App-V 5,0, passare al passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="f3d77-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="f3d77-114">Per aprire il pacchetto di applicazione virtuale esistente che contiene le impostazioni che si desidera salvare con il modello di progetto App-V 5,0, fare clic su **file**  /  **aperto**e quindi su **modifica pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="f3d77-115">Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** e individuare il pacchetto di applicazione virtuale che si vuole aprire.</span><span class="sxs-lookup"><span data-stu-id="f3d77-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="f3d77-116">Fai clic su **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-116">Click **Edit**.</span></span>

3. <span data-ttu-id="f3d77-117">Nella console sequencer App-V 5,0 per salvare il file del modello, fare clic su **file**  /  **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="f3d77-118">Dopo aver esaminato le impostazioni che verranno salvate con il nuovo modello, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="f3d77-119">Specifica un nome che verrà associato al nuovo modello di progetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f3d77-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="f3d77-120">Fare clic su Salva.</span><span class="sxs-lookup"><span data-stu-id="f3d77-120">Click Save.</span></span>
   <span data-ttu-id="f3d77-121">Il nuovo modello di progetto App-V 5,0 viene salvato nella directory specificata nel passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="f3d77-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="f3d77-122">Per applicare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="f3d77-122">To apply a project template</span></span>**

<span data-ttu-id="f3d77-123">**Importante**  La creazione di un pacchetto di applicazione virtuale con un modello di progetto in combinazione con un Acceleratore pacchetto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="f3d77-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="f3d77-124">Per avviare l'App-V 5,0 sequencer, nel computer in cui è in corso il Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3d77-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="f3d77-125">Per creare o aggiornare un nuovo pacchetto di applicazione virtuale usando un modello di progetto App-V 5,0, fare clic su **file**  /  **nuovo da modello**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="f3d77-126">Per selezionare il modello di progetto che si vuole usare, passare alla directory in cui è stato salvato il modello di progetto, selezionare il modello di progetto e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="f3d77-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="f3d77-127">Creare il nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3d77-127">Create the new virtual application package.</span></span> <span data-ttu-id="f3d77-128">Le impostazioni salvate con il modello specificato verranno applicate al nuovo pacchetto di applicazione virtuale che si sta creando.</span><span class="sxs-lookup"><span data-stu-id="f3d77-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="f3d77-129">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="f3d77-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f3d77-130">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f3d77-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f3d77-131">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="f3d77-131">Got an App-V issue?</span></span>** <span data-ttu-id="f3d77-132">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f3d77-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f3d77-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3d77-133">Related topics</span></span>


[<span data-ttu-id="f3d77-134">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f3d77-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









