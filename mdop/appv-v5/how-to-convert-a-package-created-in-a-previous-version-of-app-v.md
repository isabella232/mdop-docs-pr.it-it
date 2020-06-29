---
title: Come convertire un pacchetto creato in una versione precedente di App-V
description: Come convertire un pacchetto creato in una versione precedente di App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805668"
---
# <span data-ttu-id="731c7-103">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="731c7-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="731c7-104">Puoi usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni precedenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="731c7-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="731c7-105">Nota</span><span class="sxs-lookup"><span data-stu-id="731c7-105">Note</span></span>**  
<span data-ttu-id="731c7-106">Se si esegue un computer con un'architettura a 64 bit, è necessario usare la versione x86 di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="731c7-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="731c7-107">Il convertitore di pacchetti può convertire direttamente i pacchetti creati usando l'App-V 4,5 Sequencer o una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="731c7-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="731c7-108">I pacchetti creati con una versione precedente a App-V 4,5 devono essere aggiornati al formato App-V 4,5 o App-V 4,6 prima della conversione.</span><span class="sxs-lookup"><span data-stu-id="731c7-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="731c7-109">Le informazioni seguenti forniscono indicazioni per la conversione di pacchetti di applicazioni virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="731c7-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="731c7-110">Importante</span><span class="sxs-lookup"><span data-stu-id="731c7-110">Important</span></span>**  
<span data-ttu-id="731c7-111">È necessario configurare il convertitore di pacchetti per salvare sempre il file degli ingredienti del pacchetto in un percorso e una directory sicuri.</span><span class="sxs-lookup"><span data-stu-id="731c7-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="731c7-112">Un percorso sicuro è accessibile solo da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="731c7-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="731c7-113">Inoltre, quando si distribuisce il pacchetto, è necessario salvare il pacchetto in una posizione sicura oppure assicurarsi che durante il processo di conversione non sia consentito l'accesso a nessun altro utente.</span><span class="sxs-lookup"><span data-stu-id="731c7-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="731c7-114">Attività iniziali</span><span class="sxs-lookup"><span data-stu-id="731c7-114">Getting started</span></span>**

1.  <span data-ttu-id="731c7-115">Installare App-V Sequencer in un computer nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="731c7-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="731c7-116">Per informazioni su come installare il sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="731c7-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="731c7-117">Importare il modulo di PowerShell necessario</span><span class="sxs-lookup"><span data-stu-id="731c7-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="731c7-118">Sono disponibili i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="731c7-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="731c7-119">Test-AppvLegacyPackage: questo cmdlet è progettato per controllare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="731c7-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="731c7-120">Restituirà informazioni su eventuali errori con il pacchetto, ad esempio file mancanti **. SFT** , un'origine non valida, errori di file **OSD** o una versione del pacchetto non valida.</span><span class="sxs-lookup"><span data-stu-id="731c7-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="731c7-121">Questo cmdlet non analizzerà il file con **estensione SFT** o convaliderà in modo approfondito.</span><span class="sxs-lookup"><span data-stu-id="731c7-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="731c7-122">Per informazioni sulle opzioni e le funzionalità di base per questo cmdlet, usare PowerShell cmdline digitare `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="731c7-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="731c7-123">ConvertFrom-AppvLegacyPackage-per convertire un pacchetto esistente, digitare `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="731c7-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="731c7-124">In questo comando `c:\contentStore` rappresenta la posizione del pacchetto esistente ed `c:\convertedPackages` è la directory di output in cui verrà salvato il file del pacchetto di applicazione virtuale App-V 5,0 risultante.</span><span class="sxs-lookup"><span data-stu-id="731c7-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="731c7-125">Per impostazione predefinita, se non si specifica un nuovo nome, verrà usato il nome del pacchetto precedente per il nome del file App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="731c7-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="731c7-126">Inoltre, il convertitore di pacchetti ottimizza le prestazioni dei pacchetti in App-V 5,0 impostando il pacchetto in streaming fault il pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="731c7-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="731c7-127">Questo è più efficiente del blocco di funzionalità principale e scarica completamente il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="731c7-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="731c7-128">Il contrassegno **DownloadFullPackageOnFirstLaunch** consente di convertire il pacchetto e di impostare il pacchetto da scaricare completamente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="731c7-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="731c7-129">Nota</span><span class="sxs-lookup"><span data-stu-id="731c7-129">Note</span></span>**  
       <span data-ttu-id="731c7-130">Prima di specificare la directory di output, è necessario creare la directory di output.</span><span class="sxs-lookup"><span data-stu-id="731c7-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="731c7-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="731c7-131">Related topics</span></span>


[<span data-ttu-id="731c7-132">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="731c7-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









