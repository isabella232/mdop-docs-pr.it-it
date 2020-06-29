---
title: Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo
description: Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818325"
---
# <span data-ttu-id="71fcb-103">Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="71fcb-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="71fcb-104">Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.</span><span class="sxs-lookup"><span data-stu-id="71fcb-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="71fcb-105">**Importante**  L'arresto o la disabilitazione del servizio Advanced Group Policy Management impedirà ai client Advanced Group Policy Management di eseguire qualsiasi operazione, ad esempio elenco o modifica GPO, tramite il server.</span><span class="sxs-lookup"><span data-stu-id="71fcb-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="71fcb-106">Per completare questa procedura è necessario un account utente con accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management).</span><span class="sxs-lookup"><span data-stu-id="71fcb-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="71fcb-107">Per avviare o arrestare il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="71fcb-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="71fcb-108">Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server (e quindi il servizio Advanced Group Policy Manager), fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, **strumenti di amministrazione**e quindi fare clic su **Servizi**.</span><span class="sxs-lookup"><span data-stu-id="71fcb-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="71fcb-109">Nell'elenco dei servizi fare clic con il pulsante destro del mouse su **Servizio Advanced Group Policy Management** e scegliere **Start**, **Riavvia**o **Interrompi**.</span><span class="sxs-lookup"><span data-stu-id="71fcb-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="71fcb-110">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71fcb-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="71fcb-111">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="71fcb-111">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="71fcb-112">Per modificare le impostazioni per il servizio, vedere [gestione del servizio Advanced Group Policy Management](managing-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="71fcb-112">To modify settings for the service, see [Managing the AGPM Service](managing-the-agpm-service.md).</span></span>

     

### <span data-ttu-id="71fcb-113">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="71fcb-113">Additional references</span></span>

-   [<span data-ttu-id="71fcb-114">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="71fcb-114">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





