---
title: Usare l'ambiente di test
description: Usare l'ambiente di test
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818235"
---
# <span data-ttu-id="34226-103">Usare l'ambiente di test</span><span class="sxs-lookup"><span data-stu-id="34226-103">Use a Test Environment</span></span>


<span data-ttu-id="34226-104">Se si usa un'unità organizzativa testing (OU) per testare gli oggetti Criteri di gruppo prima della distribuzione nell'ambiente di produzione, è necessario disporre delle autorizzazioni necessarie per accedere all'unità organizzativa di test.</span><span class="sxs-lookup"><span data-stu-id="34226-104">If you use a testing organizational unit (OU) to test Group Policy objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="34226-105">L'uso di un'unità organizzativa di test è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34226-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="34226-106">Per usare un'unità organizzativa di test</span><span class="sxs-lookup"><span data-stu-id="34226-106">To use a test OU</span></span>**

1.  <span data-ttu-id="34226-107">Durante l'estrazione del GPO per la modifica, nella **console Gestione criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si gestiscono i GPO.</span><span class="sxs-lookup"><span data-stu-id="34226-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="34226-108">Fare clic sulla copia estratta dell'oggetto Criteri di controllo da testare.</span><span class="sxs-lookup"><span data-stu-id="34226-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="34226-109">Il nome verrà preceduto da **\ [Advanced Group Policy Management \]**.</span><span class="sxs-lookup"><span data-stu-id="34226-109">The name will be preceded with **\[AGPM\]**.</span></span> <span data-ttu-id="34226-110">Se non è elencato, fare clic su **azione**e quindi su **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="34226-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="34226-111">Ordinare i nomi in ordine alfabetico e **\ [Advanced Group Policy Management \]** i GPO verranno in genere visualizzati nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="34226-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="34226-112">Trascinare e rilasciare il GPO nell'unità organizzativa di test.</span><span class="sxs-lookup"><span data-stu-id="34226-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="34226-113">Fare clic su **OK** nella finestra di dialogo in cui viene chiesto se creare un collegamento al GPO nell'UO di test.</span><span class="sxs-lookup"><span data-stu-id="34226-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="34226-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="34226-114">Additional considerations</span></span>

-   <span data-ttu-id="34226-115">Al termine del test, il controllo nel GPO Elimina automaticamente il collegamento alla copia Estratto del GPO.</span><span class="sxs-lookup"><span data-stu-id="34226-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="34226-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="34226-116">Additional references</span></span>

-   [<span data-ttu-id="34226-117">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="34226-117">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





