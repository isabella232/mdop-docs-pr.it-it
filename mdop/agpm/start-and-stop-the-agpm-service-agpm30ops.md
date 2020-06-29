---
title: Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo
description: Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820216"
---
# <span data-ttu-id="6e2c4-103">Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6e2c4-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="6e2c4-104">Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="6e2c4-105">**Importante**  L'arresto o la disabilitazione del servizio Advanced Group Policy Management impedirà ai client Advanced Group Policy Management di eseguire qualsiasi operazione, ad esempio elenco o modifica GPO, tramite il server.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="6e2c4-106">Per completare questa procedura è necessario un account utente con accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management).</span><span class="sxs-lookup"><span data-stu-id="6e2c4-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="6e2c4-107">Per avviare o arrestare il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="6e2c4-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="6e2c4-108">Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server (e quindi il servizio Advanced Group Policy Manager), fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, **strumenti di amministrazione**e quindi fare clic su **Servizi**.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="6e2c4-109">Nell'elenco dei servizi fare clic con il pulsante destro del mouse su **Servizio Advanced Group Policy Management** e scegliere **Start**, **Riavvia**o **Interrompi**.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="6e2c4-110">**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="6e2c4-111">Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="6e2c4-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="6e2c4-112">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="6e2c4-112">Additional references</span></span>

-   [<span data-ttu-id="6e2c4-113">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6e2c4-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





