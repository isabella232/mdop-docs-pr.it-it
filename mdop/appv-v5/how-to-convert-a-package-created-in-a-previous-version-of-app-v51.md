---
title: Come convertire un pacchetto creato in una versione precedente di App-V
description: Come convertire un pacchetto creato in una versione precedente di App-V
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805667"
---
# <span data-ttu-id="7671b-103">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="7671b-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="7671b-104">Puoi usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni precedenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="7671b-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="7671b-105">Nota</span><span class="sxs-lookup"><span data-stu-id="7671b-105">Note</span></span>**  
<span data-ttu-id="7671b-106">Se si esegue un computer con un'architettura a 64 bit, è necessario usare la versione x86 di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7671b-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="7671b-107">Il convertitore di pacchetti può convertire direttamente i pacchetti creati usando l'App-V 4,5 Sequencer o una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7671b-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="7671b-108">I pacchetti creati con una versione precedente a App-V 4,5 devono essere aggiornati al formato App-V 4,5 o App-V 4,6 prima della conversione.</span><span class="sxs-lookup"><span data-stu-id="7671b-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="7671b-109">Le informazioni seguenti forniscono indicazioni per la conversione di pacchetti di applicazioni virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="7671b-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="7671b-110">Importante</span><span class="sxs-lookup"><span data-stu-id="7671b-110">Important</span></span>**  
<span data-ttu-id="7671b-111">È necessario configurare il convertitore di pacchetti per salvare sempre il file degli ingredienti del pacchetto in un percorso e una directory sicuri.</span><span class="sxs-lookup"><span data-stu-id="7671b-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="7671b-112">Un percorso sicuro è accessibile solo da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="7671b-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="7671b-113">Inoltre, quando si distribuisce il pacchetto, è necessario salvare il pacchetto in una posizione sicura oppure assicurarsi che durante il processo di conversione non sia consentito l'accesso a nessun altro utente.</span><span class="sxs-lookup"><span data-stu-id="7671b-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="7671b-114">La cartella di installazione di App-V 4,6 viene reindirizzata alla radice di Virtual File System</span><span class="sxs-lookup"><span data-stu-id="7671b-114">App-V 4.6 installation folder is redirected to virtual file system root</span></span>**

<span data-ttu-id="7671b-115">Quando si convertono i pacchetti da App-V 4,6 a 5,1, il pacchetto App-V 5,1 può accedere all'unità hardcoded che era necessario usare per la creazione di pacchetti di 4,6.</span><span class="sxs-lookup"><span data-stu-id="7671b-115">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="7671b-116">La lettera dell'unità sarà l'unità selezionata come unità di installazione nel computer di sequenziazione di 4,6.</span><span class="sxs-lookup"><span data-stu-id="7671b-116">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="7671b-117">(La lettera di unità predefinita è Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="7671b-117">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="7671b-118">Prima di App-V 5,1, la cartella radice di 4,6 non è stata riconosciuta e non è stato possibile accedervi dai pacchetti App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7671b-118">Prior to App-V 5.1, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="7671b-119">A questo punto, i pacchetti App-V 5,1 possono accedere ai file codificati in base al percorso completo o possono enumerare i file a livello di codice nella radice dell'installazione di App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="7671b-119">Now, App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="7671b-120">**Dettagli tecnici:** Il convertitore di pacchetti App-V 5,1 salverà la cartella radice dell'installazione di App-V 4,6 e i nomi delle cartelle brevi nel file FilesystemMetadata.xml nell'elemento filesystem.</span><span class="sxs-lookup"><span data-stu-id="7671b-120">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="7671b-121">Quando il client App-V 5,1 crea il processo virtuale, eseguirà il mapping delle richieste dalla radice di installazione di App-V 4,6 alla radice del file system virtuale.</span><span class="sxs-lookup"><span data-stu-id="7671b-121">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

**<span data-ttu-id="7671b-122">Attività iniziali</span><span class="sxs-lookup"><span data-stu-id="7671b-122">Getting started</span></span>**

1.  <span data-ttu-id="7671b-123">Installare App-V Sequencer in un computer nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="7671b-123">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="7671b-124">Per informazioni su come installare il sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="7671b-124">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  

    <span data-ttu-id="7671b-125">Sono disponibili i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="7671b-125">The following cmdlets are available:</span></span>

    -   <span data-ttu-id="7671b-126">Test-AppvLegacyPackage: questo cmdlet è progettato per controllare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="7671b-126">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="7671b-127">Restituirà informazioni su eventuali errori con il pacchetto, ad esempio file mancanti **. SFT** , un'origine non valida, errori di file **OSD** o una versione del pacchetto non valida.</span><span class="sxs-lookup"><span data-stu-id="7671b-127">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="7671b-128">Questo cmdlet non analizzerà il file con **estensione SFT** o convaliderà in modo approfondito.</span><span class="sxs-lookup"><span data-stu-id="7671b-128">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="7671b-129">Per informazioni sulle opzioni e le funzionalità di base per questo cmdlet, usare PowerShell cmdline digitare `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="7671b-129">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

    -   <span data-ttu-id="7671b-130">ConvertFrom-AppvLegacyPackage-per convertire un pacchetto esistente, digitare `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="7671b-130">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="7671b-131">In questo comando `c:\contentStore` rappresenta la posizione del pacchetto esistente ed `c:\convertedPackages` è la directory di output in cui verrà salvato il file del pacchetto di applicazione virtuale App-V 5,1 risultante.</span><span class="sxs-lookup"><span data-stu-id="7671b-131">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.1 virtual application package file will be saved.</span></span> <span data-ttu-id="7671b-132">Per impostazione predefinita, se non si specifica un nuovo nome, verrà usato il nome del pacchetto precedente per il nome del file App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7671b-132">By default, if you do not specify a new name, the old package name will be used for the App-V 5.1 filename.</span></span>

        <span data-ttu-id="7671b-133">Inoltre, il convertitore di pacchetti ottimizza le prestazioni dei pacchetti in App-V 5,1 impostando il pacchetto in streaming fault il pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="7671b-133">Additionally, the package converter optimizes performance of packages in App-V 5.1 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="7671b-134">Questo è più efficiente del blocco di funzionalità principale e scarica completamente il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7671b-134">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="7671b-135">Il contrassegno **DownloadFullPackageOnFirstLaunch** consente di convertire il pacchetto e di impostare il pacchetto da scaricare completamente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7671b-135">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

        **<span data-ttu-id="7671b-136">Nota</span><span class="sxs-lookup"><span data-stu-id="7671b-136">Note</span></span>**  
        <span data-ttu-id="7671b-137">Prima di specificare la directory di output, è necessario creare la directory di output.</span><span class="sxs-lookup"><span data-stu-id="7671b-137">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="7671b-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7671b-138">Related topics</span></span>


[<span data-ttu-id="7671b-139">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="7671b-139">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









