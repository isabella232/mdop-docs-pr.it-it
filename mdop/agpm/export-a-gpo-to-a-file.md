---
title: Esportare un oggetto Criteri di gruppo in un file
description: Esportare un oggetto Criteri di gruppo in un file
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820855"
---
# Esportare un oggetto Criteri di gruppo in un file


È possibile esportare un oggetto Criteri di gruppo (GPO) controllato in un file CAB in modo da poterlo copiare in un dominio in un'altra foresta e importare il GPO in Advanced Group Policy Management in tale dominio. Per informazioni su come importare le impostazioni GPO in un GPO nuovo o esistente, vedere [importare un oggetto Criteri di ricerca da un file](import-a-gpo-from-a-file-ed.md).

Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo.Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per esportare un oggetto Criteri di un file**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di scelta e quindi scegliere **Esporta in**.

4.  Immettere un nome file per il file a cui si vuole esportare l'oggetto Criteri di ricerca e quindi fare clic su **Esporta**. Se il file non esiste, viene creato. Se esiste già, viene sostituito.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco**, **le impostazioni di lettura**ed esportare le autorizzazioni **GPO** per l'oggetto Criteri di ricerca.

### Riferimenti aggiuntivi

-   [Uso di un ambiente di test](using-a-test-environment.md)

 

 





