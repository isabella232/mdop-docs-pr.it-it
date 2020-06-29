---
title: Come modificare un File OSD
description: Come modificare un File OSD
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817436"
---
# <span data-ttu-id="72186-103">Come modificare un File OSD</span><span class="sxs-lookup"><span data-stu-id="72186-103">How to Edit an OSD File</span></span>


<span data-ttu-id="72186-104">Usa le procedure seguenti per modificare un file OSD (Open Software Descriptor) di un pacchetto di applicazione sequenziale aggiungendo o eliminando un elemento o un attributo.</span><span class="sxs-lookup"><span data-stu-id="72186-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="72186-105">**Nota**  Alcuni elementi non hanno un attributo, quindi non è possibile aggiungere un attributo a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="72186-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="72186-106">**Importante**  Se si usa l'Editor OSD per modificare il nome del file SFT, l'attributo HREF dell'elemento CODEBASE nel file OSD, è necessario usare il comando **Salva come** per salvare la modifica nei file di progetto.</span><span class="sxs-lookup"><span data-stu-id="72186-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="72186-107">Per aggiungere un elemento</span><span class="sxs-lookup"><span data-stu-id="72186-107">To add an element</span></span>**

1.  <span data-ttu-id="72186-108">Fare clic sulla scheda **file OSD** .</span><span class="sxs-lookup"><span data-stu-id="72186-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="72186-109">Nel riquadro di spostamento selezionare il file OSD del pacchetto di applicazione sequenziato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="72186-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="72186-110">Nel riquadro di spostamento fare clic con il pulsante destro del mouse sull'elemento che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="72186-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="72186-111">Nel menu selezionare **elemento** e quindi **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="72186-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="72186-112">Nel menu selezionare l'elemento che si vuole aggiungere, ad esempio **codebase**.</span><span class="sxs-lookup"><span data-stu-id="72186-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="72186-113">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="72186-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="72186-114">Per eliminare un elemento</span><span class="sxs-lookup"><span data-stu-id="72186-114">To delete an element</span></span>**

1.  <span data-ttu-id="72186-115">Fare clic sulla scheda **file OSD** .</span><span class="sxs-lookup"><span data-stu-id="72186-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="72186-116">Nel riquadro di spostamento selezionare il file OSD del pacchetto di applicazione sequenziato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="72186-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="72186-117">Nel riquadro di spostamento fare clic con il pulsante destro del mouse sull'elemento che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="72186-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="72186-118">Nel menu selezionare **elemento** e selezionare **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="72186-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="72186-119">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="72186-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="72186-120">Per aggiungere un attributo</span><span class="sxs-lookup"><span data-stu-id="72186-120">To add an attribute</span></span>**

1.  <span data-ttu-id="72186-121">Fare clic sulla scheda **file OSD** .</span><span class="sxs-lookup"><span data-stu-id="72186-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="72186-122">Nel riquadro di spostamento selezionare il file OSD del pacchetto di applicazione sequenziato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="72186-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="72186-123">Nel riquadro sinistro fare clic con il pulsante destro del mouse sull'elemento a cui si vuole aggiungere un attributo.</span><span class="sxs-lookup"><span data-stu-id="72186-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="72186-124">Nel menu selezionare **attributo** e selezionare **Aggiungi**, scegliendo tra gli attributi disponibili elencati.</span><span class="sxs-lookup"><span data-stu-id="72186-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="72186-125">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="72186-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="72186-126">Per eliminare un attributo</span><span class="sxs-lookup"><span data-stu-id="72186-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="72186-127">Fare clic sulla scheda **file OSD** .</span><span class="sxs-lookup"><span data-stu-id="72186-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="72186-128">Nel riquadro di spostamento selezionare il file OSD del pacchetto di applicazione sequenziato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="72186-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="72186-129">Nel riquadro di spostamento fare clic con il pulsante destro del mouse sull'elemento da cui si vuole eliminare un attributo.</span><span class="sxs-lookup"><span data-stu-id="72186-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="72186-130">Nel menu selezionare **attributo** e quindi selezionare **Elimina**, scegliendo l'attributo che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="72186-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="72186-131">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="72186-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="72186-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72186-132">Related topics</span></span>


[<span data-ttu-id="72186-133">Informazioni sulla scheda OSD</span><span class="sxs-lookup"><span data-stu-id="72186-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="72186-134">Come modificare un file OSD usando un editor di testo</span><span class="sxs-lookup"><span data-stu-id="72186-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="72186-135">Elementi di file OSD</span><span class="sxs-lookup"><span data-stu-id="72186-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="72186-136">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="72186-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





