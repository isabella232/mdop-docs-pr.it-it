---
title: Scheda Elementi di esclusione
description: Scheda Elementi di esclusione
author: dansimp
ms.assetid: 864e46dd-3d6e-4a1b-acf4-9dc00548117e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f472fb61c121a1977c3c4ff927bd1ba6f680d86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821576"
---
# <span data-ttu-id="95128-103">Scheda Elementi di esclusione</span><span class="sxs-lookup"><span data-stu-id="95128-103">Exclusion Items Tab</span></span>


<span data-ttu-id="95128-104">Nella scheda **elementi di esclusione** vengono visualizzate le espressioni che l'Application Virtualization Sequencer esclude dal file system virtuale o dal registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="95128-104">The **Exclusion Items** tab displays the expressions that the Application Virtualization Sequencer excludes from the virtual file system or virtual registry.</span></span> <span data-ttu-id="95128-105">Queste espressioni sono escluse per garantire che il pacchetto di applicazione sequenziata possa essere eseguito nei client Desktop Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="95128-105">These expressions are excluded to ensure that the sequenced application package can run on Application Virtualization Desktop Clients.</span></span> <span data-ttu-id="95128-106">Puoi anche escludere le directory di installazione non standard che potrebbero essere indesiderate nella sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="95128-106">You can also exclude non-standard installation directories that might be unwanted in the sequencing.</span></span>

<span data-ttu-id="95128-107">Questa scheda contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="95128-107">This tab contains the following elements.</span></span>

<a href="" id="exclude-path"></a>**<span data-ttu-id="95128-108">Escludi percorso</span><span class="sxs-lookup"><span data-stu-id="95128-108">Exclude Path</span></span>**  
<span data-ttu-id="95128-109">Visualizza i nomi di variabile che il sequencer esclude se viene rilevato durante l'analisi di elementi di file system virtuali o elementi del registro di sistema virtuali.</span><span class="sxs-lookup"><span data-stu-id="95128-109">Displays variable names that the Sequencer excludes if encountered while parsing virtual file system items or virtual registry items.</span></span>

<a href="" id="resolves-to"></a>**<span data-ttu-id="95128-110">Risolve in</span><span class="sxs-lookup"><span data-stu-id="95128-110">Resolves To</span></span>**  
<span data-ttu-id="95128-111">Visualizza i percorsi effettivi che corrispondono alle variabili Sequencer.</span><span class="sxs-lookup"><span data-stu-id="95128-111">Displays the actual paths that correspond to the Sequencer variables.</span></span>

<a href="" id="map-type"></a>**<span data-ttu-id="95128-112">Tipo di mappa</span><span class="sxs-lookup"><span data-stu-id="95128-112">Map Type</span></span>**  
<span data-ttu-id="95128-113">Visualizza le regole di mapping che il sequencer si applica per analizzare gli elementi nel file system virtuale o nel registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="95128-113">Displays mapping rules that the Sequencer applies to parse items in the virtual file system or virtual registry.</span></span> <span data-ttu-id="95128-114">Si può verificare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="95128-114">One of the following values can occur:</span></span>

<a href="" id="new"></a>**<span data-ttu-id="95128-115">Nuovo</span><span class="sxs-lookup"><span data-stu-id="95128-115">New</span></span>**  
<span data-ttu-id="95128-116">Fare clic per immettere un nuovo elemento di esclusione.</span><span class="sxs-lookup"><span data-stu-id="95128-116">Click to enter a new exclusion item.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="95128-117">Modifica</span><span class="sxs-lookup"><span data-stu-id="95128-117">Edit</span></span>**  
<span data-ttu-id="95128-118">Fare clic per modificare un'esclusione selezionata.</span><span class="sxs-lookup"><span data-stu-id="95128-118">Click to edit a selected exclusion.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="95128-119">Delete</span><span class="sxs-lookup"><span data-stu-id="95128-119">Delete</span></span>**  
<span data-ttu-id="95128-120">Fare clic per rimuovere un'esclusione selezionata.</span><span class="sxs-lookup"><span data-stu-id="95128-120">Click to remove a selected exclusion.</span></span>

<a href="" id="save-as-default"></a>**<span data-ttu-id="95128-121">Salva come predefinito</span><span class="sxs-lookup"><span data-stu-id="95128-121">Save As Default</span></span>**  
<span data-ttu-id="95128-122">Fare clic per salvare gli elementi di esclusione correnti come predefiniti.</span><span class="sxs-lookup"><span data-stu-id="95128-122">Click to save the current exclusion items as your default.</span></span>

<a href="" id="restore-defaults"></a>**<span data-ttu-id="95128-123">Ripristinare le impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="95128-123">Restore Defaults</span></span>**  
<span data-ttu-id="95128-124">Fare clic per ripristinare gli elementi di esclusione assegnati per impostazione predefinita e rimuovere eventuali elementi aggiunti.</span><span class="sxs-lookup"><span data-stu-id="95128-124">Click to restore default-assigned exclusion items and remove any items you added.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="95128-125">OK</span><span class="sxs-lookup"><span data-stu-id="95128-125">OK</span></span>**  
<span data-ttu-id="95128-126">Fare clic per accettare le eccezioni visualizzate.</span><span class="sxs-lookup"><span data-stu-id="95128-126">Click to accept the displayed exceptions.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="95128-127">Annulla</span><span class="sxs-lookup"><span data-stu-id="95128-127">Cancel</span></span>**  
<span data-ttu-id="95128-128">Fare clic per annullare le modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="95128-128">Click to cancel any changes you have made.</span></span>

## <span data-ttu-id="95128-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95128-129">Related topics</span></span>


[<span data-ttu-id="95128-130">Finestra di dialogo Opzioni di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="95128-130">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

[<span data-ttu-id="95128-131">Finestra di dialogo Elementi di esclusione</span><span class="sxs-lookup"><span data-stu-id="95128-131">Exclusion Item Dialog Box</span></span>](exclusion-item-dialog-box.md)

 

 





