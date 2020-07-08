---
title: Identificare il numero di istanze di MED-V
description: Identificare il numero di istanze di MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824256"
---
# Identificare il numero di istanze di MED-V


Devi determinare il numero di istanze di MED-V e definire l'ambito per ogni istanza in modo da poter progettare l'infrastruttura server. Un'istanza di MED-V include le operazioni seguenti:

-   Il server MED-V e le aree di lavoro MED-V archiviate nel server, incluse le autorizzazioni di Active Directory.

-   Database di SQL Server che archivia gli eventi client. Il database può essere condiviso da più istanze di MED-V.

-   Archivio immagini per le immagini di MED-V imballate. Il repository può essere condiviso da più istanze di MED-V.

-   Console di gestione utilizzata per creare e comprimere immagini e per creare aree di lavoro MED-V. La console non può essere usata contemporaneamente da più istanze di MED-V, ma può essere disconnessa da un server MED-V e quindi connessa a un altro server MED-V.

-   I client MED-V che ricevono aree di lavoro MED-V e l'autorizzazione per usarli dal server.

Le istanze di MED-V separate non possono essere integrate o condividono aree di lavoro MED-V. Di conseguenza, ogni istanza aggiuntiva decentralizza la gestione della virtualizzazione.

## Determinare il numero di istanze MED-V necessarie


Iniziare presupponendo di usare un'istanza di MED-V. Prendi in considerazione le condizioni seguenti e Aggiungi altre istanze per ogni condizione che si applica all'infrastruttura.

-   Numero di utenti supportati: ogni istanza di MED-V può supportare fino a 5.000 client attivi concorrentemente. Attiva contemporaneamente: il client è online con il server MED-V e invia i sondaggi al server per gli aggiornamenti dei criteri e delle immagini, oltre agli eventi. Se l'infrastruttura includerà più di 5.000 utenti attivi, aggiungere un'istanza per ogni utente di 5.000.

-   Utenti nei domini non attendibili: le autorizzazioni dell'area di lavoro MED-V Server associa l'attività di SharePoint con utenti e/o gruppi di Active Directory. Ciò richiede che gli utenti di MED-V siano presenti all'interno del limite di attendibilità del server MED-V. Aggiungere un'istanza MED-V per ogni gruppo di utenti MED-V che si trova in un dominio separato e non attendibile.

-   Client in reti isolate: determinare se i client si trovano in reti isolate e quindi richiedono un'istanza MED-V separata. Ad esempio, le organizzazioni spesso isolano le reti Lab dalle reti di produzione. Aggiungere un'istanza MED-V per ogni rete isolata che conterrà client MED-V.

-   Requisiti organizzativi: l'organizzazione può richiedere che un gruppo di client venga gestito da un'istanza di MED-V separata per motivi di sicurezza, ad esempio quando le applicazioni riservate vengono recapitate solo a un set limitato di utenti all'interno di un dominio. Ad esempio, il reparto retribuzioni può impedire agli utenti di altri reparti di accedere all'istanza MED-V che archivia i criteri per l'elaborazione dei salari. Inoltre, se l'organizzazione usa un modello di gestione distribuita, potrebbe essere necessaria un'istanza di MED-V separata per ogni gruppo aziendale con client MED-V per consentire al gruppo di gestire il proprio ambiente virtualizzato. Aggiungere un'istanza MED-V per ogni requisito dell'organizzazione separato.

-   Considerazioni legali: i problemi di sicurezza o di privacy nazionali e le leggi fiduciarie potrebbero richiedere la separazione di determinati dati o impedire che altri dati attraversino i confini nazionali. Se necessario, aggiungere altre istanze di MED-V per rispondere a questa esigenza.

Dopo aver determinato il numero di istanze MED-V necessarie per l'infrastruttura, nonché il ragionamento per ognuno di essi, specificare un nome per ogni istanza.

 

 





