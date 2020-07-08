---
title: Creare un modello
description: Creare un modello
author: dansimp
ms.assetid: 8208f14a-5c18-43a7-8564-118230398cca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f6713cd0fadb651e1de028bbcf2ae3ec1dd067c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821085"
---
# Creare un modello


La creazione di un modello consente di salvare tutte le impostazioni di una specifica versione di un oggetto Criteri di gruppo da usare come punto di partenza per la creazione di nuovi GPO.

**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.

 

Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per creare un modello basato su un oggetto Criteri di lavoro esistente**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato** o **non** controllata per visualizzare i GPO disponibili.

3.  Fare clic con il pulsante destro del mouse sul GPO da cui si vuole creare un modello e quindi scegliere **Salva come modello**.

4.  Digitare un nome per il modello e un commento e quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il nuovo modello viene visualizzato nella scheda **modelli** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni di **modello** per il dominio.

-   La ridenominazione o l'eliminazione di un modello non ha effetti sugli oggetti Criteri di creazione creati da tale modello.

-   Poiché non può essere modificato, un modello non ha una cronologia.

### Riferimenti aggiuntivi

-   [Creazione di un modello e impostazione di un modello predefinito](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 





