---
title: Informazioni sull'utilizzo della riga di comando di Sequencer
description: Informazioni sull'utilizzo della riga di comando di Sequencer
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819905"
---
# <span data-ttu-id="b69cf-103">Informazioni sull'utilizzo della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="b69cf-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="b69cf-104">Puoi usare la riga di comando per creare pacchetti di applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="b69cf-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="b69cf-105">L'uso della riga di comando per creare applicazioni virtuali è utile negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="b69cf-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="b69cf-106">È necessario creare un numero elevato di pacchetti di applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="b69cf-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="b69cf-107">È necessario creare un pacchetto di applicazione sequenziale su base periodica.</span><span class="sxs-lookup"><span data-stu-id="b69cf-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="b69cf-108">**Importante**  La sequenziazione al prompt dei comandi consente solo la sequenziazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b69cf-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="b69cf-109">Se è necessario modificare i parametri di sequenziazione predefiniti, è necessario modificare manualmente un pacchetto di applicazione sequenziata o ripetere la sequenza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b69cf-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="b69cf-110">Tutte le modifiche successive apportate ai pacchetti di applicazioni sequenziate esistenti devono essere eseguite tramite la sequenziazione guidata.</span><span class="sxs-lookup"><span data-stu-id="b69cf-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="b69cf-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="b69cf-111">Prerequisites</span></span>


<span data-ttu-id="b69cf-112">Per sequenziare un'applicazione usando il prompt dei comandi, è necessario che siano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b69cf-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="b69cf-113">L'applicazione che sta per essere sequenziata non deve richiedere modifiche o soluzioni alternative apportate all'esterno del pacchetto di installazione o di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b69cf-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="b69cf-114">Prima della sequenziazione, è necessario preparare un elenco di file batch per la creazione dei pacchetti di applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="b69cf-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="b69cf-115">Per altre informazioni sui parametri della riga di comando, vedere [parametri della riga](command-line-parameters.md)di comando.</span><span class="sxs-lookup"><span data-stu-id="b69cf-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="b69cf-116">Esaminare gli errori che potrebbero essere visualizzati quando si crea un pacchetto di applicazione sequenziata tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b69cf-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="b69cf-117">Per altre informazioni, vedere questi errori, vedere [errori della riga di comando](command-line-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b69cf-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="b69cf-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b69cf-118">Related topics</span></span>


[<span data-ttu-id="b69cf-119">Come gestire le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="b69cf-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





