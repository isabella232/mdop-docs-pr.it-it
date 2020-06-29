---
title: Configurare una connessione al server di Gestione avanzata Criteri di gruppo
description: Configurare una connessione al server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 409cbbcf-3b0e-459d-9bd2-75cb7b9430b0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7fdc26045b478da14957cdfe6000d58ab72a064
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819085"
---
# Configurare una connessione al server di Gestione avanzata Criteri di gruppo


Per assicurarsi di essere connessi all'archivio centrale corretto, esaminare la configurazione della connessione al server Advanced Group Policy Management. Se un amministratore Advanced Group Policy Management (controllo completo) non ha configurato una connessione al server Advanced Group Policy Management, è necessario configurarlo manualmente.

**Per selezionare un server Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** :

    -   Se le opzioni della scheda **server Advanced Group Policy Management** non sono disponibili, sono state configurate centralmente da un amministratore della Advanced Group Policy Management.

    -   Se sono disponibili le opzioni della scheda **server Advanced Group Policy** Management, digitare il nome completo del computer per il server Advanced Group Policy Management (ad esempio, server.contoso.com) e la porta in cui è in ascolto il servizio Advanced Group Policy Management (per impostazione predefinita, la porta 4600). Fare clic su **applica**e quindi su **Sì** per confermare.

### Considerazioni aggiuntive

-   I server Advanced Group Policy Management selezionati determinano gli oggetti Criteri di visualizzazione nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni della scheda **delega del dominio** . Se non è gestito centralmente tramite il modello amministrativo, ogni amministratore dei criteri di gruppo deve configurare questa impostazione in modo che punti al server Advanced Group Policy Management per il dominio.

### Riferimenti aggiuntivi

-   [Attività del revisore](performing-reviewer-tasks-agpm40.md)

 

 





