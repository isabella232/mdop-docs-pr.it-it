---
title: Come gestire i ruoli di amministrazione di MBAM
description: Come gestire i ruoli di amministrazione di MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825116"
---
# Come gestire i ruoli di amministrazione di MBAM


Dopo che la configurazione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) è stata completata per tutte le funzionalità del server, agli utenti amministrativi dovrà essere concesso l'accesso. Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di amministrazione e monitoraggio di Microsoft BitLocker devono essere assegnati ai gruppi di sicurezza dei servizi di dominio e quindi tali gruppi devono essere aggiunti al gruppo di amministrazione locale di MBAM appropriato.

**Per gestire le appartenenze al ruolo di amministratore di MBAM**

1.  Assegnare utenti amministrativi ai gruppi di sicurezza in servizi di dominio di ActiveDirectory.

2.  Aggiungere gruppi di sicurezza di ActiveDirectory ai ruoli per MBAM Administrative Groups Local sul server MBAM per le rispettive caratteristiche.

    -   Gli **amministratori di sistema di mbam** hanno accesso a tutte le caratteristiche di MBAM nel sito Web di amministrazione e monitoraggio di mbam.

    -   **Gli utenti di mbam helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione e monitoraggio di mbam, ma devono compilare tutti i campi quando usano un'opzione qualsiasi.

    -   **Report mbam gli utenti** possono accedere ai report di conformità e controllo nel sito Web di amministrazione e monitoraggio di mbam.

    -   **Gli utenti di mbam Advanced helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione e monitoraggio di mbam, ma non sono obbligati a compilare tutti i campi quando usano un'opzione qualsiasi.

    Per altre informazioni sui ruoli per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [pianificazione dei ruoli di amministratore di MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





