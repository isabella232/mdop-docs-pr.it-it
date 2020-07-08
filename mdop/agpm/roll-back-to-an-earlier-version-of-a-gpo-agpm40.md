---
title: Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo
description: Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 06ce9251-95e0-46d0-99c2-b9a0690e5891
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1146a8ecaf25796b9ac105ba46ea7f27b06fc8aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820275"
---
# Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo


Un responsabile approvazione può eseguire il rollback delle modifiche apportate a un oggetto Criteri di gruppo ridistribuendo una versione precedente del GPO dalla cronologia. La distribuzione di una versione precedente di un oggetto Criteri di controllo sovrascrive la versione del GPO attualmente in produzione.

Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per distribuire una versione precedente di un GPO nell'ambiente di produzione del dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare doppio clic sul GPO da distribuire per visualizzarne la **cronologia**.

4.  Fare clic con il pulsante destro del mouse sulla versione da distribuire, scegliere **Distribuisci**e quindi fare clic su **Sì**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Nella finestra **cronologia** fare clic su **Chiudi**.

**Nota**  Per verificare che la versione ridistribuita corrisponda alla versione progettata, esaminare un report di differenza per le due versioni. Nella finestra **cronologia** per l'oggetto Criteri di ricerca evidenziare le due versioni, quindi fare clic con il pulsante destro del mouse e scegliere **differenza** e report **HTML** o **report XML**.

 

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Attività del responsabile approvazione](performing-approver-tasks-agpm40.md)

 

 





