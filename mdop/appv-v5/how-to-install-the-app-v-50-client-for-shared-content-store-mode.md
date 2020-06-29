---
title: Come installare il client App-V 5.0 per la modalità SCS (Shared Content Store)
description: Come installare il client App-V 5.0 per la modalità SCS (Shared Content Store)
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805440"
---
# <span data-ttu-id="1396c-103">Come installare il client App-V 5.0 per la modalità SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="1396c-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="1396c-104">Usare la procedura seguente per installare il client di Microsoft Application Virtualization (App-V) 5,0 in modo che usi la modalità SCS (Shared Content Store) App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1396c-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="1396c-105">Devi verificare che tutti i prerequisiti necessari siano installati nel computer in cui intendi installare.</span><span class="sxs-lookup"><span data-stu-id="1396c-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="1396c-106">Usare il collegamento seguente per i [prerequisiti di App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1396c-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="1396c-107">**Nota**  Prima di eseguire questa procedura, se necessario, disinstallare le versioni esistenti del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1396c-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="1396c-108">Per altre informazioni sulla modalità SCS, vedere [archivio contenuto condiviso in Microsoft App-V 5,0-dietro le quinte](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="1396c-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="1396c-109">Installare e configurare il client App-V 5,0 per la modalità SCS</span><span class="sxs-lookup"><span data-stu-id="1396c-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="1396c-110">Copiare i file di installazione del client App-V 5,0 nel computer in cui verrà installato.</span><span class="sxs-lookup"><span data-stu-id="1396c-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="1396c-111">Aprire una riga di comando e dalla directory in cui vengono salvati i file di installazione digitare una delle opzioni seguenti, a seconda della versione del client che si sta installando:</span><span class="sxs-lookup"><span data-stu-id="1396c-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="1396c-112">Per installare la versione RDS del tipo di client App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="1396c-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="1396c-113">Per installare la versione standard del tipo di client App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="1396c-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="1396c-114">**Importante**  È necessario eseguire un'installazione invisibile all'utente o l'installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1396c-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="1396c-115">Dopo aver completato l'installazione, è possibile distribuire pacchetti al computer che ha eseguito il client e tutti i contenuti del pacchetto verranno trasmessi in streaming nella rete.</span><span class="sxs-lookup"><span data-stu-id="1396c-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="1396c-116">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="1396c-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="1396c-117">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="1396c-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="1396c-118">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="1396c-118">Got an App-V issue?</span></span>** <span data-ttu-id="1396c-119">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="1396c-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="1396c-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1396c-120">Related topics</span></span>


[<span data-ttu-id="1396c-121">Distribuzione di App-V 5.0 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="1396c-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





