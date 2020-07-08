---
title: Panoramica di Gestione avanzata Criteri di gruppo
description: Panoramica di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822486"
---
# Panoramica di Gestione avanzata Criteri di gruppo


È possibile usare Advanced Group Policy Management per estendere le funzionalità della console Gestione criteri di gruppo per offrire un controllo di modifica completo e una gestione migliorata per gli oggetti Criteri di gruppo.

## Sviluppo di oggetti Criteri di gruppo con il controllo delle modifiche


Con Advanced Group Policy Management è possibile archiviare una copia di ogni oggetto Criteri di gruppo in un archivio centrale in modo che gli amministratori dei criteri di raggruppamento possano visualizzarlo e modificarlo offline senza influire immediatamente sulla versione distribuita del GPO. Inoltre, Advanced Group Policy Management archivia una copia di ogni versione di ogni GPO controllato nell'archivio in modo da poter eseguire il rollback a una versione precedente, se necessario.

I termini "Archivia" e "Estrai" vengono usati proprio come in una raccolta (o in applicazioni che includono controllo delle modifiche, controllo della versione o controllo del codice sorgente per lo sviluppo della programmazione). Per usare un libro che si trova in una raccolta, è possibile estrarlo dalla raccolta. Nessun altro utente può usarlo mentre è estratto. Dopo aver completato il libro, è possibile archiviarlo di nuovo nella raccolta, in modo che altri utenti possano usarlo.

Per usare queste funzionalità di controllo GPO, fare clic su un nodo modifica controllo nell'Editor gestione criteri di gruppo. Il nodo cambia controllo viene visualizzato solo se è stato installato il client Advanced Group Policy Management.

Quando si sviluppano GPO tramite Advanced Group Policy Management:

1.  Crea un nuovo oggetto Criteri di controllo controllato o controlla un oggetto Criteri di controllo precedentemente non controllato.

2.  Consulta il GPO, in modo che tu e solo tu possa cambiarlo.

3.  Modificare l'oggetto Criteri di stato.

4.  Archiviare il GPO modificato in modo che altri utenti possano modificarlo o in modo che possa essere distribuito.

5.  Esaminare le modifiche.

6.  Distribuire il GPO nell'ambiente di produzione.

## Delega basata sui ruoli


Advanced Group Policy Management offre una delega basata sui ruoli completa e di facile utilizzo per la gestione dell'accesso ai GPO nell'archivio. Le autorizzazioni a livello di dominio consentono agli amministratori della gestione avanzata di fornire l'accesso a singoli domini senza consentire l'accesso ad altri domini. La delega basata su GPO consente agli amministratori della Advanced Group Policy di fornire l'accesso a GPO specifici senza fornire accesso a livello di dominio.

In Advanced Group Policy Management sono presenti ruoli definiti in modo specifico: amministratore Advanced Group Policy Management (controllo completo), approvatore, editor e revisore. Il ruolo amministratore Advanced Group Policy Management include le autorizzazioni per tutti gli altri ruoli. Per impostazione predefinita, solo i responsabili approvazione hanno la possibilità di distribuire GPO nell'ambiente di produzione di un dominio, proteggendo l'ambiente dagli errori degli editori meno esperti. Anche per impostazione predefinita, tutti i ruoli includono il ruolo revisore e quindi la possibilità di visualizzare le impostazioni GPO nei report. Tuttavia, Advanced Group Policy Management offre a un amministratore della Advanced Group Policy la flessibilità di personalizzare l'accesso degli oggetti Criteri di gestione per soddisfare le esigenze dell'organizzazione.

## Delega in un ambiente di amministrazione di più criteri di gruppo


In un ambiente in cui più persone modificano gli oggetti Criteri di gruppo, un amministratore della gestione avanzata delega l'autorizzazione per gli editor, i responsabili approvazione e i revisori, come gruppi o come singoli utenti. Per un processo di sviluppo GPO tipico per un editor e un responsabile approvazione, vedere [elenco di controllo: creare, modificare e distribuire un oggetto Criteri](checklist-create-edit-and-deploy-a-gpo-agpm40.md)di ricerca.

### Riferimenti aggiuntivi

-   [Gestione avanzata Criteri di gruppo 4.0](advanced-group-policy-management-40.md)

 

 





