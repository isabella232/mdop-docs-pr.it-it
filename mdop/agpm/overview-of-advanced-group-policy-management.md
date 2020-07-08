---
title: Panoramica di Gestione avanzata Criteri di gruppo
description: Panoramica di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822485"
---
# Panoramica di Gestione avanzata Criteri di gruppo


È possibile usare Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo, garantendo un controllo completo delle modifiche e una gestione avanzata per gli oggetti Criteri di gruppo.

## Sviluppo di oggetti Criteri di gruppo con il controllo delle modifiche


Con Advanced Group Policy Management è possibile archiviare una copia di ogni oggetto Criteri di gruppo in un archivio centrale, in modo che gli amministratori di Group Policy possano visualizzarlo e modificarlo offline senza influire immediatamente sulla versione distribuita del GPO. Inoltre, Advanced Group Policy Management archivia una copia di ogni versione di ogni GPO controllato nell'archivio in modo da poter eseguire il rollback a una versione precedente, se necessario.

I termini "Archivia" e "Estrai" vengono usati in modo molto simile a quanto avviene in una raccolta (o in applicazioni che includono il controllo delle modifiche, il controllo della versione o il controllo del codice sorgente per lo sviluppo della programmazione). Per usare un libro che si trova in una raccolta, è possibile estrarlo dalla raccolta. Nessun altro utente può usarlo mentre è estratto. Dopo aver completato il libro, è possibile archiviarlo di nuovo nella raccolta, in modo che altri utenti possano usarlo.

Durante lo sviluppo di GPO tramite Advanced Group Policy Management:

1.  Crea un nuovo oggetto Criteri di controllo controllato o controlla un oggetto Criteri di controllo precedentemente non controllato.

2.  Controlla l'oggetto Criteri di stato, quindi puoi modificarlo solo tu.

3.  Modificare l'oggetto Criteri di stato.

4.  Archiviare il GPO modificato, in modo che altri utenti possano modificarlo o in modo che possa essere distribuito.

5.  Esaminare le modifiche.

6.  Distribuire il GPO nell'ambiente di produzione.

## Delega basata sui ruoli


Advanced Group Policy Management offre una delega basata sui ruoli completa e di facile utilizzo. Le autorizzazioni a livello di dominio consentono agli amministratori della gestione avanzata utenti di consentire l'accesso a singoli domini senza consentire l'accesso ad altri domini. La delega basata su GPO consente agli amministratori della gestione avanzata Criteri di consentire l'accesso solo a GPO specifici.

In Advanced Group Policy Management sono presenti ruoli definiti in modo specifico: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore. Il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli. Per impostazione predefinita, solo i responsabili approvazione hanno la possibilità di distribuire GPO nell'ambiente di produzione, proteggendo l'ambiente da errori accidentali da parte di editor meno esperti. Anche per impostazione predefinita, tutti i ruoli includono il ruolo revisore e quindi la possibilità di visualizzare le impostazioni GPO nei report. Tuttavia, Advanced Group Policy Management offre a un amministratore della Advanced Group Policy la flessibilità di personalizzare l'accesso degli oggetti Criteri di gestione per soddisfare le esigenze dell'organizzazione.

## Delega in un ambiente di amministrazione di più criteri di gruppo


In un ambiente in cui più utenti modificano gli oggetti Criteri di gruppo, un amministratore della gestione avanzata delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori, come gruppi o come singoli utenti. Per un processo di sviluppo GPO tipico per un editor e un responsabile approvazione, vedere [elenco di controllo: creare, modificare e distribuire un oggetto Criteri](checklist-create-edit-and-deploy-a-gpo.md)di ricerca.

### Riferimenti aggiuntivi

-   [Elenco di controllo: Creare, modificare e distribuire un oggetto Criteri di gruppo](checklist-create-edit-and-deploy-a-gpo.md)

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

-   [Attività dell'editor](performing-editor-tasks.md)

-   [Attività del responsabile approvazione](performing-approver-tasks.md)

-   [Attività del revisore](performing-reviewer-tasks.md)

-   [Risoluzione dei problemi di Gestione avanzata Criteri di gruppo](troubleshooting-advanced-group-policy-management.md)

-   [Interfaccia utente: Gestione avanzata Criteri di gruppo](user-interface-advanced-group-policy-management.md)

 

 





