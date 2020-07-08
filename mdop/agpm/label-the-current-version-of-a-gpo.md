---
title: Etichettare la versione corrente di un oggetto Criteri di gruppo
description: Etichettare la versione corrente di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 5e4e50f8-e4a8-4bda-aac4-1569d5fbd6a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a34232dfd1f7a755dd81cdecbe3d5d1957f01294
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820626"
---
# Etichettare la versione corrente di un oggetto Criteri di gruppo


Puoi assegnare un'etichetta alla versione corrente di un oggetto Criteri di gruppo per facilitare l'identificazione nella cronologia. Puoi usare un'etichetta per identificare una versione valida nota a cui puoi eseguire il rollback se si verifica un problema. Inoltre, contrassegnando più oggetti Criteri di gruppo con la stessa etichetta contemporaneamente, è possibile contrassegnare gli oggetti Criteri di gruppo correlati che devono essere ripristinati nello stesso punto se il rollback deve essere necessario in un secondo momento.

Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per assegnare un'etichetta alla versione corrente di GPO nelle relative cronologie**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic su un GPO per cui assegnare un'etichetta alla versione corrente. Per selezionare più GPO, premere MAIUSC e fare clic sull'ultimo GPO in un gruppo di GPO contiguo oppure premere CTRL e fare clic su singoli GPO. Fare clic con il pulsante destro del mouse su un GPO selezionato e quindi scegliere **etichetta**.

4.  Digitare un'etichetta e un commento da visualizzare nella cronologia di ogni GPO selezionato e quindi fare clic su **OK**.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il contenuto di un **elenco** e **modificare le impostazioni** o distribuire le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Modifica di un oggetto Criteri di gruppo](editing-a-gpo.md)

 

 





