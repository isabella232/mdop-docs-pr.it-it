---
title: Gestione di BitLocker con MBAM
description: Gestione di BitLocker con MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825895"
---
# Gestione di BitLocker con MBAM


Dopo la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare e usare MBAM per gestire la crittografia BitLocker aziendale. In questa sezione vengono illustrate le attività di gestione delle crittografazioni post-installazione, quotidiane, che possono essere eseguite tramite MBAM.

## Reimpostare un blocco TPM con MBAM


Un microchip TPM (Trusted Platform Module) offre funzioni di base relative alla sicurezza. Queste funzioni vengono eseguite principalmente dall'uso di chiavi di crittografia. Il TPM viene in genere installato sulla scheda madre di un computer o un portatile e comunica con il resto del sistema usando un bus hardware. I computer che incorporano un TPM possono creare chiavi crittografiche che possono essere decrittografate solo dal TPM. Se un utente immette un PIN errato troppo spesso, può verificarsi un blocco TPM. Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore. Il sistema di dati di ripristino chiave nel sito Web di amministrazione di MBAM consente di ottenere un file di password del proprietario del TPM reimpostato.

[Come ripristinare un blocco del TPM](how-to-reset-a-tpm-lockout-mbam-1.md)

## Recuperare le unità con MBAM


Verificare di essere in grado di provare il recupero di dati da unità crittografate in caso di errori hardware, modifiche al personale o altre situazioni in cui le chiavi di crittografia andranno perse. Le caratteristiche di ripristino delle unità crittografate di MBAM consentono di acquisire e archiviare i dati e la disponibilità di strumenti necessari per accedere a un volume protetto da BitLocker quando il volume entra in modalità di ripristino, viene spostato o viene danneggiato.

[Come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[Come recuperare un'unità spostata](how-to-recover-a-moved-drive-mbam-1.md)

[Come recuperare un'unità danneggiata](how-to-recover-a-corrupted-drive-mbam-1.md)

## Determinare lo stato di crittografia di BitLocker dei computer persi usando MBAM


Quando si usa MBAM, è possibile determinare l'ultimo stato di crittografia di BitLocker noto dei computer persi o rubati.

[Come determinare lo stato di crittografia BitLocker nei computer smarriti](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## Altre risorse per eseguire la gestione di BitLocker con MBAM


[Operazioni relative a MBAM 1.0](operations-for-mbam-10.md)

 

 





