---
title: Pagina Seleziona Acceleratore pacchetto
description: Pagina Seleziona Acceleratore pacchetto
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815595"
---
# <span data-ttu-id="62b5f-103">Pagina Seleziona Acceleratore pacchetto</span><span class="sxs-lookup"><span data-stu-id="62b5f-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="62b5f-104">Usare la pagina **Seleziona accelerazione pacchetto** per selezionare l'Acceleratore pacchetto che verrà usato per creare il nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b5f-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="62b5f-105">È necessario copiare l'Acceleratore pacchetto in una cartella nel computer in cui è in uso l'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="62b5f-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="62b5f-106">Per altre informazioni, vedere [informazioni sugli acceleratori di pacchetti App-v (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="62b5f-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="62b5f-107">Eseguire solo gli acceleratori pacchetto dagli editori attendibili.</span><span class="sxs-lookup"><span data-stu-id="62b5f-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="62b5f-108">Gli acceleratori di pacchetto includono in genere una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="62b5f-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="62b5f-109">Una firma digitale è un marchio di sicurezza elettronico che consente di indicare l'autore del software e se il pacchetto è stato manomesso dopo la firma originale della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="62b5f-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="62b5f-110">Se si usa una trasformazione che è stata firmata digitalmente da un autore e che il Publisher ne ha verificato l'identità con un'autorità di certificazione, è possibile avere la certezza che la trasformazione venga eseguita da tale editore specifico e non sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="62b5f-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="62b5f-111">L'App-V Sequencer informa se una delle condizioni seguenti è vera:</span><span class="sxs-lookup"><span data-stu-id="62b5f-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="62b5f-112">La trasformazione selezionata non è stata firmata digitalmente.</span><span class="sxs-lookup"><span data-stu-id="62b5f-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="62b5f-113">La trasformazione selezionata è firmata da un autore che non ne ha verificato l'identità con un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="62b5f-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="62b5f-114">La trasformazione selezionata è stata modificata dopo che è stata firmata e rilasciata digitalmente.</span><span class="sxs-lookup"><span data-stu-id="62b5f-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="62b5f-115">Se uno di questi messaggi viene visualizzato quando si usa un Acceleratore pacchetto, visitare il sito Web dell'autore degli acceleratori del pacchetto per ottenere una versione con firma digitale della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="62b5f-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="62b5f-116">Questa pagina contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="62b5f-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="62b5f-117">Esplora</span><span class="sxs-lookup"><span data-stu-id="62b5f-117">Browse</span></span>**  
<span data-ttu-id="62b5f-118">Fare clic su **Sfoglia** per specificare l'acceleratore di pacchetto che verrà usato per creare il pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="62b5f-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="62b5f-119">Salvare l'acceleratore del pacchetto specificato localmente nel computer in cui è in corso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="62b5f-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="62b5f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62b5f-120">Related topics</span></span>


[<span data-ttu-id="62b5f-121">Procedura guidata di Sequencer - Acceleratore pacchetto (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="62b5f-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





