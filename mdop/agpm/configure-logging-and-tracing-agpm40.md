---
title: Configurare registrazione e traccia
description: Configurare registrazione e traccia
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818966"
---
# <span data-ttu-id="7f6ee-103">Configurare registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="7f6ee-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="7f6ee-104">È possibile configurare centralmente la registrazione e la traccia facoltativa usando i modelli amministrativi.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="7f6ee-105">Può essere utile quando si diagnosticano eventuali problemi relativi alla gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="7f6ee-106">Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management è necessario per completare queste procedure.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="7f6ee-107">Inoltre, è necessario un account utente con accesso al server Advanced Group Policy Management per avviare la registrazione nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="7f6ee-108">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="7f6ee-109">Per configurare la registrazione e la traccia per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="7f6ee-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="7f6ee-110">Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento per cui si vuole attivare la registrazione e la traccia.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="7f6ee-111">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm40.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="7f6ee-112">Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione computer**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="7f6ee-113">Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: configurare la registrazione**.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="7f6ee-114">Nella finestra **Proprietà** fare clic su **abilitato**e configurare il livello di dettaglio da registrare nei registri.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="7f6ee-115">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-115">Click **OK**.</span></span>

6.  <span data-ttu-id="7f6ee-116">Chiudere la finestra **Editor gestione criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="7f6ee-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="7f6ee-117">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm40.md)di ricerca. Dopo l'aggiornamento dei criteri di gruppo, è necessario riavviare il servizio Advanced Group Policy Management per avviare, modificare o interrompere la registrazione nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="7f6ee-118">Gli amministratori dei criteri di gruppo devono chiudere e riavviare la console GPMC per avviare, modificare o interrompere la registrazione nei propri computer.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="7f6ee-119">**Percorsi dei file di traccia**:</span><span class="sxs-lookup"><span data-stu-id="7f6ee-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="7f6ee-120">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="7f6ee-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="7f6ee-121">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="7f6ee-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="7f6ee-122">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7f6ee-122">Additional considerations</span></span>

-   <span data-ttu-id="7f6ee-123">È necessario essere in grado di modificare e distribuire un GPO per configurare la registrazione e la traccia di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="7f6ee-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="7f6ee-124">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm40.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6ee-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="7f6ee-125">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="7f6ee-125">Additional references</span></span>

-   [<span data-ttu-id="7f6ee-126">Configurazione di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="7f6ee-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





