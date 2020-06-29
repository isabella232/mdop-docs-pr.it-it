---
title: Come configurare il file server
description: Come configurare il file server
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817785"
---
# <span data-ttu-id="60aec-103">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="60aec-103">How to Configure the File Server</span></span>


<span data-ttu-id="60aec-104">È possibile usare la procedura seguente per configurare un computer locale usato come condivisione di file e le applicazioni di flussi per il client Desktop Application Virtualization e il client per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="60aec-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="60aec-105">Questo scenario viene usato quando non si vuole aggiungere un'ulteriore infrastruttura server all'ambiente hardware esistente.</span><span class="sxs-lookup"><span data-stu-id="60aec-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="60aec-106">Se si usa un Application Virtualization Management Server come punto di distribuzione per la condivisione file installata negli uffici locali, è necessario configurare questo server prima che le applicazioni virtuali possano essere trasmesse ai computer usati come condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="60aec-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="60aec-107">Quando si configurano i server e le condivisioni file, si configura la directory di contenuto in cui vengono caricati e archiviati i file SFT.</span><span class="sxs-lookup"><span data-stu-id="60aec-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="60aec-108">I file SFT contengono l'applicazione virtuale (o le applicazioni).</span><span class="sxs-lookup"><span data-stu-id="60aec-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="60aec-109">**Importante**  Affinché le applicazioni vengano trasmesse correttamente al client Desktop Application Virtualization e al client per Servizi Desktop remoto, i flussi di file SFT dalla directory di contenuto nel server in cui è archiviata l'applicazione virtuale; il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un server diverso.</span><span class="sxs-lookup"><span data-stu-id="60aec-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="60aec-110">Per configurare l'Application Virtualization file server</span><span class="sxs-lookup"><span data-stu-id="60aec-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="60aec-111">Completare la procedura di installazione seguente per configurare il server usato come punto di distribuzione:</span><span class="sxs-lookup"><span data-stu-id="60aec-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="60aec-112">Come installare il server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="60aec-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="60aec-113">**Nota**  Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .</span><span class="sxs-lookup"><span data-stu-id="60aec-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="60aec-114">Creare una directory \\Content, che corrisponde alla directory specificata durante l'installazione del server, in ogni computer in uso come condivisione file.</span><span class="sxs-lookup"><span data-stu-id="60aec-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="60aec-115">**Importante**  Configurare i client Desktop Application Virtualization per eseguire il flusso delle applicazioni dal computer in uso come condivisione file anziché da un server di virtualizzazione dell'applicazione o da un server IIS.</span><span class="sxs-lookup"><span data-stu-id="60aec-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="60aec-116">Quando viene creata la directory \\Content, configurare la directory come condivisione file standard.</span><span class="sxs-lookup"><span data-stu-id="60aec-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="60aec-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60aec-117">Related topics</span></span>


[<span data-ttu-id="60aec-118">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="60aec-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="60aec-119">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="60aec-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="60aec-120">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="60aec-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="60aec-121">Come configurare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="60aec-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="60aec-122">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="60aec-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





