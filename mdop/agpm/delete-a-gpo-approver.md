---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820985"
---
# Eliminare un oggetto Criteri di gruppo


Advanced Group Policy Management consente agli approvatori di eliminare un oggetto Criteri di gruppo controllato, spostandolo nel Cestino.

Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per eliminare un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sul GPO da eliminare e quindi scegliere **Elimina**.

    -   Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio (Annulla controllo)**.

    -   Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.

4.  Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene rimosso dalla scheda **controllato** e viene visualizzato nella scheda **Cestino** , in cui può essere ripristinato o distrutto. Se l'oggetto Criteri di stato è stato eliminato solo dall'archivio, viene visualizzato anche nella scheda non **controllata** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un GPO distribuito. In particolare, devi avere il **contenuto dell'elenco** ed eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

-   Per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un oggetto Criteri di stato dall'archivio. In particolare, è necessario avere **contenuto elenco** e **modificare le impostazioni** o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

-   Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su ** &lt; dominio &gt; **e quindi su **oggetti Criteri di gruppo**. Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.

### Riferimenti aggiuntivi

-   [Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo](deleting-restoring-or-destroying-a-gpo.md)

 

 





