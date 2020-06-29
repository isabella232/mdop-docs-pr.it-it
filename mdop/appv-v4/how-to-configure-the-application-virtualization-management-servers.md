---
title: Come configurare i server di gestione di Application Virtualization
description: Come configurare i server di gestione di Application Virtualization
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817845"
---
# <span data-ttu-id="0136c-103">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0136c-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="0136c-104">Prima di poter eseguire il flusso delle applicazioni virtualizzate nel client Desktop Application Virtualization o nel client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare l'Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="0136c-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="0136c-105">Quando si configura il server, si sta configurando la *directory di contenuto* in cui vengono caricati e archiviati i file SFT.</span><span class="sxs-lookup"><span data-stu-id="0136c-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="0136c-106">I file SFT contengono l'applicazione o le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="0136c-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="0136c-107">**Importante**  Application Virtualization Servers Stream SFT per il client desktop e il client per i Servizi Desktop remoto usando solo protocolli RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="0136c-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="0136c-108">Il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un file o un server HTTP diverso.</span><span class="sxs-lookup"><span data-stu-id="0136c-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="0136c-109">Per configurare l'Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="0136c-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="0136c-110">Completare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="0136c-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="0136c-111">Come installare il server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0136c-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="0136c-112">**Nota**  Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .</span><span class="sxs-lookup"><span data-stu-id="0136c-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="0136c-113">Passare al percorso specificato per la directory \\Content e, se necessario, creare la directory.</span><span class="sxs-lookup"><span data-stu-id="0136c-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="0136c-114">Quando viene creata la directory di contenuto, configurare la directory come condivisione di file standard.</span><span class="sxs-lookup"><span data-stu-id="0136c-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="0136c-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0136c-115">Related topics</span></span>


[<span data-ttu-id="0136c-116">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="0136c-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="0136c-117">Requisiti di sistema di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0136c-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="0136c-118">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="0136c-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="0136c-119">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="0136c-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





