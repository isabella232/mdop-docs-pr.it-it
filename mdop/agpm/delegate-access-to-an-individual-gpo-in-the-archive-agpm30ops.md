---
title: Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio
description: Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818766"
---
# Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio


In qualità di amministratore Advanced Group Policy Management (controllo completo), puoi delegare la gestione di un oggetto Criteri di gruppo controllato nell'archivio in modo che i gruppi e gli editori selezionati possano modificarlo, i revisori possono rivederlo e i responsabili approvazione possono approvarlo.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per delegare la gestione di un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare:

    1.  Per aggiungere l'accesso per un utente o un gruppo, fare clic sul pulsante **Aggiungi** , selezionare l'utente o il gruppo e fare clic su **OK**. Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare un ruolo e fare clic su **OK**.

    2.  Per rimuovere l'accesso per un utente o un gruppo, selezionare l'utente o il gruppo e fare clic sul pulsante **Rimuovi** .

        **Nota**  Se un utente o un gruppo eredita l'accesso a livello di dominio, il pulsante **Rimuovi** non è disponibile. È possibile modificare l'accesso a livello di dominio nella scheda **delega del dominio** .

         

    3.  Per modificare i ruoli e le autorizzazioni delegati a un utente o un gruppo, fare clic sul pulsante **Avanzate** . Nella finestra di dialogo **autorizzazioni** selezionare l'utente o il gruppo, selezionare la casella di controllo relativa a ogni ruolo da assegnare all'utente o al gruppo, quindi fare clic su **OK**.

        **Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.

         

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.

-   Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** . In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management. Le altre autorizzazioni devono essere delegate in modo esplicito.

-   Gli editor devono avere l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software criteri di Group.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Gestione dell'archivio](managing-the-archive.md)

 

 





