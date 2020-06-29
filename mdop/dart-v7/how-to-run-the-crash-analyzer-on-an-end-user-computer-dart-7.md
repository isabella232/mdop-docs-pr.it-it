---
title: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823836"
---
# Come eseguire Analizzatore di arresti anomali in un computer dell'utente finale


In genere, viene eseguito Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer dalla finestra del set di strumenti di diagnostica e ripristino in un computer dell'utente finale che presenta problemi. L'analizzatore crash cerca di individuare gli strumenti di debug per Windows nel computer problema. Se la finestra di dialogo percorso directory è vuota, è necessario immettere la posizione o passare al percorso degli strumenti di debug per Windows (è possibile scaricare i file da Microsoft). Devi anche specificare il percorso in cui si trovano i file di simboli.

**Per aprire ed eseguire l'analizzatore crash in un computer dell'utente finale**

1.  Nella finestra del **set di strumenti di diagnostica e ripristino** in un computer dell'utente finale, fare clic su **analizzatore crash**.

2.  Specificare le informazioni necessarie per le operazioni seguenti:

    -   Strumenti di debug Microsoft per Windows

    -   File di simboli

        Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Un file di dump di arresto anomalo

        Seguire questa procedura per determinare la posizione del file di dump dell'arresto anomalo:

        1.  Aprire la finestra delle **proprietà del sistema** .

            Fare clic sul pulsante **Start**, digitare sysdm.cpl e quindi premere INVIO.

        2.  Fai clic sulla scheda **Avanzate**.

        3.  Nell'area di **avvio e ripristino** fare clic su **Impostazioni**.

        **Nota**  Se non si ha accesso alla finestra delle **proprietà del sistema** , è possibile cercare i file di dump nel computer dell'utente finale usando lo strumento di **ricerca** in DART.

         

3.  L' **analizzatore crash** analizza il file di dump di arresto anomalo e segnala una causa probabile dell'arresto anomalo. È possibile visualizzare altre informazioni sull'arresto anomalo, ad esempio il messaggio di arresto anomalo specifico e la descrizione, i driver caricati al momento dell'arresto anomalo e l'output completo dell'analisi.

4.  Decidere su una strategia appropriata per risolvere il problema. Questo potrebbe richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'arresto anomalo usando il nodo **Servizi e driver** dello strumento **Gestione computer** in DART.

## Argomenti correlati


[Diagnosi degli errori di sistema con Analizzatore di arresti anomali](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





