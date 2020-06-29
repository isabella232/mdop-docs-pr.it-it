---
title: Approvare o rifiutare un'azione in sospeso
description: Approvare o rifiutare un'azione in sospeso
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819216"
---
# Approvare o rifiutare un'azione in sospeso


La responsabilità principale di un responsabile approvazione consiste nel valutare e quindi approvare o rifiutare le richieste per la creazione, la distribuzione e l'eliminazione di oggetti Criteri di gruppo da parte di editori o revisori che non dispongono delle autorizzazioni necessarie per completare tali azioni. Le funzionalità del report avanzate per la gestione dei criteri di gruppo possono aiutare un responsabile dell'approvazione a valutare una nuova versione di un GPO.

Per completare questa procedura è necessario un account utente con il ruolo di approvatore o amministratore Advanced Group Policy (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per approvare o rifiutare una richiesta in sospeso**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** fare clic sulla scheda **in sospeso** per visualizzare gli oggetti Criteri di stato in sospeso.

3.  Fare clic con il pulsante destro del mouse su un GPO in sospeso e quindi scegliere **approva** o **rifiuta**.

4.  Se si approva la distribuzione, fare clic su **Avanzate** nella finestra di dialogo **Approva operazione in sospeso** per rivedere i collegamenti al GPO. Posizionare il puntatore del mouse su un nodo nell'albero per visualizzare i dettagli.

    -   Per impostazione predefinita, tutti i collegamenti al GPO verranno ripristinati.

    -   Per impedire il ripristino di un collegamento, deselezionare la casella di controllo relativa al collegamento.

    -   Per impedire il ripristino di tutti i collegamenti, deselezionare la casella di controllo **Ripristina collegamenti** nella finestra di dialogo **Distribuisci GPO** .

5.  Fare clic su **Sì** o **OK** per confermare l'approvazione o il rifiuto dell'azione in sospeso. Se è stata approvata la richiesta, il GPO viene spostato nella scheda appropriata per l'azione eseguita.

    **Nota**  Se l'indirizzo di posta elettronica di un responsabile dell'approvazione è incluso nel campo **a** della scheda **delega** del **dominio** , l'approvatore riceverà la posta elettronica dall'alias Advanced Policy Management quando un editor o un revisore invia una richiesta.

     

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, è necessario disporre delle autorizzazioni necessarie per eseguire la richiesta che si sta approvando.

### Riferimenti aggiuntivi

-   [Attività del responsabile approvazione](performing-approver-tasks.md)

 

 





