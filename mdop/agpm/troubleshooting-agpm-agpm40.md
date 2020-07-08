---
title: Risoluzione dei problemi relativi a Gestione avanzata Criteri di gruppo
description: Risoluzione dei problemi relativi a Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820155"
---
# Risoluzione dei problemi relativi a Gestione avanzata Criteri di gruppo


In questa sezione vengono elencati i problemi comuni che possono verificarsi quando si usa Gestione criteri di gruppo avanzati per gestire gli oggetti Criteri di gruppo. Per diagnosticare i problemi non elencati in questo articolo, potrebbe essere utile per un amministratore Advanced Group Policy Management (controllo completo) usare la registrazione e la traccia. Per altre informazioni, vedere [configurare la registrazione e la traccia](configure-logging-and-tracing-agpm40.md).

**Nota**  
-   Per informazioni su come ripristinare una versione precedente di un GPO in caso di problemi, vedere [eseguire il rollback a una versione precedente di un oggetto Criteri di](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)ricerca.

-   Per informazioni su come recuperare da un disastro ripristinando l'archivio completo da un backup, vedere [ripristinare l'archivio da un backup](restore-the-archive-from-a-backup-agpm40.md).

 

## Quali problemi si verificano?


-   [Non è possibile accedere a un archivio](#bkmk-access-an-archive)

-   [Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi](#bkmk-state-varies)

-   [Non è possibile modificare la connessione al server Advanced Group Policy Management](#bkmk-modify-archive-location)

-   [Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO](#bkmk-perform-task)

-   [Non è possibile usare un nome di GPO specifico](#bkmk-use-particular-name)

-   [Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management](#bkmk-email)

-   [Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management](#bkmk-port)

-   [Il servizio Advanced Group Policy Management non si avvia](#bkmk-not-start)

-   [L'installazione del software di criteri di gruppo non riesce ad installare](#bkmk-software-installation)

-   [Si è verificato un errore quando è stato ripristinato l'archivio in un nuovo server Advanced Group Policy Management](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a>Non è possibile accedere a un archivio

-   **Causa**: non è stato selezionato il server e la porta corretti per l'archivio.

-   **Soluzione**:

    -   Se si è un amministratore Advanced Group Policy Management: vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm40.md).

    -   Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata. Vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-agpm40.md).

-   **Causa**: il servizio Advanced Group Policy Management non è in esecuzione.

-   **Soluzione**:

    -   Se si è un amministratore della Advanced Group Policy Management: avviare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).

    -   Se non si è un amministratore della Advanced Group Policy Management: contattare un amministratore della Advanced Group Policy per assistenza.

### <a href="" id="bkmk-state-varies"></a>Lo stato GPO varia per gli amministratori dei criteri di gruppo diversi

-   **Causa**: diversi amministratori dei criteri di gruppo hanno selezionato diversi server Advanced Group Policy Management per lo stesso archivio.

-   **Soluzione**:

    -   Se si è un amministratore Advanced Group Policy Management: vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm40.md).

    -   Se non si è un amministratore Advanced Group Policy Management: richiedere i dettagli di connessione per il server Advanced Group Policy Management da un amministratore della gestione avanzata. Vedere [configurare una connessione al server Advanced Group Policy Management](configure-an-agpm-server-connection-agpm40.md).

### <a href="" id="bkmk-modify-archive-location"></a>Non è possibile modificare la connessione al server Advanced Group Policy Management

-   **Causa**: se le impostazioni nella scheda **server Advanced Group Policy Management** non sono disponibili, il server Advanced Group Policy Management è stato configurato centralmente usando un modello amministrativo.

-   **Soluzione**:

    -   Se si è un amministratore Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy Management** non sono disponibili, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm40.md).

    -   Se non si è un amministratore di Advanced Group Policy Management: se le impostazioni nella scheda **server Advanced Group Policy** Management non sono disponibili, non è necessario modificare il server Advanced Group Policy Management.

### <a href="" id="bkmk-perform-task"></a>Non è possibile modificare il modello o la visualizzazione predefinita, creare, modificare, rinominare, distribuire o eliminare GPO

-   **Causa**: non è stato assegnato un ruolo con le autorizzazioni necessarie per eseguire l'attività o le attività.

-   **Soluzione**:

    -   Se si è un amministratore della Advanced Group Policy Management: vedere [delegare l'accesso a livello di dominio all'archivio](delegate-domain-level-access-to-the-archive-agpm40.md) e [delegare l'accesso a un singolo GPO nell'archivio](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md). Le autorizzazioni Advanced Group Policy Management verranno sovrapposte dal dominio a tutti i GPO attualmente presenti nell'archivio. Per informazioni dettagliate sui ruoli che possono eseguire un'attività e le autorizzazioni necessarie per eseguire un'attività, vedere la guida relativa all'attività.

    -   Se non si è un amministratore di Advanced Group Policy Management e si richiedono ulteriori ruoli o autorizzazioni: contattare un amministratore della Advanced Group Policy per assistenza. Tenere presente che, se si è un editor, è possibile iniziare il processo di creazione di un GPO, distribuire un GPO o eliminare un GPO dall'ambiente di produzione del dominio, ma un approvatore o un amministratore della Advanced Group Policy Management deve approvare la richiesta.

### <a href="" id="bkmk-use-particular-name"></a>Non è possibile usare un nome di GPO specifico

-   **Causa**: il nome del GPO è già in uso o manca l'autorizzazione per elencare il GPO.

-   **Soluzione**:

    -   Se il nome del GPO viene visualizzato nella scheda **controllata** **, non controllata o** **in sospeso** , scegliere un altro nome. Se un oggetto Criteri di gruppo distribuito viene rinominato ma non ancora ridistribuito, verrà visualizzato sotto il nome precedente nell'ambiente di produzione del dominio. Di conseguenza, il vecchio nome viene ancora usato. Ridistribuire il GPO per aggiornarne il nome nell'ambiente di produzione e rilasciare tale nome per l'uso da parte di un altro GPO.

    -   Se il nome del GPO non viene visualizzato nella scheda **controllato**, non controllata o **in sospeso** , potrebbe mancare l'autorizzazione per elencare l'oggetto Criteri di **controllo**. Per richiedere l'autorizzazione, contattare un amministratore della Advanced Group Policy Management.

### <a href="" id="bkmk-email"></a>Non ricevo le notifiche tramite posta elettronica Advanced Group Policy Management

-   **Causa**: non è stato fornito un server di posta elettronica SMTP valido e un indirizzo di posta elettronica oppure non è stata eseguita alcuna azione che genera una notifica tramite posta elettronica.

-   **Soluzione**:

    -   Se si è un amministratore della Advanced Group Policy Management: per le notifiche tramite posta elettronica relative alle azioni in sospeso da inviare da Advanced Group Policy Management, un amministratore Advanced Group Policy Management deve specificare un server di posta elettronica SMTP valido e gli indirizzi di posta elettronica per i responsabili approvazione nella scheda **delega** Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm40.md).

    -   Le notifiche tramite posta elettronica vengono generate solo quando un editor, un revisore o un altro amministratore di criteri di gruppo che non dispone delle autorizzazioni necessarie per creare, distribuire o eliminare un GPO invia una richiesta di una di queste azioni. Non esiste una notifica automatica di approvazione o rifiuto di una richiesta.

### <a href="" id="bkmk-port"></a>Non è possibile usare la porta 4600 per il servizio Advanced Group Policy Management

-   **Causa**: per impostazione predefinita, la porta su cui è in ascolto il servizio Advanced Group Policy Management è la porta 4600.

-   **Soluzione**: se la porta 4600 non è disponibile per il servizio Advanced Group Policy Management, modificare la configurazione della porta nel server Advanced Group Policy Management per usare un'altra porta e quindi aggiornare la porta nella connessione del server Advanced Group Policy Management per i client Advanced Group Policy Management Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-not-start"></a>Il servizio Advanced Group Policy Management non si avvia

-   **Causa**: sono state modificate le impostazioni per il servizio Advanced Group Policy Management nel sistema operativo in strumenti e **Servizi** **amministrativi** .

-   **Soluzione**: modificare le impostazioni per **Microsoft Advanced Group Policy Management-Server** in **programmi e funzionalità** nel pannello di controllo. Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-software-installation"></a>L'installazione del software di criteri di gruppo non riesce ad installare

-   **Causa**: Advanced Group Policy Management mantiene l'integrità dei pacchetti di installazione del software di criteri di gruppo. Anche se i GPO vengono modificati offline, vengono mantenuti i collegamenti tra i pacchetti oltre alle informazioni memorizzate nella cache. Questo comportamento è da progettazione.

-   **Soluzione**: quando si modifica un oggetto Criteri di gruppo in modalità offline con Advanced Group Policy Management, configurare qualsiasi aggiornamento del software di un pacchetto in un altro GPO per fare riferimento al GPO distribuito, non alla copia selezionata. L'editor deve avere l'autorizzazione di **lettura** per l'oggetto Criteri di ricerca distribuito.

### <a href="" id="bkmk-error-on-restore"></a>Si è verificato un errore quando è stato ripristinato l'archivio in un nuovo server Advanced Group Policy Management

-   **Causa**: per motivi di sicurezza, la crittografia che protegge la password immessa nella scheda **delega del dominio** fa sì che la password non riesca se l'archivio viene spostato in un altro computer.

-   **Soluzione**: immettere di nuovo e confermare la password nella scheda **delega del dominio** . Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm40.md).

 

 





