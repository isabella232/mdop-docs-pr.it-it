---
title: Delegare l'accesso a un singolo oggetto Criteri di gruppo
description: Delegare l'accesso a un singolo oggetto Criteri di gruppo
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818735"
---
# Delegare l'accesso a un singolo oggetto Criteri di gruppo


In qualità di amministratore Advanced Group Policy Management (controllo completo), puoi delegare la gestione di un oggetto Criteri di gruppo controllato, quindi i gruppi e gli editori selezionati possono modificarlo, i revisori possono rivederlo e i responsabili approvazione possono approvarlo.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo o un account utente con le autorizzazioni necessarie per la gestione di gruppi di criteri avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per delegare la gestione di un oggetto Criteri di controllo controllato**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare i GPO controllati e quindi fare clic sul GPO per delegare.

3.  Fare clic sul pulsante **Aggiungi** , selezionare gli utenti o i gruppi a cui consentire l'accesso e quindi fare clic su **OK**.

4.  Per personalizzare le autorizzazioni per ogni utente o gruppo, fare clic sul pulsante **Avanzate** nella scheda **Sommario** e selezionare autorizzazioni ruolo per consentire o negare. Per un controllo più dettagliato, fare clic su **Avanzate** nella finestra di dialogo **autorizzazioni** .

5.  Fare clic su **applica**e quindi su **OK** nella finestra di dialogo **autorizzazioni** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere l'approvatore che ha creato o controllato l'oggetto Criteri di stato o un amministratore Advanced Group Policy Management (controllo completo). In particolare, devi avere l'autorizzazione **Sommario** per il dominio e **modificare** le autorizzazioni di sicurezza per il GPO.

-   Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** . In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management. Imposta l'autorizzazione da applicare a **questo oggetto e agli oggetti annidati**. Le altre autorizzazioni devono essere delegate in modo esplicito.

-   Gli editor devono avere l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software criteri di Group.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

 

 





