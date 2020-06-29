---
title: Delegare l'accesso a livello di dominio
description: Delegare l'accesso a livello di dominio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820996"
---
# Delegare l'accesso a livello di dominio


Configurare la delega per l'ambiente in modo che gli amministratori dei criteri di gruppo abbiano l'accesso e il controllo appropriati degli oggetti Criteri di gruppo. È possibile applicare le autorizzazioni di previsione per rendere più efficienti le operazioni di gestione avanzata di criteri di gruppo. È possibile concedere le autorizzazioni in modo che soddisfi le esigenze dell'organizzazione.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per delegare l'accesso in modo che utenti e gruppi dispongano delle autorizzazioni appropriate per tutti i GPO in un dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic sulla scheda **delega del dominio** , quindi fare clic sul pulsante **Avanzate** .

3.  Nella finestra di dialogo **autorizzazioni** fare clic sulla casella di controllo relativa a ogni ruolo da assegnare a un singolo utente e quindi fare clic sul pulsante **Avanzate** .

    **Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.

     

4.  Nella finestra di dialogo **impostazioni di sicurezza avanzate** selezionare un amministratore di criteri di gruppo e quindi fare clic su **modifica**.

5.  Per **applica su**, selezionare **questo oggetto e gli oggetti annidati**, configurare le autorizzazioni speciali oltre ai ruoli di Advanced Group Policy Management, quindi fare clic su **OK** nella finestra di dialogo **immissione** delle **autorizzazioni** .

6.  Nella finestra di dialogo **impostazioni di sicurezza avanzate** fare clic su **OK**.

7.  Nella finestra di dialogo **autorizzazioni** fare clic su **OK**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.

-   Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** . In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management. Imposta l'autorizzazione da applicare a **questo oggetto e agli oggetti annidati**. Le altre autorizzazioni devono essere delegate in modo esplicito.

-   Agli editori deve essere concessa l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software Policy Group.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata in modo che non venga usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

 

 





