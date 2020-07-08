---
title: Delegare l'accesso a un oggetto Criteri di gruppo
description: Delegare l'accesso a un oggetto Criteri di gruppo
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818785"
---
# Delegare l'accesso a un oggetto Criteri di gruppo


Un responsabile approvazione può delegare la gestione di un oggetto Criteri di gruppo controllato **creato dall'approvatore**. Come un amministratore Advanced Group Policy Management (controllo completo), l'approvatore può delegare l'accesso a un oggetto Criteri di questo tipo, quindi gli editor selezionati possono modificarlo, i revisori possono rivederlo e altri responsabili approvazione possono approvarlo. Per impostazione predefinita, un responsabile approvazione non può delegare l'accesso ai GPO creati da un altro amministratore di criteri di gruppo.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di gruppi di criteri avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per delegare la gestione di un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare.

3.  Fare clic sul pulsante **Aggiungi** , selezionare gli utenti o i gruppi a cui consentire l'accesso e quindi fare clic su **OK**.

4.  Per personalizzare le autorizzazioni per ogni, fare clic sul pulsante **Avanzate** nella scheda **Sommario** e selezionare autorizzazioni ruolo per consentire o negare. Per un controllo più dettagliato, fare clic su **Avanzate** nella finestra di dialogo **autorizzazioni** .

5.  Fare clic su **applica**e quindi su **OK** nella finestra di dialogo **autorizzazioni** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.

### Riferimenti aggiuntivi

-   [Creazione, controllo o importazione di un oggetto Criteri di gruppo](creating-controlling-or-importing-a-gpo-approver.md)

 

 





