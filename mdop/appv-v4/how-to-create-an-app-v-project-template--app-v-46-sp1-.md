---
title: Come creare un modello di progetto di App-V (App-V 4.6 SP1)
description: Come creare un modello di progetto di App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817646"
---
# <span data-ttu-id="2e4de-103">Come creare un modello di progetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2e4de-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="2e4de-104">Puoi usare un modello di progetto App-V per salvare le impostazioni comunemente applicate associate a un pacchetto di applicazione virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="2e4de-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="2e4de-105">Queste impostazioni possono quindi essere applicate quando crei nuovi pacchetti di applicazioni virtuali nell'ambiente che possono semplificare il processo di creazione di pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="2e4de-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="2e4de-106">**Nota**  Puoi applicare un modello di progetto App-V solo quando crei un nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e4de-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="2e4de-107">L'applicazione di modelli di progetto a pacchetti di applicazioni virtuali esistenti non è supportata.</span><span class="sxs-lookup"><span data-stu-id="2e4de-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="2e4de-108">Per altre informazioni sull'applicazione di un modello di progetto App-V, vedere [come applicare un modello di progetto App-v (app-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="2e4de-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="2e4de-109">I modelli di progetto di App-V si differenziano dagli acceleratori delle applicazioni App-v perché i tasti di scelta rapida dell'applicazione App-V sono specifici dell'applicazione e i modelli di progetto App-V possono essere applicati a più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2e4de-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="2e4de-110">Non è inoltre possibile usare un modello di progetto quando si usa un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e4de-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="2e4de-111">Le impostazioni generali seguenti vengono salvate con un modello di progetto App-V:</span><span class="sxs-lookup"><span data-stu-id="2e4de-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="2e4de-112">**Opzioni di monitoraggio avanzate**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="2e4de-113">Consente l'esecuzione di Microsoft Update durante il monitoraggio, rebase **. dll**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="2e4de-114">**Impostazioni di distribuzione del pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="2e4de-115">Contiene **protocollo**, **nome host**, **porta**, **percorso**, **sistemi operativi**, **applica descrittori di sicurezza**, **Crea MSI**, **Comprimi pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="2e4de-116">**Opzioni generali**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-116">**General Options**.</span></span> <span data-ttu-id="2e4de-117">Consente di generare il pacchetto di **Microsoft Windows Installer (MSI)** , **consentire la virtualizzazione degli eventi**, **consentire la virtualizzazione dei servizi**, **aggiungere la versione del pacchetto al nome del file**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="2e4de-118">**Elementi di esclusione**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-118">**Exclusion Items**.</span></span> <span data-ttu-id="2e4de-119">Contiene l'elenco dei criteri di esclusione.</span><span class="sxs-lookup"><span data-stu-id="2e4de-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="2e4de-120">Per creare un modello di progetto</span><span class="sxs-lookup"><span data-stu-id="2e4de-120">To create a project template</span></span>**

1.  <span data-ttu-id="2e4de-121">Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="2e4de-122">Se il pacchetto di applicazione virtuale è attualmente aperto in App-V Sequencer, passare al passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="2e4de-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="2e4de-123">Per aprire il pacchetto di applicazione virtuale esistente che contiene le impostazioni che si vuole salvare con il modello di progetto App-V, fare clic su **file**  /  **aperto** e quindi su **modifica** **pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="2e4de-124">Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** e individuare il pacchetto di applicazione virtuale che si vuole aprire.</span><span class="sxs-lookup"><span data-stu-id="2e4de-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="2e4de-125">Fai clic su **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="2e4de-126">Nella console App-V Sequencer fare clic su **file**  /  **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="2e4de-127">Dopo aver esaminato le impostazioni che verranno salvate con il nuovo modello, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="2e4de-128">Specifica un nome che verrà associato al nuovo modello di progetto App-V.</span><span class="sxs-lookup"><span data-stu-id="2e4de-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="2e4de-129">Fare clic su **Save**.</span><span class="sxs-lookup"><span data-stu-id="2e4de-129">Click **Save**.</span></span>

    <span data-ttu-id="2e4de-130">Il nuovo modello di progetto App-V viene salvato nella directory specificata nel passaggio 3 di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="2e4de-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="2e4de-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e4de-131">Related topics</span></span>


[<span data-ttu-id="2e4de-132">Attività per Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2e4de-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="2e4de-133">Come applicare un modello di progetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="2e4de-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





