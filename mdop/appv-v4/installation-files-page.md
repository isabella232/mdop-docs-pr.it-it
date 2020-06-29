---
title: Pagina File di installazione
description: Pagina File di installazione
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816345"
---
# <span data-ttu-id="d2ca4-103">Pagina File di installazione</span><span class="sxs-lookup"><span data-stu-id="d2ca4-103">Installation Files Page</span></span>


<span data-ttu-id="d2ca4-104">Usare la pagina **file di installazione** per specificare i file di installazione usati per creare il pacchetto di applicazione virtuale specificato nella pagina **Seleziona pacchetto** della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="d2ca4-105">Se è stato creato un pacchetto di applicazione virtuale che contiene più applicazioni, è consigliabile copiare tutti i file di installazione necessari in una singola cartella nel computer in cui è installato Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="d2ca4-106">Questa pagina contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2ca4-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="d2ca4-107">File di installazione originali</span><span class="sxs-lookup"><span data-stu-id="d2ca4-107">Original Installation Files</span></span>**  
<span data-ttu-id="d2ca4-108">Fare clic su **Sfoglia** per specificare i file di installazione usati in origine per creare il pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="d2ca4-109">La directory padre specificata deve essere salvata localmente nel computer che esegue il sequencer e deve contenere tutti i file di installazione necessari o le sottocartelle che contengono i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="d2ca4-110">I file di installazione possono essere contenuti nella cartella padre o in una delle sottocartelle della cartella padre specificata.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="d2ca4-111">File installati nel sistema locale</span><span class="sxs-lookup"><span data-stu-id="d2ca4-111">Files installed on local system</span></span>**  
<span data-ttu-id="d2ca4-112">Fare clic su **Sfoglia** per specificare i file di installazione installati localmente nel computer in cui è in uso Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="d2ca4-113">Puoi selezionare questa opzione solo se i file di installazione dell'applicazione sono stati installati nella posizione predefinita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="d2ca4-114">**Nota**  Il percorso di installazione predefinito fornito dipende dalle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2ca4-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="d2ca4-115">Radice del pacchetto specificata quando il pacchetto è stato creato in origine.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="d2ca4-116">Il percorso di installazione specificato in Windows Installer quando il pacchetto è stato creato in origine.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="d2ca4-117">Percorso di installazione dell'applicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-117">The default application installation path.</span></span>

<span data-ttu-id="d2ca4-118">Ad esempio, se la radice del pacchetto specificata è **Q:\\Office12** e durante l'installazione, il percorso di installazione predefinito viene modificato da **C:\\Programmi Files\\Office12** a **Q:\\Office12**, il percorso specificato durante la disidratazione deve essere **c:\\Programmi Files\\Office 12**.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="d2ca4-119">Se la radice del pacchetto specificata è **Q:\\Microsoft** e durante l'installazione, la posizione di installazione predefinita viene modificata da **C:\\Programmi Files\\Office12** a **Q:\\Microsoft\\Office12**, il percorso specificato durante la disidratazione deve essere **c:\\Programmi file**.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="d2ca4-120">Quando crei un pacchetto usando un acceleratore di pacchetto, ogni file nel pacchetto, ad esempio **Q:\\Office12\\file.txt** si trova nel computer locale sostituendo il pacchetto radice **Q:\\Office12** con il percorso predefinito specificato quando è stato creato l'acceleratore del pacchetto, ad esempio **c:\\Programmi Files\\Office12**.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="d2ca4-121">Nell'esempio precedente il file deve trovarsi in **c:\\programmi Files\\Office12\\file.txt**.</span><span class="sxs-lookup"><span data-stu-id="d2ca4-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="d2ca4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2ca4-122">Related topics</span></span>


[<span data-ttu-id="d2ca4-123">Procedura guidata Crea Acceleratore pacchetto (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d2ca4-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





