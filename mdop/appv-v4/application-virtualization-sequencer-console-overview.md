---
title: Panoramica di Application Virtualization Sequencer Console
description: Panoramica di Application Virtualization Sequencer Console
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822195"
---
# <span data-ttu-id="62b31-103">Panoramica di Application Virtualization Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="62b31-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="62b31-104">Application Virtualization (App-V) Sequencer crea applicazioni in modo che possano essere eseguite in un ambiente virtuale, come applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="62b31-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="62b31-105">Dopo che un'applicazione è stata sequenziata, può essere eseguita da un server App-V per indirizzare i computer che eseguono il client Desktop App-V o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando un processo denominato flusso.</span><span class="sxs-lookup"><span data-stu-id="62b31-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="62b31-106">App-V Sequencer monitora il processo di installazione e configurazione per le applicazioni e registra tutte le informazioni necessarie per l'esecuzione dell'applicazione nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b31-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="62b31-107">Questo processo determina anche i file e le configurazioni applicabili a tutti gli utenti e alle configurazioni che gli utenti possono personalizzare.</span><span class="sxs-lookup"><span data-stu-id="62b31-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="62b31-108">Le applicazioni virtuali vengono eseguite nei computer di destinazione e non hanno alcun effetto sul sistema operativo in esecuzione nel computer di destinazione o in tutte le applicazioni installate nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62b31-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="62b31-109">Considerazioni sulla sicurezza di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="62b31-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="62b31-110">App-V Sequencer esegue tutti i servizi rilevati in fase di sequenziazione usando l'account di sistema locale e non applica i descrittori di sicurezza sulle richieste di controllo del servizio.</span><span class="sxs-lookup"><span data-stu-id="62b31-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="62b31-111">Se il servizio è stato installato con un account utente diverso o se i descrittori di sicurezza hanno lo scopo di concedere autorizzazioni di servizio specifiche per gruppi di utenti diversi, valutare attentamente se il servizio deve essere virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="62b31-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="62b31-112">In alcuni casi, è necessario installare il servizio localmente per verificare che la sicurezza del servizio prevista venga mantenuta.</span><span class="sxs-lookup"><span data-stu-id="62b31-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="62b31-113">Opzioni del menu console di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="62b31-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="62b31-114">Le voci di menu seguenti sono disponibili nella console App-V Sequencer:</span><span class="sxs-lookup"><span data-stu-id="62b31-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="62b31-115">**File**: contiene vari comandi per facilitare la creazione, l'apertura, la modifica e la salvataggio di applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="62b31-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="62b31-116">**Modifica**: contiene vari comandi per la modifica delle applicazioni virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="62b31-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="62b31-117">**Visualizzazione**: contiene vari comandi per la visualizzazione delle proprietà di un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b31-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="62b31-118">**Tools**: contiene vari strumenti e diagnostica per la configurazione delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="62b31-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="62b31-119">Opzioni della barra degli strumenti console di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="62b31-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="62b31-120">I pulsanti della barra degli strumenti seguenti sono disponibili nella console App-V Sequencer:</span><span class="sxs-lookup"><span data-stu-id="62b31-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="62b31-121">**Nuovo pacchetto**: fare clic per creare una nuova applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="62b31-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="62b31-122">**Apri**: fare clic per aprire un pacchetto di applicazione sequenziata nella console App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="62b31-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="62b31-123">**Apri per l'aggiornamento**: fare clic per aprire un'applicazione sequenziata per aggiornare o applicare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="62b31-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="62b31-124">**Salva**: fare clic per salvare un'applicazione virtuale sequenziata.</span><span class="sxs-lookup"><span data-stu-id="62b31-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="62b31-125">**Sequenziazione guidata**: fare clic per aprire la procedura guidata di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="62b31-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="62b31-126">Questo pulsante deve essere usato per avviare la sequenziazione guidata se si apportano modifiche nella scheda **generale** in **Tools**  /  **Opzioni**strumenti.</span><span class="sxs-lookup"><span data-stu-id="62b31-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="62b31-127">Schede delle applicazioni virtuali</span><span class="sxs-lookup"><span data-stu-id="62b31-127">Virtual Application Tabs</span></span>


<span data-ttu-id="62b31-128">Le schede seguenti vengono visualizzate quando si visualizza un'applicazione virtuale nella console App-V Sequencer:</span><span class="sxs-lookup"><span data-stu-id="62b31-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="62b31-129">**Proprietà**: Visualizza le informazioni sull'applicazione virtuale selezionata.</span><span class="sxs-lookup"><span data-stu-id="62b31-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="62b31-130">È possibile aggiornare il **nome del pacchetto** e i **Commenti** associati all'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b31-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="62b31-131">**Distribuzione**: Visualizza le informazioni sul modo in cui l'applicazione virtuale sarà accessibile dai computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62b31-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="62b31-132">Puoi configurare il metodo di recapito dell'applicazione virtuale ed è possibile configurare i sistemi operativi che devono essere in esecuzione nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62b31-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="62b31-133">È anche possibile configurare le opzioni di output associate.</span><span class="sxs-lookup"><span data-stu-id="62b31-133">You can also configure the associated output options.</span></span> <span data-ttu-id="62b31-134">Se si prevede che i client accedano a un'applicazione virtuale da un file, usare il formato seguente quando si specifica il percorso: **file://server/share/Path/.SFT**.</span><span class="sxs-lookup"><span data-stu-id="62b31-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="62b31-135">Selezionare **applica descrittori di sicurezza** per mantenere la sicurezza associata al pacchetto durante un aggiornamento o le autorizzazioni verranno reimpostate durante l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="62b31-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="62b31-136">**Modifica cronologia**: Visualizza le informazioni sugli aggiornamenti apportati all'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b31-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="62b31-137">**File**: Visualizza i file associati all'applicazione virtuale selezionata.</span><span class="sxs-lookup"><span data-stu-id="62b31-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="62b31-138">Puoi apportare piccole revisioni alle proprietà del file associate usando i campi appropriati.</span><span class="sxs-lookup"><span data-stu-id="62b31-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="62b31-139">**Registro di sistema virtuale**: Visualizza il registro di sistema virtuale associato all'applicazione virtuale selezionata.</span><span class="sxs-lookup"><span data-stu-id="62b31-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="62b31-140">È possibile aggiungere o eliminare le chiavi del registro di sistema facendo clic con il pulsante destro del mouse sulla voce appropriata.</span><span class="sxs-lookup"><span data-stu-id="62b31-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="62b31-141">**File system virtuale**: Visualizza i sistemi di file virtuali associati all'applicazione virtuale selezionata.</span><span class="sxs-lookup"><span data-stu-id="62b31-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="62b31-142">È possibile aggiungere, eliminare o modificare le voci di file System in questa scheda facendo clic con il pulsante destro del mouse sulla voce appropriata e scegliendo l'opzione.</span><span class="sxs-lookup"><span data-stu-id="62b31-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="62b31-143">**Servizi virtuali**: Visualizza i servizi associati all'applicazione virtuale selezionata.</span><span class="sxs-lookup"><span data-stu-id="62b31-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="62b31-144">**OSD**: Visualizza informazioni sul descrittore software aperto (OSD) associato all'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b31-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="62b31-145">È possibile aggiornare i file associati al file OSD facendo clic con il pulsante destro del mouse sulla voce appropriata e selezionando l'azione desiderata.</span><span class="sxs-lookup"><span data-stu-id="62b31-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="62b31-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62b31-146">Related topics</span></span>


[<span data-ttu-id="62b31-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="62b31-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





