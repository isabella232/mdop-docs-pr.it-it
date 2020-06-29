---
title: Testare un oggetto Criteri di gruppo in un'unità organizzativa separata
description: Testare un oggetto Criteri di gruppo in un'unità organizzativa separata
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818256"
---
# <span data-ttu-id="d2d7c-103">Testare un oggetto Criteri di gruppo in un'unità organizzativa separata</span><span class="sxs-lookup"><span data-stu-id="d2d7c-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="d2d7c-104">Se si usa un'unità organizzativa testing (OU) per testare gli oggetti Criteri di gruppo all'interno dello stesso dominio prima della distribuzione nell'ambiente di produzione, è necessario disporre delle autorizzazioni necessarie per accedere all'unità organizzativa di test.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="d2d7c-105">L'uso di un'unità organizzativa di test è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="d2d7c-106">Per usare un'unità organizzativa di test</span><span class="sxs-lookup"><span data-stu-id="d2d7c-106">To use a test OU</span></span>**

1.  <span data-ttu-id="d2d7c-107">Anche se l'oggetto Criteri di **gruppo**è stato estratto per la modifica, fare clic su **oggetti Criteri di gruppo** nell'insieme di strutture e nel dominio in cui si gestiscono i GPO.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="d2d7c-108">Fare clic sulla copia estratta dell'oggetto Criteri di controllo da testare.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="d2d7c-109">Il nome verrà preceduto da **\ [Advanced Group Policy Management \]**.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="d2d7c-110">Se non è elencato, fare clic su **azione**e quindi su **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="d2d7c-111">Ordinare i nomi in ordine alfabetico e **\ [Advanced Group Policy Management \]** i GPO verranno in genere visualizzati nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="d2d7c-112">Trascinare il GPO nell'unità organizzativa di test.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="d2d7c-113">Fare clic su **OK** nella finestra di dialogo che chiede se creare un collegamento al GPO nell'UO di test.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="d2d7c-114">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d2d7c-114">Additional considerations</span></span>

-   <span data-ttu-id="d2d7c-115">Al termine del test, il controllo nel GPO Elimina automaticamente il collegamento alla copia Estratto del GPO.</span><span class="sxs-lookup"><span data-stu-id="d2d7c-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="d2d7c-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d2d7c-116">Additional references</span></span>

-   [<span data-ttu-id="d2d7c-117">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="d2d7c-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





