---
title: Gestione di BitLocker con MBAM 2.5
description: Gestione di BitLocker con MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826006"
---
# Gestione di BitLocker con MBAM 2.5


Dopo aver pianificato e quindi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurarlo e usarlo per gestire la crittografia unità BitLocker in tutta l'organizzazione. Le informazioni in questa sezione illustrano le attività di gestione della crittografia di BitLocker che si verificano dopo l'installazione e che vengono eseguite con l'amministrazione e il monitoraggio di Microsoft BitLocker.

## Reimpostare un blocco TPM


Un modulo TPM (Trusted Platform Module) è un microchip progettato per ottenere funzioni di base relative alla sicurezza, che coinvolgono principalmente le chiavi di crittografia. Il TPM viene in genere installato sulla scheda madre di un computer e comunica con il resto del sistema usando una scheda bus host. Nei computer che incorporano un TPM è possibile creare chiavi crittografiche e crittografarle in modo che possano essere decrittografate solo dal TPM.

Se un utente immette il PIN errato troppe volte, può verificarsi un blocco TPM. Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino per il produttore. Puoi usare MBAM per accedere al sistema di dati di ripristino centralizzato delle chiavi nel sito Web di amministrazione e monitoraggio, in cui puoi recuperare un file di password del proprietario del TPM quando fornisci un ID computer e un Identificativo utente associato.

[Come ripristinare un blocco del TPM](how-to-reset-a-tpm-lockout-mbam-25.md)

## Recuperare le unità


Quando si ha a che fare con la crittografia dei dati, in particolare in un ambiente aziendale, valutare il modo in cui i dati possono essere recuperati in caso di errori hardware, modifiche al personale o altre situazioni in cui le chiavi di crittografia possono essere perse.

Le funzionalità di ripristino delle unità crittografate in MBAM garantiscono che i dati possano essere acquisiti e archiviati e che gli strumenti necessari siano disponibili per accedere a un volume protetto da BitLocker quando BitLocker entra in modalità di ripristino, viene spostato o viene danneggiato.

[Come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[Come recuperare un'unità spostata](how-to-recover-a-moved-drive-mbam-25.md)

[Come recuperare un'unità danneggiata](how-to-recover-a-corrupted-drive-mbam-25.md)

## Determinare lo stato di crittografia di BitLocker dei computer persi


Con MBAM puoi determinare l'ultimo stato di crittografia di BitLocker noto dei computer che sono stati persi o rubati.

[Come determinare lo stato della crittografia BitLocker nei computer smarriti](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## Usare il portale self-service per ottenere l'accesso a un computer


Se gli utenti finali si bloccano in Windows da BitLocker, possono usare le istruzioni in questa sezione per ottenere una chiave di ripristino di BitLocker per riottenere l'accesso al computer.

[Come usare il portale self-service per riottenere l'accesso a un computer](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## Argomenti correlati


[Operazioni relative a MBAM 2.5](operations-for-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





