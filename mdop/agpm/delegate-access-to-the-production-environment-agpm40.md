---
title: Delegare l'accesso all'ambiente di produzione
description: Delegare l'accesso all'ambiente di produzione
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818726"
---
# Delegare l'accesso all'ambiente di produzione


In Advanced Group Policy Management, è possibile modificare l'accesso agli oggetti Criteri di gruppo nell'ambiente di produzione del dominio, sostituendo eventuali autorizzazioni esistenti per tali oggetti Criteri di gruppo. È possibile configurare le autorizzazioni a livello di dominio per consentire o impedire agli utenti di modificare, eliminare o modificare la sicurezza degli oggetti Criteri di gruppo nell'ambiente di produzione quando non usano la cartella di **controllo delle modifiche** nella console di gestione dei criteri di raggruppamento.

**Nota**  
-   La modifica del modo in cui l'accesso all'ambiente di produzione viene delegata non influisce sulla possibilità degli utenti di collegare GPO.

-   Quando gli oggetti Criteri di controllo vengono controllati o distribuiti, è possibile accedere ad altri account, ad eccezione di quelli con autorizzazioni di **lettura** e **applicazione** .

 

Per completare questa procedura è necessario un account utente con il ruolo di amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in gestione avanzata Criteri di gruppo. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per cambiare l'accesso a GPO nell'ambiente di produzione del dominio**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Fare clic sulla scheda **Delega produzione** .

3.  Per aggiungere le autorizzazioni per un utente o un gruppo che non ha accesso all'ambiente di produzione oppure per sostituire le autorizzazioni per un utente o un gruppo a cui è associato l'accesso:

    1.  Fare clic su **Aggiungi**, selezionare un utente o un gruppo e quindi fare clic su **OK**.

    2.  Selezionare le autorizzazioni per delegare l'utente o il gruppo per l'ambiente di produzione e quindi fare clic su **OK**.

4.  Per rimuovere tutte le autorizzazioni per l'ambiente di produzione per un utente o un gruppo, selezionare l'utente o il gruppo, fare clic su **Rimuovi**e quindi su **OK**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, è necessario disporre dell'autorizzazione **modifica sicurezza** per il dominio.

-   Le autorizzazioni per l'account del servizio Advanced Group Policy Management non possono essere modificate nella scheda **Delega produzione** .

-   Per impostazione predefinita, gli account seguenti dispongono delle autorizzazioni per i GPO nell'ambiente di produzione:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Account</th>
    <th align="left">Autorizzazioni predefinite per gli oggetti Criteri di ricerca</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;Account del servizio Advanced Group Policy Management&gt;</p></td>
    <td align="left"><p>Modificare le impostazioni, eliminare, modificare la sicurezza</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Utenti autenticati</p></td>
    <td align="left"><p>Leggere, applicare</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Amministratori di dominio</p></td>
    <td align="left"><p>Modificare le impostazioni, eliminare, modificare la sicurezza</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Amministratori aziendali</p></td>
    <td align="left"><p>Modificare le impostazioni, eliminare, modificare la sicurezza</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Controller di dominio aziendale</p></td>
    <td align="left"><p>Read</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sistema</p></td>
    <td align="left"><p>Modificare le impostazioni, eliminare, modificare la sicurezza</p></td>
    </tr>
    </tbody>
    </table>

     

-   L'appartenenza al gruppo proprietari creatori di criteri di gruppo deve essere limitata, soit non viene usata per eludere la gestione di Access a GPO per Advanced Group Policy Management. Nella console di **gestione di criteri di gruppo**fare clic su **oggetti Criteri di gruppo** nella foresta e nel dominio in cui si vogliono gestire gli oggetti GPO, fare clic su **delega**e quindi configurare le impostazioni in modo che soddisfino le esigenze dell'organizzazione.

### Riferimenti aggiuntivi

-   [Configurazione di Gestione avanzata Criteri di gruppo](configuring-advanced-group-policy-management-agpm40.md)

 

 





