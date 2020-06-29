---
title: Informazioni su DaRT 8.1
description: Informazioni su DaRT 8.1
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821265"
---
# <span data-ttu-id="f430c-103">Informazioni su DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="f430c-103">About DaRT 8.1</span></span>


<span data-ttu-id="f430c-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,1 offre i miglioramenti seguenti, descritti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f430c-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="f430c-105">Novità</span><span class="sxs-lookup"><span data-stu-id="f430c-105">What’s new</span></span>


-   **<span data-ttu-id="f430c-106">Supporto per WIMBoot</span><span class="sxs-lookup"><span data-stu-id="f430c-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="f430c-107">Set di strumenti di diagnostica e ripristino 8,1 supporta l'ambiente Windows Image file Boot (WIMBoot) se queste condizioni sono soddisfatte:</span><span class="sxs-lookup"><span data-stu-id="f430c-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="f430c-108">WIMBoot è basato su Windows 8,1 Update 1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f430c-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="f430c-109">L'immagine di DaRT 8,1 è basata su Windows 8,1 Update 1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f430c-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="f430c-110">Per altre informazioni su WIMBoot, Vedi [Panoramica di Windows Image file Boot (WIMBoot)](https://go.microsoft.com/fwlink/?LinkId=517536).</span><span class="sxs-lookup"><span data-stu-id="f430c-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="f430c-111">Supporto per Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f430c-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="f430c-112">Puoi creare immagini DaRT usando Windows Server 2012 R2 o Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="f430c-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="f430c-113">Nota</span><span class="sxs-lookup"><span data-stu-id="f430c-113">Note</span></span>**  
    <span data-ttu-id="f430c-114">Per le versioni precedenti dei sistemi operativi Windows Server e Windows, continuare a usare le versioni precedenti di DaRT.</span><span class="sxs-lookup"><span data-stu-id="f430c-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="f430c-115">Feedback dei clienti</span><span class="sxs-lookup"><span data-stu-id="f430c-115">Customer feedback</span></span>**

    <span data-ttu-id="f430c-116">DaRT 8,1 include gli aggiornamenti relativi ai problemi di indirizzo trovati dopo il rilascio di DaRT 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="f430c-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="f430c-117">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="f430c-117">Windows Defender</span></span>**

    <span data-ttu-id="f430c-118">Windows Defender in Windows 8,1 include una protezione migliorata.</span><span class="sxs-lookup"><span data-stu-id="f430c-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="f430c-119">Le modifiche non influiscono sulla modalità di utilizzo di DaRT con Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="f430c-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="f430c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f430c-120">Requirements</span></span>


-   **<span data-ttu-id="f430c-121">Windows Assessment and Development Kit 8,1</span><span class="sxs-lookup"><span data-stu-id="f430c-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="f430c-122">Windows Assessment and Development Kit (ADK) 8,1 è un prerequisito necessario per la creazione guidata immagine di ripristino di DaRT.</span><span class="sxs-lookup"><span data-stu-id="f430c-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="f430c-123">Windows ADK 8,1 contiene gli strumenti di distribuzione usati per personalizzare, distribuire e servire immagini di Windows.</span><span class="sxs-lookup"><span data-stu-id="f430c-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="f430c-124">Contiene inoltre l'ambiente di preinstallazione di Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="f430c-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="f430c-125">Nota</span><span class="sxs-lookup"><span data-stu-id="f430c-125">Note</span></span>**  
    <span data-ttu-id="f430c-126">Windows ADK 8,1 non è necessario se si sta installando solo il Visualizzatore di connessioni remote o un analizzatore di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="f430c-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="f430c-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="f430c-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="f430c-128">DaRT 8,1 richiede che sia installato .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="f430c-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="f430c-129">Per il download, vedere [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) nell'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f430c-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="f430c-130">Strumenti di debug di Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f430c-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="f430c-131">Per usare lo strumento Analizzatore crash in DaRT 8,1, ti servono gli strumenti di debug necessari, disponibili nel Software Development Kit per Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="f430c-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="f430c-132">Per il download, vedere [Windows Software Development Kit (SDK) per windows 8,1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) nell'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f430c-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="f430c-133">Disponibilità lingua</span><span class="sxs-lookup"><span data-stu-id="f430c-133">Language availability</span></span>


<span data-ttu-id="f430c-134">Il dardo 8,1 è disponibile nelle lingue seguenti:</span><span class="sxs-lookup"><span data-stu-id="f430c-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="f430c-135">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="f430c-135">English (United States) en-US</span></span>

-   <span data-ttu-id="f430c-136">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="f430c-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="f430c-137">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="f430c-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="f430c-138">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="f430c-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="f430c-139">Spagnolo, ordinamento internazionale (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="f430c-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="f430c-140">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="f430c-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="f430c-141">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="f430c-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="f430c-142">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="f430c-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="f430c-143">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="f430c-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="f430c-144">Zh-TW tradizionale cinese</span><span class="sxs-lookup"><span data-stu-id="f430c-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="f430c-145">Zh-CN semplificato in cinese</span><span class="sxs-lookup"><span data-stu-id="f430c-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="f430c-146">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="f430c-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="f430c-147">DaRT 8,1 fa parte del Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="f430c-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="f430c-148">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="f430c-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="f430c-149">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="f430c-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="f430c-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f430c-150">Related topics</span></span>


[<span data-ttu-id="f430c-151">Note sulla versione per DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="f430c-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









