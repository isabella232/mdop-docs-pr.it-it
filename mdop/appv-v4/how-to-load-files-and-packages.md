---
title: Come caricare file e pacchetti
description: Come caricare file e pacchetti
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817236"
---
# <span data-ttu-id="ff2fd-103">Come caricare file e pacchetti</span><span class="sxs-lookup"><span data-stu-id="ff2fd-103">How to Load Files and Packages</span></span>


<span data-ttu-id="ff2fd-104">È possibile usare la procedura seguente per caricare file e pacchetti nei server di virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="ff2fd-105">**Nota**  Durante il processo di installazione è stata specificata la posizione della directory \\Content nella pagina **percorso contenuto** .</span><span class="sxs-lookup"><span data-stu-id="ff2fd-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="ff2fd-106">Questa directory deve essere creata e configurata come condivisione file standard prima di puntare alla relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="ff2fd-107">Per caricare file e pacchetti</span><span class="sxs-lookup"><span data-stu-id="ff2fd-107">To load files and packages</span></span>**

1.  <span data-ttu-id="ff2fd-108">Nel computer da cui si vuole eseguire il flusso delle applicazioni, passare al percorso specificato per la directory \\Content.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="ff2fd-109">Se necessario, creare la directory e configurarla come condivisione file standard.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="ff2fd-110">Trasferire i file SFT per le applicazioni e i pacchetti virtuali nella directory \\Content.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="ff2fd-111">Per organizzare i file SFT e per evitare confusione, inserire applicazioni e pacchetti in sottocartelle dedicate.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="ff2fd-112">Caricare le applicazioni e i pacchetti in base ai requisiti dello scenario e della configurazione, considerando le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff2fd-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="ff2fd-113">Se le applicazioni e i pacchetti sono archiviati in un server di gestione di Application Virtualization (App-V), caricarli tramite la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="ff2fd-114">Per altre informazioni, Vedi [come caricare o scaricare un'applicazione](how-to-load-or-unload-an-application.md) o [come caricare applicazioni virtuali dall'area di notifica desktop](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="ff2fd-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="ff2fd-115">Se le applicazioni sono archiviate in un'app-V Streaming Server, in un server Web o in un computer configurato come file server, le applicazioni possono essere caricate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="ff2fd-116">**Nota**  App-V Streaming Server esegue automaticamente il polling della directory \\Content per le applicazioni e i pacchetti e inserisce queste informazioni in RAM per le richieste di applicazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="ff2fd-117">I client App-V devono essere configurati in modo appropriato per recuperare le applicazioni e i pacchetti da server Web e file server.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="ff2fd-118">Per altre informazioni, vedere [come configurare il client per il recupero del pacchetto dell'applicazione](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="ff2fd-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="ff2fd-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff2fd-119">Related topics</span></span>


[<span data-ttu-id="ff2fd-120">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="ff2fd-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





