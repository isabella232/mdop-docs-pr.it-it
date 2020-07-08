---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823345"
---
# Come recuperare un'unità spostata
Questo argomento spiega come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per recuperare un'unità del sistema operativo che è stata spostata dopo essere stata crittografata da Microsoft BitLocker Administration and Monitoring (MBAM). Quando un'unità viene spostata, non accetta più il PIN usato nel computer precedente perché è stato modificato il chip TPM (Trusted Platform Module). Per recuperare l'unità spostata, è necessario ottenere l'ID chiave di ripristino per recuperare la password di ripristino.

Per recuperare un'unità spostata, è necessario usare l'area di **recupero unità** del sito Web amministrazione e monitoraggio. Per accedere all'area di **ripristino dell'unità** , è necessario essere assegnati al ruolo degli utenti di mbam helpdesk o al ruolo di utenti avanzati helpdesk di mbam. Per altre informazioni su questi ruoli, vedere [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Per recuperare un'unità spostata**
1.  Nel computer che contiene l'unità spostata, avviare il computer in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft (DaRT).

2.  Dopo aver avviato il computer con WinRE o DaRT, MBAM tratterà l'unità di sistema operativo spostata come unità dati fissa. MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.

    **Nota**  In alcuni casi, è possibile fare clic su **ho dimenticato il pin** durante il processo di avvio e quindi immettere la modalità di ripristino per visualizzare l'ID chiave di ripristino.

     

3.  Usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità dal sito Web di amministrazione e monitoraggio. Per istruzioni, vedere [come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).

    Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, completare i passaggi aggiuntivi seguenti. In caso contrario, il processo di ripristino è completo.

4.  Dopo avere sbloccato l'unità e aver completato il processo di avvio, aprire un prompt dei comandi in modalità WinRE e usare il `manage-bde` comando per decrittografare l'unità. L'uso di questo strumento è l'unico modo per rimuovere il TPM più il PIN Protector senza il chip TPM originale. Per informazioni sul `manage-bde` comando, vedere [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).

5.  Al termine della rimozione, avviare il computer in genere. L'agente MBAM implicherà ora il criterio per crittografare l'unità con il TPM del nuovo computer più il PIN.



## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





