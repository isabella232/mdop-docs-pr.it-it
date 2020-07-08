---
title: Importare un oggetto Criteri di gruppo da un file
description: Importare un oggetto Criteri di gruppo da un file
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820755"
---
# Importare un oggetto Criteri di gruppo da un file


In Advanced Group Policy Management, se si è un amministratore della gestione avanzata Criteri di gruppo (controllo completo) ed è stato esportato un oggetto Criteri di gruppo in un file CAB, è possibile importare le impostazioni dei criteri da tale GPO in un nuovo GPO o in un GPO esistente in un dominio in un'altra foresta. Per informazioni sull'esportazione di impostazioni GPO in un file CAB, vedere [esportare un oggetto Criteri di ricerca in un file](export-a-gpo-to-a-file.md).

È necessario un account utente con il ruolo di amministratore Advanced Group Policy Management o le autorizzazioni necessarie in Advanced Group Policy per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato. È necessario un account utente con l'editor o il ruolo di amministratore Advanced Group Policy Management o le autorizzazioni necessarie in Advanced Group Policy per importare le impostazioni dei criteri in un GPO esistente. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Importazione di impostazioni dei criteri da un file


Quando si importano le impostazioni dei criteri da un file, è possibile importarle in un nuovo GPO o in un GPO esistente. Tuttavia, se si importano le impostazioni dei criteri in un oggetto Criteri di stato esistente, tutte le impostazioni dei criteri all'interno vengono sostituite.

-   [Importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato](#bkmk-new)

-   [Importare le impostazioni dei criteri in un GPO esistente](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**Per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Creare un nuovo oggetto Criteri di controllo controllato. Nella finestra di dialogo **nuovo GPO controllato** fare clic su **Importa** e quindi su **Avvia procedura guidata**. Per altre informazioni su come creare un oggetto Criteri di ricerca, vedere [creare un nuovo oggetto Criteri di controllo controllato](create-a-new-controlled-gpo-agpm40.md).

4.  Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per il nuovo GPO e immettere un commento per l'audit trail del nuovo GPO.

### <a href="" id="bkmk-existing"></a>

**Per importare le impostazioni dei criteri in un GPO esistente**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nel dominio in cui si vogliono importare le impostazioni dei criteri.

2.  Nella scheda **contenuto** fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.

3.  Vedere il GPO di destinazione a cui si vogliono importare le impostazioni dei criteri.

4.  Fare clic con il pulsante destro del mouse sull'oggetto Criteri di destinazione, scegliere **Importa da**e quindi fare clic su **file**.

5.  Seguire le istruzioni della **procedura guidata Importa impostazioni** per selezionare un backup degli oggetti Criteri di stato, importare le impostazioni dei criteri per sostituirle nell'oggetto Criteri di ricerca e immettere un commento per la traccia di controllo dell'oggetto Criteri di stato di destinazione. Per impostazione predefinita, l'oggetto Criteri di stato di destinazione viene archiviato al termine della procedura guidata.

### Considerazioni aggiuntive

-   Per importare le impostazioni dei criteri in un nuovo oggetto Criteri di controllo controllato, è necessario avere il **contenuto dell'elenco**, **importare un GPO**e creare le autorizzazioni **GPO** per il dominio. Per impostazione predefinita, per eseguire questa procedura è necessario essere un amministratore della Advanced Group Policy Management.

-   Per importare le impostazioni dei criteri in un oggetto Criteri di stato esistente, è necessario avere il **contenuto dell'elenco**, **modificare le impostazioni**e importare le autorizzazioni **GPO** per il dominio e l'oggetto Criteri di controllo deve essere estratto dall'utente. Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo).

### Riferimenti aggiuntivi

-   [Gestione dell'archivio](managing-the-archive-agpm40.md)

 

 





