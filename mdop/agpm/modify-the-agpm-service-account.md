---
title: Modificare l'account del servizio Gestione avanzata Criteri di gruppo
description: Modificare l'account del servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820525"
---
# Modificare l'account del servizio Gestione avanzata Criteri di gruppo


Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione. Se questo servizio viene arrestato o disabilitato, i client Advanced Group Policy Management non possono eseguire operazioni tramite il server.

Il percorso di archiviazione e l'account del servizio Advanced Group Policy Management vengono configurati durante l'installazione del server Advanced Group Policy Management e possono essere modificati successivamente tramite installazione **applicazioni** nel server Advanced Group Policy Management.

**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo. Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.

 

Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura.

**Importante**  L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà e sarà concesso **accedere come** autorizzazione del servizio. Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.

Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.

 

**Per modificare l'account del servizio Advanced Group Policy Management**

1.  Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server, fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare clic su **Aggiungi o Rimuovi programmi**.

2.  Fare clic su **Microsoft Advanced Group Policy Management-Server**e quindi su **Cambia**.

3.  Fare clic su **Avanti**e quindi su **modifica**.

4.  Seguire le istruzioni visualizzate per configurare le impostazioni per il servizio Advanced Group Policy Management:

    1.  Per il percorso di archiviazione, confermare o modificare il percorso dell'archivio relativo al server Advanced Group Policy Management. Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.

    2.  Immettere nuove credenziali per l'account del servizio Advanced Group Policy Management.

    3.  Per il proprietario dell'archivio, immettere le credenziali di un amministratore Advanced Group Policy Management (controllo completo).

5.  Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.

### Riferimenti aggiuntivi

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service.md)

 

 





