---
title: Progettare i repository delle immagini MED-V
description: Progettare i repository delle immagini MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823615"
---
# <span data-ttu-id="d8da4-103">Progettare i repository delle immagini MED-V</span><span class="sxs-lookup"><span data-stu-id="d8da4-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="d8da4-104">Dopo che le immagini MED-V vengono create e imballate, possono essere archiviate in un file server in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="d8da4-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="d8da4-105">I file possono essere inviati tramite HTTP o HTTPS da uno o più server IIS.</span><span class="sxs-lookup"><span data-stu-id="d8da4-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="d8da4-106">Il repository di immagini può essere condiviso da più istanze di MED-V.</span><span class="sxs-lookup"><span data-stu-id="d8da4-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="d8da4-107">Per progettare i repository di immagini, è prima di tutto necessario decidere in che modo verranno distribuite le immagini in ogni client e quindi se tale client richiede un repository di immagini locale.</span><span class="sxs-lookup"><span data-stu-id="d8da4-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="d8da4-108">Ogni repository viene quindi progettato e posizionato, insieme al server IIS che lo accompagna.</span><span class="sxs-lookup"><span data-stu-id="d8da4-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="d8da4-109">Determinare il modo in cui verranno distribuite le immagini</span><span class="sxs-lookup"><span data-stu-id="d8da4-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="d8da4-110">Per ogni area di lavoro MED-V, decidere in che modo pianificare la distribuzione di immagini MED-V nel client.</span><span class="sxs-lookup"><span data-stu-id="d8da4-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="d8da4-111">Questo è importante per determinare il numero di repository necessari per archiviare le immagini imballate, in cui verranno posizionati questi repository e quindi per progettare questi repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="d8da4-112">Le immagini imballate possono essere distribuite nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8da4-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="d8da4-113">Scaricati tramite rete da un server di distribuzione delle immagini, che include un file server e un server IIS.</span><span class="sxs-lookup"><span data-stu-id="d8da4-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="d8da4-114">Su supporti rimovibili, ad esempio un'unità USB o un DVD.</span><span class="sxs-lookup"><span data-stu-id="d8da4-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="d8da4-115">Preallestito in una directory dello Store di immagini nel computer client usando un centro di distribuzione del software aziendale.</span><span class="sxs-lookup"><span data-stu-id="d8da4-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="d8da4-116">Decidi quale metodo o i metodi verranno usati per distribuire le immagini MED-V in ognuno dei client e se la posizione richiederà un repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="d8da4-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="d8da4-117">Determinare il numero di repository di immagini</span><span class="sxs-lookup"><span data-stu-id="d8da4-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="d8da4-118">Dopo aver determinato il numero minimo di repository necessari, aggiungere altro se si applicano i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8da4-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="d8da4-119">Motivi di organizzazione o di regolamentazione per separare le immagini MED-V: alcune immagini MED-V potrebbero non essere in grado di coesistere nello stesso repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="d8da4-120">Ad esempio, i dati personali riservati possono richiedere spazio di archiviazione su un server disponibile solo per un set limitato di dipendenti che hanno bisogno di accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="d8da4-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="d8da4-121">Client in reti isolate: se le immagini verranno distribuite tramite la rete, determinare se le reti sono isolate e richiedono un repository separato.</span><span class="sxs-lookup"><span data-stu-id="d8da4-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="d8da4-122">Ad esempio, le organizzazioni spesso isolano le reti Lab dalle reti di produzione.</span><span class="sxs-lookup"><span data-stu-id="d8da4-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="d8da4-123">Client in reti remote: se le immagini verranno distribuite tramite la rete, alcuni computer client potrebbero essere separati dal repository da collegamenti di rete con una larghezza di banda insufficiente per offrire un'esperienza adeguata quando un client carica un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d8da4-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="d8da4-124">Se necessario, progetta altre istanze di MED-V per rispondere a questa esigenza.</span><span class="sxs-lookup"><span data-stu-id="d8da4-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="d8da4-125">Aggiungere questi repository alla struttura.</span><span class="sxs-lookup"><span data-stu-id="d8da4-125">Add these repositories to the design.</span></span> <span data-ttu-id="d8da4-126">Scegliere un nome per ogni repository e il motivo per cui è stato progettato.</span><span class="sxs-lookup"><span data-stu-id="d8da4-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="d8da4-127">Decidere quali immagini di MED-V verranno archiviate nei repository e quali client MED-V caricherà aree di lavoro MED-V con immagini del repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="d8da4-128">Progettare e posizionare i repository di immagini</span><span class="sxs-lookup"><span data-stu-id="d8da4-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="d8da4-129">Quando una nuova immagine è disponibile per i client, i client iniziano a scaricare l'immagine, possibilmente contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="d8da4-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="d8da4-130">In questo modo, viene creata una richiesta elevata nel repository e deve essere presa in considerazione durante la progettazione del repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="d8da4-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="d8da4-131">Per ogni repository, determinare la quantità di dati che verranno archiviati.</span><span class="sxs-lookup"><span data-stu-id="d8da4-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="d8da4-132">Sommare le dimensioni delle immagini che verranno archiviate nel repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="d8da4-133">Questo è il valore dello spazio su disco necessario nel file server.</span><span class="sxs-lookup"><span data-stu-id="d8da4-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="d8da4-134">Aggiungere quindi il numero di client che possono scaricare le immagini MED-V dal repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="d8da4-135">Questo è il numero massimo di download simultanei che possono verificarsi quando viene caricata una nuova immagine MED-V nel repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="d8da4-136">Il file server deve essere progettato con un sottosistema di dischi in grado di soddisfare le richieste di i/o che verranno create.</span><span class="sxs-lookup"><span data-stu-id="d8da4-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="d8da4-137">Il repository di immagini può risiedere nello stesso sistema del server MED-V e del server che ha eseguito SQL Server oppure in una condivisione file remota.</span><span class="sxs-lookup"><span data-stu-id="d8da4-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="d8da4-138">Puoi anche eseguirlo in una VM di Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d8da4-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="d8da4-139">Controllare il percorso di rete dei client che il repository di immagini sarà in grado di gestire e posizionare il repository in un percorso di rete in cui disponga di larghezza di banda sufficiente per soddisfare le aspettative dei livelli di servizio di tali client.</span><span class="sxs-lookup"><span data-stu-id="d8da4-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="d8da4-140">Tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="d8da4-140">Fault Tolerance</span></span>

<span data-ttu-id="d8da4-141">Se il repository di immagini non è disponibile, i client non saranno in grado di scaricare immagini MED-V nuove o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="d8da4-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="d8da4-142">Per progettare le opzioni di tolleranza d'errore per il file server e i dischi a tolleranza d'errore, vedere la guida alla [pianificazione e alla progettazione dell'infrastruttura Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="d8da4-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="d8da4-143">Progettare e posizionare i server IIS</span><span class="sxs-lookup"><span data-stu-id="d8da4-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="d8da4-144">Questa sezione è pertinente solo se i client scaricheranno i file di immagine tramite la rete tramite HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d8da4-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="d8da4-145">Il server IIS può coesistere nello stesso sistema del server MED-V e del server che ha eseguito SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8da4-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="d8da4-146">Può anche essere eseguito in una VM di Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d8da4-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="d8da4-147">L'infrastruttura del server IIS deve avere un throughput sufficiente per consegnare le immagini ai client all'interno delle aspettative del livello di servizio dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d8da4-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="d8da4-148">Deve essere progettata con un sottosistema di dischi in grado di soddisfare le richieste IO.</span><span class="sxs-lookup"><span data-stu-id="d8da4-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="d8da4-149">Per ogni repository di immagini, sommare il numero di client che possono scaricare immagini MED-V tramite IIS.</span><span class="sxs-lookup"><span data-stu-id="d8da4-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="d8da4-150">Questo è il numero massimo di download simultanei che possono verificarsi quando un'immagine viene caricata nel repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="d8da4-151">Usare la somma effettiva e le aspettative del livello di servizio determinate in [definire l'ambito del progetto](define-the-project-scope.md) per pianificare la progettazione dell'infrastruttura del server IIS e determinare la quantità di larghezza di banda appropriata da allocare per il repository.</span><span class="sxs-lookup"><span data-stu-id="d8da4-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="d8da4-152">Per progettare l'infrastruttura IIS, vedere la guida alla [pianificazione e progettazione dell'infrastruttura Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="d8da4-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="d8da4-153">Tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="d8da4-153">Fault Tolerance</span></span>

<span data-ttu-id="d8da4-154">Se l'infrastruttura del server IIS non è disponibile, i client non saranno in grado di scaricare immagini nuove o aggiornate.</span><span class="sxs-lookup"><span data-stu-id="d8da4-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="d8da4-155">Per configurare la tolleranza di errore, il server IIS basato su Windows Server2008 può essere inserito in un cluster di failover.</span><span class="sxs-lookup"><span data-stu-id="d8da4-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="d8da4-156">Per progettare la tolleranza d'errore per l'infrastruttura del server IIS, vedere la guida alla [pianificazione e alla progettazione dell'infrastruttura Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="d8da4-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="d8da4-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8da4-157">Related topics</span></span>


[<span data-ttu-id="d8da4-158">Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale</span><span class="sxs-lookup"><span data-stu-id="d8da4-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="d8da4-159">Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="d8da4-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





