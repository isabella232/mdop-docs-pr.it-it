---
title: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
description: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820316"
---
# Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato


A meno che non si sia un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo), è necessario richiedere la creazione di un nuovo oggetto Criteri di gruppo.

Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic con il pulsante destro del mouse su **Cambia controllo**e quindi scegliere **nuovo GPO controllato**.

3.  A meno che non si disponga di autorizzazioni speciali per la creazione di GPO, è necessario inviare una richiesta di creazione. Nella finestra di dialogo **nuovo GPO controllato** :

    1.  Per ricevere una copia della richiesta, immettere l'indirizzo di posta elettronica nel campo **CC** .

    2.  Digitare un nome per il nuovo oggetto Criteri di ricerca.

    3.  Facoltativo: digitare un commento per il nuovo oggetto Criteri di ricerca.

    4.  Per distribuire il nuovo GPO nell'ambiente di produzione del dominio subito dopo l'approvazione, fare clic su **Crea Live**. Per creare il nuovo GPO offline senza distribuirlo immediatamente dopo l'approvazione, fare clic su **Crea offline**.

    5.  Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca.

    6.  Fai clic su **Invia**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore. In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.

-   Per ritirare la richiesta prima di approvarla, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà distrutto.

### Riferimenti aggiuntivi

-   [Creazione o controllo di un oggetto Criteri di gruppo](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





