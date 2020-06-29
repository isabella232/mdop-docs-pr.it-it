---
title: Esaminare i collegamenti dell'oggetto Criteri di gruppo
description: Esaminare i collegamenti dell'oggetto Criteri di gruppo
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818346"
---
# Esaminare i collegamenti dell'oggetto Criteri di gruppo


È possibile visualizzare un diagramma che mostra dove un oggetto Criteri di gruppo o GPO selezionato è collegato alle unità organizzative. I diagrammi di collegamento GPO vengono aggiornati ogni volta che il GPO viene controllato, importato o archiviato.

Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Revisione dei collegamenti degli oggetti Criteri di stato


-   [Per uno o più GPO](#bkmk-gpos)

-   [Per una o più versioni di un oggetto Criteri di ricerca](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**Per visualizzare i collegamenti GPO per uno o più GPO**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllato**, **in sospeso**o **Cestino** per visualizzare i GPO.

3.  Selezionare uno o più GPO per cui visualizzare i collegamenti, fare clic con il pulsante destro del mouse su un oggetto Criteri di selezione selezionato, scegliere **Impostazioni**e quindi fare clic su **collegamenti GPO** per visualizzare un diagramma di domini e unità organizzative con collegamenti ai GPO selezionati.

### <a href="" id="bkmk-gpo-versions"></a>

**Per visualizzare i collegamenti GPO per una o più versioni di un oggetto Criteri di ricerca**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **Controlla** o **Cestino** per visualizzare gli oggetti Criteri di controllo.

3.  Fare doppio clic sul GPO per visualizzarne la cronologia.

4.  Fare clic con il pulsante destro del mouse sulla versione del GPO per la quale rivedere le impostazioni, fare clic su **Impostazioni**e quindi su **report HTML** o **report XML** per visualizzare un riepilogo delle impostazioni del GPO.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO. Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.

### Riferimenti aggiuntivi

-   [Attività del revisore](performing-reviewer-tasks-agpm40.md)

 

 





