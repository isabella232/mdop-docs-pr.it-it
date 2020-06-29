---
title: Nodo Associazioni del tipo di file
description: Nodo Associazioni del tipo di file
author: dansimp
ms.assetid: 48e4d9eb-00bd-4231-a68a-f8597ab683ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d94621a1d418f0af29ef9e73b8d430c81a7181c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821535"
---
# <span data-ttu-id="50cab-103">Nodo Associazioni del tipo di file</span><span class="sxs-lookup"><span data-stu-id="50cab-103">File Type Associations Node</span></span>


<span data-ttu-id="50cab-104">Il nodo **associazioni tipo di file** è un livello sotto il nodo **Application Virtualization** nel riquadro **ambito** della console di gestione client di Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="50cab-104">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="50cab-105">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="50cab-105">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

<span data-ttu-id="50cab-106">Fare clic con il pulsante destro del mouse sul nodo **Associazioni tipi di file** per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="50cab-106">Right-click the **File Type Associations** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-association"></a>**<span data-ttu-id="50cab-107">Nuova associazione</span><span class="sxs-lookup"><span data-stu-id="50cab-107">New Association</span></span>**  
<span data-ttu-id="50cab-108">Questa voce di menu Visualizza la procedura guidata nuova associazione.</span><span class="sxs-lookup"><span data-stu-id="50cab-108">This menu item displays the New Association Wizard.</span></span> <span data-ttu-id="50cab-109">Questa procedura guidata è costituita da due pagine:</span><span class="sxs-lookup"><span data-stu-id="50cab-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="50cab-110">Immettere un'estensione del nome file nuova o esistente e associare l'estensione a un tipo di file:</span><span class="sxs-lookup"><span data-stu-id="50cab-110">Enter a new or existing file name extension, and associate the extension with a file type:</span></span>

    -   <span data-ttu-id="50cab-111">**Estensione**: immettere un'estensione del nome file nuova o esistente.</span><span class="sxs-lookup"><span data-stu-id="50cab-111">**Extension**—Enter a new or existing file name extension.</span></span> <span data-ttu-id="50cab-112">Questo campo è vuoto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="50cab-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="50cab-113">**Creare un nuovo tipo di file con questa descrizione**: selezionare questo pulsante di opzione per immettere una nuova descrizione del tipo di file nel campo attivo.</span><span class="sxs-lookup"><span data-stu-id="50cab-113">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="50cab-114">Questo pulsante è selezionato per impostazione predefinita e il campo attivo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="50cab-114">This button is selected by default, and the active field is blank.</span></span>

    -   <span data-ttu-id="50cab-115">**Applica questo tipo di file a tutti gli utenti**: selezionare questa casella di controllo quando si vuole che l'associazione sia globale per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="50cab-115">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="50cab-116">Per impostazione predefinita, questa casella non è selezionata.</span><span class="sxs-lookup"><span data-stu-id="50cab-116">By default, this box is not selected.</span></span>

    -   <span data-ttu-id="50cab-117">**Collegare questa estensione a un tipo di file esistente**: selezionare questo pulsante di opzione per associare l'estensione a un tipo di file esistente.</span><span class="sxs-lookup"><span data-stu-id="50cab-117">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="50cab-118">Scegliere un tipo di file nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="50cab-118">Choose a file type from the drop-down list.</span></span> <span data-ttu-id="50cab-119">Quando si sceglie questa opzione, il **successivo** viene modificato in **fine**.</span><span class="sxs-lookup"><span data-stu-id="50cab-119">When you choose this option, **Next** is changed to **Finish**.</span></span>

2.  <span data-ttu-id="50cab-120">Selezionare l'applicazione che consente di aprire i file con l'estensione specificata:</span><span class="sxs-lookup"><span data-stu-id="50cab-120">Select the application that will open files with the specified extension:</span></span>

    -   <span data-ttu-id="50cab-121">**Aprire i file con l'applicazione selezionata**: selezionare questo pulsante di opzione per aprire il file con un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="50cab-121">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="50cab-122">Scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="50cab-122">Choose an application from the drop-down list of available applications.</span></span>

    -   <span data-ttu-id="50cab-123">**Aprire file con l'applicazione descritta in questo file OSD**: selezionare questo pulsante di opzione per specificare un file OSD (Open Software Descriptor) che determina l'applicazione usata per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="50cab-123">**Open files with the application described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="50cab-124">Passare a selezionare una posizione esistente oppure immettere un percorso o un URL in formato HTTP in questo campo.</span><span class="sxs-lookup"><span data-stu-id="50cab-124">Browse to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="50cab-125">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="50cab-125">New Window from Here</span></span>**  
<span data-ttu-id="50cab-126">Selezionare questa voce di menu per aprire una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="50cab-126">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="50cab-127">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="50cab-127">Export List</span></span>**  
<span data-ttu-id="50cab-128">Puoi usare questa voce di menu per creare un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="50cab-128">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="50cab-129">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="50cab-129">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="50cab-130">Visualizza</span><span class="sxs-lookup"><span data-stu-id="50cab-130">View</span></span>**  
<span data-ttu-id="50cab-131">Questo elenco popup di voci di menu consente di modificare l'aspetto e il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="50cab-131">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="50cab-132">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="50cab-132">Refresh</span></span>**  
<span data-ttu-id="50cab-133">Selezionare questa voce per aggiornare la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="50cab-133">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="50cab-134">Help</span><span class="sxs-lookup"><span data-stu-id="50cab-134">Help</span></span>**  
<span data-ttu-id="50cab-135">Con questa voce di menu è possibile visualizzare il sistema della Guida per la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="50cab-135">With this menu item, you can display the help system for the management console.</span></span>

## <span data-ttu-id="50cab-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50cab-136">Related topics</span></span>


[<span data-ttu-id="50cab-137">Riquadro Risultati del nodo Associazioni del tipo di file</span><span class="sxs-lookup"><span data-stu-id="50cab-137">File Type Association Results Pane</span></span>](file-type-association-results-pane.md)

[<span data-ttu-id="50cab-138">Colonne del riquadro Risultati del nodo Associazioni del tipo di file</span><span class="sxs-lookup"><span data-stu-id="50cab-138">File Type Association Results Pane Columns</span></span>](file-type-association-results-pane-columns.md)

 

 





