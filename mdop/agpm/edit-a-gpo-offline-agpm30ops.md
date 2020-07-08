---
title: Modificare un oggetto Criteri di gruppo offline
description: Modificare un oggetto Criteri di gruppo offline
author: dansimp
ms.assetid: 51677d8a-6209-41b5-82ed-4f3be817abc0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74b6ae9fdf11456a9a45cb5504ed97a9bc6aecb4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818625"
---
# Modificare un oggetto Criteri di gruppo offline


Per apportare modifiche a un oggetto Criteri di gruppo controllato, è necessario prima di tutto estrarre una copia del GPO dall'archivio. Nessun altro sarà in grado di modificare l'oggetto Criteri di gruppo finché non viene archiviato di nuovo, impedendo l'introduzione di modifiche in conflitto da parte di più amministratori di criteri di gruppi. Dopo aver modificato l'oggetto Criteri di controllo, è possibile archiviarlo nell'archivio in modo che possa essere esaminato e distribuito nell'ambiente di produzione.

Per completare questa procedura è necessario un account utente con il ruolo di amministratore dell'editor o Advanced Manager (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Modifica di un GPO offline


Per modificare un oggetto Criteri di controllo, Estrai l'oggetto Criteri di ricerca dall'archivio, modifica il GPO offline e quindi controlla l'oggetto Criteri di controllo nell'archivio in modo che possa essere esaminato e distribuito (o modificato da altri editor).

-   [Estrarre un oggetto Criteri di ricerca dall'archivio per la modifica](#bkmk-checkout)

-   [Modificare un GPO offline](#bkmk-edit)

-   [Controllare un GPO nell'archivio](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**Per estrarre un oggetto Criteri di ricerca dall'archivio per la modifica**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di modifica e quindi scegliere **Estrai**.

4.  Digitare un commento da visualizzare nella cronologia del GPO mentre è estratto e quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene ora identificato come **Estratto**.

### <a href="" id="bkmk-edit"></a>

**Per modificare un GPO offline**

1.  Nella scheda **controllato** fare clic con il pulsante destro del mouse sull'oggetto Criteri di modifica e quindi scegliere **modifica**.

2.  Nella finestra **Editor gestione criteri di gruppo** apportare modifiche a una copia offline del GPO.

    **Nota**  Per disabilitare tutte le impostazioni di configurazione del computer o tutte le impostazioni di configurazione degli utenti, **fare clic con**il pulsante destro del mouse sull'oggetto Criteri di gruppo nella finestra dell' **Editor gestione criteri** Selezionare **Disattiva impostazioni di configurazione del computer** o **Disattiva le impostazioni di configurazione degli utenti** in base alle esigenze.

     

3.  Dopo aver modificato l'oggetto Criteri di gruppo, chiudere la finestra dell' **Editor gestione criteri di raggruppamento** .

### <a href="" id="bkmk-checkin"></a>

**Per controllare un GPO nell'archivio**

1.  Nella scheda **controllati** :

    -   Se non sono state apportate modifiche al GPO, fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo e scegliere **Annulla estrazione**e quindi fare clic su **Sì** per confermare.

    -   Se sono state apportate modifiche al GPO, fare clic con il pulsante destro del mouse sull'oggetto Criteri di ricerca e scegliere **Archivia**.

2.  Digitare un commento da visualizzare nella traccia di controllo del GPO e quindi fare clic su **OK**.

3.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.

### Considerazioni aggiuntive

-   Per estrarre e modificare un oggetto Criteri di controllo, per impostazione predefinita è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di ricerca, un editor o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo). In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca. Per modificare l'oggetto Criteri di controllo, è inoltre necessario essere l'utente che ha estratto l'oggetto Criteri di stato.

-   Per archiviare un GPO per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo). In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca. Se non si è un approvatore o un amministratore della gestione avanzata Criteri di gruppo con l'autorizzazione **Distribuisci GPO** , è necessario essere l'editor che ha estratto il GPO.

-   Quando si modifica un oggetto Criteri di gruppo, qualsiasi aggiornamento dell'installazione del software di un pacchetto in un altro GPO deve fare riferimento al GPO distribuito e non alla copia Estratto.

### Riferimenti aggiuntivi

-   [Modifica di un oggetto Criteri di gruppo](editing-a-gpo-agpm30ops.md)

-   Revisione di un oggetto Criteri di stato

    -   [Esaminare le impostazioni dell'oggetto Criteri di gruppo](review-gpo-settings-agpm30ops.md)

    -   [Esaminare i collegamenti dell'oggetto Criteri di gruppo](review-gpo-links-agpm30ops.md)

    -   [Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)

-   Distribuzione di un GPO

    -   [Richiedere la distribuzione di un oggetto Criteri di gruppo](request-deployment-of-a-gpo-agpm30ops.md)

    -   [Distribuire un oggetto Criteri di gruppo](deploy-a-gpo-agpm30ops.md)

 

 





