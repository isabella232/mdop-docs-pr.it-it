---
title: Richiedere il ripristino di un oggetto Criteri di gruppo eliminato
description: Richiedere il ripristino di un oggetto Criteri di gruppo eliminato
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820366"
---
# Richiedere il ripristino di un oggetto Criteri di gruppo eliminato


A meno che non si sia un approvatore o un amministratore Advanced Group Policy Management (controllo completo), è necessario richiedere il ripristino di un oggetto Criteri di gruppo eliminato dal Cestino per restituirlo all'archivio.

Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per richiedere il ripristino di un oggetto Criteri di stato eliminato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di stato eliminati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto che si vuole ripristinare e quindi scegliere **Ripristina**.

4.  A meno che non si disponga di autorizzazioni speciali per il ripristino di GPO, è necessario inviare una richiesta di ripristino dell'oggetto Criteri di ricerca eliminato. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** . Digitare un commento da visualizzare in audit trail per il GPO e quindi fare clic su **Invia**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. L'oggetto Criteri di controllo viene rimosso dalla scheda **Cestino** e viene visualizzato nella scheda **controllati** .

**Nota**  Se un oggetto Criteri di stato è stato eliminato dall'ambiente di produzione, il suo ripristino nell'archivio non verrà ridistribuito automaticamente nell'ambiente di produzione. Per restituire il GPO all'ambiente di produzione, distribuire il GPO. Per informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca.

 

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un editor per eseguire questa procedura. In particolare, è necessario avere il **contenuto dell'elenco** e le autorizzazioni di **modifica delle impostazioni** per il GPO.

-   Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**. Il GPO verrà restituito nella scheda **Cestino** .

### Riferimenti aggiuntivi

-   [Eliminazione, ripristino o distruzione di un oggetto Criteri di gruppo](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





