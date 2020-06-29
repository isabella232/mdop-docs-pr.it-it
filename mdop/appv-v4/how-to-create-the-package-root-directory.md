---
title: Come creare la directory radice del pacchetto
description: Come creare la directory radice del pacchetto
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817626"
---
# <span data-ttu-id="b173d-103">Come creare la directory radice del pacchetto</span><span class="sxs-lookup"><span data-stu-id="b173d-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="b173d-104">La directory radice del pacchetto è la directory nel computer che esegue App-V Sequencer in cui sono installati i file per l'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="b173d-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="b173d-105">Questa directory esiste anche virtualmente nel computer in cui verrà trasmessa un'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="b173d-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="b173d-106">Devi creare la directory radice del pacchetto prima di monitorare l'installazione di una nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="b173d-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="b173d-107">Dopo aver creato la directory radice del pacchetto, è possibile iniziare a sequenziare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b173d-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="b173d-108">Per altre informazioni sulla sequenziazione di una nuova applicazione, vedere [come installare Sequencer](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="b173d-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="b173d-109">Per creare la directory radice del pacchetto</span><span class="sxs-lookup"><span data-stu-id="b173d-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="b173d-110">Per creare la directory radice del pacchetto, nel computer in cui è in uso l'App-V Sequencer eseguire il mapping dell'unità Q:\\ al percorso di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="b173d-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="b173d-111">La posizione specificata dovrebbe avere spazio sufficiente per salvare l'applicazione che si sta sequenziando.</span><span class="sxs-lookup"><span data-stu-id="b173d-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="b173d-112">Per creare una directory che è possibile usare per una nuova applicazione virtuale, creare una cartella nell'unità Q:\\ e assegnarle un nome.</span><span class="sxs-lookup"><span data-stu-id="b173d-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="b173d-113">**Importante**  Il nome assegnato ai file delle applicazioni virtuali che verranno salvati nella directory radice del pacchetto deve usare il formato di denominazione di 8,3.</span><span class="sxs-lookup"><span data-stu-id="b173d-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="b173d-114">I nomi di file non devono avere più di 8 caratteri con un'estensione di file di tre caratteri.</span><span class="sxs-lookup"><span data-stu-id="b173d-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="b173d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b173d-115">Related topics</span></span>


[<span data-ttu-id="b173d-116">Attività per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="b173d-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





