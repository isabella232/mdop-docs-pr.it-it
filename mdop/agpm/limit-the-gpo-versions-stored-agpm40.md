---
title: Limitare le versioni degli oggetti Criteri di gruppo archiviate
description: Limitare le versioni degli oggetti Criteri di gruppo archiviate
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820616"
---
# <span data-ttu-id="9ef5d-103">Limitare le versioni degli oggetti Criteri di gruppo archiviate</span><span class="sxs-lookup"><span data-stu-id="9ef5d-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="9ef5d-104">Per impostazione predefinita, tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato vengono mantenute nell'archivio nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="9ef5d-105">Tuttavia, puoi limitare il numero di versioni conservate per ogni GPO ed eliminare le versioni meno recenti quando tale limite viene superato.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="9ef5d-106">Quando vengono eliminate le versioni di GPO, un record della versione rimane nella cronologia dell'oggetto Criteri di controllo, ma la versione del GPO viene eliminata dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="9ef5d-107">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9ef5d-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9ef5d-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9ef5d-109">Per limitare il numero di versioni degli oggetti Criteri di archiviazione archiviate</span><span class="sxs-lookup"><span data-stu-id="9ef5d-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="9ef5d-110">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9ef5d-111">Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .</span><span class="sxs-lookup"><span data-stu-id="9ef5d-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="9ef5d-112">Selezionare la casella di controllo **Elimina versioni precedenti di ogni oggetto Criteri** di ricerca e digitare il numero massimo di versioni di GPO da archiviare per ogni oggetto Criteri di ricerca, senza includere la versione corrente.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="9ef5d-113">Per mantenere solo la versione corrente, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="9ef5d-114">Il valore massimo non deve essere maggiore di 999.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="9ef5d-115">**Importante**  Solo le versioni di GPO visualizzate nella scheda **versioni univoche** del conteggio della finestra **cronologia** verso il limite.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="9ef5d-116">Fare clic sul pulsante **applica** .</span><span class="sxs-lookup"><span data-stu-id="9ef5d-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="9ef5d-117">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9ef5d-117">Additional considerations</span></span>

-   <span data-ttu-id="9ef5d-118">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9ef5d-119">In particolare, devi avere il **contenuto dell'elenco** e modificare le autorizzazioni di **Opzioni** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="9ef5d-120">È possibile impedire l'eliminazione di una versione di un GPO contrassegnata nella cronologia come non idonea per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="9ef5d-121">A questo scopo, fai clic con il pulsante destro del mouse sulla versione nella cronologia del GPO e fai clic su non **eliminare**.</span><span class="sxs-lookup"><span data-stu-id="9ef5d-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="9ef5d-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9ef5d-122">Additional references</span></span>

-   [<span data-ttu-id="9ef5d-123">Gestione dell'archivio</span><span class="sxs-lookup"><span data-stu-id="9ef5d-123">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





