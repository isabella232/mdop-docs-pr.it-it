---
title: Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0
description: Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804516"
---
# Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0


Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 Language release è un aggiornamento di MBAM che include il supporto di nuove lingue. Le nuove lingue sono:

-   Inglese (en-US)

-   Francese (FR)

-   Italiano (it)

-   Tedesco (de)

-   Spagnolo (es)

-   Coreano (KO)

-   Giapponese (ja)

-   Portoghese brasiliano (PT-BR)

-   Russo (RU)

-   Cinese tradizionale (ZH-TW)

-   Cinese semplificato (zh-CN)

L'aggiornamento della lingua MBAM 1.0 cambierà il numero di versione da MBAM 1.0.1237.1 a MBAM 1.0.2001.

Non è necessario reinstallare tutte le funzionalità di MBAM per aggiungere altre lingue. Questo argomento definisce i passaggi necessari per aggiungere le lingue appena supportate.

## Distribuire la versione di MBAM International per le funzionalità del server MBAM


Per iniziare, è necessario aggiornare le caratteristiche seguenti del server MBAM:

-   Report di conformità e controllo

-   Server di amministrazione e monitoraggio

-   Modelli di criteri

Devi quindi eseguire **MbamSetup.exe** per aggiornare le funzionalità di mbam eseguite nello stesso server contemporaneamente.

[Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## Installare l'aggiornamento della lingua MBAM per i criteri di gruppo


I modelli di criteri di gruppo di MBAM possono essere installati in ogni workstation di gestione oppure possono essere copiati nell'archivio centrale di criteri di gruppo, in modo da rendere disponibili i modelli per tutti gli amministratori dei criteri di gruppo. I modelli di criteri non possono essere installati direttamente in un controller di dominio. Se non si usa un archivio centrale di criteri di gruppo, è necessario copiare i criteri manualmente in ogni controller di dominio che gestisce i criteri di gruppo di MBAM.

Per aggiungere i modelli dei criteri di linguaggio di MBAM, copiare i file di lingua dei criteri di gruppo da%SystemRoot%\\PolicyDefinitions nel computer in cui è stato installato il ruolo "modelli di criteri" nella stessa posizione nel computer della workstation. Ecco alcuni esempi di file di criteri di gruppo:

-   BitLockerManagement. admx

-   BitLockerUserManagement. admx

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   fr-fr\\ BitLockerManagement. adml

-   fr-fr\\ BitLockerUserManagement. adml

-   (e similmente per ogni lingua supportata)

## Problemi noti della versione di MBAM International


Questo argomento contiene problemi noti per l'amministrazione e il monitoraggio delle versioni internazionali di Microsoft BitLocker.

[Problemi noti nella versione internazionale di MBAM](known-issues-in-the-mbam-international-release-mbam-1.md)

## Altre risorse per la distribuzione dell'aggiornamento della lingua MBAM 1,0


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)

 

 





