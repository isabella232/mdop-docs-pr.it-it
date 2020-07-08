---
title: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824366"
---
# Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale


Per eseguire l' **analizzatore crash** dalla finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale in cui si verificano problemi, è necessario che siano installati gli strumenti di debug Microsoft per Windows e i file di simboli. Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=266248).

**Per eseguire l'analizzatore crash in un computer dell'utente finale**

1.  Nella finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale, fare clic su **analizzatore crash**.

2.  Fornisci le informazioni necessarie per gli strumenti di debug Microsoft per Windows.

3.  Fornisci le informazioni necessarie per i file di simboli. Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).

4.  Fornisci le informazioni necessarie per un file di dump della memoria. Per determinare la posizione del file di dump della memoria:

    1.  Aprire la finestra delle **proprietà del sistema** .

    2.  Fare clic sul pulsante **Start**, digitare **sysdm.cpl**e quindi premere **invio**.

    3.  Fai clic sulla scheda **Avanzate**.

    4.  Nell'area di **avvio e ripristino** fare clic su **Impostazioni**.

        Se non si ha accesso alla finestra delle **proprietà del sistema** , è possibile cercare i file di dump nel computer dell'utente finale usando lo strumento di **ricerca** in Microsoft Diagnostics and Recovery Toolset (DART) 8,0.

    L' **analizzatore crash** analizza il file di dump della memoria e segnala una causa probabile del problema. È possibile visualizzare altre informazioni sull'errore, ad esempio il messaggio di dump della memoria specifico e la descrizione, i driver caricati al momento dell'errore e l'output completo dell'analisi.

5.  Identificare la strategia appropriata per risolvere il problema. La strategia può richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'errore usando il nodo **Servizi e driver** dello strumento **Gestione Computer** in DaRT 8,0.

## Argomenti correlati


[Diagnosi degli errori di sistema con Analizzatore di arresti anomali](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[Operazioni relative a DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





