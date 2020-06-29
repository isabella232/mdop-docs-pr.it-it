---
title: Configurare una connessione al server di Gestione avanzata Criteri di gruppo
description: Configurare una connessione al server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 409cbbcf-3b0e-459d-9bd2-75cb7b9430b0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7fdc26045b478da14957cdfe6000d58ab72a064
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819085"
---
# <span data-ttu-id="d6af6-103">Configurare una connessione al server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d6af6-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="d6af6-104">Per assicurarsi di essere connessi all'archivio centrale corretto, esaminare la configurazione della connessione al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="d6af6-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="d6af6-105">Se un amministratore Advanced Group Policy Management (controllo completo) non ha configurato una connessione al server Advanced Group Policy Management, è necessario configurarlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="d6af6-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="d6af6-106">Per selezionare un server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="d6af6-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="d6af6-107">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="d6af6-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d6af6-108">Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** :</span><span class="sxs-lookup"><span data-stu-id="d6af6-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="d6af6-109">Se le opzioni della scheda **server Advanced Group Policy Management** non sono disponibili, sono state configurate centralmente da un amministratore della Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="d6af6-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="d6af6-110">Se sono disponibili le opzioni della scheda **server Advanced Group Policy** Management, digitare il nome completo del computer per il server Advanced Group Policy Management (ad esempio, server.contoso.com) e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600).</span><span class="sxs-lookup"><span data-stu-id="d6af6-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="d6af6-111">Fare clic su **applica**e quindi su **Sì** per confermare.</span><span class="sxs-lookup"><span data-stu-id="d6af6-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="d6af6-112">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d6af6-112">Additional considerations</span></span>

-   <span data-ttu-id="d6af6-113">I server Advanced Group Policy Management selezionati determinano gli oggetti Criteri di visualizzazione nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="d6af6-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="d6af6-114">Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.</span><span class="sxs-lookup"><span data-stu-id="d6af6-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="d6af6-115">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d6af6-115">Additional references</span></span>

-   [<span data-ttu-id="d6af6-116">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="d6af6-116">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





