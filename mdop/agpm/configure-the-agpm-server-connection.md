---
title: Configurare la connessione al server di Gestione avanzata Criteri di gruppo
description: Configurare la connessione al server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818915"
---
# Configurare la connessione al server di Gestione avanzata Criteri di gruppo


Advanced Group Policy Management consente di archiviare tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato in un archivio centrale, in modo che gli amministratori dei criteri di gruppo possano visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni GPO.

Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie per la gestione dei criteri di raggruppamento avanzati è necessario per completare queste procedure per la configurazione centralizzata dei percorsi di archiviazione per tutti gli amministratori dei criteri di gruppo. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Configurazione della connessione del server Advanced Group Policy Management


In qualità di amministratore Advanced Group Policy Management (controllo completo), è possibile verificare che tutti gli amministratori dei criteri di gruppo si connettano allo stesso server Advanced Group Policy configurando centralmente l'impostazione. Se l'ambiente richiede server Advanced Group Policy Management separati per alcuni o tutti i domini, configurare tali server aggiuntivi per Advanced Group Policy Management come eccezioni per l'impostazione predefinita. Se non si configurano in modo centralizzato le connessioni del server Advanced Group Policy Management, ogni amministratore dei criteri di gruppo deve configurare manualmente il server Advanced Group Policy Management da visualizzare per ogni dominio.

-   [Configurare un server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo](#bkmk-defaultarchiveloc)

-   [Configurare altri server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo](#bkmk-additionalarchiveloc)

-   [Configurare manualmente un server Advanced Group Policy Management per l'account](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Per configurare un server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo**

1.  Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.

2.  Nell' **Editor oggetti Criteri di gruppo**fare clic su **Configurazione utente**, **modelli amministrativi**e **componenti di Windows**.

3.  Se **Advanced Group Policy Management** non è elencato in **componenti di Windows**:

    1.  Fare clic con il pulsante destro del mouse su **modelli amministrativi** e scegliere **Aggiungi/Rimuovi modelli**.

    2.  Fare clic su **Aggiungi**, selezionare **Advanced Group Policy Management. admx** o **Advanced Group Policy Management. adm**, fare clic su **Apri**e quindi su **Chiudi**.

4.  In **componenti di Windows**fare doppio clic su **Advanced Group Policy Management**.

5.  Nel riquadro dei dettagli fare doppio clic su **server Advanced Group Policy Management (tutti i domini)**.

6.  Nella finestra delle **proprietà del server Advanced Group Policy Management (tutti i domini)** selezionare la casella di controllo **abilitata** e digitare il nome completo del computer e la porta (ad esempio, server.contoso.com:4600).

7.  Fai clic su **OK**. A meno che non si vogliano configurare altre connessioni del server Advanced Group Policy Management, chiudere l' **Editor oggetti Criteri di gruppo** e distribuire il GPO. Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management è configurata per tutti gli amministratori dei criteri

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Per configurare altri server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo**

1.  Se non è stata configurata una connessione al server Advanced Group Policy Management, seguire la procedura precedente per configurare un server Advanced Group Policy Management per tutti i domini.

2.  Per configurare distinti server Advanced Group Policy Management per alcuni o tutti i domini (eseguendo l'override del server Advanced Group Policy Manager), nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.

3.  In **Configurazione utente** nell' **Editor oggetti Criteri di gruppo**fare doppio clic su **modelli amministrativi**, **componenti di Windows**e quindi **Advanced Group Policy Management**.

4.  Nel riquadro dei dettagli fare doppio clic su **server Advanced Group Policy Management**.

5.  Nella finestra delle **proprietà del server Advanced Group Policy Management** selezionare la casella di controllo **abilitata** e fare clic su **Mostra**.

6.  Nella finestra **Mostra contenuto** :

    1.  Fai clic su **Aggiungi**.

    2.  Per **nome valore**Digitare il nome di dominio, ad esempio Server1.contoso.com.

    3.  Per **valore**Digitare il nome del server Advanced Group Policy Management e la porta da usare per il dominio, ad esempio server2.contoso.com:4600, e quindi fare clic su **OK**. (Per impostazione predefinita, il servizio Advanced Group Policy Management ascolta la porta 4600. Per usare una porta diversa, vedere [modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management](modify-the-port-on-which-the-agpm-service-listens.md).

    4.  Ripetere l'impostazione per ogni dominio che non usa il server Advanced Group Policy Management.

7.  Fare clic su **OK** per chiudere le finestre **Mostra contenuto** e **proprietà del server Advanced Group Policy Management** .

8.  Chiudere l' **Editor oggetti Criteri di gruppo**. Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Quando si aggiornano i criteri di gruppo, le nuove connessioni del server Advanced Group Policy Management sono configurate per tutti gli amministratori dei criteri

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Se la connessione al server Advanced Group Policy Management è stata configurata in modo centralizzato, l'opzione manualmente non è disponibile per tutti gli amministratori dei criteri di gruppo.

**Per configurare manualmente il server Advanced Group Policy Management da visualizzare per l'account**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .

3.  Immettere il nome completo del computer per il server Advanced Group Policy Management che gestisce l'archivio usato per questo dominio, ad esempio server.contoso.com, e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600).

4.  Fare clic su **applica**e quindi su **Sì** per confermare.

### Considerazioni aggiuntive

-   È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per eseguire le procedure per la configurazione centralizzata delle connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo.md) .

-   Il server Advanced Group Policy Management selezionato determina quali GPO vengono visualizzati nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** . Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione dell'accesso a GPO da Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

 

 





