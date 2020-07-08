---
title: Rinominare un oggetto Criteri di gruppo o un modello
description: Rinominare un oggetto Criteri di gruppo o un modello
author: dansimp
ms.assetid: 64a1aaf4-f672-48b5-94c6-473bf1076cf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 495fc090487ff324bc19c89dcd36ecf0efbcb151
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818495"
---
# Rinominare un oggetto Criteri di gruppo o un modello


È possibile rinominare un oggetto Criteri di gruppo (GPO) controllato o un modello.

Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di criteri di raggruppamento avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per rinominare un GPO o un modello**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controlli** o **modelli** per visualizzare l'elemento da rinominare.

3.  Fare clic con il pulsante destro del mouse sull'oggetto o sul modello da rinominare e scegliere **Rinomina**.

4.  Digitare il nuovo nome per il GPO o il modello e un commento, quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. L'oggetto Criteri di gruppo o il modello viene visualizzato sotto il nuovo nome nella scheda **contenuto** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato, un editor o un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, è necessario avere il **contenuto dell'elenco** e le autorizzazioni di **modifica delle impostazioni** per il GPO.

-   Quando si rinomina un oggetto Criteri di distribuzione distribuito, il nome viene immediatamente modificato nell'archivio. Il nome viene modificato nell'ambiente di produzione solo quando il GPO viene ridistribuito.

    Finché il GPO non viene ridistribuito o la copia di produzione viene eliminata, il vecchio nome è ancora in uso nell'ambiente di produzione e quindi non può essere usato per un altro GPO. Analogamente, l'oggetto Criteri di stato nell'archivio non può essere rinominato nel nome originale finché l'oggetto Criteri di stato non è stato distribuito (modificando il nome della copia di produzione) o se la copia di produzione è stata eliminata.

### Riferimenti aggiuntivi

-   [Modifica di un oggetto Criteri di gruppo](editing-a-gpo.md)

 

 





