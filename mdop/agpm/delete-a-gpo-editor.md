---
title: Eliminare un oggetto Criteri di gruppo
description: Eliminare un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820975"
---
# Eliminare un oggetto Criteri di gruppo


Come editor, potresti non avere l'autorizzazione per completare l'eliminazione di un oggetto Criteri di gruppo, ma hai le autorizzazioni necessarie per avviare il processo e inviare la richiesta a un responsabile dell'approvazione.

Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per richiedere l'eliminazione di un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sul GPO da eliminare e quindi scegliere **Elimina**.

    -   Per eliminare il GPO dall'archivio lasciando invariata la versione distribuita del GPO nell'ambiente di produzione, fare clic su **Elimina GPO solo dall'archivio (Annulla controllo)**.

    -   Per eliminare il GPO dall'ambiente di archiviazione e produzione, fare clic su **Elimina GPO dall'archivio e dalla produzione**.

        A meno che non si disponga di autorizzazioni speciali per eliminare gli oggetti Criteri di ricerca, è necessario inviare una richiesta per l'eliminazione del GPO distribuito. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** . Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **Invia**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato dalla scheda **in sospeso** alla scheda **Cestino** , in cui può essere ripristinato o distrutto.

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un editor per richiedere l'eliminazione di un GPO distribuito. In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca.

-   Per impostazione predefinita, è necessario essere un editor, un approvatore o un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per eliminare un oggetto Criteri di stato dall'archivio. In particolare, è necessario avere **contenuto elenco** e **modificare le impostazioni** o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

-   Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà restituito alla scheda **controllato** .

-   Per eliminare un oggetto Criteri di gruppo non controllato dall'ambiente di produzione senza prima controllarlo, fare clic su **foresta**in **console Management Policy di Group**, fare clic su **domini**, fare clic su ** &lt; dominio &gt; **e quindi su **oggetti Criteri di gruppo**. Fare clic con il pulsante destro del mouse sull'oggetto Criteri di controllo non controllato e quindi scegliere **Elimina**.

### Riferimenti aggiuntivi

-   [Attività dell'editor](performing-editor-tasks.md)

 

 





