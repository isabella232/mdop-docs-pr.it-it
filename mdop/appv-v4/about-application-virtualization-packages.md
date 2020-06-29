---
title: Informazioni sui pacchetti di Application Virtualization
description: Informazioni sui pacchetti di Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820085"
---
# <span data-ttu-id="2f125-103">Informazioni sui pacchetti di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2f125-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="2f125-104">Nella virtualizzazione delle applicazioni, un *pacchetto* è l'output del processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="2f125-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="2f125-105">Si usano i pacchetti per la prima volta che si distribuiscono applicazioni nei server e quando si aggiornano le applicazioni con una nuova versione.</span><span class="sxs-lookup"><span data-stu-id="2f125-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="2f125-106">I pacchetti consentono di controllare le versioni delle applicazioni virtuali nei server di gestione della virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f125-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="2f125-107">Un singolo pacchetto può contenere una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2f125-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="2f125-108">Ogni pacchetto di applicazione contiene un set di file come unità indipendente.</span><span class="sxs-lookup"><span data-stu-id="2f125-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="2f125-109">Gestione dei pacchetti</span><span class="sxs-lookup"><span data-stu-id="2f125-109">Managing Packages</span></span>


<span data-ttu-id="2f125-110">Dopo che il Sequencer crea un pacchetto di una o più applicazioni durante il processo, è possibile copiare i file generati dal sequencer in un server di gestione della virtualizzazione delle applicazioni e renderli disponibili per il flusso.</span><span class="sxs-lookup"><span data-stu-id="2f125-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="2f125-111">I pacchetti disponibili vengono visualizzati sotto il contenitore **pacchetti** nel riquadro sinistro della console di gestione di Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2f125-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="2f125-112">Quando si importa un'applicazione con un file di progetto sequencer (SPRJ) o un file OSD (Open Software Descriptor), nel contenitore **pacchetti** viene visualizzata una voce correlata.</span><span class="sxs-lookup"><span data-stu-id="2f125-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="2f125-113">Dalla console di gestione di Application Virtualization Server è quindi possibile distribuire, aggiornare o eliminare pacchetti e versioni.</span><span class="sxs-lookup"><span data-stu-id="2f125-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="2f125-114">Ogni applicazione virtuale ha un pacchetto associato.</span><span class="sxs-lookup"><span data-stu-id="2f125-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="2f125-115">Questo pacchetto include i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f125-115">This package includes the following files:</span></span>

-   <span data-ttu-id="2f125-116">SFT-il file che trasmette l'applicazione ai client.</span><span class="sxs-lookup"><span data-stu-id="2f125-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="2f125-117">OSD: il file Open Software Descriptor contiene le informazioni necessarie per trovare e avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f125-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="2f125-118">ICO: il file icona che rappresenta visivamente l'applicazione in interfacce utente e tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="2f125-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="2f125-119">SPRJ-il file di progetto Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f125-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="2f125-120">Quando si importa il file SPRJ, per impostazione predefinita tutte le applicazioni sequenziate sono disponibili per la distribuzione, ma le applicazioni non sono abilitate per il flusso.</span><span class="sxs-lookup"><span data-stu-id="2f125-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="2f125-121">Puoi scegliere di eseguire il flusso di tutte o alcune delle applicazioni nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f125-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="2f125-122">Se ad esempio è stato sequenziato e importato Microsoft Office, è possibile scegliere di non distribuire alcune applicazioni, ad esempio la procedura guidata Salva impostazioni personali.</span><span class="sxs-lookup"><span data-stu-id="2f125-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="2f125-123">In questo caso, fare clic con il pulsante destro del mouse su ogni applicazione che si vuole distribuire, scegliere **Proprietà**e verificare che la casella **abilitato** sia deselezionata (vuota).</span><span class="sxs-lookup"><span data-stu-id="2f125-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="2f125-124">Solo le applicazioni con la casella **attivata** verranno trasmesse ai computer client.</span><span class="sxs-lookup"><span data-stu-id="2f125-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="2f125-125">Dopo aver risequenziato un pacchetto e prodotto un nuovo file SFT per lo streaming, è possibile aggiornare il vecchio pacchetto in modo semplice e veloce tramite la console di gestione dei server Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2f125-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="2f125-126">L'unico scenario operativo che richiede l'uso del nodo **packages** è quando si introduce una nuova versione (file SFT) per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f125-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="2f125-127">Ogni volta che si importano applicazioni, si assegnano accessi e licenze alle applicazioni e così via, il sistema di virtualizzazione delle applicazioni tiene traccia di queste informazioni a livello di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f125-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="2f125-128">Ciò significa che quando si autorizza un utente a usare un'applicazione, si sta dando all'utente l'autorizzazione per eseguire qualsiasi applicazione nello stesso pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f125-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="2f125-129">Versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="2f125-129">Package Version</span></span>

<span data-ttu-id="2f125-130">Una versione del pacchetto è rappresentata da un file SFT specifico.</span><span class="sxs-lookup"><span data-stu-id="2f125-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="2f125-131">Quando si aggiorna un pacchetto (si applica un aggiornamento a un'applicazione o si aggiunge un'applicazione a un pacchetto), si genera un nuovo file SFT.</span><span class="sxs-lookup"><span data-stu-id="2f125-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="2f125-132">Ogni volta che si crea un nuovo file SFT, si crea una nuova versione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f125-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="2f125-133">Quando si importano applicazioni tramite la console di gestione di Application Virtualization Server, il software crea automaticamente un pacchetto e una versione del pacchetto, se non sono già presenti.</span><span class="sxs-lookup"><span data-stu-id="2f125-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="2f125-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f125-134">Related topics</span></span>


[<span data-ttu-id="2f125-135">Informazioni sulle applicazioni di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="2f125-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="2f125-136">Informazioni su Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="2f125-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="2f125-137">Come gestire i pacchetti in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="2f125-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





