---
title: Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo
description: Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824755"
---
# Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo


Microsoft BitLocker Administration and Monitoring (MBAM) include quattro ruoli del server che possono essere eseguiti in uno o più computer. Tuttavia, solo due funzionalità di MBAM server richiedono l'aggiornamento per supportare l'installazione della versione del linguaggio MBAM 1,0 e il modello di criteri di mbam. Per aggiornare tutte e tre le funzionalità di MBAM necessarie per l'installazione in un computer, eseguire i passaggi descritti in questo argomento.

**Per installare l'aggiornamento della lingua MBAM in un singolo server**

1.  Aprire la console di gestione di Internet Information Services (IIS), accedere a **siti**e quindi arrestare il sito Web di amministrazione e monitoraggio di Microsoft BitLocker.

2.  Modificare i binding per il sito Web di MBAM e quindi modificare temporaneamente i binding del sito. Ad esempio, cambia la porta da 443 a 9443.

3.  Individuare ed eseguire la configurazione guidata di MBAM (MBAMsetup.exe) e selezionare le tre caratteristiche seguenti:

    1.  Report di conformità e controllo

    2.  Server di amministrazione e monitoraggio

    3.  Modelli di criteri di gruppo

    **Importante**  Le caratteristiche del server MBAM devono essere aggiornate nell'ordine seguente: report di conformità e controllo prima, quindi Amministrazione e monitoraggio Server. I modelli di criteri di gruppo possono essere aggiornati in qualsiasi momento senza problemi di sequenza.

     

4.  Dopo aver aggiornato il database del server, aprire la console di gestione di IIS ed esaminare i binding del sito Web di amministrazione e monitoraggio di Microsoft BitLocker.

5.  Eliminare uno dei binding e verificare che il binding rimanente abbia il nome host, il certificato e il numero di porta corretti per la configurazione di MBAM Enterprise.

6.  Riavviare il sito Web di MBAM.

7.  Testare la funzionalità del sito Web MBAM:

    -   Aprire l'interfaccia Web di MBAM e verificare che sia possibile recuperare una chiave di ripristino per un client.

    -   Applicare la crittografia di un computer client nuovo o decrittografato manualmente.

        **Nota**  Il client MBAM si apre solo se può comunicare con il database di ripristino e hardware.

         

## Argomenti correlati


[Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





