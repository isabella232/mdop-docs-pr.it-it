---
title: Richiedere il controllo di un oggetto Criteri di gruppo non controllato
description: Richiedere il controllo di un oggetto Criteri di gruppo non controllato
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818455"
---
# Richiedere il controllo di un oggetto Criteri di gruppo non controllato


Per specificare il controllo delle modifiche per un oggetto Criteri di gruppo (GPO) esistente, è necessario che il GPO sia controllato. A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere che venga controllato.

Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per controllare un oggetto Criteri di controllo non controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.

3.  Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.

4.  A meno che non si disponga di autorizzazioni speciali per controllare gli oggetti Criteri di controllo, è necessario inviare una richiesta di controllo. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** . Digitare un commento da visualizzare nella **cronologia** del GPO e quindi fare clic su **Invia**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene rimosso dall'elenco nella scheda non **controllata** e aggiunto alla scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore. In particolare, per il dominio è necessario disporre delle autorizzazioni per il **contenuto degli elenchi** e per le **impostazioni di lettura** .

-   Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà restituito alla scheda non **controllata** .

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





