---
title: Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo
description: Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818986"
---
# Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo


Per impostazione predefinita, le notifiche tramite posta elettronica inviate a causa di azioni in Advanced Group Policy Management non vengono crittografate e vengono inviate tramite la porta SMTP 25. Tuttavia, puoi configurare la sicurezza della posta elettronica per Advanced Group Policy Management usando le impostazioni del registro di sistema per specificare se usare la crittografia SSL (Secure Sockets Layer) e la porta SMTP da usare.

Crittografando le notifiche tramite posta elettronica Advanced Group Policy Management, è possibile proteggere meglio quelle che potrebbero rivelare informazioni riservate sulla sicurezza dell'organizzazione. È consigliabile crittografare le notifiche tramite posta elettronica quando vengono inoltrate tramite server di posta remoti e possono essere richieste da alcune normative di conformità.

**Attenzione**  La modifica in modo non corretto del registro di sistema può danneggiare gravemente il computer. Prima di apportare modifiche al registro di sistema, è consigliabile eseguire il backup di tutti i dati valutati nel computer.

 

Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente che disponga delle autorizzazioni necessarie in Advanced Group Policy Management è necessario per completare queste procedure. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per configurare la sicurezza della posta elettronica per Advanced Group Policy con preferenze di criteri di gruppo**

1.  Nell'albero della **console Gestione criteri di gruppo** modificare un GPO applicato a tutti i server Advanced Group Policy Management per cui si vuole configurare la sicurezza della posta elettronica. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.

2.  Nella finestra **Editor gestione criteri di gruppo** espandere la **configurazione del computer**, le **Preferenze**, **le impostazioni di Windows**e le cartelle **del registro di sistema** .

3.  Nell'albero della console fare clic con il pulsante destro del mouse su **Registro**, scegliere **nuovo**, fare clic su **elemento raccolta**e quindi digitare **sicurezza della posta elettronica Advanced Group Policy Management**.

4.  Creare un elemento preferenza del registro di sistema per attivare la crittografia:

    1.  Nell'albero della console fare clic con il pulsante destro del mouse sulla **sicurezza della posta elettronica avanzata**, scegliere **nuovo**e quindi **elemento del registro di sistema**.

    2.  Nella finestra di dialogo **nuove proprietà del registro di sistema** selezionare l'azione di **aggiornamento** .

    3.  Per **hive**selezionare **HKEY \ _LOCAL \ _MACHINE**.

    4.  Per il **percorso chiave**digitare **SOFTWARE\\Microsoft\\AGPM**.

    5.  Per **nome valore**digitare **EncryptSmtp**.

    6.  Per **tipo di valore**selezionare **reg \ _DWORD**.

    7.  Per **base**selezionare **decimale**e per **i dati di valore**digitare **1** per usare la crittografia SSL oppure **0** per consentire l'invio della posta elettronica senza crittografia. Per impostazione predefinita, il messaggio di posta elettronica viene inviato senza crittografia.

    8.  Fai clic su **OK**.

5.  Creare un elemento preferenza del registro di sistema per specificare la porta SMTP:

    1.  Nell'albero della console fare clic con il pulsante destro del mouse sulla **sicurezza della posta elettronica avanzata**, scegliere **nuovo**e quindi **elemento del registro di sistema**.

    2.  Nella finestra di dialogo **nuove proprietà del registro di sistema** selezionare l'azione di **aggiornamento** .

    3.  Per **hive**selezionare **HKEY \ _LOCAL \ _MACHINE**.

    4.  Per la finestra di dialogo **percorso chiave** digitare **SOFTWARE\\Microsoft\\AGPM**.

    5.  Per **nome valore**digitare **SmtpPort**.

    6.  Per **tipo di valore**selezionare **reg \ _DWORD**.

    7.  Per **base**selezionare **decimale**e per i **dati di valore**digitare un numero di porta per la porta SMTP. Per impostazione predefinita, la porta SMTP è la porta 25 se la crittografia non è abilitata o porta 587 se è abilitata la crittografia SSL.

    8.  Fai clic su **OK**.

6.  Chiudere la finestra **Editor gestione criteri di gruppo** e quindi archiviare e distribuire il GPO. Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca.

### Considerazioni aggiuntive

-   È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per configurare le impostazioni del registro di sistema usando le preferenze dei criteri di raggruppamento. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm30ops.md) .

### Riferimenti aggiuntivi

-   [Configurazione di Gestione avanzata Criteri di gruppo](configuring-advanced-group-policy-management.md)

 

 





