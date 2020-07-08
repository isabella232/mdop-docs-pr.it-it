---
title: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
description: Importare un oggetto Criteri di gruppo dall'ambiente di produzione
author: dansimp
ms.assetid: c5b2f40d-1dc7-4dbf-b8b3-4d97ad73e1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea01341e13696f8b06f22e3f352034b60a713f8a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820706"
---
# Importare un oggetto Criteri di gruppo dall'ambiente di produzione


Se vengono apportate modifiche a un oggetto Criteri di gruppo (GPO) controllato all'esterno della gestione avanzata Criteri di gruppo, è possibile importare una copia del GPO dall'ambiente di produzione del dominio e salvarla nell'archivio per avvicinare l'archivio e l'ambiente di produzione a uno stato coerente. Per importare un oggetto Criteri di controllo non controllato, controlla l'oggetto Criteri di controllo. Vedere [controllare un oggetto Criteri di](control-an-uncontrolled-gpo-agpm40.md)controllo non controllato.

Per completare questa procedura è necessario un account utente con l'editor, l'approvatore o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie inAGPM. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per importare un GPO dall'ambiente di produzione del dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di scelta e quindi scegliere **Importa dalla produzione**.

4.  Digitare un commento per l'audit trail dell'oggetto Criteri di controllo e quindi fare clic su **OK**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor, un responsabile dell'approvazione o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e **modificare le impostazioni**, **distribuire GPO**o eliminare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Creazione o controllo di un oggetto Criteri di gruppo](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





