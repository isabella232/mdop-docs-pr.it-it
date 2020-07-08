---
title: Richiedere la distribuzione di un oggetto Criteri di gruppo
description: Richiedere la distribuzione di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820385"
---
# Richiedere la distribuzione di un oggetto Criteri di gruppo


Dopo aver modificato e archiviato un oggetto Criteri di gruppo, distribuire il GPO, in modo che diventi effettivo nell'ambiente di produzione.

Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per richiedere la distribuzione di un GPO all'ambiente di produzione del dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distribuzione e quindi scegliere **Distribuisci**.

4.  A meno che non si sia un approvatore o un amministratore della Advanced Group Policy Management o si disponga di autorizzazioni speciali per distribuire GPO, è necessario inviare una richiesta di distribuzione. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** . Digitare un commento da visualizzare nella **cronologia** per il GPO e quindi fare clic su **Invia**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato dalla scheda **in sospeso** alla scheda **controllata** e sarà distribuito.

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un editor per eseguire questa procedura. In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca.

-   Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà restituito alla scheda **controllato** .

### Riferimenti aggiuntivi

-   [Attività dell'editor](performing-editor-tasks-agpm40.md)

 

 





