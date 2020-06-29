---
title: Esaminare i collegamenti dell'oggetto Criteri di gruppo
description: Esaminare i collegamenti dell'oggetto Criteri di gruppo
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818346"
---
# <span data-ttu-id="6638d-103">Esaminare i collegamenti dell'oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6638d-103">Review GPO Links</span></span>


<span data-ttu-id="6638d-104">È possibile visualizzare un diagramma che mostra dove un oggetto Criteri di gruppo o GPO selezionato è collegato alle unità organizzative.</span><span class="sxs-lookup"><span data-stu-id="6638d-104">You can display a diagram showing where a Group Policy Object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="6638d-105">I diagrammi di collegamento GPO vengono aggiornati ogni volta che il GPO viene controllato, importato o archiviato.</span><span class="sxs-lookup"><span data-stu-id="6638d-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="6638d-106">Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="6638d-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="6638d-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="6638d-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="6638d-108">Revisione dei collegamenti degli oggetti Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="6638d-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="6638d-109">Per uno o più GPO</span><span class="sxs-lookup"><span data-stu-id="6638d-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="6638d-110">Per una o più versioni di un oggetto Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="6638d-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="6638d-111">Per visualizzare i collegamenti GPO per uno o più GPO</span><span class="sxs-lookup"><span data-stu-id="6638d-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="6638d-112">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="6638d-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6638d-113">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato**, **in sospeso**o **Cestino** per visualizzare i GPO.</span><span class="sxs-lookup"><span data-stu-id="6638d-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="6638d-114">Selezionare uno o più GPO per cui visualizzare i collegamenti, fare clic con il pulsante destro del mouse su un oggetto Criteri di selezione selezionato, scegliere **Impostazioni**e quindi fare clic su **collegamenti GPO** per visualizzare un diagramma di domini e unità organizzative con collegamenti ai GPO selezionati.</span><span class="sxs-lookup"><span data-stu-id="6638d-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="6638d-115">Per visualizzare i collegamenti GPO per una o più versioni di un oggetto Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="6638d-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="6638d-116">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="6638d-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="6638d-117">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **Controlla** o **Cestino** per visualizzare gli oggetti Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="6638d-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="6638d-118">Fare doppio clic sul GPO per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="6638d-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="6638d-119">Fare clic con il pulsante destro del mouse sulla versione del GPO per la quale rivedere le impostazioni, fare clic su **Impostazioni**e quindi su **report HTML** o **report XML** per visualizzare un riepilogo delle impostazioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="6638d-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="6638d-120">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="6638d-120">Additional considerations</span></span>

-   <span data-ttu-id="6638d-121">Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="6638d-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="6638d-122">In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO.</span><span class="sxs-lookup"><span data-stu-id="6638d-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="6638d-123">Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="6638d-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="6638d-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="6638d-124">Additional references</span></span>

-   [<span data-ttu-id="6638d-125">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="6638d-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





