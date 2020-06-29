---
title: Attività di amministrazione per Gestione avanzata Criteri di gruppo
description: Attività di amministrazione per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822416"
---
# Attività di amministrazione per Gestione avanzata Criteri di gruppo


Gestione avanzata Criteri di gruppo consente a un amministratore Advanced Group Policy Management (controllo completo) di configurare le opzioni a livello di dominio e di delegare le autorizzazioni per i responsabili approvazione, gli editor, i revisori e gli amministratori dell'organizzazione avanzata. Per impostazione predefinita, un amministratore Advanced Group Policy Management è un utente che ha il controllo completo, tutte le autorizzazioni di Advanced Group Policy Management, e che può quindi eseguire attività associate a qualsiasi ruolo.

In un ambiente in cui più persone sviluppano oggetti Criteri di gruppo (GPO) è possibile scegliere di consentire a tutti gli amministratori dei criteri di gruppo di eseguire le stesse attività e di avere lo stesso livello di accesso. In alternativa, puoi scegliere di consentire agli amministratori della gestione avanzata di delegare le autorizzazioni agli editor che possono modificare gli oggetti Criteri di gruppo e agli approvatori che distribuiscono GPO nell'ambiente di produzione. Gli amministratori della gestione avanzata possono configurare le autorizzazioni per soddisfare le esigenze dell'organizzazione.

-   [Configurazione della gestione dei criteri di gruppo avanzati](configuring-advanced-group-policy-management-agpm40.md): configurare la connessione e la notifica tramite posta elettronica del server Advanced Group Policy Management, delegare l'accesso ai GPO nell'ambiente di produzione e configurare la registrazione e la traccia per la risoluzione

-   [Gestione dell'archivio](managing-the-archive-agpm40.md): delegare l'accesso ai GPO nell'archivio, limitare il numero di versioni di ogni GPO archiviato, importare un oggetto Criteri di un altro dominio ed eseguire il backup e il ripristino dell'archivio.

-   [Gestione del servizio Advanced Group Policy Management](managing-the-agpm-service-agpm40.md): arrestare e avviare il servizio Advanced Group Policy Management o modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management o la porta in cui viene ascoltato il servizio Advanced Group Policy Management.

-   [Trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive-agpm40.md): trasferire il servizio Advanced Group Policy Management, l'archivio o entrambi in un server diverso.

**Nota**  Poiché il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli, un amministratore Advanced Group Policy Management può eseguire le attività in genere associate a qualsiasi altro ruolo.

[Esecuzione di attività di approvazione](performing-approver-tasks-agpm40.md), ad esempio la creazione, la distribuzione o l'eliminazione di GPO

[Esecuzione di attività dell'editor](performing-editor-tasks-agpm40.md), ad esempio la modifica, la ridenominazione, l'etichettatura o l'importazione di GPO, la creazione di modelli o l'impostazione di un modello predefinito

[Esecuzione di attività di revisore](performing-reviewer-tasks-agpm40.md), ad esempio la revisione delle impostazioni e il confronto degli oggetti Criteri di lavoro

 

### Considerazioni aggiuntive

Per impostazione predefinita, il ruolo amministratore Advanced Group Policy Management ha il controllo completo, tutte le autorizzazioni per Advanced Group Policy

-   Contenuto dell'elenco

-   Impostazioni di lettura

-   Modificare le impostazioni

-   Creare un oggetto Criteri di stato

-   Distribuire un oggetto Criteri di stato

-   Elimina GPO

-   Esporta GPO

-   Importa oggetto Criteri di stato

-   Creare un modello

-   Opzioni di modifica

-   Modificare la sicurezza

Le autorizzazioni **modifica opzioni** e **modifica sicurezza** sono univoche per il ruolo di amministratore Advanced Group Policy Management.

 

 





