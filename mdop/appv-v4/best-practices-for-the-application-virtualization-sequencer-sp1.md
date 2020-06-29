---
title: Procedure consigliate per Application Virtualization Sequencer
description: Procedure consigliate per Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821996"
---
# <span data-ttu-id="69492-103">Procedure consigliate per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="69492-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="69492-104">Questo argomento illustra le procedure consigliate per l'uso di Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="69492-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="69492-105">Esaminare e prendere in considerazione i suggerimenti seguenti per la pianificazione e l'uso del sequencer nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="69492-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="69492-106">Sequenziazione delle procedure consigliate per la configurazione del computer</span><span class="sxs-lookup"><span data-stu-id="69492-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="69492-107">Quando si configura il computer che ha eseguito App-V Sequencer, è necessario considerare le procedure consigliate seguenti:</span><span class="sxs-lookup"><span data-stu-id="69492-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="69492-108">Sequenza in un computer con una configurazione simile e che esegua una versione precedente del sistema operativo rispetto ai computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="69492-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="69492-109">Verificare che il computer in cui è in esecuzione Sequencer esegua una versione precedente del sistema operativo rispetto ai computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="69492-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="69492-110">Sono incluse le versioni Service Pack e Update.</span><span class="sxs-lookup"><span data-stu-id="69492-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="69492-111">Ad esempio, se i computer di destinazione eseguono WindowsVista e WindowsXP, dovresti sequenziare le applicazioni in un computer che esegue WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="69492-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="69492-112">La possibilità di sequenziare in un sistema operativo ed eseguire l'applicazione virtualizzata in un sistema operativo diverso non è garantita e dipende dalla particolare applicazione e dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69492-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="69492-113">Se si verificano problemi, potrebbe essere necessario eseguire la sequenza nello stesso ambiente del sistema operativo di quello in cui è in uso il client App-V.</span><span class="sxs-lookup"><span data-stu-id="69492-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="69492-114">Configurare il computer che esegue il sequencer con più partizioni.</span><span class="sxs-lookup"><span data-stu-id="69492-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="69492-115">Devi configurare il computer che esegue il sequencer con almeno due partizioni primarie.</span><span class="sxs-lookup"><span data-stu-id="69492-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="69492-116">La prima partizione (**C:**) deve contenere il sistema operativo e deve essere formattata con il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="69492-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="69492-117">La seconda partizione (**Q:**) viene usata come percorso di destinazione per l'installazione dell'applicazione virtuale e deve essere formattata anche tramite il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="69492-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="69492-118">Configurare la directory Temp con sufficiente spazio disponibile su disco.</span><span class="sxs-lookup"><span data-stu-id="69492-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="69492-119">Il sequencer usa la directory **% tmp%** o **% Temp%** e la directory **Scratch** per archiviare i file temporanei durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="69492-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="69492-120">Queste directory devono essere configurate nel computer in cui è in esecuzione il sequencer con spazio libero su disco equivalente ai requisiti stimati per l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69492-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="69492-121">È possibile verificare la posizione della directory **Scratch** aprendo la console sequencer e selezionando **strumenti**, **Opzioni**e quindi selezionando la scheda **percorsi** . la configurazione delle directory Temp e della directory **Scratch** in partizioni del disco rigido diverse può migliorare le prestazioni durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="69492-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="69492-122">Sequenziare le applicazioni usando Microsoft VirtualPC.</span><span class="sxs-lookup"><span data-stu-id="69492-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="69492-123">La maggior parte delle applicazioni verrà sequenziata più di una volta.</span><span class="sxs-lookup"><span data-stu-id="69492-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="69492-124">Per semplificare questa operazione, è consigliabile eseguire la sequenziazione in un computer in cui è in uso un ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="69492-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="69492-125">In questo modo potrai sequenziare un'applicazione e ripristinare uno stato pulito, con una riconfigurazione minima, nel computer che sta usando sequencer.</span><span class="sxs-lookup"><span data-stu-id="69492-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="69492-126">Se si esegue Microsoft Hyper-V nell'ambiente, l'App-V Sequencer verrà eseguita quando il computer virtuale Hyper-V in cui è in esecuzione è:</span><span class="sxs-lookup"><span data-stu-id="69492-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="69492-127">in pausa e ripresa.</span><span class="sxs-lookup"><span data-stu-id="69492-127">paused and resumed.</span></span>

    -   <span data-ttu-id="69492-128">il relativo stato viene salvato e ripristinato.</span><span class="sxs-lookup"><span data-stu-id="69492-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="69492-129">viene salvato come snapshot e viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="69492-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="69492-130">migrazione a hardware diverso nell'ambito di una migrazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="69492-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="69492-131">Prima di sequenziare una nuova applicazione, arrestare altre applicazioni in uso.</span><span class="sxs-lookup"><span data-stu-id="69492-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="69492-132">I processi e le attività pianificate che in genere vengono eseguiti nel computer di sequenziazione possono rallentare il processo di sequenziazione e causare la raccolta di dati irrilevanti durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="69492-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="69492-133">Tutte le applicazioni e i programmi non necessari devono essere arrestati prima di iniziare la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="69492-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="69492-134">Sequenza in un computer che gestisce servizi Terminal</span><span class="sxs-lookup"><span data-stu-id="69492-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="69492-135">Non è consigliabile configurare la modalità di installazione in un computer che gestisce servizi terminal prima di installare il sequencer.</span><span class="sxs-lookup"><span data-stu-id="69492-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="69492-136">Sequenziazione delle procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="69492-136">Sequencing Best Practices</span></span>


<span data-ttu-id="69492-137">Durante la sequenziazione di una nuova applicazione, è necessario considerare le procedure consigliate seguenti:</span><span class="sxs-lookup"><span data-stu-id="69492-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="69492-138">**Nota**  Se si esegue App-V 4,6 SP1, non è necessario eseguire la sequenza in una directory successiva alla convenzione di denominazione di 8,3.</span><span class="sxs-lookup"><span data-stu-id="69492-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="69492-139">Sequenza a una directory univoca che segue la convenzione di denominazione di 8,3.</span><span class="sxs-lookup"><span data-stu-id="69492-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="69492-140">Devi sequenziare tutte le applicazioni in una directory successiva alla convenzione di denominazione di 8,3.</span><span class="sxs-lookup"><span data-stu-id="69492-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="69492-141">Il nome di directory specificato non può contenere più di otto caratteri, seguiti da un'estensione di file di tre caratteri, ad esempio **Q:\\MYAPP. ABC**.</span><span class="sxs-lookup"><span data-stu-id="69492-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="69492-142">Sequenza in una cartella di destinazione nella radice dell'unità, non in una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="69492-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="69492-143">Se la famiglia di applicazioni ha più parti, installare ogni applicazione in una sottodirectory della directory principale.</span><span class="sxs-lookup"><span data-stu-id="69492-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="69492-144">Ad esempio, se un pacchetto contiene un'applicazione insieme a un client, USA **Q:\\AppSuite** come directory principale e Sequenzia l'applicazione principale in **Q:\\AppSuite\\Main**e Sequenzia il client in **Q:\\AppSuite\\Client**.</span><span class="sxs-lookup"><span data-stu-id="69492-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="69492-145">Configurare e testare l'applicazione durante la fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="69492-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="69492-146">Il completamento dell'installazione di un'applicazione richiede spesso l'esecuzione di più passaggi manuali che non fanno parte del processo di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69492-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="69492-147">Questa procedura può coinvolgere la configurazione di una connessione a un database o la copia di file aggiornati.</span><span class="sxs-lookup"><span data-stu-id="69492-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="69492-148">È consigliabile eseguire queste configurazioni durante la fase di installazione e quindi eseguire l'applicazione per verificare che funzioni.</span><span class="sxs-lookup"><span data-stu-id="69492-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="69492-149">Eseguire l'applicazione, più volte se necessario, finché il programma non è stabile.</span><span class="sxs-lookup"><span data-stu-id="69492-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="69492-150">È consigliabile eseguire l'applicazione più volte durante l'installazione per verificare che tutte le configurazioni della registrazione e della finestra di dialogo associate siano state completate.</span><span class="sxs-lookup"><span data-stu-id="69492-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="69492-151">Quando si apre l'applicazione più volte durante l'installazione, viene garantito che solo le caratteristiche dell'applicazione rilevanti vengano caricate nel **blocco di funzionalità principale**.</span><span class="sxs-lookup"><span data-stu-id="69492-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="69492-152">Disabilitare tutte le funzionalità di aggiornamento automatico associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69492-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="69492-153">Alcune applicazioni hanno la possibilità di verificare automaticamente gli aggiornamenti più recenti durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="69492-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="69492-154">Per facilitare il controllo delle versioni dei pacchetti di applicazioni virtuali, è consigliabile disabilitare questa funzionalità durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="69492-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="69492-155">Se sono presenti aggiornamenti obbligatori, è necessario sequenziare un nuovo pacchetto di applicazione virtuale con gli aggiornamenti associati installati.</span><span class="sxs-lookup"><span data-stu-id="69492-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="69492-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69492-156">Related topics</span></span>


[<span data-ttu-id="69492-157">Pianificazione della distribuzione del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="69492-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





