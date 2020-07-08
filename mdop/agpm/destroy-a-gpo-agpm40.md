---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 09bce8c4-f75b-4633-b80b-d894bbec95c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d93b95fceda99a5840705c33e8919d6d7414fe8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818655"
---
# Eliminare un oggetto Criteri di gruppo


I responsabili approvazione possono eliminare un oggetto Criteri di gruppo, rimuoverlo dal Cestino e eliminarlo definitivamente in modo che non possa più essere ripristinato.

Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per eliminare definitivamente un oggetto Criteri di stato in modo che non possa più essere ripristinato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di stato eliminati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distruzione e quindi scegliere **Elimina**.

4.  Fare clic su **Sì** per confermare che si vuole eliminare definitivamente l'oggetto Criteri di stato selezionato e tutti i backup dall'archivio.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. L'oggetto Criteri di stato viene rimosso dalla scheda **Cestino** e viene eliminato definitivamente.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





