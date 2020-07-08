---
title: Creare un nuovo oggetto Criteri di gruppo controllato
description: Creare un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: 5ce760f6-9f05-42b4-b787-7835ab8e324e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67c6af686b9ba7254cdaf93bd2d294b2d5bbb681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821096"
---
# Creare un nuovo oggetto Criteri di gruppo controllato


I nuovi oggetti Criteri di gruppo creati tramite la cartella del **controllo di modifica** verranno controllati automaticamente, consentendo di gestirli.

Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic con il pulsante destro del mouse su **Cambia controllo**e quindi scegliere **nuovo GPO controllato**.

3.  Nella finestra di dialogo **nuovo GPO controllato** :

    1.  Digitare un nome per il nuovo oggetto Criteri di ricerca.

    2.  Facoltativo: digitare un commento per il nuovo GPO da visualizzare nella **cronologia** per l'oggetto Criteri di ricerca.

    3.  Per distribuire immediatamente il nuovo GPO nell'ambiente di produzione del dominio, fare clic su **Crea Live**. Per creare il nuovo GPO offline senza immediatamente distribuirlo, fare clic su **Crea offline**.

    4.  Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca e quindi fare clic su **OK**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni **GPO** per il dominio.

### Riferimenti aggiuntivi

-   [Creazione o controllo di un oggetto Criteri di gruppo](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





