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
# Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo


Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.

**Importante**  L'arresto o la disabilitazione del servizio Advanced Group Policy Management impedirà ai client Advanced Group Policy Management di eseguire qualsiasi operazione, ad esempio elenco o modifica GPO, tramite il server.

 

Per completare questa procedura è necessario un account utente con accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management).

**Per avviare o arrestare il servizio Advanced Group Policy Management**

1.  Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server (e quindi il servizio Advanced Group Policy Manager), fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, **strumenti di amministrazione**e quindi fare clic su **Servizi**.

2.  Nell'elenco dei servizi fare clic con il pulsante destro del mouse su **Servizio Advanced Group Policy Management** e scegliere **Start**, **Riavvia**o **Interrompi**.

    **Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo. Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management. Per modificare le impostazioni per il servizio, vedere [gestione del servizio Advanced Group Policy Management](managing-the-agpm-service.md).

     

### Riferimenti aggiuntivi

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service.md)

 

 





