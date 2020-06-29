---
title: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
description: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
author: dansimp
ms.assetid: 071270fa-1890-40ce-ab89-ce070a54aa59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6974edc08805b56a7a69925f4c10233720488314
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820695"
---
# Importare un oggetto Criteri di gruppo dall'ambiente di produzione


Se vengono apportate modifiche a un oggetto Criteri di gruppo (GPO) controllato all'esterno della gestione avanzata Criteri di gruppo, è possibile importare una copia del GPO dall'ambiente di produzione e salvarla nell'archivio per avvicinare l'archivio e l'ambiente di produzione a uno stato coerente. Per importare un oggetto Criteri di controllo non controllato, controlla l'oggetto Criteri di controllo. Vedere [controllare un GPO in precedenza non controllato](control-a-previously-uncontrolled-gpo.md).

Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per importare un GPO dall'ambiente di produzione**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di scelta e quindi scegliere **Importa dalla produzione**.

4.  Digitare un commento per l'audit trail dell'oggetto Criteri di controllo e quindi fare clic su **OK**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un responsabile dell'approvazione o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e **modificare le impostazioni**, **distribuire GPO**o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-approver.md)

 

 





