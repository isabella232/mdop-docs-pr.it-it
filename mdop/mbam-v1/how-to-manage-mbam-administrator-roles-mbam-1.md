---
title: Come gestire i ruoli di amministrazione di MBAM
description: Come gestire i ruoli di amministrazione di MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804624"
---
# Come gestire i ruoli di amministrazione di MBAM


Dopo la configurazione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso a queste funzionalità del server. Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati a gruppi di sicurezza di Active Directory e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.

**Per gestire le appartenenze al ruolo di amministratore di MBAM**

1.  Assegnare utenti amministrativi ai gruppi di sicurezza in Servizi ActiveDirectoryDomain.

2.  Aggiungere gruppi di sicurezza di ActiveDirectoryDomain Services ai ruoli per MBAM Administrative Groups Local nel server di amministrazione e monitoraggio di Microsoft BitLocker per le rispettive funzionalità. I ruoli utente sono i seguenti:

    -   Gli **amministratori di sistema di mbam** hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker nel sito Web di amministrazione di mbam.

    -   **Gli utenti di mbam hardware** hanno accesso alle funzionalità di compatibilità hardware nel sito Web di amministrazione di mbam.

    -   **Gli utenti di mbam helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione di mbam, ma devono compilare tutti i campi quando usano un'opzione qualsiasi.

    -   **Report mbam gli utenti** possono accedere ai report di conformità e controllo nel sito Web di amministrazione di mbam.

    -   **Mbam Advanced helpdesk USA** consente di accedere alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione di mbam. Questi utenti non sono tenuti a compilare tutti i campi quando usano un'opzione qualsiasi.

    Per altre informazioni sui ruoli per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)

 

 





