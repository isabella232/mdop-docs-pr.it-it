---
title: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
description: Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820315"
---
# Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato


A meno che non si sia un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo), è necessario richiedere la creazione di un nuovo oggetto Criteri di gruppo se deve essere gestito tramite Advanced Group Policy Management.

Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.

3.  A meno che non si disponga di autorizzazioni speciali per la creazione di GPO, è necessario inviare una richiesta di creazione. Nella finestra di dialogo **nuovo GPO controllato** :

    1.  Per ricevere una copia della richiesta, immettere l'indirizzo di posta elettronica nel campo **CC** .

    2.  Digitare un nome per il nuovo oggetto Criteri di ricerca.

    3.  Facoltativo: digitare un commento per il nuovo oggetto Criteri di ricerca.

    4.  Per distribuire il nuovo GPO nell'ambiente di produzione subito dopo l'approvazione, fare clic su **Crea Live**. Per creare il nuovo GPO offline senza distribuirlo immediatamente dopo l'approvazione, fare clic su **Crea offline**.

    5.  Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca.

    6.  Fai clic su **Invia**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore. In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.

-   Per ritirare la richiesta prima di approvarla, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà distrutto.

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-editor.md)

 

 





