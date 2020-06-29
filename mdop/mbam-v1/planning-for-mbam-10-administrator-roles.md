---
title: Pianificazione dei ruoli di amministrazione di MBAM 1.0
description: Pianificazione dei ruoli di amministrazione di MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825886"
---
# Pianificazione dei ruoli di amministrazione di MBAM 1.0


Questo argomento include e descrive i ruoli di amministratore disponibili in Microsoft BitLocker Administration and Monitoring (MBAM), nonché i percorsi del server in cui vengono creati i gruppi locali.

## Ruoli di amministratore di MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Amministratori di sistema MBAM**  
Gli amministratori di questo ruolo hanno accesso a tutte le caratteristiche di MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.

<a href="" id="---------------mbam-hardware-users"></a> **Utenti di hardware MBAM**  
Gli amministratori di questo ruolo hanno accesso alle funzionalità di funzionalità hardware di MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.

<a href="" id="---------------mbam-helpdesk-users"></a> **Utenti di MBAM helpdesk**  
Gli amministratori di questo ruolo hanno accesso alle funzionalità dell'helpdesk da MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.

<a href="" id="---------------mbam--report-users"></a> **Utenti di report MBAM**  
Gli amministratori di questo ruolo hanno accesso alla caratteristica conformità e rapporti di controllo da MBAM. Il gruppo locale per questo ruolo è installato nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo.

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **MBAM Advanced helpdesk utenti**  
Gli amministratori di questo ruolo hanno aumentato l'accesso alle funzionalità dell'helpdesk da MBAM. Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio. Se un utente è un membro di entrambi gli utenti di MBAM helpdesk e MBAM Advanced helpdesk utenti, le autorizzazioni di MBAM Advanced helpdesk utenti sovrascriveranno le autorizzazioni utente di MBAM helpdesk.

**Importante**  Per visualizzare i report, un utente di amministrazione deve essere un membro del gruppo di sicurezza degli **utenti del report mbam** nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita la funzionalità conformità e report. Come procedura consigliata, creare un gruppo di sicurezza in Active Directory con i diritti sul gruppo di sicurezza Local **report degli utenti di mbam** nel server di amministrazione e monitoraggio e nel server che ospita la conformità e i report.

 

## Argomenti correlati


[Preparazione dell'ambiente per MBAM 1.0](preparing-your-environment-for-mbam-10.md)

 

 





