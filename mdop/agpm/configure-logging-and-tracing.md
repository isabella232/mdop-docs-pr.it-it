---
title: Configurare registrazione e traccia
description: Configurare registrazione e traccia
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818975"
---
# <span data-ttu-id="9965b-103">Configurare registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="9965b-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="9965b-104">È possibile configurare centralmente la registrazione e la traccia facoltative per Advanced Group Policy Management (Advanced criteri di gruppo) usando modelli amministrativi.</span><span class="sxs-lookup"><span data-stu-id="9965b-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="9965b-105">Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie per la gestione dei criteri di raggruppamento avanzati è necessario per completare queste procedure.</span><span class="sxs-lookup"><span data-stu-id="9965b-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="9965b-106">Inoltre, è necessario un account utente con accesso al server Advanced Group Policy Management per avviare la registrazione nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="9965b-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="9965b-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9965b-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9965b-108">Per configurare la registrazione e la traccia per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9965b-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="9965b-109">Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento per cui si vuole attivare la registrazione e la traccia.</span><span class="sxs-lookup"><span data-stu-id="9965b-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="9965b-110">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9965b-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="9965b-111">Nell' **Editor oggetti Criteri di gruppo**fare clic su **Configurazione computer**, **modelli amministrativi**e **componenti di Windows**.</span><span class="sxs-lookup"><span data-stu-id="9965b-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="9965b-112">Se **Advanced Group Policy Management** non è elencato in **componenti di Windows**:</span><span class="sxs-lookup"><span data-stu-id="9965b-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="9965b-113">Fare clic con il pulsante destro del mouse su **modelli amministrativi** e scegliere **Aggiungi/Rimuovi modelli**.</span><span class="sxs-lookup"><span data-stu-id="9965b-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="9965b-114">Fare clic su **Aggiungi**, selezionare **Advanced Group Policy Management. admx** o **Advanced Group Policy Management. adm**, fare clic su **Apri**e quindi su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="9965b-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="9965b-115">In **componenti di Windows**fare doppio clic su **Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="9965b-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="9965b-116">Nel riquadro dei dettagli fare doppio clic su **registrazione Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="9965b-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="9965b-117">Nella finestra **Proprietà registrazione Advanced Group Policy Management** fare clic su **Enabled**e configurare il livello di dettaglio da registrare nei registri.</span><span class="sxs-lookup"><span data-stu-id="9965b-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="9965b-118">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="9965b-118">Click **OK**.</span></span>

8.  <span data-ttu-id="9965b-119">Chiudere l' **Editor oggetti Criteri di gruppo**.</span><span class="sxs-lookup"><span data-stu-id="9965b-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="9965b-120">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Dopo l'aggiornamento dei criteri di gruppo, è necessario riavviare il servizio Advanced Group Policy Management per iniziare la registrazione nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="9965b-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="9965b-121">Gli amministratori dei criteri di gruppo devono chiudere e riavviare la GPMC per iniziare la registrazione nei propri computer.</span><span class="sxs-lookup"><span data-stu-id="9965b-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="9965b-122">**Percorsi dei file di traccia**:</span><span class="sxs-lookup"><span data-stu-id="9965b-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="9965b-123">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="9965b-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="9965b-124">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="9965b-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="9965b-125">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9965b-125">Additional considerations</span></span>

-   <span data-ttu-id="9965b-126">È necessario essere in grado di modificare e distribuire un GPO per configurare la registrazione e la traccia di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="9965b-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="9965b-127">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="9965b-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="9965b-128">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9965b-128">Additional references</span></span>

-   [<span data-ttu-id="9965b-129">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="9965b-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





