---
title: Informazioni su Application Virtualization Sequencer
description: Informazioni su Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819996"
---
# <span data-ttu-id="afbab-103">Informazioni su Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="afbab-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="afbab-104">Microsoft Application Virtualization (App-V) Sequencer monitora e registra tutti i processi di installazione e configurazione per un'applicazione e crea i file seguenti: **ico**, **OSD**, **SFT**e **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="afbab-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="afbab-105">Questi file contengono tutte le informazioni necessarie su un'applicazione in modo che l'applicazione possa essere eseguita in un ambiente virtuale nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="afbab-106">Puoi usare Microsoft Application Virtualization (App-V) Sequencer per creare applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="afbab-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="afbab-107">Dopo aver sequenziato un'applicazione, è possibile eseguirne il flusso per i computer di destinazione oppure i computer di destinazione possono eseguire l'applicazione virtuale scaricando il contenuto del pacchetto di applicazione virtuale ed eseguendo l'applicazione localmente.</span><span class="sxs-lookup"><span data-stu-id="afbab-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="afbab-108">**Importante**  Per eseguire un pacchetto di applicazione virtuale, il computer di destinazione deve eseguire la versione appropriata del client App-V.</span><span class="sxs-lookup"><span data-stu-id="afbab-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="afbab-109">I pacchetti di applicazioni virtuali vengono eseguiti nei computer di destinazione senza interagire con il sistema operativo sottostante nel computer di destinazione, perché ogni applicazione viene eseguita in un ambiente virtuale ed è isolata da altre applicazioni installate o in esecuzione nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="afbab-110">Questo isolamento può ridurre i conflitti tra le applicazioni e può contribuire a diminuire la quantità necessaria di test pre-distribuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="afbab-111">Terminologia Sequencer</span><span class="sxs-lookup"><span data-stu-id="afbab-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="afbab-112">Unità di virtualizzazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="afbab-112">Application Virtualization drive</span></span>  
<span data-ttu-id="afbab-113">L'unità di virtualizzazione dell'applicazione è l'unità predefinita (Q:\) nel computer di destinazione in cui vengono eseguite le applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="afbab-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="afbab-114">File ICO</span><span class="sxs-lookup"><span data-stu-id="afbab-114">ICO file</span></span>  
<span data-ttu-id="afbab-115">Il file dell'icona sul desktop client che viene usato per avviare un'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="afbab-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="afbab-116">Directory di installazione</span><span class="sxs-lookup"><span data-stu-id="afbab-116">Installation directory</span></span>  
<span data-ttu-id="afbab-117">Directory utilizzata dal sequencer per inserire i file di installazione durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="afbab-118">File OSD (Open Software Descriptor)</span><span class="sxs-lookup"><span data-stu-id="afbab-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="afbab-119">Un file basato su XML che indica al client App-V come recuperare l'applicazione sequenziata dall'App-V Streaming Server e come eseguire l'applicazione sequenziata nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="afbab-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="afbab-120">Directory radice del pacchetto</span><span class="sxs-lookup"><span data-stu-id="afbab-120">Package root directory</span></span>  
<span data-ttu-id="afbab-121">Directory nel computer di sequenziazione in cui sono installati i file per il pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="afbab-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="afbab-122">Questa directory esiste anche virtualmente nel computer in cui verrà trasmessa un'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="afbab-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="afbab-123">Applicazione sequenziata</span><span class="sxs-lookup"><span data-stu-id="afbab-123">Sequenced application</span></span>  
<span data-ttu-id="afbab-124">Un'applicazione monitorata dal sequencer, suddivisa in blocchi di funzionalità primari e secondari, in streaming in un computer di destinazione in cui è in esecuzione l'App-V Client t e viene eseguito un ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="afbab-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="afbab-125">Pacchetto di applicazione sequenziata</span><span class="sxs-lookup"><span data-stu-id="afbab-125">Sequenced application package</span></span>  
<span data-ttu-id="afbab-126">I file che includono un'applicazione virtuale e consentono l'esecuzione di un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="afbab-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="afbab-127">Questi file vengono creati dopo la sequenziazione e includono in particolare i file **OSD**, **SFT**, **SPRJ**e **ico** .</span><span class="sxs-lookup"><span data-stu-id="afbab-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="afbab-128">Sequenziamento</span><span class="sxs-lookup"><span data-stu-id="afbab-128">Sequencing</span></span>  
<span data-ttu-id="afbab-129">Processo di creazione di un pacchetto dell'applicazione tramite App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="afbab-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="afbab-130">In questo processo viene monitorata un'applicazione, vengono configurati i tasti di scelta rapida e viene creato un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="afbab-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="afbab-131">Sequenziazione del computer</span><span class="sxs-lookup"><span data-stu-id="afbab-131">Sequencing computer</span></span>  
<span data-ttu-id="afbab-132">Il computer usato per sequenziare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="afbab-133">Applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="afbab-133">Virtual application</span></span>  
<span data-ttu-id="afbab-134">Un'applicazione imballata dal sequencer per l'esecuzione in un ambiente virtuale indipendente.</span><span class="sxs-lookup"><span data-stu-id="afbab-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="afbab-135">L'ambiente virtuale contiene le informazioni necessarie per eseguire l'applicazione nel client senza installare l'applicazione localmente.</span><span class="sxs-lookup"><span data-stu-id="afbab-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="afbab-136">Blocco di funzionalità principale</span><span class="sxs-lookup"><span data-stu-id="afbab-136">Primary feature block</span></span>  
<span data-ttu-id="afbab-137">Il contenuto minimo in un pacchetto di applicazione virtuale necessario per l'esecuzione di un'applicazione in un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="afbab-138">Il contenuto del blocco di funzionalità principale viene identificato durante la fase di applicazione della sequenziazione e in genere è costituito dal contenuto per le caratteristiche dell'applicazione più usate.</span><span class="sxs-lookup"><span data-stu-id="afbab-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="afbab-139">Sequenziazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="afbab-139">Sequencing Applications</span></span>


<span data-ttu-id="afbab-140">Esistono due metodi per creare e modificare pacchetti di applicazioni virtuali nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="afbab-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="afbab-141">Il primo metodo consiste nell'usare la **sequenziazione** guidata.</span><span class="sxs-lookup"><span data-stu-id="afbab-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="afbab-142">La **sequenziazione** guidata consente di creare nuovi o modificare i pacchetti di applicazioni virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="afbab-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="afbab-143">Per altre informazioni sull'uso della procedura guidata per la **sequenziazione** , vedere [come sequenziare una nuova applicazione](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="afbab-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="afbab-144">Il secondo metodo consiste nell'usare la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="afbab-144">The second method is by using the command-line.</span></span> <span data-ttu-id="afbab-145">La riga di comando consente di creare nuovi o modificare pacchetti di applicazioni virtuali esistenti tramite il prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="afbab-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="afbab-146">Per altre informazioni sull'uso della riga di comando, vedere [come gestire le applicazioni virtuali tramite la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="afbab-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="afbab-147">La **sequenziazione** guidata offre le funzioni seguenti per la creazione di pacchetti di applicazioni virtuali:</span><span class="sxs-lookup"><span data-stu-id="afbab-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="afbab-148">**Configurazione del pacchetto**: la **sequenziazione** guidata richiede le informazioni di configurazione del pacchetto necessarie per completare il file OSD (Open Software Descriptor), che è un file obbligatorio per l'avvio di un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="afbab-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="afbab-149">**Installazione dell'applicazione**: la **sequenziazione** guidata raccoglie informazioni sulle configurazioni di installazione e avvio di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="afbab-150">Monitora e registra le informazioni di installazione e avvio associate all'applicazione per creare i file necessari per un pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="afbab-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="afbab-151">**Avvio di un'applicazione**: la **sequenziazione** guidata raccoglie informazioni per la compilazione e l'ordinamento dei blocchi di codice necessari per eseguire l'avvio iniziale del pacchetto di applicazione sequenziata nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afbab-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="afbab-152">La compilazione del blocco di codice viene definita blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="afbab-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="afbab-153">Considerazioni sulla sicurezza di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="afbab-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="afbab-154">App-V Sequencer esegue tutti i servizi rilevati in fase di sequenziazione usando l'account di sistema locale e non applica i descrittori di sicurezza sulle richieste di controllo del servizio.</span><span class="sxs-lookup"><span data-stu-id="afbab-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="afbab-155">Se il servizio è stato installato con un account utente diverso o se i descrittori di sicurezza hanno lo scopo di concedere autorizzazioni di servizio specifiche per gruppi di utenti diversi, valutare attentamente se il servizio deve essere virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="afbab-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="afbab-156">In alcuni casi, è necessario installare il servizio localmente per verificare che la sicurezza del servizio prevista venga mantenuta.</span><span class="sxs-lookup"><span data-stu-id="afbab-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="afbab-157">**Importante**  È consigliabile salvare sempre i pacchetti di applicazioni virtuali in una posizione sicura.</span><span class="sxs-lookup"><span data-stu-id="afbab-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="afbab-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="afbab-158">Related topics</span></span>


[<span data-ttu-id="afbab-159">Panoramica di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="afbab-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





