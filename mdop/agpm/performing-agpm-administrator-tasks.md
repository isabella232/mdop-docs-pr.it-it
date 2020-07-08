---
title: Attività di amministrazione per Gestione avanzata Criteri di gruppo
description: Attività di amministrazione per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820476"
---
# Attività di amministrazione per Gestione avanzata Criteri di gruppo


Un amministratore Advanced Group Policy Management (controllo completo) configura le opzioni a livello di dominio e delega le autorizzazioni per i responsabili approvazione, gli editor, i revisori e altri amministratori della gestione avanzata Criteri di gruppo. Per impostazione predefinita, un amministratore della Advanced Group Policy Management è un utente con controllo completo (tutte le autorizzazioni avanzate di gestione dei criteri di gruppo \ [Advanced Group Policy Manager \]) e pertanto può eseguire anche attività associate a qualsiasi ruolo.

In un ambiente in cui più persone sviluppano oggetti Criteri di gruppo, è possibile scegliere se tutti gli utenti avanzati di gestione dei criteri di gruppo eseguono le stesse attività e hanno lo stesso livello di accesso o se gli amministratori della tecnologia avanzata delegano le autorizzazioni agli editor che apportano modifiche a GPO e agli approvatori che distribuiscono GPO nell'ambiente di produzione. Gli amministratori della gestione avanzata possono configurare le autorizzazioni per soddisfare le esigenze dell'organizzazione.

-   [Configurare la connessione al server di Gestione avanzata Criteri di gruppo](configure-the-agpm-server-connection.md)

-   [Configurare la notifica di posta elettronica](configure-e-mail-notification.md)

-   [Delegare l'accesso a livello di dominio](delegate-domain-level-access.md)

-   [Delegare l'accesso a un singolo oggetto Criteri di gruppo](delegate-access-to-an-individual-gpo.md)

-   [Configurare registrazione e traccia](configure-logging-and-tracing.md)

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service.md)

    -   [Avviare e arrestare il servizio Gestione avanzata Criteri di gruppo](start-and-stop-the-agpm-service.md)

    -   [Modificare il percorso di archiviazione](modify-the-archive-path.md)

    -   [Modificare l'account del servizio Gestione avanzata Criteri di gruppo](modify-the-agpm-service-account.md)

    -   [Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo](modify-the-port-on-which-the-agpm-service-listens.md)

Inoltre, poiché il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli, un amministratore della Advanced Group Policy Management può eseguire le attività normalmente associate a qualsiasi altro ruolo.

-   [Esecuzione di attività di approvazione](performing-approver-tasks.md), ad esempio la creazione, la distribuzione o l'eliminazione di GPO

-   [Esecuzione di attività dell'editor](performing-editor-tasks.md), ad esempio la modifica, la ridenominazione, l'etichettatura o l'importazione di GPO, la creazione di modelli o l'impostazione di un modello predefinito

-   [Esecuzione di attività di revisore](performing-reviewer-tasks.md), ad esempio la revisione delle impostazioni e il confronto degli oggetti Criteri di lavoro

### Considerazioni aggiuntive

Per impostazione predefinita, il ruolo amministratore Advanced Group Policy Management ha il controllo completo, tutte le autorizzazioni per Advanced Group Policy

-   Contenuto dell'elenco

-   Impostazioni di lettura

-   Modificare le impostazioni

-   Creare un oggetto Criteri di stato

-   Distribuire un oggetto Criteri di stato

-   Elimina GPO

-   Opzioni di modifica

-   Modificare la sicurezza

-   Creare un modello

Le autorizzazioni **modifica opzioni** e **modifica sicurezza** sono univoche per il ruolo di amministratore Advanced Group Policy Management.

 

 





