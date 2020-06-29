---
title: Come configurare Application Virtualization Streaming Server
description: Come configurare Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817825"
---
# <span data-ttu-id="742bd-103">Come configurare Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="742bd-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="742bd-104">Prima che le applicazioni virtuali possano essere trasmesse al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario configurare i server di streaming Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="742bd-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="742bd-105">Quando configuri i server, stai configurando la *directory di contenuto* in cui vengono caricati e archiviati i file SFT.</span><span class="sxs-lookup"><span data-stu-id="742bd-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="742bd-106">I file SFT contengono l'applicazione virtuale (o le applicazioni).</span><span class="sxs-lookup"><span data-stu-id="742bd-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="742bd-107">**Importante**  Application Virtualization Servers Stream SFT per il client desktop e il client per i Servizi Desktop remoto usando solo protocolli RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="742bd-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="742bd-108">Il file ICO (icona) e il file OSD (Open Software Descriptor) possono essere configurati in streaming da un file o un server HTTP diverso.</span><span class="sxs-lookup"><span data-stu-id="742bd-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="742bd-109">Per configurare i server di streaming Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="742bd-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="742bd-110">Completare la procedura di installazione per Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="742bd-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="742bd-111">Durante la procedura di installazione, specificare la posizione della directory \\Content nella schermata **percorso contenuto** .</span><span class="sxs-lookup"><span data-stu-id="742bd-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="742bd-112">Passare al percorso specificato per la directory \\Content e, se necessario, creare la directory.</span><span class="sxs-lookup"><span data-stu-id="742bd-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="742bd-113">Quando viene creata la directory di contenuto, configurare la directory come condivisione di file standard.</span><span class="sxs-lookup"><span data-stu-id="742bd-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="742bd-114">Configurare le autorizzazioni di file system NTFS per la directory di contenuto e le cartelle del pacchetto nella directory di contenuto.</span><span class="sxs-lookup"><span data-stu-id="742bd-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="742bd-115">È consigliabile usare i gruppi di sicurezza in servizi di dominio Active Directory che definiscono gli utenti che possono accedere a ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="742bd-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="742bd-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="742bd-116">Related topics</span></span>


[<span data-ttu-id="742bd-117">Scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="742bd-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="742bd-118">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="742bd-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="742bd-119">Come configurare i server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="742bd-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="742bd-120">Come configurare il file server</span><span class="sxs-lookup"><span data-stu-id="742bd-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="742bd-121">Come configurare il server per IIS</span><span class="sxs-lookup"><span data-stu-id="742bd-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





