---
title: Importare un oggetto Criteri di gruppo da un file
description: Importare un oggetto Criteri di gruppo da un file
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820725"
---
# Importare un oggetto Criteri di gruppo da un file


In Advanced Group Policy Management, se è stato esportato un oggetto Criteri di gruppo (GPO) in un file CAB, è possibile importare le impostazioni dei criteri da tale oggetto Criteri di gruppo in un GPO esistente in un dominio in un'altra foresta. L'importazione delle impostazioni dei criteri in un GPO esistente sostituisce tutte le impostazioni dei criteri all'interno di tale oggetto. Per informazioni sull'esportazione di impostazioni GPO in un file CAB, vedere [esportare un oggetto Criteri di ricerca in un file](export-a-gpo-to-a-file.md).

Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo.Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## <a href="" id="bkmk-existing"></a>


**Per importare le impostazioni dei criteri in un GPO esistente**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Vedere il GPO di destinazione a cui si vogliono importare le impostazioni dei criteri.

4.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di destinazione, scegliere **Importa da**e quindi fare clic su **file**.

5.  Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per sostituirle nell'oggetto Criteri di ricerca e immettere un commento per la traccia di controllo dell'oggetto Criteri di stato di destinazione. Per impostazione predefinita, l'oggetto Criteri di stato di destinazione viene archiviato al termine della procedura guidata.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco**, **modificare le impostazioni**e importare le autorizzazioni **GPO** per il dominio e il GPO deve essere estratto dall'utente.

-   Anche se un editor non può importare le impostazioni dei criteri in un nuovo oggetto Criteri di ricerca durante la creazione, un editor può richiedere la creazione di un nuovo oggetto Criteri di ricerca e quindi importarvi le impostazioni del criterio al termine della sua realizzazione.

### Riferimenti aggiuntivi

-   [Uso di un ambiente di test](using-a-test-environment.md)

 

 





