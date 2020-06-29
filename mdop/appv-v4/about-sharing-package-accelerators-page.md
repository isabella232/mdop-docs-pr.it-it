---
title: Pagina Informazioni sulla condivisione degli Acceleratori pacchetto
description: Pagina Informazioni sulla condivisione degli Acceleratori pacchetto
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819995"
---
# <span data-ttu-id="5030e-103">Pagina Informazioni sulla condivisione degli Acceleratori pacchetto</span><span class="sxs-lookup"><span data-stu-id="5030e-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="5030e-104">Le informazioni seguenti forniscono informazioni sulle procedure consigliate per condividere gli acceleratori di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5030e-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="5030e-105">Se si prevede di condividere i file degli acceleratori di pacchetto, le informazioni come i nomi di computer, le informazioni sugli account utente e le informazioni sulle applicazioni incluse nelle trasformazioni potrebbero essere incluse nel file degli acceleratori di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5030e-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="5030e-106">È consigliabile esaminare le impostazioni o i file di configurazione associati al pacchetto di applicazione virtuale per assicurarsi che le applicazioni non contengano informazioni personali. Questa pagina contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5030e-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="5030e-107">**Username**.</span><span class="sxs-lookup"><span data-stu-id="5030e-107">**Username**.</span></span> <span data-ttu-id="5030e-108">Quando si accede al computer che utilizza Microsoft App-V Sequencer, è necessario usare un account utente generico, ad esempio l'account di **amministratore** predefinito.</span><span class="sxs-lookup"><span data-stu-id="5030e-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="5030e-109">Non usare un account basato su un nome utente esistente.</span><span class="sxs-lookup"><span data-stu-id="5030e-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="5030e-110">**Nome computer**.</span><span class="sxs-lookup"><span data-stu-id="5030e-110">**Computer Name**.</span></span> <span data-ttu-id="5030e-111">Specificare un nome generale non Identificativo del computer che usa il sequencer.</span><span class="sxs-lookup"><span data-stu-id="5030e-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="5030e-112">**URL del server**.</span><span class="sxs-lookup"><span data-stu-id="5030e-112">**Server URL**.</span></span> <span data-ttu-id="5030e-113">Nella scheda **distribuzione** della console App-V Sequencer usare le impostazioni predefinite per le informazioni di configurazione dell'URL del server.</span><span class="sxs-lookup"><span data-stu-id="5030e-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="5030e-114">**Applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="5030e-114">**Applications**.</span></span> <span data-ttu-id="5030e-115">Se non si vuole condividere l'elenco delle applicazioni installate nel computer che esegue il sequencer quando è stato creato l'acceleratore del pacchetto, è necessario eliminare il file **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="5030e-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="5030e-116">Questo file si trova nella directory radice del pacchetto del pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="5030e-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="5030e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5030e-117">Related topics</span></span>


[<span data-ttu-id="5030e-118">Procedura guidata Crea Acceleratore pacchetto (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5030e-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="5030e-119">Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5030e-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





