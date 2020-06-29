---
title: Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato
description: Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818465"
---
# Richiedere il controllo di un oggetto Criteri di gruppo in precedenza non controllato


Per usare Gestione avanzata Criteri di gruppo per specificare il controllo delle modifiche per un oggetto Criteri di gruppo esistente, è necessario che il GPO sia controllato con Advanced Group Policy Management. A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere che venga controllato.

Per completare questa procedura è necessario un account utente con il ruolo di editor o revisore o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per controllare un oggetto Criteri di controllo non controllato in precedenza**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda non **controllata** per visualizzare gli oggetti Criteri di controllo incontrollati.

3.  Fare clic con il pulsante destro del mouse sul GPO da controllare con Advanced Group Policy Management e quindi scegliere **controllo**.

4.  A meno che non si disponga di autorizzazioni speciali per controllare gli oggetti Criteri di controllo, è necessario inviare una richiesta di controllo. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** . Digitare un commento da visualizzare nella **cronologia** del GPO e quindi fare clic su **Invia**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene rimosso dall'elenco nella scheda non **controllata** e aggiunto alla scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un revisore. In particolare, per il dominio è necessario disporre delle autorizzazioni per il **contenuto degli elenchi** e per le **impostazioni di lettura** .

-   Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà restituito alla scheda non **controllata** .

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-editor.md)

 

 





