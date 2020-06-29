---
title: Esaminare le impostazioni dell'oggetto Criteri di gruppo
description: Esaminare le impostazioni dell'oggetto Criteri di gruppo
author: dansimp
ms.assetid: c346bcde-dd6a-4775-aeab-721ca3a361b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 336118fb8d099fa5a373415320e7ca5ce8bde761
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820295"
---
# Esaminare le impostazioni dell'oggetto Criteri di gruppo


Puoi generare report basati su HTML e basato su XML per la revisione delle impostazioni in qualsiasi versione di un oggetto Criteri di gruppo.

Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per rivedere le impostazioni in qualsiasi versione di un GPO**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare gli oggetti Criteri di stato.

3.  Fare doppio clic sul GPO per visualizzarne la cronologia.

4.  Fare clic con il pulsante destro del mouse sulla versione del GPO per la quale rivedere le impostazioni, fare clic su **Impostazioni**e quindi su **report HTML** o **report XML** per visualizzare un riepilogo delle impostazioni del GPO.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO. Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.

### Riferimenti aggiuntivi

-   [Attività del revisore](performing-reviewer-tasks-agpm40.md)

 

 





