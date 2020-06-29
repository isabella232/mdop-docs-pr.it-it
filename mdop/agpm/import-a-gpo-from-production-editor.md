---
title: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
description: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
author: dansimp
ms.assetid: ffa02b2a-2a43-4fc0-a06e-7d4b59022cc3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 239ac6938645325292bfc647ef89a77710c5f074
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820676"
---
# <span data-ttu-id="a0651-103">Importare un oggetto Criteri di gruppo dall'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="a0651-103">Import a GPO from Production</span></span>


<span data-ttu-id="a0651-104">Se vengono apportate modifiche a un oggetto Criteri di gruppo (GPO) controllato all'esterno della gestione avanzata Criteri di gruppo, è possibile importare una copia del GPO dall'ambiente di produzione e salvarla nell'archivio per avvicinare l'archivio e l'ambiente di produzione a uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="a0651-104">If changes are made to a controlled Group Policy object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="a0651-105">Per importare un oggetto Criteri di controllo non controllato, controlla l'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a0651-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="a0651-106">Vedere [richiedere il controllo di un oggetto Criteri di controllo precedentemente non controllato](request-control-of-a-previously-uncontrolled-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="a0651-106">See [Request Control of a Previously Uncontrolled GPO](request-control-of-a-previously-uncontrolled-gpo.md).)</span></span>

<span data-ttu-id="a0651-107">Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="a0651-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="a0651-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a0651-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a0651-109">Per importare un GPO dall'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="a0651-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="a0651-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="a0651-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a0651-111">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="a0651-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="a0651-112">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di scelta e quindi scegliere **Importa dalla produzione**.</span><span class="sxs-lookup"><span data-stu-id="a0651-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="a0651-113">Digitare un commento per l'audit trail dell'oggetto Criteri di controllo, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0651-113">Type a comment for the audit trail of the GPO, then click **OK**.</span></span>

### <span data-ttu-id="a0651-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a0651-114">Additional considerations</span></span>

-   <span data-ttu-id="a0651-115">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un responsabile dell'approvazione o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="a0651-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a0651-116">In particolare, devi avere il **contenuto dell'elenco** e **modificare le impostazioni**, **distribuire GPO**o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a0651-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="a0651-117">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="a0651-117">Additional references</span></span>

-   [<span data-ttu-id="a0651-118">Creazione, controllo o importazione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a0651-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





