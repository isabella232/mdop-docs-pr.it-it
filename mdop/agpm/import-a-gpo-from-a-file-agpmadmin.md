---
title: Importare un oggetto Criteri di gruppo da un file
description: Importare un oggetto Criteri di gruppo da un file
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820755"
---
# <span data-ttu-id="944b2-103">Importare un oggetto Criteri di gruppo da un file</span><span class="sxs-lookup"><span data-stu-id="944b2-103">Import a GPO from a File</span></span>


<span data-ttu-id="944b2-104">In Advanced Group Policy Management, se si è un amministratore della gestione avanzata Criteri di gruppo (controllo completo) ed è stato esportato un oggetto Criteri di gruppo in un file CAB, è possibile importare le impostazioni dei criteri da tale GPO in un nuovo GPO o in un GPO esistente in un dominio in un'altra foresta.</span><span class="sxs-lookup"><span data-stu-id="944b2-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="944b2-105">Per informazioni sull'esportazione di impostazioni GPO in un file CAB, vedere [esportare un oggetto Criteri di ricerca in un file](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="944b2-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="944b2-106">È necessario un account utente con il ruolo di amministratore Advanced Group Policy Management o le autorizzazioni necessarie in Advanced Group Policy per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato.</span><span class="sxs-lookup"><span data-stu-id="944b2-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="944b2-107">È necessario un account utente con l'editor o il ruolo di amministratore Advanced Group Policy Management o le autorizzazioni necessarie in Advanced Group Policy per importare le impostazioni dei criteri in un GPO esistente.</span><span class="sxs-lookup"><span data-stu-id="944b2-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="944b2-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="944b2-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="944b2-109">Importazione di impostazioni dei criteri da un file</span><span class="sxs-lookup"><span data-stu-id="944b2-109">Importing policy settings from a file</span></span>


<span data-ttu-id="944b2-110">Quando si importano le impostazioni dei criteri da un file, è possibile importarle in un nuovo GPO o in un GPO esistente.</span><span class="sxs-lookup"><span data-stu-id="944b2-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="944b2-111">Tuttavia, se si importano le impostazioni dei criteri in un oggetto Criteri di stato esistente, tutte le impostazioni dei criteri all'interno vengono sostituite.</span><span class="sxs-lookup"><span data-stu-id="944b2-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="944b2-112">Importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="944b2-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="944b2-113">Importare le impostazioni dei criteri in un GPO esistente</span><span class="sxs-lookup"><span data-stu-id="944b2-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="944b2-114">Per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato</span><span class="sxs-lookup"><span data-stu-id="944b2-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="944b2-115">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="944b2-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="944b2-116">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="944b2-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="944b2-117">Creare un nuovo oggetto Criteri di controllo controllato.</span><span class="sxs-lookup"><span data-stu-id="944b2-117">Create a new controlled GPO.</span></span> <span data-ttu-id="944b2-118">Nella finestra di dialogo **nuovo GPO controllato** fare clic su **Importa** e quindi su **Avvia procedura guidata**.</span><span class="sxs-lookup"><span data-stu-id="944b2-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="944b2-119">Per altre informazioni su come creare un oggetto Criteri di ricerca, vedere [creare un nuovo oggetto Criteri di controllo controllato](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="944b2-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="944b2-120">Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per il nuovo GPO e immettere un commento per l'audit trail del nuovo GPO.</span><span class="sxs-lookup"><span data-stu-id="944b2-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="944b2-121">Per importare le impostazioni dei criteri in un GPO esistente</span><span class="sxs-lookup"><span data-stu-id="944b2-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="944b2-122">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="944b2-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="944b2-123">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="944b2-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="944b2-124">Vedere il GPO di destinazione a cui si vogliono importare le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="944b2-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="944b2-125">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di destinazione, scegliere **Importa da**e quindi fare clic su **file**.</span><span class="sxs-lookup"><span data-stu-id="944b2-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="944b2-126">Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per sostituirle nell'oggetto Criteri di ricerca e immettere un commento per la traccia di controllo dell'oggetto Criteri di stato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="944b2-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="944b2-127">Per impostazione predefinita, l'oggetto Criteri di stato di destinazione viene archiviato al termine della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="944b2-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="944b2-128">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="944b2-128">Additional considerations</span></span>

-   <span data-ttu-id="944b2-129">Per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato, è necessario avere il **contenuto dell'elenco**, **importare un GPO**e creare le autorizzazioni **GPO** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="944b2-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="944b2-130">Per impostazione predefinita, per eseguire questa procedura è necessario essere un amministratore della Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="944b2-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="944b2-131">Per importare le impostazioni dei criteri in un oggetto Criteri di stato esistente, è necessario avere il **contenuto dell'elenco**, **modificare le impostazioni**e importare le autorizzazioni **GPO** per il dominio e l'oggetto Criteri di controllo deve essere estratto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="944b2-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="944b2-132">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="944b2-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="944b2-133">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="944b2-133">Additional references</span></span>

-   [<span data-ttu-id="944b2-134">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="944b2-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





