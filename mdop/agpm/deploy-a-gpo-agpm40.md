---
title: Distribuire un oggetto Criteri di gruppo
description: Distribuire un oggetto Criteri di gruppo
author: dansimp
ms.assetid: a6febeaa-144b-4c02-99af-d972f0f2b544
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 208fd95ec48f81b6c3a2a59bf92f53128eb3d529
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818705"
---
# Distribuire un oggetto Criteri di gruppo


Un responsabile approvazione può distribuire un oggetto Criteri di gruppo nuovo o modificato nell'ambiente di produzione. Per informazioni su come ridistribuire una versione precedente di un oggetto Criteri di controllo, vedere [eseguire il rollback a una versione precedente di un oggetto Criteri di](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)ricerca.

Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per distribuire un GPO nell'ambiente di produzione**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distribuzione e quindi scegliere **Distribuisci**.

4.  Per rivedere i collegamenti all'oggetto Criteri di controllo, fare clic su **Avanzate**. Posizionare il puntatore del mouse su un elemento nell'albero per visualizzare i dettagli.

    -   Per impostazione predefinita, tutti i collegamenti al GPO verranno ripristinati.

    -   Per impedire il ripristino di un collegamento, deselezionare la casella di controllo relativa al collegamento.

    -   Per impedire il ripristino di tutti i collegamenti, deselezionare la casella di controllo **Ripristina collegamenti** nella finestra di dialogo **Distribuisci GPO** .

5.  Fai clic su **Sì**. Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.

**Nota**  Per verificare se la versione più recente di un oggetto Criteri di controllo è stata distribuita, fare doppio clic sul GPO nella scheda **controllati** per visualizzarne la **cronologia**. Nella **cronologia** per il GPO la colonna **stato** indica se un oggetto Criteri di ricerca è stato distribuito.

 

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Attività del responsabile approvazione](performing-approver-tasks-agpm40.md)

 

 





