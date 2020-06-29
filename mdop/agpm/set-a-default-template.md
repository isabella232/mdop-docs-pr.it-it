---
title: Impostare un modello predefinito
description: Impostare un modello predefinito
author: dansimp
ms.assetid: e0acf980-437f-4357-b237-298aaebe490d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 870c1d4c13049992509f6aa831966736e6ba25ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820226"
---
# <span data-ttu-id="18d1d-103">Impostare un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="18d1d-103">Set a Default Template</span></span>


<span data-ttu-id="18d1d-104">In qualità di Editor puoi specificare quale dei modelli disponibili sarà il modello predefinito consigliato per tutti gli amministratori di criteri di gruppo per la creazione di nuovi oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="18d1d-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy objects (GPOs).</span></span>

<span data-ttu-id="18d1d-105">**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.</span><span class="sxs-lookup"><span data-stu-id="18d1d-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="18d1d-106">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="18d1d-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="18d1d-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="18d1d-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="18d1d-108">Per impostare il modello predefinito da usare per la creazione di nuovi GPO</span><span class="sxs-lookup"><span data-stu-id="18d1d-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="18d1d-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="18d1d-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="18d1d-110">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **modelli** per visualizzare i modelli disponibili.</span><span class="sxs-lookup"><span data-stu-id="18d1d-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="18d1d-111">Fare clic con il pulsante destro del mouse sul modello che si desidera impostare come predefinito e quindi scegliere **Imposta come predefinito**.</span><span class="sxs-lookup"><span data-stu-id="18d1d-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="18d1d-112">Fare clic su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="18d1d-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="18d1d-113">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="18d1d-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="18d1d-114">Il modello predefinito ha un'icona blu e lo stato è identificato come **modello (impostazione predefinita)** nella scheda **modelli** .</span><span class="sxs-lookup"><span data-stu-id="18d1d-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="18d1d-115">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="18d1d-115">Additional considerations</span></span>

-   <span data-ttu-id="18d1d-116">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="18d1d-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="18d1d-117">In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni di **modello** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="18d1d-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="18d1d-118">Dopo aver impostato un modello come predefinito, tale modello sarà quello selezionato inizialmente nella finestra di dialogo **nuovo GPO controllato** quando gli amministratori dei criteri di gruppo creano nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="18d1d-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="18d1d-119">Tuttavia, avranno la possibilità di selezionare un altro modello di GPO, incluso il \*\* &lt; GPO &gt; vuoto\*\*, che non include alcuna impostazione.</span><span class="sxs-lookup"><span data-stu-id="18d1d-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="18d1d-120">La ridenominazione o l'eliminazione di un modello non ha effetti sugli oggetti Criteri di creazione creati da tale modello.</span><span class="sxs-lookup"><span data-stu-id="18d1d-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="18d1d-121">Poiché non può essere modificato, un modello non ha una cronologia.</span><span class="sxs-lookup"><span data-stu-id="18d1d-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="18d1d-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="18d1d-122">Additional references</span></span>

-   [<span data-ttu-id="18d1d-123">Creazione di un modello e impostazione di un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="18d1d-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="18d1d-124">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="18d1d-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





