---
title: Attività di amministrazione per Gestione avanzata Criteri di gruppo
description: Attività di amministrazione per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822425"
---
# Attività di amministrazione per Gestione avanzata Criteri di gruppo


In Advanced Group Policy Management, un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) configura le opzioni a livello di dominio e delega le autorizzazioni per i responsabili approvazione, gli editor, i revisori e gli altri amministratori della tecnologia avanzata. Per impostazione predefinita, un amministratore della Advanced Group Policy Management è un utente con controllo completo, tutte le autorizzazioni di Advanced Group Policy Management, che può quindi eseguire attività associate a qualsiasi ruolo.

In un ambiente in cui più persone sviluppano oggetti Criteri di gruppo, è possibile scegliere se tutti gli utenti della Advanced Group Policy app eseguono le stesse attività e hanno lo stesso livello di accesso o se gli amministratori della gestione avanzata delegano le autorizzazioni agli editor che apportano modifiche a GPO e agli approvatori che distribuiscono GPO nell'ambiente di produzione. Gli amministratori della gestione avanzata possono configurare le autorizzazioni per soddisfare le esigenze dell'organizzazione.

-   [Configurazione della gestione dei criteri di gruppo avanzati](configuring-advanced-group-policy-management.md): configurare la connessione e la notifica tramite posta elettronica del server Advanced Group Policy Management, delegare l'accesso ai GPO nell'ambiente di produzione e configurare la registrazione e la traccia per la risoluzione

-   [Gestione dell'archivio](managing-the-archive.md): delegare l'accesso ai GPO nell'archivio e limitare il numero di versioni di ogni GPO archiviato.

-   [Gestione del servizio Advanced Group Policy Management](managing-the-agpm-service-agpm30ops.md): arrestare e avviare il servizio Advanced Group Policy Management o modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management o la porta in cui viene ascoltato il servizio Advanced Group Policy Management.

-   [Trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive.md): trasferire il servizio Advanced Group Policy Management, l'archivio o entrambi in un server diverso.

Inoltre, poiché il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli, un amministratore della Advanced Group Policy Management può eseguire le attività normalmente associate a qualsiasi altro ruolo.

-   [Esecuzione di attività di approvazione](performing-approver-tasks-agpm30ops.md), ad esempio la creazione, la distribuzione o l'eliminazione di GPO

-   [Esecuzione di attività dell'editor](performing-editor-tasks-agpm30ops.md), ad esempio la modifica, la ridenominazione, l'etichettatura o l'importazione di GPO, la creazione di modelli o l'impostazione di un modello predefinito

-   [Esecuzione di attività di revisore](performing-reviewer-tasks-agpm30ops.md), ad esempio la revisione delle impostazioni e il confronto degli oggetti Criteri di lavoro

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

 

 





