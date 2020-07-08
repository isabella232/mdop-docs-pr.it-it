---
title: Come installare il modello Criteri di gruppo di MBAM 2.0
description: Come installare il modello Criteri di gruppo di MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826255"
---
# Come installare il modello Criteri di gruppo di MBAM 2.0


Oltre alle caratteristiche di amministrazione e monitoraggio Microsoft BitLocker correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo per l'amministrazione e il monitoraggio di Microsoft BitLocker. Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o gestione avanzata Criteri di gruppo.

I passaggi seguenti descrivono come installare il modello dei criteri di gruppo di MBAM.

**Nota**  Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.

 

**Per installare il modello dei criteri di gruppo di MBAM**

1.  Nel server in cui si vuole installare MBAM eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Per impostazione predefinita, tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker sono selezionate per l'installazione. Deselezionare tutte le opzioni di funzionalità tranne il **modello di criteri**e quindi fare clic su **Avanti** per continuare l'installazione.

    **Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Dopo aver soddisfatto tutti i prerequisiti, l'installazione verrà ripresa.

     

5.  Per istruzioni specifiche su come e dove installare i modelli, vedere [come scaricare e distribuire i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://technet.microsoft.com/library/dn659707.aspx).

6.  Dopo aver visualizzato la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker per le caratteristiche selezionate, fare clic su **fine** per chiudere la configurazione di mbam.

## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





