---
title: Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo
description: Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820285"
---
# Eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo


Advanced Group Policy Management consente a un approvatore di ripristinare le modifiche apportate a un oggetto Criteri di gruppo ridistribuendo una versione precedente dell'oggetto Criteri di gruppo dalla cronologia. La distribuzione di una versione precedente di un oggetto Criteri di controllo sovrascrive la versione del GPO attualmente in produzione.

Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per distribuire una versione precedente di un GPO nell'ambiente di produzione**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare doppio clic sul GPO da distribuire per visualizzarne la **cronologia**.

4.  Fare clic con il pulsante destro del mouse sulla versione da distribuire, scegliere **Distribuisci**e quindi fare clic su **Sì**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Nella finestra **cronologia** fare clic su **Chiudi**.

**Nota**  Per verificare che la versione ridistribuita corrisponda alla versione progettata, esaminare un report di differenza per le due versioni. Nella finestra **cronologia** per l'oggetto Criteri di ricerca evidenziare le due versioni, quindi fare clic con il pulsante destro del mouse e scegliere **differenza** e report **HTML** o **report XML**.

 

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Attività del responsabile approvazione](performing-approver-tasks.md)

 

 





