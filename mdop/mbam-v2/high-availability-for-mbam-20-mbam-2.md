---
title: Disponibilità elevata per MBAM 2.0
description: Disponibilità elevata per MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824726"
---
# Disponibilità elevata per MBAM 2.0


Questo argomento fornisce informazioni di base su un'installazione a elevata disponibilità di Microsoft BitLocker Administration and Monitoring (MBAM). Gli scenari di disponibilità elevata non sono completamente supportati in questa versione di MBAM, quindi non sono descritti qui. Si consiglia di cercare i Blog e i forum correlati, in cui gli utenti descrivono come hanno configurato correttamente l'elevata disponibilità per MBAM nei loro ambienti.

## Scenari di disponibilità elevata per MBAM


L'amministrazione e il monitoraggio di Microsoft BitLocker sono progettati per essere a tolleranza d'errore. Se un server diventa non disponibile, gli utenti non devono essere interessati negativamente. Ad esempio, se l'agente MBAM non riesce a connettersi al server Web MBAM, gli utenti non devono essere richieste di azione.

Quando si pianifica l'installazione di MBAM, prendere in considerazione gli elementi seguenti, che possono influire sulla disponibilità del servizio MBAM:

-   Crittografia unità e password di ripristino: se non è possibile escrowE una password di ripristino, la crittografia non viene avviata nel computer client.

-   Caricamento dei dati sullo stato di conformità: se il server che ospita il servizio report stato conformità non è disponibile, i dati di conformità non rimangono aggiornati.

-   Help desk Recovery Key Access-se il supporto tecnico non è in grado di accedere alle informazioni sul database MBAM, il supporto tecnico non può fornire chiavi di ripristino agli utenti.

-   Disponibilità dei report: se il server che ospita i report di conformità e controllo non è disponibile, i report non saranno disponibili.

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a>In che modo il backup di MBAM usa il servizio Copia Shadow del volume (VSS)


MBAM 2.0 offre un writer del servizio Copia Shadow del volume (VSS), denominato Microsoft BitLocker Administration and Management writer, che facilita il backup del database di conformità e audit e del database di ripristino.

Il server di Windows Installer di MBAM registra MBAM VSS writer. Qualsiasi errore durante la registrazione di VSS Writer fa sì che l'installazione di MBAM server venga ritirata. In una topologia in cui il database di conformità e controllo e il database di ripristino sono installati in server diversi, è registrata un'istanza distinta di MBAM VSS Writer in ogni server. MBAM VSS Writer dipende da SQL Server VSS writer. SQL Server VSS writer viene registrato come parte dell'installazione di Microsoft SQL Server. Qualsiasi tecnologia di backup che usa writer VSS per eseguire il backup può individuare il writer di MBAM VSS.

## Argomenti correlati


[Manutenzione di MBAM 2.0](maintaining-mbam-20-mbam-2.md)

 

 





