---
title: Componenti aggiuntivi del pacchetto applicazione virtuale
description: Componenti aggiuntivi del pacchetto applicazione virtuale
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815076"
---
# <span data-ttu-id="01926-103">Componenti aggiuntivi del pacchetto applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="01926-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="01926-104">App-V Sequencer ha rilevato una directory che contiene file eseguibili a 64 bit e a 32 bit e/o dll (Dynamic-Link Library) che dipendono dallo stesso assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="01926-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="01926-105">In genere, il Sequencer crea assembly side-by-side privati per tutti gli assembly pubblici usati dal pacchetto. Tuttavia, non è possibile creare versioni a 32 bit e a 64 bit degli assembly privati nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="01926-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="01926-106">Se il sequencer rileva un singolo conflitto, eseguirà le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="01926-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="01926-107">Rimuovere tutti gli assembly privati a 64 bit esistenti nell'intero pacchetto, indipendentemente dal fatto che la directory abbia un conflitto.</span><span class="sxs-lookup"><span data-stu-id="01926-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="01926-108">Creare solo versioni a 32 bit degli assembly side-by-side privati.</span><span class="sxs-lookup"><span data-stu-id="01926-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="01926-109">È consigliabile installare in modo nativo le versioni pubbliche di tutti gli assembly di 64 bit necessari nel computer che eseguono Sequencer e in tutti i computer client App-V.</span><span class="sxs-lookup"><span data-stu-id="01926-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="01926-110">Per individuare gli assembly pubblici esistenti necessari, aprire la directory in cui viene salvato il pacchetto e cercare nella cartella **VFS** .</span><span class="sxs-lookup"><span data-stu-id="01926-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="01926-111">Ad esempio, se la radice del pacchetto è **Q:\\MyApp**, quando si sequenzia l'applicazione, cercare in **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** e individuare tutti gli assembly pubblici esistenti.</span><span class="sxs-lookup"><span data-stu-id="01926-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="01926-112">Le versioni a 64 bit di questi file inizieranno sempre con il testo seguente all'inizio del nome del manifesto: **amd64...**.</span><span class="sxs-lookup"><span data-stu-id="01926-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="01926-113">Il nome e la versione esatta dell'assembly possono essere trovati nel file manifesto associato.</span><span class="sxs-lookup"><span data-stu-id="01926-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="01926-114">Usare uno dei collegamenti seguenti per scaricare e installare la versione corretta dei prerequisiti necessari:</span><span class="sxs-lookup"><span data-stu-id="01926-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="01926-115">Pacchetto ridistribuibile di Microsoft Visual C++ 2005 (x64)</span><span class="sxs-lookup"><span data-stu-id="01926-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="01926-116">Pacchetto ridistribuibile di Microsoft Visual C++ 2005 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="01926-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="01926-117">Pacchetto ridistribuibile di Microsoft Visual C++ 2008 (x64)</span><span class="sxs-lookup"><span data-stu-id="01926-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="01926-118">Pacchetto ridistribuibile di Microsoft Visual C++ 2008 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="01926-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





