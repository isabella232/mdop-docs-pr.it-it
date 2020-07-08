---
title: Modificare il servizio Gestione avanzata Criteri di gruppo
description: Modificare il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820505"
---
# Modificare il servizio Gestione avanzata Criteri di gruppo


Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione. Se questo servizio viene arrestato o disabilitato, i client Advanced Group Policy Management non possono eseguire operazioni tramite il server. È possibile modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management e la porta in cui è in ascolto il servizio Advanced Group Policy Management.

**Attenzione**  Non modificare le impostazioni per il servizio Advanced Group Policy Management tramite strumenti e **Servizi** **amministrativi** nel sistema operativo. Questa operazione può impedire l'avvio del servizio Advanced Group Policy Management.

 

Un account utente che è un membro del gruppo Domain Admins e ha accesso al server Advanced Group Policy Management (il computer in cui è installato Microsoft Advanced Group Policy Manager-Server) è necessario per completare questa procedura. È inoltre necessario specificare le credenziali per l'account del servizio Advanced Group Policy Management per completare questa procedura.

**Per modificare il servizio Advanced Group Policy Management**

1.  Nel computer in cui è installato Microsoft Advanced Group Policy Management-Server:

    -   Per WindowsServer2008, fare clic su **Start**, **Pannello di controllo**e **programmi e funzionalità**.

    -   Per WindowsVista, fare clic su **Start**, **Pannello di controllo**, **programmi** **e programmi e funzionalità**.

2.  Fare clic con il pulsante destro del mouse su **Microsoft Advanced Group Policy Management-Server**e quindi scegliere **Cambia**.

3.  Fare clic su **Avanti**e quindi su **modifica**.

4.  Seguire le istruzioni per configurare il servizio Advanced Group Policy Management:

    1.  Nella finestra di dialogo **percorso di archiviazione** immettere una nuova posizione per l'archivio relativo al server Advanced Group Policy Management oppure confermare il percorso di archiviazione corrente e quindi fare clic su **Avanti**.

        **Importante**  Il percorso di archiviazione può puntare a una cartella nel server Advanced Group Policy Management o altrove, ma la posizione deve avere spazio sufficiente per archiviare tutti i GPO e i dati della cronologia gestiti da questo server Advanced Group Policy Management.

         

    2.  Nella finestra di dialogo **account di servizio Advanced Group Policy Management** immettere le credenziali per un account del servizio in cui verrà eseguito il servizio Advanced Group Policy Management e fare clic su **Avanti**.

        **Importante**  La modifica dell'installazione Cancella le credenziali per l'account del servizio Advanced Group Policy Management. È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.

        L'account del servizio Advanced Group Policy Management deve avere accesso completo ai GPO che gestirà e sarà concesso **accedere come** autorizzazione del servizio. Se si gestiscono GPO in un singolo dominio, è possibile impostare l'account di sistema locale per il controller di dominio primario l'account del servizio Advanced Group Policy Management.

        Se si gestiscono gli oggetti Criteri di gruppo in più domini o se un server membro sarà il server Advanced Group Policy Management, è necessario configurare un account diverso come account del servizio Advanced Group Policy Management perché l'account di sistema locale di un controller di dominio non può accedere a GPO in altri domini.

         

    3.  Nella finestra di dialogo **proprietario archivio** immettere il nome utente di un amministratore Advanced Group Policy Management (controllo completo) o di un gruppo di amministratori Advanced Group Policy Management, quindi fare clic su **Avanti**.

        **Nota**  La modifica dell'installazione Cancella le credenziali per il proprietario dell'archivio. È necessario immettere di nuovo le credenziali, ma non è necessario che corrispondano alle credenziali usate durante l'installazione originale.

         

    4.  Nella finestra di dialogo **configurazione porta** Digitare una nuova porta in cui il servizio Advanced Group Policy Management deve ascoltare o confermare la porta attualmente selezionata e fare clic su **Avanti**.

        **Nota**  Per impostazione predefinita, il servizio Advanced Policy Management è in ascolto sulla porta 4600.

        Se si configurano manualmente le eccezioni della porta o si hanno regole per la configurazione delle eccezioni della porta, è possibile deselezionare la casella **di controllo Aggiungi eccezione porta al firewall** .

         

5.  Fare clic su **Cambia**e, al termine dell'installazione, fare clic su **fine**.

6.  Se è stata modificata la porta in cui è in ascolto il servizio Advanced Group Policy Management, modificare la porta nella connessione del server Advanced Group Policy Management per ogni amministratore di criteri di gruppo. Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).

7.  Ripetere la procedura per ogni server Advanced Group Policy Management a cui applicare le modifiche alla configurazione.

### Riferimenti aggiuntivi

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service-agpm30ops.md)

 

 





