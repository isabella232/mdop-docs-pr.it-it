---
title: Novità in App-V 5.0 SP1
description: Novità in App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804810"
---
# <span data-ttu-id="3fcb0-103">Novità in App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="3fcb0-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="3fcb0-104">Questa sezione è dedicata agli utenti che hanno già familiarità con App-V e vogliono sapere cosa è cambiato in App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="3fcb0-105">Se non si ha familiarità con l'App-V, è consigliabile iniziare leggendo [la pianificazione per l'app-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="3fcb0-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="3fcb0-106">Modifiche della funzionalità standard</span><span class="sxs-lookup"><span data-stu-id="3fcb0-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="3fcb0-107">Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per l'App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="3fcb0-108">Modifiche alle lingue supportate</span><span class="sxs-lookup"><span data-stu-id="3fcb0-108">Changes to Supported Languages</span></span>

<span data-ttu-id="3fcb0-109">Per altre informazioni, vedere [informazioni su App-V 5,0 SP1](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="3fcb0-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="3fcb0-110">L'elenco seguente contiene altre informazioni sui nuovi Language Pack:</span><span class="sxs-lookup"><span data-stu-id="3fcb0-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="3fcb0-111">I Language Pack di App-V 5.0 SP1 vengono raggruppati nel programma di installazione di **appv\_xxx\_setup.exe** per tutti i componenti di App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="3fcb0-112">Quando si esegue il programma di installazione, verrà installato automaticamente il Language Pack più appropriato in base alle impostazioni locali del sistema operativo associato in esecuzione nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="3fcb0-113">Se sono necessari altri Language Pack, è necessario estrarre questi Language Pack dal programma di installazione eseguendo il comando seguente: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` .</span><span class="sxs-lookup"><span data-stu-id="3fcb0-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="3fcb0-114">Dopo l'esecuzione, il contenuto del programma di installazione viene estratto nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="3fcb0-115">È necessario installare il Language Pack desiderato applicando il file di installazione di Windows del Language Pack appropriato.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="3fcb0-116">Ad esempio, **appv\_hib\_LP\_jmmb\_x86.msi** o **appv\_hib\_LP\_jmmb\_x64.msi**, in cui **Hib** si riferisce al componente e **jmmb** fa riferimento alle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="3fcb0-117">Supporto avanzato per Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="3fcb0-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="3fcb0-118">**Microsoft Office 2010, kit di sequenziazione per Application Virtualization 5,0** , consente agli utenti un'esperienza coerente con una versione virtualizzata di Microsoft office2010.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="3fcb0-119">Il **Kit di sequenziazione di Microsoft office 2010 per Application Virtualization 5,0** viene usato in combinazione con **Microsoft Office 2010 Deployment Kit per App-V** e offre anche il servizio di gestione delle licenze Microsoft Office2010 richiesto.</span><span class="sxs-lookup"><span data-stu-id="3fcb0-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="3fcb0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fcb0-120">Related topics</span></span>


[<span data-ttu-id="3fcb0-121">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3fcb0-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





