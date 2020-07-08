---
title: Creare un nuovo oggetto Criteri di gruppo controllato
description: Creare un nuovo oggetto Criteri di gruppo controllato
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821095"
---
# Creare un nuovo oggetto Criteri di gruppo controllato


I nuovi oggetti Criteri di gruppo creati tramite il nodo **Change Control** verranno controllati automaticamente, consentendo di gestirli con Advanced Group Policy Management (Advanced Policy Manager).

Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic con il pulsante destro del mouse sul nodo **Cambia controllo** e quindi scegliere **nuovo GPO controllato**.

3.  Nella finestra di dialogo **nuovo GPO controllato** :

    1.  Digitare un nome per il nuovo oggetto Criteri di ricerca.

    2.  Facoltativo: digitare un commento per il nuovo GPO da visualizzare nella **cronologia** per l'oggetto Criteri di ricerca.

    3.  Per distribuire immediatamente il nuovo GPO nell'ambiente di produzione, fare clic su **Crea Live**. Per creare il nuovo GPO offline senza immediatamente distribuirlo, fare clic su **Crea offline**.

    4.  Selezionare il modello di GPO da usare come punto di partenza per il nuovo oggetto Criteri di ricerca.

    5.  Fai clic su **OK**.

4.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il nuovo GPO viene visualizzato nell'elenco dei GPO nella scheda **controllato** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni **GPO** per il dominio.

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-approver.md)

 

 





