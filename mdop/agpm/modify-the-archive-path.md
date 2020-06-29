---
title: Modificare il percorso di archiviazione
description: Modificare il percorso di archiviazione
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820495"
---
# Modificare il percorso di archiviazione


Il percorso di archiviazione è la posizione dell'archivio relativo al server Advanced Group Policy Management. Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o in un altro server della stessa foresta.

Il percorso di archiviazione e l'account del servizio Advanced Group Policy Management vengono configurati durante l'installazione del server Advanced Group Policy Management e possono essere modificati successivamente tramite installazione **applicazioni** nel server Advanced Group Policy Management.

Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura.

**Per modificare il percorso di archiviazione**

1.  Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server, fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare clic su **Aggiungi o Rimuovi programmi**.

2.  Fare clic su **Microsoft Advanced Group Policy Management-Server**e quindi su **Cambia**.

3.  Fare clic su **Avanti**e quindi su **modifica**.

4.  Seguire le istruzioni visualizzate per configurare le impostazioni per il servizio Advanced Group Policy Management:

    1.  Per il percorso di archiviazione, immettere un nuovo percorso per l'archivio relativo al server Advanced Group Policy Management. Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.

    2.  Immettere le credenziali per l'account del servizio Advanced Group Policy Management.

        **Importante**  La modifica dell'installazione Cancella le credenziali per l'account del servizio Advanced Group Policy Management. È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.

        L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà. Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.

        Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.

         

    3.  Per il proprietario dell'archivio, immettere le credenziali di un amministratore Advanced Group Policy Management (controllo completo).

5.  Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.

### Riferimenti aggiuntivi

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service.md)

 

 





