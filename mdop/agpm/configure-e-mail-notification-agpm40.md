---
title: Configurare la notifica di posta elettronica
description: Configurare la notifica di posta elettronica
author: dansimp
ms.assetid: 06f19556-f296-4a80-86a4-4f446c992204
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b751a49d3d22f893c420be7fef9714b242d1f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818996"
---
# Configurare la notifica di posta elettronica


Quando un editor o un revisore tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo, una richiesta di questa azione viene inviata a un indirizzo di posta elettronica o indirizzi designati in modo che un responsabile approvazione possa valutare la richiesta e implementarla o negarla. Puoi determinare l'indirizzo di posta elettronica o gli indirizzi a cui vengono inviate le notifiche, nonché l'alias da cui vengono inviate le notifiche.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .

3.  Nel campo **da indirizzo di posta elettronica** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.

4.  Nel campo **indirizzo di posta elettronica** Digitare un elenco delimitato da virgole di indirizzi di posta elettronica dei responsabili approvazione che devono ricevere le richieste di approvazione.

5.  Nel campo **server SMTP** Digitare un server di posta SMTP valido.

6.  Nei campi **nome utente** e **password** digitare le credenziali di un utente con accesso al servizio SMTP.

7.  Fai clic su **Applica**.

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, devi avere il **contenuto dell'elenco** e modificare le autorizzazioni di **Opzioni** per il dominio.

-   La notifica tramite posta elettronica per Advanced Group Policy Management è un'impostazione a livello di dominio. È possibile specificare gli indirizzi di posta elettronica di approvazione o gli alias di posta elettronica della gestione avanzata nella scheda **delega** di ogni dominio oppure usare gli stessi indirizzi di posta elettronica in tutto l'ambiente.

-   Per impostazione predefinita, i messaggi di posta elettronica inviati come risultato di azioni in Advanced Group Policy Management non sono crittografati. Puoi tuttavia configurare la sicurezza della posta elettronica per Advanced Group Policy Management usando le impostazioni del registro di sistema per specificare se usare la crittografia SSL (Secure Sockets Layer) e la porta SMTP da usare. Per altre informazioni, vedere [configurare la sicurezza della posta elettronica per Advanced Group Policy Management](configure-e-mail-security-for-agpm-agpm40.md).

### Riferimenti aggiuntivi

-   [Configurazione di Gestione avanzata Criteri di gruppo](configuring-advanced-group-policy-management-agpm40.md)

 

 





