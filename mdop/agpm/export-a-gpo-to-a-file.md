---
title: Esportare un oggetto Criteri di gruppo in un file
description: Esportare un oggetto Criteri di gruppo in un file
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820855"
---
# <span data-ttu-id="e7110-103">Esportare un oggetto Criteri di gruppo in un file</span><span class="sxs-lookup"><span data-stu-id="e7110-103">Export a GPO to a File</span></span>


<span data-ttu-id="e7110-104">È possibile esportare un oggetto Criteri di gruppo (GPO) controllato in un file CAB in modo da poterlo copiare in un dominio in un'altra foresta e importare il GPO in Advanced Group Policy Management in tale dominio.</span><span class="sxs-lookup"><span data-stu-id="e7110-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="e7110-105">Per informazioni su come importare le impostazioni GPO in un GPO nuovo o esistente, vedere [importare un oggetto Criteri di ricerca da un file](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="e7110-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="e7110-106">Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e7110-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="e7110-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e7110-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e7110-108">Per esportare un oggetto Criteri di un file</span><span class="sxs-lookup"><span data-stu-id="e7110-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="e7110-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="e7110-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e7110-110">Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="e7110-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e7110-111">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di scelta e quindi scegliere **Esporta in**.</span><span class="sxs-lookup"><span data-stu-id="e7110-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="e7110-112">Immettere un nome file per il file a cui si vuole esportare l'oggetto Criteri di ricerca e quindi fare clic su **Esporta**.</span><span class="sxs-lookup"><span data-stu-id="e7110-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="e7110-113">Se il file non esiste, viene creato.</span><span class="sxs-lookup"><span data-stu-id="e7110-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="e7110-114">Se esiste già, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="e7110-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="e7110-115">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e7110-115">Additional considerations</span></span>

-   <span data-ttu-id="e7110-116">Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="e7110-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e7110-117">In particolare, devi avere il **contenuto dell'elenco**, **le impostazioni di lettura**ed esportare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e7110-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="e7110-118">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="e7110-118">Additional references</span></span>

-   [<span data-ttu-id="e7110-119">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="e7110-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





