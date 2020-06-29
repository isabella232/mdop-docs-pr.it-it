---
title: Eliminare un oggetto Criteri di gruppo controllato
description: Eliminare un oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818715"
---
# Eliminare un oggetto Criteri di gruppo controllato


I responsabili approvazione possono eliminare un oggetto Criteri di gruppo controllato, spostandolo nel Cestino.

Per completare questa procedura è necessario un account utente con l'approvatore o l'amministratore della gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management per il completamento. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per eliminare un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto che si vuole eliminare e quindi scegliere **Elimina**.

    -   Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio**.

    -   Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.

4.  Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto. Se l'oggetto Criteri di stato è stato eliminato solo dall'archivio, viene visualizzato anche nella scheda non **controllata** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

-   Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su ** &lt; dominio &gt; **e quindi su **oggetti Criteri di gruppo**. Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.

### Riferimenti aggiuntivi

-   [Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





