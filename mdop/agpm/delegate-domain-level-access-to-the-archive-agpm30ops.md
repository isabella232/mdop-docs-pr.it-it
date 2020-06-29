---
title: Delegare l'accesso a livello di dominio all'archivio
description: Delegare l'accesso a livello di dominio all'archivio
author: dansimp
ms.assetid: d232069e-71d5-4b4d-b22e-bef11de1cfd4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01fbc4964493da6ba40382ac40671922eeffa30e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821006"
---
# Delegare l'accesso a livello di dominio all'archivio


Configurare la delega per l'ambiente in modo che gli amministratori dei criteri di gruppo abbiano l'accesso e il controllo appropriati degli oggetti Criteri di gruppo nell'archivio. Per rendere più efficiente l'operazione, è possibile applicare le autorizzazioni di previsione. È possibile concedere le autorizzazioni in modo che soddisfi le esigenze dell'organizzazione.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per delegare l'accesso in modo che gli utenti e i gruppi dispongano delle autorizzazioni appropriate per tutti i GPO in un dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic sulla scheda **delega dominio** e configurare l'accesso a tutti i GPO nel dominio:

    1.  Per aggiungere l'accesso per un utente o un gruppo, fare clic sul pulsante **Aggiungi** , selezionare l'utente o il gruppo e fare clic su **OK**. Nella finestra di dialogo **Aggiungi gruppo o utente** selezionare un ruolo e fare clic su **OK**.

    2.  Per rimuovere l'accesso per un utente o un gruppo, selezionare l'utente o il gruppo e fare clic sul pulsante **Rimuovi** .

    3.  Per modificare i ruoli e le autorizzazioni delegati a un utente o un gruppo, selezionare fare clic sul pulsante **Avanzate** . Nella finestra di dialogo **autorizzazioni** selezionare l'utente o il gruppo, selezionare la casella di controllo relativa a ogni ruolo da assegnare all'utente o al gruppo e quindi fare clic su **OK**.

        **Nota**  L'editor e l'approvatore includono le autorizzazioni del revisore.

         

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.

-   Per delegare l'accesso in lettura agli amministratori dei criteri di gruppo che usano Advanced Group Policy Management, è necessario concedere il **contenuto dell'elenco** e le autorizzazioni di **lettura delle impostazioni** . In questo modo è possibile visualizzare gli oggetti Criteri di dialogo nella scheda **contenuto** di Advanced Group Policy Management. Le altre autorizzazioni devono essere delegate in modo esplicito.

-   Agli editori deve essere concessa l'autorizzazione di **lettura** per la copia distribuita di un oggetto Criteri di gruppo per utilizzare in modo completo l'installazione del software Policy Group.

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Gestione dell'archivio](managing-the-archive.md)

 

 





