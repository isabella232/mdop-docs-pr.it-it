---
title: Disponibilità elevata per MBAM 1.0
description: Disponibilità elevata per MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825365"
---
# Disponibilità elevata per MBAM 1.0


Questo argomento descrive come configurare un'installazione a elevata disponibilità di Microsoft BitLocker Administration and Monitoring (MBAM).

## Scenari di disponibilità elevata per MBAM


L'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) sono progettati per essere a tolleranza d'errore. Se un server diventa non disponibile, gli utenti non devono essere colpiti negativamente. Ad esempio, se l'agente MBAM non riesce a connettersi al server Web MBAM, gli utenti non devono essere richieste di azione.

Quando si pianifica l'installazione di MBAM, prendere in considerazione i seguenti problemi che possono influenzare la disponibilità del servizio MBAM:

-   Crittografia unità e password di ripristino: se non è possibile escrowE una password di ripristino, la crittografia non viene avviata nel computer client.

-   Caricamento dei dati sullo stato di conformità: se il server che ospita il servizio report stato conformità non è disponibile, i dati di conformità non rimarranno aggiornati.

-   Help desk Recovery Key Access-se l'help desk non può accedere alle informazioni sul database MBAM, non sarà in grado di fornire chiavi di ripristino agli utenti.

-   Disponibilità dei report: i report non saranno disponibili se il server che ospita i report di conformità e controllo non è disponibile.

La principale preoccupazione per MBAM High Availability è la disponibilità del ripristino della chiave BitLocker. Se il supporto tecnico non è in grado di fornire chiavi di ripristino, gli utenti bloccati non riescono a sbloccare i computer. Per evitare questo problema, è consigliabile implementare server Web ridondanti e database per garantire un'elevata disponibilità.

Per altre informazioni sulla scalabilità e l'elevata disponibilità di MBAM, vedi la [scalabilità di mbam white paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Per informazioni generali sull'elevata disponibilità per Microsoft SQL Server, vedere [disponibilità elevata](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .

Per indicazioni generali sulla disponibilità e scalabilità per i server Web, vedere [disponibilità e scalabilità](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## Argomenti correlati


[Manutenzione di MBAM 1.0](maintaining-mbam-10.md)

 

 





