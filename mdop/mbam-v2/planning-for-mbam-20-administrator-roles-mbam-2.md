---
title: Pianificazione dei ruoli di amministrazione di MBAM 2.0
description: Pianificazione dei ruoli di amministrazione di MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824895"
---
# Pianificazione dei ruoli di amministrazione di MBAM 2.0


Questo argomento elenca e descrive i ruoli di amministratore disponibili disponibili in Microsoft BitLocker Administration and Monitoring (MBAM), nonché i percorsi del server in cui vengono creati i gruppi locali.

## Ruoli di amministratore di MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Amministratori di sistema MBAM**  
Gli amministratori di questo ruolo hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.

<a href="" id="---------------mbam-helpdesk-users"></a> **Utenti di MBAM helpdesk**  
Gli amministratori di questo ruolo hanno accesso alle funzionalità dell'help desk di MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.

<a href="" id="---------------mbam-report-users"></a> **Utenti di report MBAM**  
Gli amministratori di questo ruolo hanno accesso ai report di conformità e controllo di MBAM. Il gruppo locale per questo ruolo è installato nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **MBAM Advanced helpdesk utenti**  
Gli amministratori in questo ruolo hanno aumentato l'accesso alle funzionalità dell'help desk di MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio. Se un utente è un membro di entrambi gli utenti di MBAM helpdesk e MBAM Advanced helpdesk utenti, le autorizzazioni di MBAM Advanced helpdesk utenti eseguiranno l'override delle autorizzazioni utente di MBAM helpdesk.

**Importante**  Per visualizzare i report, un utente di amministrazione deve essere un membro del gruppo di sicurezza degli **utenti del report mbam** nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita la funzionalità report di conformità e controllo. Come procedura consigliata, creare un gruppo di sicurezza in servizi di dominio Active Directory con diritti sul gruppo di sicurezza Local **report degli utenti di mbam** nel server di amministrazione e monitoraggio e nel server che ospita i report di conformità e controllo.

 

## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





