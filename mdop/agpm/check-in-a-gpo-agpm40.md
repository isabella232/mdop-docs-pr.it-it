---
title: Archiviare un oggetto Criteri di gruppo
description: Archiviare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: b838c8a2-eb9e-4e5b-8740-d7701a4294ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 27924e57e7430cdf992a7730e5cd141ed4fb52ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819185"
---
# Archiviare un oggetto Criteri di gruppo


In genere, gli editor devono eseguire il check-in oggetti Criteri di gruppo che sono stati modificati al termine delle modifiche. Per informazioni dettagliate, vedere [modificare un GPO offline](edit-a-gpo-offline-agpm40.md). Tuttavia, se l'editor non è disponibile, l'approvatore può anche archiviare un oggetto Criteri di ricerca.

Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per archiviare un oggetto Criteri di controllo Estratto da un editor**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

    -   Per ignorare le modifiche apportate dall'editor, fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo, scegliere **Annulla estrazione**e quindi fare clic su **Sì** per confermare.

    -   Per mantenere le modifiche apportate dall'editor, fare clic con il pulsante destro del mouse sull'oggetto Criteri di ricerca e quindi scegliere **Archivia**.

3.  Digitare un commento da visualizzare nella traccia di controllo del GPO e quindi fare clic su **OK**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Nella scheda **controllato** lo stato dell'oggetto Criteri di controllo viene identificato come **archiviato**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca. Se non si è un approvatore o un amministratore della gestione avanzata Criteri di gruppo con l'autorizzazione **Distribuisci GPO** , è necessario essere l'editor che ha estratto il GPO.

### Riferimenti aggiuntivi

-   [Attività del responsabile approvazione](performing-approver-tasks-agpm40.md)

-   [Modificare un oggetto Criteri di gruppo offline](edit-a-gpo-offline-agpm40.md)

 

 





