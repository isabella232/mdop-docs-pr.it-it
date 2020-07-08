---
title: Configurare le connessioni server di Gestione avanzata Criteri di gruppo
description: Configurare le connessioni server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 6062b77b-2fd7-442c-ad1b-6f14419ebd5f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42f2ac4b219bed99db1ceae12859b992f4976db9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821186"
---
# Configurare le connessioni server di Gestione avanzata Criteri di gruppo


Tutte le versioni di ogni oggetto Criteri di gruppo controllato sono archiviate in un archivio centrale, in modo che gli amministratori dei criteri di gruppo possano visualizzare e modificare i GPO offline senza influire immediatamente sulla versione distribuita di ogni GPO.

Un account utente con il ruolo Amministratore Gestione avanzata Criteri di gruppo (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management (Advanced Policy Manager) è necessario per completare queste procedure per la configurazione centralizzata dei percorsi di archiviazione per tutti gli amministratori dei criteri. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Configurazione delle connessioni del server Advanced Group Policy


In qualità di amministratore della gestione avanzata Criteri di gruppo, è possibile verificare che tutti gli amministratori dei criteri di raggruppamento si connettano allo stesso server Advanced Group Policy per la configurazione centralizzata. Se l'ambiente richiede server Advanced Group Policy Management separati per alcuni o tutti i domini, configurare tali server aggiuntivi per Advanced Group Policy Management come eccezioni per l'impostazione predefinita. Se non si configurano in modo centralizzato le connessioni del server Advanced Group Policy Management, ogni amministratore dei criteri di gruppo deve configurare manualmente il server Advanced Group Policy Management da visualizzare per ogni dominio.

-   [Configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori di criteri di gruppo](#bkmk-defaultarchiveloc)

-   [Configurare altre connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo](#bkmk-additionalarchiveloc)

-   [Configurare manualmente una connessione al server Advanced Group Policy Management per l'account](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Per configurare una connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo**

1.  Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.

2.  Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.

3.  Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)**.

4.  Nella finestra **Proprietà** selezionare la casella di controllo **abilitata** e digitare il nome completo del computer e la porta (ad esempio, server.contoso.com:4600).

5.  Fai clic su **OK**. A meno che non si vogliano configurare altre connessioni del server Advanced Group Policy Management, chiudere la finestra **Editor gestione criteri di gruppo** e distribuire l'oggetto criteri. Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca. Quando i criteri di gruppo vengono aggiornati, la connessione del server Advanced Group Policy Management è configurata per tutti gli amministratori dei criteri

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Per configurare altre connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo**

1.  Se non è stata configurata una connessione al server Advanced Group Policy Management, seguire la procedura precedente per configurare un server Advanced Group Policy Management per tutti i domini.

2.  Per configurare distinti server Advanced Group Policy Management per alcuni o tutti i domini (eseguendo l'override del server Advanced Group Policy Manager), nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.

3.  Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione utente**, **criteri**, **modelli amministrativi**, **componenti di Windows**e quindi **Advanced Group Policy**Management.

4.  Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: specificare server Advanced Group Policy Management**.

5.  Nella finestra **Proprietà** selezionare la casella di controllo **abilitata** e fare clic su **Mostra**.

6.  Nella finestra **Mostra contenuto** :

    1.  Fai clic su **Aggiungi**.

    2.  Per **nome valore**Digitare il nome di dominio, ad esempio Server1.contoso.com.

    3.  Per **valore**Digitare il nome del server Advanced Group Policy Management e la porta da usare per il dominio, ad esempio server2.contoso.com:4600, e quindi fare clic su **OK**. (Per impostazione predefinita, il servizio Advanced Group Policy Management ascolta la porta 4600. Per usare una porta diversa, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).

    4.  Ripetere l'impostazione per ogni dominio che non usa il server Advanced Group Policy Management.

7.  Fare clic su **OK** per chiudere le finestre **Mostra contenuto** e **proprietà** .

8.  Chiudere la finestra **Editor gestione criteri di gruppo** . Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca. Quando si aggiornano i criteri di gruppo, le nuove connessioni del server Advanced Group Policy Management sono configurate per tutti gli amministratori dei criteri

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Se è stata configurata centralmente la connessione al server Advanced Group Policy Management, l'opzione per la configurazione manuale non è disponibile per tutti gli amministratori dei criteri di gruppo.

**Per configurare manualmente il server Advanced Group Policy Management da visualizzare per l'account**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .

3.  Immettere il nome completo del computer per il server Advanced Group Policy Management che gestisce l'archivio usato per questo dominio, ad esempio server.contoso.com, e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600).

4.  Fare clic su **applica**e quindi su **Sì** per confermare.

### Considerazioni aggiuntive

-   È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per eseguire le procedure per la configurazione centralizzata delle connessioni del server Advanced Group Policy Management per tutti gli amministratori dei criteri. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm30ops.md) .

-   Il server Advanced Group Policy Management selezionato determina quali GPO vengono visualizzati nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** . Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Configurazione di Gestione avanzata Criteri di gruppo](configuring-advanced-group-policy-management.md)

 

 





