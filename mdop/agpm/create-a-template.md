---
title: Creare un modello
description: Creare un modello
author: dansimp
ms.assetid: 6992bd55-4a4f-401f-9815-c468bac598ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9ad57204170fc3f49b01b571d82b00e1faf62de0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821066"
---
# <span data-ttu-id="15738-103">Creare un modello</span><span class="sxs-lookup"><span data-stu-id="15738-103">Create a Template</span></span>


<span data-ttu-id="15738-104">La creazione di un modello consente di salvare tutte le impostazioni di una specifica versione di un oggetto Criteri di gruppo da usare come punto di partenza per la creazione di nuovi GPO.</span><span class="sxs-lookup"><span data-stu-id="15738-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="15738-105">**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.</span><span class="sxs-lookup"><span data-stu-id="15738-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="15738-106">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="15738-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="15738-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="15738-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="15738-108">Per creare un modello basato su un oggetto Criteri di lavoro esistente</span><span class="sxs-lookup"><span data-stu-id="15738-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="15738-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="15738-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="15738-110">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato** o **non** controllata per visualizzare i GPO disponibili.</span><span class="sxs-lookup"><span data-stu-id="15738-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="15738-111">Fare clic con il pulsante destro del mouse sul GPO da cui si vuole creare un modello, quindi scegliere **Salva come modello**.</span><span class="sxs-lookup"><span data-stu-id="15738-111">Right-click the GPO from which you want to create a template, then click **Save as Template**.</span></span>

4.  <span data-ttu-id="15738-112">Digitare un nome per il modello e un commento, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="15738-112">Type a name for the template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="15738-113">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="15738-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="15738-114">Il nuovo modello viene visualizzato nella scheda **modelli** .</span><span class="sxs-lookup"><span data-stu-id="15738-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="15738-115">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="15738-115">Additional considerations</span></span>

-   <span data-ttu-id="15738-116">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="15738-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="15738-117">In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni di **modello** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="15738-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="15738-118">La ridenominazione o l'eliminazione di un modello non ha effetti sugli oggetti Criteri di creazione creati da tale modello.</span><span class="sxs-lookup"><span data-stu-id="15738-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="15738-119">Poiché non può essere modificato, un modello non ha una cronologia.</span><span class="sxs-lookup"><span data-stu-id="15738-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="15738-120">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="15738-120">Additional references</span></span>

-   [<span data-ttu-id="15738-121">Creazione di un modello e impostazione di un modello predefinito</span><span class="sxs-lookup"><span data-stu-id="15738-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="15738-122">Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato</span><span class="sxs-lookup"><span data-stu-id="15738-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





