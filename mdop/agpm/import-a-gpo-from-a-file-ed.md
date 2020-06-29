---
title: Importare un oggetto Criteri di gruppo da un file
description: Importare un oggetto Criteri di gruppo da un file
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820725"
---
# <span data-ttu-id="264db-103">Importare un oggetto Criteri di gruppo da un file</span><span class="sxs-lookup"><span data-stu-id="264db-103">Import a GPO from a File</span></span>


<span data-ttu-id="264db-104">In Advanced Group Policy Management, se è stato esportato un oggetto Criteri di gruppo (GPO) in un file CAB, è possibile importare le impostazioni dei criteri da tale oggetto Criteri di gruppo in un GPO esistente in un dominio in un'altra foresta.</span><span class="sxs-lookup"><span data-stu-id="264db-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="264db-105">L'importazione delle impostazioni dei criteri in un GPO esistente sostituisce tutte le impostazioni dei criteri all'interno di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="264db-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="264db-106">Per informazioni sull'esportazione di impostazioni GPO in un file CAB, vedere [esportare un oggetto Criteri di ricerca in un file](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="264db-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="264db-107">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="264db-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="264db-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="264db-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="264db-109">Per importare le impostazioni dei criteri in un GPO esistente</span><span class="sxs-lookup"><span data-stu-id="264db-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="264db-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="264db-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="264db-111">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="264db-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="264db-112">Vedere il GPO di destinazione a cui si vogliono importare le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="264db-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="264db-113">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di destinazione, scegliere **Importa da**e quindi fare clic su **file**.</span><span class="sxs-lookup"><span data-stu-id="264db-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="264db-114">Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per sostituirle nell'oggetto Criteri di ricerca e immettere un commento per la traccia di controllo dell'oggetto Criteri di stato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="264db-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="264db-115">Per impostazione predefinita, l'oggetto Criteri di stato di destinazione viene archiviato al termine della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="264db-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="264db-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="264db-116">Additional considerations</span></span>

-   <span data-ttu-id="264db-117">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="264db-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="264db-118">In particolare, devi avere il **contenuto dell'elenco**, **modificare le impostazioni**e importare le autorizzazioni **GPO** per il dominio e il GPO deve essere estratto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="264db-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="264db-119">Anche se un editor non può importare le impostazioni dei criteri in un nuovo oggetto Criteri di ricerca durante la creazione, un editor può richiedere la creazione di un nuovo oggetto Criteri di ricerca e quindi importarvi le impostazioni del criterio al termine della sua realizzazione.</span><span class="sxs-lookup"><span data-stu-id="264db-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="264db-120">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="264db-120">Additional references</span></span>

-   [<span data-ttu-id="264db-121">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="264db-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





