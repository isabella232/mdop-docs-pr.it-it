---
title: Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti
description: Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825696"
---
# Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti


Microsoft BitLocker Administration and Monitoring (MBAM) include quattro ruoli del server che possono essere eseguiti in uno o più computer. Tuttavia, solo due funzionalità di MBAM server richiedono l'aggiornamento per supportare l'installazione della versione del linguaggio MBAM 1,0 e il modello di criteri di mbam. In configurazioni con le funzionalità di MBAM Server installate in più computer, è necessario aggiornare solo le funzionalità del server seguenti:

-   I report di controllo e conformità di MBAM

-   Il server di amministrazione e monitoraggio di MBAM

**Importante**  Le caratteristiche del server MBAM devono essere aggiornate in questo ordine: i report di conformità e controllo prima e quindi il server di amministrazione e monitoraggio. I modelli di criteri di gruppo di MBAM possono essere aggiornati in qualsiasi momento senza problemi di sequenza.

 

**Per installare l'aggiornamento della lingua MBAM nella funzionalità MBAM Compliance and audit report server**

1.  Nel computer che esegue la funzionalità MBAM Compliance and audit report individuare ed eseguire la configurazione guidata aggiornamento lingua MBAM (MBAMsetup.exe).

2.  Completare la procedura guidata per i report di conformità e controllo e quindi chiudere la procedura guidata.

**Per installare l'aggiornamento della lingua MBAM nella funzionalità MBAM Administration and Monitoring Server**

1.  Nel computer in cui è in uso la funzionalità di amministrazione e monitoraggio di MBAM aprire la console di gestione di Internet Information Services (IIS), accedere a **siti**e quindi arrestare il sito Web di amministrazione e monitoraggio di Microsoft BitLocker.

2.  Scegliere di modificare i binding per il sito Web di MBAM e quindi modificare i binding del sito. Ad esempio, cambia la porta da 443 a 9443.

3.  Individuare ed eseguire la configurazione guidata aggiornamento lingua MBAM (MBAMsetup.exe). Completare la procedura guidata per la funzionalità di amministrazione e monitoraggio Server e quindi chiudere la procedura guidata.

4.  Dopo aver aggiornato il database del server, aprire la console di gestione di IIS ed esaminare i binding del sito Web di amministrazione e monitoraggio di Microsoft BitLocker.

5.  Eliminare il binding precedente e verificare che il binding rimanente abbia il nome host, il certificato e il numero di porta corretti per la configurazione di MBAM Enterprise.

6.  Riavviare il sito Web di MBAM.

7.  Testare la funzionalità del sito Web MBAM:

    -   Aprire l'interfaccia Web di MBAM e verificare che sia possibile ottenere una chiave di ripristino per un client.

    -   Applicare la crittografia di un computer client nuovo o decrittografato manualmente.

        **Nota**  Il client MBAM si apre solo se può comunicare con il database di ripristino e hardware.

         

## Argomenti correlati


[Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





